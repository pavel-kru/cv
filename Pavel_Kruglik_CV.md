# Pavel Kruglik

**Senior Front-End Engineer / Architect — React · TypeScript · Node.js · AI Engineering**

Remote (Europe) · Available as B2B contractor
Email: pavelkruglik7@gmail.com · Telegram/Phone: +375 29 800 25 35
LinkedIn: https://www.linkedin.com/in/pavel-kruglik-402723200/
GitHub: https://github.com/pavel-kru

---

## Summary

Senior front-end engineer with 6+ years building large-scale enterprise platforms in React and TypeScript — currently the principal front-end engineer on a property-management and accounting suite of five production applications (16,900+ commits over four years, ~11,300-file NX monorepo). Diagnosed and fixed a TypeScript compiler bottleneck, cutting a full type-check **426 s → 41.8 s (10×)**.

Also the team's AI engineering lead: built the agent knowledge base, reusable agent skills, and enforcement hooks that let LLM coding agents (Claude Code, day to day; Codex, Cursor and Warp also used) work correctly inside the codebase — then applied the same method solo on **Locus Meus**, a two-app OAuth2/PKCE product built on React 19 and Vite.

Seeking B2B engagements where deep React/TypeScript architecture and practical AI/LLM engineering are both valued.

---

## Core Skills

**Languages & Runtime** — TypeScript (strict), JavaScript (ES2023+), Node.js, HTML5, CSS3, OData

**Front-End** — React 19, React Router 7, TanStack Query, Redux/Redux-Saga, Zustand, Next.js (SSR/SSG), Single-SPA microfrontends, Stencil.js, PWAs

**Node.js & Build Tooling** — Node.js CLI/build scripts, NX, Vite, Webpack, Babel/SWC, Yarn workspaces, npm package publishing, Husky + lint-staged

**AI / LLM Engineering** — Claude Code (primary), Claude API, OpenAI Codex, Cursor, Warp; agent skill authoring, context engineering, agentic knowledge bases, MCP integration, LangGraph orchestration, guardrail hooks

**UI & Architecture** — Tailwind, Radix/shadcn, Styled Components, MUI, Storybook, Feature-Sliced Design, OAuth2/OIDC + PKCE, accessible (WCAG-minded) components

**Quality** — Jest, React Testing Library, Cypress, ESLint, Sentry, TS compiler performance profiling

**Payments** — Stripe, Plaid (bank linking & reconciliation), chargebacks/refunds/NSF, ACH & card flows, tokenised payment links

**Domains** — FinTech & double-entry accounting, property management, KYC/compliance, IoT & automotive

---

## AI & LLM Engineering

*I don't just use AI coding tools — I build the infrastructure that makes them reliable on a large, idiosyncratic codebase, and I apply the same method to my own projects.*

- **Agent-readable knowledge base:** authored **27 documents (~3,150 lines)**, committed to the team repo and routed through a conditional index (`CLAUDE.md` → "working with the API? read this") so agents load only what a task needs — **43 of the 50 commits** to the repo's AI-tooling directories are mine. Applied the identical pattern solo on Locus Meus (`AGENTS.md` + `agents/auth.md`), proving it's a portable method, not a one-employer artefact.
- **Reusable agent skills:** designed **4 end-to-end workflow skills** (~1,100 lines) that turn a multi-day onboarding problem — adding a feature, building an OData report, wiring a company setting — into a single correct-on-first-try prompt.
- **Deterministic guardrails:** wrote Bash hooks that enforce what a model can't be trusted to self-police — blocking bad commit trailers, refusing to end a session with unsynced shared knowledge. Where a rule must never break, it belongs in the harness, not the prompt.
- **Multi-agent tooling:** built a Claude-to-DeerFlow bridge (LangGraph) for delegated research, integrated MCP servers (Figma, Jira, Sentry, Swagger, Slack) into the daily loop, and defined the coordination protocol for running parallel agent sessions safely on one working tree.
- **Daily practice:** Claude Code is my primary development driver for features, refactors and migrations, with human review on every change; Codex, Cursor and Warp used alongside it. Prompt/context engineering and verifying model output against the type-checker and live API specs are routine, not novel — output is a draft to be proven, never trusted outright.

