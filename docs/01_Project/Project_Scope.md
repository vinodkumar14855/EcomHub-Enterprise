# Project Scope

> **Version:** 1.0  
> **Status:** Draft  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines the **boundaries of the EcomHub Enterprise MVP** — what is included, what is excluded, and what is deferred to future phases. All implementation work must align with this scope document.

Scope changes require approval per [PROJECT_RULES.md](../../PROJECT_RULES.md#change-management).

---

## Table of Contents

1. [Scope Overview](#scope-overview)
2. [In Scope — MVP Verticals](#in-scope--mvp-verticals)
3. [In Scope — Portals](#in-scope--portals)
4. [In Scope — Platform Services](#in-scope--platform-services)
5. [In Scope — Geography & Payments](#in-scope--geography--payments)
6. [Out of Scope — MVP](#out-of-scope--mvp)
7. [Deferred Decisions](#deferred-decisions)
8. [Assumptions & Constraints](#assumptions--constraints)
9. [Related Documents](#related-documents)

---

## Scope Overview

The EcomHub Enterprise MVP includes **all five commerce verticals**, **three user portals**, and **shared platform services**, launching as an **India-first platform** with **J&K / Srinagar marketplace positioning**.

| Dimension | MVP Scope |
|-----------|-----------|
| Verticals | All five (Marketplace, Services, Insurance, Travel, Digital) |
| Portals | Customer, Vendor, Admin |
| Geography | India — J&K / Srinagar launch positioning |
| Payments | Razorpay, UPI, cards, net banking, wallets, COD |
| Platform | Auth, RBAC, audit, CRM, CMS, finance, marketing, notifications |

---

## In Scope — MVP Verticals

### Vertical 1: Marketplace Products

**Status:** ✅ In Scope — MVP

| Category | Products / Sub-Categories |
|----------|----------------------------|
| **Kashmiri Specialties** | Pashmina, dry fruits, honey, ghee, saffron, Kashmiri handicrafts |
| **Organic Products** | Organic food, organic personal care, organic home products |
| **General Consumer Products** | National and international consumer goods |

**Capabilities:**

| Feature | Included |
|---------|----------|
| Product catalog with categories and sub-categories | ✅ |
| Brand management | ✅ |
| Product variants (size, weight, color) | ✅ |
| Product images and descriptions | ✅ |
| Customer reviews and ratings | ✅ |
| Wishlist | ✅ |
| Shopping cart | ✅ |
| Checkout with address management | ✅ |
| Order tracking | ✅ |
| COD and online payment | ✅ |
| Vendor product management | ✅ |
| Inventory tracking | ✅ |

---

### Vertical 2: Professional Services

**Status:** ✅ In Scope — MVP

| Service | Description |
|---------|-------------|
| CA Services | Chartered accountant consultations and services |
| GST Filing | Goods and Services Tax filing and compliance |
| ITR Filing | Income Tax Return filing |
| Accounting Services | Bookkeeping, financial statements, accounting |
| Legal Services | Legal consultation, documentation, compliance |
| Business Consultancy | Business advisory, strategy, startup guidance |

**Capabilities:**

| Feature | Included |
|---------|----------|
| Service listing and categorization | ✅ |
| Service provider profiles | ✅ |
| Inquiry and booking request | ✅ |
| Service order tracking | ✅ |
| Customer reviews | ✅ |
| Provider management (vendor portal) | ✅ |
| Document upload/sharing (basic) | ✅ |

---

### Vertical 3: Insurance Marketplace

**Status:** ✅ In Scope — MVP

| Insurance Type | Description |
|----------------|-------------|
| Health Insurance | Individual and family health plans |
| Car Insurance | Four-wheeler motor insurance |
| Bike Insurance | Two-wheeler motor insurance |
| Life Insurance | Term and life coverage plans |
| Travel Insurance | Domestic and international travel coverage |

**Capabilities:**

| Feature | Included |
|---------|----------|
| Insurance product listing | ✅ |
| Quote comparison (basic) | ✅ |
| Inquiry and lead capture | ✅ |
| Partner insurer integration (API or manual) | ✅ |
| Policy document storage (customer portal) | ✅ |
| Insurance category browsing | ✅ |

> EcomHub is an **insurance marketplace/aggregator**, not an underwriter. All insurance products are provided by IRDAI-licensed partners.

---

### Vertical 4: Travel & Hospitality

**Status:** ✅ In Scope — MVP

| Offering | Description |
|----------|-------------|
| Houseboat Booking | Kashmir houseboat reservations |
| Hotel Booking | Hotel search and reservation |
| Taxi Booking | Local taxi and cab booking |
| Holiday Packages | Curated travel packages |
| Tour Activities | Guided tours and activities |
| Local Experiences | Cultural and experiential offerings |

**Capabilities:**

| Feature | Included |
|---------|----------|
| Listing search and filtering | ✅ |
| Availability display | ✅ |
| Booking request and confirmation | ✅ |
| Booking management (customer portal) | ✅ |
| Vendor listing management | ✅ |
| Booking calendar (basic) | ✅ |
| Customer reviews | ✅ |

---

### Vertical 5: Digital Services & Products

**Status:** ✅ In Scope — MVP

| Offering | Description |
|----------|-------------|
| Online Services | Remote-deliverable professional services |
| Digital Downloads | E-books, templates, media files |
| Memberships | Subscription-based access programs |
| Future SaaS Offerings | Placeholder category for future software products |

**Capabilities:**

| Feature | Included |
|---------|----------|
| Digital product listing | ✅ |
| Instant delivery / download | ✅ |
| Membership subscription management | ✅ |
| Access entitlement control | ✅ |
| SaaS category placeholder | ✅ (listing only, no SaaS engine in MVP) |

---

## In Scope — Portals

### Customer Portal

**Status:** ✅ In Scope — MVP

| Module | Features |
|--------|----------|
| Dashboard | Order summary, recent activity, quick actions |
| Orders | Product orders, service orders, booking history |
| Bookings | Travel and hospitality booking management |
| Wishlist | Saved products and services |
| Addresses | Shipping and billing address management |
| Wallet | Platform wallet balance, transaction history |
| Notifications | Order updates, booking confirmations, promotions |

### Vendor Portal

**Status:** ✅ In Scope — MVP

| Module | Features |
|--------|----------|
| Dashboard | Sales summary, pending orders, alerts |
| Products / Listings | Catalog management across applicable verticals |
| Orders & Bookings | Order fulfillment, booking management |
| Inventory | Stock levels, low-stock alerts |
| Analytics | Sales trends, top products, revenue summary |
| Payments | Payout history, pending settlements |

### Admin Portal

**Status:** ✅ In Scope — MVP

| Module | Features |
|--------|----------|
| Dashboard | Platform KPIs, vendor activity, revenue overview |
| CMS | Page management, banners, SEO content |
| CRM | Customer records, support tickets, communication |
| Reports | Sales, vendor, vertical, and financial reports |
| Finance | Revenue tracking, vendor settlements, reconciliation |
| Marketing | Promotions, coupons, campaigns |
| RBAC | Role and permission management |
| Audit Logs | Action tracking for admin and system events |

---

## In Scope — Platform Services

| Service | MVP Scope |
|---------|-----------|
| **Authentication** | JWT, OAuth, social login (Google, Facebook) |
| **Authorization** | RBAC for admin and vendor users |
| **Payments** | Razorpay integration, COD workflow |
| **Notifications** | Email, SMS, in-app notifications |
| **Search** | Full-text search across verticals |
| **Reviews** | Product, service, travel review system |
| **Media Management** | Image upload and storage for products/listings |
| **Audit Logging** | Admin action audit trail |
| **SEO** | Meta tags, structured data, sitemap |

---

## In Scope — Geography & Payments

### Geography — Phase 1

| Aspect | Scope |
|--------|-------|
| Launch positioning | Jammu & Kashmir / Srinagar |
| Product delivery | Pan-India shipping |
| Service providers | India-based professionals |
| Insurance | India IRDAI-regulated products |
| Travel | J&K primary; pan-India packages |
| Languages | English, Hindi |

### Payments — Phase 1

| Method | Provider |
|--------|----------|
| UPI | Razorpay |
| Credit / Debit Cards | Razorpay |
| Net Banking | Razorpay |
| Wallets | Razorpay |
| Cash on Delivery | Platform-managed |

---

## Out of Scope — MVP

The following are explicitly **excluded** from the MVP:

| Item | Reason | Future Phase |
|------|--------|--------------|
| International payments (Stripe, PayPal) | India-first launch | Phase 3 |
| Native mobile apps (iOS, Android) | Responsive web first | Post-MVP |
| Multi-currency support | India-only at launch | Phase 3 |
| Full SaaS product engine | Placeholder category only | Phase 2+ |
| AI-powered recommendations (live) | Architecture-ready; implementation deferred | Post-MVP |
| Blockchain / cryptocurrency payments | Not aligned with business model | Not planned |
| Physical POS integration | Online-first platform | Not planned |
| White-label multi-tenant SaaS | Platform operator model only | Year 3+ |
| Logistics / last-mile delivery ownership | Integrate with third-party providers | Post-MVP |
| Live chat / chatbot support | CRM ticket system first | Post-MVP |
| Advanced analytics / BI dashboards | Basic analytics in MVP | Phase 2 |
| Multi-language beyond English/Hindi | Urdu/Kashmiri considered | Phase 2 |
| Vendor mobile app | Responsive vendor portal first | Post-MVP |
| Home services (plumbing, cleaning, etc.) | Removed from MVP services scope | Future consideration |

---

## Deferred Decisions

The following decisions are **acknowledged but not yet finalized**. They must be resolved before Phase 2 (Architecture):

| # | Decision | Options | Impact |
|---|----------|---------|--------|
| D-01 | Multi-vendor cart strategy | Single cart with split orders vs. vendor-specific carts | Checkout architecture |
| D-02 | Insurance integration model | API integration vs. manual lead handoff | Insurance vertical depth |
| D-03 | Travel inventory source | Vendor-managed vs. GDS/OTA API | Travel vertical architecture |
| D-04 | Vendor onboarding | Self-serve vs. approval-based with KYC | Vendor portal workflow |
| D-05 | Guest checkout | Allow guest checkout vs. login required | Auth flow |
| D-06 | Commission structure | Flat rate vs. vertical-specific vs. tiered | Finance module |
| D-07 | Cloud primary provider | Azure vs. AWS vs. hybrid | Infrastructure |
| D-08 | Wallet scope | Platform wallet vs. payment-only (no stored balance) | Payment architecture |

> AI assistants and contributors must **ask before making major architectural changes** related to these decisions. See [PROJECT_RULES.md](../../PROJECT_RULES.md).

---

## Assumptions & Constraints

### Assumptions

1. Vendors can fulfill pan-India shipping for physical products at launch.
2. Insurance partners will provide API or structured lead integration.
3. Travel vendors will manage their own inventory and availability.
4. Razorpay supports all required India payment methods.
5. Target users have smartphone access with reliable internet connectivity.

### Constraints

1. MVP must include all five verticals (per project owner approval).
2. Phase 1 is India-only for payments and regulatory compliance.
3. No application code until Phase 0 and Phase 1 documentation is approved.
4. Technology stack as defined in [README.md](../../README.md) unless formally changed.

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [Business_Goals.md](Business_Goals.md) | Why we build each vertical |
| [Project_Objectives.md](Project_Objectives.md) | How we build the platform |
| [Target_Audience.md](Target_Audience.md) | Who uses each vertical |
| [Project_Roadmap.md](Project_Roadmap.md) | When each scope item is delivered |
| [PROJECT_RULES.md](../../PROJECT_RULES.md) | Scope change process |
| [README.md](../../README.md) | Module overview |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 0 release |
