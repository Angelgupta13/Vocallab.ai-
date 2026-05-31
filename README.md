# Vocallabs.ai — Product Teardown

**Product Intern Assignment · May 2026**  
**Candidate:** Angel Gupta  
**Company chosen:** Vocallabs.ai (of the two provided: Vocallabs.ai · Subspace.money)

---

## Repository Structure

```
vocallabs-teardown/
├── README.md                   ← This file — overview, methodology, key findings
├── report/
│   └── index.html              ← Polished, printable teardown report (single-file HTML)
├── evidence/
│   ├── screenshots/            ← Screen captures for every key observation
│   │                            (capture instructions in each file if re-taking)
│   └── user-journey/
│       └── full-walkthrough.md ← Complete step-by-step trace of product evaluation
├── research/
│   ├── 01-gtm-and-icps.md      ← GTM audit, ICP mapping, positioning analysis
│   ├── 02-competitor-analysis.md ← Deep dives: Vapi, Retell, Bland, Gnani.ai, Bolna
│   ├── 03-features-audit.md    ← Feature-by-feature audit with screenshots
│   ├── 04-ux-journey.md        ← Full UX walkthrough with DevTools inspection
│   └── 05-collaborations.md    ← Partnership surface: Exotel, n8n, Subspace, ecosystem
└── assets/
    └── about-candidate.md      ← Brief background (optional reading for evaluators)
```

## Methodology

1. **Full site exploration** — every nav link, every route, every footer link on vocallabs.ai, docs.vocallabs.ai, and subspace.money
2. **DevTools analysis** — network tab (API domains, CDN origins), coverage tab (JS/CSS usage), source tab (page structure)
3. **Competitor evaluation** — signed up for Vapi, Retell AI, Bland AI; traced signup flows end-to-end
4. **Content audit** — all blog posts, all GitHub repos, all social media presence
5. **Infrastructure mapping** — DNS lookups, API endpoint tracing, domain relationships

## Key Findings (Top 3)

| # | Finding | Pillar | Impact |
|---|---------|--------|--------|
| 1 | "⚡ 2 mins" CTA leads to a contact form, not a product — the promise mismatches the reality on first click | UX | Loses developers in seconds |
| 2 | "India-first" is stated as a moat but has zero visible evidence — no Indian language demos, no TRAI docs, no INR pricing, no Indian case studies | GTM & ICPs | Strategic window closing as competitors enter India |
| 3 | Exotel integration is Vocallabs' strongest India-telephony asset — documented only on Exotel's site, not on vocallabs.ai | Collaborations | Free distribution channel going unused |

## Why Vocallabs (over Subspace)

Subspace.money is bootstrapped, profitable (Rs.36.5 Cr ARR), and has a live consumer product. It is arguably a safer company to analyze. I chose Vocallabs because:

- The gap between product quality and go-to-market execution is wider — more room for high-leverage feedback
- The "India-first" voice AI category is at an inflection point (Gnani.ai raised $10M in March 2026, Bolna raised $6.3M)
- Joey Dash's experience building Subspace (bootstrapped to Rs.36.5 Cr ARR) provides a unique lens: what patterns from Subspace transfer to Vocallabs, and which ones don't?

The Subspace connection weaves through several feedbacks — particularly the Collaborations and GTM sections — because the most non-obvious observation in this teardown is that Vocallabs and Subspace are solving the same distribution problem with opposite strategies.

---

*All observations documented at time of analysis: 29–30 May 2026.*
