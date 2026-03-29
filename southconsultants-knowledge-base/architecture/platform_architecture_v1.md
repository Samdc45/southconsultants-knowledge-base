# South Consultants — Platform Architecture
**Version:** 1.0  
**Date:** 29 March 2026  
**Status:** Approved — Living Document (updates continuously as products develop)  
**Prepared by:** Penelope, South Consultants AI  

---

## The Vision

South Consultants builds the intelligence layer for the global civil construction industry. Every product is built on a single compounding idea: knowledge, communicated clearly and built into smart systems, creates safe sites and efficient operations.

The ecosystem is not a collection of standalone apps. It is a connected platform where each product feeds data into a central intelligence engine — the whole becoming exponentially more valuable than the sum of its parts.

**Knowledge + Communication + Systems = Safety**

---

## Product Ecosystem

### The Two Delivery Platforms

| | SiteMate | SiteGuard (via CivilApp) |
|---|---|---|
| **Layer** | The Human Layer | The Machine / Tech Layer |
| **Focus** | People & Learning | Technology & Site Intelligence |
| **Goal** | Happy, informed, safe people | Smart, efficient, safe operations |
| **Status** | Active | In Development — Waitlist Open |
| **Delivery** | Mobile-first (iOS & Android) | CivilApp — Base44 (ID: 69c1bfaee2b0e16e430da777) |

**SiteMate features:** Digital site inductions · Real-time hazard reporting · Toolbox talk management · Compliance dashboards · Incident tracking · Mobile-first

**SiteGuard/CivilApp features:** AI utility strike prevention · Geofencing & exclusion zones · Autonomous machinery monitoring · Real-time AI safety alerts · Remote override · Incident prevention log

### The Tagline Maps to the Platforms
- **Smarter Operations** = CivilApp / SiteGuard (tech layer)
- **Safer Sites** = SiteMate (people layer)

---

### Supporting Products

**TruPeg** — AR Site Set-Out & Survey (In Development)
- iPhone + GNSS RTK base station (Emlid Reach RS3 — V1)
- QR-tagged 3D printed set-out rings
- ±10mm survey-grade accuracy
- ARKit confirmation overlay
- VMarker: NZTA M12-compliant road stud with NTAG216 NFC + QR laser etch
- Permanent scannable as-built datum for future crews
- Status: iOS Swift code in development. Rename Vsite→TruPeg in progress (plan documented by Hugo)

**Civil App LMS** — Training & Course Delivery (Active)
- 9 courses, 104+ lessons
- 5 countries: NZ, AU, PH, CA, USA
- Live at: https://south-lms-production.up.railway.app
- Gumroad storefront: southsam.gumroad.com

**Knowledge Hub** — Intelligence Engine (Concept — Priority IP)
- Sits under all products
- Ingests all site data
- Generates training content, hazard alerts, workflow triggers
- The company moat — not for external release

---

## System Architecture — Layered Stack

```
┌─────────────────────────────────────────────────────────────┐
│  LAYER 4: INTELLIGENCE — Knowledge Hub                      │
│  Ingests all data · Generates prompts · Automates workflows │
│  The compounding moat. Gets smarter every site day.         │
└─────────────────────────────────────────────────────────────┘
                              ↑
┌─────────────────────────────────────────────────────────────┐
│  LAYER 3: CLOUD BACKEND                                     │
│  Railway (Docker: mass161/south-lms:latest)                 │
│  Base44 (CivilApp/SiteGuard · SiteMate · Agent Team)        │
│  API: south-lms-production.up.railway.app                   │
└─────────────────────────────────────────────────────────────┘
                              ↑
┌─────────────────────────────────────────────────────────────┐
│  LAYER 2: APPLICATIONS                                      │
│  SiteMate (mobile — people layer)                           │
│  CivilApp/SiteGuard (web + mobile — tech layer)             │
│  TruPeg (iOS AR — site set-out)                             │
│  Civil App LMS (web — training delivery)                    │
└─────────────────────────────────────────────────────────────┘
                              ↑
┌─────────────────────────────────────────────────────────────┐
│  LAYER 1: SITE / HARDWARE                                   │
│  GNSS RTK Base Station (Emlid Reach RS3)                    │
│  QR-Tagged 3D Printed Set-Out Rings                         │
│  VMarker (NZTA M12 + NTAG216 NFC + QR)                      │
│  Site sensors & autonomous machinery (SiteGuard)            │
└─────────────────────────────────────────────────────────────┘
```

