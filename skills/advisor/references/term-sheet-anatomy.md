# Term Sheet Anatomy: Economics vs Control

## Context

Use this reference when the user has received a term sheet, is negotiating specific clauses, or wants to understand what a particular provision means in practice. This is the primary reference for Term Sheet Mode. The central framework: every term sheet clause belongs to one of two categories — economics (what you get at exit) or control (who makes decisions). Prioritize negotiating energy accordingly. Most noise terms are not worth fighting over.

---

## The Two Categories That Govern Everything

Feld and Mendelson's core insight is that founders spend time negotiating the wrong things. Lawyers argue about registration rights for days while the liquidation preference — which can cut founder proceeds by 40% in a realistic exit — gets two minutes of attention.

Before analyzing any term sheet clause, classify it:

- **Economics**: Terms that affect how money is distributed at a liquidity event. Fight hard here.
- **Control**: Terms that affect who has decision-making authority. Fight selectively here.
- **Noise**: Terms that feel significant but rarely change outcomes. Concede quickly here.

---

## Economics Terms

### Valuation

**Pre-money valuation**: Value of the company before the investment arrives.
**Post-money valuation**: Pre-money + investment amount.

When a VC says "$20M valuation" they almost always mean post-money. Founders often assume pre-money. This is a $5M disagreement on a $5M round.

- "$5M investment at $20M post-money" → VC gets $5M / $20M = 25% ownership
- "$5M investment at $20M pre-money" → Post-money = $25M → VC gets $5M / $25M = 20% ownership

Always clarify: pre or post?

**Price per share formula**:
```
Price per share = Pre-money valuation / Fully diluted shares outstanding
```

"Fully diluted" includes all common, all preferred on as-converted basis, all options granted AND ungranted in the pool, and any new option pool expansion required pre-money. See cap-table-math.md for the option pool shuffle mechanics that make this critical.

---

### Liquidation Preference

This is the single most important economic term after valuation. It determines who gets paid first — and how much — when the company is sold or wound down.

All examples below use: $5M investment at $10M pre-money = 33.33% VC ownership. Exit scenarios at $15M, $30M, and $100M.

---

**Variant 1: 1x Non-Participating ("Simple Preferred") — GREEN**

The investor gets the BETTER of:
- Option A: Return of their investment (1x = $5M)
- Option B: Convert to common and receive their pro-rata share of proceeds

At $15M exit:
- Option A: $5M
- Option B: 33.33% × $15M = $5M
- Result: Equal — investor gets $5M, founders get $10M

At $30M exit:
- Option A: $5M
- Option B: 33.33% × $30M = $10M → investor converts
- Result: Investor gets $10M, founders get $20M

At $100M exit:
- Option A: $5M
- Option B: 33.33% × $100M = $33.3M → investor converts
- Result: Investor gets $33.3M, founders get $66.7M

This is the founder-friendly standard. Push for this in every negotiation. It aligns incentives — the investor only participates meaningfully in large exits.

---

**Variant 2: 1x Fully Participating ("Double Dip") — RED**

The investor gets:
- FIRST: Return of their investment (1x = $5M) off the top
- THEN: Their pro-rata share of the REMAINING proceeds as if converted

At $15M exit:
- Preference: $5M
- Remaining: $15M - $5M = $10M
- Participation: 33.33% × $10M = $3.33M
- Total investor: $8.33M | Founders: $6.67M
- (vs. $10M for founders under non-participating)

At $30M exit:
- Preference: $5M
- Remaining: $25M
- Participation: 33.33% × $25M = $8.33M
- Total investor: $13.33M | Founders: $16.67M
- (vs. $20M for founders under non-participating)

At $100M exit:
- Preference: $5M
- Remaining: $95M
- Participation: 33.33% × $95M = $31.67M
- Total investor: $36.67M | Founders: $63.33M

Fully participating always extracts more than the investor's ownership percentage. The $5M preference is effectively a tax on the exit before anyone else participates. Flag as a hard negotiating point.

---

**Variant 3: 1x Participating with Cap — YELLOW**

