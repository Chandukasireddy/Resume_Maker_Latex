# Day 0: Workspace Bootstrapping Runbook

Use this runbook when the user initiates setup (e.g., says *"Start"*, *"Initialize workspace"*, or provides their raw resume in an uninitialized directory where `about_me.md` does not yet exist).

---

## Autonomous Setup Sequence

### 1. Ingest User Background
- Extract all text, dates, roles, tools, and metrics from the user's provided resume (pasted text or file).
- Use [about_me_schema.md](../resources/schema/about_me_schema.md) as the formatting blueprint.
- Write the parsed content into `about_me.md` in the root of the workspace.
- **Rule:** Do not invent any work experience, company names, or degrees. Keep only genuine details from the user.

### 2. Scaffold Application Category Folders
Create the standard categorized directory tree under `applications/`:
```text
applications/
├── full-time/
├── master-thesis/
├── phd/
├── werk-student/
└── internship/
```

### 3. Deploy Master Templates
1. Create a `master/` directory in the root of the workspace.
2. Copy `master-resume.tex` from [master-resume.tex](../resources/templates/master-resume.tex) into `master/master-resume.tex`.
3. Copy `master-cover-letter.tex` from [master-cover-letter.tex](../resources/templates/master-cover-letter.tex) into `master/master-cover-letter.tex`.
4. Pre-populate the contact header fields in both files with the user's personal details extracted from step 1 (Name, Email, Phone, Location, LinkedIn).

### 4. Initialize Tracker Database
- Copy [tracker.csv](../resources/templates/tracker.csv) into the root of the workspace as `tracker.csv`.
- Ensure the header row is:
  `Company,Role,Location,Status,Date,Contact,Contact Email,Job URL,Language,Key Requirements,Tailoring Notes,Next Step,Notes`

### 5. Completion Confirmation
Provide a crisp confirmation message to the user:
```text
🎉 Workspace successfully initialized!

Created files:
- about_me.md (Your Single Source of Truth background)
- master/ (Base LaTeX master templates)
- applications/ (full-time, internship, thesis, phd, werk-student)
- tracker.csv (Application tracking database)

👉 Next Step: Whenever you want to apply for a role, simply paste the Job Description here (e.g. "Apply for Senior AI Engineer at BMW: [paste JD]").
```
