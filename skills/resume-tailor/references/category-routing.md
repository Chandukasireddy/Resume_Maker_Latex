# Category Routing Rules

Every new job application must be categorized into exactly one subfolder under `applications/`. Never place application folders directly in the root of `applications/`.

---

## Routing Priority Order

1. **`applications/master-thesis/`**
   - **Keywords:** master thesis, masterarbeit, thesis, master's thesis, Abschlussarbeit Master.
   - **Usage:** Academic graduation thesis projects conducted at universities or partner corporations.

2. **`applications/phd/`**
   - **Keywords:** PhD, doctoral, doctorate, doktorand, research assistant (doctoral level).
   - **Usage:** Post-graduate doctoral research applications and fellowships.

3. **`applications/werk-student/`**
   - **Keywords:** werkstudent, working student, studentische hilfskraft, student worker, hiwi.
   - **Usage:** Part-time employment in Germany specifically reserved for enrolled university students (up to 20 hrs/week).

4. **`applications/internship/`**
   - **Keywords:** intern, internship, praktikant, praktikum, mandatory internship, freiwilliges praktikum.
   - **Usage:** Short-term training or seasonal industry internships.

5. **`applications/full-time/`**
   - **Default:** Use for all permanent, contract, regular engineering, and non-student industry roles when none of the above categories apply.

---

## Folder Naming Convention

- Always create the folder using lowercase hyphenated format:
  `applications/<category>/<company-role>/`
- Make `<company-role>` descriptive to avoid namespace clashes:
  - ✅ `applications/full-time/bmw-senior-ai-engineer-genai/`
  - ✅ `applications/master-thesis/siemens-generative-ai-benchmarking/`
  - ❌ `applications/full-time/bmw/` (Too generic)
