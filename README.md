# AACLP – AmritaConstant AIGC Content Licensing Policy

**Version:** 1.0  
**Published:** 2026

AACLP is an auxiliary policy for open‑source projects that want to govern contributions involving AI‑generated content (AIGC). It does not replace your primary open‑source license (MIT, GPL, Apache‑2.0, etc.) – instead, it adds a clear, enforceable framework for **responsibility, review, and transparency** when AI tools are used in development.

---

## Why AACLP?

Existing open‑source licenses were written before AI assistants became widespread. They do not answer fundamental questions:

- Who is responsible if AI‑generated code contains a bug or vulnerability?
- Can an AI tool approve a pull request?
- Does the AI service provider enter the project’s chain of liability?

AACLP answers these directly. It is designed to be **practical**, not prohibitive – it allows AI assistance while keeping **human accountability** at the centre.

---

## Core Principles

- **AI is a tool, not an author** – AI assistants are on par with compilers or linters; they carry no responsibility for the output.
- **Human beings are always the final helmsmen** – Every contributor who uses AI takes full responsibility for what they submit.
- **Core business logic prefers human authorship** – If AI is used for critical parts, the contributor must be able to explain the logic line‑by‑line when asked.
- **Review approval must be human** – AI may assist (comment, suggest), but the final `approve` or `merge` decision must be made by a natural person.

---

## Recommended File Placement

We **strongly recommend** that projects adopting this policy place the full license text in a file named:

```
POLICY_OF_AIGC
```

(at the repository root). This makes the policy’s purpose immediately recognisable and keeps it separate from the main software license (e.g., `LICENSE`).

---

## Quick Start for Project Maintainers

### 1. Add the policy file

Copy the full AACLP text into `POLICY_OF_AIGC` in your repository root.

### 2. Declare it in your README

Add a short section to your project’s `README.md`:

```markdown
## AI‑Generated Content Policy

This project follows the [AACLP v1.0](./POLICY_OF_AIGC) for all AI‑assisted contributions. By submitting content, contributors agree to its terms.
```

### 3. (Optional) Provide specific guidance in `CONTRIBUTING.md`

As allowed by **Article 1.4**, maintainers should define what constitutes “Core Business Logic” for their project. Example:

```markdown
## AI Contribution Guidelines

Under AACLP, the following are considered Core Business Logic:
- All code under `src/core/`
- Authentication, payment, and encryption modules
- Database migration scripts

AI‑generated contributions to these areas must satisfy Article 3.2 (understanding, responsibility, and additional review).
```

---

## Summary of Articles

| Article | Subject |
|---------|---------|
| **1** | Definitions (AIGC, Contributor, Maintainer, Core Business Logic) |
| **2** | AI tools as development toolchain; service providers not liable; ultimate human responsibility |
| **3** | Core logic: human‑written preferred; AI allowed if contributor can explain, takes responsibility, and accepts extra review |
| **4** | Documentation: AI drafts allowed, but final version must be factually accurate |
| **5** | Tests: AI may generate test cases; they must provide real coverage and no dummy assertions |
| **6** | All AI‑assisted content must be reviewed by a human; the reviewer cannot be an AI tool (approval power reserved for humans) |
| **7** | Severability; revisions require maintainer approval and changelog |

> Read the full text in [`POLICY_OF_AIGC`](./POLICY_OF_AIGC).

---

## Frequently Asked Questions

**Q: Does AACLP replace my existing open‑source license?**  
No. It is an **additional policy**. Your primary license (e.g., MIT, GPL) governs distribution terms; AACLP governs how AI‑generated contributions are submitted and reviewed.

**Q: “Reviewer must not be an AI tool” – does that ban AI‑powered code review bots?**  
Not at all. AI may act as an **assistant** – scanning code, leaving comments, suggesting changes – as part of your CI/CD pipeline. The prohibition applies only to the **final approval decision** (the act of merging or accepting). That decision must be made by a human.

**Q: “Able to explain line by line” – do I have to write a long explanation for every PR?**  
No. The wording uses **“able to”** (a cognitive requirement), not **“shall”** (a documentation requirement). You are not required to attach a written essay every time. However, if a maintainer questions your contribution, you must be capable of explaining the logic orally or in writing upon request.

**Q: What if my AI service provider’s terms conflict with AACLP?**  
AACLP takes precedence within the project. Article 2.2 explicitly excludes service providers from the project’s responsibility chain. Contributors are responsible for ensuring their tool usage does not violate the project’s policies.

---

## Versioning and Revisions

- **v1.0** (2026) – initial release.

Future revisions must be reviewed and approved by the Maintainer, with a changelog recorded.

---

## Author

**AmritaConstant**

---

## Contributing to This Policy

Issues and pull requests are welcome. For substantial changes, please explain the rationale and expected impact.

---

## Disclaimer

This document is provided “as is” and does not constitute legal advice. Projects should consult qualified legal counsel before adopting it in their specific jurisdiction.
