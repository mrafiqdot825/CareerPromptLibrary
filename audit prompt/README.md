# The Complete Production Code Audit Prompt Kit

*Turn any AI coding assistant into a full review team — Principal Engineer, Security Engineer, Staff Engineer, DevOps Engineer, Performance Engineer, QA Engineer, and Solutions Architect — before you ship.*

**By MRafiqdot825**

> **Model-agnostic by design.** These prompts use plain role instructions, not tool-specific syntax. Run them in Claude Code, Cursor, Windsurf, GitHub Copilot, ChatGPT, Gemini, or DeepSeek. For the deepest results, use a coding agent that can read your actual repository rather than pasted snippets.

---

## Table of Contents

1. [Objective](#objective)
2. [How to Use This Kit](#how-to-use-this-kit)
3. [Standard Issue Format](#standard-issue-format)
4. [The Master Audit Prompt](#the-master-audit-prompt)
5. [The 20 Individual Audit Prompts](#the-20-individual-audit-prompts)
6. [The Final Deliverables Prompt](#the-final-deliverables-prompt)
7. [Recommended Order to Run These](#recommended-order-to-run-these)
8. [Tips for Best Results](#tips-for-best-results)
9. [Closing Note](#closing-note)

---

## Objective

You are asking the AI to act as a **Principal Software Engineer, Security Engineer, Staff Engineer, DevOps Engineer, Performance Engineer, QA Engineer, and Solutions Architect** — all at once.

Its mission: perform a **complete production-grade review** of the entire repository before deployment.

Ground rules for every audit in this kit:

- Do **not** focus on formatting or stylistic preferences unless they affect maintainability or production quality.
- Identify every issue that could impact security, reliability, scalability, performance, developer experience, or long-term maintainability.
- Every issue gets a severity, a location, a real-world impact, and a recommended fix — never just a vague warning.

---

## How to Use This Kit

1. **Point the agent at the whole repo**, not a single pasted file. These prompts are written for full-codebase context — architecture, cross-file consistency, and dependency issues can't be caught from a snippet.
2. **Run the Master Audit Prompt first** for a full sweep. It compresses all 20 categories into one pass and gives you a triage list fast.
3. **Run individual audits when you need depth.** The Master Prompt is broad; each of the 20 focused prompts below goes deep on one area (security, performance, architecture, etc.) and will surface issues the broad pass skims past.
4. **Reuse the Standard Issue Format** for every prompt so findings stay consistent, sortable, and easy to hand to a team.
5. **Run this before every production deploy** — not just once at launch. Re-run the Security and Bug Hunter prompts after any significant feature merge.

---

## Standard Issue Format

Paste this once at the start of a session (or include it inside any prompt below) so every finding comes back in the same shape:

```
For every issue found, report it using this exact structure:

- Title
- Severity: Critical / High / Medium / Low
- Category
- Location: File / Folder / Function / Component
- Description
- Real-world Impact
- Recommended Fix
- Priority
- Estimated Effort: Small / Medium / Large

Do not skip fields. If a field genuinely does not apply, write "N/A"
rather than omitting it.
```

---

## The Master Audit Prompt

Run this when you want one complete pass across the entire codebase before a release.

```
Act as a Principal Software Engineer, Security Engineer, Staff Engineer,
DevOps Engineer, Performance Engineer, QA Engineer, and Solutions
Architect.

Perform a complete production-grade review of this entire repository
before deployment.

Do not focus on formatting or stylistic preferences unless they affect
maintainability or production quality. Your goal is to identify every
issue that could impact security, reliability, scalability,
performance, developer experience, or long-term maintainability.

Evaluate across these areas:
- Critical bugs and edge cases
- Architecture problems and layer violations
- Missing validation and error handling
- Security vulnerabilities (injection, auth, access control, secrets)
- Performance bottlenecks (rendering, queries, bundle size, caching)
- Logging strategy and monitoring readiness
- Code smells and maintainability
- Scalability limits
- Production configuration and environment handling
- Reliability, failure recovery, and disaster recovery

For every issue, use this exact format:
- Title
- Severity: Critical / High / Medium / Low
- Category
- Location: File / Folder / Function / Component
- Description
- Real-world Impact
- Recommended Fix
- Priority
- Estimated Effort: Small / Medium / Large

At the end, provide:
- Executive Summary
- Risk Score (0-100)
- Production Readiness Score (0-100)
- Technical Debt Score (0-100)

Prioritize findings by severity, Critical first.
```

---

## The 20 Individual Audit Prompts

Run these one at a time for a focused, deep pass on a specific area. Each assumes you've already shared the [Standard Issue Format](#standard-issue-format) in the session.

### 1. Production Readiness Audit

```
Review this entire project as if deployment is scheduled today.

Evaluate:
- Critical bugs
- Architecture problems
- Missing validation
- Missing error handling
- Security vulnerabilities
- Performance bottlenecks
- Logging strategy
- Monitoring readiness
- Code smells
- Maintainability
- Scalability
- Production configuration
- Reliability
- Failure recovery
- Disaster recovery considerations

Report every finding using the Standard Issue Format, prioritized by
severity.
```

### 2. Deployment Readiness Checklist

```
Assume deployment begins in one hour. Audit the repository and verify
readiness across each category below. For anything missing or
misconfigured, report it as a blocker using the Standard Issue Format.

Environment:
- Environment variables
- Secret management
- Runtime configuration
- Feature flags

Infrastructure:
- CI/CD
- Health checks
- Monitoring
- Logging
- Alerting
- Error reporting

Security:
- HTTPS
- CSP
- Rate limiting
- Secure cookies
- Security headers

Reliability:
- Retry mechanisms
- Timeouts
- Circuit breakers
- Graceful shutdown
- Rollback strategy

Observability:
- Metrics
- Distributed tracing
- Log aggregation
- Dashboards

Backups:
- Database backups
- Restore process
- Disaster recovery

List every blocker that must be resolved before release, in priority
order.
```

### 3. Performance Audit

```
Act as a Performance Engineer. Review this application's production
performance.

Analyze:
- Unnecessary re-renders
- Expensive computations
- Duplicate API requests
- Memory leaks
- Bundle size
- Code splitting
- Lazy loading
- Dynamic imports
- Tree shaking
- Image optimization
- Font optimization
- Caching strategy
- CDN usage
- Server vs client boundaries
- Streaming opportunities
- Suspense usage
- Hydration costs
- Database performance
- Query efficiency
- Pagination
- Background jobs

For each finding, use the Standard Issue Format and estimate the
expected performance improvement if fixed.
```

### 4. Security Audit

```
Act as a Security Engineer. Perform a complete security assessment of
this codebase.

Look for:
- SQL injection
- NoSQL injection
- XSS (stored and reflected)
- CSRF
- SSRF
- Path traversal
- Command injection
- Authentication flaws
- Authorization issues
- Broken access control
- Privilege escalation
- Session fixation
- Weak JWT implementation
- Weak cookies
- Missing HTTP security headers
- Exposed secrets
- Environment variable misuse
- API vulnerabilities
- Missing rate limiting
- Missing input validation
- File upload vulnerabilities
- Dependency vulnerabilities

For every vulnerability, use the Standard Issue Format and additionally
explain:
- Attack scenario
- Business impact
- Exploitability
- Recommended mitigation
```

### 5. API Review

```
Review every API endpoint in this codebase.

Check each one for:
- Input validation
- Schema validation
- Authentication
- Authorization
- Error handling
- HTTP status code correctness
- Response consistency
- Pagination
- Rate limiting
- Caching
- Logging
- Request tracing
- Input sanitization
- API versioning
- Idempotency

Report every issue using the Standard Issue Format and identify which
ones are production risks versus nice-to-haves.
```

### 6. Database Review

```
Review all database interactions in this codebase.

Analyze:
- N+1 queries
- Missing indexes
- Full table scans
- Slow queries
- Transaction handling
- Locking
- Race conditions
- Connection pooling
- ORM usage
- Query optimization
- Pagination
- Batch operations

Report every issue using the Standard Issue Format and recommend
specific improvements, including index or query changes where
relevant.
```

### 7. Staff Engineer Review

```
Review this project like a Principal or Staff Software Engineer.

Focus on:
- Overall architecture
- Scalability
- Feature boundaries
- Separation of concerns
- Domain modeling
- Dependency flow
- Layer violations
- Long-term maintainability
- Code ownership clarity
- Developer experience
- Future extensibility

Highlight architectural decisions that will become expensive as the
project grows, and explain why, using the Standard Issue Format.
```

### 8. Bug Hunter

```
Find every possible bug in this codebase.

Look for:
- Race conditions
- Async issues
- Improper promise handling
- Missing awaits
- Infinite loops
- Memory leaks
- Stale closures
- Null references
- Undefined access
- State synchronization issues
- Timing issues
- Event listener leaks
- Subscription leaks
- Incorrect dependency arrays
- Edge cases

Report every bug using the Standard Issue Format. Only suggest a
rewrite when a targeted fix is genuinely not possible.
```

### 9. React / Next.js Audit

```
Review this application using modern React and Next.js best practices.

Analyze:
- Server Components vs Client Components usage
- Server Actions
- Hydration mismatches
- Suspense
- Streaming
- App Router usage
- Metadata
- SEO
- Dynamic vs static rendering
- Route handlers
- Middleware
- Image optimization
- Fonts
- Caching
- React anti-patterns
- Accessibility

Report every issue using the Standard Issue Format.
```

### 10. AI Code Smell Detector

```
Identify code in this repository that was likely generated by AI
without sufficient review.

Look for:
- Duplicate logic
- Repeated helper functions
- Overengineering
- Unnecessary abstractions
- Dead code
- Placeholder logic
- Generic or meaningless naming
- Inconsistent conventions
- Unused utilities

For each finding, use the Standard Issue Format and suggest a
simplification.
```

### 11. Refactoring Audit

```
Identify refactoring opportunities in this codebase.

Review:
- Long functions
- Large components
- Repeated logic
- Poor abstractions
- Hidden coupling
- Deep nesting
- Feature extraction opportunities
- Shared utility opportunities
- Component composition
- Reusable hook opportunities

Report each opportunity using the Standard Issue Format and rank them
by impact.
```

### 12. Architecture Review

```
Evaluate the overall architecture of this repository.

Inspect:
- Folder organization
- Module boundaries
- Dependency direction
- Feature isolation
- Domain separation
- Shared libraries
- State management approach
- API organization
- Infrastructure layer
- Business logic placement

Report issues using the Standard Issue Format and recommend
improvements for long-term growth.
```

### 13. Frontend UX Audit

```
Act as a UX Engineer. Evaluate the user experience of this application.

Inspect:
- Loading states
- Skeleton screens
- Empty states
- Error states
- Accessibility
- Keyboard navigation
- Responsive layouts
- CLS (Cumulative Layout Shift)
- LCP (Largest Contentful Paint)
- INP (Interaction to Next Paint)
- Animation performance
- Perceived performance
- Form validation
- User feedback on actions
- Offline handling

Report each issue using the Standard Issue Format and suggest specific
improvements.
```

### 14. Scalability Audit

```
Assume this application needs to grow from 100 users, to 10,000 users,
to 100,000 users, to 1 million users.

Identify:
- Database bottlenecks
- Server bottlenecks
- API bottlenecks
- Caching opportunities
- Background job requirements
- Queue system needs
- CDN opportunities
- Horizontal scaling issues
- Vertical scaling limitations
- Cost optimization opportunities

For each finding, use the Standard Issue Format and note at which
user-scale tier it becomes a real problem.
```

### 15. Production Failure Simulation

```
Pretend this application has just failed in production. Predict the 20
most likely causes.

For each one, provide:
- Probability
- Impact
- Root cause
- Detection method
- Prevention
- Recovery strategy

Rank the list from most to least likely.
```

### 16. Pull Request Review

```
Review this repository like a strict GitHub Pull Request reviewer.

Ignore formatting entirely. Only report issues that would block
approval.

For each blocking issue, explain:
- Issue
- Why it matters
- Required fix

Do not include nice-to-have suggestions in this pass.
```

### 17. Startup CTO Review

```
You are the CTO reviewing this project before launch. Answer directly:

1. Would you approve deployment?
2. If not, why not?
3. What must be fixed before release?
4. What can wait until after launch?
5. What should be prioritized in the first post-launch sprint?

End with a clear Go / No-Go decision and a one-paragraph justification.
```

### 18. Codebase Consistency Audit

```
Review consistency across this entire repository.

Evaluate:
- Naming conventions
- Folder organization
- Component architecture
- Hook patterns
- API patterns
- Logging approach
- Error handling approach
- Testing strategy
- State management
- Documentation
- Import organization

Report inconsistencies using the Standard Issue Format and recommend
one unified standard for each category.
```

### 19. Dependency Audit

```
Analyze every dependency in this project.

Identify:
- Unused packages
- Outdated packages
- Duplicate libraries solving the same problem
- Heavy dependencies with lighter alternatives
- Known security vulnerabilities
- Bundle size impact
- License concerns

For each finding, use the Standard Issue Format and estimate:
- Bundle size reduction
- Build speed improvement
- Security improvement
```

### 20. Technical Debt Audit

```
Categorize the technical debt in this repository into three buckets:

1. Quick Wins — easy improvements with immediate value
2. Needs Refactor — requires moderate, planned effort
3. Major Rewrite — structural problems that get more expensive the
   longer they're left

For each item, explain why it becomes more costly over time if
ignored, and place it using the Standard Issue Format.
```

---

## The Final Deliverables Prompt

Run this after the Master Prompt and/or individual audits to compile everything into a single decision-ready report.

```
Compile everything found across this review into a final report with
these sections:

Executive Summary
Summarize the overall quality and readiness of the project in a few
paragraphs.

Severity Breakdown
Count of issues by severity: Critical / High / Medium / Low.

Scores (0-100 each, with a one-line justification for each):
- Production Readiness Score
- Security Score
- Performance Score
- Maintainability Score
- Scalability Score
- Technical Debt Score

Top 10 Highest Priority Fixes
Rank the most important issues to resolve before production.

Nice-to-Have Improvements
List non-blocking enhancements for future iterations.

Final Decision — choose exactly one:
- Approved for Production
- Approved with Minor Issues
- Deployment Not Recommended
- Block Production Release

Provide a detailed explanation supporting the decision. Be direct — do
not soften the verdict to be diplomatic.
```

---

## Recommended Order to Run These

Don't run all 20 in one sitting on a large repo — you'll get shallow results and burn context. A practical sequence:

1. **Master Audit Prompt** — get the full picture and spot obvious blockers fast.
2. **Security Audit + Bug Hunter** — these two catch the issues most likely to actually break production or get exploited.
3. **Performance Audit + Database Review + API Review** — the technical depth pass.
4. **Staff Engineer Review + Architecture Review + Refactoring Audit** — the long-term-cost pass.
5. **Frontend UX Audit + Scalability Audit** — the growth and experience pass.
6. **Production Failure Simulation + Deployment Readiness Checklist** — the "are we actually ready right now" pass.
7. **Pull Request Review + Startup CTO Review** — the go/no-go gate.
8. **Final Deliverables Prompt** — compile everything into one report for the team.

---

## Tips for Best Results

- **Give the agent real repo access.** A coding agent that can open every file will catch cross-file issues (inconsistent patterns, duplicate logic, layer violations) that a pasted-snippet review never will.
- **Run per-module on large repos.** If the codebase is big, scope each audit to one app, service, or feature area at a time rather than the whole monorepo in one pass.
- **Don't accept vague findings.** If a "fix" is just "improve error handling," push back and ask for the specific file, function, and code change.
- **Re-run after fixes.** Treat this as a loop, not a one-time report — fix the Critical and High items, then re-run the relevant audit to confirm they're resolved.
- **Keep a running log.** Save each audit's output; it becomes your technical debt backlog and a useful record of what's already been reviewed.

---

## Closing Note

A generic "review my code" prompt gets a generic answer. Giving the AI a specific role, a specific checklist, and a specific output format is what turns it from a code-reading assistant into something closer to a full review team.

Run the Master Prompt before every release. Pull the individual audits out whenever you need to go deep on one area. Compile with the Final Deliverables Prompt when it's time to make the call.
