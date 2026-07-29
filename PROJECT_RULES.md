# EcomHub Enterprise — Project Rules

> **Version:** 1.0  
> **Status:** Active  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines the **rules, standards, and governance** for the EcomHub Enterprise project. All contributors — human and AI — must follow these rules when creating documentation, code, designs, or architectural artifacts.

When in doubt, refer to [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md) as the single source of truth.

---

## Table of Contents

1. [Documentation Standards](#documentation-standards)
2. [Document Hierarchy & Authority](#document-hierarchy--authority)
3. [Naming Conventions](#naming-conventions)
4. [Change Management](#change-management)
5. [Phase Gate Rules](#phase-gate-rules)
6. [Scope Boundaries](#scope-boundaries)
7. [Technology Governance](#technology-governance)
8. [AI Assistant Rules](#ai-assistant-rules)
9. [Git & Repository Rules](#git--repository-rules)
10. [Review & Approval Process](#review--approval-process)
11. [Quality Standards](#quality-standard)

---

## Documentation Standards

### Format

- All documentation must be written in **Markdown** (`.md`).
- Use clear headings, tables, and lists for scannability.
- Include document metadata at the top: version, status, last updated, owner.
- Cross-reference related documents using relative links.
- Do not use proprietary or binary formats for documentation.

### Structure

Every document must include:

1. **Title** — Clear, descriptive document name
2. **Metadata block** — Version, status, date, owner
3. **Purpose statement** — Why this document exists
4. **Table of contents** — For documents longer than one page
5. **Body content** — Organized with logical headings
6. **Related documents** — Links to interconnected docs
7. **Revision history** — For master-level documents

### Writing Style

- Use plain, professional English suitable for enterprise stakeholders.
- Write in complete sentences; avoid telegraphic shorthand.
- Define acronyms on first use.
- Be specific — avoid vague terms like "etc." or "and more" in scope documents.
- Distinguish between **decided**, **proposed**, and **future** items explicitly.

### Interconnection Rule

All documentation must be **interconnected**. Every document must:

- Reference its parent document in the Master Bible hierarchy.
- Link to at least two related documents where applicable.
- Use consistent terminology from the [Glossary](MASTER_PROJECT_BIBLE.md#glossary).

---

## Document Hierarchy & Authority

Documents are authoritative in this order (highest to lowest):

| Priority | Document | Role |
|----------|----------|------|
| 1 | `MASTER_PROJECT_BIBLE.md` | Single source of truth |
| 2 | `PROJECT_RULES.md` | Governance and standards |
| 3 | `docs/01_Project/*` | Business foundation |
| 4 | Phase-specific docs (`docs/02_*` through `docs/09_*`) | Domain and technical detail |
| 5 | `README.md` | Public overview (must stay aligned with Bible) |
| 6 | `TASKS.md` | Operational backlog |
| 7 | `AI_MASTER_PROMPT.md` | AI context bundle |

If `README.md` conflicts with the Master Bible, **update README.md** to match the Bible.

---

## Naming Conventions

### Documentation Files

| Rule | Example |
|------|---------|
| Use PascalCase with underscores for multi-word doc names | `Project_Vision.md` |
| Prefix phase directories with numbers | `docs/01_Project/` |
| No spaces in file or directory names | ✅ `Business_Goals.md` ❌ `Business Goals.md` |
| Master-level docs at repository root | `MASTER_PROJECT_BIBLE.md` |

### Future Code Conventions (Reference — Not Active Yet)

| Layer | Convention |
|-------|------------|
| Frontend components | PascalCase — `ProductCard.tsx` |
| Frontend utilities | camelCase — `formatPrice.ts` |
| Backend projects/namespaces | PascalCase — `EcomHub.Marketplace` |
| API endpoints | kebab-case — `/api/v1/product-catalog` |
| Database tables | PascalCase singular — `Order`, `Vendor` |
| Environment variables | SCREAMING_SNAKE_CASE — `RAZORPAY_KEY_ID` |

> Code conventions become enforceable when Phase 6 (Engineering) documentation is approved.

---

## Change Management

### Minor Changes

Minor changes (typo fixes, clarifications, non-scope edits) may be made directly with a note in the revision history.

### Major Changes

Major changes require **explicit approval** before implementation. Major changes include:

- Adding or removing MVP verticals
- Changing primary geography or payment strategy
- Altering technology stack choices
- Modifying user types or portal structure
- Changing business model or revenue strategy
- Architectural decisions (monolith vs microservices, database strategy)

**Process:**

1. Document the proposed change with rationale.
2. Present to project owner for approval.
3. Update Master Bible and all affected documents.
4. Record in revision history.

### AI Assistant Constraint

AI assistants must **ask before making major architectural changes**. See [AI Assistant Rules](#ai-assistant-rules).

---

## Phase Gate Rules

Documentation and artifacts must be created in phase order. Do not skip phases.

| Phase | Gate — Must Be Complete Before Proceeding |
|-------|---------------------------------------------|
| **Phase 0** | Business foundation docs approved |
| **Phase 1** | Domain PRDs and compliance matrix drafted |
| **Phase 2** | Architecture and ADRs approved |
| **Phase 3** | Data models approved |
| **Phase 4** | API specifications approved |
| **Phase 5** | Design system and UX approved |
| **Phase 6** | Engineering standards and CI/CD defined |
| **Phase 7** | Operations runbooks defined |
| **Phase 8** | Release plan and risk register approved |

### Phase 0 Restrictions (Current)

During Phase 0, the following are **prohibited**:

- ❌ Writing application code
- ❌ Creating UI designs or mockups
- ❌ Creating database schemas or migrations
- ❌ Creating API endpoint implementations
- ❌ Deploying infrastructure

Phase 0 is **business and product foundation only**.

---

## Scope Boundaries

### In Scope (MVP)

- All five verticals as defined in [Project_Scope.md](docs/01_Project/Project_Scope.md)
- Three portals: Customer, Vendor, Admin
- India-first payments via Razorpay and COD
- J&K / Srinagar marketplace positioning
- Shared platform services (auth, payments, notifications, RBAC, audit)

### Out of Scope (MVP)

- International payments (Stripe, PayPal) — future phase
- Native mobile apps (iOS/Android) — responsive web first
- Blockchain or cryptocurrency payments
- Physical POS integration
- White-label multi-tenant SaaS for third parties
- Full SaaS product suite (placeholder only in Digital vertical)

### Deferred Decisions

The following require clarification before Phase 2 architecture:

- Multi-vendor cart split strategy
- Insurance partner integration model
- Travel inventory source (own vs API/GDS)
- Vendor self-serve vs approval-based onboarding
- Guest checkout policy

---

## Technology Governance

### Approved Stack (Directional)

As defined in [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md#technology-stack). Changes to the stack require formal approval.

### Architecture Decision Records (ADRs)

All significant technical decisions must be recorded as ADRs in `docs/03_Architecture/adr/` during Phase 2. Format:

```
# ADR-NNN: Title

## Status
Proposed | Accepted | Deprecated | Superseded

## Context
Why this decision is needed.

## Decision
What was decided.

## Consequences
Positive and negative outcomes.
```

### API Strategy

- REST for CRUD and external integrations
- GraphQL for flexible frontend data fetching
- Final boundary decisions deferred to Phase 4

---

## AI Assistant Rules

This repository is designed for AI-assisted development. All AI tools (Cursor, Claude Code, Copilot, NotebookLM) must follow these rules:

### Must Do

1. Read `MASTER_PROJECT_BIBLE.md` before any significant work.
2. Follow phase gate rules — do not create code/design/DB artifacts in Phase 0.
3. Keep all documentation interconnected with cross-references.
4. Match existing naming conventions and writing style.
5. Ask before making major architectural changes.
6. Reference [README.md](README.md) and Phase 0 docs when generating content.
7. Minimize scope — only change what is requested.

### Must Not Do

1. Create commits unless explicitly requested by the project owner.
2. Invent scope not defined in approved documents.
3. Override the Master Bible without approval.
4. Create secrets, credentials, or `.env` files with real values.
5. Skip documentation when implementing features (in future phases).
6. Force-push to main/master branches.

### AI Context Bundle

`AI_MASTER_PROMPT.md` provides a condensed context for AI sessions. It must be kept in sync when Phase 0 docs change.

---

## Git & Repository Rules

### Branching (Future — When Code Begins)

| Branch | Purpose |
|--------|---------|
| `main` | Production-ready code |
| `develop` | Integration branch |
| `feature/*` | Feature development |
| `docs/*` | Documentation updates |
| `fix/*` | Bug fixes |

### Commit Messages

Follow conventional style:

```
type(scope): concise description

feat(marketplace): add product catalog API
docs(project): update Phase 0 vision document
fix(checkout): resolve Razorpay webhook validation
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

### Protected Actions

- Never force-push to `main` or `master`
- Never skip git hooks unless explicitly requested
- Never commit secrets or credential files
- Never amend commits that have been pushed to remote

---

## Review & Approval Process

### Documentation Review

| Document Type | Reviewer |
|---------------|----------|
| Master Bible | Project Owner + Product Architecture |
| Phase 0 docs | Project Owner |
| Architecture docs (Phase 2+) | Project Owner + Tech Lead |
| API specs (Phase 4+) | Tech Lead |
| PRDs (Phase 1+) | Product Owner |

### Approval States

| Status | Meaning |
|--------|---------|
| **Draft** | Work in progress, not authoritative |
| **Review** | Ready for stakeholder review |
| **Approved** | Authoritative, governs implementation |
| **Deprecated** | Superseded, kept for history |

Current Phase 0 documents are in **Draft** status pending project owner review.

---

## Quality Standards

### Documentation Quality Checklist

Before marking any document as "Review":

- [ ] Metadata block present
- [ ] Purpose statement clear
- [ ] Cross-references to related docs included
- [ ] Terminology matches Glossary
- [ ] No contradictions with Master Bible
- [ ] Scope items marked as decided/proposed/future
- [ ] Revision history updated (for master docs)

### Enterprise Standards

- All customer-facing content must support accessibility (WCAG 2.1 AA — future Phase 5).
- All payment flows must comply with PCI-DSS via gateway tokenization.
- All data handling must comply with India DPDP Act principles.
- Insurance flows must comply with IRDAI regulations.
- Audit logs required for all admin and financial actions.

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [docs/01_Project/Project_Scope.md](docs/01_Project/Project_Scope.md) | MVP scope boundaries |
| [docs/01_Project/Project_Roadmap.md](docs/01_Project/Project_Roadmap.md) | Delivery phases |
| [README.md](README.md) | Public project overview |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 0 release |

---

*All contributors must read this document before contributing to EcomHub Enterprise.*