Functions like fully participating until cumulative return reaches a defined cap (commonly 2x-4x), then the investor must choose: take the capped amount or convert to common.

Example: $5M investment, 3x cap = $15M cap on total return.

Break-even formula (exit value where cap equals as-converted return):
```
Break-even exit = Cap / Ownership percentage
$15M cap / 33.33% = $45M exit
```

Below $45M exit: participation is active, investor earns up to $15M total
Above $45M exit: investor converts, earns 33.33% of total proceeds

At $100M exit: 33.33% × $100M = $33.3M > $15M cap → investor converts, gets $33.3M
At $30M exit: participation active → $5M + 33.33% × $25M = $13.33M (below cap)

This is a compromise position. Acceptable if the cap is 2x-3x and the expected exit range is above the break-even. Resist caps below 2x or exit ranges where you rarely clear break-even.

---

**Multiple Rounds: Stacked vs. Pari Passu Preferences**

When there are multiple rounds of preferred stock, the order of preference payment matters enormously.

**Stacked (senior/junior)**: Series B gets paid before Series A. Each round has separate preference paid in reverse chronological order.

**Pari Passu**: All preferred series share in the liquidation preference pool proportionally.

Example: $5M Series A + $20M Series B. Company sells for $15M.

Stacked outcome: Series B gets $15M (their $20M preference exceeds available proceeds). Series A and common get nothing.

Pari Passu outcome: A and B share pro-rata: Series A gets $15M × ($5M / $25M) = $3M. Series B gets $15M × ($20M / $25M) = $12M.

Founders strongly prefer Pari Passu. Series B investors strongly prefer stacked. This is a real negotiating point in bridge and later-stage rounds.

---

### Antidilution

Protects preferred investors when a future round prices lower (a "down round"). Without protection, existing preferred investors convert at their original price, getting fewer shares and higher dilution in the same down round as everyone else.

**Full Ratchet — RED**:
ANY down-round issuance — even one share — reprices ALL of that investor's preferred shares to the new, lower price. Extremely aggressive.

Example: Series A at $5/share, 1M shares = $5M invested. Down round at $1/share.
Full ratchet reprices all 1M shares to $1/share equivalent. Investor effectively gets 5x the shares on conversion. Catastrophic dilution for founders and common.

**Broad-Based Weighted Average — GREEN (standard)**:
Adjusts conversion price based on the magnitude of the down round. A tiny down round causes tiny adjustment. A massive down round causes significant adjustment.

Formula:
```
NCP = OCP × (CSO + CSP) / (CSO + CSAP)

NCP  = New conversion price
OCP  = Old conversion price
CSO  = Fully diluted shares outstanding (including options)
CSP  = Shares purchasable at old price with new money raised
CSAP = Shares actually purchased in the down round
```

Example: Series A at $5/share, 2M shares outstanding. Down round at $3/share for 500K shares.
- CSP = (500K × $3) / $5 = 300K (hypothetical shares at old price)
- NCP = $5 × (2,000,000 + 300,000) / (2,000,000 + 500,000) = $5 × 0.92 = $4.60

Conversion price adjusts from $5.00 to $4.60 — significant but proportional.

**Narrow-Based Weighted Average — YELLOW**:
Same formula but with a smaller denominator (excludes options, sometimes only counts common). Produces a lower NCP, which means more dilution for founders in a down round than broad-based.

---

### Pay-to-Play

Investors who do not invest their pro-rata share in future rounds have their preferred shares automatically converted to common.

This is good for founders — it enforces investor commitment and prevents free-rider investors from maintaining preference without continuing to support the company.

Carve-outs to negotiate: Seed-stage funds and micro-VCs structurally cannot do follow-on rounds. Include an explicit carve-out for any investor whose fund size makes pro-rata participation impossible. A $10M seed fund cannot lead a $30M Series B — punishing them for structural limitations is unfair and will poison the relationship.

Softer variant: Partial conversion proportional to shortfall (if investor does half their pro-rata, half their shares convert to common). Reasonable compromise.

---

