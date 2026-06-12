# Daily Question Generator — Course Learning Skill

## Purpose
Pull 1-3 targeted questions from any course in your repo to test retention, deepen understanding, or apply concepts to your real constraints.

## Input Required
1. **COURSE NAME**: [e.g., "ai-business-claude"]
2. **MODULE RANGE**: [e.g., "module-01" / "module-01 through module-03" / "all completed modules"]
3. **ENERGY LEVEL**: [high / medium / low]
4. **FOCUS TYPE**: [retention / application / teaching / mixed]

## The Prompt

Run this with Claude/Kimi:

---
You are my daily learning coach. Generate questions from my course materials.

**My Context:**
- Name: Shastrie Ramdhanie
- Location: Trinidad, 3-hour daily window
- Current energy: [ENERGY LEVEL]
- Learning goal: 1% daily improvement, consistency over intensity

**Course:** [COURSE NAME]
**Modules to pull from:** [MODULE RANGE]
**Question type:** [FOCUS TYPE]

**Rules:**
- If energy is LOW: generate exactly 1 question, make it a single specific application to my real life (debt, PropBot, newsletter, etc.)
- If energy is MEDIUM: generate 2 questions — 1 retention, 1 application
- If energy is HIGH: generate 3 questions — 1 retention, 1 application, 1 teaching (how would I explain this to someone else?)
- Every question must connect to my actual constraints (Trinidad, $0 budget, 3-hour window, $242K debt)
- No generic "what did you learn" questions. Make them specific and actionable.
- Include the exact module source for each question so I can reference back.

**Output Format:**
DAILY QUESTIONS — [DATE]
Course: [COURSE NAME] Modules Covered: [RANGE]
Q1 ([TYPE]): [Specific question] → Source: [module-XX.md, section: XXX]
Q2 ([TYPE]): [Specific question] (if applicable) → Source: [module-XX.md, section: XXX]
Q3 ([TYPE]): [Specific question] (if applicable) → Source: [module-XX.md, section: XXX]
ANSWER LOG: [Paste your answers here, or reply verbally]
STREAK TRACKER: [X days in a row]

**Example (Low Energy):**
Q1 (Application): The AI business course says client acquisition is more important than technical skills. What is the ONE outreach action you will take in today's Hour 2 to land your first Upwork client, and what exact sentence will you use in the first line of your proposal?
→ Source: module-03.md, section: "Client Acquisition Systems"
---

## Usage Notes
- Run this as part of Hour 3 (Testing/Learning) or at the end of Hour 1 if energy is high
- Save answers in `logs/YYYY-MM-DD-learning.md`
- If you miss a day: next session, ask for a "catch-up review" — 1 question from the last module you touched
- When a course is complete: add "COMPLETED" to `course-index.md` with completion date

## Remember This
- **Q:** What happens when energy is low?  
  **A:** Exactly 1 question, applied to real life, no theory.
- **Q:** Where do answers get saved?  
  **A:** `logs/YYYY-MM-DD-learning.md`

