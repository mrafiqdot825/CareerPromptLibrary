# Production Deployment Checklist Prompt

> **Category:** Deployment 
> **Role:** Lead Release Engineer & Production Auditor 
> **Objective:** Perform a rigorous pre-deployment audit to ensure zero-downtime, secure, and reliable releases.

---

## System Prompt

```markdown
You are a Lead Release Engineer. Conduct a mandatory production audit based on the production checklist below. Verify authorization, input validation, CORS, rate limits, database performance, logging, and rollback strategies.
```

---

## Comprehensive Checklist Reference

# Production Deployment Checklist

> A comprehensive pre-deployment checklist for modern web, mobile, and backend applications.
>
> **Goal:** Ensure your application is secure, scalable, reliable, and production-ready before every deployment.

---

# Introduction

Deploying an application to production is one of the most critical stages of the software development lifecycle.

A single overlooked security issue, missing database index, or poor deployment strategy can quickly turn into downtime, security breaches, unhappy users, and expensive cloud bills.

This checklist covers the essential areas every developer should verify before pressing the **Deploy** button.

---

# 1. Authorization (Resource Ownership)

## Objective

Ensure every authenticated user can only access resources they own.

Authentication only verifies **who the user is**.

Authorization determines **what the user is allowed to access**.

Never trust IDs received from the frontend.

---

### Verify

- Resource ownership on every protected endpoint
- User ID matches the authenticated session
- Tenant isolation (if multi-tenant)
- Admin routes require admin privileges
- Role-Based Access Control (RBAC)
- Permission checks for every update/delete request

---

### Avoid

```ts
GET /api/orders/123
```

Without checking ownership, users could change the ID:

```ts
GET /api/orders/124
GET /api/orders/125
GET /api/orders/126
```

This creates an **IDOR (Insecure Direct Object Reference)** vulnerability.

---

### Best Practice

Always query using both:

- Resource ID
- Authenticated User ID

Example:

```sql
SELECT *
FROM orders
WHERE id = ?
AND user_id = ?
```

---

## Why It Matters

Skipping authorization allows attackers to access or modify other users' private data.

---

# 2. Password Reset Security

## Objective

Password reset links should be temporary and single-use.

---

### Verify

- Tokens expire within **15–60 minutes**
- Token becomes invalid immediately after use
- Creating a new reset request invalidates previous tokens
- Tokens are cryptographically random
- Tokens are stored hashed (not plaintext)

---

### Why It Matters

Leaked or intercepted reset links should never become permanent backdoors into user accounts.

---

# 3. Input Validation & Injection Protection

## Objective

Treat every piece of client input as untrusted.

Never trust:

- Forms
- Query parameters
- Headers
- Cookies
- JSON payloads

---

### Verify

- Request validation
- Type validation
- Required fields
- Length limits
- File upload validation
- Email validation
- URL validation

---

## SQL Injection Prevention

Always use:

- Parameterized queries
- Prepared statements
- ORM query builders

Never concatenate SQL strings.

---

## XSS Prevention

Always:

- Escape HTML output
- Sanitize rich text
- Validate markdown rendering
- Encode user-generated content

---

## Why It Matters

Proper validation prevents:

- SQL Injection
- Cross-Site Scripting (XSS)
- Command Injection
- Broken application logic

---

# 4. CORS Configuration

## Objective

Allow only trusted frontend domains to communicate with your API.

---

### Verify

Production origins only.

Example:

```
https://app.example.com
https://admin.example.com
```

---

### Never Use

```
Access-Control-Allow-Origin: *
```

Especially when authentication cookies are involved.

---

### Also Verify

- Allowed methods
- Allowed headers
- Credentials configuration
- Preflight responses

---

## Why It Matters

Improper CORS configuration enables malicious websites to send authenticated requests on behalf of your users.

---

# 5. Rate Limiting

## Objective

Prevent abuse and protect infrastructure.

---

### Apply Rate Limits To

- Login
- Signup
- Password Reset
- OTP Verification
- File Uploads
- AI Endpoints
- Payment APIs
- Search APIs

---

### Recommended Limits

| Endpoint | Suggested Limit |
|-----------|-----------------|
| Login | 5–10/minute |
| Signup | 5/hour |
| Password Reset | 3/hour |
| Public API | 100/minute |

---

## Why It Matters

Rate limiting protects against:

