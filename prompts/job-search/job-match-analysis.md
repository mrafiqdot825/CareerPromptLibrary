---
title: Job Match Analysis Matrix
category: Job Search
difficulty: Intermediate
use_case: Evaluating candidate qualification match against job postings to identify gaps and application viability
---

# Job Match Analysis Matrix

> Compare your actual background against a target job posting to uncover match strengths, skill gaps, and strategic application recommendations.

## What This Prompt Does

This prompt evaluates your resume against a job description. It generates a clear match assessment highlighting strong matches, partial matches, missing requirements, and key gaps, while providing actionable advice on how to address those gaps in your cover letter or interview.

## Best For

- Deciding whether to apply for a role.
- Preparing to address skill or experience gaps proactively during interviews.
- Understanding how recruiters will evaluate your application background.

## Information You Need

- Your Current Resume Text
- Target Job Description Text

## Copy & Paste Prompt

```text
Act as a hiring manager and career placement consultant.

TASK:
Perform a detailed match analysis comparing my resume background against the target job posting.

INPUT DATA:
- MY RESUME: [WORK_EXPERIENCE]
- JOB DESCRIPTION: [JOB_DESCRIPTION]

EVALUATION MATRIX:
1. Strong Matches: Requirements where my experience directly aligns or exceeds expectations.
2. Partial Matches: Requirements where I have transferable or related experience, but not an exact title/tool match.
3. Missing Requirements & Skill Gaps: Hard or soft requirements present in the job description but absent from my resume.
4. Strategic Mitigation Advice: How to address or offset partial matches and missing requirements in my cover letter or interview.
5. Overall Fit Assessment: Objective qualitative evaluation of application strength (Strong Fit, Potential Fit with Bridge Needed, or High Gap Risk).

CONSTRAINTS:
- Do NOT present arbitrary or fake match score percentages as factual metrics.
- Provide honest, objective feedback without sugarcoating qualification gaps.

OUTPUT FORMAT:
Structured Markdown report featuring a comparison matrix table followed by strategic advice.
```

## How to Use

1. Copy the prompt block above.
2. Paste your resume into `[WORK_EXPERIENCE]` and the job text into `[JOB_DESCRIPTION]`.
3. Run the prompt in your AI assistant.
4. Review the gap analysis and adjust your application strategy accordingly.

## Expected Output

A comparison table detailing match categories alongside practical suggestions for framing transferable skills.

## Tips

- Use the "Partial Matches" section to write your cover letter's main body paragraph.
- Address missing hard requirements honestly in interviews by emphasizing fast learning capability.

## Notes

- Match assessments are qualitative tools designed to aid preparation, not absolute hiring guarantees.