---

## Data Flow

| Platform | Flow |
|---|---|
| **SiteMate** | Worker scans in → induction → hazard logged → compliance dashboard updates → incident logged → feeds Knowledge Hub |
| **CivilApp/SiteGuard** | Machine enters geofence → AI detects utility proximity → alert issued → override available → prevented → logged → feeds Hub |
| **TruPeg** | Base placed → phone calibrated → QR ring scanned → AR confirms ±10mm → upload to project → as-built record → VMarker installed → permanent datum |
| **Civil App LMS** | Hub generates content → LMS delivers → competency recorded → feeds back as verified knowledge |
| **Knowledge Hub** | All data ingested → patterns identified → alerts generated → training updated → moat deepens |

---

## Technology Stack

| Component | Technology | Status | Notes |
|---|---|---|---|
| iOS App (TruPeg) | Swift / Xcode / ARKit | In Development | Rename Vsite→TruPeg — Hugo plan documented |
| GNSS Hardware | Emlid Reach RS3 | V1 Specified | V2: proprietary u-blox base station |
| Backend API | Docker mass161/south-lms:latest | Live on Railway | south-lms-production.up.railway.app |
| LMS Platform | Custom LMS + Gumroad | Live | 9 courses · 5 countries |
| CivilApp/SiteGuard | Base44 | In Development | App ID: 69c1bfaee2b0e16e430da777 |
| SiteMate | Base44 | Active | Entities: Hazard, ToolboxTalk, CheckIn, Induction, SiteCheck |
| AI Agent Team | Base44 Agents | Active | Penelope · Hugo · Lisa |
| Payments | Stripe + Gumroad | Test/Live | southsam.gumroad.com |
| Website | Vercel (HTML/CSS/JS) | Live | southconsultants-website.vercel.app |
| Domain | Cloudflare → Vercel | Migrating | From Wix · Auth code expires 2026-04-02 — URGENT |
| VMarker NFC | NTAG216 (ISO 14443-3A) | Prototype Stage | 100-unit ~NZD $2,020 · 5–6 weeks |
| Knowledge Hub | TBD | Concept | Core IP — not for external release |

---

## Strategic Roadmap

| Phase | Timeline | Focus |
|---|---|---|
| **Phase 1** | Now | SiteMate live · Civil App LMS live · TruPeg in dev · SiteGuard waitlist · AI team operational |
| **Phase 2** | Q2–Q3 2026 | TruPeg App Store release · VMarker 100-unit prototype · SiteGuard beta · NZ provisional patent filed |
| **Phase 3** | Q4 2026 | SiteGuard GA · TruPeg commercial · Knowledge Hub MVP · 15+ courses · AU market entry |
| **Phase 4** | Y2–Y3 | Knowledge Hub operational · SE Asia + Middle East · Autonomous machinery · Global data moat |

---

## AI Agent Team

| Agent | Role | Responsibilities |
|---|---|---|
| **Penelope** | Lead PA & Orchestrator | Strategy · App building · Team coordination · Integrations · NEVER publishes without Sam's approval |
| **Hugo** | Research & Code Review | Deep research · Competitive analysis · Manufacturer contacts · Code review · Patent landscape |
| **Lisa** | Course Content Builder | All course content · Lesson frameworks · Personality-type pedagogy · Civil App LMS builds |

---

## Brand

- **Tagline:** Smarter Operations. Safer Sites. *(THIS ORDER. ALWAYS.)*
- **Philosophy:** Knowledge + Communication + Systems = Safety
- **Heritage:** Plan. Efficient. Safe.
- **Colours:** Navy #1a2744 · Orange #e8634a
- **Reach:** NZ · AU · PH · CA · USA

---

*South Consultants · sam@southconsultants.biz · southconsultants.biz*  
*PDF version: https://base44.app/api/apps/69c4b8fd6141e7261bf847fc/files/mp/public/69c4b8fd6141e7261bf847fc/99efe023a_SouthConsultants_Architecture_2026-03-29.pdf*
