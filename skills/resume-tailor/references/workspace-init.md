# Day 0: Workspace Bootstrapping Runbook

Use this runbook when the user initiates setup (e.g., says *"Start"*, *"Initialize workspace"*, or provides their raw resume where `about_me.md` does not yet exist). Always cross-check whether folders or config files already exist before creating them.

---

## Autonomous Setup Sequence

### 1. Ingest User Background (`about_me.md`)
- If `about_me.md` is missing, extract all roles, dates, tools, and metrics from the user's provided resume using [about_me_schema.md](../resources/schema/about_me_schema.md) and write `about_me.md` in the workspace root.
- **Rule:** Never invent experience, companies, or degrees.

### 2. Verify & Create Workspace Directories
Check and create any missing directories:
```text
applications/
├── full-time/
├── master-thesis/
├── phd/
├── werk-student/
└── internship/
master/
temp-tex/
.vscode/
```

### 3. Deploy Master Templates
1. If missing in `master/`, copy [master-resume.tex](../resources/templates/master-resume.tex) and [master-cover-letter.tex](../resources/templates/master-cover-letter.tex) into `master/`.
2. Pre-populate the contact header fields in both files with the user's details (Name, Email, Phone, Location, LinkedIn).

### 4. Configure Clean LaTeX Builds & Git Ignore
1. **`.vscode/settings.json`**: Check if `.vscode/settings.json` exists. If missing, copy [vscode-settings.json](../resources/templates/vscode-settings.json) to `.vscode/settings.json` (routes LaTeX auxiliary files to `temp-tex/`, keeps compiled PDFs in `%DIR%`, and enables terminal auto-approve).
2. **`.gitignore`**: Check if `.gitignore` exists. If missing, copy [gitignore](../resources/templates/gitignore) to `.gitignore` in the workspace root to ignore PDFs, `temp-tex/`, and LaTeX build artifacts.

### 5. Initialize Tracker Database (`tracker.csv`)
- If `tracker.csv` does not exist in the workspace root, copy [tracker.csv](../resources/templates/tracker.csv) to `tracker.csv` with headers:
  `Company,Role,Location,Status,Date,Contact,Contact Email,Job URL,Language,Key Requirements,Tailoring Notes,Next Step,Notes`

### 6. Completion Confirmation
Output a concise confirmation message:
```text
🎉 Workspace initialized and verified!

Configured:
- about_me.md (Single source of truth)
- master/ (Base LaTeX templates)
- applications/ (Categorized job folders)
- .vscode/settings.json & temp-tex/ (Clean LaTeX compilation)
- .gitignore & tracker.csv

👉 Next Step: Paste a Job Description to generate a tailored application (e.g. "Apply for Senior AI Engineer at BMW: [paste JD]").
```
