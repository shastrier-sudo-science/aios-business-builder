# PropBot — Client Build Spec

Status: Portfolio reference build (pre-sale demo, becomes template for real estate clients)
Spec locked: 2026-06-13
Reference builds: All Fours (Firebase multiplayer), PREDICT (Monte Carlo engine), SOVEREIGN (Supabase system_state pattern)

---

## 1. Feature List (locked, 5 items max)

1. **Listing Content Generator** — input property details (address, beds, baths, sqft, features, tone), output 3 listing description variations
2. **Social Media Caption Generator** — output 5 captions with hashtags, tailored to the property
3. **Brand Voice Memory** — user saves a tone description + example sentence once; every generation applies it automatically
4. **Usage Limiter** — free tier capped at 10 generations/month, enforced server-side
5. **One-click export** — copy to clipboard

Everything else (MLS formatting, multi-voice teams, referral systems) is Phase 2. Not in v1.

## 2. Data Model (Supabase, RLS on every table)

Reference: SOVEREIGN's `owner_config` + `is_owner()` SECURITY DEFINER pattern, idempotent migrations.

```sql
-- USERS (extends Supabase Auth)
CREATE TABLE IF NOT EXISTS users (
    id UUID PRIMARY KEY REFERENCES auth.users(id) ON DELETE CASCADE,
    email TEXT UNIQUE NOT NULL,
    stripe_customer_id TEXT,
    plan TEXT DEFAULT 'free',
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- BRAND VOICES
CREATE TABLE IF NOT EXISTS brand_voices (
    id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
    user_id UUID NOT NULL REFERENCES users(id) ON DELETE CASCADE,
    tone_description TEXT NOT NULL,
    example_sentence TEXT NOT NULL,
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- USAGE LOGS
CREATE TABLE IF NOT EXISTS usage_logs (
    id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
    user_id UUID NOT NULL REFERENCES users(id) ON DELETE CASCADE,
    generation_count INTEGER NOT NULL DEFAULT 0,
    date DATE NOT NULL,
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
    UNIQUE (user_id, date)
);

CREATE INDEX IF NOT EXISTS idx_brand_voices_user_id ON brand_voices(user_id);
CREATE INDEX IF NOT EXISTS idx_usage_logs_user_id ON usage_logs(user_id);
CREATE INDEX IF NOT EXISTS idx_usage_logs_date ON usage_logs(date);
```

**RLS policy summary** (every table, drop-before-create):
```sql
DROP POLICY IF EXISTS "own_data_only" ON brand_voices;
CREATE POLICY "own_data_only" ON brand_voices
  FOR ALL USING (auth.uid() = user_id);

DROP POLICY IF EXISTS "own_data_only" ON usage_logs;
CREATE POLICY "own_data_only" ON usage_logs
  FOR ALL USING (auth.uid() = user_id);

DROP POLICY IF EXISTS "own_data_only" ON users;
CREATE POLICY "own_data_only" ON users
  FOR ALL USING (auth.uid() = id);
```

No table is publicly writable. Usage counter increments happen via a Supabase RPC function (`check_and_increment_usage`), not direct table writes — prevents users resetting their own limits via the REST API (see safety doc, rate-limiting section).

## 3. Hosting

- **Frontend**: Vercel or Netlify (real account, custom domain). Client provides domain or uses a subdomain of their existing site.
- **Backend**: Supabase Edge Function (`generate-content`) calls the AI API server-side. AI API key lives in Supabase environment variables, never in client code.
- **AI provider**: Claude API or OpenAI, server-side only, with hard spending cap set in provider dashboard before launch.

## 4. Sign-off

This spec is delivered as the first deliverable (part of the $150 scoping call). Client approves in writing before any code is written. Changes after sign-off go through a change-order process, not silent scope expansion.

## 5. Out of Scope (v1)

- MLS direct integration (Phase 2)
- Multiple brand voices per account / team accounts (Agency tier, Phase 2)
- Referral system
- Mobile app packaging
- Analytics dashboard for the client's own usage stats beyond the basic usage counter
- Any data migration from the client's existing tools

---

## Pricing Reference (from prior PropBot research)

- Free: 10 generations/month
- Pro: $19/month, unlimited + brand voice
- Agency: $49/month, unlimited + team voices (Phase 2, not v1)

For a **custom client build** (client owns the Supabase project, Vercel deployment, and domain): one-time build fee $497-997 based on this spec, positioned as "your own private PropBot," not a subscription to your SaaS.
