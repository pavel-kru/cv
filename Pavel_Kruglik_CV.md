# Pavel Kruglik

**Senior Front-End Engineer / Architect — React · TypeScript · Node.js · AI Engineering**

Belarus (UTC+3) · Remote, EU/US working-hours overlap · Available as B2B contractor
Email: pavelkruglik7@gmail.com · Telegram/Phone: +375 29 800 25 35
LinkedIn: https://www.linkedin.com/in/pavel-kruglik-402723200/
GitHub: https://github.com/pavel-kru

---

## Summary

Senior front-end engineer with 6+ years building enterprise platforms in React and TypeScript. Since 2022, principal front-end engineer on a property-management and accounting suite of five production apps in an ~11,300-file NX monorepo. Cut the suite's full TypeScript type-check from **426 s to 41.8 s (10×)**, and since Sep 2026 lead the front end of a legacy ASP.NET WebForms → React modernization.

Also the team's AI engineering lead: built the agent knowledge base, workflow skills and guardrail hooks that let LLM coding agents (Claude Code primarily) work reliably inside the codebase.

Seeking B2B engagements that value React/TypeScript architecture and practical AI/LLM engineering.

---

## Core Skills

**Languages & Runtime** — TypeScript (strict), JavaScript (ES2023+), Node.js, HTML5, CSS3, OData

**Front-End** — React 19, React Router 7, TanStack Query, Redux/Redux-Saga, Zustand, Next.js (SSR/SSG), Single-SPA microfrontends, Stencil.js, PWAs

**Node.js & Build Tooling** — Node.js CLI/build scripts, NX, Vite, Webpack, Babel/SWC, Yarn workspaces, npm package publishing, Husky + lint-staged

**AI / LLM Engineering** — Claude Code (primary), Claude API, OpenAI Codex, Cursor, Warp; agent skill authoring, context engineering, agentic knowledge bases, MCP integration, LangGraph orchestration, guardrail hooks

**UI & Architecture** — Tailwind, Radix/shadcn, Styled Components, MUI, Storybook, Feature-Sliced Design, OAuth2/OIDC + PKCE, accessible (WCAG-minded) components

**DevOps & Team Automation** — GitHub Actions (CI workflows, event triggers, secrets), Telegram Bot API, Slack Workflow Builder, Jira/Confluence integrations, scheduled jobs, Bash/curl scripting

**Quality** — Jest, Vitest, React Testing Library, Mock Service Worker, Cypress, ESLint, Sentry, TS compiler performance profiling

**Payments** — Stripe, Plaid (bank linking & reconciliation), chargebacks/refunds/NSF, ACH & card flows, tokenised payment links

**Domains** — FinTech & double-entry accounting, property management, KYC/compliance, IoT & automotive

---

## AI & LLM Engineering

- **Agent knowledge base:** authored 27 documents (~3,150 lines) in the team repo, routed through a conditional `CLAUDE.md` index so agents load only the docs a task needs.
- **Ownership of AI tooling:** wrote 43 of the 50 commits to the repo's AI-tooling directories; reused the same knowledge-base pattern in a personal project (`AGENTS.md`).
- **Workflow skills:** designed 4 end-to-end agent skills (~1,100 lines) for adding a feature, building an OData report and wiring a company setting, replacing multi-day onboarding with one prompt.
- **Guardrail hooks:** wrote Bash hooks that block malformed commit trailers and prevent a session ending with unsynced shared knowledge.
- **Multi-agent tooling:** built a Claude-to-DeerFlow (LangGraph) bridge for delegated research, and integrated MCP servers (Figma, Jira, Sentry, Swagger, Slack) into daily development.
- **Parallel sessions:** defined the coordination protocol for running several agent sessions safely on one working tree. Every agent change is human-reviewed and checked against the type-checker and live API specs.

---

## Professional Experience

### Senior Front-End Engineer / Architect — Property Management & Accounting Platform
**Independent B2B Contractor (via Symfony Art) · Aug 2022 – Present · Remote**

Principal front-end engineer on a multi-tenant SaaS suite — five production React apps in a shared NX monorepo (~11,300 TS files). Own UI architecture, the shared component library, the API type layer, build tooling, and AI developer tooling.

