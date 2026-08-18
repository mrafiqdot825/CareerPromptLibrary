# Prompt Library

A curated collection of production-grade AI system prompts, templates, and engineering workflows for developers, system architects, DevOps engineers, and UI/UX designers.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

![Prompt Library Banner](assets/banner.png)

---

## Directory Functionalities & Available Prompts

### [Frontend Development](frontend/)
Production-grade prompts for modern client-side web applications and UI components.
- [react.md](frontend/react.md) - React 19 / Modern React component design, hooks, state management & performance.
- [nextjs.md](frontend/nextjs.md) - Next.js App Router, Server Components (RSC), Server Actions & SSR optimizations.
- [vue.md](frontend/vue.md) - Vue 3 Composition API, Pinia state management & script setup patterns.
- [angular.md](frontend/angular.md) - Angular Standalone Components, Signals, RxJS streams & dependency injection.
- [tailwind.md](frontend/tailwind.md) - Tailwind CSS responsive design, dark mode, animation utilities & custom design tokens.
- [ui-components.md](frontend/ui-components.md) - Accessible, reusable UI component architecture (Radix, Shadcn style).
- [accessibility.md](frontend/accessibility.md) - WCAG 2.1 AA accessibility audit, keyboard navigation & ARIA remediation.

---

### [Backend Engineering](backend/)
Prompts for server-side architecture, REST/GraphQL APIs, and microservices.
- [nodejs.md](backend/nodejs.md) - Asynchronous Node.js microservices, event loop tuning & stream processing.
- [express.md](backend/express.md) - Express REST API design, middleware chains & error handling wrappers.
- [nestjs.md](backend/nestjs.md) - NestJS Enterprise backend architecture, modules, services, DTOs & interceptors.
- [fastapi.md](backend/fastapi.md) - FastAPI async endpoints, Pydantic v2 schemas & OpenAPI generation.
- [laravel.md](backend/laravel.md) - Laravel 11 REST APIs, Eloquent ORM tuning, queues & service layer.
- [api-design.md](backend/api-design.md) - RESTful & GraphQL API specs, pagination, rate limiting & error codes.

---

### [Mobile Development](mobile/)
Prompts for cross-platform and native mobile applications.
- [react-native.md](mobile/react-native.md) - React Native cross-platform app development & native bridging.
- [expo.md](mobile/expo.md) - Expo Router file-based navigation, EAS builds & push notifications.
- [flutter.md](mobile/flutter.md) - Flutter BLoC / Riverpod state management & smooth 60fps widget rendering.
- [kotlin.md](mobile/kotlin.md) - Android Native Jetpack Compose, Coroutines & Clean Architecture.
- [swift.md](mobile/swift.md) - iOS Native SwiftUI, Swift Concurrency (async/await) & Combine.
- [optimization.md](mobile/optimization.md) - Mobile app performance, memory footprint tuning & startup time reduction.

---

### [AI & GenAI](ai/)
Prompts for building LLM applications, RAG pipelines, AI Agents, and model protocols.
- [llm.md](ai/llm.md) - LLM application prompt engineering, output structuring & JSON enforcement.
- [rag.md](ai/rag.md) - Retrieval-Augmented Generation, chunking strategies, embeddings & hybrid search.
- [agents.md](ai/agents.md) - Autonomous AI Agent workflows, tool calling, memory management & state machines.
- [prompt-engineering.md](ai/prompt-engineering.md) - System prompt optimization, zero-shot/few-shot prompting & meta-prompts.
- [langchain.md](ai/langchain.md) - LangChain & LangGraph stateful workflow construction.
- [openai.md](ai/openai.md) - OpenAI Structured Outputs, Function Calling & Vision APIs.
- [gemini.md](ai/gemini.md) - Google Gemini 1.5 Pro/Flash multimodal prompting & long-context processing.
- [mcp.md](ai/mcp.md) - Model Context Protocol (MCP) server design, tools, and resource definitions.

---

### [Software Architecture](architecture/)
Prompts for designing enterprise-grade software systems and application structures.
- [microservices.md](architecture/microservices.md) - Microservices decomposition, Saga pattern, API Gateways & service mesh.
- [monolith.md](architecture/monolith.md) - Modular Monolith design, boundary isolation & domain-driven design.
- [clean-architecture.md](architecture/clean-architecture.md) - Clean / Hexagonal Architecture layers, entities, use cases & adapters.
- [event-driven.md](architecture/event-driven.md) - Event-Driven Architecture, Kafka/RabbitMQ topics, idempotency & consistency.
- [scalability.md](architecture/scalability.md) - Horizontal vs vertical scaling, stateless design & multi-region architecture.

---

