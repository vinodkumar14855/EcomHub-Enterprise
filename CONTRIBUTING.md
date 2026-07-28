# CONTRIBUTING.md — Contribution Guide for EcomHub Enterprise

> **Version:** 1.0
> **Status:** Active
> **Last Updated:** July 2026
> **Document Owner:** Product Architecture
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines the contribution process for EcomHub Enterprise — covering branch strategy, pull request rules, documentation standards, commit standards, code review process, and AI collaboration rules. All contributors, whether human engineers or AI coding agents, must follow this guide.

For the full governance framework, refer to [PROJECT_RULES.md](PROJECT_RULES.md). For AI-specific operating instructions, refer to [AGENTS.md](AGENTS.md) and [CLAUDE.md](CLAUDE.md).

---

## Table of Contents

1. [Who This Guide Applies To](#who-this-guide-applies-to)
2. [Phase Gate Reminder](#phase-gate-reminder)
3. [Branch Strategy](#branch-strategy)
4. [Pull Request Rules](#pull-request-rules)
5. [Commit Standards](#commit-standards)
6. [Documentation Standards](#documentation-standards)
7. [Code Review Process](#code-review-process)
8. [AI Collaboration Rules](#ai-collaboration-rules)
9. [Forbidden Actions](#forbidden-actions)
10. [Getting Help](#getting-help)
11. [Related Documents](#related-documents)

---

## Who This Guide Applies To

| Contributor Type | Applies? |
|-----------------|----------|
| Human engineers and product contributors | ✅ Yes — all sections |
| AI coding agents (Claude Code, Cursor, Copilot, Codex) | ✅ Yes — especially AI Collaboration Rules |
| External collaborators or reviewers | ✅ Yes — all sections |
| Project owner | ✅ Yes — review and approval sections |

---

## Phase Gate Reminder

The project is currently in **Phase 1 — Business Detail (Documentation)**. Before contributing any artifact, confirm it is permitted in the current phase.

| Phase | Permitted Artifacts |
|-------|---------------------|
| Phase 0 and 1 (current) | Markdown documentation (`.md`) only |
| Phase 2 and 3 (planned) | Architecture diagrams, data models |
| Phase 4 (planned) | API specifications (OpenAPI, GraphQL schema) |
| Phase 5 (planned) | UX wireframes, design tokens |
| Phase 6+ (planned) | Application code, database migrations, CI/CD |

If you are unsure which phase a contribution belongs to, consult [ROADMAP.md](ROADMAP.md) or ask the project owner before creating the artifact.

---

## Branch Strategy

### Branch Types

| Branch | Pattern | Purpose | Who Creates |
|--------|---------|---------|-------------|
| `main` | `main` | Production-ready, approved artifacts | Protected — merge via PR only |
| `documentation` | `documentation` | Active documentation work | Default working branch |
| `docs/*` | `docs/phase1-market-strategy` | Isolated documentation additions | Any contributor |
| `feature/*` | `feature/marketplace-prd` | Feature documentation or (future) feature code | Any contributor |
| `fix/*` | `fix/broken-cross-references` | Corrections to existing artifacts | Any contributor |
| `chore/*` | `chore/update-index` | Housekeeping (index updates, formatting) | Any contributor |

### Branching Rules

1. **Never commit directly to `main`.** All changes to `main` must go through a pull request.
2. **The `documentation` branch is the default working branch** during documentation phases. It is the integration branch for all doc-phase PRs.
3. **Create a named branch** for any non-trivial change (new document, significant edit, structural change). Use the patterns above.
4. **Branch from `documentation`** during Phases 0–5. Branch from `develop` (when created in Phase 6) for engineering work.
5. **Delete branches after merge.** Merged branches are removed to keep the branch list clean.
6. **Branch names use kebab-case** with the type prefix. No spaces, no special characters.

```
✅ docs/phase1-revenue-model
✅ feature/marketplace-vertical-prd
✅ fix/user-journey-broken-links
❌ "new document"
❌ DOCS_phase1
❌ myBranch
```

---

## Pull Request Rules

### When a PR Is Required

| Change Type | PR Required? |
|-------------|-------------|
| New Markdown document | ✅ Yes |
| Significant edit to existing document (scope, content, cross-references) | ✅ Yes |
| Structural directory or file rename | ✅ Yes |
| Minor corrections (typo, formatting, link fix) | Optional for `documentation` branch; required for `main` |
| Updating `PROJECT_INDEX.md`, `ROADMAP.md`, `DECISIONS.md` | ✅ Yes |

### PR Title Format

```
type(scope): concise description

docs(business): add revenue model document
docs(phase1): complete market strategy
fix(links): resolve broken cross-references in user-personas
chore(index): update project index with phase 1 additions
```

### PR Description Template

Every pull request description must include:

```markdown
## Summary
Brief description of what this PR adds or changes (1–3 sentences).

## Documents Changed
- `docs/02_Business/Revenue_Model.md` — New document: revenue stream definitions and commission rate tables
- `PROJECT_INDEX.md` — Updated to reflect new document

## Phase Gate Confirmation
- [ ] All artifacts in this PR are permitted in the current project phase
- [ ] No code, database schemas, or UI designs included (if in documentation phase)

## Documentation Standards Checklist
- [ ] Metadata block present (Version, Status, Last Updated, Owner, Parent Document)
- [ ] Purpose statement included
- [ ] Table of Contents included (if document is longer than one page)
- [ ] Cross-references to related documents included
- [ ] Terminology consistent with MASTER_PROJECT_BIBLE.md Glossary
- [ ] No contradictions with Master Bible
- [ ] Revision history updated

## Related Issues or Decisions
- Resolves: [Link to issue or decision ID, e.g., DECISIONS.md#D-06]
- References: [Related PRs or documents]

## Reviewer Notes
[Anything the reviewer should know — assumptions made, open questions, alternatives considered]
```

### PR Review Requirements

| Change Category | Required Reviewers | Approval Requirement |
|----------------|-------------------|----------------------|
| Master-level documents (Bible, Rules) | Project Owner | Project Owner must approve |
| Phase 0 documents | Project Owner | Project Owner must approve |
| Phase 1 documents | Project Owner | At least 1 approval |
| Governance files (CLAUDE.md, AGENTS.md, DECISIONS.md, CONTRIBUTING.md) | Project Owner | Project Owner must approve |
| Minor corrections and index updates | Any contributor | 1 approval sufficient |

### PR Merge Rules

- **Squash and merge** is the preferred merge strategy for documentation PRs to keep history clean.
- **Rebase and merge** may be used for feature branches when preserving individual commit history is valuable.
- **No merge commits** on `main` — keep main's history linear.
- PRs must pass all review requirements before merge.
- The author must not merge their own PR without a separate review approval.

---

## Commit Standards

### Commit Message Format

All commits follow the **Conventional Commits** specification:

```
type(scope): concise description in present tense

[optional body — explain WHY, not WHAT, if non-obvious]

[optional footer — references to issues, decisions, co-authors]
```

### Type Reference

| Type | When to Use |
|------|-------------|
| `docs` | Creating or editing documentation |
| `feat` | Adding a new feature or module (Phase 6+) |
| `fix` | Correcting a bug, broken link, or factual error |
| `style` | Formatting changes only — no content change |
| `refactor` | Restructuring without changing meaning |
| `test` | Adding or updating tests (Phase 6+) |
| `chore` | Housekeeping — index updates, tooling, config |
| `ci` | CI/CD pipeline changes (Phase 6+) |

### Scope Reference

Use the relevant scope to identify what was changed:

| Scope | Applies To |
|-------|-----------|
| `project` | `docs/01_Project/` documents |
| `business` | `docs/02_Business/` documents |
| `product` | `docs/03_Product/` documents |
| `architecture` | `docs/05_Architecture/` documents |
| `phase1`, `phase2`, etc. | Phase-level changes |
| `index` | `PROJECT_INDEX.md` |
| `roadmap` | `ROADMAP.md` |
| `decisions` | `DECISIONS.md` |
| `governance` | `CLAUDE.md`, `AGENTS.md`, `CONTRIBUTING.md`, `PROJECT_RULES.md` |
| `marketplace` | Marketplace vertical documents |
| `travel` | Travel vertical documents |
| `insurance` | Insurance vertical documents |
| `services` | Services vertical documents |
| `digital` | Digital vertical documents |

### Commit Examples

```
docs(business): add revenue model with commission rate tables

Defines approved commission rates for all five verticals and documents
the subscription tier discount structure. Resolves DECISIONS.md D-06.

docs(project): complete phase 0 project objectives document

fix(links): resolve 7 broken cross-references in 02_Business documents

Market_Strategy.md, Revenue_Model.md, and User_Journey.md were empty;
links to these files from Business_Model.md, BRD, and User_Personas.md
were flagged as broken in the July 2026 audit.

chore(index): update PROJECT_INDEX.md to reflect phase 1 additions

docs(governance): add DECISIONS.md architecture decision log
```

### Commit Rules

- **Write in the present tense:** "add document" not "added document"
- **Keep the subject line under 72 characters**
- **Explain the WHY in the body** when the reason is non-obvious
- **Reference decision IDs** when a commit resolves or relates to `DECISIONS.md` entries
- **One logical change per commit** — do not bundle unrelated changes
- **Never commit generated secrets**, credentials, or `.env` files
- **Never skip hooks** (`--no-verify`)

---

## Documentation Standards

All documentation created in this repository must conform to these standards, as defined in [PROJECT_RULES.md](PROJECT_RULES.md).

### Required Metadata Block

Every new document must begin with:

```markdown
# Document Title

> **Version:** 1.0
> **Status:** Draft
> **Last Updated:** [Month Year]
> **Document Owner:** Product Architecture
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](path/to/MASTER_PROJECT_BIBLE.md)
```

### Status Values

| Status | Meaning |
|--------|---------|
| `Draft` | Work in progress — not yet authoritative |
| `Review` | Ready for stakeholder review |
| `Approved` | Authoritative — governs implementation |
| `Deprecated` | Superseded — kept for history |

### Required Document Structure

1. **Title** — Clear and descriptive
2. **Metadata block** — Version, Status, Last Updated, Owner, Parent Document
3. **Purpose** — 2–4 sentences explaining why this document exists
4. **Table of Contents** — Required for documents longer than one printed page
5. **Body content** — Organized with logical headings and enterprise-quality prose
6. **Related Documents** — Table with at least two links to connected documents
7. **Revision History** — Required for all master-level and phase-level documents

### Writing Rules

- Use **complete sentences** — no bullet fragments, no telegraphic shorthand
- **Define every acronym** on first use
- Use **exact terminology** from `MASTER_PROJECT_BIBLE.md#glossary`
- Mark items explicitly as **Decided**, **Proposed**, or **Future**
- Be exhaustive and specific in scope documents — never write "etc." or "and more"
- **Distinguish facts from proposals**: approved decisions are stated as facts; unapproved items are clearly labelled "Proposed" and require formal approval before acting on them

### Naming Conventions

| Item | Convention | Example |
|------|------------|---------|
| Multi-word document names | PascalCase with underscores | `Market_Strategy.md` |
| Phase directories | Number prefix | `docs/02_Business/` |
| Master-level root files | ALL_CAPS with underscores | `MASTER_PROJECT_BIBLE.md` |
| No spaces in paths | Enforced | ✅ `User_Journey.md` ❌ `User Journey.md` |

### Interconnection Rule

Every document must:
- Reference its parent document (at minimum the Master Bible) in the metadata block
- Link to at least two related documents in the Related Documents section
- Use consistent terminology from the Master Bible Glossary

### Quality Checklist Before Marking "Review"

- [ ] Metadata block present and complete
- [ ] Purpose statement is clear and specific
- [ ] Cross-references to related docs included
- [ ] Terminology matches the Glossary in `MASTER_PROJECT_BIBLE.md`
- [ ] No contradictions with the Master Bible
- [ ] Scope items marked as decided/proposed/future
- [ ] Revision history updated
- [ ] Linked documents actually exist and have content (no links to empty files)

---

## Code Review Process

> **Note:** Code review applies from Phase 6 (Engineering) onwards. During documentation phases, "review" refers to document review, not code review. This section establishes the process ahead of Phase 6.

### Document Review Process (Current Phase)

1. **Author** creates or edits a document on a named branch
2. **Author** runs the Documentation Quality Checklist
3. **Author** opens a PR with the template above
4. **Reviewer** reads the document against the Master Bible for:
   - Factual accuracy and consistency with approved decisions
   - Documentation standards compliance
   - No broken links
   - No scope violations for the current phase
5. **Reviewer** leaves inline comments or approves
6. **Author** addresses comments and updates the PR
7. **Project Owner** gives final approval for master-level or phase-gated documents
8. **Author (or reviewer)** merges using squash merge

### Code Review Process (Phase 6+)

1. **Author** creates feature branch from `develop`; implements changes
2. **Author** ensures all tests pass locally and CI is green
3. **Author** opens PR with summary, test plan, and checklist
4. **At least one peer reviewer** reviews for correctness, security, performance, and style
5. **Tech Lead** approves for architecture-impacting changes
6. No PR may be merged with failing tests, security warnings, or unresolved review comments
7. Merge uses **squash and merge** for feature work; **rebase and merge** for critical fixes

### Review Principles

- **Review the artifact, not the author.** Feedback is always about the work.
- **Be specific.** Vague comments ("this seems off") are unhelpful; link to the governing document or rule.
- **Suggest, don't dictate** (unless it is a compliance or governance violation, which must be corrected).
- **Approve with comments** is permitted when comments are non-blocking — the author should still address them.
- **Acknowledge what is done well**, not only what needs changing.

---

## AI Collaboration Rules

AI coding agents (Claude Code, Cursor, GitHub Copilot, Codex, and others) are first-class contributors to this repository. The following rules govern how they must operate.

### Startup Protocol

Every AI agent session must begin by reading:

1. `MASTER_PROJECT_BIBLE.md`
2. `PROJECT_RULES.md`
3. `PROJECT_INDEX.md`
4. `CLAUDE.md` (Claude Code) or `AGENTS.md` (all other tools)
5. Any documents directly relevant to the current task

### Permitted AI Actions

| Action | Permitted |
|--------|-----------|
| Creating new Markdown documents (in current phase) | ✅ |
| Editing existing documents when explicitly requested | ✅ |
| Updating `PROJECT_INDEX.md`, `ROADMAP.md`, `DECISIONS.md` | ✅ |
| Suggesting content, structure, or phrasing improvements | ✅ |
| Identifying broken links, empty files, or standards violations | ✅ |
| Flagging conflicts between documents | ✅ |
| Creating git commits when explicitly requested | ✅ |

### Forbidden AI Actions

| Action | Reason |
|--------|--------|
| Creating application code in documentation phases | Phase gate violation |
| Modifying `MASTER_PROJECT_BIBLE.md` | Must not be changed without project owner approval |
| Modifying `PROJECT_RULES.md` | Must not be changed without project owner approval |
| Resolving deferred decisions (D-01 to D-08) unilaterally | Requires project owner decision |
| Making major changes without explicit approval | Change management rule |
| Committing without being explicitly asked | AI assistant governance rule |
| Force-pushing to any branch | Git safety rule |
| Creating secrets, credentials, or `.env` files | Security rule |
| Inventing scope, features, or decisions not in approved documents | Scope integrity rule |
| Silently resolving document conflicts | Must flag and ask |

### AI Document Quality Rule

When an AI agent creates a document, it must meet the full documentation standard:
- Complete metadata block
- Purpose statement
- Table of Contents (if applicable)
- Cross-references to the Master Bible
- Related Documents table
- Revision History

An AI agent must not create a document that links to an empty file. If the target document is empty, the agent must flag this before creating the link.

### AI Conflict Detection Rule

If an AI agent detects any of the following, it must stop and surface the issue before continuing:

- A request that contradicts an accepted decision in `DECISIONS.md`
- A request that violates the current phase gate
- A request that touches a deferred decision without project owner authorization
- Two documents that contradict each other
- A task that would require making a major change (per `PROJECT_RULES.md`)

### AI Commit Conventions

When an AI agent creates a commit (only when explicitly requested):

```
type(scope): description

[body explaining what and why]

Co-Authored-By: [AI Tool Name] <noreply@[provider].com>
```

The `Co-Authored-By` footer must always be included to maintain traceability.

---

## Forbidden Actions

These actions are prohibited for all contributors — human and AI — at all times:

| Action | Rule |
|--------|------|
| Force-pushing to `main` or `master` | Protected branch — irreversible history damage |
| Committing secrets, passwords, or credentials | Security — zero tolerance |
| Skipping git hooks (`--no-verify`) | Hooks enforce quality gates; skipping voids them |
| Amending commits pushed to a remote branch | Rewrites shared history |
| Creating artifacts outside the current phase gate | Phase gate integrity |
| Overriding the Master Bible without project owner approval | Governance hierarchy |
| Creating documentation that contradicts an accepted decision without flagging it | Decision integrity |
| Merging your own PR without a separate reviewer approval | Review integrity |

---

## Getting Help

| Situation | Where to Look |
|-----------|--------------|
| Understanding the project | `README.md` → `MASTER_PROJECT_BIBLE.md` |
| Current phase and status | `ROADMAP.md` → `PROJECT_INDEX.md` |
| Whether a decision has been made | `DECISIONS.md` |
| Documentation standards | `PROJECT_RULES.md` → this file |
| AI tool behaviour | `CLAUDE.md` (Claude Code) · `AGENTS.md` (all tools) |
| What documents exist | `PROJECT_INDEX.md` |
| Phase gate rules | `PROJECT_RULES.md` → [Phase Gate Rules] |
| Commit and PR examples | See [Commit Standards](#commit-standards) → [Pull Request Rules](#pull-request-rules) |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [PROJECT_RULES.md](PROJECT_RULES.md) | Full governance and standards |
| [AGENTS.md](AGENTS.md) | AI agent operating manual (all tools) |
| [CLAUDE.md](CLAUDE.md) | Claude Code specific operating manual |
| [DECISIONS.md](DECISIONS.md) | Architecture and governance decision log |
| [ROADMAP.md](ROADMAP.md) | Phase status and milestones |
| [PROJECT_INDEX.md](PROJECT_INDEX.md) | Repository navigation |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial release — covers documentation phase contribution rules; code review section pre-established for Phase 6 |

---

*All contributors — human and AI — are bound by this guide. When in doubt, ask the project owner before creating or modifying any artifact.*
