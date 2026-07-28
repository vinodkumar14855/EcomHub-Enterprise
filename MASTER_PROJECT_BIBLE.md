# EcomHub Enterprise — Master Project Bible

> **Version:** 1.0  
> **Status:** Planning Phase  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Classification:** Internal — Single Source of Truth

---

## Purpose of This Document

This Master Project Bible is the **central reference** for EcomHub Enterprise. It consolidates vision, scope, domains, users, modules, technology direction, and documentation index into one authoritative document.

All project documentation must align with this bible. When conflicts arise, this document takes precedence until formally revised through the change process defined in [PROJECT_RULES.md](PROJECT_RULES.md).

---

## Table of Contents

1. [Executive Overview](#executive-overview)
2. [Project Identity](#project-identity)
3. [Strategic Vision](#strategic-vision)
4. [Business Domains](#business-domains)
5. [MVP Vertical Scope](#mvp-vertical-scope)
6. [User Types & Portals](#user-types--portals)
7. [Platform Modules](#platform-modules)
8. [Geography & Market Strategy](#geography--market-strategy)
9. [Payments Strategy](#payments-strategy)
10. [Technology Stack](#technology-stack)
11. [Repository Structure](#repository-structure)
12. [Documentation Index](#documentation-index)
13. [Glossary](#glossary)
14. [Related Documents](#related-documents)

---

## Executive Overview

EcomHub Enterprise is an **enterprise-grade, multi-vendor commerce platform** designed to unify physical products, professional services, insurance, travel and hospitality, and digital products within a single ecosystem.

Phase 1 launches as an **India-first marketplace** with strategic positioning in **Jammu & Kashmir / Srinagar**, showcasing regional specialties — Pashmina, dry fruits, saffron, handicrafts — alongside national and global commerce categories.

The platform is built to be **scalable, modular, AI-ready, and cloud-native**, supporting unlimited vendors, multiple business models, and future international expansion.

> See [docs/01_Project/Executive_Summary.md](docs/01_Project/Executive_Summary.md) for the full executive narrative.

---

## Project Identity

| Attribute | Value |
|-----------|-------|
| **Project Name** | EcomHub Enterprise |
| **Version** | 1.0 |
| **Phase** | Planning |
| **License** | MIT |
| **Primary Geography (Phase 1)** | India — Jammu & Kashmir / Srinagar |
| **MVP Verticals** | All five (Marketplace, Services, Insurance, Travel, Digital) |
| **Documentation Home** | `/docs` directory |

---

## Strategic Vision

EcomHub Enterprise exists to become the **definitive unified commerce hub** — where customers discover, compare, purchase, book, and manage every type of commercial transaction through one trusted platform.

### Vision Statement

> To build a modern enterprise commerce platform that empowers regional artisans and national vendors, connects customers to essential services, and delivers travel, insurance, and digital experiences — all from a single, intelligent, mobile-first ecosystem.

### Guiding Principles

1. **Unified Experience** — One account, one cart philosophy where feasible; consistent UX across all verticals.
2. **Vendor Empowerment** — Self-service tools for onboarding, catalog management, fulfillment, and payouts.
3. **Regional Pride, National Scale** — Launch with J&K identity; architect for pan-India and global expansion.
4. **Enterprise Grade** — RBAC, audit logs, CRM, finance, and compliance built in from the start.
5. **AI-Ready Architecture** — Search, recommendations, and operational intelligence as first-class capabilities.
6. **Modular by Design** — Verticals are pluggable domains sharing common platform services.

> See [docs/01_Project/Project_Vision.md](docs/01_Project/Project_Vision.md) for the complete vision document.

---

## Business Domains

EcomHub Enterprise operates across **five product verticals** and **three operational layers**, supported by **shared platform services**.

### Product Verticals

| # | Domain | Description |
|---|--------|-------------|
| 1 | **Marketplace Products** | Physical consumer goods — regional specialties and general merchandise |
| 2 | **Professional Services** | CA, tax, legal, accounting, and business consultancy services |
| 3 | **Insurance Marketplace** | Health, motor, life, and travel insurance aggregation |
| 4 | **Travel & Hospitality** | Houseboats, hotels, taxis, packages, tours, and local experiences |
| 5 | **Digital Services & Products** | Online services, downloads, memberships, and future SaaS |

### Operational Layers

| Layer | Description |
|-------|-------------|
| **Customer Portal** | End-user account, orders, bookings, wallet, and notifications |
| **Vendor Portal** | Seller operations — catalog, inventory, orders, analytics, payments |
| **Admin Portal** | Platform governance — CMS, CRM, finance, marketing, RBAC, audit |

### Shared Platform Services (Cross-Cutting)

- Identity & Authentication (JWT, OAuth, Social Login)
- Payments & Settlements
- Notifications (email, SMS, push, in-app)
- Search & AI Recommendations
- CMS & SEO
- CRM & Support
- Marketing & Promotions
- Finance & Reporting
- RBAC & Audit Logging
- Multi-vendor Order Management

---

## MVP Vertical Scope

All five verticals are included in the MVP. Detailed scope is defined in [docs/01_Project/Project_Scope.md](docs/01_Project/Project_Scope.md).

### 1. Marketplace Products

| Category | Products |
|----------|----------|
| Regional Specialties | Pashmina, dry fruits, honey, ghee, saffron, Kashmiri handicrafts |
| General Merchandise | Organic products, general consumer products |

**Core capabilities:** Products, categories, brands, reviews, wishlist, cart, checkout.

### 2. Professional Services

| Service Type |
|--------------|
| CA Services |
| GST Filing |
| ITR Filing |
| Accounting Services |
| Legal Services |
| Business Consultancy |

**Core capabilities:** Service listings, inquiry/booking, provider matching, order tracking.

### 3. Insurance Marketplace

| Insurance Type |
|----------------|
| Health Insurance |
| Car Insurance |
| Bike Insurance |
| Life Insurance |
| Travel Insurance |

**Core capabilities:** Quote comparison, policy inquiry, partner insurer integration, policy document management.

### 4. Travel & Hospitality

| Offering |
|----------|
| Houseboat Booking |
| Hotel Booking |
| Taxi Booking |
| Holiday Packages |
| Tour Activities |
| Local Experiences |

**Core capabilities:** Search, availability, booking, itinerary management, vendor fulfillment.

### 5. Digital Services & Products

| Offering |
|----------|
| Online services |
| Digital downloads |
| Memberships |
| Future SaaS offerings |

**Core capabilities:** Digital delivery, entitlement management, subscription billing, access control.

---

## User Types & Portals

| User Type | Portal | Primary Responsibilities |
|-----------|--------|--------------------------|
| **Customer** | Customer Portal + Storefront | Browse, purchase, book, manage account |
| **Vendor / Seller** | Vendor Portal | Manage catalog, fulfill orders, view analytics, receive payouts |
| **Platform Admin** | Admin Portal | Operate platform, manage vendors, CMS, CRM, finance, marketing |
| **Support Agent** | Admin Portal (CRM module) | Handle tickets, refunds, disputes |
| **Finance Operator** | Admin Portal (Finance module) | Settlements, reconciliation, reporting |
| **Content Manager** | Admin Portal (CMS module) | Pages, SEO content, campaigns |
| **Guest** | Storefront (limited) | Browse catalog, add to cart (login required at checkout) |

> See [docs/01_Project/Target_Audience.md](docs/01_Project/Target_Audience.md) for personas and journey context.

---

## Platform Modules

### Customer Portal Modules

- Dashboard
- Orders (products, services, insurance, travel, digital)
- Bookings
- Wishlist
- Addresses
- Wallet
- Notifications

### Vendor Portal Modules

- Dashboard
- Products / Service Listings
- Orders & Bookings
- Inventory
- Analytics
- Payments & Payouts

### Admin Portal Modules

- Dashboard
- CMS (Content Management)
- CRM (Customer Relationship Management)
- Reports & Analytics
- Finance & Settlements
- Marketing & Promotions
- RBAC (Role-Based Access Control)
- Audit Logs

### Shared Commerce Modules

- Product Catalog & Taxonomy
- Cart & Checkout
- Order Management
- Reviews & Ratings
- Search & Discovery
- Payment Processing
- Notification Engine

---

## Geography & Market Strategy

### Phase 1 — India Focus

- **Launch Region:** Jammu & Kashmir / Srinagar marketplace positioning
- **Market Identity:** Showcase Kashmiri heritage products alongside national categories
- **Regulatory Context:** Indian tax (GST), payment (RBI/UPI), insurance (IRDAI), and consumer protection frameworks
- **Language:** English and Hindi at launch; Urdu/Kashmiri considered for regional UX

### Future Expansion

| Phase | Scope |
|-------|-------|
| Phase 2 | Multiple Indian cities — pan-India vendor and customer base |
| Phase 3 | International marketplace — multi-currency, cross-border payments, localization |

---

## Payments Strategy

### Phase 1 — India First

| Method | Provider / Mechanism |
|--------|---------------------|
| UPI | Razorpay |
| Credit / Debit Cards | Razorpay |
| Net Banking | Razorpay |
| Wallets | Razorpay |
| Cash on Delivery (COD) | Platform-managed |

**Primary payment gateway:** Razorpay

### Future — International

| Method | Provider |
|--------|----------|
| International cards | Stripe |
| Global payments | PayPal |
| Additional local methods | Region-specific gateways |

> Payment architecture decisions require formal approval before implementation. See [PROJECT_RULES.md](PROJECT_RULES.md).

---

## Technology Stack

As defined in [README.md](README.md). Technology choices are **directional** during the planning phase. Architectural changes require approval.

| Layer | Technology |
|-------|------------|
| **Frontend** | Next.js, React, TypeScript, Tailwind CSS, Shadcn UI |
| **Backend** | ASP.NET Core, REST API, GraphQL |
| **Database** | SQL Server |
| **Authentication** | JWT, OAuth, Social Login |
| **Payments (Phase 1)** | Razorpay, COD |
| **Payments (Future)** | Stripe, PayPal |
| **Cloud** | Azure, AWS |

### AI Workflow Tools

This repository is designed to work with:

- NotebookLM
- Cursor
- Claude Code
- GitHub Copilot
- Figma AI

---

## Repository Structure

```
EcomHub-Enterprise/
├── README.md                    # Project overview and quick reference
├── MASTER_PROJECT_BIBLE.md      # This document — single source of truth
├── PROJECT_RULES.md             # Documentation and development rules
├── TASKS.md                     # Living task backlog
├── AI_MASTER_PROMPT.md          # AI assistant context bundle
├── mkdocs.yml                   # Documentation site configuration
├── docs/                        # All project documentation
│   └── 01_Project/              # Phase 0 — business foundation
├── api/                         # API specifications (future)
├── database/                    # Database artifacts (future)
├── assets/                      # Static assets
├── design-system/               # Design system (future)
├── prompts/                     # AI prompt templates
└── templates/                   # Document templates
```

---

## Documentation Index

### Phase 0 — Business Foundation (Current)

| Document | Location | Purpose |
|----------|----------|---------|
| Master Project Bible | `MASTER_PROJECT_BIBLE.md` | Single source of truth |
| Project Rules | `PROJECT_RULES.md` | Standards and governance |
| Project Vision | `docs/01_Project/Project_Vision.md` | Long-term vision and principles |
| Executive Summary | `docs/01_Project/Executive_Summary.md` | Stakeholder overview |
| Business Goals | `docs/01_Project/Business_Goals.md` | Strategic business objectives |
| Project Scope | `docs/01_Project/Project_Scope.md` | MVP boundaries and inclusions |
| Target Audience | `docs/01_Project/Target_Audience.md` | Personas and user segments |
| Project Objectives | `docs/01_Project/Project_Objectives.md` | Measurable project objectives |
| Success Metrics | `docs/01_Project/Success_Metrics.md` | KPIs and success criteria |
| Project Roadmap | `docs/01_Project/Project_Roadmap.md` | Phased delivery timeline |

### Future Documentation Phases

| Phase | Directory | Focus |
|-------|-----------|-------|
| Phase 1 | `docs/02_Business/` | Domain PRDs, personas, compliance |
| Phase 2 | `docs/03_Architecture/` | System design, ADRs, cloud |
| Phase 3 | `docs/04_Data/` | Data models, migrations |
| Phase 4 | `docs/05_API/` | REST/GraphQL specifications |
| Phase 5 | `docs/06_Design/` | UX, design system, wireframes |
| Phase 6 | `docs/07_Engineering/` | Implementation standards, CI/CD |
| Phase 7 | `docs/08_Operations/` | Runbooks, SLAs, monitoring |
| Phase 8 | `docs/09_Delivery/` | Release management, risk register |

---

## Glossary

| Term | Definition |
|------|------------|
| **Vertical** | A distinct business domain (e.g., Marketplace, Insurance) |
| **Vendor** | A third-party seller or service provider on the platform |
| **Portal** | A dedicated web application surface for a user type |
| **MVP** | Minimum Viable Product — first releasable version with all five verticals |
| **RBAC** | Role-Based Access Control — permission system for admin and vendor users |
| **COD** | Cash on Delivery — payment upon physical delivery |
| **UPI** | Unified Payments Interface — India instant payment system |
| **CRM** | Customer Relationship Management |
| **CMS** | Content Management System |
| **ADR** | Architecture Decision Record |
| **PRD** | Product Requirements Document |
| **GDS** | Global Distribution System (travel industry) |
| **IRDAI** | Insurance Regulatory and Development Authority of India |

---

## Related Documents

| Document | Relationship |
|----------|--------------|
| [README.md](README.md) | Public-facing project overview |
| [PROJECT_RULES.md](PROJECT_RULES.md) | Governance and standards |
| [docs/01_Project/Project_Vision.md](docs/01_Project/Project_Vision.md) | Detailed vision |
| [docs/01_Project/Executive_Summary.md](docs/01_Project/Executive_Summary.md) | Stakeholder summary |
| [docs/01_Project/Business_Goals.md](docs/01_Project/Business_Goals.md) | Business objectives |
| [docs/01_Project/Project_Scope.md](docs/01_Project/Project_Scope.md) | Scope boundaries |
| [docs/01_Project/Target_Audience.md](docs/01_Project/Target_Audience.md) | User personas |
| [docs/01_Project/Project_Objectives.md](docs/01_Project/Project_Objectives.md) | Project objectives |
| [docs/01_Project/Success_Metrics.md](docs/01_Project/Success_Metrics.md) | KPIs |
| [docs/01_Project/Project_Roadmap.md](docs/01_Project/Project_Roadmap.md) | Delivery timeline |

---

## Document Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 0 release |

---

*This document is maintained by the Product Architecture team. All changes must follow the process defined in [PROJECT_RULES.md](PROJECT_RULES.md).*
