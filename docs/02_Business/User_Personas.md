# User Personas

> **Version:** 1.0  
> **Status:** Draft  
> **Last Updated:** July 2026  
> **Document Owner:** Product Architecture  
> **Parent Document:** [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md)

---

## Purpose

This document defines **detailed user personas** for EcomHub Enterprise across customer, vendor, and admin user types. Personas drive product design, feature prioritization, marketing messaging, and user journey mapping.

Phase 0 audience segments are defined in [docs/01_Project/Target_Audience.md](../01_Project/Target_Audience.md). This document expands those segments into actionable personas.

User journeys are documented in [User_Journey.md](User_Journey.md).

---

## Table of Contents

1. [Persona Overview](#persona-overview)
2. [Customer Personas](#customer-personas)
3. [Vendor Personas](#vendor-personas)
4. [Admin Personas](#admin-personas)
5. [Persona-Vertical Matrix](#persona-vertical-matrix)
6. [Persona Priority Matrix](#persona-priority-matrix)
7. [Related Documents](#related-documents)

---

## Persona Overview

EcomHub Enterprise serves **13 primary personas** across three user groups:

| Group | Personas | Count |
|-------|----------|-------|
| **Customer** | Buyer, Traveller, Service Customer, Insurance Customer | 4 |
| **Vendor** | Product Seller, Service Provider, Hotel Owner, Houseboat Owner, Taxi Operator | 5 |
| **Admin** | Platform Admin, Finance Admin, Support Admin | 3 |
| **Guest** | Unauthenticated browser (referenced, not detailed) | 1 |

---

## Customer Personas

### CP-01: Buyer

**Name:** Aisha Khan  
**Archetype:** The Regional Product Shopper  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 28–45 |
| Gender | Female |
| Location | Delhi, Mumbai, Bangalore (metro cities) |
| Occupation | Working professional, homemaker |
| Income | ₹8–25 LPA household |
| Education | Graduate or post-graduate |
| Tech Proficiency | High — daily smartphone user |
| Device | Android smartphone (primary), occasional laptop |

#### Goals

- Purchase authentic Kashmiri products (Pashmina, saffron, dry fruits, honey, ghee, handicrafts)
- Verify product authenticity before buying
- Get reliable pan-India delivery with tracking
- Find competitive pricing with quality assurance

#### Behaviors

- Researches products via Google and social media before purchasing
- Reads customer reviews and ratings carefully
- Compares prices across platforms but prioritizes authenticity over lowest price
- Uses UPI as primary payment method; selects COD for high-value first purchases
- Adds products to wishlist for later purchase during sales or festivals
- Shops more during festivals (Eid, Diwali, weddings) and winter (Pashmina season)

#### Pain Points

- Cannot distinguish authentic Pashmina from machine-made imitations online
- Previous bad experiences with fake saffron from unverified sellers
- High shipping costs and unreliable delivery for Kashmir products
- No single trusted platform for all Kashmiri specialties

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Authenticity verification | Verified vendor badges, GI tagging, review system |
| Product discovery | Categories, search, filters, wishlist |
| Trust | Reviews, ratings, vendor profiles, return policy |
| Payment flexibility | UPI, COD, cards |
| Order tracking | Real-time delivery status in customer portal |

#### Quote

> *"I want to buy real Kashmiri saffron for my family, but I don't know which online seller to trust. If EcomHub verifies the sellers, I'll buy everything from there."*

---

### CP-02: Traveller

**Name:** Arjun Mehta  
**Archetype:** The Experience Seeker  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 25–35 |
| Gender | Male |
| Location | Pan-India (planning Kashmir trip from any city) |
| Occupation | IT professional, entrepreneur |
| Income | ₹10–20 LPA |
| Education | Graduate |
| Tech Proficiency | High |
| Device | Android/iPhone smartphone |

#### Goals

- Plan a complete Kashmir vacation from one platform
- Book houseboat stay on Dal Lake
- Arrange hotel, taxi, and local tour activities
- Read reviews from other travelers before booking
- Get transparent pricing with no hidden charges

#### Behaviors

- Plans trips 2–4 weeks in advance
- Reads travel blogs, Instagram, and YouTube for Kashmir inspiration
- Compares houseboat and hotel options by price, location, and reviews
- Books taxi and activities after confirming accommodation
- Shares travel experiences on social media after the trip
- Prefers online payment (UPI/cards) for advance bookings

#### Pain Points

- Must use 3–4 different websites/apps for houseboat, hotel, taxi, and activities
- Unclear pricing on local travel sites; hidden charges at checkout
- Difficulty verifying houseboat quality from photos alone
- No unified booking confirmation or itinerary management

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Unified travel booking | All travel categories in one platform |
| Reviews and photos | Traveler reviews, verified photos, ratings |
| Transparent pricing | Full price displayed before booking |
| Itinerary management | All bookings visible in customer portal |
| Local experiences | Curated activities and experiences in Kashmir |

#### Quote

> *"I'm planning my first Kashmir trip. I wish I could book the houseboat, taxi, and activities all in one place instead of calling five different people."*

---

### CP-03: Service Customer

**Name:** Rajesh Gupta  
**Archetype:** The SMB Service Seeker  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 30–50 |
| Gender | Male |
| Location | Jammu, Srinagar, Delhi, Tier 1/2 cities |
| Occupation | Small business owner (retail, trading, services) |
| Income | ₹5–15 LPA |
| Education | Graduate |
| Tech Proficiency | Medium — uses smartphone for business |
| Device | Android smartphone |

#### Goals

- Find reliable CA for GST filing and ITR filing
- Get legal consultation for business compliance
- Hire business consultant for growth strategy
- Compare service providers by qualification, price, and reviews
- Track service progress after booking

#### Behaviors

- Searches for services when compliance deadlines approach (GST quarterly, ITR July)
- Asks for referrals from business network before trying online platforms
- Values provider credentials (CA number, bar council registration) over price
- Prefers fixed-price services over hourly billing
- Needs document sharing capability for tax and legal work

#### Pain Points

- Finds CA/legal services through word-of-mouth only — limited options
- No way to compare service provider credentials and pricing online
- Unclear service scope and deliverables before engagement
- Difficulty tracking service progress after hiring

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Verified providers | Credential display, verification badges |
| Service comparison | Side-by-side provider profiles with pricing |
| Booking and tracking | Inquiry, booking, status tracking in portal |
| Document sharing | Secure upload/download for tax and legal documents |
| Reviews | Ratings from other business customers |

#### Quote

> *"Every quarter I scramble to find someone for GST filing. If I could find a verified CA on EcomHub with reviews from other business owners, that would save me so much stress."*

---

### CP-04: Insurance Customer

**Name:** Priya Sharma  
**Archetype:** The Informed Insurance Buyer  
**Priority:** Secondary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 25–40 |
| Gender | Female |
| Location | Pan-India |
| Occupation | Salaried professional, government employee |
| Income | ₹6–18 LPA |
| Education | Graduate or post-graduate |
| Tech Proficiency | Medium–High |
| Device | Android smartphone |

#### Goals

- Compare health insurance plans for family coverage
- Find affordable car/bike insurance with good claim settlement
- Purchase travel insurance for Kashmir trip
- Understand policy terms before buying
- Store policy documents in one accessible place

#### Behaviors

- Researches insurance online but finds insurer websites confusing
- Compares 3–5 plans before deciding
- Values claim settlement ratio and network hospital coverage
- Reads policy exclusions carefully
- Renews motor insurance annually — price-sensitive
- Prefers online payment for instant policy issuance

#### Pain Points

- Too many insurer websites with different formats and jargon
- Agents push products with high commissions, not best fit
- Difficulty comparing plans side-by-side
- Policy documents scattered across emails and physical files

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Plan comparison | Side-by-side comparison by type, coverage, premium |
| Clear information | Policy terms, exclusions, claim process displayed |
| Trusted partners | IRDAI-licensed insurers only |
| Policy storage | Digital policy documents in customer portal |
| Travel insurance | Quick purchase for trip-specific coverage |

#### Quote

> *"I spent three hours comparing health insurance plans on different websites. If EcomHub showed them all in one place with clear comparisons, I'd buy today."*

---

## Vendor Personas

### VP-01: Product Seller

**Name:** Gulzar Ahmed  
**Archetype:** The Kashmiri Artisan-Entrepreneur  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 35–55 |
| Location | Srinagar, J&K |
| Business | Pashmina and handicraft production and retail |
| Business Size | Micro — 2–5 employees, family-operated |
| Revenue | ₹5–20 LPA |
| Tech Proficiency | Low–Medium — uses WhatsApp Business, basic smartphone |
| Device | Android smartphone |

#### Goals

- Sell authentic handmade Pashmina and handicrafts directly to national buyers
- Eliminate middlemen who take 40–60% margin
- Manage orders and inventory from phone
- Receive timely payments without chasing buyers
- Build online reputation through customer reviews

#### Behaviors

- Currently sells through local shops, exhibitions, and WhatsApp orders
- Takes product photos on smartphone; needs simple upload process
- Checks orders once or twice daily
- Prefers COD settlement tracking over complex financial dashboards
- Values personal relationship with customers but wants scale

#### Pain Points

- No online storefront — depends on middlemen and word-of-mouth
- Cannot reach customers outside Kashmir
- No inventory management tools — tracks stock manually
- Payment delays from wholesale buyers
- Fear of technology complexity

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Simple listing | Easy product upload with photos from phone |
| Order notifications | SMS/app notification for new orders |
| Simple fulfillment | Mark order shipped with tracking number |
| Payout visibility | Clear payout schedule and history |
| Minimal complexity | Intuitive vendor portal, minimal training needed |

#### Quote

> *"I make the finest Pashmina shawls in Srinagar, but customers in Delhi and Mumbai never find me. If EcomHub helps me sell directly, I'll list my entire catalog."*

---

### VP-02: Service Provider

**Name:** Advocate Meera Sharma  
**Archetype:** The Professional Service Expert  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 35–50 |
| Location | Jammu / Srinagar / Delhi |
| Business | Legal practice and GST/ITR consultancy |
| Business Size | Solo or small firm (1–3 professionals) |
| Revenue | ₹8–30 LPA |
| Tech Proficiency | Medium |
| Device | Laptop + smartphone |

#### Goals

- Acquire new clients through online discovery
- Display qualifications and specializations prominently
- Manage client inquiries and service orders efficiently
- Receive secure document uploads from clients
- Build professional reputation through client reviews

#### Behaviors

- Gets most clients through referrals currently
- Maintains professional profiles on LinkedIn
- Responds to inquiries within 24 hours
- Offers fixed-price packages for GST filing and ITR
- Needs secure document exchange for client confidentiality

#### Pain Points

- Limited online presence beyond LinkedIn
- No platform to showcase services with pricing and reviews
- Client acquisition depends entirely on network
- Manual tracking of service orders and deliverables

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Professional profile | Credentials, specializations, experience display |
| Inquiry management | Receive, respond, and convert inquiries |
| Service listing | Package-based service offerings with pricing |
| Document exchange | Secure upload/download with clients |
| Review building | Client reviews after service completion |

#### Quote

> *"I'm a qualified CA with 15 years of experience, but my clients find me only through referrals. An EcomHub profile with my credentials and client reviews would bring me new business."*

---

### VP-03: Hotel Owner

**Name:** Imran Dar  
**Archetype:** The Hospitality Operator  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 40–55 |
| Location | Srinagar, Pahalgam, Gulmarg (J&K) |
| Business | 15–30 room hotel / guest house |
| Business Size | Small — 5–15 staff |
| Revenue | ₹30–80 LPA (seasonal) |
| Tech Proficiency | Medium |
| Device | Smartphone + laptop |

#### Goals

- Increase direct bookings and reduce OTA commission (15–25%)
- Manage room availability and pricing across seasons
- Showcase hotel with quality photos and amenities
- Receive booking notifications and manage confirmations
- Build reputation through guest reviews

#### Behaviors

- Currently lists on MakeMyTrip, Goibibo with high commissions
- Manages availability manually or through OTA extranet
- Seasonal business — peak Apr–Oct, low Nov–Mar
- Adjusts pricing based on season and occupancy
- Values direct customer relationship for repeat bookings

#### Pain Points

- OTA commissions eat 15–25% of booking value
- No direct booking channel with own branding
- Double-booking risks with manual availability management
- Cannot differentiate from competitors on OTA platforms

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Direct booking channel | Lower commission than OTAs |
| Availability calendar | Room availability management by date |
| Photo gallery | Multiple photos, amenities list, location map |
| Booking management | Confirm, modify, cancel bookings |
| Seasonal pricing | Different rates for peak/off-peak seasons |

#### Quote

> *"MakeMyTrip takes 20% of every booking. If EcomHub gives me direct bookings at 10% commission with my own hotel page, I'll switch half my inventory here."*

---

### VP-04: Houseboat Owner

**Name:** Abdul Rahman  
**Archetype:** The Heritage Experience Provider  
**Priority:** Primary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 45–60 |
| Location | Dal Lake / Nigeen Lake, Srinagar |
| Business | Traditional houseboat (1–3 houseboats) |
| Business Size | Family-operated, 2–4 staff per houseboat |
| Revenue | ₹10–40 LPA (highly seasonal) |
| Tech Proficiency | Low |
| Device | Android smartphone |

#### Goals

- Fill houseboat bookings during tourist season (Apr–Oct)
- Showcase houseboat heritage, decor, and lake experience
- Manage bookings without double-booking
- Receive fair payment without agent intermediaries
- Get reviews from national and international guests

#### Behaviors

- Currently gets bookings through travel agents (30–40% commission)
- Lists on 1–2 OTAs reluctantly due to high fees
- Manages availability verbally or via WhatsApp
- Peak season fully booked by May; struggles with off-season
- Takes photos of houseboat but needs help with online presentation

#### Pain Points

- Travel agents take 30–40% commission on houseboat bookings
- No direct online presence — invisible to independent travelers
- Cannot manage availability digitally — double-booking risks
- Low tech comfort — needs extremely simple tools

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Simple listing | Houseboat photos, amenities, pricing per night |
| Booking calendar | Visual calendar showing booked/available dates |
| Direct bookings | Reach travelers without agent intermediaries |
| Easy management | Minimal clicks to confirm/manage bookings |
| Phone-friendly portal | Full functionality on smartphone |

#### Quote

> *"Travel agents take half my earnings. If tourists could book my houseboat directly on EcomHub, I'd give them the best rate and best experience."*

---

### VP-05: Taxi Operator

**Name:** Farooq Ahmad  
**Archetype:** The Local Transport Provider  
**Priority:** Secondary — Launch

#### Demographics

| Attribute | Detail |
|-----------|--------|
| Age | 30–45 |
| Location | Srinagar, J&K |
| Business | Taxi/cab service (1–5 vehicles) |
| Business Size | Micro — owner-driver or small fleet |
| Revenue | ₹4–12 LPA |
| Tech Proficiency | Low–Medium |
| Device | Android smartphone |

#### Goals

- Get airport pickup and local sightseeing bookings from tourists
- Display fare structure transparently
- Manage booking requests and schedule efficiently
- Build reputation through customer reviews
- Reduce dependency on hotel concierges for referrals

#### Behaviors

- Gets most business through hotel referrals and airport queue
- Uses WhatsApp for booking coordination
- Offers fixed fares for airport transfers and day sightseeing packages
- Available 6 AM – 10 PM during tourist season
- Prefers cash payments but accepts UPI

#### Pain Points

- No online presence — invisible to tourists planning ahead
- Unpredictable income — depends on being at the right place
- Hotel concierges take referral cuts
- No way to receive advance bookings from arriving tourists

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Service listing | Vehicle type, capacity, fare structure |
| Advance bookings | Tourists book airport pickup before arrival |
| Booking notifications | Instant notification of new booking requests |
| Route packages | Pre-defined packages (airport, Gulmarg day trip, etc.) |
| Simple interface | Easy to use on smartphone while driving |

#### Quote

> *"Tourists land at Srinagar airport and don't know who to call for a taxi. If they could book me on EcomHub before they arrive, I'd get steady business all season."*

---

## Admin Personas

### AP-01: Platform Admin

**Name:** Admin User (Platform Operations)  
**Archetype:** The Platform Governor  
**Priority:** Primary — Launch

#### Role

| Attribute | Detail |
|-----------|--------|
| Title | Platform Administrator |
| Department | Operations |
| Access Level | Full admin portal access with RBAC |
| Team Size | 2–5 platform admins at launch |

#### Responsibilities

- Vendor registration review and approval/rejection
- Platform content management (CMS — pages, banners, SEO)
- Marketing campaign creation and coupon management
- Platform configuration and settings management
- User role and permission management (RBAC)
- Audit log review and compliance monitoring
- Report generation and KPI monitoring

#### Goals

- Maintain platform quality through vendor verification
- Ensure content is accurate, current, and SEO-optimized
- Monitor platform health via dashboard KPIs
- Manage marketing promotions to drive growth
- Enforce platform policies consistently

#### Daily Activities

| Activity | Frequency |
|----------|-----------|
| Review vendor registration applications | Daily |
| Monitor dashboard KPIs | Daily |
| Update CMS content (banners, pages) | Weekly |
| Create/manage marketing promotions | Weekly |
| Review audit logs | Daily |
| Generate operational reports | Weekly |

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Vendor management | Approval workflow, vendor search, status management |
| Dashboard | Real-time KPIs across all verticals |
| CMS | Page editor, banner management, SEO tools |
| RBAC | Role creation, permission assignment |
| Audit logs | Searchable, filterable action history |

---

### AP-02: Finance Admin

**Name:** Finance Manager (Platform Finance)  
**Archetype:** The Financial Controller  
**Priority:** Primary — Launch

#### Role

| Attribute | Detail |
|-----------|--------|
| Title | Finance Administrator |
| Department | Finance |
| Access Level | Finance module + reports + audit logs |
| Team Size | 1–2 finance admins at launch |

#### Responsibilities

- Vendor payout processing and scheduling
- Payment reconciliation with Razorpay
- Commission calculation verification
- Financial report generation (revenue, GMV, payouts)
- Refund processing and approval
- GST reporting and tax compliance
- COD collection tracking and reconciliation

#### Goals

- Ensure accurate and timely vendor payouts
- Maintain zero discrepancy in payment reconciliation
- Generate accurate financial reports for leadership
- Comply with GST and tax regulations
- Minimize payment-related disputes

#### Daily Activities

| Activity | Frequency |
|----------|-----------|
| Process scheduled vendor payouts | Weekly (payout cycle) |
| Reconcile Razorpay transactions | Daily |
| Review and approve refunds | Daily |
| Generate financial reports | Weekly |
| Verify commission calculations | Per payout cycle |
| Track COD collections | Daily |

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| Payout management | Schedule, process, track vendor payouts |
| Reconciliation | Razorpay transaction matching |
| Commission reports | Per-vendor, per-vertical commission breakdown |
| Refund workflow | Approve/process refunds with audit trail |
| GST reports | Tax collection and liability reports |
| Export | CSV/Excel export for accounting systems |

---

### AP-03: Support Admin

**Name:** Support Lead (Customer & Vendor Support)  
**Archetype:** The Resolution Specialist  
**Priority:** Primary — Launch

#### Role

| Attribute | Detail |
|-----------|--------|
| Title | Support Administrator |
| Department | Customer Support |
| Access Level | CRM module + order lookup + limited admin |
| Team Size | 2–4 support agents at launch |

#### Responsibilities

- Customer support ticket management and resolution
- Vendor support inquiries
- Dispute management (refunds, returns, booking cancellations)
- Order and booking status lookup for customer inquiries
- Escalation to Platform Admin for policy exceptions
- Support quality monitoring and response time tracking

#### Goals

- Resolve customer issues within 24 hours
- Maintain customer satisfaction score ≥ 4.0
- Handle disputes fairly with clear documentation
- Reduce repeat tickets through root cause identification
- Support both customers and vendors effectively

#### Daily Activities

| Activity | Frequency |
|----------|-----------|
| Triage and respond to new tickets | Continuous |
| Investigate order/booking issues | Per ticket |
| Process refund requests | Per ticket |
| Communicate resolution to customer/vendor | Per ticket |
| Escalate complex disputes to Platform Admin | As needed |
| Review ticket metrics and trends | Daily |

#### Needs from EcomHub

| Need | Platform Feature |
|------|-----------------|
| CRM ticketing | Create, assign, track, resolve tickets |
| Order lookup | Search orders/bookings by ID, customer, vendor |
| Customer history | View customer order history and past tickets |
| Refund initiation | Initiate refunds from ticket interface |
| Canned responses | Templates for common support scenarios |
| Escalation workflow | Route complex issues to Platform Admin |

---

## Persona-Vertical Matrix

| Persona | Marketplace | Services | Insurance | Travel | Digital |
|---------|-------------|----------|-----------|--------|---------|
| **Buyer (CP-01)** | ✅ Primary | — | — | — | — |
| **Traveller (CP-02)** | — | — | ✅ Travel insurance | ✅ Primary | — |
| **Service Customer (CP-03)** | — | ✅ Primary | — | — | — |
| **Insurance Customer (CP-04)** | — | — | ✅ Primary | ✅ Travel | — |
| **Product Seller (VP-01)** | ✅ Primary | — | — | — | — |
| **Service Provider (VP-02)** | — | ✅ Primary | — | — | ✅ Possible |
| **Hotel Owner (VP-03)** | — | — | — | ✅ Primary | — |
| **Houseboat Owner (VP-04)** | — | — | — | ✅ Primary | — |
| **Taxi Operator (VP-05)** | — | — | — | ✅ Primary | — |

---

## Persona Priority Matrix

| Priority | Personas | Rationale |
|----------|----------|-----------|
| **P0 — Launch Critical** | Buyer, Product Seller, Platform Admin, Finance Admin, Support Admin | Core marketplace loop + operations |
| **P1 — Launch Important** | Traveller, Houseboat Owner, Hotel Owner, Service Customer, Service Provider | Key differentiators for J&K launch |
| **P2 — Launch Secondary** | Insurance Customer, Taxi Operator | Important but lower initial volume |

---

## Related Documents

| Document | Purpose |
|----------|---------|
| [MASTER_PROJECT_BIBLE.md](../../MASTER_PROJECT_BIBLE.md) | Single source of truth |
| [User_Journey.md](User_Journey.md) | Persona-driven user journeys |
| [Business_Requirements_Document.md](Business_Requirements_Document.md) | Business requirements |
| [Market_Strategy.md](Market_Strategy.md) | Acquisition strategy per persona |
| [docs/01_Project/Target_Audience.md](../01_Project/Target_Audience.md) | Phase 0 audience segments |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | July 2026 | Product Architecture | Initial Phase 1 release |
