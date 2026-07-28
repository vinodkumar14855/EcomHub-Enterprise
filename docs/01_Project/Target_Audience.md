# Target Audience

> **Version:** 1.0  
> **Status:** Draft  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines the **target audience segments, user types, and personas** for EcomHub Enterprise. Understanding our users drives portal design, vertical prioritization, and go-to-market strategy.

User types and portal mapping are defined in [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md#user-types--portals).

---

## Table of Contents

1. [Audience Overview](#audience-overview)
2. [Primary User Types](#primary-user-types)
3. [Customer Personas](#customer-personas)
4. [Vendor Personas](#vendor-personas)
5. [Admin & Operations Personas](#admin--operations-personas)
6. [Audience by Vertical](#audience-by-vertical)
7. [Geographic Segmentation](#geographic-segmentation)
8. [Related Documents](#related-documents)

---

## Audience Overview

EcomHub Enterprise serves **three primary user groups** across **five commerce verticals** in the **India market**, launching with **J&K / Srinagar positioning**.

```
                    ┌─────────────────────┐
                    │  EcomHub Enterprise │
                    └─────────┬───────────┘
          ┌───────────────────┼───────────────────┐
          ▼                   ▼                   ▼
    ┌───────────┐       ┌───────────┐       ┌───────────┐
    │ Customers │       │  Vendors  │       │   Admins  │
    │ (Buyers)  │       │ (Sellers) │       │(Operators)│
    └─────┬─────┘       └─────┬─────┘       └─────┬─────┘
          │                   │                   │
    5 Verticals          5 Verticals         Platform Ops
```

---

## Primary User Types

| User Type | Portal | Description |
|-----------|--------|-------------|
| **Customer** | Customer Portal + Storefront | Individuals and businesses who browse, purchase, book, and manage accounts |
| **Vendor** | Vendor Portal | Sellers, service providers, and operators who list, fulfill, and manage business on the platform |
| **Platform Admin** | Admin Portal | Internal team managing platform operations, content, finance, and governance |
| **Support Agent** | Admin Portal (CRM) | Handles customer support tickets, refunds, and disputes |
| **Finance Operator** | Admin Portal (Finance) | Manages settlements, reconciliation, and financial reporting |
| **Content Manager** | Admin Portal (CMS) | Manages pages, banners, SEO content, and marketing assets |
| **Guest** | Storefront (limited) | Unauthenticated visitor browsing the catalog |

---

## Customer Personas

### Persona C1: The Regional Shopper — "Aisha"

| Attribute | Detail |
|-----------|--------|
| **Age** | 28–45 |
| **Location** | Metro cities (Delhi, Mumbai, Bangalore) |
| **Goal** | Purchase authentic Kashmiri products (Pashmina, saffron, dry fruits) |
| **Behavior** | Mobile-first; researches products via search and reviews; price-conscious but values authenticity |
| **Pain Points** | Cannot verify product authenticity online; limited trusted sources for regional products |
| **Verticals Used** | Marketplace Products |
| **Payment Preference** | UPI, COD |

### Persona C2: The SMB Owner — "Rajesh"

| Attribute | Detail |
|-----------|--------|
| **Age** | 30–50 |
| **Location** | Tier 1 and Tier 2 cities across India |
| **Goal** | Find reliable CA, GST filing, and legal services for his business |
| **Behavior** | Compares service providers; reads reviews; prefers bundled services |
| **Pain Points** | Fragmented service discovery; difficulty comparing pricing and credentials |
| **Verticals Used** | Professional Services |
| **Payment Preference** | UPI, net banking, cards |

### Persona C3: The Insurance Buyer — "Priya"

| Attribute | Detail |
|-----------|--------|
| **Age** | 25–40 |
| **Location** | Pan-India |
| **Goal** | Compare and purchase health or motor insurance at competitive rates |
| **Behavior** | Researches online; compares quotes; values clear policy details |
| **Pain Points** | Too many insurer websites; confusing policy terms; distrust of agents |
| **Verticals Used** | Insurance Marketplace |
| **Payment Preference** | UPI, cards |

### Persona C4: The Travel Explorer — "Arjun"

| Attribute | Detail |
|-----------|--------|
| **Age** | 25–35 |
| **Location** | Pan-India; planning Kashmir trip |
| **Goal** | Book houseboat, hotel, taxi, and local experiences for Kashmir vacation |
| **Behavior** | Plans trips via mobile; reads reviews; books activities in advance |
| **Pain Points** | Must use multiple apps/sites for houseboat, hotel, taxi, and activities |
| **Verticals Used** | Travel & Hospitality |
| **Payment Preference** | UPI, cards |

### Persona C5: The Digital Consumer — "Neha"

| Attribute | Detail |
|-----------|--------|
| **Age** | 22–35 |
| **Location** | Urban India |
| **Goal** | Access online services, download digital products, subscribe to memberships |
| **Behavior** | Comfortable with digital payments; expects instant delivery |
| **Pain Points** | Scattered digital product sources; no unified account |
| **Verticals Used** | Digital Services & Products |
| **Payment Preference** | UPI, wallets |

### Persona C6: The Local Kashmiri Buyer — "Faisal"

| Attribute | Detail |
|-----------|--------|
| **Age** | 20–50 |
| **Location** | Jammu & Kashmir / Srinagar |
| **Goal** | Buy local and national products; book local services and travel; access insurance |
| **Behavior** | Mobile-first; UPI-native; values local vendor relationships |
| **Pain Points** | Limited e-commerce options tailored to Kashmir; delivery constraints |
| **Verticals Used** | All verticals |
| **Payment Preference** | UPI, COD |

---

## Vendor Personas

### Persona V1: The Kashmiri Artisan — "Gulzar"

| Attribute | Detail |
|-----------|--------|
| **Business** | Pashmina and handicraft producer |
| **Location** | Srinagar, J&K |
| **Goal** | Sell authentic handmade products to national and international buyers |
| **Behavior** | Limited tech proficiency; needs simple listing and order tools |
| **Pain Points** | Depends on middlemen; no direct online market access; cannot manage inventory digitally |
| **Verticals** | Marketplace Products |
| **Needs** | Easy product upload, order notifications, simple payout tracking |

### Persona V2: The Service Professional — "Advocate Sharma"

| Attribute | Detail |
|-----------|--------|
| **Business** | Legal and CA practice |
| **Location** | Jammu / Srinagar / Delhi |
| **Goal** | Acquire new clients for GST, ITR, and legal services through the platform |
| **Behavior** | Professional; values credibility; needs client management tools |
| **Pain Points** | Client acquisition cost; no digital presence for service discovery |
| **Verticals** | Professional Services |
| **Needs** | Service profile, inquiry management, document sharing, reviews |

### Persona V3: The Insurance Partner — "PolicyHub India"

| Attribute | Detail |
|-----------|--------|
| **Business** | IRDAI-licensed insurance aggregator |
| **Location** | Pan-India |
| **Goal** | Distribute insurance products through EcomHub's customer base |
| **Behavior** | API-driven; needs lead quality and conversion tracking |
| **Pain Points** | High customer acquisition cost; needs trusted distribution channels |
| **Verticals** | Insurance Marketplace |
| **Needs** | Product listing API, lead management, conversion reporting |

### Persona V4: The Travel Operator — "Dal Lake Tours"

| Attribute | Detail |
|-----------|--------|
| **Business** | Houseboat and tour operator |
| **Location** | Srinagar, J&K |
| **Goal** | Fill houseboat bookings and tour activities through online channel |
| **Behavior** | Seasonal business; manages availability manually; needs booking calendar |
| **Pain Points** | Depends on travel agents; high commission to OTAs; no direct booking channel |
| **Verticals** | Travel & Hospitality |
| **Needs** | Listing management, booking calendar, availability control, payout tracking |

### Persona V5: The Digital Creator — "TechLearn Academy"

| Attribute | Detail |
|-----------|--------|
| **Business** | Online courses and digital downloads |
| **Location** | Pan-India (remote) |
| **Goal** | Sell digital products and memberships through a trusted platform |
| **Behavior** | Tech-savvy; expects instant delivery and subscription management |
| **Pain Points** | Platform fees on global platforms; needs India-focused payment support |
| **Verticals** | Digital Services & Products |
| **Needs** | Digital upload, entitlement management, subscription billing |

---

## Admin & Operations Personas

### Persona A1: Platform Administrator — "Admin User"

| Role | Platform Admin |
| **Goal** | Operate the entire platform — vendors, content, finance, marketing |
| **Needs** | Dashboard, RBAC, audit logs, full admin portal access |

### Persona A2: Support Agent — "Support Team"

| Role | CRM Support Agent |
| **Goal** | Resolve customer tickets, process refunds, manage disputes |
| **Needs** | CRM module, order lookup, customer communication tools |

### Persona A3: Finance Manager — "Finance Team"

| Role | Finance Operator |
| **Goal** | Manage vendor settlements, reconcile payments, generate financial reports |
| **Needs** | Finance module, Razorpay reconciliation, payout management |

---

## Audience by Vertical

| Vertical | Primary Customers | Primary Vendors |
|----------|-------------------|-----------------|
| **Marketplace Products** | C1 (Regional Shopper), C6 (Local Buyer) | V1 (Artisan) |
| **Professional Services** | C2 (SMB Owner), C6 (Local Buyer) | V2 (Service Professional) |
| **Insurance Marketplace** | C3 (Insurance Buyer), C6 (Local Buyer) | V3 (Insurance Partner) |
| **Travel & Hospitality** | C4 (Travel Explorer), C6 (Local Buyer) | V4 (Travel Operator) |
| **Digital Services & Products** | C5 (Digital Consumer) | V5 (Digital Creator) |

---

## Geographic Segmentation

### Phase 1 — Launch

| Segment | Description |
|---------|-------------|
| **J&K Vendors** | Artisans, producers, travel operators, service professionals in Kashmir |
| **J&K Customers** | Local buyers using the platform for all verticals |
| **Pan-India Customers** | Buyers in metro and tier 1/2 cities purchasing regional products, services, insurance, travel |
| **Pan-India Vendors** | National brands, service professionals, insurance partners, digital creators |

### Phase 2 — Expansion

| Segment | Description |
|---------|-------------|
| **Multi-City Vendors** | Vendors in Delhi, Mumbai, Bangalore, Chennai, Kolkata |
| **Multi-City Customers** | Expanded customer base across major Indian cities |

### Phase 3 — International

| Segment | Description |
|---------|-------------|
| **International Customers** | NRIs and global buyers seeking authentic Indian products |
| **International Vendors** | Global brands and service providers |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [Project_Scope.md](Project_Scope.md) | What each persona can access |
| [Business_Goals.md](Business_Goals.md) | Business outcomes per segment |
| [Project_Vision.md](Project_Vision.md) | Vision alignment with audience needs |
| [Success_Metrics.md](Success_Metrics.md) | Audience-related KPIs |
| [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md) | User types and portal mapping |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 0 release |
