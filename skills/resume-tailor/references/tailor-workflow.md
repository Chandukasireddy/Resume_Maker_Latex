# Day 1+: Application Tailoring Runbook

Follow this runbook when `about_me.md` exists and the user provides a Job Description to generate a tailored application.

---

## 7-Step Autonomous Execution Engine

### Step 1: Ingest & Route Category
1. Parse the company name, role title, and job requirements from the user's provided Job Description.
2. Consult [category-routing.md](./category-routing.md) to pick the correct folder:
   - `applications/full-time/<company-role>/`
   - `applications/master-thesis/<company-role>/`
   - `applications/phd/<company-role>/`
   - `applications/werk-student/<company-role>/`
   - `applications/internship/<company-role>/`
3. Create the job folder.

### Step 2: Clone Master Templates
1. Copy **only** these two files from `master/` into the new folder:
   - `master/master-resume.tex`
   - `master/master-cover-letter.tex`
2. Rename them to reflect the candidate's name:
   - `master-resume.tex` → `[your_name]_resume.tex`
   - `master-cover-letter.tex` → `[your_name]_cover-letter.tex`
3. **Rule:** Do not copy PDFs, cache files, or auxiliary build artifacts.

### Step 3: Create `notes.md` Immediately
Create `notes.md` inside the job folder following [sample-notes.md](../examples/sample-notes.md) with this exact structure:
1. **Line 1 Metadata:**
   `# YYYY-MM-DD | Company: <Company> | Role: <Role> | Location: <Location> | Link: <URL or N/A>`
2. **Questionnaire / Portal Answers (if any):**
   - Answer any specific questions present in the JD or user prompt.
   - If no questions exist, state: `No explicit application questions were provided.`
3. **Full Job Description:**
   - Paste the raw JD text under `## Job Description`.
4. **Generation & Tailoring Audit:**
   - Record edited sections, keywords matched from `about_me.md`, and company research summary.

### Step 4: Tailor Resume LaTeX
1. Read `about_me.md` to identify the most relevant skills, projects, and experiences matching the JD.
2. Edit `[your_name]_resume.tex` following [latex-rules.md](./latex-rules.md):
   - Update `Role` line under the name header to align with target title.
   - Tailor `Profile` summary (must not exceed **330 characters**).
   - Rewrite bullet points in `Professional Experience` using the [humanizer-formula.md](./humanizer-formula.md) (each bullet must not exceed **150 characters**).
   - Reorder and emphasize relevant keywords in `Skills`.
   - **Crucial:** Never add/remove sections. Keep strict 1-page layout.

### Step 5: Tailor Cover Letter LaTeX
1. Edit `[your_name]_cover-letter.tex` following [latex-rules.md](./latex-rules.md):
   - Update recipient company name, address, and date.
   - Write **exactly two paragraphs** of body content:
     - Paragraph 1: Motivation & strategic alignment with the company's specific mission/products.
     - Paragraph 2: Proven track record from `about_me.md` directly solving the team's posted challenges.
   - Verify layout stays strictly under 1 page.

### Step 6: Log Application to `tracker.csv`
1. Prepend / append a new record row to `tracker.csv` in the root of the workspace.
2. Columns:
   `Company,Role,Location,Status,Date,Contact,Contact Email,Job URL,Language,Key Requirements,Tailoring Notes,Next Step,Notes`
   - `Status`: Default to `Applied` (or `To Apply`).
   - `Date`: Today's date formatted as `DD-MM-YYYY`.
   - `Key Requirements`: Extracted top 2-3 skills (e.g. `"Python, LLMs, RAG"`).
   - `Tailoring Notes`: Brief 3-word summary (e.g. `"Emphasized GenAI & Cloud"`).

### Step 7: Final Summary for the User
Inform the user:
- Dedicated application directory created: `applications/<category>/<company-role>/`
- Tailored files: `resume.tex`, `cover-letter.tex`, `notes.md`
- Tracker updated in `tracker.csv`
- Advise user to compile `.tex` to PDF locally or in Overleaf.
