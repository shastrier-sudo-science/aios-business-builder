# Newsletter Writer — Ultimate Beginner Skill

## Purpose
Generate a complete daily newsletter issue from a raw idea, transcript, or single insight. Designed for non-technical writers building consistency through AI assistance.

## Input Required
1. **TOPIC/HOOK**: [One sentence — what's the core idea?]
2. **SOURCE MATERIAL** (optional): [Transcript, article link, voice memo text, or "none — invent from scratch"]
3. **TONE**: [Direct / Story-driven / Tactical / Philosophical]
4. **LENGTH**: [Short (300 words) / Medium (600 words) / Long (1000+ words)]
5. **CTA**: [What should reader do? — "buy book" / "reply" / "share" / "read yesterday's issue"]

## The Prompt

Run this with Claude/Kimi:

---
You are my newsletter ghostwriter. I publish daily to overwhelmed people trying to escape debt using AI-powered mindset systems.

**Today's Topic:** [TOPIC/HOOK]
**Source Material:** [SOURCE MATERIAL or "none"]
**Tone:** [TONE]
**Length:** [LENGTH]
**CTA:** [CTA]

**Constraints:**
- I am Shastrie Ramdhanie, published author of "Hacking Your Mindset" (2023)
- I built from zero in Trinidad, $242K debt, 3-hour daily window
- My readers are stuck, overwhelmed, and need one actionable insight per issue
- No generic motivation. No "believe in yourself." Specific mechanisms only.
- Every issue must feel like a conversation, not a lecture

**Structure:**
1. **Hook** (1-2 sentences — open loop or contradiction)
2. **Context** (2-3 sentences — why this matters today, grounded in real constraint)
3. **Mechanism** (the core insight — how it works, not just what to do)
4. **Action** (one specific, tiny step they can take in 10 minutes)
5. **CTA** (natural bridge to the book or next issue)

**Output:**
- Full newsletter text, ready to paste into email platform
- Suggested subject line (under 50 characters)
- Suggested preview text (under 100 characters)

**Tone Guardrails:**
- No "unlock your potential," "level up," "crush it"
- No paragraphs longer than 3 sentences
- Every claim must connect to a specific outcome
- Use "I" only when sharing lived experience, not as authority posturing
---

## Usage Notes
- Run this every morning as part of Hour 1 (Creation/Trust)
- Save outputs to `artifacts/newsletter/YYYY-MM-DD-issue.md`
- Track open/reply rates in `logs/`
- Repurpose top-performing issues into LinkedIn posts using Profile Optimizer

## Remember This
- **Q:** What's the maximum paragraph length?  
  **A:** 3 sentences.
- **Q:** What's the CTA priority?  
  **A:** $27 book bundle.
