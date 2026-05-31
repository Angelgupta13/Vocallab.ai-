# Full Product Walkthrough

**Date:** 29–30 May 2026  
**Method:** Manual browsing + Chrome DevTools + curl API probes

---

## 1. Homepage (vocallabs.ai)

### First Impression
- Loads a Next.js app — heavy but functional
- Hero: "Conversational AI platform for modern businesses"
- Subtitle: "AI voice agents automating business calls with human-like fluency"
- Two primary CTAs: "GET STARTED ⚡ 2 mins" and "Contact Sales" (both → /contact)

### Nav Inventory
| Nav Item | Route | Content | Working? |
|----------|-------|---------|----------|
| Home | / | Full homepage | ✅ |
| Solutions | /# | Scrolls to features | ⚠️ Anchor only |
| Industries | /# | Scrolls to features | ⚠️ Anchor only |
| VocalFlow | /vocalflow | OSS dictation app page | ✅ |
| About | /about | Returns homepage | ❌ Empty |
| Pricing Policy | /pricing-policy | Generic philosophy page | ⚠️ No rates |
| Contact | /contact | Typeform clone | ✅ |
| Blog | subspace.money/blog | SEO spam articles | ⚠️ Wrong domain |
| Noise-Cancellation | /noise-cancellation | Returns homepage | ❌ Empty |
| VocalStack | /vocalstack | Returns homepage | ❌ Empty |
| Hire With Us | hiringg.ai | External ATS | ✅ |

### Feature List on Homepage
1. "AI voice agents for sales, support & booking — natural, unscripted flows"
2. "Intelligent Call Flow Builder for customizable AI call scripts"
3. "SDK, n8n node & Chrome extension for workflow automation"
4. "Hybrid model: seamless AI ↔ live agent transitions"
5. "Voice analytics: emotion, intent & tone beyond transcription"

### Moats List on Homepage
1. "Full-stack ownership: design → execution → analytics"
2. "India-first: tuned for local languages, accents & workflows"
3. "Founder conviction: Joey Dash goes all-in post-Subspace"
4. "Data flywheel: proprietary conversation intelligence at scale"

### DevTools: Network Tab
- API domain: `api.superflow.run/b2b/` — NOT a vocallabs.ai subdomain
- CDN: `cdn.subspace.money` — shares infrastructure with Subspace
- Frames: `subspace.money` loaded in iframe for blog content

### DevTools: Coverage Tab
- 1.2MB JS loaded (Next.js framework + page bundles)
- ~95% unused for initial render of a mostly-static page
- Heavy framework overhead for simple content

### Structured Data
- No JSON-LD for SoftwareApplication
- No Product schema
- No Organization schema
- No breadcrumbs

---

## 2. Contact Flow (/contact)

### Form Fields
- Name (required)
- Email (required)
- Phone (required)
- Company Size (dropdown: 1-10, 11-50, 51-200, 200+)
- Message (textarea)
- Submit: "Schedule Your Free Demo"

### Experience
- Typeform-style embed, branded to Vocallabs
- No CAPTCHA observed
- No option to skip and try the product directly
- No "or use our API directly" alternative

---

## 3. Documentation (docs.vocallabs.ai)

### Root Page
- Minimal content — 3 sections visible:
  - IP Whitelist
  - API Keys
  - Webhooks
- Each section has 1-2 sentences of description
- No API reference linked
- No getting started guide
- No authentication guide

### API Reference (docs.vocallabs.ai/vocallabs)
- NOT linked from docs root or homepage
- Discovered via search engine
- Contains:
  - 40+ API endpoints across 11 resource groups
  - Agents, Calls, Conversations, Analytics, SIP, Campaigns, Templates, Webhooks, Phone Numbers, Services, Transactions
  - createAIAgent, createSIPCall, getCallConversation, getCallSummary
  - WebSocket URL for real-time streaming
  - Authentication headers documented
- Response schemas are inconsistently documented — some have examples, some don't

---

## 4. GitHub Presence (github.com/Vocallabsai)

| Repo | Stars | Forks | Commits | Last Update | Description |
|------|-------|-------|---------|-------------|-------------|
| vocal-sdk | ~0 | ~0 | Few | Unknown | React Native SDK |
| n8n-nodes-vocallabs | 3 | 3 | Unknown | Recent | 100+ ops, 11 resources |
| n8n-nodes-vocallabs-backend | ~0 | ~0 | Few | Unknown | Backend for n8n nodes |
| vocalflow | 1 | 12 | 18 | Mar 2025 | macOS dictation app (OSS) |

---

## 5. Subspace.money Connection

### Discovered Via
- DevTools network tab → api.superflow.run/b2b/
- Image src → cdn.subspace.money
- Blog redirect → subspace.money/blog
- Footer link → subspace.money

### Founder Overlap
- subspace.run/about-us: "IIT Madras alumni, 2X founder, ISRO, 2-year experience at SocGen Bank"
- Matches Vocallabs founder profile (Joey Dash, post-Subspace)

### API Naming
- Endpoints in API reference include "whatsub" prefixes:
  - whatsubTransactionHistory
  - whatsub_services
- Suggests shared codebase evolution from a previous product

---

## 6. Competitor Signups (Quick Comparison)

### Vapi (app.vapi.ai/register)
- Email + password → verify → dashboard with API key
- 60 free minutes pre-loaded
- Time to first API call: ~3 minutes
- Dashboard shows call logs, analytics, agent builder

### Retell AI (dashboard.retellai.com)
- Email + Google signup → verify
- $10 free credit
- Time to first agent: ~5 minutes
- Documentation has SDK examples, response schemas, webhook setup

### Bland AI (app.bland.ai)
- Email + Google signup → verify
- Free tier with limited minutes
- Time to first call: ~5 minutes
- Dashboard shows call history, analytics, templates
