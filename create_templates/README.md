# Creative Single-Page Executive LaTeX CV Template with Photo

A modern, highly creative single-page tech resume template designed for maximum readability, strict single-page budget, and high ATS (Applicant Tracking System) & ADS (Automated Document Scoring) compatibility.

---

## 📁 Included Files

| File | Purpose |
| :--- | :--- |
| `cv.txt` | One-pager source file named `cv.txt` (compiles directly with `pdflatex`) |
| `cv.tex` | Full LaTeX source code formatted for modern LaTeX editors / VS Code |
| `cv.pdf` | Cleanly rendered, production-ready 1-page PDF output |
| `cv_preview-1.png` | 150 DPI visual rendered preview of the single-page CV |
| `profile_photo.png` | Professional 1:1 circular headshot portrait |
| `profile_photo.jpg` | High-resolution JPG version of the headshot |

---

## 🎯 High ATS / ADS Score Architecture

1. **Linear Top-to-Bottom Semantic Order:**
   - The document flows naturally: **Executive Header $\rightarrow$ Executive Summary $\rightarrow$ Professional Experience $\rightarrow$ Education $\rightarrow$ Technical Skills $\rightarrow$ Publications & Honors**.
   - Verified with `pdftotext` to ensure zero scrambled text columns, zero overlapping layers, and clean machine-readable text streams.

2. **Semantic Section Headings:**
   - Standard uppercase sections (`EXECUTIVE SUMMARY`, `PROFESSIONAL EXPERIENCE`, `EDUCATION`, `TECHNICAL SKILLS`, `PUBLICATIONS, HONORS & LEADERSHIP`) easily recognized by major ATS engines (Workday, Greenhouse, Lever, Taleo, SAP SuccessFactors).

3. **Universal Placeholder Data Structure:**
   - Pre-configured with clean, standard placeholders ready to be customized:
     - `[Your Full Name]`, `[Your Professional Title]`, `[Core Specialization & Domain]`
     - Contact pills (`[your.email@example.com]`, `[+1 (555) 012-3456]`, `[linkedin.com/in/yourprofile]`, `[yourportfolio.com]`, `[City, Country]`)
     - High-impact bullet placeholders following the Action Verb + Task + Tool + Quantified Metric formula.
     - Flexible education, technical skill domains, peer-reviewed publications, and leadership sections.

4. **Executive Portrait Integration:**
   - Framed 2.3 cm circular headshot with an accent ring (`PrimaryColor`) that sits cleanly in the header without disrupting the text flow.

5. **Strict Single-Page Guarantee:**
   - Calibrated margins (`top=0.36in, bottom=0.36in, left=0.48in, right=0.48in`) and tight vertical item spacing ensure that content fills the page with balanced whitespace and zero overflow.

---

## 🛠️ Compilation Instructions

To compile using pdfTeX from the command line:

```bash
# Compile directly from cv.txt:
pdflatex -jobname=cv -interaction=nonstopmode cv.txt

# Or compile from cv.tex:
pdflatex -interaction=nonstopmode cv.tex
```

---

## 🎨 Customization Quick Guide

- **Swap the Photo:** Replace `profile_photo.png` with your portrait image (square 1:1 ratio recommended).
- **Change Primary Accent Color:** In the preamble, adjust `\definecolor{PrimaryColor}{HTML}{0F2A4A}` (Navy) and `\definecolor{SecondaryColor}{HTML}{1D63B8}` (Tech Blue).
- **Edit Content:** Modify personal details, roles, and skills directly in `cv.txt` or `cv.tex`.