- Brute-force attacks
- Credential stuffing
- API abuse
- Denial-of-Service (DoS)
- Unexpected cloud costs

---

# 6. Error Handling

## Objective

Show users helpful error messages while hiding internal implementation details.

---

### Verify

- No stack traces in production
- Generic error responses
- Centralized exception handling
- Validation errors are readable
- Sensitive information is never exposed

---

### Never Expose

- Database queries
- API keys
- File paths
- Framework versions
- Internal server details

---

## Why It Matters

Verbose error messages help attackers fingerprint your application and identify vulnerabilities.

---

# 7. Database Performance

## Objective

Ensure the database can handle production traffic efficiently.

---

### Verify Indexes On

- Foreign keys
- User IDs
- Email columns
- Created dates
- Frequently filtered fields
- Frequently sorted fields

---

### Also Check

- Slow queries
- N+1 query problems
- Query execution plans
- Pagination
- Connection pooling

---

## Why It Matters

Missing indexes can cause:

- Slow responses
- High CPU usage
- Database lockups
- Connection exhaustion

---

# 8. Logging & Monitoring

## Objective

Detect issues before users do.

---

### Logging Checklist

- Structured logs (JSON preferred)
- Error logging
- Authentication logs
- API request logs
- Database error logs
- Deployment logs

---

### Monitoring Checklist

Monitor:

- Error rate
- Response time
- CPU usage
- Memory usage
- Database latency
- Queue failures
- Third-party service failures

---

### Alerting

Configure alerts for:

- High error rates
- API downtime
- Increased latency
- Failed deployments
- Database connection spikes

---

## Why It Matters

Good monitoring shortens incident response time and helps maintain service reliability.

---

# 9. Rollback Strategy

## Objective

Be prepared to recover quickly if a deployment fails.

---

## Recommended: Blue-Green Deployment

Maintain two identical production environments:

- **Blue** → Current live version
- **Green** → New release

Deploy to Green, verify functionality, then switch traffic.

If problems occur, redirect traffic back to Blue immediately.

---

## Alternative Strategies

- Rolling Deployment
- Canary Deployment
- Feature Flags

---

## Verify

- Automated rollback process
- Database migration rollback
- Backup restoration
- Version tagging
- Health checks

---

## Why It Matters

A reliable rollback strategy minimizes downtime and reduces deployment risk.

---

# Additional Production Checks

Before deployment, also confirm:

- Environment variables are correctly configured
- Secrets are stored securely (never in source code)
- HTTPS is enabled everywhere
- Security headers are configured (CSP, HSTS, X-Frame-Options, etc.)
- SSL certificates are valid
- Dependencies are up to date
- Known vulnerabilities have been patched
- Backups are running successfully
- Health check endpoints are available
- API documentation is current
- Feature flags are reviewed
- Scheduled jobs (cron) are functioning correctly
- File storage permissions are secure
- Cache configuration is optimized
- CDN settings are verified (if applicable)

---

# Final Deployment Checklist

Mark each item before deploying:

- [] Authorization checks implemented
- [] Password reset tokens expire correctly
- [] Input validation completed
- [] SQL Injection prevention verified
- [] XSS protection implemented
- [] CORS restricted to production domains
- [] Rate limiting configured
- [] Production error handling enabled
- [] Database indexes reviewed
- [] Logging enabled
- [] Monitoring configured
- [] Alerts tested
- [] Backups verified
- [] Environment variables validated
- [] Secrets secured
- [] HTTPS enforced
- [] Security headers configured
- [] Dependencies updated
- [] Vulnerability scan completed
- [] Health checks passing
- [] Rollback strategy tested
- [] Deployment approved

---

# TL;DR

Before every production deployment, verify the following:

| Category | Key Check |
|----------|-----------|
| Authorization | Users can only access their own data |
| Authentication | Password reset tokens expire and are single-use |
| Security | Validate input, prevent SQL Injection & XSS |
| API Security | Restrict CORS to trusted production domains |
| Performance | Apply rate limiting and optimize database indexes |
| Reliability | Hide internal errors and monitor application health |
| Observability | Enable structured logging and automated alerts |
| Deployment | Have a tested rollback strategy (preferably Blue-Green) |

---

# Remember

> **Production isn't the place to discover bugs.**

Every item marked as **"We'll fix it later"** is often the first one to cause an outage, security incident, or customer complaint. Treat this checklist as a mandatory gate before every release to ensure your application is secure, performant, and reliable.
