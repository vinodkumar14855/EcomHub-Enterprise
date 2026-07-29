# CLAUDE.md — Claude Code Operating Manual for EcomHub Enterprise

> **For:** Claude Code (claude-code CLI and IDE extensions)
> **Authority:** This file is the Claude-specific operating layer. It supplements but never overrides [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md).
> **Last Updated:** July 2026

---

## Session Startup Protocol

Every Claude Code session must begin with this sequence before taking any action:

1. Read `MASTER_PROJECT_BIBLE.md` — single source of truth
2. Read `PROJECT_RULES.md` — governance and standards
3. Read `PROJECT_INDEX.md` — current repository state and phase status
4. Read this file (`CLAUDE.md`) — Claude-specific operating instructions
5. Read any document directly relevant to the user's request

**Do not skip this sequence.** The project contains multiple phases with strict gate rules. Working from memory or assumptions will produce incorrect output.

---

## Project Identity (Quick Reference)

| Attribute | Value |
|-----------|-------|
| **Platform** | EcomHub Enterprise — multi-vendor commerce platform |
| **Current Phase** | Phase 0 complete; Phase 1 in progress |
| **Active Branch** | `documentation` |
| **Governed By** | `MASTER_PROJECT_BIBLE.md` |
| **Phase Gate** | No code, DB, or UI artifacts until Phase 5+ documentation is approved |
| **Tech Stack** | Next.js · ASP.NET Core · SQL Server · Razorpay · Azure/AWS |
| **Launch Market** | India — Jammu & Kashmir / Srinagar |

---

## Document Authority Hierarchy

Resolve all conflicts using this priority order (highest first):

| Priority | Document | Role |
|----------|----------|------|
| 1 | `MASTER_PROJECT_BIBLE.md` | Single source of truth |
| 2 | `PROJECT_RULES.md` | Governance and standards |
| 3 | `docs/01_Project/*` | Business foundation (Phase 0) |
| 4 | `docs/02_Business/*` | Business detail (Phase 1) |
| 5 | `docs/03_Product/*` | Product specifications |
| 6 | `README.md` | Public overview (must align with Bible) |
| 7 | `PROJECT_INDEX.md` | Navigation and status |
| 8 | `TASKS.md` | Operational backlog |
| 9 | `AI_MASTER_PROMPT.md` | Condensed AI context |

If any document contradicts the Master Bible, **flag the contradiction** and ask the project owner before acting.

---

## Phase Gate Rules — What Is Permitted Now

The project is in **Phase 1 (Business Detail)**. Phase 0 documentation is complete.

### Currently Permitted

- Creating and editing Markdown documentation (`.md` files)
- Adding new documents inside `docs/01_Project/`, `docs/02_Business/`, `docs/03_Product/`
- Updating `AI_MASTER_PROMPT.md`, `TASKS.md`, `CHANGELOG.md`, `mkdocs.yml`
- Writing git commits when explicitly requested
- Adding new numbered directories under `docs/` when authorized

### Strictly Forbidden Until Phase 5+ Approval

| Forbidden Action | Reason |
|-----------------|--------|
| Writing application code (`.ts`, `.tsx`, `.cs`, `.js`, etc.) | Phase 0/1 restrictions — PROJECT_RULES.md |
| Creating database schemas or migration files | Phase 3 gate not passed |
| Creating API endpoint implementations | Phase 4 gate not passed |
| Creating UI mockups, wireframes, or design files | Phase 5 gate not passed |
| Deploying or configuring infrastructure | Phase 7 gate not passed |
| Force-pushing to `main` | Git safety rule |
| Creating commits without explicit request | AI assistant rule |
| Inventing scope not in approved documents | Scope boundary rule |
| Overriding the Master Bible without approval | Governance rule |
| Creating `.env` files or credential files | Security rule |

---

## Documentation Standards — Every File You Create

### Required Metadata Block

Every new Markdown document must open with:

```markdown
# Document Title

> **Version:** 1.0
> **Status:** Draft
> **Last Updated:** [Month Year]
> **Document Owner:** Product Architecture
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)
```

### Required Sections (in order)

1. **Title** — Clear, descriptive
2. **Metadata block** — Version, Status, Last Updated, Owner, Parent Document
3. **Purpose** — Why this document exists (2–4 sentences)
4. **Table of Contents** — For documents longer than one page
5. **Body content** — Organized with logical headings
6. **Related Documents** — Table linking to ≥ 2 related docs
7. **Revision History** — For master-level documents

### Writing Style Rules

- Enterprise professional English — complete sentences, no telegraphic shorthand
- Define every acronym on first use
- Use the exact terminology from `MASTER_PROJECT_BIBLE.md#glossary`
- Distinguish **decided**, **proposed**, and **future** items explicitly
- Be specific — never write "etc." or "and more" in scope documents
- All docs must cross-reference their parent document in the Master Bible hierarchy

### Naming Conventions

| Type | Convention | Example |
|------|------------|---------|
| Multi-word doc names | PascalCase with underscores | `Revenue_Model.md` |
| Phase directories | Number prefix | `docs/02_Business/` |
| Master-level docs | SCREAMING_SNAKE at root | `MASTER_PROJECT_BIBLE.md` |
| No spaces in paths | Enforced | `Business_Goals.md` not `Business Goals.md` |

---

## Directory Schema (Canonical)

