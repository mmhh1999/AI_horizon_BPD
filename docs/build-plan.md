# Build Plan

## Rules we must not break

- [ ] Repo is **public** at submission and stays public afterward. *(It is currently private; switch before submitting.)*
- [ ] Commit history is intact: no force-push or squash that rewrites history.
- [ ] No API keys or credentials in any commit. Use `.env`, which is git-ignored.
- [ ] The README lists every library, framework, dataset, and API we use.

## Development tasks

- [ ] **Team sync:** confirm scope, pick the name, assign owners, pick the demo neighborhood, choose the runtime LLM.
- [ ] Arrange an advisor call; bring the [advisor questions](#questions-for-advisors-and-office-hours).
- [ ] Bring zoning-interpretation questions to the subject-matter-expert channel.
- [ ] Complete the submission form.
- [ ] **P0 core:** data loaded for 2 demo neighborhoods; `current` rules table verified; Layer 1 working; **HNA replication check** run with `pre-2025` rules.
- [ ] **P0 complete:** six scores, ranking, tipping points, SMAA robustness, AI explainers with fallback, UI end-to-end.
- [ ] **P1:** Reform Lens switcher and equity lens.
- [ ] Polish the interface, README, limitations, and AI log.
- [ ] Record the demo video.

## Workstreams (owners TBD at the sync)

| Workstream | Output | Owner |
|---|---|---|
| Data pipeline | Parcels, zoning, hazards, GTFS, and ACS joined for the demo area; retrieval dates logged | |
| Zoning rules (AI A1 plus verification) | Rules tables (`current`, `pre-2025`, then `bill-2025-1545`) with section citations and `verified_by`; the replication check against HNA p. 32 | |
| Typology specs | Geometry table from Parolek and MMH with sources; RECS energy coefficients | |
| Scoring and counterfactuals | Six scores, ranking, dominance, tipping points, SMAA robustness, binding rule, zoning stretch | |
| Equity lens | Existing-occupancy check, MVA join, displacement-pathway flags, evidence panel text | |
| AI layer (A2–A4) | Explainers with the number-grounding check and template fallback | |
| Interface and massing | [ui-spec.md](ui-spec.md) and [massing-and-metrics.md](massing-and-metrics.md) | Minghao |
| **Community-first rework (branch `mso-v0`)**: full-county pipeline; County → neighborhood → parcel drill-down; community needs; opportunity layers; expanded housing types; solar envelope; stakeholder priorities | [branch-notes/mso-v0.md](branch-notes/mso-v0.md), [concept.md § v3](concept.md#v3-what-changed-after-the-sat-2026-09-26-advisor-review) | Meltem |

**Branching:** each member develops on their own branch from `main`, and selected features are cherry-picked back. Branch manifests live in [branch-notes/](branch-notes/).
| Docs, limitations, video | README, limitations, AI log, script, recording | |

## Questions for advisors and office hours

1. **Ord. 2025-1579.** Did it remove the minimum lot area *per unit*, or only reduce minimum lot sizes? Our sources disagree. After the 2025 change, which Ch. 903 standard most often blocks duplexes, fourplexes, and townhouses: unit type by district, setbacks, height, or something else?
2. **Use permissions.** In R2, R3, and RM, which multi-unit types are permitted by right and which need a special exception or conditional use? Is a use gap (for example, a fourplex in R2) realistically a rezoning conversation?
3. **Bill 2025-1545.** What happened at the 2026-09-23 hearing, and when is the vote? Is the June 2026 draft the right text to model for ADUs and parking? Would City Planning find a parcel-level "what this bill changes" view useful?
4. **Anti-Displacement Review.** The 2022 HNA recommends reviewing zoning changes for displacement effects. Has the City started this? Would our Reform Lens plus equity lens help as a prototype?
5. **Primary user.** Should the demo center on a planner, a CDC, or a small developer?
6. **Benchmarks.** What thresholds do practitioners use for transit access (such as walk distance or frequency)? Are there reasonable defaults for the persona weights? (Olaf's question.)
7. **Displacement.** Is the MVA 2021 appropriate as market context? What is a responsible way to show the two displacement pathways without the tool becoming a targeting map?
8. **Demo sites.** Which pair of neighborhoods works best, one appreciating and one weak market with vacancy? Garfield (the Picket Fence site) is one candidate.
9. **Picket Fence.** Are there any preliminary cost or timeline findings from the Pitt/HUD study that we could cite?

## Submission checklist (Google Form)

- [ ] Team name; every member's name, email, and affiliation
- [ ] Track: **3, Housing Typology, Equity & Climate Matchmaker**
- [ ] Title and description: what it does, who it is for, what we would build next
- [ ] Demo video link (3–5 min, stays public)
- [ ] Public repo link
- [ ] Data sources: from [data-sources.md](data-sources.md)
- [ ] AI tool disclosure: from [ai-usage-log.md](ai-usage-log.md)
- [ ] Attestation: everyone is 18+

## Demo video outline (3–5 min)

Superseded 2026-09-27. The outline once here matched the pre-`mso-v0` single-parcel prototype (a Reform Lens switcher, inline DATA/ASSUMPTION/VALUE tags) and no longer matches the shipped app. The current, ready-to-record outline is the four-speaker voiceover script in [docs/demo-video-script.md](demo-video-script.md): who says what, exact on-screen clicks, timing per speaker, and the fallback line if Horizon doesn't answer live.