- Fixed a **TypeScript compiler performance collapse**: traced a 7-minute full check to a polymorphic component re-inferring generics across ~950 props, and restructured its typing — **426 s → 41.8 s (10×)**, type instantiations **395k → 197k (−50%)**.
- Cut the component library's type-check **204 s → 10 s (−95%)**, using a minimal-repro profiling harness I built with `tsc --generateTrace`/`--generateCpuProfile` (iteration loop ~7 min → ~25 s).
- Built the **financial reporting system** (P&L, balance sheet, cash flow, operating statement) with scheduled email delivery and multi-format export.
- Architected the **custom reports engine on OData**: a two-step builder with type-aware filters and generated `$select`/`$filter`/`$orderby`, so non-technical users build their own reports; drag-and-drop column reordering on the native HTML5 API.
- Built the **payments layer**: bulk payments, chargebacks/refunds/NSF fees, security deposits, **Plaid** bank linking with auto-categorising transaction rules, and **Payment by Link** (tokenised public payment links).
- Re-architected the **global sidebar system** into a provider-based state model, removing a last-writer-wins bug class at the hook level.
- Delivered the **owners & distributions module** end to end: breakdowns, payment runs, audit logging and soundex search.
- Led the **API type-layer migration** out of the shared library, with hand-written types verified against live Swagger specs; centralised routing behind **typed route builders**.
- Automated the team's weekly cross-timezone (Minsk/London) front-end call with a scheduled **Slack Workflow Builder** workflow that posts the reminder, collects attendance via reactions and links the shared Confluence agenda.
- Designed the table system's **navigable row/cell links** as real anchors, so middle-click, new-tab and keyboard navigation all work.
- Highest-volume contributor to the monorepo: **16,900+ small, atomic commits** over four years, sustaining five apps without a separate front-end team.

**Legacy modernization (Sep 2026 – present)** — leading the front end of a legacy ASP.NET WebForms → React rewrite of a second product.

- Built the new SPA's foundation: React 19, Vite, TanStack Query, Feature-Sliced Design with **ESLint-enforced layer boundaries**, and an in-house design system of 20+ accessible components.
- Migrated **10 report pages** (cash receipts, tenant balances, legal, labels, envelopes, custom letters and more) to full legacy parity against an ASP.NET 8 Swagger contract, deployed as an IIS sub-application beside the live legacy site.
- Authored **22 of the repo's 31 commits (~60k lines)** in a codebase with 100+ Vitest suites, and wrote the front-end build/review skills for the team's agent-driven, spec-first migration pipeline.

### Software Developer — Administrative Tools & Tenant Portal
**Independent B2B Contractor (via Symfony Art) · Jun 2022 – Aug 2022 · Remote**

- Built internal admin dashboards in Next.js with SSR/SSG for the public tenant portal, improving performance and SEO.
- Shipped features and fixes on the React + Redux-Saga tenant portal serving residents.

### Front-End Engineer — IoT, Component Libraries & FinTech
**Independent B2B Contractor (via Omertex) · Sep 2020 – May 2022 · Remote**

- **IoT & automotive:** led migration of a roadside-assistance platform from Angular to React microfrontends (Single-SPA), integrating **Stripe** payments and live mapping while the legacy system stayed live.
- **Component library:** built a framework-agnostic Web Components library (Stencil.js + Storybook), published to npm and adopted across multiple projects.
- **FinTech:** built the onboarding and transaction UI for an investment platform, with multi-step form validation.

---

## Personal Projects

### Locus Meus — Mobile-First Gallery Platform *(2026 – present)*
**Sole engineer & architect** · React 19 · TypeScript · Vite · Tailwind · Zustand · GitHub Actions
**github.com/Locus-Meus/Locus-Front** · **github.com/Locus-Meus/Locus-Admin-FE** *(public)*

Solo two-app product (end-user PWA + admin console) on a Java/Spring backend.

- Implemented **OAuth2 Authorization Code + PKCE** end to end — S256 challenge, CSRF state validation, silent iframe re-authentication, redirect restoration — with no client secret in the SPA.
- Automated the project's delivery communication: a **GitHub Actions** workflow posts every new pull request (repo, title, link, author) to a Telegram topic via the Bot API.
- Set up a scheduled **Jira → Telegram** digest that sends the current task list with direct issue links.
- Built on **Feature-Sliced Design**; shipped as an installable **PWA** with 3-language i18n and its own `AGENTS.md` agent knowledge base.

---

## Collaboration & Availability

B2B contract, short- or long-term; part-time to full-time. Four years as the sole front-end engineer on an async, international team.

---

## Education

**Belarusian State Economic University** — Bachelor's Degree, Economics & Trade Management

## Languages

**English** — Professional working proficiency · **Russian** — Native · **Hebrew** — Pre-intermediate
