---
name: latex-formatter
description: Converts humanized text and resume content into clean, error-free, 1-page compilable LaTeX resume code with proper special-character escaping and layout macros. Use when converting text into LaTeX format or generating .tex resume files.
---

# LaTeX Formatter Skill

The **LaTeX Formatter Skill** converts raw or humanized resume text into clean, error-free, and compilable LaTeX syntax. It enforces strict rules for special character escaping, macro usage, and layout spacing to guarantee a professional 1-page resume output.

---

## When to Trigger This Skill

Trigger this skill whenever:
- Converting raw or humanized bullet points into LaTeX format.
- Formatting resume entries (`\item`, `\textbf`, custom macros).
- Fixing LaTeX compilation errors (unescaped `%`, `&`, `$`, `_`, `#`).
- Adjusting page layout or spacing (`\vspace`) to fit a resume onto **1 single page**.
- Creating or editing `.tex` resume files.

---

## Core Workflow

```mermaid
flowchart TD
    A[Humanized Text Input] --> B[Escape Special Characters %, &, $, _, #]
    B --> C[Wrap Terms in \textbf{...}]
    C --> D[Apply Resume Macros \resumeItem / \item]
    D --> E[Check Page Layout & \vspace Spacing]
    E --> F[Generate Clean Compilable .tex Output]
```

1. **Escape Reserved Characters:** Run text through [syntax-and-escaping-rules.md](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/references/syntax-and-escaping-rules.md) to escape `%`, `&`, `$`, `_`, `#`.
2. **Apply Bold Formatting:** Wrap metrics, key technologies, and outcomes in `\textbf{...}`.
3. **Format Macros:** Apply standard resume macro environments outlined in [latex-resume-macros.md](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/references/latex-resume-macros.md).
4. **Enforce 1-Page Layout:** Follow vertical spacing guidelines in [layout-and-spacing-guide.md](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/references/layout-and-spacing-guide.md).
5. **Verify Against Examples:** Compare formatted snippets with [raw-to-latex-bullets.md](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/examples/raw-to-latex-bullets.md) and reference [full-resume-template.tex](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/examples/full-resume-template.tex).

---

## Key Escaping Quick Guide

| Input Character | Meaning in LaTeX | Escaped Output |
|---|---|---|
| `%` | Comment marker | `\%` |
| `&` | Table / Alignment column separator | `\&` |
| `$` | Math mode toggle | `\$` |
| `_` | Subscript operator | `\_` |
| `#` | Macro parameter | `\#` |

---

## Skill File Map

- 🔤 [Syntax & Escaping Rules](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/references/syntax-and-escaping-rules.md) - Complete rules for escaping reserved LaTeX characters.
- 📐 [LaTeX Resume Macros](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/references/latex-resume-macros.md) - Standard macros for headings, items, and sections.
- 📄 [Layout & Spacing Guide](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/references/layout-and-spacing-guide.md) - Techniques for keeping resume content strictly on 1 page.
- 💡 [Raw to LaTeX Bullets](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/examples/raw-to-latex-bullets.md) - 15+ conversion examples.
- 📜 [Full Resume Template](file:///c:/Users/prave/Desktop/projects/latex_applications/skills/latex-formatter/examples/full-resume-template.tex) - Minimal, error-free, compilable `.tex` template.
