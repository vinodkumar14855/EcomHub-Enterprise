# Business Model

> **Version:** 1.0  
> **Status:** Draft  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines the **business model** for EcomHub Enterprise — how the platform creates, delivers, and captures value across all five verticals. It describes marketplace mechanics, vendor relationships, and revenue mechanisms.

Revenue rate specifics are defined in [Revenue_Model.md](Revenue_Model.md). Business requirements in [Business_Requirements_Document.md](Business_Requirements_Document.md).

---

## Table of Contents

1. [Business Model Overview](#business-model-overview)
2. [Marketplace Model](#marketplace-model)
3. [Multi-Vendor Model](#multi-vendor-model)
4. [Commission Structure](#commission-structure)
5. [Subscription Opportunities](#subscription-opportunities)
6. [Service Provider Revenue](#service-provider-revenue)
7. [Travel Partner Revenue](#travel-partner-revenue)
8. [Insurance Partner Revenue](#insurance-partner-revenue)
9. [Advertising Revenue](#advertising-revenue)
10. [Future Revenue Streams](#future-revenue-streams)
11. [Value Chain](#value-chain)
12. [Related Documents](#related-documents)

---

## Business Model Overview

EcomHub Enterprise operates as a **multi-vendor marketplace platform** — connecting buyers with sellers, service providers, travel operators, insurance partners, and digital creators through a unified platform. The platform captures value through transaction commissions, subscriptions, referral fees, and advertising.

### Business Model Canvas Summary

| Canvas Element | EcomHub Enterprise |
|----------------|-------------------|
| **Customer Segments** | Indian consumers, SMBs, travelers, insurance buyers, digital consumers |
| **Value Proposition** | One trusted platform for products, services, insurance, travel, and digital goods |
| **Channels** | Web storefront, customer portal, mobile-responsive web, SEO, marketing |
| **Customer Relationships** | Self-service, automated notifications, CRM support, reviews |
| **Revenue Streams** | Commissions, subscriptions, referral fees, advertising, lead generation |
| **Key Resources** | Platform technology, vendor network, brand, payment infrastructure |
| **Key Activities** | Platform operations, vendor onboarding, marketing, compliance |
| **Key Partners** | Vendors, Razorpay, insurance partners, logistics providers |
| **Cost Structure** | Technology, cloud, marketing, operations, payment processing fees |

---

## Marketplace Model

### Model Type

EcomHub Enterprise is a **managed multi-vendor marketplace** — the platform operator (EcomHub) governs vendor quality, customer experience, and transaction integrity while vendors retain ownership of their inventory, listings, and fulfillment.

### Marketplace Characteristics

| Characteristic | EcomHub Approach |
|----------------|-----------------|
| **Vendor ownership** | Vendors own products, services, and listings |
| **Platform governance** | EcomHub sets policies, verifies vendors, manages disputes |
| **Transaction facilitation** | Platform processes payments, calculates commissions, manages payouts |
| **Customer relationship** | Primary customer relationship is with EcomHub brand |
| **Inventory model** | Vendor-managed inventory (not platform-owned stock) |
| **Pricing control** | Vendors set their own prices within platform guidelines |
| **Fulfillment** | Vendor-fulfilled (products shipped by vendor; services delivered by provider) |

### Marketplace Flow

```
Customer → EcomHub Platform → Vendor
                │
         Payment Processing
         Commission Deduction
         Vendor Payout
         Customer Support
         Dispute Resolution
```

### Vertical Marketplace Variations

| Vertical | Marketplace Dynamic |
|----------|-------------------|
| **Products** | Standard e-commerce: vendor lists, customer buys, vendor ships |
| **Services** | Service marketplace: provider lists, customer inquires/books, provider delivers |
| **Insurance** | Aggregation marketplace: platform lists partner products, captures leads, partner converts |
| **Travel** | Booking marketplace: operator lists, customer books, operator fulfills experience |
| **Digital** | Digital marketplace: creator lists, customer purchases, platform delivers instantly |

---

## Multi-Vendor Model

### Vendor Types

| Vendor Type | Verticals | Examples |
|-------------|-----------|----------|
| **Product Seller** | Marketplace Products | Pashmina artisan, dry fruit producer, organic brand |
| **Service Provider** | Professional Services | CA firm, legal advocate, business consultant |
| **Insurance Partner** | Insurance Marketplace | IRDAI-licensed insurer or aggregator |
| **Travel Operator** | Travel & Hospitality | Houseboat owner, hotel, taxi service, tour guide |
| **Digital Creator** | Digital Products | Course creator, e-book publisher, membership provider |

### Vendor Lifecycle

```
Registration → Document Submission → Admin Verification →
Account Activated → Listing Creation → Listing Published →
Order/Booking Reception → Fulfillment → Payout → Ongoing Operations
```

### Vendor Tiers (Proposed)

| Tier | Name | Features | Cost |
|------|------|----------|------|
| **Tier 1** | Basic | Standard listing, basic analytics, standard commission rate | Free |
| **Tier 2** | Professional | Enhanced analytics, priority support, reduced commission rate | Monthly subscription |
| **Tier 3** | Enterprise | Premium placement, dedicated account manager, lowest commission rate | Monthly subscription |

> Tier pricing and commission rates defined in [Revenue_Model.md](Revenue_Model.md).

### Multi-Vendor Order Handling

| Scenario | Handling |
|----------|----------|
| Single vendor, single product | Direct order to vendor |
| Single vendor, multiple products | Combined order to vendor |
| Multiple vendors, multiple products | Split orders per vendor (deferred decision D-01) |
| Service booking | Direct booking to service provider |
| Travel booking | Direct booking to travel operator |
| Insurance inquiry | Lead routed to insurance partner |

---

## Commission Structure

### Commission Model

EcomHub earns a **percentage commission** on completed transactions. Commission is deducted from the vendor payout, not added to the customer price.

```
Customer Payment = Product/Service Price + GST + Shipping (if applicable)
Platform Commission = Transaction Value × Commission Rate
Vendor Payout = Transaction Value − Platform Commission − Payment Gateway Fee
```

### Proposed Commission Rates

| Vertical | Commission Rate | Basis |
|----------|----------------|-------|
| **Marketplace Products** | 8–15% | Category-dependent (see Revenue_Model.md) |
| **Professional Services** | 10–20% | Service type-dependent |
| **Travel & Hospitality** | 10–18% | Booking type-dependent |
| **Digital Products** | 15–25% | Product type-dependent |
| **Insurance** | Referral fee model | Per converted policy (not % commission) |

> All rates are **proposed** and require project owner approval. See [Revenue_Model.md](Revenue_Model.md) for detailed rate tables.

### Commission Rules

| Rule | Description |
|------|-------------|
| Commission calculated on pre-GST transaction value | GST passed through to vendor |
| Commission deducted before vendor payout | Transparent in vendor portal |
| No commission on cancelled/refunded orders | Commission reversed on refund |
| Subscription tier vendors receive reduced rates | Incentive for premium tiers |
| COD orders: commission deducted from next payout cycle | After delivery confirmation |

---

## Subscription Opportunities

### Vendor Subscription Tiers

| Feature | Basic (Free) | Professional | Enterprise |
|---------|-------------|-------------|------------|
| Product/service listings | Up to 50 | Up to 500 | Unlimited |
| Analytics | Basic (30-day) | Advanced (12-month) | Custom reports |
| Commission rate | Standard | Reduced (2% lower) | Lowest (4% lower) |
| Support | Email | Priority email + chat | Dedicated account manager |
| Promoted listings | Not included | 2 per month | 10 per month |
| API access | No | No | Yes (future) |
| Monthly cost | Free | ₹999/month | ₹4,999/month |

> Pricing is **proposed** and subject to market validation.

### Customer Subscription (Future)

| Offering | Description | Timeline |
|----------|-------------|----------|
| **EcomHub Plus** | Free shipping on products, priority support, exclusive deals | Post-MVP |
| **Digital membership bundles** | Access to digital product libraries | MVP (via Digital vertical) |

---

## Service Provider Revenue

### Professional Services Revenue Model

| Revenue Mechanism | Description |
|-------------------|-------------|
| **Service commission** | Percentage of completed service transaction value |
| **Lead generation fee** | Fixed fee per qualified inquiry delivered to provider |
| **Premium provider listing** | Enhanced visibility in service category search results |
| **Featured provider badge** | "Verified Professional" badge for subscription providers |

### Service Categories and Revenue Potential

| Service | Avg. Transaction Value (INR) | Commission Rate | Platform Revenue per Transaction |
|---------|------------------------------|-----------------|--------------------------------|
| CA Services | ₹2,000–₹10,000 | 15% | ₹300–₹1,500 |
| GST Filing | ₹1,500–₹5,000 | 15% | ₹225–₹750 |
| ITR Filing | ₹500–₹3,000 | 15% | ₹75–₹450 |
| Legal Services | ₹3,000–₹25,000 | 12% | ₹360–₹3,000 |
| Business Consultancy | ₹5,000–₹50,000 | 10% | ₹500–₹5,000 |

### Service Provider Engagement Model

1. Provider registers and creates service profile with qualifications
2. Provider lists services with pricing (fixed or "starting from")
3. Customer submits inquiry or books directly
4. Provider delivers service and marks complete
5. Platform processes payment and deducts commission
6. Provider receives payout on scheduled cycle

---

## Travel Partner Revenue

### Travel Revenue Model

| Revenue Mechanism | Description |
|-------------------|-------------|
| **Booking commission** | Percentage of confirmed booking value |
| **Featured listing** | Premium placement in travel search results |
| **Package promotion** | Promoted holiday packages on homepage and category pages |
| **Seasonal campaigns** | Sponsored travel campaigns (e.g., "Kashmir Summer Special") |

### Travel Categories and Revenue Potential

| Category | Avg. Booking Value (INR) | Commission Rate | Platform Revenue per Booking |
|----------|--------------------------|-----------------|------------------------------|
| Houseboat Booking | ₹3,000–₹15,000/night | 12% | ₹360–₹1,800 |
| Hotel Booking | ₹2,000–₹10,000/night | 10% | ₹200–₹1,000 |
| Taxi Booking | ₹500–₹3,000 | 15% | ₹75–₹450 |
| Holiday Packages | ₹10,000–₹50,000 | 12% | ₹1,200–₹6,000 |
| Tour Activities | ₹500–₹5,000 | 15% | ₹75–₹750 |
| Local Experiences | ₹1,000–₹8,000 | 15% | ₹150–₹1,200 |

### Travel Partner Engagement Model

1. Travel operator registers with business details and licenses
2. Operator creates listings with photos, pricing, availability calendar
3. Customer searches, views, and books with payment
4. Operator confirms booking and delivers experience
5. Platform deducts commission and processes operator payout

---

## Insurance Partner Revenue

### Insurance Revenue Model

EcomHub operates as an **insurance marketplace/aggregator**, not an underwriter. Revenue is generated through **referral fees** paid by partner insurers on converted policies.

| Revenue Mechanism | Description |
|-------------------|-------------|
| **Policy conversion fee** | Fixed or percentage fee per policy sold through platform referral |
| **Lead generation fee** | Fee per qualified insurance inquiry delivered to partner |
| **Featured insurer placement** | Premium placement in insurance comparison results |
| **Co-branded campaigns** | Joint marketing campaigns with insurance partners |

### Insurance Categories and Revenue Potential

| Category | Avg. Annual Premium (INR) | Referral Fee Model | Estimated Platform Revenue |
|----------|--------------------------|--------------------|-----------------------------|
| Health Insurance | ₹8,000–₹30,000 | 5–10% of first-year premium | ₹400–₹3,000 |
| Car Insurance | ₹5,000–₹20,000 | 10–15% of premium | ₹500–₹3,000 |
| Bike Insurance | ₹1,000–₹5,000 | 10–15% of premium | ₹100–₹750 |
| Life Insurance | ₹10,000–₹50,000 | 15–25% of first-year premium | ₹1,500–₹12,500 |
| Travel Insurance | ₹300–₹2,000 | 15–20% of premium | ₹45–₹400 |

### Insurance Partner Requirements

- IRDAI license verification before partnership
- API integration for quote comparison (preferred) or structured lead handoff
- Compliance with IRDAI intermediary guidelines
- Clear disclosure of platform role as aggregator, not underwriter

---

## Advertising Revenue

### Advertising Products

| Ad Product | Description | Pricing Model |
|------------|-------------|---------------|
| **Homepage banner** | Rotating banner on storefront homepage | Monthly fixed fee |
| **Category featured placement** | Top placement within a product/service category | Monthly fixed fee |
| **Search result promotion** | Sponsored results in search (clearly labeled) | CPC or monthly fee |
| **Email campaign inclusion** | Vendor featured in platform email newsletters | Per campaign fee |
| **Seasonal campaign sponsorship** | Named sponsorship of seasonal promotions | Campaign-based fee |
| **Vendor storefront branding** | Enhanced vendor profile page with custom branding | Monthly subscription |

### Proposed Advertising Rates

| Placement | Monthly Rate (INR) | Target Advertiser |
|-----------|-----------------|-------------------|
| Homepage banner (top) | ₹10,000–₹25,000 | National brands, travel operators |
| Category featured (per category) | ₹3,000–₹8,000 | Product sellers, service providers |
| Search promotion (CPC) | ₹5–₹20 per click | All vendor types |
| Email feature | ₹5,000 per campaign | Product sellers, digital creators |

> Rates are **proposed** and will be validated against market benchmarks.

### Advertising Rules

| Rule | Description |
|------|-------------|
| Sponsored content clearly labeled | "Sponsored" or "Promoted" badge on all paid placements |
| No misleading claims | Advertising content must comply with platform listing standards |
| Insurance ads require IRDAI compliance | Insurance advertising follows IRDAI advertising guidelines |
| Admin approval required | All advertising content reviewed before publication |

---

## Future Revenue Streams

| Stream | Description | Timeline | Potential |
|--------|-------------|----------|-----------|
| **SaaS offerings** | Platform-hosted software products in Digital vertical | Year 2+ | High |
| **White-label platform** | License platform to other regional marketplaces | Year 3+ | High |
| **Logistics services** | Platform-managed shipping with margin | Year 2 | Medium |
| **Financial services** | Vendor loans, customer EMI, wallet interest | Year 2+ | High |
| **Data insights** | Anonymized market analytics sold to brands | Year 2+ | Medium |
| **International transaction fees** | Cross-border payment and currency conversion fees | Year 3+ | Medium |
| **API access fees** | Developer API for third-party integrations | Year 2 | Low–Medium |
| **Training & certification** | Vendor training programs and platform certification | Year 2 | Low |

---

## Value Chain

```
┌─────────────┐    ┌──────────────┐    ┌─────────────┐    ┌──────────────┐
│   Vendors    │───▶│   EcomHub    │───▶│  Customers  │───▶│   Reviews    │
│  (Supply)    │    │  (Platform)  │    │  (Demand)   │    │  (Trust)     │
└─────────────┘    └──────┬───────┘    └─────────────┘    └──────────────┘
                          │
              ┌───────────┼───────────┐
              ▼           ▼           ▼
        ┌──────────┐ ┌─────────┐ ┌──────────┐
        │ Payments │ │Marketing│ │Compliance│
        │(Razorpay)│ │  & SEO  │ │ & Audit  │
        └──────────┘ └─────────┘ └──────────┘
                          │
                          ▼
                   Platform Revenue
              (Commission + Subscription
               + Referral + Advertising)
```

### Value Created at Each Stage

| Stage | Value Created | Revenue Capture |
|-------|--------------|-----------------|
| **Vendor onboarding** | Supply side growth | Subscription fees |
| **Listing & discovery** | Product/service visibility | Advertising, premium listing |
| **Transaction** | Commerce facilitation | Commission |
| **Payment processing** | Payment convenience | Embedded in commission |
| **Fulfillment support** | Order tracking, notifications | Embedded in commission |
| **Insurance referral** | Lead qualification | Referral fee |
| **Trust building** | Reviews, verification, audit | Retention → repeat transactions |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [Business_Requirements_Document.md](Business_Requirements_Document.md) | Business requirements |
| [Revenue_Model.md](Revenue_Model.md) | Detailed revenue rates and projections |
| [Market_Strategy.md](Market_Strategy.md) | Go-to-market and competitive positioning |
| [User_Personas.md](User_Personas.md) | Target user segments |
| [docs/01_Project/Business_Goals.md](../01_Project/Business_Goals.md) | Strategic business goals |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 1 release |
