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
