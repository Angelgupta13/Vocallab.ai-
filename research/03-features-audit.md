# Features / Services — Research Notes

## Feature Claims on Homepage

Homepage lists 5 features:
1. AI voice agents for sales, support & booking — natural, unscripted flows
2. Intelligent Call Flow Builder for customizable AI call scripts
3. SDK, n8n node & Chrome extension for workflow automation
4. Hybrid model: seamless AI ↔ live agent transitions
5. Voice analytics: emotion, intent & tone beyond transcription

## Verifiability Check

| Feature | Claim Visible? | Evidence Found? | Evidence Type |
|---------|---------------|-----------------|---------------|
| AI voice agents | Homepage + docs | API has createAIAgent, createSIPCall endpoints | API reference at docs.vocallabs.ai/vocallabs |
| Call Flow Builder | Homepage only | No UI, no screenshots, no demo | None |
| SDK (React Native) | Homepage + GitHub | GitHub repo exists, README with setup | github.com/Vocallabsai/vocal-sdk |
| n8n node | Homepage + GitHub + n8n marketplace | 100+ ops across 11 resources, 3 stars | github.com/Vocallabsai/n8n-nodes-vocallabs |
| Chrome extension | Homepage + Chrome Web Store | Exists but not deeply evaluated | Not tested — time constraint |
| Hybrid AI→live handoff | Homepage only | Not documented in API reference | None |
| Voice analytics | Homepage only | No sample output, no dashboard, no schema | **Gap** |

## The Analytics Gap (Deepest Feature Concern)

**Claim:** "Voice analytics: emotion, intent & tone beyond transcription"

**What exists:**
- n8n node has `Analytics` resource with 3 operations: Get Call Conversation, Get Call Summary, Get Post-Call Data
- API reference mentions analytics endpoints but response schemas are not documented

**What is missing:**
- No dashboard screenshot anywhere
- No sample analytics output (transcript with emotion labels, intent classification)
- No accuracy benchmarks
- No description of what "emotion" means (anger/happiness/frustration per turn? per call?)
- No description of intent taxonomy
- No demo video
- No case study referencing emotion or intent data

**Assessment:** The analytics endpoints may exist in the API. But without documented schemas, sample outputs, or a dashboard view, a buyer cannot evaluate whether this is a production-grade feature or a thin wrapper around a third-party sentiment API.

## The n8n Node (Bright Spot)

The n8n community node is actually well-built:
- 100+ operations across 11 resource groups
- Covers agents, calls, conversations, analytics, SIP, campaigns, templates, webhooks, phone numbers, services, transactions
- Documented operations with input fields

**Problem:** 3 stars and 3 forks after months on the marketplace suggests either:
- Zero promotion (likely — no mention of n8n on vocallabs.ai homepage)
- Developers try and abandon (possible — no way to evaluate without a demo)
- No community engagement (expected — no Discord, no forum, no support channel)

## Subspace Comparison

Subspace.money ships a working consumer app (Android/iOS/Web) with real features. The product is the marketing. Vocallabs ships an API that requires a sales call to access. The feature development philosophy appears similar (build real infrastructure) but the GTM wrapping is completely different.
