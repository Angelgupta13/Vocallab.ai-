# UX Journey — Research Notes

## Full Evaluation Walkthrough

Traced the complete path a developer would follow to evaluate Vocallabs:

### Step 1: Land on vocallabs.ai
- Hero: "Conversational AI platform for modern businesses"
- Nav: Home, Solutions, Industries, VocalFlow, About, Pricing Policy, Contact, Blog, Noise-Cancellation, VocalStack, Hire With Us
- Primary CTA: "GET STARTED ⚡ 2 mins" (appears 4x on page)

### Step 2: Click "GET STARTED"
- Lands on /contact
- Typeform-like form: Name, Email, Phone, Company Size, Message
- Submit button: "Schedule Your Free Demo"
- Expected: sandbox/API key → Got: contact form → Gap

### Step 3: Check "Pricing Policy" (nav item #7)
- /pricing-policy page
- Generic content about pricing philosophy
- No per-minute rates, no tiers, no ranges, no INR pricing
- Expected: pricing → Got: philosophy → Gap

### Step 4: Check "About" (nav item #5)
- /about page
- Returns same homepage content (confirmed via HTML payload comparison)
- Expected: founder story, company info → Got: homepage → Gap

### Step 5: Check "Docs" (no nav item — found manually at docs.vocallabs.ai)
- Root page: 3 links — IP Whitelist, API Keys, Webhooks
- Looks like a starter template with no content
- Actual API reference at docs.vocallabs.ai/vocallabs (NOT linked from root or homepage)
- Expected: documentation → Got: empty root → Gap

### Step 6: Check "VocalFlow" (nav item #4)
- /vocalflow page
- Free open-source macOS dictation app
- MIT License, Swift, 1 GitHub star
- Uses Deepgram + Groq (not Vocallabs API)
- Expected: relevant product info → Got: unrelated OSS project → Gap

### Step 7: Check "Blog" (nav item #9)
- Links to subspace.money/blog
- 15+ posts titled "AI Voice Agents Benefits: [keyword]" — identically templated
- SEO spam quality, no technical depth
- Expected: product blog → Got: SEO farm on different domain → Gap

### Step 8: Google search "vocallabs pricing"
- No pricing page indexed
- No schema.org/Product structured data
- Expected: find pricing → Got: nothing → Gap

**Result: 8 steps, 5 broken, 1 misleading, 0 forward progress**

## DevTools Findings

### Network Tab (informal, not reproduced in all environments)
- Some API calls observed routing through shared infrastructure domains
- Images may be served from subspace-related CDN
- Indicates shared infrastructure between Vocallabs and Subspace/Whatsub (expected given common founder)

### Coverage Tab
- Next.js framework loaded but 95%+ of JS/CSS unused
- Site is mostly static content delivered through a heavy framework

### Structured Data
- No JSON-LD for SoftwareApplication type
- No Product schema with pricing
- No Organization schema with location/founder info

## Competitive UX Comparison

| Action | Vapi | Retell AI | Bland AI | Vocallabs |
|--------|------|-----------|----------|-----------|
| See pricing on homepage | ✅ $0.05/min hero | ✅ $0.07–$0.31 | ✅ $0.09/min | ❌ None |
| Sign up without talking to anyone | ✅ Free, no CC | ✅ Free credits | ✅ Free tier | ❌ Demo form |
| Make first API call | ~3 min | ~5 min | ~5 min | 2–5 days |
| See a dashboard | ✅ app.vapi.ai | ✅ Dashboard | ✅ Dashboard | ❌ None |
