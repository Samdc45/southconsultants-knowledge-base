# South Consultants — Full Tech Stack & Repository Map

**Last audited:** 2026-03-26  
**Audited by:** Penelope (AI PA)

---

## Repository Overview

| Repo | Purpose | Language | Status | Visibility |
|------|---------|----------|--------|------------|
| southconsultants-website | Main company website | HTML/CSS/JS | Live (Vercel) | Public |
| southconsultants-knowledge-base | Company knowledge base | Markdown | Live (GitHub) | Public |
| civil-app | Custom LMS platform | Python/Flask | Live (Railway) | Private |
| nzci-flexi-webhook | Gumroad→EdApp auto-enrolment | Python/Flask | Live (Railway) | Private |
| sam-central-app | Mac menu bar command app | Electron/JS | Local install | Private |
| compaction-101 | Compaction 101 landing page | HTML | Not yet deployed | Private |

---

## civil-app (LMS Platform)

**URL:** Deployed on Railway  
**Stack:** Python Flask, SQLite, Jinja2, ReportLab, Gunicorn  
**Courses (13 total):**

| Course | Country | Price |
|--------|---------|-------|
| Compaction 101 | 🇳🇿 NZ | $97 |
| NZCI Flexi: Excavator Awareness | 🇳🇿 NZ | $97 |
| NZ Site Safety | 🇳🇿 NZ | $97 |
| Civil Construction Safety 2026 | 🇳🇿 NZ | $97 |
| AU Entry Level | 🇦🇺 AU | $97 |
| CA Entry Level | 🇨🇦 CA | $97 |
| US Entry Level | 🇺🇸 US | $97 |
| Global H&S | 🌏 Global | $97 |
| AI & Autonomous Equipment | 🇳🇿 NZ | $297 |
| Philippines OFW Civil Safety | 🇵🇭 PH | Free (500 beta spots) |
| Survey & Machine Guidance | 🇳🇿 NZ | $97 |
| Culture Retention Challenge | 🌏 Global | $97 |
| Daily Safety Records | 🇳🇿 NZ | $97 |

**Features:**
- Student auth, progress tracking, certificates (PDF via ReportLab)
- CV/job application portal
- Daily safety records (toolbox meeting records)
- Admin dashboard
- Weekly content mailer (52-week LinkedIn/Reddit/Facebook calendar)
- Gumroad payment integration

**Required Environment Variables (Railway):**
- `SECRET_KEY` — Flask session secret
- `GMAIL_USER` — Gmail address for mailer
- `GMAIL_APP_PASSWORD` — Gmail app password

---

## nzci-flexi-webhook (Gumroad→EdApp Webhook)

**URL:** https://nzci-flexi-webhook-production.up.railway.app  
**Stack:** Python Flask, Railway  
**Function:** Auto-enrols students in EdApp when they purchase on Gumroad

**Course Map:**
| Gumroad Permalink | EdApp Course ID | Price |
|-------------------|-----------------|-------|
| wqlta | 6243abf7 | $97 Intro |
| emmgw | 612f306e | $497 Certificate |
| jxefqz | 612f3428 | $997 Corporate |

**Endpoints:**
- `GET /health` — Health check
- `POST /webhook/gumroad` — Gumroad purchase handler
- `GET /linkedin/auth` — LinkedIn OAuth
- `GET /linkedin/callback` — OAuth callback
- `POST /linkedin/post` — Auto-post to LinkedIn
- `GET /dashboard` — Sam Central command dashboard (password protected)

**Required Environment Variables (Railway):**
- `EDAPP_API_KEY` — EdApp API key
- `LI_CLIENT_ID` — LinkedIn app client ID
- `LI_CLIENT_SECRET` — LinkedIn app client secret
- `LI_REDIRECT_URI` — LinkedIn OAuth callback URL
- `GMAIL_USER` — Gmail for dashboard
- `GMAIL_APP_PASSWORD` — Gmail app password
- `DASHBOARD_PASSWORD` — Sam Central dashboard password

---

## sam-central-app (Mac Menu Bar App)

**Stack:** Electron, Node.js, AppleScript, Shell  
**Function:** Mac menu bar app — command centre for South Consultants  
**Features:**
- Unread email count in menu bar
- Siri shortcuts (samcentral://briefing, status, emails, open)
- Morning briefing at 8am
- Connects to Railway webhook, Gumroad, WordPress
- iPhone PWA via Railway dashboard

**Setup:** `bash setup.sh` then `npm start`  
**Build distributable:** `npm run build-mac`

**Required Environment Variables:**
- `DASHBOARD_PASSWORD` — Dashboard access password

---

## compaction-101 (Landing Page)

**Stack:** Pure HTML  
**Status:** Built, not yet deployed to Vercel  
**Pricing:** $197 individual / $797 team of 5 / $1,497 corporate  
**Payments:** Gumroad (https://southsam.gumroad.com/l/wpkqyo)  
**Note:** Currently branded as "Sam Central" — needs South Consultants rebrand

---

## southconsultants-website (Main Website)

**URL:** https://southconsultants-website.vercel.app  
**Stack:** HTML/CSS/JS  
**Deploy:** Auto-deploys from GitHub main branch via Vercel  
**Branding:** Navy (#1a2744) + Orange (#e8634a)

---

## Security Audit (2026-03-26)

All hardcoded secrets have been removed from public code. The following were patched:

| Repo | Issue | Fixed |
|------|-------|-------|
| nzci-flexi-webhook | EdApp API key hardcoded | ✅ Removed — use EDAPP_API_KEY env var |
| nzci-flexi-webhook | LinkedIn client secret hardcoded | ✅ Removed — use LI_CLIENT_SECRET env var |
| nzci-flexi-webhook | Dashboard password hardcoded | ✅ Removed — use DASHBOARD_PASSWORD env var |
| sam-central-app | Dashboard password in README | ✅ Removed from docs |
| civil-app | Flask secret key hardcoded | ✅ Removed — use SECRET_KEY env var |

**Action required:** Rotate the following credentials as they were exposed in a public repo:
- EdApp API key: `42350a01-d8cf-4c5f-85c3-a9cb55a17978` — **regenerate in EdApp dashboard**
- LinkedIn client secret — **regenerate in LinkedIn Developer Console**
- Dashboard password `SamCentral2026` — **change in Railway env vars**

---

## Integrations Map

| Service | Used By | Purpose |
|---------|---------|---------|
| Railway | civil-app, nzci-flexi-webhook | Hosting & deployment |
| Vercel | southconsultants-website | Hosting & deployment |
| Gumroad | compaction-101, nzci-flexi-webhook | Payment processing |
| EdApp | nzci-flexi-webhook | Course delivery platform |
| LinkedIn API | nzci-flexi-webhook | Auto-posting |
| Gmail IMAP | nzci-flexi-webhook, sam-central-app | Email dashboard |
| GitHub | All repos | Source control |

---
