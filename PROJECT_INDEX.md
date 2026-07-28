# PROJECT_INDEX.md — EcomHub Enterprise Repository Index

> **Version:** 1.1
> **Status:** Active
> **Last Updated:** July 2026
> **Document Owner:** Product Architecture
> **Purpose:** Single-file navigation guide to the entire EcomHub Enterprise repository. Reflects the state of the repository as of the July 2026 governance setup. Update this file whenever documents are added, completed, or restructured.

---

## Table of Contents

1. [Repository Overview](#repository-overview)
2. [Root Files](#root-files)
3. [Phase Status Dashboard](#phase-status-dashboard)
4. [Documentation Index by Directory](#documentation-index-by-directory)
5. [Document Relationship Map](#document-relationship-map)
6. [Empty Files Register](#empty-files-register)
7. [Broken Links Register](#broken-links-register)
8. [Auxiliary Directories](#auxiliary-directories)
9. [Open Decisions Register](#open-decisions-register)
10. [Navigation Quick Reference](#navigation-quick-reference)

---

## Repository Overview

| Attribute | Value |
|-----------|-------|
| **Project** | EcomHub Enterprise |
| **Type** | Enterprise multi-vendor commerce platform |
| **Current Phase** | Phase 1 — Business Detail (Phase 0 complete) |
| **Active Branch** | `documentation` |
| **Main Branch** | `main` |
| **Version** | 1.0 |
| **Status** | Planning — documentation-first, no code yet |
| **Launch Target** | India — Jammu & Kashmir / Srinagar |

### Repository Statistics (July 2026 Audit)

| Metric | Count |
|--------|-------|
| Total directories | 26 (including `.git`, auxiliary) |
| Total Markdown files | 30 |
| Files with substantive content | 23 |
| Empty Markdown files | 7 |
| Empty documentation directories | 16 |
| Git commits | 16 |
| Broken links (pointing to empty files) | 7 |

---

## Root Files

These files live at the repository root and govern the entire project.

| File | Status | Content | Purpose |
|------|--------|---------|---------|
| `README.md` | ✅ Complete | Project overview, modules, tech stack | Public-facing entry point |
| `MASTER_PROJECT_BIBLE.md` | ✅ Complete | Vision, scope, domains, tech, doc index | **Single source of truth** |
| `PROJECT_RULES.md` | ✅ Complete | Standards, governance, phase gates | Rules for all contributors |
| `CLAUDE.md` | ✅ Complete | Claude Code operating manual | AI assistant — Claude specific |
| `AGENTS.md` | ✅ Complete | Universal AI agent operating manual | AI assistant — all tools |
| `PROJECT_INDEX.md` | ✅ Complete | This file — full repository index | Navigation and status |
| `AI_MASTER_PROMPT.md` | ❌ Empty | — | AI context bundle — **needs content** |
| `CHANGELOG.md` | ❌ Empty | — | Release history — **needs content** |
| `TASKS.md` | ❌ Empty | — | Task backlog — **needs content** |
| `mkdocs.yml` | ❌ Empty | — | Documentation site config — **needs content** |
| `LICENSE` | ✅ Present | MIT license | Legal |
| `.gitignore` | ✅ Present | Git exclusions | Repository hygiene |

---

## Phase Status Dashboard

| Phase | Name | Directory | Docs Planned | Docs Complete | Docs Empty | Status |
|-------|------|-----------|-------------|---------------|------------|--------|
| **0** | Business Foundation | `docs/01_Project/` | 10 | 8 | 0 | ✅ **Complete** |
| **1** | Business Detail | `docs/02_Business/` | 12 | 3 | 3 | 🔄 **In Progress (~40%)** |
| **—** | Product Specifications | `docs/03_Product/` | — | 8 | 0 | ⚠️ **Outside schema — needs alignment** |
| **2** | Architecture | `docs/05_Architecture/` | 10 | 0 | 0 | 📋 **Not Started** |
| **3** | Data Design | `docs/16_Database/` | 6 | 0 | 0 | 📋 **Not Started** |
| **4** | API Design | `docs/17_API/` | 11 | 0 | 0 | 📋 **Not Started** |
| **5** | UX & Design | `docs/06_UX/`, `docs/07_UI/`, `docs/08_Design_System/` | 9 | 0 | 0 | 📋 **Not Started** |
| **6** | Engineering | Code (future) | 10 | 0 | 0 | 📋 **Not Started** |
| **7** | Operations | `docs/19_Deployment/` | 7 | 0 | 0 | 📋 **Not Started** |
| **8** | Launch & Delivery | Launch artifacts | 7 | 0 | 0 | 📋 **Not Started** |

**Legend:** ✅ Complete · 🔄 In Progress · ⚠️ Needs Attention · 📋 Not Started · ❌ Blocked

---

## Documentation Index by Directory

### `docs/01_Project/` — Phase 0: Business Foundation
**Status:** ✅ Complete | 8 of 10 planned docs present, all with full content

| File | Status | Purpose | Key References |
|------|--------|---------|---------------|
| `Project_Vision.md` | ✅ Complete | Long-term vision, mission, guiding principles | Links to Executive_Summary, Business_Goals, Roadmap |
| `Executive_Summary.md` | ✅ Complete | Stakeholder overview — opportunity, solution, delivery | Links to all Phase 0 docs |
| `Business_Goals.md` | ✅ Complete | Strategic business objectives (BG-01 through BG-P07) | Links to Vision, Objectives, Scope, Metrics |
| `Project_Scope.md` | ✅ Complete | MVP boundaries, in/out of scope, deferred decisions D-01–D-08 | Links to Business_Goals, Objectives, Roadmap |
| `Target_Audience.md` | ✅ Complete | User types, customer personas (C1–C6), vendor personas (V1–V5) | Links to Scope, Business_Goals, Vision |
| `Project_Objectives.md` | ✅ Complete | Platform objectives (PO-01 through PO-11) with traceability | Links to Business_Goals, Metrics, Scope |
| `Success_Metrics.md` | ✅ Complete | KPIs — North Star (GMV), platform, vertical, portal, technical | Links to Business_Goals, Objectives, Roadmap |
| `Project_Roadmap.md` | ✅ Complete | Phased delivery — Phase 0 through Post-Launch Growth | Links to Scope, Metrics, Objectives |

> **Note:** `Project_Roadmap.md` lists 10 Phase 0 deliverables (all ✅ Complete). The Master Bible Documentation Index also lists 10. Eight are the above docs; `MASTER_PROJECT_BIBLE.md` and `PROJECT_RULES.md` complete the set of 10.

---

### `docs/02_Business/` — Phase 1: Business Detail
**Status:** 🔄 In Progress | 6 files exist — 3 with content, 3 empty

| File | Status | Purpose | Blocked By |
|------|--------|---------|-----------|
| `Business_Model.md` | ✅ Complete | Marketplace model, multi-vendor model, commission structure, revenue streams | — |
| `Business_Requirements_Document.md` | ✅ Complete | BRD — business processes (BP-01–09), business rules (BR-01–D04), compliance matrix | — |
| `User_Personas.md` | ✅ Complete | 13 detailed personas: CP-01–04 (customer), VP-01–05 (vendor), AP-01–03 (admin) | — |
| `Market_Strategy.md` | ❌ **Empty** | Go-to-market strategy, competitive positioning | Needs to be written |
| `Revenue_Model.md` | ❌ **Empty** | Detailed revenue rates, commission tables, projections | Needs to be written |
| `User_Journey.md` | ❌ **Empty** | End-to-end user journeys per persona per vertical | Needs to be written |

> **Missing from Phase 1** (per `Project_Roadmap.md`): Per-vertical PRDs (5), Per-portal PRDs (3), Competitive Analysis (1). Total: 6 of 12 Phase 1 deliverables still missing.

---

### `docs/03_Product/` — Product Specifications
**Status:** ⚠️ Needs Alignment | 8 files, all with content — but outside Master Bible schema and below documentation standards

| File | Status | Purpose | Quality Issues |
|------|--------|---------|---------------|
| `Product_Requirements_Document.md` | ⚠️ Content present | Platform PRD — modules, roles, NFRs, integrations | No metadata block, no cross-references, telegraphic style |
| `Product_Strategy.md` | ⚠️ Content present | Product vision, positioning, pillars, growth phases | No metadata block, mentions WhatsApp (not in approved stack) |
| `Feature_Catalog.md` | ⚠️ Content present | Feature list — customer app, vendor portal, admin, platform | No metadata block, no cross-references |
| `Functional_Requirements.md` | ⚠️ Content present | FR-CUST, FR-PROD, FR-VENDOR, FR-SERVICE, FR-TRAVEL, FR-INS, FR-ADMIN | No metadata block, no revision history |
| `User_Stories.md` | ⚠️ Content present | Agile user stories — US-CUST, US-VEND, US-SERVICE, US-TRAVEL, US-INS, US-ADMIN | No metadata block, no cross-references |
| `Acceptance_Criteria.md` | ⚠️ Content present | AC per feature — AC-CUST, AC-PROD, AC-CART, AC-PAY, AC-ORDER, AC-SERVICE, AC-TRAVEL, AC-INS, AC-VENDOR, AC-ADMIN, AC-NOTIFY | No metadata block |
| `Product_Workflows.md` | ⚠️ Content present | 17 workflow diagrams — customer, vendor, travel, insurance, admin flows | No metadata block, no cross-references |
| `Release_Plan.md` | ⚠️ Content present | 7-phase release plan | **Contradicts Master Bible** — proposes phased vertical releases; Bible mandates all-5-verticals MVP |

> **Schema note:** This directory was created outside the Master Bible's phase schema. The Bible defines `docs/03_Architecture/` as the next directory after `02_Business`. A schema reconciliation decision is needed from the project owner.

---

### `docs/04_Research/` through `docs/19_Deployment/` — Future Phase Directories
**Status:** 📋 All 16 directories are empty — awaiting phase execution

| Directory | Intended Content | Phase Gate |
|-----------|-----------------|------------|
| `docs/04_Research/` | Research and competitive analysis | Phase 1 approval |
| `docs/05_Architecture/` | System design, C4 diagrams, ADRs | Phase 1 approval |
| `docs/06_UX/` | User experience, wireframes, user flows | Phase 4 (API) approval |
| `docs/07_UI/` | UI specifications, component inventory | Phase 4 (API) approval |
| `docs/08_Design_System/` | Design tokens, component library, Shadcn/Tailwind | Phase 4 (API) approval |
| `docs/09_Marketplace/` | Marketplace vertical deep-dive PRDs | Phase 1 approval |
| `docs/10_Travel/` | Travel vertical deep-dive PRDs | Phase 1 approval |
| `docs/11_Services/` | Services vertical deep-dive PRDs | Phase 1 approval |
| `docs/12_Insurance/` | Insurance vertical deep-dive PRDs | Phase 1 approval |
| `docs/13_Customer/` | Customer portal documentation | Phase 1 approval |
| `docs/14_Vendor/` | Vendor portal documentation | Phase 1 approval |
| `docs/15_Admin/` | Admin portal documentation | Phase 1 approval |
| `docs/16_Database/` | Data models, schemas, migration strategy | Phase 2 (Architecture) approval |
| `docs/17_API/` | REST and GraphQL API specifications | Phase 3 (Data Design) approval |
| `docs/18_AI/` | AI features — search, recommendations | Phase 2 (Architecture) approval |
| `docs/19_Deployment/` | Deployment runbooks, monitoring, SLAs | Phase 6 (Engineering) approval |

---

## Document Relationship Map

This map shows how documents connect to each other. Read it top-down from the Master Bible.

```
MASTER_PROJECT_BIBLE.md (Single Source of Truth)
│
├── PROJECT_RULES.md (Governance)
│   └── Governs all documents below
│
├── README.md (Public Overview)
│
├── CLAUDE.md (Claude Code operating manual)
├── AGENTS.md (Universal AI operating manual)
├── PROJECT_INDEX.md (This file — navigation)
│
├── docs/01_Project/ (Phase 0 — Foundation)
│   ├── Project_Vision.md
│   │   └── ← Referenced by: Executive_Summary, Business_Goals
│   ├── Executive_Summary.md
│   │   └── ← References: Vision, Business_Goals, Scope, Audience, Objectives, Metrics, Roadmap
│   ├── Business_Goals.md (BG-01 to BG-P07)
│   │   └── ← References: Vision, Objectives, Scope, Metrics, Roadmap
│   ├── Project_Scope.md (In/Out of scope + D-01 to D-08)
│   │   └── ← References: Business_Goals, Objectives, Audience, Roadmap
│   ├── Target_Audience.md (C1–C6, V1–V5, A1–A3)
│   │   └── ← References: Scope, Business_Goals, Vision, Metrics, Bible
│   ├── Project_Objectives.md (PO-01 to PO-11)
│   │   └── ← References: Business_Goals, Metrics, Scope, Roadmap
│   ├── Success_Metrics.md (SM-01 to SM-B05)
│   │   └── ← References: Business_Goals, Objectives, Roadmap, Scope
│   └── Project_Roadmap.md (Phases 0–8 + Post-Launch)
│       └── ← References: Scope, Metrics, Objectives, Business_Goals
│
└── docs/02_Business/ (Phase 1 — Business Detail)
    ├── Business_Model.md
    │   ├── → Links to: Revenue_Model.md ❌ (empty)
    │   ├── → Links to: Market_Strategy.md ❌ (empty)
    │   └── → Links to: User_Personas.md ✅, BRD ✅, Business_Goals ✅
    ├── Business_Requirements_Document.md
    │   ├── → Links to: Revenue_Model.md ❌ (empty)
    │   ├── → Links to: User_Journey.md ❌ (empty)
    │   ├── → Links to: Market_Strategy.md ❌ (empty)
    │   └── → Links to: Business_Model ✅, User_Personas ✅, Project_Scope ✅
    ├── User_Personas.md
    │   ├── → Links to: User_Journey.md ❌ (empty)
    │   ├── → Links to: Market_Strategy.md ❌ (empty)
    │   └── → Links to: BRD ✅, Target_Audience ✅, Bible ✅
    ├── Market_Strategy.md ← ❌ EMPTY — needed by 3 documents
    ├── Revenue_Model.md ← ❌ EMPTY — needed by 3 documents
    └── User_Journey.md ← ❌ EMPTY — needed by 3 documents
```

---

## Empty Files Register

Files that exist on disk but contain no substantive content. These create broken links and block downstream work.

| # | File | Size | Documents Linking to It | Priority |
|---|------|------|------------------------|----------|
| 1 | `AI_MASTER_PROMPT.md` | ~0 bytes | PROJECT_RULES.md, MASTER_PROJECT_BIBLE.md, CLAUDE.md | 🔴 Critical |
| 2 | `docs/02_Business/Revenue_Model.md` | 0 bytes | Business_Model.md, Business_Requirements_Document.md | 🔴 Critical |
| 3 | `docs/02_Business/Market_Strategy.md` | 0 bytes | Business_Model.md, Business_Requirements_Document.md, User_Personas.md | 🔴 Critical |
| 4 | `docs/02_Business/User_Journey.md` | 0 bytes | Business_Requirements_Document.md, User_Personas.md | 🟠 High |
| 5 | `TASKS.md` | ~0 bytes | PROJECT_RULES.md (referenced as living task backlog) | 🟠 High |
| 6 | `mkdocs.yml` | ~0 bytes | Documentation site cannot be built | 🟠 High |
| 7 | `CHANGELOG.md` | ~0 bytes | No release history tracked | 🟡 Medium |

---

## Broken Links Register

Links that resolve to a file that exists but is empty (content absent).

| # | Source Document | Link Text | Target File | Status |
|---|----------------|-----------|-------------|--------|
| 1 | `docs/02_Business/Business_Model.md` | Revenue_Model.md | `docs/02_Business/Revenue_Model.md` | ❌ Target empty |
| 2 | `docs/02_Business/Business_Model.md` | Market_Strategy.md | `docs/02_Business/Market_Strategy.md` | ❌ Target empty |
| 3 | `docs/02_Business/Business_Requirements_Document.md` | Revenue_Model.md | `docs/02_Business/Revenue_Model.md` | ❌ Target empty |
| 4 | `docs/02_Business/Business_Requirements_Document.md` | User_Journey.md | `docs/02_Business/User_Journey.md` | ❌ Target empty |
| 5 | `docs/02_Business/Business_Requirements_Document.md` | Market_Strategy.md | `docs/02_Business/Market_Strategy.md` | ❌ Target empty |
| 6 | `docs/02_Business/User_Personas.md` | User_Journey.md | `docs/02_Business/User_Journey.md` | ❌ Target empty |
| 7 | `docs/02_Business/User_Personas.md` | Market_Strategy.md | `docs/02_Business/Market_Strategy.md` | ❌ Target empty |

**Directories referenced in governance docs that do not exist:**

| Referenced Path | Referenced In | Status |
|----------------|--------------|--------|
| `docs/03_Architecture/adr/` | PROJECT_RULES.md (ADR format section) | ❌ Directory missing |

---

## Auxiliary Directories

These directories were established in the initial repository structure and are awaiting phase execution.

| Directory | Purpose | Status |
|-----------|---------|--------|
| `api/` | API specifications (OpenAPI/GraphQL) | ❌ Empty — Phase 4 (API Design) |
| `database/` | Database artifacts, migration scripts | ❌ Empty — Phase 3 (Data Design) |
| `assets/` | Static assets — logos, images, media | ❌ Empty |
| `design-system/` | Design system tokens and components | ❌ Empty — Phase 5 (UX & Design) |
| `prompts/` | AI prompt templates for development | ❌ Empty |
| `templates/` | Document templates for new files | ❌ Empty |
| `.github/workflows/` | CI/CD pipeline definitions | ❌ Empty — Phase 6 (Engineering) |

---

## Open Decisions Register

These eight decisions from `docs/01_Project/Project_Scope.md` must be resolved before Phase 2 (Architecture) begins. No agent or contributor may make assumptions on these without project owner direction.

| ID | Decision | Options Under Consideration | Impact Domain |
|----|----------|----------------------------|--------------|
| D-01 | Multi-vendor cart split strategy | Single cart with split orders vs. vendor-specific carts | Checkout, order management |
| D-02 | Insurance integration model | API integration vs. manual lead handoff | Insurance vertical architecture |
| D-03 | Travel inventory source | Vendor-managed vs. GDS/OTA API | Travel vertical architecture |
| D-04 | Vendor onboarding model | Self-serve vs. approval-based with KYC | Vendor portal workflow |
| D-05 | Guest checkout policy | Allow guest checkout vs. login required | Auth flow |
| D-06 | Commission structure | Flat rate vs. vertical-specific vs. tiered | Finance module |
| D-07 | Cloud primary provider | Azure vs. AWS vs. hybrid | Infrastructure |
| D-08 | Wallet scope | Platform wallet with stored balance vs. payment-only | Payment architecture |

---

## Navigation Quick Reference

### "I need to understand the project" → Start here

1. `README.md` — 2-minute overview
2. `MASTER_PROJECT_BIBLE.md` — full context (5 minutes)
3. `docs/01_Project/Project_Vision.md` — the why
4. `docs/01_Project/Project_Scope.md` — MVP boundaries

### "I need to work on business documentation" → Phase 1

1. `docs/02_Business/Business_Requirements_Document.md` — business rules and processes
2. `docs/02_Business/Business_Model.md` — revenue and marketplace mechanics
3. `docs/02_Business/User_Personas.md` — detailed personas
4. `docs/02_Business/Market_Strategy.md` — go-to-market (⚠️ currently empty)
5. `docs/02_Business/Revenue_Model.md` — commission rates (⚠️ currently empty)
6. `docs/02_Business/User_Journey.md` — user journeys (⚠️ currently empty)

### "I need to understand product requirements" → Phase 1 / Product

1. `docs/03_Product/Product_Requirements_Document.md` — platform PRD
2. `docs/03_Product/Functional_Requirements.md` — FR per module
3. `docs/03_Product/User_Stories.md` — agile user stories
4. `docs/03_Product/Acceptance_Criteria.md` — AC per feature
5. `docs/03_Product/Feature_Catalog.md` — complete feature list

### "I need to understand user workflows" → Product

1. `docs/03_Product/Product_Workflows.md` — 17 workflow diagrams
2. `docs/02_Business/User_Journey.md` — journey maps (⚠️ currently empty)

### "I need the rules and governance" → Governance

1. `PROJECT_RULES.md` — full governance manual
2. `MASTER_PROJECT_BIBLE.md#glossary` — terminology
3. `CLAUDE.md` — Claude Code specific rules
4. `AGENTS.md` — all AI tool rules

### "I need to understand what to build next" → Roadmap

1. `docs/01_Project/Project_Roadmap.md` — full phased plan
2. `TASKS.md` — living task backlog (⚠️ currently empty)

### "I'm an AI agent starting a new session" → Protocol

1. `MASTER_PROJECT_BIBLE.md`
2. `PROJECT_RULES.md`
3. `PROJECT_INDEX.md` (this file)
4. `CLAUDE.md` (if Claude Code) or `AGENTS.md` (if any other tool)
5. Documents relevant to the specific task

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial index — created from July 2026 repository audit |

---

*This index must be updated whenever: a new document is created, a document is completed, a phase changes status, or the repository structure changes. It is the navigation layer for all contributors — human and AI.*
