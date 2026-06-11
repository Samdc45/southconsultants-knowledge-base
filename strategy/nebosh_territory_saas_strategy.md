# South Consultants — NEBOSH + Territory Overlay SaaS Strategy
**Date:** 2026-06-11  
**Status:** Strategic — SaaS product development roadmap

---

## The Concept

Build a territory-aware civil construction H&S training SaaS platform:

- **Core layer** = NEBOSH IGC-aligned content (globally portable, internationally credentialed)
- **Territory overlay layer** = jurisdiction-specific legislation, forms, and compliance references — activates based on the learner's or company's country/region
- **Outcome** = one platform that works for a NZ contractor, Canadian PCBU, UAE developer, and US general contractor — each sees content relevant to their regulatory environment, all working toward NEBOSH IGC

No existing LMS does this specifically for civil construction. This is SC's global differentiator.

---

## Product Architecture

```
┌─────────────────────────────────────────────────────────┐
│               SC Civil Training Platform                │
├─────────────────────────────────────────────────────────┤
│  GLOBAL CORE (NEBOSH IGC-aligned, always present)       │
│  GIC1: Management | GIC2: Hazards | Risk Assessment     │
├─────────────────────────────────────────────────────────┤
│  TERRITORY OVERLAY (selected at org/learner level)      │
│  NZ  │  AU  │  UK  │  Canada  │  US  │  UAE  │  EU     │
├─────────────────────────────────────────────────────────┤
│  CIVIL SPECIALISATION (SC's existing content)           │
│  Excavation │ Lifting │ Utility Strike │ Compaction…    │
└─────────────────────────────────────────────────────────┘
```

