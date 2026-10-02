# Contributing to Automated Resumes

First of all, thank you for your interest in contributing! 🎉

Our mission is to build the world's best open-source, automated LaTeX resume generator—transforming the tedious job application process into a streamlined, high-quality, AI-assisted experience.

We have evolved this framework into a **universal, installable agent skill** (installable via `npx skills add Chandukasireddy/Resume_Maker_Latex`), and we welcome community contributions to expand its capabilities.

---

## 🚀 Where We Need Help Most

We are currently looking for contributors across four major pillars:

### 1. 🎨 New LaTeX Resume & Cover Letter Templates
We want to offer job seekers a rich collection of battle-tested, ATS-friendly, and visually distinct LaTeX templates:
- **Styles**: Modern, Minimalist, Academic / CV, Two-Column, Executive, Creative, and Tech/Engineering.
- **Requirements**:
  - Must compile cleanly with standard compilers (`pdflatex`, `xelatex`, or `lualatex`).
  - No obscure or deprecated packages.
  - Well-commented sections that AI agents can easily parse and edit.
  - Must use **placeholders only** (never commit personal contact info).

### 2. ⚡ Agent Skills & Extensions (`skills/`)
Expand and refine modular skills under the `skills/` directory:
- Additional skills (e.g., ATS compliance scanners, interview question generators, cover letter polishers).
- Enhancement of `skills/resume-tailor/` and `skills/humanizer/`.

### 3. 🤖 Automation, Tooling & CI
- Automated LaTeX compilation test runners and GitHub Actions CI.
- LaTeX syntax validators and error recovery workflows for AI agents.
- Cross-platform CLI scripts for compiling PDFs locally on Windows, macOS, and Linux.

### 4. 📚 Documentation & Guides
- Setup guides for different operating systems (Linux, macOS, Windows) and LaTeX distributions (TeX Live, MiKTeX, MacTeX).
- Best practices for pairing with AI coding agents (AntiGravity, Cursor, Claude Code, VSCode Copilot).

---

## 🛠️ Contribution Workflow

### 1. Find or Propose an Issue
- Browse [open issues](https://github.com/Chandukasireddy/Resume_Maker_Latex/issues) to find something you'd like to work on.
- If you have a new idea, feature request, or template, please open an issue or discussion first so we can align on the approach.

### 2. Fork & Branch
- Fork the repository to your own GitHub account.
- Clone your fork locally:
  ```bash
  git clone https://github.com/<your-username>/Resume_Maker_Latex.git
  ```
- Create a focused branch with a descriptive name:
  ```bash
  git checkout -b feat/add-modern-two-column-template
  # or
  git checkout -b feat/npx-skill-scaffold
  ```

### 3. Making Changes
- **No Personal Information**: Double-check that your commits do **not** contain personal phone numbers, emails, addresses, or private job notes. Always use generic placeholders (`John Doe`, `john.doe@example.com`, `+1 (555) 123-4567`).
- **Test Compilations**: If submitting LaTeX files, verify they compile to PDF without fatal errors.

### 4. Commit Guidelines
We follow standard Conventional Commits:
- `feat:` A new feature or template (e.g., `feat(templates): add modern minimalist resume template`)
- `fix:` A bug fix or LaTeX compilation correction
- `docs:` Documentation updates
- `refactor:` Code or prompt refactoring without feature changes

### 5. Submit a Pull Request
- Push your branch to your fork:
  ```bash
  git push origin feat/your-feature-name
  ```
- Open a Pull Request against the `main` branch.
- Fill out the PR template or describe:
  - What was added/changed.
  - If a template was added, include a screenshot or preview of the compiled PDF.
  - Any relevant issue numbers (e.g., `Closes #4`).

---

## 📜 Non-Commercial Commitment

This project is licensed under the [PolyForm Noncommercial License 1.0.0](LICENSE). By contributing to this repository, you agree that your contributions will be shared openly under these non-commercial terms, ensuring the tools and templates remain free, accessible, and protected from commercial exploitation for all job seekers.

