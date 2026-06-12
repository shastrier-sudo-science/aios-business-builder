# Doc Improver — Tighten Any Draft

## Purpose
Take any rough draft, transcript, or brain-dump and tighten it for clarity, professionalism, and business use. Removes fluff, fixes structure, preserves voice.

## Input Required
1. **DRAFT**: [Paste your raw text]
2. **FORMAT**: [Email / LinkedIn post / Proposal / Script / Landing page / Newsletter]
3. **TONE**: [Direct / Diplomatic / Authoritative / Empathetic / Sales]
4. **LENGTH TARGET**: [Shorter / Same / Longer — specify word count if known]
5. **CTA NEEDED**: [Yes/No — what should reader do next?]

## The Prompt

Run this with Claude/Kimi:

---
You are a senior editor specializing in business communication. Tighten the following draft for [FORMAT] use.

**Raw Draft:**
[PASTE DRAFT HERE]

**Parameters:**
- Format: [FORMAT]
- Tone: [TONE]
- Length target: [LENGTH TARGET]
- CTA needed: [CTA NEEDED]

**Editing Rules:**
1. Cut every sentence that doesn't move the reader toward understanding or action
2. Replace passive voice with active voice
3. Replace abstract nouns with concrete verbs (e.g., "implementation of" → "build")
4. Break up sentences longer than 20 words
5. Ensure the first sentence earns the second sentence
6. If CTA needed, make it specific and low-friction (not "let me know" — "reply with YES and I'll send it")
7. Preserve the author's original voice — don't make it sound like corporate AI

**Output Format:**
1. **Clean Draft** (full rewritten text)
2. **Changes Made** (bullet list of specific edits and why)
3. **Word Count** (before → after)
4. **Confidence Score** (1-10: how much this draft improved)

**Tone Guardrails:**
- No "leverage," "synergize," "unlock potential," "empower"
- No "I hope this email finds you well"
- No "just checking in"
- No multiple ideas per sentence
---

## Example Use Cases
- **Transcript cleanup:** Paste a voice memo transcript, get polished LinkedIn post
- **Proposal tightening:** Turn a rambling pitch into a 3-paragraph close
- **Email clarity:** Fix "I wanted to reach out regarding the possibility of" → "Can you do X by Friday?"
- **Landing page:** Turn feature list into problem-agitation-solution flow

## Usage Notes
- Run this on your own bio before using Profile Optimizer
- Run this on client drafts before delivery
- Save improved versions as templates in `artifacts/`
- Track which tone settings work best for your voice in `logs/`
