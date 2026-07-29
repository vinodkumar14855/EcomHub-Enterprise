# DECISIONS.md — Architecture & Governance Decision Log

> **Version:** 1.0
> **Status:** Active — Living Document
> **Last Updated:** July 2026
> **Document Owner:** Product Architecture
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md)
> **Classification:** Internal — Decision Registry

---

## Purpose

This document is the **authoritative decision log** for EcomHub Enterprise. It records every significant decision made across architecture, business, technology, UI/UX, and security domains — along with its rationale, consequences, and status.

Decisions are immutable once accepted. If a decision needs to change, a superseding decision must be created and the original marked **Superseded**. This ensures full audit traceability.

All AI agents and contributors must read this document before proposing or implementing changes that could conflict with accepted decisions.

---

## Table of Contents

1. [How to Use This Document](#how-to-use-this-document)
2. [Decision Status Definitions](#decision-status-definitions)
3. [Architecture Decisions](#architecture-decisions)
4. [Business Decisions](#business-decisions)
5. [Technology Decisions](#technology-decisions)
6. [UI/UX Decisions](#uiux-decisions)
7. [Security Decisions](#security-decisions)
8. [Deferred Decisions](#deferred-decisions)
9. [Decision Log Template](#decision-log-template)
10. [Related Documents](#related-documents)

---

## How to Use This Document

- **Before proposing a change:** Search this document to check if the decision has already been made.
- **Before implementing:** Confirm the decision status is **Accepted**, not **Deferred** or **Proposed**.
- **When adding a new decision:** Use the [Decision Log Template](#decision-log-template) and assign the next sequential ID in the appropriate category.
- **When a decision is reversed:** Do not delete or edit the original entry. Create a new superseding entry and update the original's status to **Superseded**, linking to the new entry.

---

## Decision Status Definitions

| Status | Meaning |
|--------|---------|
| **Accepted** | Decision has been made and approved by the project owner. It is authoritative and governs implementation. |
| **Proposed** | Decision has been suggested but not yet formally approved. Do not implement. |
| **Deferred** | Decision is acknowledged but intentionally postponed. Do not assume or implement. |
| **Superseded** | A newer decision replaces this one. Reference the superseding decision ID. |
| **Deprecated** | Decision is no longer applicable due to scope change or project evolution. |

---

## Architecture Decisions

### AD-001: Documentation-First, Phase-Gate Development Approach

| Field | Value |
|-------|-------|
| **ID** | AD-001 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Architecture Process |
| **Approved By** | Project Owner |

**Context:** EcomHub Enterprise spans five verticals, three portals, and multiple regulatory domains. Building without documented foundations risks scope creep, architectural inconsistency, and compliance gaps.

**Decision:** The project follows a documentation-first approach. No application code, database schemas, UI designs, or API implementations may be created until the documentation phase gate for that layer has been completed and approved. Phase gates must be passed sequentially.

**Consequences:**
- Positive: All stakeholders, engineers, and AI tools share a single authoritative reference before implementation begins.
- Positive: Reduces rework from undocumented assumptions.
- Negative: Longer time-to-code compared to code-first approaches.
- Negative: Requires discipline to enforce phase gate restrictions.

**Reference:** [PROJECT_RULES.md — Phase Gate Rules](PROJECT_RULES.md) · [docs/01_Project/Project_Roadmap.md](docs/01_Project/Project_Roadmap.md)

---

### AD-002: Multi-Vertical Monorepo Structure

| Field | Value |
|-------|-------|
| **ID** | AD-002 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Repository Structure |
| **Approved By** | Project Owner |

**Context:** EcomHub spans documentation, API specs, database artifacts, design systems, and future code. A single repository structure was needed to ensure coherent cross-referencing and AI-assisted workflow.

**Decision:** All project artifacts — documentation, API specs, database models, design assets, and future code — live in a single repository (`EcomHub-Enterprise`), organized by functional directory (`docs/`, `api/`, `database/`, `design-system/`, `assets/`, `prompts/`, `templates/`).

**Consequences:**
- Positive: Single source of truth; AI tools can traverse the full project context.
- Positive: Cross-referencing between docs, specs, and code is straightforward.
- Negative: Repository will grow large as code phases begin; may require tooling to manage build scope.

**Reference:** [MASTER_PROJECT_BIBLE.md — Repository Structure](MASTER_PROJECT_BIBLE.md)

---

### AD-003: Modular Vertical Architecture — Pluggable Domains

| Field | Value |
|-------|-------|
| **ID** | AD-003 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | System Architecture |
| **Approved By** | Project Owner |

**Context:** The platform must support five distinct commerce verticals (Marketplace, Services, Insurance, Travel, Digital) while sharing common infrastructure. Tight coupling would make it impossible to add or modify verticals independently.

**Decision:** Each vertical is architected as a **pluggable domain module** — owning its own business logic, data model, and API surface — while consuming shared platform services (Auth, Payments, Notifications, Search, CRM, CMS, Finance, RBAC, Audit). New verticals can be added without rebuilding the platform core.

**Consequences:**
- Positive: Verticals can be developed, scaled, and released independently.
- Positive: Platform core improvements benefit all verticals simultaneously.
- Negative: Higher initial design complexity for the shared services layer.
- Negative: Inter-module contracts must be rigorously defined during Phase 2 (Architecture).

**Reference:** [MASTER_PROJECT_BIBLE.md — Business Domains](MASTER_PROJECT_BIBLE.md) · [docs/01_Project/Project_Vision.md — Modular by Design](docs/01_Project/Project_Vision.md)

---

### AD-004: All Five Verticals Included in MVP

| Field | Value |
|-------|-------|
| **ID** | AD-004 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Scope |
| **Approved By** | Project Owner |

**Context:** An alternative approach would have been to launch with one or two verticals and expand. The project owner explicitly approved all five verticals for the MVP.

**Decision:** The MVP includes all five verticals — Marketplace Products, Professional Services, Insurance Marketplace, Travel & Hospitality, and Digital Services & Products. No vertical may be deferred to a post-MVP phase without a new approval decision.

**Consequences:**
- Positive: Full platform differentiation at launch; no phased vertical rollout needed.
- Positive: Marketing can lead with the complete "one platform for everything" proposition from day one.
- Negative: Higher build complexity; five vertical domains must be production-ready simultaneously.
- Negative: Vendor acquisition across all five verticals required before launch.

**Reference:** [docs/01_Project/Project_Scope.md — MVP Verticals](docs/01_Project/Project_Scope.md) · [MASTER_PROJECT_BIBLE.md — MVP Vertical Scope](MASTER_PROJECT_BIBLE.md)

---

### AD-005: India-First Launch with J&K / Srinagar Positioning

| Field | Value |
|-------|-------|
| **ID** | AD-005 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Market Strategy |
| **Approved By** | Project Owner |

**Context:** The platform must launch with a specific geographic identity rather than a generic national marketplace to achieve differentiation, brand identity, and authentic vendor supply.

**Decision:** Phase 1 launches as an **India-first platform with Jammu & Kashmir / Srinagar marketplace positioning** — showcasing regional specialties (Pashmina, saffron, dry fruits, honey, ghee, Kashmiri handicrafts) as the launch identity. Product delivery is pan-India. International expansion is Phase 3.

**Consequences:**
- Positive: Unique regional identity that no competitor currently owns.
- Positive: Strong authentic vendor supply from J&K artisan community.
- Positive: Kashmir tourism creates natural demand for travel vertical at launch.
- Negative: Requires targeted vendor acquisition in J&K before launch.
- Negative: Some customers may not associate Kashmir branding with all five verticals.

**Reference:** [docs/01_Project/Project_Vision.md — Regional Pride, National Scale](docs/01_Project/Project_Vision.md) · [MASTER_PROJECT_BIBLE.md — Geography & Market Strategy](MASTER_PROJECT_BIBLE.md)

---

## Business Decisions

### BD-001: Commission-Based Marketplace with Subscription and Advertising Revenue

| Field | Value |
|-------|-------|
| **ID** | BD-001 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Business Model |
| **Approved By** | Project Owner |

**Context:** The platform needed a sustainable revenue model that aligns platform incentives with vendor success and scales with transaction volume.

**Decision:** The primary revenue model is **platform commission on completed transactions**, deducted from vendor payouts (not added to customer price). Secondary revenue streams include optional vendor subscription tiers (Basic/Professional/Enterprise), advertising revenue (promoted listings, banners), and insurance referral fees per converted policy.

**Consequences:**
- Positive: Zero-cost entry for vendors removes onboarding friction.
- Positive: Platform revenue scales directly with vendor and transaction growth (aligned incentives).
- Negative: Revenue is delayed until transactions complete; no upfront revenue from vendor registration.
- Negative: Commission structure for five distinct verticals adds complexity to the finance module.

**Reference:** [docs/02_Business/Business_Model.md](docs/02_Business/Business_Model.md) · [docs/01_Project/Executive_Summary.md — Business Model](docs/01_Project/Executive_Summary.md)

---

### BD-002: Managed Multi-Vendor Marketplace — Vendor-Fulfilled, Platform-Governed

| Field | Value |
|-------|-------|
| **ID** | BD-002 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Business Model |
| **Approved By** | Project Owner |

**Context:** The platform needed to decide whether to hold inventory (first-party model) or operate purely as a marketplace (third-party model).

**Decision:** EcomHub operates as a **managed multi-vendor marketplace**. Vendors own their inventory, listings, and fulfillment. The platform governs vendor quality, processes payments, manages disputes, and settles payouts. The platform does not hold its own product inventory or employ delivery staff.

**Consequences:**
- Positive: Asset-light model; no inventory capital required.
- Positive: Scales to unlimited vendors without proportional cost increase.
- Negative: Customer experience depends on vendor fulfillment quality, which the platform does not directly control.
- Negative: Dispute and refund scenarios require clear policy frameworks enforced through the Admin Portal.

**Reference:** [docs/02_Business/Business_Model.md — Marketplace Model](docs/02_Business/Business_Model.md)

---

### BD-003: EcomHub Is an Insurance Aggregator, Not an Underwriter

| Field | Value |
|-------|-------|
| **ID** | BD-003 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Regulatory / Business |
| **Approved By** | Project Owner |

**Context:** Operating as an insurance underwriter requires an IRDAI underwriting license, significant capital reserves, and actuarial capability — none of which are in scope.

**Decision:** EcomHub's insurance vertical operates exclusively as an **insurance marketplace and aggregator**. All insurance products are provided by IRDAI-licensed partner insurers. The platform generates leads and earns referral fees. The platform explicitly displays its aggregator role and never represents itself as an insurer.

**Consequences:**
- Positive: No underwriting license required; significantly lower regulatory burden.
- Positive: Revenue model (referral fees) is straightforward and partner-funded.
- Negative: Margin is lower than underwriting; growth depends on partner insurer conversion rates.
- Negative: Policy claim outcomes are entirely outside platform control.

**Reference:** [docs/01_Project/Project_Scope.md — Vertical 3: Insurance](docs/01_Project/Project_Scope.md) · [docs/02_Business/Business_Requirements_Document.md — Insurance Rules](docs/02_Business/Business_Requirements_Document.md)

---

### BD-004: Mobile-First Responsive Web — No Native Apps in MVP

| Field | Value |
|-------|-------|
| **ID** | BD-004 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Product / Business |
| **Approved By** | Project Owner |

**Context:** Native iOS and Android apps require significant additional development effort, separate release cycles, App Store compliance, and maintenance overhead. India's commerce is mobile-first, but web-based experiences with responsive design can serve the mobile user base effectively at launch.

**Decision:** The MVP delivers a **mobile-first, fully responsive web application** for all portals (Customer, Vendor, Admin) and the storefront. Native iOS and Android apps are explicitly deferred to post-MVP. All UI must be designed mobile-first with desktop as a secondary consideration.

**Consequences:**
- Positive: Single codebase serves all devices; faster MVP delivery.
- Positive: No App Store review delays or Apple/Google policies at launch.
- Negative: Web apps cannot access full native device capabilities (push notifications require service workers, camera access is limited).
- Negative: Some vendor and customer segments may expect a native app experience.

**Reference:** [docs/01_Project/Project_Scope.md — Out of Scope](docs/01_Project/Project_Scope.md) · [docs/01_Project/Project_Vision.md — Mobile First](docs/01_Project/Project_Vision.md)

---

## Technology Decisions

### TD-001: Next.js and React for Frontend

| Field | Value |
|-------|-------|
| **ID** | TD-001 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Frontend Framework |
| **Approved By** | Project Owner |

**Context:** The storefront requires SEO optimization, fast page loads, and a mobile-first responsive design. Multiple portals require component reuse and a consistent design system.

**Decision:** **Next.js** (with React, TypeScript, Tailwind CSS, Shadcn UI) is the approved frontend framework for the storefront and all three portals. Next.js provides server-side rendering (SSR) for SEO, static generation for performance, and a full React ecosystem for component development.

**Consequences:**
- Positive: SSR and ISR directly support the SEO optimization requirement (PO-10).
- Positive: TypeScript provides type safety across a large multi-developer codebase.
- Positive: Tailwind CSS and Shadcn UI accelerate consistent UI development.
- Negative: SSR complexity increases server infrastructure requirements.

**Reference:** [README.md — Technology Stack](README.md) · [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md)

---

### TD-002: ASP.NET Core for Backend API

| Field | Value |
|-------|-------|
| **ID** | TD-002 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Backend Framework |
| **Approved By** | Project Owner |

**Context:** A high-performance, enterprise-grade backend is required to handle multi-vendor transactions, complex business logic across five verticals, and regulatory compliance requirements.

**Decision:** **ASP.NET Core** is the approved backend framework, exposing both **REST API** (for CRUD operations and external integrations) and **GraphQL** (for flexible frontend data fetching). The exact boundary between REST and GraphQL endpoints is a deferred decision to be resolved in Phase 4 (API Design).

**Consequences:**
- Positive: ASP.NET Core's performance and enterprise tooling align with the platform's governance requirements.
- Positive: Strong typing, dependency injection, and middleware pipeline suit the multi-module architecture.
- Negative: C# / .NET expertise required in the engineering team.

**Reference:** [README.md — Technology Stack](README.md) · [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md)

---

### TD-003: SQL Server as Primary Database

| Field | Value |
|-------|-------|
| **ID** | TD-003 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Database |
| **Approved By** | Project Owner |

**Context:** A relational database is required to handle transactional commerce data with ACID compliance — orders, payments, vendor settlements, audit logs, and multi-vertical product data with complex relationships.

**Decision:** **Microsoft SQL Server** is the approved primary database. The multi-tenancy strategy, schema design, and migration approach are deferred to Phase 3 (Data Design).

**Consequences:**
- Positive: ACID compliance for financial and transactional data.
- Positive: Strong tooling support in the Azure ecosystem.
- Negative: SQL Server licensing cost at scale.
- Negative: Less flexible for unstructured data (e.g., AI embeddings, search indexes) — may require supplementary stores in future phases.

**Reference:** [README.md — Technology Stack](README.md) · [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md)

---

### TD-004: Razorpay as Phase 1 Payment Gateway

| Field | Value |
|-------|-------|
| **ID** | TD-004 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Payments |
| **Approved By** | Project Owner |

**Context:** The platform launches India-first. A payment gateway with deep UPI, net banking, wallet, and card support — and strong developer tooling — is required. Stripe and PayPal lack UPI support and COD workflow management.

**Decision:** **Razorpay** is the exclusive payment gateway for Phase 1. Supported payment methods: UPI, credit/debit cards, net banking, wallets, and Cash on Delivery (COD) as a platform-managed workflow. Stripe (international cards) and PayPal are deferred to Phase 3 (International Expansion).

**Consequences:**
- Positive: UPI support covers 70%+ of India digital payments.
- Positive: Razorpay's vendor payout and route APIs align with multi-vendor settlement requirements.
- Negative: Single gateway creates a payment dependency risk; gateway outages affect all transactions.
- Negative: International customers cannot transact until Phase 3.

**Reference:** [MASTER_PROJECT_BIBLE.md — Payments Strategy](MASTER_PROJECT_BIBLE.md) · [docs/01_Project/Project_Scope.md — Payments Phase 1](docs/01_Project/Project_Scope.md)

---

### TD-005: JWT and OAuth with Social Login for Authentication

| Field | Value |
|-------|-------|
| **ID** | TD-005 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Authentication |
| **Approved By** | Project Owner |

**Context:** The platform requires authentication for three distinct portals (Customer, Vendor, Admin) with different permission levels. Customers expect social login options; vendors and admins require more secure session management.

**Decision:** Authentication uses **JWT (JSON Web Tokens)** for stateless session management, **OAuth 2.0** for authorization flows, and **social login** (Google, Facebook) for customer portal sign-in. The specific OAuth provider library, token refresh strategy, and MFA approach are deferred to Phase 2 (Architecture) and Phase 4 (API Design).

**Consequences:**
- Positive: Stateless JWT reduces server-side session overhead.
- Positive: Social login reduces customer registration friction.
- Negative: JWT token revocation requires a denylist or short expiry strategy (to be resolved in Phase 2).

**Reference:** [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md) · [docs/01_Project/Project_Scope.md — Platform Services](docs/01_Project/Project_Scope.md)

---

### TD-006: Azure and AWS as Cloud Providers (Hybrid Evaluation)

| Field | Value |
|-------|-------|
| **ID** | TD-006 |
| **Status** | ✅ Accepted (Provider Selection Deferred — see D-07) |
| **Date** | July 2026 |
| **Category** | Cloud Infrastructure |
| **Approved By** | Project Owner |

**Context:** Both Azure and AWS offer the services required for the platform. A final primary provider selection requires cost modelling, team expertise assessment, and Azure's alignment with the ASP.NET Core stack.

**Decision:** The platform will deploy to cloud infrastructure — either **Azure**, **AWS**, or a hybrid configuration. The specific primary provider is **Deferred Decision D-07**, to be resolved during Phase 2 (Architecture). The platform must be architected for cloud portability regardless of which provider is selected.

**Consequences:**
- Positive: Cloud-native deployment enables global scalability and managed service consumption.
- Negative: Provider selection deferred — infrastructure design cannot be fully finalized until D-07 is resolved.

**Reference:** [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md) · [Deferred Decision D-07](#d-07-cloud-primary-provider)

---

## UI/UX Decisions

### UD-001: Shadcn UI and Tailwind CSS as the Design System Foundation

| Field | Value |
|-------|-------|
| **ID** | UD-001 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Design System |
| **Approved By** | Project Owner |

**Context:** Three portals (Customer, Vendor, Admin) plus a public storefront require a consistent component library that is accessible, customizable, and compatible with Next.js.

**Decision:** **Shadcn UI** (component collection built on Radix UI primitives) with **Tailwind CSS** (utility-first CSS) forms the design system foundation. Custom EcomHub design tokens (colors, typography, spacing) will be applied over this base. The full design system specification is deferred to Phase 5 (UX & Design).

**Consequences:**
- Positive: Shadcn UI's copy-and-own model gives full control without dependency lock-in.
- Positive: Tailwind CSS's utility classes enable rapid, consistent styling across all portals.
- Negative: Design system customization work is required before engineering begins (Phase 5 gate).

**Reference:** [README.md — Technology Stack](README.md) · [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md)

---

### UD-002: WCAG 2.1 AA Accessibility Target

| Field | Value |
|-------|-------|
| **ID** | UD-002 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Accessibility |
| **Approved By** | Project Owner |

**Context:** Enterprise platforms serving a broad public audience must meet accessibility standards. India's disability population and global customer base both require accessible interfaces.

**Decision:** All customer-facing surfaces (storefront, customer portal) must target **WCAG 2.1 Level AA** compliance. Vendor and Admin portals should target AA where feasible. Implementation guidelines are defined during Phase 5 (UX & Design).

**Consequences:**
- Positive: Broader audience reach; reduced legal risk.
- Negative: Accessibility audit and remediation effort required during and after engineering.

**Reference:** [PROJECT_RULES.md — Quality Standards](PROJECT_RULES.md)

---

### UD-003: English and Hindi at Launch — Urdu/Kashmiri Deferred

| Field | Value |
|-------|-------|
| **ID** | UD-003 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Localization |
| **Approved By** | Project Owner |

**Context:** The platform launches in J&K / Srinagar. Urdu and Kashmiri are regional languages, but full localization doubles content and engineering effort. English and Hindi cover the national audience.

**Decision:** The MVP launches in **English and Hindi only**. Urdu and Kashmiri language support are deferred to Phase 2 (National Expansion). The architecture must support i18n from the start, but only two languages are loaded at MVP.

**Consequences:**
- Positive: Reduced content and engineering scope at launch.
- Negative: Local Kashmiri vendors and customers may find Hindi/English a barrier; a limited UX gap for the primary launch audience.

**Reference:** [docs/01_Project/Project_Scope.md — Geography & Payments](docs/01_Project/Project_Scope.md)

---

## Security Decisions

### SD-001: PCI-DSS Compliance via Razorpay Tokenization — No Card Data Stored

| Field | Value |
|-------|-------|
| **ID** | SD-001 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Payment Security |
| **Approved By** | Project Owner |

**Context:** Storing card data requires PCI-DSS Level 1 certification, significant security investment, and ongoing audit obligations. Tokenization via the payment gateway eliminates this requirement.

**Decision:** The EcomHub platform **never stores, processes, or transmits raw card data**. All card handling is performed exclusively through Razorpay's tokenization and vault. The platform stores only Razorpay payment tokens and order references.

**Consequences:**
- Positive: PCI-DSS compliance achieved through Razorpay's certified infrastructure, not platform-level certification.
- Positive: Card data breach risk eliminated at the platform level.
- Negative: Full payment flow depends on Razorpay uptime and API availability.

**Reference:** [docs/02_Business/Business_Requirements_Document.md — Payment Compliance](docs/02_Business/Business_Requirements_Document.md) · [PROJECT_RULES.md — Quality Standards](PROJECT_RULES.md)

---

### SD-002: RBAC Mandatory for All Admin and Vendor Operations

| Field | Value |
|-------|-------|
| **ID** | SD-002 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Access Control |
| **Approved By** | Project Owner |

**Context:** The Admin Portal is operated by multiple roles (Platform Admin, Finance Admin, Support Admin, Content Manager). Vendor Portal is accessed by multiple vendor types. Undifferentiated access creates data exposure risk and compliance violations.

**Decision:** **Role-Based Access Control (RBAC)** is mandatory from MVP for all Admin Portal and Vendor Portal operations. Each user type has a defined permission set. The RBAC model is configurable through the Admin Portal. No admin or vendor action occurs outside a defined role boundary. All permission changes are logged in the audit trail.

**Consequences:**
- Positive: Data exposure and unauthorized action risk contained at role boundaries.
- Positive: RBAC model supports regulatory compliance for financial and personal data access.
- Negative: RBAC model design complexity during Phase 2 (Architecture); role definitions must be exhaustive before engineering.

**Reference:** [docs/01_Project/Project_Scope.md — Platform Services](docs/01_Project/Project_Scope.md) · [MASTER_PROJECT_BIBLE.md — Admin Portal Modules](MASTER_PROJECT_BIBLE.md)

---

### SD-003: Audit Logging for All Admin and Financial Actions — 100% Coverage

| Field | Value |
|-------|-------|
| **ID** | SD-003 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Audit and Compliance |
| **Approved By** | Project Owner |

**Context:** Enterprise-grade platforms handling financial transactions, vendor payouts, and customer personal data require a tamper-evident record of all administrative and financial actions for regulatory compliance, dispute resolution, and fraud detection.

**Decision:** All admin actions, financial operations (settlements, refunds, payouts), vendor approvals/rejections, and permission changes must be recorded in an immutable audit log. The target is **100% audit coverage** of admin and financial actions (Success Metric SM-10). Audit log access is restricted by RBAC.

**Consequences:**
- Positive: Full audit trail supports DPDP Act, Consumer Protection Act, and GST compliance requirements.
- Positive: Reduces dispute resolution time — every action is traceable.
- Negative: Audit log storage grows continuously; a retention and archival policy is required (Phase 2).

**Reference:** [docs/01_Project/Success_Metrics.md — SM-10](docs/01_Project/Success_Metrics.md) · [docs/02_Business/Business_Requirements_Document.md — Business Rules BR-04](docs/02_Business/Business_Requirements_Document.md)

---

### SD-004: DPDP Act 2023 Compliance — Consent-First Data Handling

| Field | Value |
|-------|-------|
| **ID** | SD-004 |
| **Status** | ✅ Accepted |
| **Date** | July 2026 |
| **Category** | Data Privacy |
| **Approved By** | Project Owner |

**Context:** India's Digital Personal Data Protection Act 2023 (DPDP Act) mandates consent-based collection, the right to deletion, and data minimization for all personal data processing.

**Decision:** All personal data collection on the platform must be **consent-based**. The platform must implement the right to data deletion (account and personal data erasure on customer request), collect only data necessary for the stated purpose (data minimization), and share customer data with insurance or other partners only with explicit opt-in consent. Full DPDP compliance architecture is defined during Phase 2.

**Consequences:**
- Positive: Legal compliance with India's primary personal data law.
- Positive: Trust-building with privacy-aware customers.
- Negative: Consent management and deletion workflows add engineering complexity.
- Negative: Insurance lead data sharing flows must include explicit consent gating.

**Reference:** [docs/02_Business/Business_Requirements_Document.md — Compliance Requirements](docs/02_Business/Business_Requirements_Document.md)

---

## Deferred Decisions

These decisions are intentionally open. **No contributor or AI agent may assume, propose, or implement a solution for any deferred decision without explicit project owner authorization.** Each must be resolved before Phase 2 (Architecture) begins.

---

### D-01: Multi-Vendor Cart Split Strategy

| Field | Value |
|-------|-------|
| **ID** | D-01 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 2 — Architecture |
| **Category** | Checkout / Order Management |

**Context:** When a customer adds products from multiple vendors to a single cart, the platform must decide how to handle checkout and order creation.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — Single cart, split orders | Customer checks out once; platform creates one order per vendor automatically | Simpler customer UX; complex order splitting logic; payment split required |
| B — Vendor-specific carts | Cart is scoped per vendor; customer checks out with each vendor separately | Simpler backend; worse customer UX; friction for multi-vendor purchases |

**Impact:** Checkout flow design, order management schema, payment split architecture, vendor notification system.

**Reference:** [docs/01_Project/Project_Scope.md — Deferred Decisions](docs/01_Project/Project_Scope.md)

---

### D-02: Insurance Partner Integration Model

| Field | Value |
|-------|-------|
| **ID** | D-02 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 2 — Architecture |
| **Category** | Insurance Vertical |

**Context:** The insurance vertical requires connecting customers with partner insurers. The depth of integration determines the customer experience and engineering effort.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — API integration | Real-time quote comparison via partner insurer APIs | Best UX; requires partner API availability and integration effort |
| B — Manual lead handoff | Customer inquiry captured; lead sent to partner via email or CRM | Lower engineering effort; slower customer experience; no real-time quotes |

**Impact:** Insurance vertical architecture, quote comparison UX, partner onboarding process.

**Reference:** [docs/01_Project/Project_Scope.md — Deferred Decisions](docs/01_Project/Project_Scope.md)

---

### D-03: Travel Inventory Source

| Field | Value |
|-------|-------|
| **ID** | D-03 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 2 — Architecture |
| **Category** | Travel Vertical |

**Context:** Travel listings (hotels, houseboats, taxis, packages) require inventory and availability data. The source of this data determines architecture and vendor dependency.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — Vendor-managed | Each travel partner manages their own availability calendar on the platform | Simpler integration; accuracy depends on vendor discipline |
| B — GDS / OTA API | Connect to a Global Distribution System or OTA API for real-time inventory | Richer inventory; high integration cost; dependency on third-party GDS |

**Impact:** Travel listing architecture, availability management, booking calendar design.

**Reference:** [docs/01_Project/Project_Scope.md — Deferred Decisions](docs/01_Project/Project_Scope.md)

---

### D-04: Vendor Onboarding Model

| Field | Value |
|-------|-------|
| **ID** | D-04 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 1 — Business Detail |
| **Category** | Vendor Portal |

**Context:** Vendor onboarding requires a decision on how much of the process is automated versus admin-reviewed.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — Self-serve | Vendor registers, submits documents, and is automatically approved if criteria are met | Fast onboarding; risk of fraudulent or low-quality vendors |
| B — Approval-based with KYC | Vendor submits documents; admin manually reviews and approves before activation | Higher quality control; slower onboarding; admin workload |

**Impact:** Vendor portal workflow, admin portal approval module, vendor quality control.

**Reference:** [docs/01_Project/Project_Scope.md — Deferred Decisions](docs/01_Project/Project_Scope.md)

---

### D-05: Guest Checkout Policy

| Field | Value |
|-------|-------|
| **ID** | D-05 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 2 — Architecture |
| **Category** | Authentication / Checkout |

**Context:** Allowing guest checkout reduces purchase friction but limits the ability to track customers, send notifications, and manage returns and refunds effectively.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — Login required | All purchases require a registered account | Better customer data; reduced checkout abandonment concern |
| B — Guest checkout allowed | Purchase without registration; email collected at checkout | Reduced friction; lower customer data quality; complicates return/refund flows |

**Impact:** Auth flow, checkout design, order management, customer data model.

**Reference:** [docs/01_Project/Project_Scope.md — Deferred Decisions](docs/01_Project/Project_Scope.md)

---

### D-06: Commission Structure

| Field | Value |
|-------|-------|
| **ID** | D-06 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 1 — Business Detail (Revenue_Model.md) |
| **Category** | Finance / Revenue |

**Context:** Commission rates directly determine platform revenue and vendor profitability. Proposed rates exist in `Business_Model.md` but require formal approval before they become operative.

**Options Under Consideration:**

| Option | Description |
|--------|-------------|
| A — Flat rate per vertical | Fixed percentage per vertical (e.g., 10% Marketplace, 15% Services) |
| B — Category-specific rates | Different rates per product/service category within each vertical |
| C — Tiered by vendor subscription | Rate decreases as vendor moves to higher subscription tier |

**Proposed rates** (from `Business_Model.md`, status: Proposed — not yet approved):
- Marketplace Products: 8–15% (category-dependent)
- Professional Services: 10–20%
- Travel & Hospitality: 10–18%
- Digital Products: 15–25%
- Insurance: Referral fee model (not % commission)

**Impact:** Finance module, vendor payout calculation, Revenue_Model.md content.

**Reference:** [docs/02_Business/Business_Model.md — Commission Structure](docs/02_Business/Business_Model.md)

---

### D-07: Cloud Primary Provider

| Field | Value |
|-------|-------|
| **ID** | D-07 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 2 — Architecture |
| **Category** | Infrastructure |

**Context:** Both Azure and AWS are listed in the approved technology stack. A primary provider must be selected before infrastructure architecture can be finalized.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — Azure primary | Aligns with ASP.NET Core ecosystem; Azure App Service, SQL Azure, Application Insights | Strong .NET integration; Azure Application Insights for APM |
| B — AWS primary | Broader managed service catalog; EC2, RDS, CloudWatch | More DevOps tooling options; less native .NET alignment |
| C — Hybrid | Specific services on each cloud | Maximum flexibility; higher operational complexity |

**Impact:** Infrastructure architecture, cost modeling, DevOps tooling, monitoring strategy.

**Reference:** [MASTER_PROJECT_BIBLE.md — Technology Stack](MASTER_PROJECT_BIBLE.md)

---

### D-08: Wallet Scope

| Field | Value |
|-------|-------|
| **ID** | D-08 |
| **Status** | ⏳ Deferred |
| **Must Resolve By** | Phase 2 — Architecture |
| **Category** | Payments |

**Context:** The Customer Portal includes a wallet module. The scope of this wallet requires a decision that has implications for RBI regulatory compliance (stored value) and payment architecture.

**Options Under Consideration:**

| Option | Description | Trade-offs |
|--------|-------------|-----------|
| A — Platform wallet with stored balance | Customer can load funds into a platform wallet; use balance for purchases | Richer UX; requires RBI prepaid payment instrument (PPI) license or partnership |
| B — Payment-only (no stored balance) | Wallet stores refund credits only; no customer-loaded funds | Simpler regulatory posture; limited wallet utility |

**Impact:** Payment architecture, RBI compliance, customer portal wallet module design.

**Reference:** [docs/01_Project/Project_Scope.md — Deferred Decisions](docs/01_Project/Project_Scope.md)

---

## Decision Log Template

Use this template when adding new decisions to this document.

```markdown
### [Category Code]-[NNN]: [Decision Title]

| Field | Value |
|-------|-------|
| **ID** | [AD/BD/TD/UD/SD/D]-[NNN] |
| **Status** | [Accepted / Proposed / Deferred / Superseded / Deprecated] |
| **Date** | [Month Year] |
| **Category** | [Category name] |
| **Approved By** | [Project Owner / Tech Lead / Product Owner] |
| **Supersedes** | [Previous decision ID, if applicable] |

**Context:** [Why this decision was needed — the problem or question it answers.]

**Decision:** [What was decided, stated clearly and unambiguously.]

**Consequences:**
- Positive: [Benefit 1]
- Positive: [Benefit 2]
- Negative: [Trade-off 1]
- Negative: [Trade-off 2]

**Reference:** [Links to related documents]
```

### Category Code Reference

| Code | Category |
|------|----------|
| AD | Architecture Decision |
| BD | Business Decision |
| TD | Technology Decision |
| UD | UI/UX Decision |
| SD | Security Decision |
| D | Deferred Decision (open — use D-01 through D-08 for existing; D-09+ for new) |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](MASTER_PROJECT_BIBLE.md) | Single source of truth — all decisions must align |
| [PROJECT_RULES.md](PROJECT_RULES.md) | Change management process and major change definition |
| [docs/01_Project/Project_Scope.md](docs/01_Project/Project_Scope.md) | Original deferred decisions D-01 through D-08 |
| [docs/01_Project/Project_Roadmap.md](docs/01_Project/Project_Roadmap.md) | Phase gate at which each deferred decision must be resolved |
| [docs/02_Business/Business_Model.md](docs/02_Business/Business_Model.md) | Business model decisions detail |
| [ROADMAP.md](ROADMAP.md) | Current phase and upcoming milestones |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial release — 5 Architecture, 4 Business, 6 Technology, 3 UI/UX, 4 Security decisions recorded; 8 Deferred decisions migrated from Project_Scope.md |

---

*This is a living document. Every significant decision for EcomHub Enterprise must be recorded here before it governs implementation. All contributors — human and AI — must consult this document before proposing changes that touch accepted decisions.*
