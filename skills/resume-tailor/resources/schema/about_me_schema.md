# About Me Schema & Parsing Blueprint

When parsing a user's raw resume into `about_me.md`, use the following structure. Every section should be comprehensive and act as the single source of truth for all future resume and cover letter tailoring.

```markdown
# About Me

**[Full Legal Name]**
[City, Country]

- Mobile: [Phone Number]
- Email: [Email Address]
- LinkedIn: [[Username]]([Full LinkedIn URL])
- GitHub / Portfolio: [[Username]]([Full URL])
- Nationality: [Nationality]

---

## Professional Summary
[A 2-3 sentence high-impact summary covering current focus, core strengths, domain expertise, and career aspirations.]

---

## Technical Expertise
- **Languages:** [e.g., Python, C++, SQL, TypeScript, Bash]
- **AI / ML / Data:** [e.g., PyTorch, TensorFlow, LLMs, RAG, HuggingFace, Scikit-Learn]
- **Cloud & DevOps:** [e.g., AWS, GCP, Azure, Docker, Kubernetes, CI/CD]
- **Databases:** [e.g., PostgreSQL, Redis, Qdrant, MongoDB]
- **Frameworks & Tools:** [e.g., FastAPI, React, Git, Linux]

---

## Experience

### [Company Name]
*[Location] | [Employment Type: Full-time / Internship / Working Student] | [Start Date – End Date or Present]*
- **[Job Title / Role]**
  - [Strong Action Verb] [core task/system built] using [technologies], achieving [quantified metric/outcome].
  - [Strong Action Verb] [core task/system built] using [technologies], achieving [quantified metric/outcome].

---

## Education

### [Degree & Major]
*[University / Institution Name] | [City, Country] | [Start Year – End Year]*
- Grade / GPA: [Grade / GPA if applicable]
- Key Focus: [Relevant coursework or research topics]

---

## Projects

### [Project Name]
*[Tech Stack: Tool 1, Tool 2, Tool 3] | [GitHub / Demo Link]*
- [Problem solved and architecture built.]
- [Measurable impact, performance benchmark, or outcome achieved.]

---

## Leadership, Certifications & Languages
- **Certifications:** [e.g., Google Cloud Certified, AWS Solutions Architect]
- **Languages:** [e.g., English (Fluent), German (B2), Hindi (Native)]
- **Leadership & Community:** [e.g., Hackathon winner, student club lead, open-source contributor]
```

### Parsing Rules for the Agent:
1. **Never Invent Facts:** Extract only what is present in the user's provided resume text or uploaded file.
2. **Preserve Dates & Metrics:** Keep exact dates, percentages, and metrics.
3. **Format Bullet Points:** If the user's original bullets are weak, apply the Action Verb + Task + Tool + Metric formula to format them cleanly into `about_me.md`.
