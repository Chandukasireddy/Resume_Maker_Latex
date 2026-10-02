# LaTeX Editing & Layout Integrity Rules

LaTeX resumes look professional only when spacing, geometry, and section alignments remain pixel-perfect. When tailoring `.tex` files, follow these strict constraints.

---

## Allowed Sections for Editing in Resume

When tailoring `[your_name]_resume.tex`, modify **ONLY** these sections:
1. `Role` line under the candidate's name (e.g., `\large{...}`) — update only if justified by the JD alignment.
2. `Profile` / Summary statement.
3. `Professional Experience` bullet points.
4. `Skills` and skill groupings.

### Strict Non-Negotiable Constraints:
- **No Structural Alteration:** Do not add or delete sections. Do not alter fonts, margins, column widths, packages, or document geometry.
- **Strict 1-Page Constraint:** The compiled document must fit onto exactly ONE page.
- **Character Length Limits:**
  - `Profile` statement: Maximum **330 characters** total (including spaces).
  - Each `Professional Experience` bullet point: Maximum **150 characters** (including spaces).
  - If a tailored bullet point exceeds 150 characters, rephrase concisely without losing key metrics or keywords.
- **Preserve Bullet Count:** Reword existing bullet points for maximum relevance to the JD; do not arbitrarily inflate or cut the number of bullets.
- **Escape Special Characters:** Always escape LaTeX reserved characters:
  - `&` → `\&`
  - `%` → `\%`
  - `$` → `\$`
  - `_` → `\_`
  - `#` → `\#`

---

## Cover Letter Constraints

When tailoring `[your_name]_cover-letter.tex`:
- **Preserve Template Layout:** Keep header macros, signature blocks, and spacing untouched.
- **Two Paragraphs Body:** The body of the letter must contain **exactly two paragraphs**:
  - *Paragraph 1:* Motivation, interest in the company's specific mission/product, and direct alignment of your core expertise with the role.
  - *Paragraph 2:* Concrete achievements and impactful project examples extracted from `about_me.md` proving your ability to deliver immediate value.
- **Under One Page:** The entire letter, including header and signature, must fit cleanly on one single page.
- **No Hyphen En-Dashes:** Do not use `--` symbols.
- **Natural Tone:** Maintain an authentic, human professional tone. Avoid generic AI boilerplate (*"I am writing with great enthusiasm to express my sincere interest..."*).

---

## Experience Framing Rules

1. **For Full-Time Roles:**
   - Clearly highlight current professional industry engagement, leadership, and production system delivery.
2. **For Student / Graduate Roles (Thesis, Internship, Working Student):**
   - Explicitly mention enrolled student status (e.g. Master's candidate) combined with ongoing practical experience.
