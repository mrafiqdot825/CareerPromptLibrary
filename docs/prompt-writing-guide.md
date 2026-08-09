# Prompt Engineering Standard & Writing Guide

This document outlines the design architecture and prompt engineering guidelines used throughout **CareerPromptLibrary**. Use this guide when customizing existing prompts or contributing new ones.

---

## Anatomy of a High-Quality Prompt

Every prompt in this repository adheres to a 9-part structured architecture:

```text
┌─────────────────────────────────────────────────────────┐
│ 1. Role Assignment (e.g., "Act as an expert recruiter") │
├─────────────────────────────────────────────────────────┤
│ 2. Objective / Task Definition                          │
├─────────────────────────────────────────────────────────┤
│ 3. Context & Background                                 │
├─────────────────────────────────────────────────────────┤
│ 4. Input Data & Structured Placeholders                 │
├─────────────────────────────────────────────────────────┤
│ 5. Strict Constraints & Quality Rules                   │
├─────────────────────────────────────────────────────────┤
│ 6. Step-by-Step Processing Directives                   │
├─────────────────────────────────────────────────────────┤
│ 7. Explicit Output Formatting Requirements               │
├─────────────────────────────────────────────────────────┤
│ 8. Ground Truth / No Fabrication Safeguards              │
├─────────────────────────────────────────────────────────┤
│ 9. Missing Data Handling Directives                      │
└─────────────────────────────────────────────────────────┘
```

---

## Core Design Principles

### 1. Zero-Fabrication Safeguard (Rule of Truthfulness)
The single most important rule across all prompts is enforcing truthfulness:
- The AI must **NEVER** fabricate dates, job titles, companies, degrees, certifications, or metrics.
- If necessary information is missing from user input, the prompt instructs the AI to either insert a `[MISSING: detail]` tag or explicitly request the information.

### 2. Standardized Placeholder System
Maintainers and users must use consistent `[UPPERCASE_SNAKE_CASE]` identifiers:
- Correct: `[YOUR_NAME]`, `[TARGET_JOB_TITLE]`, `[WORK_EXPERIENCE]`
- Incorrect: `<name>`, `{name}`, `YOUR NAME HERE`, `[Name]`, `xxx`

### 3. Model Independence
Avoid model-specific syntax or proprietary features (such as OpenAI GPTs actions or Claude-only XML tags). Standard Markdown code blocks and structured bullet points work reliably across all AI systems.

### 4. Human Tone Over Hype
Prompts explicitly instruct the AI to write in clear, natural human language. Avoid robotic tropes such as:
- *"I am thrilled to apply for..."*
- *"A dynamic, results-driven synergy leader..."*
- Excessive buzzwords, overused metaphors, or emoji-heavy text.

### 5. Clear Constraints & Formatting Directives
Instruct the AI on exact structure (e.g., Markdown headers, bullet points, table formats) and negative constraints (e.g., "Do not exceed 300 words", "Do not repeat points from the resume word-for-word").

---

## Example Prompt Pattern

```text
Act as an expert ATS Resume Specialist and Career Strategist.

OBJECTIVE:
Tailor the user's provided resume to align tightly with the target job description.

INPUT DATA:
- Target Job Title: [TARGET_JOB_TITLE]
- Current Resume: [WORK_EXPERIENCE]
- Job Posting: [JOB_DESCRIPTION]

CONSTRAINTS:
1. Do not invent achievements, companies, or credentials.
2. Focus on action verbs and quantifiable results provided in the input.
3. Keep formatting clean and ATS-parseable.

OUTPUT FORMAT:
- Summary Section
- Key Keyword Matches
- Tailored Experience Bullet Points
```

---

## Summary

Following this prompt architecture guarantees that prompts remain reusable, maintainable, and capable of generating high-value outputs regardless of AI platform evolution.
