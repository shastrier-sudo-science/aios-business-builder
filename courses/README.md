# Courses — Daily Learning System

**Purpose:** Store all AI-generated courses. Pull daily questions for consistent learning without re-reading entire modules.

**How It Works:**
1. Save each course as a folder with numbered modules
2. Run `daily-question-generator.md` skill each morning
3. Answer 1-3 questions in `logs/` or verbally to AI
4. Track streak and completion in `course-index.md`

**Folder Structure:**
courses/ 
├── README.md 
├── course-index.md 
├── daily-question-generator.md 
├── ai-business-claude/ 
│ ├── module-01.md │ 
├── module-02.md │ └── ... 
├── mindset-systems/ │ 
├── module-01.md │ └── ... └── ...

**Rules:**
- One course per folder
- Modules numbered sequentially
- Each module must have a "Key Concepts" section at the bottom (used by the question generator)
- No course longer than 10 modules (split if needed)

## 📚 Courses Folder (`/courses`)

This folder contains plain-text learning resources covering **Coding, Math, Algorithms, Business, and Finances**. Since all files are `.txt` or `.md`, they can be fed directly into your AI with zero preprocessing—maximizing your limited 3-hour daily window.

### Recommended Folder Structure
Organize your text files by domain for easier retrieval:

/courses/
├── coding/          # Language syntax, frameworks, best practices
├── math/            # Linear algebra, calculus, statistics for AI/Dev
├── algorithms/      # Data structures, sorting, dynamic programming
├── business/        # Sales, marketing, operations, systems thinking
├── finances/        # Accounting, valuation, cash flow management
└── daily-question-generator.md  # YOUR CORE TOOL (see below)

---

## 🚀 The "Sovereign" Playbook: How to Get the HIGHEST Value

Since you have **3 hours/day** and a **$419 TTD** constraint, passive reading is a waste of time. Here is the exact system to turn every text file into applied, profit-generating knowledge.

### 1. The Daily Question Generator (Your Primary Engine)
Your `daily-question-generator.md` is the most important file in this folder. Before you read *any* new course text, run this prompt with your AI:

> *"Using the `daily-question-generator.md` framework, take this course text and generate 3 specific questions. They must force me to: (1) Recall the core rule, (2) Apply it to my current active project (e.g., PropBot or Proposal-Forge), and (3) Adapt it to my Trinidad & Tobago market context."*

**Why this gives max value**: It turns passive text into an active, high-stakes quiz. You don't read to "know"; you read to *answer*. This drastically reduces study time and increases retention.

### 2. The "Build or Compute" Rule (Coding, Math, Algorithms)
For technical texts, **never read code or formulas without executing them**.
- Copy the code/algo from the text file and paste it into your AI.
- Prompt: *"Rewrite this [algorithm/formula] to solve my specific problem in [Project Name]. Then, explain it to me like I'm building an MVP, not a PhD thesis."*
- Immediately save the AI's working implementation into `/artifacts/code-snippets/`. 
- **Value**: You now own a working piece of code, not just a textbook concept.

### 3. The "Framework Extraction" Rule (Business & Finances)
For business and finance texts, your goal is to extract **calculators and checklists**.
- Take a chapter on, say, "Cash Flow Management" or "Value-Based Pricing."
- Prompt: *"Extract the exact mathematical formula or step-by-step checklist from this text. Turn it into a reusable prompt I can add to my `/prompts` folder for future proposal generation."*
- Save the resulting prompt in `/prompts/finance-pricing-expert.md`.
- **Value**: Next time you write a client proposal, your AI will automatically apply that financial framework without you re-reading the book.

### 4. The "Synthesize Across Domains" Hack (The Superpower)
This is where you get **exponential** value. Since you have Coding, Math, *and* Business texts, merge them:
- Take an algorithm from `/algorithms` and a business constraint from `/business`.
- Prompt: *"Combine the efficiency principle from this algorithm with the customer acquisition framework from this business text. Design a lean workflow for my daily 3-hour block."*
- **Value**: You create interdisciplinary insights that most founders miss. This makes your `AIOS` system truly unique.

