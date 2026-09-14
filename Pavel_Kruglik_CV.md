# Pavel Kruglik

**Senior Front-End Engineer / Front-End Architect — React · TypeScript · Node.js · AI Engineering**

Remote (Europe) · Available as B2B contractor
Email: pavelkruglik7@gmail.com · Telegram/Phone: +375 29 800 25 35
LinkedIn: https://www.linkedin.com/in/pavel-kruglik-402723200/
GitHub: https://github.com/pavel-kru · GitHub Org: https://github.com/orgs/Locus-Meus

---

## Summary

Senior front-end engineer with 6+ years building large-scale enterprise platforms in React and TypeScript, currently the principal front-end engineer on a property-management and accounting suite of five production applications. Author of 16,900+ commits to a 11,300-file NX monorepo over four years, owning UI architecture, the shared component library, the API type layer, and the build tooling end to end.

Also the team's AI engineering lead: designed and shipped the agent infrastructure — a 27-document, 3,100-line machine-readable knowledge base plus reusable agent skills, deterministic enforcement hooks, and MCP tool integrations — that lets LLM coding agents work correctly inside the codebase.

Independently building **Locus Meus**, a two-application product on a current stack (React 19, Vite, Tailwind, Zustand, OAuth2/PKCE, PWA) — keeping hands-on with modern tooling outside the enterprise codebase.

Seeking B2B engagements where deep React/TypeScript architecture expertise and practical AI/LLM engineering are both valued.

---

## Core Skills

**Languages & Runtime** — TypeScript (expert, strict mode), JavaScript (ES2023+), Node.js, HTML5, CSS3, SQL-like query languages (OData)

**Front-End** — React 19, React Router 7, TanStack Query, Redux + Redux-Saga, Zustand, Next.js (SSR/SSG), Single-SPA microfrontends, Stencil.js Web Components, Progressive Web Apps

**Node.js & Tooling** — Node.js build tooling and CLI scripts, NX monorepo (22.x), Vite 6, Webpack 5, Babel/SWC, Yarn workspaces, npm package authoring & publishing, Husky + lint-staged, `env-cmd` multi-environment pipelines, custom Node packaging scripts

**AI / LLM Engineering** — Claude Code, Anthropic Claude API, Cursor, GPT-4, Gemini; agent skill authoring, prompt engineering, context engineering, agentic knowledge bases, MCP (Model Context Protocol) server integration, LangGraph-based multi-agent orchestration, agent guardrail hooks, n8n automation workflows

**UI & Design Systems** — Styled Components, MUI, Tailwind CSS, Radix UI / shadcn primitives, Storybook 10, design-system architecture, WCAG-minded accessible components, responsive and mobile-first patterns

**Quality & Observability** — Jest, React Testing Library, Cypress, ESLint, Stylelint, Prettier, Sentry, TypeScript compiler performance profiling

**Architecture & Security** — Feature-Sliced Design (FSD), microfrontends, OAuth2 / OpenID Connect, PKCE authorization-code flow, silent token refresh, CSRF protection, internationalisation (i18next)

**Domains** — FinTech & double-entry accounting, property management, payments (Plaid, ACH, chargeback/NSF), KYC/compliance, IoT & automotive

---

## AI & LLM Engineering

*A dedicated focus area since 2025. I do not just use AI coding tools — I build the infrastructure that makes them reliable on a large, idiosyncratic codebase, and I ship it to the whole team.*

### Agent-readable knowledge base (production, team-wide)
- Identified that LLM coding agents produced incorrect code on a 11,300-file monorepo because the project's conventions existed only as tribal knowledge. Designed and authored a structured, machine-readable knowledge base — **27 documents, ~3,150 lines**, committed to the team repository and routed from a root `CLAUDE.md` index — covering the API layer, routing, permissions, form library, table/column system, styling rules, and per-application guides.
- Authored **43 of the 50 commits** to the repository's AI-tooling directories, establishing the pattern the rest of the team now follows.
- Built the index as a **conditional routing table** ("working with the API → read this; adding routes → read that"), so agents load only the context a task needs instead of exhausting the context window — a deliberate context-engineering decision that keeps large tasks inside a single session.

- Applied the same pattern to my own product (**Locus Meus**), shipping an `AGENTS.md` startup-rules index plus a domain deep-dive (`agents/auth.md`) that documents the full OAuth2/PKCE flow — proof the approach is a portable method I apply to any codebase, not a one-off artefact of a single employer.