This is the **authorized** directory structure per the Master Bible. Do not create directories outside this schema without project owner approval.

```
docs/
├── 01_Project/          Phase 0 — Business foundation       ✅ Complete
├── 02_Business/         Phase 1 — Business detail           🔄 In progress
├── 03_Product/          Product specifications               🔄 In progress
├── 04_Research/         Research and competitive analysis    📋 Planned
├── 05_Architecture/     System design and ADRs               📋 Planned
├── 06_UX/               User experience and wireframes       📋 Planned
├── 07_UI/               UI specifications                    📋 Planned
├── 08_Design_System/    Design system and components         📋 Planned
├── 09_Marketplace/      Marketplace vertical PRDs            📋 Planned
├── 10_Travel/           Travel vertical PRDs                 📋 Planned
├── 11_Services/         Services vertical PRDs               📋 Planned
├── 12_Insurance/        Insurance vertical PRDs              📋 Planned
├── 13_Customer/         Customer portal documentation        📋 Planned
├── 14_Vendor/           Vendor portal documentation          📋 Planned
├── 15_Admin/            Admin portal documentation           📋 Planned
├── 16_Database/         Data models and schemas              📋 Planned
├── 17_API/              API specifications                   📋 Planned
├── 18_AI/               AI features documentation            📋 Planned
└── 19_Deployment/       Deployment and operations            📋 Planned
```

---

## Deferred Decisions — Do Not Resolve Unilaterally

These eight decisions from `Project_Scope.md` are intentionally open. **Do not make assumptions or implement solutions for them** without explicit project owner direction:

| ID | Decision | Impact |
|----|----------|--------|
| D-01 | Multi-vendor cart split strategy | Checkout architecture |
| D-02 | Insurance integration model | Insurance vertical depth |
| D-03 | Travel inventory source (own vs GDS) | Travel vertical architecture |
| D-04 | Vendor onboarding model (self-serve vs approval) | Vendor portal workflow |
| D-05 | Guest checkout policy | Auth flow |
| D-06 | Commission structure (flat vs tiered) | Finance module |
| D-07 | Cloud primary provider (Azure vs AWS) | Infrastructure |
| D-08 | Wallet scope (platform wallet vs payment-only) | Payment architecture |

When a user request touches one of these decisions, **surface the open decision and ask** before proceeding.

---

## Interaction Rules

### Before Starting Any Task

1. Confirm which phase the requested work belongs to
2. Confirm the phase gate has been passed for that work type
3. Identify all documents that need to be read for context
4. If the task involves a deferred decision, flag it

### When Creating New Documents

1. Check `PROJECT_INDEX.md` to confirm the document doesn't already exist
2. Place it in the correct phase directory
3. Apply the full documentation standard (metadata, ToC, related docs)
4. Cross-reference from the new document back to the Master Bible
5. Update `PROJECT_INDEX.md` to reflect the new document
6. Note in your response that the index should be updated

### When Asked to Make Major Changes

Major changes (per `PROJECT_RULES.md`) include changes to:
- MVP verticals, geography, or payment strategy
- Technology stack choices
- User types or portal structure
- Business or revenue model
- Architecture approach

**Process for major changes:** Document the proposed change with rationale → present to project owner for approval → only then update documents.

### When Documents Conflict

If you detect a conflict between two documents, **do not silently resolve it**. Flag both versions, identify which document has higher authority in the hierarchy, and ask the project owner to confirm the correct position before updating anything.

---

## Git Rules

- Never commit without explicit request from project owner
- Follow conventional commit style: `docs(scope): description`
- Valid types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`
- Never force-push to `main` or `master`
- Never skip git hooks
- Never commit credential files, `.env` files, or files with real secrets
- Never amend commits that have been pushed to remote

---

## Known Issues to Watch For

These are open issues identified during the July 2026 repository audit:

| Issue | Location | Action Required |
|-------|----------|-----------------|
| `AI_MASTER_PROMPT.md` is empty | Root | Needs to be written |
| `TASKS.md` is empty | Root | Needs active task list |
| `CHANGELOG.md` is empty | Root | Needs changelog entries |
| `mkdocs.yml` is empty | Root | Needs site configuration |
| `Market_Strategy.md` is empty | `docs/02_Business/` | Phase 1 gap |
| `Revenue_Model.md` is empty | `docs/02_Business/` | Phase 1 gap |
| `User_Journey.md` is empty | `docs/02_Business/` | Phase 1 gap |
| `docs/03_Product/` docs lack metadata and cross-references | `docs/03_Product/` | Quality remediation needed |
| `Release_Plan.md` contradicts MVP scope | `docs/03_Product/` | Needs reconciliation with Master Bible |
| 7 broken links pointing to empty files | Multiple docs | Blocked until empty files are filled |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [PROJECT_RULES.md](PROJECT_RULES.md) | Governance and standards |
| [PROJECT_INDEX.md](PROJECT_INDEX.md) | Repository navigation and status |
| [AGENTS.md](AGENTS.md) | Tool-agnostic AI agent operating manual |
| [docs/01_Project/Project_Roadmap.md](docs/01_Project/Project_Roadmap.md) | Phased delivery plan |
| [docs/01_Project/Project_Scope.md](docs/01_Project/Project_Scope.md) | MVP boundaries |

---

*This file is read automatically by Claude Code at session start. Keep it current whenever the project phase, schema, or governance changes.*