### [Database Engineering](databases/)
Prompts for relational, NoSQL, and caching databases.
- [postgres.md](databases/postgres.md) - PostgreSQL relational schema design, JSONB indexing, partitioning & tuning.
- [mysql.md](databases/mysql.md) - MySQL InnoDB storage engine tuning, query indexing & replication.
- [mongodb.md](databases/mongodb.md) - MongoDB document modeling, aggregation pipelines & sharding strategies.
- [supabase.md](databases/supabase.md) - Supabase Row Level Security (RLS) policies, Edge Functions & Realtime.
- [redis.md](databases/redis.md) - Redis caching patterns, distributed locking, Pub/Sub & rate limiters.
- [optimization.md](databases/optimization.md) - Query profiling, EXPLAIN ANALYZE interpretation & index optimization.

---

### [DevOps & Infrastructure](devops/)
Prompts for containerization, orchestration, CI/CD, and monitoring.
- [docker.md](devops/docker.md) - Multi-stage Dockerfile builds, rootless containers & compose stacks.
- [kubernetes.md](devops/kubernetes.md) - Kubernetes manifest generation (Deployment, Ingress, HPA, ConfigMap).
- [ci-cd.md](devops/ci-cd.md) - CI/CD pipeline design, blue-green deployment & automated smoke tests.
- [github-actions.md](devops/github-actions.md) - GitHub Actions workflow automation, caching, matrix builds & secrets.
- [nginx.md](devops/nginx.md) - Nginx reverse proxy configs, SSL termination, rate limiting & gzip/brotli.
- [monitoring.md](devops/monitoring.md) - Prometheus metrics, Grafana dashboards & OpenTelemetry tracing.

### [Pre-Deployment Checklist](Pre-Deployment%20Checklist/)
Production readiness gates, authorization checks, rate limiting, and rollback strategy guides.
- [PROMPT.md](Pre-Deployment%20Checklist/PROMPT.md) - Comprehensive production deployment checklist covering authorization, input security, rate limits, and blue-green rollbacks.
- [README.md](Pre-Deployment%20Checklist/README.md) - Pre-deployment verification overview and production risk mitigation guide.

---

### [Deployment & Production](deployment/)
Prompts for cloud hosting, production checklists, and platform deployments.
- [production-checklist.md](deployment/production-checklist.md) - Comprehensive production release checklist covering Auth, Input, Security & Rollback.
- [security-checklist.md](deployment/security-checklist.md) - Cloud infrastructure deployment security audit checklist.
- [vercel.md](deployment/vercel.md) - Vercel edge deployments, env vars, serverless function limits & previews.
- [aws.md](deployment/aws.md) - AWS ECS/Fargate, Lambda, S3, CloudFront deployment infrastructure.
- [azure.md](deployment/azure.md) - Azure App Service, Container Apps & Key Vault deployment integration.
- [cloudflare.md](deployment/cloudflare.md) - Cloudflare Workers, Pages, Zero Trust & CDN caching strategies.

---

### [Testing & QA](testing/)
Prompts for unit, integration, and E2E testing across popular testing frameworks.
- [unit-testing.md](testing/unit-testing.md) - Unit test generation using AAA pattern & dependency mocking.
- [integration.md](testing/integration.md) - API & database integration testing setup with Testcontainers.
- [e2e.md](testing/e2e.md) - End-to-end testing strategy & Page Object Model pattern.
- [playwright.md](testing/playwright.md) - Playwright cross-browser automation, network interception & visual diffing.
- [cypress.md](testing/cypress.md) - Cypress component & E2E test suites with custom commands.
- [vitest.md](testing/vitest.md) - Vitest fast unit test setup, snapshot testing & coverage reports.

---

### [Security & AppSec](security/)
Prompts for application security, authentication, and vulnerability audits.
- [auth.md](security/auth.md) - Authentication implementation (OAuth2, OIDC, Session vs Token).
- [jwt.md](security/jwt.md) - JWT security, token rotation, refresh token patterns & algorithm hardening.
- [owasp.md](security/owasp.md) - OWASP Top 10 vulnerability identification & code remediation.
- [penetration-testing.md](security/penetration-testing.md) - Web application penetration testing checklist & diagnostic prompt.
- [api-security.md](security/api-security.md) - API security hardening, CORS, rate limiting & payload sanitization.
- [audit.md](security/audit.md) - Security code audit, dependency vulnerability scanning & secret leaks.

---

### [Performance Optimization](performance/)
Prompts for full-stack performance tuning, caching, and Core Web Vitals.
- [frontend.md](performance/frontend.md) - Core Web Vitals optimization (LCP, INP, CLS), bundle splitting & lazy loading.
- [backend.md](performance/backend.md) - Event loop unblocking, worker threads, async I/O tuning & connection pooling.
- [database.md](performance/database.md) - Database query response time reduction, indexing & connection pool sizing.
- [caching.md](performance/caching.md) - Multi-layer caching strategy (Browser, CDN, Redis, In-Memory).
- [optimization.md](performance/optimization.md) - Full-stack performance audit and bottleneck identification.