### 5. The 24-Hour Log Rule (Close the Loop)
After using the Daily Question Generator and applying the lesson, you **must** log it within 24 hours.
Create a log entry in `/logs/course-applications.md` with this exact format:
- **Date**: [Today]
- **Source**: [Course file name]
- **Question Asked** (from the generator): [The question]
- **My Action**: [What I coded, built, or priced]
- **Result**: [Did it save time? Make money? Fix a bug?]
- **Tweak**: [What I changed to fit my local context]

**Why this gives max value**: This log becomes your *custom* playbook. After 10 logs, you stop needing the original courses altogether—you just read your own battle-tested adaptations.

## 📚 Courses Folder (`/courses`)

This folder contains plain-text learning resources across **5 critical domains**: Coding, Math, Algorithms, Business, and Finances. All files are `.txt` or `.md`, optimized for direct AI consumption.

### Recommended Folder Structure
/courses/
├── coding/          # Python, JS, API patterns, system design
├── math/            # Linear algebra, statistics, probability
├── algorithms/      # Data structures, sorting, dynamic programming
├── business/        # Sales, operations, systems thinking, copywriting
├── finances/        # Accounting, valuation, break-even, cash flow
└── daily-question-generator.md  # Your primary engagement tool (v2.0)

---

## 🚀 How to Get the HIGHEST Value from These Courses

Passive reading is a trap. With a **3-hour daily window** and **$419 TTD** surplus, you must extract working code, accurate math, and profitable frameworks—not just facts.

Here is the **Sovereign 3-Step Execution Playbook**:

### Step 1: Always Start with the `daily-question-generator.md`
**Before you open a single text file**, run the generator with your AI. Feed it the **COURSE DOMAIN** (e.g., "algorithms") and your **ENERGY LEVEL**. 
- *Why this is #1:* It forces the AI to pre-scan the material and hand you only the most relevant, high-leverage pieces. You stop reading "cover to cover" and start reading to *answer specific questions*. This cuts study time by 60%.

### Step 2: Apply the "Domain-Lock" Rule
Based on the domain of the course, your answer to the generator's question must produce a *tangible asset*:

| Domain | Tangible Asset to Produce |
| :--- | :--- |
| **Coding / Algorithms** | A deployable code snippet. Save it in `/artifacts/code-snippets/`. Immediately integrate it into PropBot or Proposal-Forge. |
| **Math** | A working formula or spreadsheet. Calculate something real (e.g., user growth, conversion rates) using your own `logs/` data. |
| **Business** | A reusable prompt or sales script. Save it in `/prompts/sales-*.md`. You will use it in your next client interaction. |
| **Finances** | An updated P&L or break-even chart. Update your `knowledge/financial-constraints.md` with the new numbers. |

**The Rule**: If you can't build, calculate, or script it, you haven't learned it. Go back to the AI and ask: *"Rewrite this so I can apply it to my actual project right now."*

### Step 3: Log Within 24 Hours (Close the Loop)
After answering the generator's questions, immediately save your answers in `logs/YYYY-MM-DD-learning.md` using the **exact output format** from the generator. 
- *Why this is critical:* Your `logs/` folder will quickly become more valuable than the original courses. After 2 weeks, you will stop referencing the course texts entirely—you will just read your own application logs to refresh your memory, saving you dozens of hours.

### Bonus: The "Interdisciplinary Merge" (Your Secret Advantage)
Since you own all 5 domains, do this once a week: 
- Take 1 concept from **Finances** and 1 from **Algorithms**. 
- Prompt your AI: *"Combine the efficiency of this algorithm with the cost-saving principle from this finance module. Design a single daily checklist for my 3-hour work block."*
This produces unique insights that founders who study siloed topics will never discover.
