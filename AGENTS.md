# AGENTS.md — AI Agent Operating Manual for EcomHub Enterprise

> **Applies To:** Claude Code · Cursor · GitHub Copilot · OpenAI Codex · Gemini Code Assist · Any future AI coding agent
> **Authority:** This file is the universal AI operating layer. It supplements but never overrides [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md).
> **Last Updated:** July 2026

---

## Purpose

This document defines how **any AI coding agent or assistant** must operate within the EcomHub Enterprise repository. It establishes the reading sequence, permitted actions, forbidden actions, documentation standards, and decision boundaries that all tools must follow regardless of vendor.

---

## Mandatory Reading Sequence

Before taking any action in this repository, every AI agent must read these documents in order:

| Step | Document | Why |
|------|----------|-----|
| 1 | `MASTER_PROJECT_BIBLE.md` | Single source of truth for all scope, vision, and decisions |
| 2 | `PROJECT_RULES.md` | Governance rules, naming standards, and phase gate restrictions |
| 3 | `PROJECT_INDEX.md` | Current state — which files exist, which phases are complete |
| 4 | Tool-specific manual | `CLAUDE.md` for Claude Code; equivalent for other tools if present |
| 5 | Task-relevant documents | Any file directly needed for the requested task |

**An agent that acts without completing this reading sequence risks creating content that conflicts with approved governance documents.**

---

## Project Context Summary

EcomHub Enterprise is an **enterprise-grade, multi-vendor commerce platform** designed for the India market, launching in Jammu & Kashmir / Srinagar.

### Five Commerce Verticals

| # | Vertical | Core Offerings |
|---|----------|----------------|
| 1 | Marketplace Products | Pashmina, saffron, dry fruits, handicrafts, general merchandise |
| 2 | Professional Services | CA, GST, ITR, legal, accounting, business consultancy |
| 3 | Insurance Marketplace | Health, car, bike, life, travel insurance |
| 4 | Travel & Hospitality | Houseboats, hotels, taxis, holiday packages, experiences |
| 5 | Digital Services & Products | Online services, downloads, memberships, future SaaS |

### Three Portals

- **Customer Portal** — Account, orders, bookings, wishlist, wallet, notifications
- **Vendor Portal** — Catalog, inventory, orders, analytics, payouts
- **Admin Portal** — CMS, CRM, finance, marketing, RBAC, audit logs

### Technology Stack (Approved — Directional)

| Layer | Technology |
|-------|------------|
| Frontend | Next.js, React, TypeScript, Tailwind CSS, Shadcn UI |
| Backend | ASP.NET Core, REST API, GraphQL |
| Database | SQL Server |
| Auth | JWT, OAuth, Social Login |
| Payments (Phase 1) | Razorpay, UPI, COD |
| Payments (Future) | Stripe, PayPal |
| Cloud | Azure / AWS |

### Current Project Phase

The project is in **Phase 1 (Business Detail)** documentation. Phase 0 (Business Foundation) is complete. **No application code exists yet** — this is by design.

---

## Document Authority Hierarchy

When documents conflict, the higher-priority document governs. Never silently resolve conflicts — surface them to the project owner.

| Priority | Document | Role |
|----------|----------|------|
| 1 | `MASTER_PROJECT_BIBLE.md` | Single source of truth |
| 2 | `PROJECT_RULES.md` | Governance |
| 3 | `docs/01_Project/*` | Phase 0 foundation |
| 4 | `docs/02_Business/*` | Phase 1 detail |
| 5 | `docs/03_Product/*` | Product specs |
| 6 | `README.md` | Public overview |
| 7 | `PROJECT_INDEX.md` | Navigation |
| 8 | `TASKS.md` | Operational backlog |

---

## Phase Gate System

The project enforces **phase-gate discipline** — certain artifact types are forbidden until the documentation gate for that phase is passed and approved by the project owner.

### Current Phase Status

| Phase | Directory | Status | Gate Condition |
|-------|-----------|--------|----------------|
| 0 — Business Foundation | `docs/01_Project/` | ✅ Complete | All 10 docs approved |
| 1 — Business Detail | `docs/02_Business/` | 🔄 In Progress | PRDs + compliance + decisions |
| Product Specs | `docs/03_Product/` | 🔄 In Progress | Alignment with Master Bible needed |
| 2 — Architecture | `docs/05_Architecture/` | 📋 Planned | Phase 1 approval required |
| 3 — Data Design | `docs/16_Database/` | 📋 Planned | Phase 2 approval required |
| 4 — API Design | `docs/17_API/` | 📋 Planned | Phase 3 approval required |
| 5 — UX & Design | `docs/06_UX/`, `docs/07_UI/`, `docs/08_Design_System/` | 📋 Planned | Phase 4 approval required |
| 6 — Engineering | Code repositories | 📋 Planned | Phase 5 approval required |
| 7 — Operations | `docs/19_Deployment/` | 📋 Planned | Phase 6 approval required |
| 8 — Launch | Launch artifacts | 📋 Planned | Phase 7 approval required |

