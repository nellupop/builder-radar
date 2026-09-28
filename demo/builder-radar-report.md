# Builder Radar Report — SYNTHETIC RUN

Sources: 5 local records (`fixtures/builder-radar-input.json`), all fabricated for demonstration. Generated 2026-09-28.

## 1. Recurring On-Chain Report Agent
**Deliverable:** A scheduled agent that pulls a supplied set of DEX pools or wallets via read-only public APIs and posts a formatted volume/treasury report on a fixed cadence.
**Buyer:** Small DeFi teams and independent traders currently pulling this data by hand.

**Evidence**
- REC-002 [observed] — job post explicitly requests a daily DEX volume bot, budget $200.
- REC-005 [observed] — support ticket logs a customer asking for an automatic weekly treasury summary instead of manual CSV pulls.
- REC-001 [inference] — a parallel manual-copying complaint about a payments dashboard suggests the pattern isn't DeFi-specific.
- REC-002 [unverified_demand] — the $200 figure is posted, not paid.

**Limitations:** needs buyer-supplied read-only API access, no custody; report-only, no trading advice; accuracy tied to the freshness of the public data source.
**Next validation step:** post one $150–200 fixed-price offer scoped to exactly this deliverable; 3+ serious replies within a week counts as validation.

## 2. Protocol Parameter-Change Watcher
**Deliverable:** An agent that checks up to 5 supplied protocol doc URLs on a schedule and outputs a plain-text diff since the last check.
**Buyer:** Newsletter writers and researchers tracking multiple protocols.

**Evidence**
- REC-004 [observed] — post states manually checking 15 protocol docs weekly, asks for an agent to do it.
- REC-003 [inference] — same "manual repeated checking of external sources" pattern as the sanctions-flagging request, suggesting watcher-agents are a recurring category, not a one-off.
- REC-004 [unverified_demand] — only one source, no confirmed willingness to pay.

**Limitations:** reliable only on pages with stable, diffable structure; flags that text changed, not whether it's material; bounded to 5 URLs per run.
**Next validation step:** run against 3 real protocol docs for 2 weeks and count false-positive diffs before offering it.

## 3. Wallet Hop-Distance Flagging Agent
**Deliverable:** Takes a supplied wallet list plus a public sanctions list, outputs a CSV flagging wallets within N hops of a sanctioned address, using public chain data only.
**Buyer:** Compliance-adjacent teams at small exchanges or protocols.

**Evidence**
- REC-003 [observed] — GitHub issue explicitly requests auto-flagging within 2 hops, notes the current manual spreadsheet process.

**Limitations:** weakest-supported idea (single source); accuracy bounded by the sanctions list supplied, not legal/compliance advice; simple N-hop heuristic will miss more complex laundering patterns.
**Next validation step:** run against one publicly known sanctioned test wallet and manually confirm correct 1- and 2-hop flags before showing it to anyone.

---
*All evidence above is labeled observed / inference / unverified_demand per the SKILL.md workflow. All five source records are synthetic and were not drawn from real people or platforms.*