---

### [System Design](system-design/)
Prompts for distributed systems design, scalability, and technical interview prep.
- [interviews.md](system-design/interviews.md) - System design interview preparation, back-of-the-envelope estimation & trade-offs.
- [distributed-systems.md](system-design/distributed-systems.md) - Distributed consensus, CAP theorem, partition handling & fault tolerance.
- [caching.md](system-design/caching.md) - Distributed cache design, eviction policies (LRU/LFU) & write-through strategies.
- [queues.md](system-design/queues.md) - Message queue architecture, dead-letter queues & exactly-once delivery.
- [scaling.md](system-design/scaling.md) - High-availability scaling, global load balancing & data sharding strategies.

---

### [Technical Documentation](documentation/)
Prompts for technical writing, API specs, PRDs, and engineering RFCs.
- [api-docs.md](documentation/api-docs.md) - OpenAPI 3.0 specification & markdown API reference documentation.
- [changelog.md](documentation/changelog.md) - Automated Keep a Changelog & Conventional Commits release notes.
- [prd.md](documentation/prd.md) - Product Requirement Document (PRD) authoring template.
- [srs.md](documentation/srs.md) - Software Requirement Specification (SRS) ISO/IEC standard document prompt.
- [technical-spec.md](documentation/technical-spec.md) - Engineering Technical Specification & RFC template.

---

### [GitHub Workflows & Automation](github/)
Prompts for repository templates, release workflows, and automation.
- [issues.md](github/issues.md) - Standardized GitHub Issue Templates (Bug Report, Feature Request).
- [pull-requests.md](github/pull-requests.md) - PR description template with testing steps & reviewer checklists.
- [release.md](github/release.md) - Automated GitHub Release notes and changelog summaries.
- [templates.md](github/templates.md) - GitHub issue & PR template directory configuration generator.
- [workflows.md](github/workflows.md) - GitHub Actions custom workflow authoring & debugging prompt.

---

### [UI / UX Design](ui-ux/)
Prompts for interface design, design systems, and converting Figma designs to code.
- [figma.md](ui-ux/figma.md) - Translating Figma design specs to semantic HTML/CSS code.
- [design-system.md](ui-ux/design-system.md) - Design system token definitions, color palettes & typography scale.
- [dashboard.md](ui-ux/dashboard.md) - Analytical admin dashboard layout design & UX best practices.
- [landing-page.md](ui-ux/landing-page.md) - High-conversion SaaS landing page layout & copy prompt.
- [mobile-ui.md](ui-ux/mobile-ui.md) - Touch-first mobile UI design patterns, gesture UX & navigation.

---

### [Prompt Engineering Meta-Prompts](prompt-engineering/)
Prompts for prompt engineering techniques, reasoning frameworks, and AI Agent personas.
- [chain-of-thought.md](prompt-engineering/chain-of-thought.md) - Chain-of-Thought (CoT) and Step-by-Step reasoning prompt framework.
- [reasoning.md](prompt-engineering/reasoning.md) - Deep reasoning & reflection system prompts (Tree of Thoughts, Self-Consistency).
- [agent-prompts.md](prompt-engineering/agent-prompts.md) - Multi-step AI agent role definitions, task tool execution & fallback loops.
- [reusable-prompts.md](prompt-engineering/reusable-prompts.md) - Modular parameterized prompt building blocks.
- [best-practices.md](prompt-engineering/best-practices.md) - Top prompt engineering principles, token reduction & context management.

---

### [Development Workflow Templates](templates/)
Templates for code reviews, refactoring, bug fixes, and engineering tasks.
- [bug-fix.md](templates/bug-fix.md) - Systematic Bug Fix & RCA (Root Cause Analysis) prompt template.
- [feature.md](templates/feature.md) - End-to-end Feature Implementation prompt template.
- [refactor.md](templates/refactor.md) - Legacy Code Refactoring & Tech Debt Reduction template.
- [code-review.md](templates/code-review.md) - Senior Code Reviewer feedback & security checklist template.
- [migration.md](templates/migration.md) - Framework/Database Migration execution prompt template.
- [optimization.md](templates/optimization.md) - Profiling & Performance Tuning prompt template.
- [checklist.md](templates/checklist.md) - Custom engineering task checklist prompt generator.

---

## How to Use These Prompts
1. Navigate to the relevant category folder or click on any specific prompt file above (e.g., [react.md](frontend/react.md) or [rag.md](ai/rag.md)).
2. Copy the **System Prompt** into your LLM tool (ChatGPT, Claude, Gemini, Cursor, Antigravity).
3. Fill out the variable placeholders in the **User Prompt Template**.
4. Generate production-ready code, specs, or diagnostic reports!

---

## Contributing
Contributions are warmly welcomed! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) guide before submitting a Pull Request.

---

## License
This repository is licensed under the [MIT License](LICENSE).