Every course = 3 layers:
- Global module (NEBOSH-aligned)
- Territory module (local legislation reference, local forms, local regulator, local compliance checklist)
- Civil specialisation (SC's technical depth)

**Revenue:** License per seat (SaaS). Each territory = additional module pack. White-label for large contractors or territory resellers.

---

## Territory Overlay Map

---

### NEW ZEALAND (SC Home Territory)

**Regulator:** WorkSafe New Zealand  
**Primary law:** Health and Safety at Work Act 2015 (HSWA)  
**Key regs:**
- H&SW (General Risk and Workplace Management) Regulations 2016
- H&SW (Hazardous Substances) Regulations 2017
- CoPTTM → superseded by NZGTTM (from Nov 2024)

**Overlay modules:**
- PCBU concept (Person Conducting Business or Undertaking) — replaces "employer"
- Notifiable events — WorkSafe notification duties (deaths, serious injuries, dangerous incidents)
- Health and Safety Representatives (HSRs) — election rights, powers
- H&S committees — when required (>20 workers)
- Approved Codes of Practice (ACoPs) — safe harbour defence
- ACC system — no-fault injury compensation, return-to-work obligations unique to NZ
- NZGTTM — new traffic management guidelines replacing CoPTTM
- BYDA NZ — Before You Dig utility locate service
- Site Safe NZ — industry body, site safety card scheme
- NZQA unit standards — formal qualification alignment

**NEBOSH crosswalk:** HSWA 2015 maps to ILO C155 (NEBOSH reference). PCBU = duty holder. Risk assessment requirements align with NEBOSH 5-step.

---

### AUSTRALIA

**Regulator:** Safe Work Australia (federal model); state-based enforcement  
**Primary law:** Model WHS Act (all states/territories except Victoria)
- NSW: WHS Act 2011 | QLD: WHS Act 2011 | SA: WHS Act 2012 | WA: WHS Act 2020
- Victoria: Occupational Health and Safety Act 2004 (separate framework)

**2025–26 updates:**
- Model WHS Amendment (Incident Notification) 2025 — expanded notification including extended absences, violent incidents, work-related suicide
- SA: High Risk Construction Work Amendment Regulations 2025 — fall threshold 3m (not 2m), effective 1 July 2026

**Overlay modules:**
- PCBU framework (same as NZ — both based on same model law; low content lift)
- High Risk Work (HRW) licences — mandatory for crane, rigging, dogging, scaffolding, forklift, pressure equipment
- Safe Work Method Statements (SWMS) — required for High Risk Construction Work (HRCW)
- Safety Management Plans — required for notifiable construction work
- Construction Induction Card (White Card) — mandatory nationally, all workers; SC content should support White Card delivery
- Principal Contractor duties — site safety plan, co-ordination
- State-specific differences: SafeWork NSW / WorkSafe QLD / WorkSafe VIC / SafeWork SA / WorkSafe WA
- BYDA Australia — Before You Dig utility locate

**Entry strategy:** Partner with RTOs delivering White Card training; SC civil specialisation is the premium overlay on top.

---

### UNITED KINGDOM

**Regulator:** Health and Safety Executive (HSE)  
**Primary law:** Health and Safety at Work etc. Act 1974  
**Key regulations:**
- Construction (Design and Management) Regulations 2015 (CDM 2015) — most important for civil construction
- Management of H&SW Regulations 1999
- COSHH Regulations 2002
- Work at Height Regulations 2005
- Confined Spaces Regulations 1997
- Control of Noise at Work Regulations 2005
- Control of Vibration at Work Regulations 2005
- RIDDOR 2013 (reporting)
- Electricity at Work Regulations 1989

**Overlay modules:**
- CDM 2015 duty holders: Client, Principal Designer, Principal Contractor, Contractor, Worker
- Construction Phase Plan (CPP) — required on notifiable projects
- Health and Safety File — required on notifiable projects
- RIDDOR — what/how to report: fatalities, specified injuries, over-7-day absence, occupational diseases, dangerous occurrences
- COSHH — Control of Substances Hazardous to Health — WELs, monitoring, medical surveillance
- CSCS Card (Construction Skills Certification Scheme) — mandatory on most UK construction sites
- Workplace Exposure Limits (WELs) — EH40 document

**Why critical:** NEBOSH is a UK body — IGC most recognised in UK-linked markets. Becoming a NEBOSH LP gives direct UK market access. Tyler Baker's NEBOSH knowledge base most directly applicable here.

---

### CANADA (Tyler Baker's Territory)

**Regulator:** Provincial/territorial (94% of workers under provincial jurisdiction)  
**No single national construction standard — province by province:**

| Province | Act | Regulator |
|----------|-----|-----------|
| Ontario | OHSA + O. Reg. 213/91 (Construction Projects) | Ministry of Labour |
| British Columbia | Workers Compensation Act + OHS Regulation Part 20 | WorkSafeBC |
| Alberta | Occupational Health and Safety Act 2018 | Alberta OHS |
| Quebec | Act Respecting OH&S (LSST) | CNESST |
| Federal | Canada Labour Code Part II | ESDC |

**2025–26 updates:**
- Ontario Bill 30 (Working for Workers Seven Act 2025) — new AMP scheme effective Jan 1, 2026
- Ontario O. Reg. 213/91 updated April 2025

**Overlay modules:**
- Ontario: Constructor duties under O. Reg. 213/91; fall protection (3m threshold); Ontario One Call
- BC: WorkSafeBC Part 20 — excavation shoring, fall protection, confined space; OFA First Aid levels 1/2/3
- Alberta: Hazard Assessment, Elimination and Control — written HCS, site orientation
- JHSC (Joint Health and Safety Committee) — required in most provinces for >20 workers
- COR (Certificate of Recognition) — AB, BC, SK — safety management certification for tender pre-qualification
- CRSP (Canadian Registered Safety Professional) — professional designation pathway after NEBOSH IGC
- CCOHS — Canadian Centre for Occupational Health and Safety reference body

**Entry strategy:** Tyler Baker leads Canada territory development. Target IHSA (Ontario), BCCSA (BC), Alberta Safety Codes Council as channel partners.

---

### UNITED STATES (SC's first office expansion)

**Regulator:** OSHA (federal); 22 states have own OSHA-approved state plans  
**Primary law:** Occupational Safety and Health Act 1970  
**Key standard:** 29 CFR Part 1926 — Safety and Health Regulations for Construction

**Key regulations by topic:**
- 1926 Subpart P — Excavations (benching, shoring, soil classification — Class A/B/C)
- 1926 Subpart M — Fall Protection (6-foot threshold in construction)
- 1926 Subpart AA — Confined Spaces in Construction
- 1926 Subpart L — Scaffolding
- 1926 Subpart K — Electrical
- 1926 Subpart Q — Concrete and masonry
- 1926.600–606 — Motor vehicles and mechanised equipment
- 1926.1153 — Silica Rule (critical for civil: action level 25 μg/m³ TWA)
- HAZCOM 1910.1200 — Hazard Communication (GHS labels, Safety Data Sheets)

**Overlay modules:**
- "Competent Person" definition — OSHA-mandated for excavations, fall protection, scaffolding, confined space; authority to correct hazards
- "Qualified Person" — professional credential requirement
- OSHA 300 Log — injury/illness recordkeeping (required >10 workers)
- OSHA 300A — annual summary posted Feb–Apr
- OSHA 10-Hour (worker awareness) vs OSHA 30-Hour (supervisor) — state mandate map
- Cal/OSHA differences — most stringent state plan (relevant for CA market)
- Process Safety Management (PSM) — for sites near major chemical hazards

**Entry strategy:** Align SC content with OSHA 10/30-hour syllabus topics. Position NEBOSH IGC as the internationally recognised equivalent with civil construction depth. Target AGC (Associated General Contractors) chapters and ENR top contractors.

---

### MIDDLE EAST (UAE / Saudi Arabia / Qatar)

**UAE:**
- Abu Dhabi: OSHAD-SF (OHS Management System Framework) — mandatory for all Abu Dhabi government projects; ISO 45001-aligned
- Dubai: Dubai Municipality Construction Safety Code + Roads & Transport Authority
- Federal: Ministry of Human Resources and Emiratisation (MOHRE) — Labour Law Federal Decree No. 33 of 2021
- No single UAE-wide regulator — emirate-by-emirate enforcement

**Saudi Arabia:**
- Ministry of Human Resources and Social Development (MHRSD)
- Vision 2030 mega-projects (NEOM, Red Sea, Qiddiya) — all require international H&S standards
- 2026: Large sites (500+ workers) must have on-site medical clinic
- "Zero-Cost to Worker" rule — PPE costs cannot be deducted from wages
- Integrated Emergency Response Plan mandatory on all large sites

**Qatar:**
- Ministry of Labour
- Worker Welfare Standards mandatory for large developers (FIFA World Cup legacy, now institutionalised)

**Overlay modules:**
- OSHAD-SF Element requirements (Abu Dhabi) — maps directly to NEBOSH IG1 management elements
- ISO 45001:2018 — required across the region; maps to NEBOSH IGC
- Heat stress management — mandatory; UAE/KSA outdoor work ban June–Sep 10am–3pm
- Welfare standards for migrant workers — accommodation, food, medical care requirements
- Permit-to-work system requirements — OSHAD mandated
- Emergency Response Plan documentation

**Why critical:** NEBOSH IGC has its strongest global market in the Middle East — 40%+ of NEBOSH candidates come from Middle East/South Asia corridor. SC can sell directly to UAE/KSA EPC contractors who currently send workers to generic NEBOSH LPs.

---

### EUROPEAN UNION

**Framework:** EU Framework Directive 89/391/EEC  
**Construction-specific:** Temporary/Mobile Construction Sites Directive 92/57/EEC  
**Key directives:**
- Noise Directive 2003/10/EC — action levels 80/85/87 dB(A)
- Vibration Directive 2002/44/EC — HAV/WBV exposure limits
- Chemical Agents Directive 98/24/EC + Carcinogens Directive 2004/37/EC
- Work at Height Directive 2001/45/EC
- PPE Regulation EU 2016/425
- GDPR — data privacy for learner records (critical for SaaS compliance)

**Key markets:**
- Germany (DGUV — Deutsche Gesetzliche Unfallversicherung)
- Netherlands (Arbo Act)
- Ireland (Safety, Health and Welfare at Work Act 2005)
- Poland (Labour Code Chapter X — large civil construction workforce)

**Overlay approach:** EU modules delivered in English first (Ireland, Netherlands); German and French as Phase 2. GDPR compliance built into platform from day one.

---

## SaaS Technical Specification

### Data Model
```
Organisation
  └── territory: [NZ | AU | UK | CA | US | UAE | EU]
  └── Courses: filtered by territory tag
  └── Learners: inherit org territory; can override per project

Course
  └── global_modules: [] — NEBOSH-aligned, always present
  └── territory_modules:
        NZ: [HSWA, PCBU, ACC, NZGTTM, SiteSafe]
        AU: [WHS, SWMS, HRW, WhiteCard]
        UK: [CDM2015, RIDDOR, COSHH, CSCS]
        CA: [province-specific: ON/BC/AB/QC]
        US: [OSHA1926, CompetentPerson, OSHA10-30]
        UAE: [OSHAD-SF, ISO45001, HeatStress]
        EU: [89-391-EEC, GDPR, Directives]

Learner
  └── territory: from org
  └── progress: global_modules + territory_modules
  └── certificate: NEBOSH element % + territory compliance %
```

### Platform Roadmap
| Phase | Scope | Timeline |
|-------|-------|----------|
| 1 | NZ territory overlay built on Moodle | Q3 2026 |
| 2 | AU overlay + White Card alignment | Q4 2026 |
| 3 | NEBOSH LP accreditation application | Q1 2027 |
| 4 | Canada overlay (Tyler Baker lead) + UK overlay | Q2 2027 |
| 5 | US overlay + OSHA 10/30 alignment | Q3 2027 |
| 6 | UAE/KSA overlay + Arabic language | Q4 2027 |
| 7 | EU overlay + GDPR compliance + German/French | 2028 |

---

## Go-to-Market Summary

| Territory | Entry Strategy | Key Partner | SC Revenue Play |
|-----------|---------------|-------------|-----------------|
| NZ | Organic — home market | WorkSafe NZ, Site Safe | Foundation + brand |
| AU | White Card RTO partnerships | SafeWork preferred providers | Year 2 |
| UK | NEBOSH LP accreditation | Tyler Baker / IOSH members | Year 2 |
| Canada | Tyler Baker — direct channel | IHSA ON, BCCSA, COR bodies | Year 2 |
| US | Office expansion | AGC chapters, ENR top 400 | Year 3 |
| UAE/KSA | NEBOSH IGC demand | OSHAD-approved training cos | Year 3 |
| EU | Language-first (English/French) | Local H&S training partners | Year 4 |

---

## Immediate Actions

1. Complete NEBOSH gap fill (Safety Leadership, WAH, Confined Space, Fire, Hazardous Substances) → 75%+ alignment
2. Build NZ territory overlay modules for existing courses → low lift, home market
3. Build AU overlay → same PCBU framework, minimum delta from NZ
4. Engage Tyler Baker formally on Canada territory + NEBOSH LP pathway
5. Submit NEBOSH Learning Partner accreditation application
6. Architect territory plugin on Moodle (or spec new SaaS platform)
7. Build Arabic language track for Middle East market (high NEBOSH demand)

---

## References

- NEBOSH LP programme: https://www.nebosh.org.uk/guidance/guidance-for-learning-partners/
- NZ HSWA 2015: https://www.legislation.govt.nz/act/public/2015/0070/
- Safe Work Australia: https://www.safeworkaustralia.gov.au/
- OSHA 29 CFR 1926: https://www.osha.gov/laws-regs/regulations/standardnumber/1926
- UK CDM 2015: https://www.hse.gov.uk/construction/cdm/2015/
- OSHAD-SF: https://www.oshad.ae/
- CCOHS Canada: https://www.ccohs.ca/
- Ontario IHSA: https://www.ihsa.ca/
- Safe Work Australia WHS Model Act: https://www.safeworkaustralia.gov.au/doc/model-work-health-and-safety-act
