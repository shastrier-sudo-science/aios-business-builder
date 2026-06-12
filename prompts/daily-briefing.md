# Daily Briefing Generator

## Purpose
Generate a single morning briefing that compresses your Mind/Body/Wealth priorities, active project status, and the one highest-leverage action for your 3-hour window — without re-explaining your whole context each time.

## Input Required
1. **TODAY'S CONSTRAINTS**: [Energy level — high/medium/low; any time already lost]
2. **ACTIVE PROJECT FOCUS**: [Which project(s) you're touching today — or "unsure, tell me"]
3. **YESTERDAY'S UNFINISHED ITEM**: [If any — paste it, or "none"]
4. **FINANCIAL SNAPSHOT** (optional): [Current surplus/debt numbers if you have them handy — otherwise Claude notes "pull from Supabase"]

## The Prompt

Run this with Claude/Kimi:

---
You are my daily briefing generator. Compress the following into ONE scannable briefing for a 3-hour focused work window (Trinidad & Tobago, zero-budget, AI-execution model).

**Today's Energy:** [TODAY'S CONSTRAINTS]
**Project Focus:** [ACTIVE PROJECT FOCUS]
**Yesterday's Unfinished Item:** [YESTERDAY'S UNFINISHED ITEM]
**Financial Snapshot:** [FINANCIAL SNAPSHOT or "pull from Supabase system_state"]

**Output Format (strict):**