### Vesting

Standard four-year vesting with one-year cliff, monthly thereafter.

**Cliff**: No shares vest until the one-year anniversary. At 12 months, 25% vests at once. Thereafter, 1/48th per month.

**Founder vesting credit at financing**: Founders typically receive credit for time already worked. A co-founder who started two years ago gets two years of vesting credit — only two years remain on their schedule.

**Single-trigger acceleration**: All unvested shares vest immediately upon acquisition. Rare in VC-backed companies. Acquirers hate it because it eliminates retention incentive. VCs hate it because unvested equity is considered part of acquisition price negotiation. Avoid unless you have exceptional leverage.

**Double-trigger acceleration (standard)**: Unvested shares vest only if BOTH triggers occur: (1) acquisition closes AND (2) employee is terminated without cause or resigns for good reason within 12-18 months of closing. This is the acceptable standard. Fight for double-trigger.

---

### Option Pool

The unissued portion of the option pool is typically required to be a certain size (10-20% post-money) before the financing closes. The pool increase comes from the pre-money valuation, not shared with the investor.

This is the option pool shuffle — see cap-table-math.md for full mechanics and how to negotiate it.

Rule of thumb: Every extra point of post-money option pool costs founders that percentage of their ownership without affecting the investor's ownership. A 20% pool vs. a 15% pool with the same pre-money valuation is a 5% transfer from founders to future employees — worth building an option budget to justify the smaller number.

---

## Control Terms

### Board of Directors

The board governs the company. Who controls the board controls the company's direction, CEO tenure, major decisions, and ultimately whether founders get fired.

Early-stage typical structure (Seed / Series A):
- 2 common seats (founders, usually CEO + CTO or CEO + one other)
- 1 preferred seat (lead VC)
- 1 independent outside director (agreed upon by both sides)
- Total: 4 seats (or 3: 1 common + 1 preferred + 1 outside)

Later-stage mature structure:
- 2-3 management seats
- 2-3 VC seats
- 2-3 independent directors
- Total: 6-9 seats

Outside directors are the pivotal variable. In a 2-1-1 or 2-2-1 board, the outside director is the tiebreaker. Who selects that outside director matters enormously — push for mutual agreement, not VC approval alone.

Board observers: Non-voting participants who attend meetings, receive materials, and can participate in discussions. They have no vote but can significantly influence dynamics. Limit observer seats; they dilute executive focus without adding governance accountability.

---

### Protective Provisions

These are investor veto rights — the company cannot take certain actions without consent from a defined percentage of preferred stockholders.

Standard list of protected actions:
- Amend the certificate of incorporation in ways that adversely affect preferred stock
- Create any new class of stock senior to or pari passu with preferred
- Increase the authorized shares of preferred
- Issue new shares above a defined threshold
- Sell, merge, or otherwise transfer control of the company
- Pay any dividend on common stock
- Increase or decrease the authorized board size
- Incur debt above a defined threshold (typically $1M-$2M for early stage)
- Declare bankruptcy or wind down
- Make acquisitions above a defined threshold

**Single class vote (standard / GREEN)**: All preferred series vote together as one class. A subsequent Series B investor cannot block a transaction without the consent of both Series A and B holders combined. Prevents any single series from having disproportionate veto power.

**Separate class vote per series (RED)**: Each series of preferred votes independently. Series A can block even if Series B, C, and common all agree. This gives early investors outsized control power as the company scales. Avoid.

---

### Drag-Along

Allows a majority shareholder group to force other shareholders to approve a sale.

**Investor-favorable variant (RED)**: Preferred shareholders alone can drag common along into a sale. Founders can be forced to vote for a sale they oppose.

**Founder-reasonable variant (YELLOW)**: A combination of common majority + preferred majority must agree to trigger drag-along. Neither side alone can force it.

**Departed founder clause (acceptable)**: Shares held by departed founders are deemed to vote proportionally with all remaining shareholders. This prevents a disgruntled ex-founder from blocking a transaction with a minority stake. Reasonable.