### Reusable agent skills (domain-specific automation)
- Designed and shipped **4 production agent skills** (~1,100 lines) that encode entire end-to-end workflows — adding a new feature with correct architecture layout, building an OData-backed custom report, creating a company setting across API/form/view layers, and modifying a complex multi-mode lease form.
- Each skill turns a multi-day onboarding problem into a single prompt, letting an agent produce architecturally correct code on the first attempt instead of requiring several review rounds.

### Deterministic guardrails (hooks)
- Wrote **PreToolUse and Stop hooks** in Bash that enforce correctness the model cannot be trusted to self-police: blocking non-compliant git commit trailers outright, and refusing to end a session while the shared knowledge repository has drifted, uncommitted, or unpushed changes.
- **Principle applied:** where a rule must never be violated, enforce it in the harness rather than the prompt — the model advises, the hook decides.

### Multi-agent & tool integration
- Built a **Claude-to-DeerFlow bridge skill** (LangGraph-based agent platform) to delegate long-running research and analysis to a separate agent runtime over HTTP — thread management, streaming runs, model/skill discovery, memory, and file upload — with fully env-var-driven configuration so it runs unchanged across machines.
- Integrated **MCP servers** (Figma, Atlassian/Jira, Sentry, Swagger, Google Workspace, Slack) into the daily development loop, letting agents read designs, tickets, production errors, and live API specifications directly instead of working from stale second-hand descriptions.
- Ran **parallel agent sessions** against a single shared working tree, and defined the coordination protocol (pre-edit status checks, inter-agent messaging, per-hunk commit splitting via temporary worktrees) that prevents concurrent sessions from clobbering each other's work.

### Cross-machine knowledge synchronisation
- Built a private **knowledge-sync repository** that versions skills, hooks, settings, memory, and documentation across two development machines, with a verification script and an automated sync step enforced by hook — so AI capability improvements propagate instead of being stranded on one laptop.
- Maintain a **persistent agent memory system** (22 structured entries, cross-linked) capturing verified project facts, corrections, and working preferences, so each new session starts with accumulated context rather than from zero.

### Practical LLM application
- Use **Claude Code and Cursor as the primary development workflow** for feature delivery, large refactors, and migrations across the monorepo, with human architectural review on every change.
- Apply prompt and context engineering daily: scoping task context, structuring documentation for retrieval, decomposing work for agent execution, and verifying AI output against the type-checker, tests, and live API specifications — treating model output as a draft to be proven, never as ground truth.
- Built **n8n automation workflows** integrating LLM steps into business and development processes.

---

## Professional Experience

### Senior Front-End Engineer / Front-End Architect — Property Management & Accounting Platform
**Independent B2B Contractor (via Symfony Art) · Aug 2022 – Present · Remote**

Principal front-end engineer on a multi-tenant SaaS suite for property management and double-entry accounting — five production React applications (property-management, tenant, vendor, internal admin, KYC) in a shared NX monorepo of ~11,300 TypeScript files. Own UI architecture, the shared component library, the API type layer, build tooling, and AI developer tooling.

- Authored **16,900+ commits over four years** (~2,780 features, ~3,730 fixes, ~2,590 refactors) as the consistently highest-volume contributor to the codebase, sustaining delivery across five applications without a dedicated front-end team.
- Built the platform's **financial reporting system** — P&L, balance sheet, cash flow, operating statement, bills overview, and unit performance — including customisable totals, drill-down navigation, scheduled email delivery, and multi-format export (CSV, PDF, and per-building split reports), replacing manual accountant spreadsheet work.
- Architected the **custom (memorised) reports engine on OData**: a two-step report builder with type-aware filter operators per column type, drag-and-drop column ordering, include/exclude rule sets, base64-encoded shareable report state, and dynamic `$select`/`$filter`/`$orderby` query generation — letting non-technical users build their own reports without engineering involvement.
- Re-architected the **global sidebar system** into a provider-based state model with a unified API, and diagnosed a long-standing data-persistence bug as a last-writer-wins registration conflict — fixing it at the hook level so the entire class of bug could not recur.
- Delivered the **owners & distributions module** end to end: ownership-breakdown tables, distribution generation, payment runs, audit logging, permission-module gating, and soundex-based fuzzy entity search.
- Built **payments and banking integrations** — Plaid bank linking, bulk payment processing, chargeback and NSF fee handling, deposit scheduling, and payment-gateway configuration.
- Diagnosed and fixed a **TypeScript compiler performance collapse**, cutting a full type-check from **415 s to 48 s (–88%)** by restructuring the generic typing of a core component — removing a daily multi-minute tax on every developer and CI run.
- Led the **API type-layer migration**, extracting app-specific types out of the shared library to remove architectural boundary violations, and established verification of hand-written types against live Swagger specifications after finding front-end types silently diverging from the real API.
- Centralised routing behind **typed route builders**, replacing scattered string concatenation with a type-safe API that makes broken links a compile-time error.
- Maintain the shared **UI component library and Storybook** (10.x) used across all five applications, plus internal forks of three form/layout packages.
- Introduced **Sentry** monitoring and use it to triage production issues directly from error signal to fix.

