# AI Task Router — Multi-Platform Division of Labor

Status: Living reference document, update when a routing assignment proves wrong
Platforms: Claude, ChatGPT, Gemini, Grok, Kimi, DeepSeek

---

## Routing Decision Tree (run this first, every time)

1. Does it touch auth, payments, API keys, or RLS policies? → **Claude only.** Skip the rest of this tree.
2. Is it market/trend research or niche validation? → **Gemini**
3. Is it a first-draft technical spec, architecture blueprint, or SQL schema? → **DeepSeek**
4. Is it a no-code click-path (Bubble/Glide/FlutterFlow) or marketing/landing copy? → **ChatGPT**
5. Is it real-time social data, X/Twitter trends, or social hooks? → **Grok**
6. Is it a whole-repo audit, long-document synthesis, or session handoff? → **Kimi**
7. Anything else, or any conflict between two AI outputs → **Claude** (final arbiter)

## Assignment Table

| Task Type | Primary AI | Mechanism (why this AI) | Backup |
|---|---|---|---|
| Market & trend research | Gemini | Largest context window for synthesizing many sources into structured findings | DeepSeek |
| Technical blueprint / first-draft architecture | DeepSeek | Strong exhaustive technical reasoning at lowest cost (proven on PropBot blueprint) | Kimi |
| SQL schema / database first draft | DeepSeek | Proven pattern (PropBot schema), Claude audits before any table goes live | Claude (audit only) |
| No-code UI walkthroughs (Bubble, Glide, FlutterFlow) | ChatGPT | Deepest exposure to no-code platform documentation patterns | Gemini |
| Marketing/landing page copy, pricing pages | ChatGPT | Consistent structured persuasive copy | Grok (for raw/edgy variants) |
| Real-time social trend scanning, X hooks | Grok | Only platform with live X data access | — |
| Whole-repo audits, long handoff capsules | Kimi | Largest context window, persistent memory_space across a thread | Claude (final pass) |
| Security-sensitive code: auth, payments, RLS, API keys | Claude | Final say only, never delegated regardless of who drafted the surrounding code | — |
| Architecture decisions, conflict resolution between AI outputs | Claude | Cross-checker role: reconciles multiple AI outputs into one shippable artifact | — |
| Image/screenshot analysis, multimodal UI QA | Gemini | Strongest multimodal reasoning of the free-tier set | ChatGPT |

## Handoff Capsule (paste this between AIs so context survives the jump)

AI HANDOFF — [Project Name]
From: [AI name]
To: [AI name]
Task: [one sentence]
Constraints: Trinidad & Tobago, $0 budget, free-tier tools only, mobile-only editing
Input: [paste the source AI's output below this line]
Expected output: [exact format needed — code block / table / step list]

## Conflict Resolution Rule

If two AI outputs disagree (naming mismatch, conflicting schema, contradictory advice): paste both to Claude with the flag `//AUDIT CONFLICT`. Claude reconciles and ships the final version. Claude's call is final on anything touching security or architecture, no exceptions.

## Update Log

- 2026-06-20: Initial version, created to formalize the existing DeepSeek-blueprint / ChatGPT-build / Claude-audit pattern already proven on PropBot.
