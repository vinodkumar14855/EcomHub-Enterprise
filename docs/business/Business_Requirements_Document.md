# Business Requirements Document (BRD)

> **Version:** 1.0  
> **Status:** Draft  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)  
> **Classification:** Internal — Business Requirements

---

## Purpose

This Business Requirements Document (BRD) defines the **business needs, processes, rules, and success criteria** for EcomHub Enterprise. It translates strategic vision from Phase 0 into actionable business requirements that will drive product, architecture, and implementation decisions in subsequent phases.

This document does not define technical specifications, UI designs, or database schemas.

---

## Table of Contents

1. [Business Overview](#business-overview)
2. [Problem Statement](#problem-statement)
3. [Market Opportunity](#market-opportunity)
4. [Business Objectives](#business-objectives)
5. [Revenue Opportunities](#revenue-opportunities)
6. [Stakeholders](#stakeholders)
7. [Business Processes](#business-processes)
8. [Business Rules](#business-rules)
9. [Operational Requirements](#operational-requirements)
10. [Compliance Requirements](#compliance-requirements)
11. [Success Criteria](#success-criteria)
12. [Related Documents](#related-documents)

---

## Business Overview

### Platform Summary

EcomHub Enterprise is an **enterprise-grade, multi-vendor commerce platform** that unifies five business verticals within a single ecosystem:

| # | Vertical | Core Offerings |
|---|----------|----------------|
| 1 | **Marketplace Products** | Pashmina, dry fruits, honey, ghee, saffron, Kashmiri handicrafts, organic products, general consumer products |
| 2 | **Professional Services** | CA services, GST filing, ITR filing, accounting, legal, business consultancy |
| 3 | **Insurance Marketplace** | Health, car, bike, life, travel insurance |
| 4 | **Travel & Hospitality** | Houseboats, hotels, taxis, holiday packages, tour activities, local experiences |
| 5 | **Digital Services & Products** | Online services, digital downloads, memberships, future SaaS |

### Business Context

| Attribute | Detail |
|-----------|--------|
| **Project Name** | EcomHub Enterprise |
| **Launch Geography** | India — Jammu & Kashmir / Srinagar |
| **Delivery Model** | Multi-vendor marketplace with platform-operated governance |
| **Target Market** | Indian consumers, SMBs, travelers, and regional/national vendors |
| **Payment Model (Phase 1)** | Razorpay (UPI, cards, net banking, wallets) + Cash on Delivery |
| **Business Model** | Commission-based marketplace with subscription, referral, and advertising revenue |

### Strategic Position

EcomHub Enterprise launches with **Kashmir marketplace identity** — authentic regional products and travel experiences — while architecting for **pan-India expansion** and future international markets. The platform operates three dedicated portals:

- **Customer Portal** — Purchase, booking, and account management
- **Vendor Portal** — Catalog, fulfillment, analytics, and payouts
- **Admin Portal** — CMS, CRM, finance, marketing, RBAC, audit logs

> Reference: [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)

---

## Problem Statement

### Customer Problems

| Problem | Impact | Affected Segments |
|---------|--------|-------------------|
| **Fragmented commerce** | Customers use separate platforms for products, services, insurance, travel, and digital goods | All customer segments |
| **Regional product authenticity** | No trusted single destination for verified Kashmiri products (Pashmina, saffron, handicrafts) | Buyers nationwide |
| **Service discovery friction** | CA, GST, ITR, and legal services require word-of-mouth or disconnected directories | SMB owners, individuals |
| **Insurance complexity** | Too many insurer websites; confusing comparison; distrust of agents | Insurance buyers |
| **Travel booking fragmentation** | Kashmir trips require multiple apps for houseboats, hotels, taxis, and activities | Travelers |
| **Inconsistent payment experience** | Different payment flows across platforms; limited UPI/COD integration | All Indian customers |

### Vendor Problems

| Problem | Impact | Affected Segments |
|---------|--------|-------------------|
| **Limited market reach** | Kashmiri artisans and producers depend on intermediaries with reduced margins | Product sellers, handicraft artisans |
| **No unified selling platform** | Vendors managing products cannot also offer services or bookings on the same platform | Multi-category vendors |
| **High cost of independent e-commerce** | Building standalone online stores is expensive and technically complex | Small and medium vendors |
| **Lack of enterprise tools** | No access to CRM, analytics, marketing, and payout management | All vendor types |
| **OTA commission burden** | Travel operators pay high commissions to existing OTAs with no direct customer relationship | Hotels, houseboats, taxi operators |

### Platform Operator Problems

| Problem | Impact |
|---------|--------|
| **Multiple system overhead** | Operating separate systems for each vertical creates integration cost and data silos |
| **Trust and compliance burden** | Insurance, legal services, and high-value products require governance frameworks |
| **Vendor quality control** | Unverified vendors damage platform trust, especially for authentic regional products |

---

## Market Opportunity

### India E-Commerce Landscape

India's e-commerce market continues rapid growth, driven by UPI adoption, smartphone penetration, and Tier 2/3 city expansion. Key market dynamics:

| Factor | Opportunity for EcomHub |
|--------|--------------------------|
| **UPI dominance** | 70%+ of digital payments in India; Razorpay-native platform advantage |
| **Regional product demand** | Growing demand for authentic, traceable regional specialties online |
| **Service digitization** | GST/ITR/legal services increasingly sought online post-Digital India |
| **Insurance penetration** | Low insurance penetration in India; comparison platforms add value |
| **Domestic tourism recovery** | Kashmir tourism demand creates houseboat, hotel, and experience booking opportunity |
| **Digital product growth** | Online courses, downloads, and memberships expanding in India |

### Jammu & Kashmir Opportunity

| Segment | Opportunity |
|---------|-------------|
| **Regional products** | Pashmina, saffron, dry fruits, honey, ghee, handicrafts have national and NRI demand |
| **Tourism** | Dal Lake houseboats, Gulmarg, Pahalgam, Sonamarg drive domestic and international tourism |
| **Local services** | CA, legal, and consultancy services for J&K businesses and residents |
| **Artisan economy** | Direct-to-consumer channel eliminates middlemen for Kashmiri producers |

### Addressable Market (Directional)

| Segment | Phase 1 Focus | Expansion |
|---------|---------------|-----------|
| **Product buyers** | Pan-India customers purchasing Kashmiri and general products | Multi-city, international |
| **Service customers** | J&K and pan-India SMBs and individuals | National service provider network |
| **Insurance customers** | Pan-India insurance buyers | Same, with deeper insurer partnerships |
| **Travelers** | Domestic tourists planning Kashmir trips | Pan-India travel packages |
| **Digital consumers** | Urban India digital product buyers | National and global |

> Detailed market strategy in [Market_Strategy.md](Market_Strategy.md). Revenue detail in [Revenue_Model.md](Revenue_Model.md).

---

## Business Objectives

Business objectives align with [docs/01_Project/Business_Goals.md](../01_Project/Business_Goals.md).

### Strategic Objectives

| ID | Objective | Target Horizon |
|----|-----------|----------------|
| BO-01 | Launch EcomHub as a recognized unified commerce brand rooted in J&K identity | Year 1 |
| BO-02 | Onboard and operate unlimited vendors across all five verticals | MVP – Year 1 |
| BO-03 | Establish platform trust for high-value regional products and regulated services | MVP – Year 1 |
| BO-04 | Empower Kashmiri artisans and producers with direct national market access | Year 1 |
| BO-05 | Build modular platform ready for pan-India and international expansion | Year 1–3 |

### Vertical Objectives

| Vertical | Objective |
|----------|-----------|
| **Marketplace Products** | Curated catalog of authentic Kashmiri products plus national/general merchandise |
| **Professional Services** | Connect customers with verified CA, legal, and consultancy professionals |
| **Insurance Marketplace** | Offer IRDAI-compliant insurance comparison and lead conversion |
| **Travel & Hospitality** | Become the preferred Kashmir travel booking platform |
| **Digital Products** | Enable online services, downloads, and membership sales |

### Commercial Objectives

| ID | Objective | Metric Reference |
|----|-----------|------------------|
| BO-C01 | Achieve positive platform revenue within 12 months of launch | SM-B02 |
| BO-C02 | Reach ₹5L monthly GMV at launch scaling to ₹5Cr by month 12 | SM-B01 |
| BO-C03 | Maintain payment success rate ≥ 95% | SM-05 |
| BO-C04 | Achieve platform trust score ≥ 4.0 at launch | SM-03 |

---

## Revenue Opportunities

Revenue opportunities are detailed in [Revenue_Model.md](Revenue_Model.md) and [Business_Model.md](Business_Model.md).

| # | Revenue Stream | Vertical | Model |
|---|----------------|----------|-------|
| 1 | **Product commission** | Marketplace Products | % of product sale value |
| 2 | **Service commission** | Professional Services | % of service transaction value |
| 3 | **Booking commission** | Travel & Hospitality | % of booking value |
| 4 | **Insurance referral fee** | Insurance Marketplace | Fixed/variable fee per converted policy |
| 5 | **Digital product commission** | Digital Products | % of digital sale/subscription value |
| 6 | **Vendor subscription** | All verticals | Monthly/annual premium vendor tiers |
| 7 | **Premium listing / promoted placement** | All verticals | Pay-per-placement or subscription boost |
| 8 | **Advertising revenue** | All verticals | Banner ads, sponsored categories, email campaigns |
| 9 | **Lead generation fees** | Services, Insurance | Fee per qualified lead delivered |

---

## Stakeholders

### Internal Stakeholders

| Stakeholder | Role | Interest |
|-------------|------|----------|
| **Project Owner** | Strategic direction and approval authority | Platform success, ROI, brand |
| **Product Architecture** | Documentation, scope, and alignment | Coherent platform design |
| **Platform Admin** | Day-to-day platform operations | Efficient admin tools, RBAC, audit |
| **Finance Team** | Settlements, reconciliation, reporting | Accurate financial operations |
| **Support Team** | Customer and vendor support | CRM, ticket resolution, dispute tools |
| **Content/Marketing Team** | CMS, campaigns, SEO | Content management, promotional tools |

### External Stakeholders

| Stakeholder | Role | Interest |
|-------------|------|----------|
| **Customers** | Purchase, book, and manage services | Trust, value, seamless UX |
| **Vendors / Sellers** | List and fulfill on platform | Reach, tools, fair payouts |
| **Insurance Partners** | IRDAI-licensed insurers/aggregators | Quality leads, conversions |
| **Payment Gateway (Razorpay)** | Payment processing | Transaction volume, compliance |
| **Logistics Partners** | Product delivery (future integration) | Shipping volume |
| **Regulatory Bodies** | IRDAI, GST Council, RBI, DPDP Authority | Compliance adherence |
| **Regional Artisan Communities** | Product suppliers | Fair pricing, market access |

### Stakeholder Influence Matrix

```
                    Interest
                Low         High
           ┌──────────┬──────────┐
    High   │ Keep     │ Manage   │
 Influence │ Satisfied│ Closely  │
           ├──────────┼──────────┤
    Low    │ Monitor  │ Keep     │
           │          │ Informed │
           └──────────┴──────────┘

Manage Closely: Project Owner, Customers, Vendors, Razorpay
Keep Satisfied:  Insurance Partners, Platform Admin, Finance
Keep Informed:   Regulatory Bodies, Logistics Partners
Monitor:         Competitors, Regional Communities
```

---

## Business Processes

### BP-01: Customer Purchase Process (Marketplace Products)

```
Browse Catalog → Search/Filter → View Product → Add to Cart →
Checkout → Select Address → Select Payment (UPI/Card/COD) →
Place Order → Order Confirmation → Vendor Fulfillment →
Delivery → Customer Review
```

| Step | Actor | Business Requirement |
|------|-------|---------------------|
| Browse/Search | Customer | Access categorized catalog with search and filters |
| Add to Cart | Customer | Multi-product cart with quantity management |
| Checkout | Customer | Address selection, payment method, order summary |
| Payment | Customer + Platform | Razorpay online payment or COD selection |
| Fulfillment | Vendor | Accept order, pack, ship with tracking |
| Delivery | Logistics | Pan-India delivery with status updates |
| Review | Customer | Post-delivery rating and review |

### BP-02: Service Booking Process (Professional Services)

```
Browse Services → View Provider Profile → Submit Inquiry →
Provider Response → Confirm Booking → Service Delivery →
Payment Settlement → Customer Review
```

### BP-03: Insurance Inquiry Process

```
Browse Insurance Types → Compare Products → Request Quote →
Lead Captured → Partner Insurer Contact → Policy Purchase (off-platform or integrated) →
Policy Document Upload → Customer Portal Storage
```

### BP-04: Travel Booking Process

```
Search Listings → Filter (dates, location, type) → View Details →
Check Availability → Book → Payment → Booking Confirmation →
Experience Delivery → Customer Review
```

### BP-05: Digital Product Purchase Process

```
Browse Digital Products → View Details → Purchase →
Instant Payment → Digital Delivery/Access → Entitlement Active
```

### BP-06: Vendor Onboarding Process

```
Vendor Registration → Profile Creation → Document Submission →
Admin Verification/Approval → Catalog Setup → Listing Published →
Order/Booking Reception → Fulfillment → Payout Settlement
```

### BP-07: Vendor Payout Process

```
Order Completed → Commission Calculated → Payout Scheduled →
Razorpay Transfer → Vendor Notified → Finance Reconciliation
```

### BP-08: Admin Governance Process

```
Vendor/Application Review → Approve/Reject → Ongoing Monitoring →
Report Generation → Dispute Resolution → Audit Log Entry
```

### BP-09: Dispute Management Process

```
Customer Raises Dispute → Support Ticket Created →
Evidence Collection → Admin Review → Resolution (Refund/Replacement/Reject) →
Audit Log → Customer/Vendor Notification
```

> Detailed user journeys in [User_Journey.md](User_Journey.md).

---

## Business Rules

### General Platform Rules

| Rule ID | Rule | Applies To |
|---------|------|------------|
| BR-01 | All vendors must complete registration and verification before listing | Vendors |
| BR-02 | All product listings must include accurate descriptions, images, and pricing | Vendors |
| BR-03 | Platform commission is deducted from vendor payout, not added to customer price | Finance |
| BR-04 | All admin actions must be logged in the audit trail | Admin |
| BR-05 | Customer reviews are permitted only after order/booking completion | Customers |
| BR-06 | Refund policies are defined per vertical and displayed before purchase | All |
| BR-07 | GST is applied as per Indian tax regulations on applicable transactions | Finance |
| BR-08 | Platform wallet balance cannot go negative | Customers |

### Marketplace Product Rules

| Rule ID | Rule |
|---------|------|
| BR-M01 | COD is available for product orders below a configurable maximum value |
| BR-M02 | Vendors must update inventory within 24 hours of stock change |
| BR-M03 | Product returns follow a 7-day return policy (configurable per category) |
| BR-M04 | Authenticity claims (e.g., "GI Tagged Pashmina") require verification documentation |
| BR-M05 | Prohibited products (weapons, narcotics, counterfeit) are not permitted |

### Professional Services Rules

| Rule ID | Rule |
|---------|------|
| BR-S01 | Service providers must display qualifications and registration numbers where applicable |
| BR-S02 | Service inquiries must receive provider response within 48 hours |
| BR-S03 | Service fees must be clearly stated before booking confirmation |
| BR-S04 | Document sharing between customer and provider is encrypted |

### Insurance Rules

| Rule ID | Rule |
|---------|------|
| BR-I01 | Only IRDAI-licensed partners may list insurance products |
| BR-I02 | Platform is an aggregator/marketplace, not an underwriter |
| BR-I03 | Insurance terms, exclusions, and claim processes must be displayed per product |
| BR-I04 | Customer consent is required before sharing lead data with insurance partners |

### Travel & Hospitality Rules

| Rule ID | Rule |
|---------|------|
| BR-T01 | Travel vendors must maintain accurate availability calendars |
| BR-T02 | Booking cancellations follow vendor-defined cancellation policies displayed at booking |
| BR-T03 | Houseboat and hotel listings must include photos, amenities, and location |
| BR-T04 | Taxi operators must display fare structure before booking confirmation |

### Digital Products Rules

| Rule ID | Rule |
|---------|------|
| BR-D01 | Digital products must be delivered instantly upon successful payment |
| BR-D02 | Membership subscriptions auto-renew unless cancelled by customer |
| BR-D03 | Download links expire after a configurable number of days |
| BR-D04 | Refunds on digital products are at platform discretion after download |

### Payment Rules

| Rule ID | Rule |
|---------|------|
| BR-P01 | Online payments processed exclusively through Razorpay in Phase 1 |
| BR-P02 | COD orders are confirmed upon placement; payment collected at delivery |
| BR-P03 | Vendor payouts occur on a configurable schedule (proposed: weekly) |
| BR-P04 | Payment disputes follow Razorpay dispute resolution process |
| BR-P05 | Failed online payments do not create orders |

---

## Operational Requirements

### OR-01: Vendor Operations

| Requirement | Description | Priority |
|-------------|-------------|----------|
| OR-01.1 | Vendor self-registration with profile and document upload | MVP |
| OR-01.2 | Admin approval workflow for vendor verification | MVP |
| OR-01.3 | Vendor dashboard with order/booking notifications | MVP |
| OR-01.4 | Vendor catalog management (add, edit, deactivate listings) | MVP |
| OR-01.5 | Vendor inventory management with low-stock alerts | MVP |
| OR-01.6 | Vendor payout tracking and history | MVP |
| OR-01.7 | Vendor analytics (sales, top products, revenue trends) | MVP |

### OR-02: Customer Operations

| Requirement | Description | Priority |
|-------------|-------------|----------|
| OR-02.1 | Customer registration via email, phone, or social login | MVP |
| OR-02.2 | Unified order and booking history across verticals | MVP |
| OR-02.3 | Address management for product delivery | MVP |
| OR-02.4 | Platform wallet for refunds and credits | MVP |
| OR-02.5 | Notification preferences (email, SMS, in-app) | MVP |
| OR-02.6 | Wishlist for products and saved services | MVP |

### OR-03: Admin Operations

| Requirement | Description | Priority |
|-------------|-------------|----------|
| OR-03.1 | Admin dashboard with platform KPIs | MVP |
| OR-03.2 | Vendor approval and management | MVP |
| OR-03.3 | CMS for pages, banners, and SEO content | MVP |
| OR-03.4 | CRM for customer support tickets | MVP |
| OR-03.5 | Finance module for settlements and reconciliation | MVP |
| OR-03.6 | Marketing module for promotions and coupons | MVP |
| OR-03.7 | RBAC with configurable roles and permissions | MVP |
| OR-03.8 | Audit log for all admin and financial actions | MVP |

### OR-04: Payment Operations

| Requirement | Description | Priority |
|-------------|-------------|----------|
| OR-04.1 | Razorpay integration for UPI, cards, net banking, wallets | MVP |
| OR-04.2 | COD workflow with delivery confirmation | MVP |
| OR-04.3 | Automated commission calculation per transaction | MVP |
| OR-04.4 | Scheduled vendor payout processing | MVP |
| OR-04.5 | Payment reconciliation with Razorpay dashboard | MVP |
| OR-04.6 | Refund processing through Razorpay | MVP |

### OR-05: Fulfillment Operations

| Requirement | Description | Priority |
|-------------|-------------|----------|
| OR-05.1 | Order status lifecycle (placed → confirmed → shipped → delivered) | MVP |
| OR-05.2 | Booking status lifecycle (requested → confirmed → completed) | MVP |
| OR-05.3 | Service order tracking (inquiry → booked → in-progress → completed) | MVP |
| OR-05.4 | Digital product instant delivery upon payment | MVP |
| OR-05.5 | Notification at each status change | MVP |

---

## Compliance Requirements

### Regulatory Compliance Matrix

| Regulation | Applicability | Requirement |
|------------|---------------|-------------|
| **GST Act** | All taxable transactions | GST calculation, invoicing, vendor GSTIN collection |
| **Income Tax Act** | Vendor payouts | TDS on vendor payments above threshold (future) |
| **RBI Payment Guidelines** | Online payments | Razorpay PCI-DSS compliant payment processing |
| **IRDAI Regulations** | Insurance vertical | Only licensed partners; clear aggregator disclosure |
| **DPDP Act 2023** | All personal data | Consent-based data collection, storage, and deletion rights |
| **Consumer Protection Act 2019** | All customer transactions | Clear pricing, return/refund policies, grievance redressal |
| **IT Act 2000** | Digital operations | Data security, electronic records, digital signatures |
| **Geographical Indications (GI)** | Regional products | Accurate GI tagging for Pashmina and other GI products |

### Data Protection Requirements

| Requirement | Description |
|-------------|-------------|
| CR-D01 | Customer consent before collecting personal data |
| CR-D02 | Data minimization — collect only necessary information |
| CR-D03 | Right to deletion — customers can request account and data deletion |
| CR-D04 | Encryption of sensitive data (payment tokens, documents) |
| CR-D05 | Insurance lead data shared with partners only with explicit consent |
| CR-D06 | Audit trail for all data access by admin users |

### Payment Compliance

| Requirement | Description |
|-------------|-------------|
| CR-P01 | No storage of card details — Razorpay tokenization only |
| CR-P02 | PCI-DSS compliance via Razorpay gateway |
| CR-P03 | UPI transactions follow NPCI guidelines |
| CR-P04 | COD collection records maintained for reconciliation |

### Insurance Compliance

| Requirement | Description |
|-------------|-------------|
| CR-I01 | Platform displays IRDAI registration details of partner insurers |
| CR-I02 | Insurance product information includes IRDAI-mandated disclosures |
| CR-I03 | No platform guarantee on insurance claims — insurer responsibility |
| CR-I04 | Lead sharing complies with IRDAI intermediary guidelines |

---

## Success Criteria

Success criteria align with [docs/01_Project/Success_Metrics.md](../01_Project/Success_Metrics.md).

### Launch Success Criteria (Month 0–1)

| Criteria | Target |
|----------|--------|
| Platform live with all five verticals operational | Yes |
| Minimum 50 active vendors onboarded | ≥ 50 |
| Minimum 500 registered customers | ≥ 500 |
| Payment success rate | ≥ 95% |
| Platform trust score (average review) | ≥ 4.0 |
| All admin modules functional (CMS, CRM, RBAC, audit) | Yes |
| Zero critical security vulnerabilities in production | Yes |

### Growth Success Criteria (Month 6)

| Criteria | Target |
|----------|--------|
| Monthly GMV | ≥ ₹50L |
| Active vendors | ≥ 200 |
| Registered customers | ≥ 5,000 |
| Search conversion rate | ≥ 3% |
| Vendor monthly active rate | ≥ 60% |
| Customer repeat purchase rate (30-day) | ≥ 15% |

### Scale Success Criteria (Month 12)

| Criteria | Target |
|----------|--------|
| Monthly GMV | ≥ ₹5Cr |
| Active vendors | ≥ 1,000 |
| Registered customers | ≥ 25,000 |
| Platform trust score | ≥ 4.5 |
| Organic traffic percentage | ≥ 40% |
| Vertical adoption (customers using 2+ verticals) | ≥ 30% |

### Business Health Indicators

| Indicator | Healthy Range |
|-----------|---------------|
| Vendor retention rate (monthly) | ≥ 80% |
| Customer acquisition cost | ≤ ₹150 |
| COD order percentage | Declining trend (≤ 40% by month 12) |
| Support ticket resolution time | ≤ 24 hours |
| Vendor payout success rate | ≥ 99% |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [Business_Model.md](Business_Model.md) | Business and revenue model detail |
| [Revenue_Model.md](Revenue_Model.md) | Revenue stream definitions |
| [User_Personas.md](User_Personas.md) | Detailed user personas |
| [User_Journey.md](User_Journey.md) | End-to-end user journeys |
| [Market_Strategy.md](Market_Strategy.md) | Go-to-market strategy |
| [docs/01_Project/Project_Scope.md](../01_Project/Project_Scope.md) | MVP scope boundaries |
| [docs/01_Project/Success_Metrics.md](../01_Project/Success_Metrics.md) | KPI definitions and targets |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 1 release |
