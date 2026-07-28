# Success Metrics

> **Version:** 1.0  
> **Status:** Draft  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines the **Key Performance Indicators (KPIs) and success criteria** for EcomHub Enterprise. Metrics are linked to business goals ([Business_Goals.md](Business_Goals.md)) and project objectives ([Project_Objectives.md](Project_Objectives.md)).

Metrics are classified by measurement phase: **Launch**, **Growth (6 months)**, and **Scale (12 months)**.

---

## Table of Contents

1. [Metrics Framework](#metrics-framework)
2. [Platform KPIs](#platform-kpis)
3. [Vertical KPIs](#vertical-kpis)
4. [Portal KPIs](#portal-kpis)
5. [Technical KPIs](#technical-kpis)
6. [Business KPIs](#business-kpis)
7. [Metric Definitions & Targets](#metric-definitions--targets)
8. [Measurement Tools (Proposed)](#measurement-tools-proposed)
9. [Related Documents](#related-documents)

---

## Metrics Framework

| Classification | Description |
|----------------|-------------|
| **North Star Metric** | Single primary indicator of platform success |
| **Platform KPIs** | Cross-vertical platform health metrics |
| **Vertical KPIs** | Domain-specific performance metrics |
| **Portal KPIs** | User-type-specific engagement metrics |
| **Technical KPIs** | Performance, reliability, and security metrics |
| **Business KPIs** | Revenue, growth, and commercial metrics |

### North Star Metric

> **Monthly Gross Merchandise Value (GMV)** — Total value of all transactions (products, services, bookings, insurance leads, digital purchases) processed through the platform in a calendar month.

---

## Platform KPIs

| ID | Metric | Description | Launch Target | 6-Month Target | 12-Month Target |
|----|--------|-------------|---------------|----------------|-----------------|
| SM-01 | **Registered Customers** | Total customer accounts created | 500 | 5,000 | 25,000 |
| SM-02 | **Active Vendors** | Vendors with at least one active listing | 50 | 200 | 1,000 |
| SM-03 | **Platform Trust Score** | Average customer rating across all verticals (1–5) | ≥ 4.0 | ≥ 4.2 | ≥ 4.5 |
| SM-04 | **Regional Vendor %** | Percentage of vendors based in J&K | ≥ 40% | ≥ 30% | ≥ 20% |
| SM-05 | **Payment Success Rate** | Successful payment transactions / total attempts | ≥ 95% | ≥ 97% | ≥ 98% |
| SM-06 | **Search Conversion Rate** | Purchases/bookings from search / total searches | ≥ 2% | ≥ 3% | ≥ 5% |
| SM-07 | **Mobile Traffic %** | Sessions from mobile devices / total sessions | ≥ 70% | ≥ 75% | ≥ 80% |
| SM-08 | **Vertical Adoption** | Customers using 2+ verticals / total customers | ≥ 10% | ≥ 20% | ≥ 30% |
| SM-09 | **International Readiness** | Architecture supports multi-currency (yes/no) | No | No | Yes |
| SM-10 | **Admin Audit Coverage** | Admin actions logged / total admin actions | 100% | 100% | 100% |

---

## Vertical KPIs

### Marketplace Products

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-M01 | Product SKUs listed | 200 | 1,000 | 5,000 |
| SM-M02 | Product orders / month | 100 | 1,000 | 5,000 |
| SM-M03 | Average order value (INR) | ₹500 | ₹750 | ₹1,000 |
| SM-M04 | COD order % | ≤ 60% | ≤ 50% | ≤ 40% |
| SM-M05 | Product review rate | ≥ 5% | ≥ 10% | ≥ 15% |

### Professional Services

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-S01 | Service providers listed | 20 | 100 | 500 |
| SM-S02 | Service inquiries / month | 50 | 500 | 2,000 |
| SM-S03 | Inquiry-to-booking conversion | ≥ 20% | ≥ 25% | ≥ 30% |
| SM-S04 | Service completion rate | ≥ 80% | ≥ 85% | ≥ 90% |

### Insurance Marketplace

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-I01 | Insurance products listed | 20 | 50 | 100 |
| SM-I02 | Quote inquiries / month | 100 | 1,000 | 5,000 |
| SM-I03 | Inquiry-to-policy conversion | ≥ 5% | ≥ 8% | ≥ 10% |
| SM-I04 | Partner insurers onboarded | 2 | 5 | 10 |

### Travel & Hospitality

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-T01 | Travel listings active | 30 | 150 | 500 |
| SM-T02 | Bookings / month | 50 | 500 | 2,000 |
| SM-T03 | Booking confirmation rate | ≥ 85% | ≥ 90% | ≥ 95% |
| SM-T04 | Average booking value (INR) | ₹3,000 | ₹5,000 | ₹8,000 |

### Digital Services & Products

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-D01 | Digital products listed | 20 | 100 | 500 |
| SM-D02 | Digital downloads / month | 50 | 500 | 2,000 |
| SM-D03 | Active memberships | 20 | 200 | 1,000 |
| SM-D04 | Digital delivery success rate | ≥ 99% | ≥ 99.5% | ≥ 99.9% |

---

## Portal KPIs

### Customer Portal

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-C01 | Customer registration completion rate | ≥ 70% | ≥ 80% | ≥ 85% |
| SM-C02 | Repeat purchase rate (30-day) | ≥ 10% | ≥ 15% | ≥ 25% |
| SM-C03 | Customer portal daily active users | 50 | 500 | 2,500 |
| SM-C04 | Wallet adoption rate | ≥ 5% | ≥ 10% | ≥ 15% |

### Vendor Portal

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-V01 | Vendor onboarding completion rate | ≥ 60% | ≥ 75% | ≥ 85% |
| SM-V02 | Vendor monthly active rate | ≥ 50% | ≥ 60% | ≥ 70% |
| SM-V03 | Average vendor response time (orders) | ≤ 24h | ≤ 12h | ≤ 6h |
| SM-V04 | Vendor payout success rate | ≥ 98% | ≥ 99% | ≥ 99.5% |

### Admin Portal

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-A01 | Support ticket resolution time (avg) | ≤ 48h | ≤ 24h | ≤ 12h |
| SM-A02 | CMS content pages published | 20 | 50 | 100 |
| SM-A03 | CRM ticket resolution rate | ≥ 80% | ≥ 90% | ≥ 95% |

---

## Technical KPIs

| ID | Metric | Target | Measurement |
|----|--------|--------|-------------|
| SM-T01 | **Page Load Time (LCP)** | ≤ 2.5 seconds (mobile) | Lighthouse / RUM |
| SM-T02 | **API Response Time (p95)** | ≤ 500ms | APM monitoring |
| SM-T03 | **Platform Uptime** | ≥ 99.5% | Infrastructure monitoring |
| SM-T04 | **Error Rate** | ≤ 0.5% of requests | Application monitoring |
| SM-T05 | **SEO Score** | ≥ 90 (Lighthouse) | Lighthouse audit |
| SM-T06 | **Security Vulnerabilities** | Zero critical/high in production | Security scanning |
| SM-T07 | **Deployment Frequency** | ≥ 1 per week (post-launch) | CI/CD metrics |

> Performance targets align with PO-11 (High Performance) and PO-10 (SEO Optimization) from [Project_Objectives.md](Project_Objectives.md).

---

## Business KPIs

| ID | Metric | Launch | 6-Month | 12-Month |
|----|--------|--------|---------|----------|
| SM-B01 | **Monthly GMV (INR)** | ₹5L | ₹50L | ₹5Cr |
| SM-B02 | **Platform Revenue (INR)** | ₹25K | ₹2.5L | ₹25L |
| SM-B03 | **Customer Acquisition Cost (INR)** | ≤ ₹200 | ≤ ₹150 | ≤ ₹100 |
| SM-B04 | **Vendor Retention Rate (monthly)** | ≥ 70% | ≥ 80% | ≥ 85% |
| SM-B05 | **Organic Traffic %** | ≥ 20% | ≥ 30% | ≥ 40% |

> Revenue targets are **proposed estimates** and require validation with the project owner.

---

## Metric Definitions & Targets

### Gross Merchandise Value (GMV)

**Definition:** Total transaction value of all completed orders, bookings, and service engagements on the platform before returns and cancellations.

**Formula:** `GMV = Σ (order value) for all completed transactions in period`

**Excludes:** Cancelled orders, refunded amounts, insurance lead inquiries (not converted)

### Payment Success Rate

**Definition:** Percentage of payment attempts that result in successful transaction completion.

**Formula:** `Payment Success Rate = (Successful Payments / Total Payment Attempts) × 100`

### Search Conversion Rate

**Definition:** Percentage of search sessions that result in a purchase, booking, or inquiry.

**Formula:** `Search Conversion = (Conversions from Search / Total Search Sessions) × 100`

### Platform Trust Score

**Definition:** Average rating (1–5 stars) across all customer reviews on the platform.

**Formula:** `Trust Score = Σ (review rating) / Total Reviews`

---

## Measurement Tools (Proposed)

| Category | Tool (Proposed) | Metrics Covered |
|----------|-----------------|-----------------|
| Web Analytics | Google Analytics 4 / Plausible | Traffic, conversion, mobile % |
| Application Performance | Azure Application Insights / Datadog | API response, error rate, uptime |
| SEO | Google Search Console, Lighthouse | Organic traffic, SEO score |
| Payments | Razorpay Dashboard | Payment success rate, GMV |
| CRM | Admin Portal CRM module | Ticket resolution, support metrics |
| Business Intelligence | Admin Portal Reports module | GMV, revenue, vendor metrics |

> Tool selection is proposed and will be finalized during Phase 2 (Architecture).

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [Business_Goals.md](Business_Goals.md) | Goals that metrics measure |
| [Project_Objectives.md](Project_Objectives.md) | Objectives that metrics validate |
| [Project_Roadmap.md](Project_Roadmap.md) | Timeline for achieving targets |
| [Project_Scope.md](Project_Scope.md) | Scope that metrics cover |
| [Target_Audience.md](Target_Audience.md) | Audience segments measured |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 0 release |