### What Is Permitted at Current Phase (Phase 1)

- Writing and editing Markdown (`.md`) documentation
- Creating new documents within approved directories
- Updating `AI_MASTER_PROMPT.md`, `TASKS.md`, `CHANGELOG.md`, `mkdocs.yml`
- Suggesting architectural options for deferred decisions (without implementing)

### What Is Forbidden Until Later Phases

| Artifact Type | Blocked Until |
|---------------|--------------|
| Application code (TypeScript, C#, JavaScript, etc.) | Phase 6 (Engineering) |
| Database schemas, migrations, ERDs | Phase 3 (Data Design) approved |
| API endpoint implementations | Phase 4 (API Design) approved |
| UI designs, mockups, wireframes | Phase 5 (UX & Design) approved |
| Infrastructure configuration | Phase 7 (Operations) approved |
| CI/CD pipeline definitions | Phase 6 (Engineering) approved |

---

## Documentation Standards — Non-Negotiable

Every Markdown document created or modified in this repository must conform to these standards.

### Metadata Block (Required at Top of Every Document)

```markdown
# Document Title

> **Version:** 1.0
> **Status:** Draft
> **Last Updated:** [Month Year]
> **Document Owner:** Product Architecture
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](path/to/MASTER_PROJECT_BIBLE.md)
```

### Required Document Sections

1. Title
2. Metadata block
3. Purpose statement
4. Table of contents (if longer than one page)
5. Body content with logical headings
6. Related Documents table (≥ 2 links)
7. Revision History (for master-level documents)

### Writing Style

- Professional enterprise English — complete sentences
- No telegraphic shorthand, bullet fragments, or one-word items
- Define all acronyms on first use
- Use exact terminology from `MASTER_PROJECT_BIBLE.md#glossary`
- Mark items explicitly as: **decided**, **proposed**, or **future**
- Never use "etc." or "and more" in scope documents — be exhaustive and specific

### Cross-Reference Rule

Every document must:
- Reference its parent document in the Master Bible hierarchy
- Link to at least two related documents
- Use only terminology consistent with the Master Bible Glossary

### Naming Conventions

| Item | Convention | Example |
|------|------------|---------|
| Documentation files | PascalCase with underscores | `Market_Strategy.md` |
| Phase directories | Numeric prefix | `docs/02_Business/` |
| Master-level root files | ALL_CAPS with underscores | `MASTER_PROJECT_BIBLE.md` |
| No spaces in file or folder names | Enforced | ✅ `User_Journey.md` ❌ `User Journey.md` |

---

## Scope Boundaries

### In Scope for MVP

- All five verticals (Marketplace, Services, Insurance, Travel, Digital)
- Three portals (Customer, Vendor, Admin)
- India-first payments: Razorpay, UPI, cards, net banking, wallets, COD
- J&K / Srinagar marketplace positioning
- Shared services: Auth, RBAC, notifications, search, CRM, CMS, finance, audit

### Explicitly Out of Scope for MVP

| Item | Reason |
|------|--------|
| International payments (Stripe, PayPal) | Phase 3 future |
| Native iOS / Android apps | Post-MVP |
| Blockchain or cryptocurrency | Not planned |
| Physical POS integration | Online-first |
| White-label multi-tenant SaaS | Year 3+ |
| Live AI recommendations (production) | Architecture-ready; implementation post-MVP |
| Multi-language beyond English/Hindi | Phase 2 |

---

## Open Decisions — Do Not Resolve Without Authorization

Eight architectural decisions are intentionally deferred in `Project_Scope.md`. **No agent may make assumptions or implement solutions for these without explicit project owner direction:**

| ID | Open Decision |
|----|--------------|
| D-01 | Multi-vendor cart split strategy (single cart vs. vendor-specific) |
| D-02 | Insurance partner integration model (API vs. manual lead handoff) |
| D-03 | Travel inventory source (vendor-managed vs. GDS/OTA API) |
| D-04 | Vendor onboarding model (self-serve vs. approval-based KYC) |
| D-05 | Guest checkout policy (allow vs. login required) |
| D-06 | Commission structure (flat rate vs. tiered vs. vertical-specific) |
| D-07 | Cloud primary provider (Azure vs. AWS vs. hybrid) |
| D-08 | Wallet scope (platform wallet with balance vs. payment-only) |

When a task touches one of these decisions, surface the open question and ask the project owner before proceeding.

---

## Major Change Protocol

The following changes are classified as **major** and require explicit project owner approval before any agent implements them:

- Adding or removing MVP verticals
- Changing primary geography or payment strategy
- Modifying the technology stack
- Altering user types or portal structure
- Changing the business model or revenue strategy
- Making architectural decisions (monolith vs. microservices, database strategy, etc.)

**Protocol:**
1. Document the proposed change with full rationale
2. Present to project owner and await approval
3. Only after approval: update Master Bible and all affected documents
4. Record in revision history

---

## Conflict Detection Rules

AI agents must detect and flag the following conditions rather than silently proceeding:

| Condition | Required Action |
|-----------|----------------|
| Two documents contradict each other | Flag both, cite document hierarchy, ask project owner |
| A request would violate a phase gate | Explain the restriction and the gate that must be passed |
| A request touches a deferred decision (D-01 to D-08) | Surface the open decision and ask |
| A new document would duplicate an existing one | Point to the existing document, ask if it should be updated instead |
| A link target is empty or missing | Flag the broken link, do not create content that depends on it |

---

## Git and Repository Safety Rules

These rules apply to all AI agents operating in this repository:

| Rule | Rationale |
|------|-----------|
| Never commit without explicit project owner request | Prevents unauthorized changes to repository history |
| Use conventional commit messages: `type(scope): description` | Consistency with project standards |
| Valid commit types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore` | PROJECT_RULES.md standard |
| Never force-push to `main` or `master` | Protects shared history |
| Never skip git hooks | Hooks enforce quality gates |
| Never commit credentials, secrets, or `.env` files | Security requirement |
| Never amend commits pushed to remote | Preserves audit trail |
| Only stage specific files — never `git add .` without review | Prevents accidental secret commit |

---

## Compliance and Regulatory Context

The platform operates under Indian law. Documentation and architecture must account for:

| Regulation | Applicability |
|------------|---------------|
| **GST Act** | All taxable transactions — GST calculation, invoicing, vendor GSTIN |
| **RBI Payment Guidelines** | Razorpay PCI-DSS compliant payment processing |
| **IRDAI Regulations** | Insurance vertical — only licensed partners, clear aggregator disclosure |
| **DPDP Act 2023** | All personal data — consent-based collection, deletion rights |
| **Consumer Protection Act 2019** | Clear pricing, return/refund policies, grievance redressal |
| **IT Act 2000** | Data security, electronic records |
| **GI Act** | Accurate GI tagging for Pashmina and other protected regional products |

When producing content related to insurance, payments, or personal data, these compliance requirements must be respected and never contradicted.

---

## Repository Health Reference

The following known issues were identified in the July 2026 audit. Agents should be aware of these when navigating the repository:

| Issue | Location | Status |
|-------|----------|--------|
| Empty AI context bundle | `AI_MASTER_PROMPT.md` | Needs content |
| Empty task backlog | `TASKS.md` | Needs active tasks |
| Empty changelog | `CHANGELOG.md` | Needs entries |
| Empty doc site config | `mkdocs.yml` | Needs configuration |
| Three empty Phase 1 documents | `docs/02_Business/` | `Market_Strategy.md`, `Revenue_Model.md`, `User_Journey.md` |
| Product docs lack metadata and cross-references | `docs/03_Product/` | Quality remediation needed |
| Release Plan contradicts MVP scope | `docs/03_Product/Release_Plan.md` | Needs reconciliation |
| 16 directories are empty | `docs/04_Research/` through `docs/19_Deployment/` | Await phase execution |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [PROJECT_RULES.md](PROJECT_RULES.md) | Governance and standards |
| [PROJECT_INDEX.md](PROJECT_INDEX.md) | Repository navigation and status |
| [CLAUDE.md](CLAUDE.md) | Claude Code specific operating manual |
| [docs/01_Project/Project_Roadmap.md](docs/01_Project/Project_Roadmap.md) | Phased delivery plan |
| [docs/01_Project/Project_Scope.md](docs/01_Project/Project_Scope.md) | MVP scope boundaries |
| [docs/01_Project/Success_Metrics.md](docs/01_Project/Success_Metrics.md) | KPIs and success criteria |

---

*This file must be kept current whenever the project phase, schema, or governance changes. All AI tools reading this file are bound by its contents for the duration of their engagement with this repository.*
