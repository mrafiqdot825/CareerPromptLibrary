# Contributing to CareerPromptLibrary

Thank you for your interest in contributing to **CareerPromptLibrary**! Our goal is to maintain a high-quality, practical, open-source collection of copy-paste-ready AI prompts that empower job seekers, professionals, students, and freelancers worldwide.

---

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please report any unacceptable behavior to repository maintainers.

---

## What Makes a Good Prompt?

Every prompt in this library must be:

- **Practical & Actionable**: Solves a real career, job search, or workplace challenge.
- **Copy-Paste Ready**: Works out of the box with minimal customization.
- **Truthful & Grounded**: Strict prohibition against inventing achievements, fake degrees, or false employment history.
- **Model-Agnostic**: Works smoothly across ChatGPT, Claude, Gemini, DeepSeek, and other LLMs.
- **Human-Centric**: Free from robotic AI jargon or hyperbolic buzzwords ("revolutionary", "unbeatable").
- **No Unrealistic Guarantees**: We never claim a prompt "guarantees a job" or "ensures a 100% interview rate".

---

## Placeholder Convention

All prompts **MUST** use uppercase snake-case surrounded by square brackets for variable fields:

```text
[YOUR_NAME]
[TARGET_JOB_TITLE]
[COMPANY_NAME]
[YEARS_OF_EXPERIENCE]
[WORK_EXPERIENCE]
[SKILLS]
[JOB_DESCRIPTION]
```

Do **NOT** use formats such as `<name>`, `{name}`, `YOUR NAME HERE`, or `xxx`.

---

## File Structure & Naming Conventions

All prompt files live within subdirectories inside `prompts/`:

```text
prompts/
├── resume/
├── cover-letter/
├── job-search/
├── linkedin/
├── interviews/
├── career-planning/
├── education/
├── freelancing/
└── workplace/
```

### File Naming Rules
- Use lowercase kebab-case for filenames: `ats-resume.md`, `behavioral-interview.md`.
- Keep names concise and descriptive.

---

## Prompt File Standard Structure

Every prompt file must begin with YAML frontmatter, followed by the standardized markdown sections:

```markdown
---
title: Prompt Title
category: Category Name
difficulty: Beginner | Intermediate | Advanced
use_case: Specific Use Case Description
---

# Prompt Title

> A concise 1-2 sentence tagline summarizing the prompt.

## What This Prompt Does

Explain the specific purpose and outcome in 2-4 clear sentences.

## Best For

- Use case 1
- Use case 2
- Use case 3

## Information You Need

List all details the user needs to gather before running the prompt.

## Copy & Paste Prompt

```text
[Full structured prompt text using standard placeholders]
```

## How to Use

1. Copy the text block above.
2. Replace all `[PLACEHOLDER]` fields with your actual details.
3. Paste into your preferred AI model.
4. Review and refine the output.

## Expected Output

Describe the format, structure, and tone of the response produced by the AI.

## Tips

- Useful tip 1
- Useful tip 2

## Notes

List model considerations, verification steps, or limitations.
```

Refer to [`templates/prompt-template.md`](templates/prompt-template.md) as a starting point.

---

## How to Submit a Pull Request

1. **Fork the Repository**: Create a personal fork on GitHub.
2. **Create a Branch**: `git checkout -b feat/add-new-prompt-name`
3. **Add or Edit Prompt**: Create your markdown file following the [Prompt File Standard Structure](#prompt-file-standard-structure).
4. **Test Your Prompt**:
   - Run the prompt with realistic, non-fabricated inputs on at least two major AI models (e.g., ChatGPT and Claude).
   - Ensure the output meets quality guidelines.
5. **Check Metadata & Links**: Verify frontmatter parameters and ensure all file paths match.
6. **Submit PR**: Fill out the [Pull Request Template](.github/pull_request_template.md).

Thank you for helping build a better, more accessible career resource for everyone!