### Software Developer — Administrative Tools & Tenant Portal
**Jun 2022 – Aug 2022 · Remote**

- Developed internal dashboards and administrative tooling in Next.js, improving day-to-day operational efficiency for business users.
- Implemented server-side rendering and static generation on the public tenant portal, improving load performance and SEO.
- Shipped features and resolved defects on the React + Redux-Saga tenant portal serving residents.

### Front-End Engineer — IoT, Component Libraries & FinTech
**Sep 2020 – May 2022 · Remote**

- **IoT & automotive platform:** Led migration of a legacy roadside-assistance application from Angular to a modern React microfrontend architecture (Single-SPA), integrating mapping and payment functionality while keeping the legacy system live throughout.
- **Distributed component library:** Built a framework-agnostic Web Components library with Stencil.js and Storybook, published to NPM and adopted across multiple company projects — giving teams on different frameworks one shared UI vocabulary.
- **FinTech investment platform:** Built the complete user onboarding and transaction interface, focusing on robust multi-step form validation and secure handling of financial data.

---

## Personal Projects

### Locus Meus — Mobile-First Gallery Platform *(2026 – present)*
**Sole front-end engineer & architect** · React 19 · TypeScript · Vite · Tailwind · Zustand · TanStack Query
`github.com/orgs/Locus-Meus` *(private — walkthrough available on request)*

Self-directed two-application product: a mobile-first installable PWA for end users and a separate admin console, both consuming a Java/Spring backend.

- Implemented the complete **OAuth2 Authorization Code flow with PKCE** against a Java authorization server — `S256` challenge generation, CSRF `state` validation, session-storage verifier handling, token exchange, **silent re-authentication** via hidden iframe, post-login redirect restoration, and email verification. Chose browser-redirect PKCE over storing a client secret in the SPA, keeping no long-lived credential in front-end code.
- Architected both applications on **Feature-Sliced Design** (`app` / `pages` / `features` / `entities` / `shared`) with public `index.ts` entry points per slice, enforcing one-directional dependencies in a codebase built to grow.
- Built a typed **`BaseApiClient`** over Axios centralising auth headers, error normalisation, and a global 401 handler that clears the session and redirects — so no feature re-implements auth failure handling.
- Shipped as an **installable PWA** (`vite-plugin-pwa`, auto-update service worker) with a **three-language i18n layer** (English, Spanish, Russian) and persisted browser language detection.
- Delivered **image upload and gallery management** across both apps: upload with processing-status handling, blob-based preview, and admin-side moderation.
- Wrote the repository's **agent knowledge base** (`AGENTS.md` + `agents/auth.md`) so LLM agents follow the project's auth and architecture rules — the same practice I introduced at work, applied here from day one.

---

## Selected Technical Achievements

| Achievement | Impact |
|---|---|
| TypeScript compile optimisation | Full type-check **415 s → 48 s (–88%)** |
| Agent knowledge base | **27 docs / ~3,150 lines**, team-wide, committed to repo |
| Reusable agent skills | **4 skills / ~1,100 lines** encoding end-to-end workflows |
| Commit contribution | **16,900+ commits** across 4 years, 5 applications |
| OData report engine | Self-service custom reporting, zero engineering per report |
| Sidebar re-architecture | Provider-based state model; eliminated a bug class |
| Locus Meus (personal) | 2 apps, OAuth2/PKCE + PWA + 3-language i18n, solo |

---

## Collaboration & Availability

- **Engagement model:** B2B contract, short-term or long-term.
- **Workload:** Flexible; scalable part-time to full-time according to project needs.
- **Work style:** Fully autonomous with extensive asynchronous collaboration experience across international, distributed teams — proven by four years as the sole front-end engineer on a cross-functional product team.

---

## Education

**Belarusian State Economic University** — Bachelor's Degree, Economics & Trade Management

---

## Languages

**English** — Professional working proficiency · **Russian** — Native · **Hebrew** — Pre-intermediate
