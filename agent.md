# agent.md — Annuity.com Channel Knowledge Base

Guide for AI agents and humans using this knowledge base.

## What this repo is
A knowledge base extracted from the YouTube channel @annuity-com (Annuity.com's agent-education channel: "The Closing Room" training calls, "Agent Opportunity" calls, carrier spotlights, agent summits) — 20 videos, ~14 hours of content, ~700K characters of cleaned transcripts.

Built for reuse in marketing materials, creator briefs, and SEO/GEO articles.

## Files

| File | Contents |
|---|---|
| `index.html` | Browser dashboard — renders every markdown file with navigation and search |
| `glossary.md` | **151 terms** with the channel's own definitions, source video noted |
| `knowledge-graph.md` | **162 typed entities** (People / Carriers & Companies / Products / Platform & Tools / Programs) + key-relationships section |
| `claims-library.md` | **226 claims** split COMPANY-reported vs EDUCATIONAL/industry. ⚠️ VERIFY flags mark compliance-sensitive or company-reported figures |
| `sales-playbook.md` | **155 sales teachings** indexed by source video (frameworks, objection handling, outreach hooks) |
| `seo-briefs.md` | 8 article briefs mined from topic clusters, richest definitional source first, plus GEO (AI-engine) guidance |
| `knowledge-base.json` | The structured merge (all entities, terms, claims, teachings, quotes, topics) — machine-readable |
| `parts/batch1-4.json` | Per-video extraction batches (source of truth for source-video attribution) |
| `videos.txt` | The 20 video IDs + titles |

Raw transcripts are kept locally in the project folder (`~/projects/annuity-com/text/`) and are intentionally NOT published in this repo.

## Rules for agents using this KB

1. **⚠️ VERIFY flags are binding.** Any claim marked VERIFY is company-reported, speaker-asserted, or compliance-sensitive (share valuations, fee claims, tax-free claims, Social Security figures). Fact-check against primary sources before publishing. The channel contradicts itself on some numbers (retirees/day: 10K vs 11K vs 11.2K; annuity sales $434B vs $460B; agent counts) — the variants are recorded, never averaged.
2. **Distinguish COMPANY from EDUCATIONAL.** Company facts (Annuity.com platform, commissions, stock programs, CORE/AgentPay/LeadPro) are the company's own representations. Educational content (annuity concepts, Social Security mechanics) is generic. Never blend the two in one article.
3. **Caption artifacts.** Transcripts are auto-captions. Known corrupted items were flagged `[unclear]` during extraction: LeadPro "$1.99/mo" is almost certainly $199/mo; "Irma" = IRMAA; "MIGA" = MYGA; "Zaghorn"/"NASA/Ethos" = Nassau Athos; the "Broach/Roach/Broich" surname = Broach. Anything else suspicious: check `parts/*.json` or the raw transcript locally.
4. **Attribution.** Source-video attribution lives in `parts/batch*.json` per record. The rendered markdown files carry shortened source names; use the JSON for exact mapping.
5. **Compliance.** Annuity/insurance marketing is regulated. Sales-teaching content describes what the channel teaches — republishing product guarantees, rates, or tax claims without verification and compliance review is on you.
6. **Update path.** New channel videos: pull transcripts with yt-dlp → convert with `vtt_to_text.py` → run extraction subagents per the youtube-channel-knowledge-base skill → merge → regenerate the five markdown files.

## Key entities (quick reference)
- **Brett Blake** — CEO; Agent Opportunity calls, 4-phase AI roadmap, stock programs
- **Bill Broach** — partner; relationship-selling teachings, All Hands updates
- **John Stevenson** — top producer; Cap-the-Company case study (6mo→3mo→~5 weeks)
- **Tom Hegna** — objection framework, Social Security tax torpedo, MYGA, SPIA legacy structures
- **Matthew Allen** — Social Security deep dive (FRA, WEP/GPO, Fairness Act, IRMAA) — richest SEO source
- **Bruce Jensen** — COO; need-matching philosophy, 2x5 plan
- **Platform** — CORE dashboard, AgentPay, LeadPro ($199/mo), Agency Builder (7 layers), stock tiers $1M/$3M/$5M, Race to a Million
- **Carriers** — Nassau Athos FIA, Malibu Life, 60-80 carriers / 2,400+ products
