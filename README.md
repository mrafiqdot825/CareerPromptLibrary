# CareerPromptLibrary

<p align="center">
  <strong>The open-source, production-grade AI prompt toolkit for job seekers, professionals, students, and freelancers.</strong>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-Welcome-brightgreen.svg" alt="PRs Welcome"></a>
  <img src="https://img.shields.io/badge/Prompts-45%2B%20Curated-orange.svg" alt="Prompts Count">
  <img src="https://img.shields.io/badge/Categories-9%20Domains-purple.svg" alt="Categories">
  <img src="https://img.shields.io/badge/AI%20Compatibility-ChatGPT%20%7C%20Claude%20%7C%20Gemini%20%7C%20DeepSeek-informational.svg" alt="Model Agnostic">
  <img src="https://img.shields.io/badge/Truthfulness-0%25%20Fabrication-red.svg" alt="Zero Fabrication">
</p>

---

## Repository Metrics & Overview

| Total Prompts | Categories | Model Compatibility | Safety Standard | License |
| :---: | :---: | :---: | :---: | :---: |
| **45+ Prompts** | **9 Categories** | **100% Agnostic** | **Zero Fabrication** | **MIT Open Source** |

---

## Table of Contents

- [About The Project](#-about-the-project)
- [Start Here (Quick Paths)](#-start-here-quick-paths)
- [Prompt Categories & Directory](#-prompt-categories--directory)
- [Featured Prompts](#-featured-prompts)
- [Example Usage](#-example-usage)
- [How It Works](#%EF%B8%8F-how-it-works)
- [Supported AI Tools](#%EF%B8%8F-supported-ai-tools)
- [Quality & Engineering Standards](#-quality--engineering-standards)
- [Contributing & Community Statistics](#-contributing--community-statistics)
- [License & Disclaimer](#-license--disclaimer)

---

## About The Project

Most AI career prompts on the internet suffer from three core flaws: they produce generic fluff (*"Make my resume sound executive"*), depend on model-specific hacks, or encourage AI to fabricate fake achievements and metrics.

**CareerPromptLibrary** is a community-driven, production-grade prompt collection built on rigorous prompt engineering standards. Every prompt is:

- 🟢 **Copy-Paste Ready**: Standardized `[UPPERCASE_SNAKE_CASE]` placeholders.
- 🟢 **Truthful & Grounded**: Strict anti-hallucination rules prevent inventing titles, degrees, or metrics.
- 🟢 **Model-Agnostic**: Works seamlessly across ChatGPT, Claude, Gemini, DeepSeek, and open LLMs.
- 🟢 **Human-Centric**: Free from robotic AI clichés ("synergistic leader", "revolutionary guru").

---

## Start Here (Quick Paths)

Choose your primary career goal for a fast-track prompt recommendation:

| Your Goal | Recommended Prompt | What It Accomplishes |
| :--- | :--- | :--- |
| **Tailor resume for an ATS posting** | [`prompts/resume/ats-resume.md`](prompts/resume/ats-resume.md) | Generates an ATS-compliant resume + 5-point match report. |
| **Practice for an upcoming interview** | [`prompts/interviews/mock-interview.md`](prompts/interviews/mock-interview.md) | Runs an interactive, one-question-at-a-time mock interview. |
| **Pivot into a new career or field** | [`prompts/career-planning/career-change.md`](prompts/career-planning/career-change.md) | Audits transferable skills & constructs a transition blueprint. |
| **Pitch freelance client proposals** | [`prompts/freelancing/freelance-proposal.md`](prompts/freelancing/freelance-proposal.md) | Writes customized project proposals addressing client goals. |
| **Ask for a raise or promotion** | [`prompts/workplace/promotion-request.md`](prompts/workplace/promotion-request.md) | Builds a data-backed business case & verbal script. |

---

## Prompt Categories & Directory

Explore our full prompt collection across 9 specialized domains:

| Category | Files | Description | Primary Prompts |
| :--- | :---: | :--- | :--- |
| **[Resume](prompts/resume/)** | `7` | ATS optimization, summary statements, impact bullet points | [`ats-resume.md`](prompts/resume/ats-resume.md) • [`resume-tailoring.md`](prompts/resume/resume-tailoring.md) • [`resume-bullet-points.md`](prompts/resume/resume-bullet-points.md) |
| **[Cover Letter](prompts/cover-letter/)** | `3` | Job-specific, cold outreach, and general cover letters | [`cover-letter.md`](prompts/cover-letter/cover-letter.md) • [`job-specific-cover-letter.md`](prompts/cover-letter/job-specific-cover-letter.md) |
| **[Job Search](prompts/job-search/)** | `5` | Posting analysis, candidate fit matrix, search strategy | [`job-search-strategy.md`](prompts/job-search/job-search-strategy.md) • [`job-description-analysis.md`](prompts/job-search/job-description-analysis.md) |
| **[LinkedIn](prompts/linkedin/)** | `5` | SEO profile optimization, headlines, About narrative | [`linkedin-profile.md`](prompts/linkedin/linkedin-profile.md) • [`linkedin-headline.md`](prompts/linkedin/linkedin-headline.md) |
| **[Interviews](prompts/interviews/)** | `6` | Interactive mock simulator, STAR responses, questions | [`mock-interview.md`](prompts/interviews/mock-interview.md) • [`behavioral-interview.md`](prompts/interviews/behavioral-interview.md) |
| **[Career Planning](prompts/career-planning/)** | `5` | Milestones, career pivots, skill gap audits, 5-year plans | [`career-roadmap.md`](prompts/career-planning/career-roadmap.md) • [`career-change.md`](prompts/career-planning/career-change.md) |
| **[Education](prompts/education/)** | `5` | Technical study schedules, self-taught roadmaps, scholarships | [`study-plan.md`](prompts/education/study-plan.md) • [`scholarship-application.md`](prompts/education/scholarship-application.md) |
| **[Freelancing](prompts/freelancing/)** | `4` | Marketplace profiles, proposal bids, cold outreach pitches | [`freelancer-profile.md`](prompts/freelancing/freelancer-profile.md) • [`freelance-proposal.md`](prompts/freelancing/freelance-proposal.md) |
| **[Workplace](prompts/workplace/)** | `5` | Performance reviews, promotion business cases, emails | [`performance-review.md`](prompts/workplace/performance-review.md) • [`promotion-request.md`](prompts/workplace/promotion-request.md) |

---

## Featured Prompts

Here are 4 of the most popular prompts in the library:

1. **[ATS Resume Generator](prompts/resume/ats-resume.md)**
   - Rebuilds work history to match job description keywords, providing both a **Compact 5-Point Optimization Prompt** and a **Detailed Deep-Dive Generator**.
2. **[Interactive Mock Interview Simulator](prompts/interviews/mock-interview.md)**
   - Turns your AI assistant into an interviewer that asks questions one at a time, scores responses 1–5, and provides feedback.
3. **[Job Match Analysis Matrix](prompts/job-search/job-match-analysis.md)**
   - Evaluates your resume against a target job description to highlight strong matches, partial matches, missing skills, and strategic advice.
4. **[Promotion & Salary Raise Business Case](prompts/workplace/promotion-request.md)**
   - Builds a formal written business case and verbal 1-on-1 meeting script for requesting a promotion or raise.

---

## Example Usage

### Input Prompt (From [`prompts/resume/resume-summary.md`](prompts/resume/resume-summary.md))

```text
Act as a professional resume editor and talent acquisition manager.

INPUT DATA:
- Target Job Title: Senior Frontend Engineer
- Years of Experience: 6 Years
- Primary Field / Industry: E-Commerce & SaaS
- Core Strengths & Key Skills: React, TypeScript, Performance Optimization, Team Mentorship
- Major Career Highlights: Improved checkout page load times by 40%
```

### AI Output Produced

> **Senior Frontend Engineer** with 6 years of experience building high-performance web applications across e-commerce and SaaS platforms. Specialized in React, TypeScript, and front-end performance optimization, with a proven track record of cutting page load times by 40% to drive user conversion. Experienced in mentoring junior developers and collaborating closely with product teams to deliver scalable user interfaces.

---

## How It Works

```text
┌───────────────────────────┐
│ 1. Select Prompt File     │ (e.g., prompts/resume/ats-resume.md)
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ 2. Prepare Data Inputs    │ (Use templates/resume-input-template.md)
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ 3. Customize Placeholders │ (Replace [YOUR_NAME], [JOB_DESCRIPTION], etc.)
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ 4. Run in AI Model        │ (Paste into ChatGPT, Claude, Gemini, or DeepSeek)
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│ 5. Review & Verify Output │ (Fact-check titles, dates, and metrics)
└───────────────────────────┘
```

For complete step-by-step workflow guidance, visit the **[Getting Started Guide](docs/getting-started.md)**.

---

## Supported AI Tools

All prompts in this repository are **model-agnostic** and do not depend on proprietary AI extensions:

- **OpenAI**: ChatGPT (GPT-4o, GPT-4o-mini, GPT-3.5)
- **Anthropic**: Claude (Claude 3.5 Sonnet, Claude 3 Opus, Claude 3 Haiku)
- **Google**: Gemini (Gemini 1.5 Pro, Gemini 1.5 Flash)
- **Open-Source & Local Models**: DeepSeek-V3 / R1, Meta Llama 3, Mistral, Perplexity

---

## Quality & Engineering Standards

Every prompt contributed to **CareerPromptLibrary** follows 5 core rules:

1. **Zero Fabrication**: AI must never invent degrees, companies, credentials, or metrics.
2. **Standardized Placeholders**: All variables strictly use `[UPPERCASE_SNAKE_CASE]`.
3. **Model Independence**: No proprietary syntax or platform-locked formatting.
4. **Natural Human Voice**: No robotic buzzwords ("synergy", "rockstar", "ninja").
5. **No Unrealistic Guarantees**: Honest, practical prompts designed for real-world application.

Read our full **[Prompt Engineering Guide](docs/prompt-writing-guide.md)** to learn more.

---

## Contributing & Community Statistics

Contributions are welcome! Whether you want to add a new prompt, fix formatting, or improve documentation:

- Review the **[Contributing Guidelines](CONTRIBUTING.md)**.
- Use the **[Standard Prompt Template](templates/prompt-template.md)**.
- Submit feature requests or report bugs via **[GitHub Issue Templates](.github/ISSUE_TEMPLATE/)**.
- Follow our **[Code of Conduct](CODE_OF_CONDUCT.md)**.

---

## Helper Templates

Organize your information cleanly before running prompts:

- [`templates/resume-input-template.md`](templates/resume-input-template.md): Formatted text block for organizing your work history.
- [`templates/job-description-template.md`](templates/job-description-template.md): Formatted text block for structuring job postings.

---

## Frequently Asked Questions

Have questions about commercial usage, privacy, or prompt customization? Visit the **[FAQ Document](docs/faq.md)**.

---

## License & Disclaimer

- **License**: This project is licensed under the open-source **[MIT License](LICENSE)**.
- **Disclaimer**: The prompts in this repository assist users in structuring and drafting career materials. AI-generated content should always be reviewed and verified by the user prior to submission. CareerPromptLibrary makes no guarantee of employment, job offers, or interview invitations.
