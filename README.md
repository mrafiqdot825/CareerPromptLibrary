# CareerPromptLibrary

> A collection of practical, copy-paste-ready AI prompts for careers, jobs, education, and professional growth.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**CareerPromptLibrary** is a curated, open-source library of high-quality AI prompts engineered to help job seekers, working professionals, students, and freelancers achieve real-world career results.

---

## Why CareerPromptLibrary?

Most career prompts found online are either too generic (*"make my resume sound better"*), overly complex, or force AI models to hallucinate fake metrics and credentials. 

**CareerPromptLibrary** fixes this by adhering to strict prompt engineering standards:

* **Copy-Paste Ready**: Fill in clearly marked `[PLACEHOLDER]` fields and get instant, useful outputs.
* **Truthful & Grounded**: Built-in safeguards prohibit AI models from inventing fake degrees, companies, or metrics.
* **Model-Agnostic**: Tested to work reliably across ChatGPT, Claude, Gemini, DeepSeek, and other LLMs.
* **Human Tone**: Free from robotic AI clichés ("synergistic leader", "revolutionary thinker").
* **No Unrealistic Guarantees**: Honest, practical prompts designed to showcase your real experience.

---

## Who Is This For?

- **Job Seekers**: Tailor resumes to ATS screeners, generate targeted cover letters, and track application strategy.
- **Working Professionals**: Prepare for performance reviews, build promotion business cases, and draft clear workplace emails.
- **Students & Graduates**: Craft internship applications, scholarship personal statements, and technical study plans.
- **Freelancers & Consultants**: Write high-converting marketplace profiles, project proposals, and cold outreach pitches.
- **Career Switchers**: Audit transferable skills and construct step-by-step career transition roadmaps.

---

## How to Use the Prompts

Using prompts from this repository follows a simple 5-step workflow:

```text
Select a Prompt
       │
       ▼
Gather Information & Open Template
       │
       ▼
Replace [UPPERCASE_SNAKE_CASE] Placeholders
       │
       ▼
Paste into ChatGPT / Claude / Gemini
       │
       ▼
Review & Verify Factual Accuracy
```

For detailed instructions, see the **[Getting Started Guide](docs/getting-started.md)**.

---

## Prompt Categories & Navigation

Explore our complete prompt collection organized by category:

| Category | Description | Key Prompts |
| :--- | :--- | :--- |
| **[Resume](prompts/resume/)** | ATS optimization, summaries, bullet points, tailoring | [`ats-resume.md`](prompts/resume/ats-resume.md), [`resume-tailoring.md`](prompts/resume/resume-tailoring.md), [`resume-bullet-points.md`](prompts/resume/resume-bullet-points.md) |
| **[Cover Letter](prompts/cover-letter/)** | General, job-specific, and speculative outreach letters | [`cover-letter.md`](prompts/cover-letter/cover-letter.md), [`job-specific-cover-letter.md`](prompts/cover-letter/job-specific-cover-letter.md) |
| **[Job Search](prompts/job-search/)** | Posting analysis, fit matrix, multi-channel strategy | [`job-search-strategy.md`](prompts/job-search/job-search-strategy.md), [`job-description-analysis.md`](prompts/job-search/job-description-analysis.md) |
| **[LinkedIn](prompts/linkedin/)** | SEO profiles, headlines, About summaries, post creation | [`linkedin-profile.md`](prompts/linkedin/linkedin-profile.md), [`linkedin-headline.md`](prompts/linkedin/linkedin-headline.md) |
| **[Interviews](prompts/interviews/)** | Interactive mock interviews, STAR responses, questions to ask | [`mock-interview.md`](prompts/interviews/mock-interview.md), [`behavioral-interview.md`](prompts/interviews/behavioral-interview.md) |
| **[Career Planning](prompts/career-planning/)** | Career roadmaps, transition strategy, 5-year plans | [`career-roadmap.md`](prompts/career-planning/career-roadmap.md), [`career-change.md`](prompts/career-planning/career-change.md) |
| **[Education](prompts/education/)** | Study schedules, self-taught roadmaps, scholarships | [`study-plan.md`](prompts/education/study-plan.md), [`scholarship-application.md`](prompts/education/scholarship-application.md) |
| **[Freelancing](prompts/freelancing/)** | Profiles, proposal bids, cold outreach, niche positioning | [`freelancer-profile.md`](prompts/freelancing/freelancer-profile.md), [`freelance-proposal.md`](prompts/freelancing/freelance-proposal.md) |
| **[Workplace](prompts/workplace/)** | Emails, meeting agendas, reviews, promotion cases | [`performance-review.md`](prompts/workplace/performance-review.md), [`promotion-request.md`](prompts/workplace/promotion-request.md) |