If drag-along is unavoidable: Push for trigger requiring majority of common (not preferred) plus any required preferred consent. The common vote effectively gives founders a blocking position.

---

### Conversion

**Voluntary conversion**: Any preferred shareholder can convert to common at any time. This is non-negotiable and always included. It allows investors to participate in upside if the company is performing well.

**Automatic conversion (IPO)**: All preferred automatically converts to common when the company completes a qualified IPO — defined by minimum offering price (e.g., 3x the Series A price) and minimum offering size (e.g., $50M gross proceeds).

Critical issue: If different series have different automatic conversion thresholds, later investors (with higher prices) may not meet the threshold that triggers conversion. This gives them a blocking position over the IPO unless their preferred shares convert — they can demand their liquidation preference even in a public offering.

Solution: Negotiate a single unified automatic conversion threshold that applies equally to all series. Or ensure that the threshold is set as a multiple of each series' respective conversion price, not a single dollar amount.

---

## Noise Terms — Concede Quickly

These terms consume significant legal negotiation time but rarely change outcomes in practice. Accept reasonable versions and move on.

**Registration rights**: Who can force the company to register shares for public sale, in what order, and how many times. Investment bankers overrule these provisions in any real IPO. The bank determines timing and allocation, not registration rights agreements.

**Information rights**: Investors receive quarterly financials, annual audited statements, board meeting notice. You should be sending this anyway. Agree to standard package without negotiation.

**Right of First Refusal / Pro Rata**: If a founder wants to sell shares, existing investors have right to buy first. If new shares are issued, existing investors can buy their pro-rata to avoid dilution. Both are standard. The pro-rata right is actively good for you — it encourages investors to support future rounds.

**Co-sale agreement (tag-along)**: If a founder sells shares, investors can sell proportionally into the same transaction. Unavoidable. Accept standard version.

**Founders' activities clause**: Founders agree to devote full time to the company. Just agree to this without negotiation.

**No-shop clause**: Company agrees not to shop the deal to other investors during due diligence and documentation. Standard 30-45 days is acceptable. Over 60 days is too long — push back.

---

## Red / Yellow / Green Triage Table

| Term | Green (Standard) | Yellow (Negotiate) | Red (Push Back Hard) |
|------|------------------|--------------------|----------------------|
| Liquidation Preference | 1x non-participating | 1x participating with 2x-3x cap | >1x multiple; uncapped participating; full ratchet |
| Option Pool | 10-15% unissued | 15-20% unissued | >20% from pre-money without justification |
| Board | Balanced (common = preferred) + outside | VC majority with strong outside tiebreaker | VC supermajority; no independent directors |
| Protective Provisions | Single class vote, standard list | Separate class votes, extended list | Unusual provisions; very low consent threshold |
| Antidilution | Broad-based weighted average | Narrow-based weighted average | Full ratchet |
| Vesting | 4yr/1yr cliff, double-trigger acceleration | 4yr/1yr cliff, no acceleration provision | Single-trigger; aggressive clawback; <4 year total |
| No-Shop | 30-45 days | 45-60 days | >60 days; no termination provision |
| Dividends | Non-cumulative when declared | Cumulative 5-8% | Cumulative >10% |
| Drag-Along | Majority common + majority preferred required | Common majority alone sufficient | Preferred alone can trigger; low threshold |
| Conversion Threshold | Unified threshold for all series | Separate thresholds with carve-outs | Per-series thresholds giving late investors IPO veto |

---

## Sequencing Advice

When reviewing a term sheet, work through it in this order:

1. Identify the valuation — pre or post? Confirm in writing.
2. Map the liquidation preference variant — non-participating, participating, or capped?
3. Check the option pool size and understand the option pool shuffle impact.
4. Review board composition — who controls the board post-financing?
5. Review protective provisions — single class or separate class vote?
6. Check antidilution — broad-based or something worse?
7. Review vesting terms — double-trigger present?
8. Everything else — assess quickly, concede or push back on specific language, do not negotiate extensively.

The first four items determine 90% of the economic and control outcome. The rest is real but secondary.