---

## Professional Experience

### Senior Front-End Engineer / Architect — Property Management & Accounting Platform
**Independent B2B Contractor (via Symfony Art) · Aug 2022 – Present · Remote**

Principal front-end engineer on a multi-tenant SaaS suite — five production React apps in a shared NX monorepo (~11,300 TS files). Own UI architecture, the shared component library, the API type layer, build tooling, and AI developer tooling.

- **16,900+ commits over four years** as the highest-volume contributor, sustaining delivery across five apps without a dedicated front-end team.
- Fixed a **TypeScript compiler performance collapse** (7-minute full check). Profiled with `tsc --generateTrace`/`--generateCpuProfile`, traced it to a polymorphic component re-inferring generics across ~950 props per call site, and restructured the typing: **426 s → 41.8 s (10×)**, type instantiations **395k → 197k (−50%)**, component library **204 s → 10 s (−95%)**. Also built the minimal-repro profiling harness that made the diagnosis possible (~7 min → ~25 s iteration loop).
- Built the platform's **financial reporting system** (P&L, balance sheet, cash flow, operating statement) with scheduled email delivery and multi-format export, and architected the **custom reports engine on OData** — a two-step builder with type-aware filters and dynamic `$select`/`$filter`/`$orderby` generation, letting non-technical users build their own reports. Hand-rolled its drag-and-drop column reordering on the native HTML5 API with no DnD library.
- Built the **payments layer**: bulk payments, chargebacks/refunds/NSF fees, security deposits, **Plaid** bank linking with auto-categorising memorised transaction rules, and **Payment by Link** (tokenised public payment links with full lifecycle management).
- Re-architected the **global sidebar system** into a provider-based state model, fixing a last-writer-wins bug at the hook level so the entire bug class couldn't recur. Delivered the **owners & distributions module** end to end (breakdowns, payment runs, audit logging, soundex search).
- Led the **API type-layer migration** out of the shared library and established verification of hand-written types against live Swagger specs. Centralised routing behind **typed route builders**, and designed the table system's **navigable row/cell links** (real anchors cloned per-cell, so middle-click/new-tab/keyboard all work — not a JS `onClick`).

### Software Developer — Administrative Tools & Tenant Portal
**Jun 2022 – Aug 2022 · Remote**

- Built internal admin dashboards in Next.js with SSR/SSG for the public tenant portal, improving performance and SEO.
- Shipped features and fixes on the React + Redux-Saga tenant portal serving residents.

### Front-End Engineer — IoT, Component Libraries & FinTech
**Sep 2020 – May 2022 · Remote**

- **IoT & automotive:** led migration of a roadside-assistance platform from Angular to React microfrontends (Single-SPA), integrating **Stripe** payments and live mapping while keeping the legacy system live throughout.
- **Component library:** built a framework-agnostic Web Components library (Stencil.js + Storybook), published to NPM and adopted across multiple projects.
- **FinTech:** built the onboarding and transaction UI for an investment platform, with robust multi-step form validation.

---

## Personal Projects

### Locus Meus — Mobile-First Gallery Platform *(2026 – present)*
**Sole engineer & architect** · React 19 · TypeScript · Vite · Tailwind · Zustand
**github.com/Locus-Meus/Locus-Front** · **github.com/Locus-Meus/Locus-Admin-FE** *(public)*

Solo two-app product (end-user PWA + admin console) on a Java/Spring backend.

- Implemented **OAuth2 Authorization Code + PKCE** end to end — S256 challenge, CSRF state validation, silent iframe re-authentication, redirect restoration — deliberately avoiding a client secret in the SPA.
- Built on **Feature-Sliced Design**; shipped as an installable **PWA** with 3-language i18n; wrote the project's own `AGENTS.md` agent knowledge base.

---

## Collaboration & Availability

B2B contract, short- or long-term; workload flexible from part-time to full-time. Fully autonomous with four years' experience as the sole front-end engineer on an async, international team.

---

## Education

**Belarusian State Economic University** — Bachelor's Degree, Economics & Trade Management

## Languages

**English** — Professional working proficiency · **Russian** — Native · **Hebrew** — Pre-intermediate