---

## Featured Prompts

Here are 4 of the most popular prompts to get started immediately:

1. **[ATS Resume Generator](prompts/resume/ats-resume.md)**: Rebuilds your work history to match job description keywords while preserving 100% factual accuracy.
2. **[Interactive Mock Interview Simulator](prompts/interviews/mock-interview.md)**: Turns your AI model into an interviewer that asks questions one-by-one and provides immediate feedback.
3. **[Job Match Analysis Matrix](prompts/job-search/job-match-analysis.md)**: Evaluates your resume against a target posting to highlight strong matches, partial matches, and skill gaps.
4. **[Promotion & Salary Raise Business Case](prompts/workplace/promotion-request.md)**: Constructs a data-backed business case and verbal script for requesting a title promotion or raise.

---

## Example Usage

### Input (From [`prompts/resume/resume-summary.md`](prompts/resume/resume-summary.md))

```text
Act as a professional resume editor and talent acquisition manager.

INPUT DATA:
- Target Job Title: Senior Frontend Engineer
- Years of Experience: 6 Years
- Primary Field / Industry: E-Commerce & SaaS
- Core Strengths & Key Skills: React, TypeScript, Performance Optimization, Team Mentorship
- Major Career Highlights: Improved checkout page load times by 40%
```

### Output Produced by AI

> **Senior Frontend Engineer** with 6 years of experience building high-performance web applications across e-commerce and SaaS platforms. Specialized in React, TypeScript, and front-end performance optimization, with a proven track record of cutting page load times by 40% to drive user conversion. Experienced in mentoring junior developers and collaborating closely with product teams to deliver scalable user interfaces.

---

## Supported AI Tools

All prompts in this library are **model-agnostic** and do not rely on proprietary AI features. They work with:

- **OpenAI**: ChatGPT (GPT-4o, GPT-4o-mini, GPT-3.5)
- **Anthropic**: Claude (Claude 3.5 Sonnet, Claude 3 Opus, Claude 3 Haiku)
- **Google**: Gemini (Gemini 1.5 Pro, Gemini 1.5 Flash)
- **Open-Source & Other Models**: DeepSeek, Meta Llama 3, Mistral, Perplexity

---

## Prompt Quality Guidelines

Every prompt in this repository adheres to 5 strict quality guidelines:

1. **Rule of Truthfulness**: The AI must never invent degrees, companies, credentials, or metrics.
2. **Standard Placeholders**: All variable fields use `[UPPERCASE_SNAKE_CASE]`.
3. **Model Independence**: No proprietary syntax or platform-locked formatting.
4. **Natural Human Tone**: No artificial buzzwords ("synergy", "rockstar", "revolutionary").
5. **No Fake Claims**: No promises of "100% guaranteed interviews" or "impossible to reject" claims.

For details, read our **[Prompt Engineering Guide](docs/prompt-writing-guide.md)**.

---

## Contributing

We welcome contributions from prompt engineers, recruiters, technical writers, and career coaches! 

- Read our **[Contributing Guidelines](CONTRIBUTING.md)** to learn how to submit new prompts or improve existing ones.
- Check our **[Prompt Template](templates/prompt-template.md)** for standard file structure.
- Adhere to our **[Code of Conduct](CODE_OF_CONDUCT.md)**.

---

## Helper Templates

Before running prompts, organize your information using our helper templates:

- [`templates/resume-input-template.md`](templates/resume-input-template.md): Gather your work history and skills.
- [`templates/job-description-template.md`](templates/job-description-template.md): Clean and structure target job postings.

---

## Frequently Asked Questions

Have questions about commercial usage, privacy, or prompt customization? Read our **[FAQ Document](docs/faq.md)**.

---

## Disclaimer

> **Disclaimer**: The prompts provided in this repository are designed to assist users in structuring, drafting, and optimizing career and application materials. AI-generated content should always be reviewed, edited, and verified by the user prior to submission. CareerPromptLibrary makes no guarantee of employment, job offers, interview calls, or financial advancement.

---

## License

This project is licensed under the open-source **[MIT License](LICENSE)**. Feel free to use, modify, and distribute these prompts for personal or commercial projects.
