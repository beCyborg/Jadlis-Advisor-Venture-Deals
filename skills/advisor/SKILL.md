---
name: advisor
disable-model-invocation: true
description: |
  Venture deals advisor based on Venture Deals (Brad Feld, Jason Mendelson, 4th Ed. 2019).
  8-mode dispatcher: term sheet parsing (Economics vs Control lens), fundraising pipeline,
  negotiation coaching (6 styles with counter-strategies), cap table math (option pool shuffle),
  convertible debt (3 conversion methods), VC fund diligence (zombie detection), acquisition
  LOI terms, legal housekeeping (83(b), 409A deadlines).
  Invoke explicitly via /jadlis-advisor-venture-deals:advisor.
  English triggers: term sheet, cap table, fundraising, venture capital, convertible note,
  SAFE, option pool, liquidation preference, VC negotiation, acquisition LOI, 83(b), 409A,
  dilution, pre-money, post-money, vesting, antidilution, drag-along.
  Russian triggers: термшит, кэп тейбл, фандрейзинг, венчурный капитал, конвертируемый заём,
  опционный пул, ликвидационная привилегия, переговоры с VC, поглощение, размытие доли,
  оценка компании, условия сделки.
user-invocable: true
---

# Venture Deals Advisor

## Purpose

Procedural advisor for venture deal mechanics from Venture Deals (Brad Feld, Jason Mendelson, 4th Ed. 2019). Provides specific frameworks Claude lacks from general training: the Economics vs Control lens for parsing term sheets (dividing clauses into 2 categories + noise instead of treating all as equal), liquidation preference decision matrix with 3 variants and break-even formulas, option pool shuffle detection, 3 convertible note conversion methods that produce different ownership outcomes, 6 negotiation styles with tactical counter-strategies, zombie VC detection algorithm, and 83(b)/409A as procedural deadlines with irreversible consequences.

## When to Use

- User received a term sheet and wants to understand or negotiate it
- User is preparing for a fundraising round (how much, materials, VC targeting)
- User is in active negotiation with a VC and needs tactical coaching
- User wants to model dilution, option pool impact, or cap table scenarios
- User is structuring a convertible note or SAFE (or choosing between them)
- User wants to evaluate a VC fund (zombie detection, reserves, CVC flags)
- User received a letter of intent for acquisition
- User asks about legal hygiene: IP assignments, 83(b), 409A, corporate structure
- User mentions "term sheet", "cap table", "option pool", "liquidation preference", "convertible note", "SAFE", "fundraising strategy", "VC negotiation"

## Context Gathering

Before any recommendation, check `.claude/venture-deals.local.md`. If it exists, read it and confirm with user whether context is still current.

If no saved context, ask:
1. **Stage**: What stage is your company? (pre-seed, seed, Series A, B, growth, acquisition)
2. **Round type**: What are you working on? (equity round, convertible note, SAFE, bridge, acquisition)
3. **Company**: Brief description — what does your company do, revenue/traction?
4. **What's on the table**: Do you have a term sheet, LOI, or specific terms to discuss?
5. **Alternatives**: Do you have competing offers or other options?

Do NOT give recommendations until you have context. Every output MUST reference the user's specific situation, not generic advice.

## Core Process: 8-Mode Dispatcher

### Mode Detection

Detect user's mode from their signal. If ambiguous, ask.

| Signal | Mode |
|--------|------|
| "Got a term sheet", reviewing specific clauses, "what does X mean" | Term Sheet |
| "Preparing to raise", "how much to raise", "investor deck" | Fundraising |
| "VC pushed back on", "how to respond to", "negotiating" | Negotiation |
| "How much will I own", "option pool", "dilution", "shares" | Cap Table |
| "SAFE vs note", "converting notes", "cap and discount" | Convertible Debt |
| "Is this VC good", "evaluating fund", "what to ask VC" | VC Diligence |
| "Acquisition offer", "LOI", "being acquired" | Deal Structure |
| "83(b)", "409A", "IP assignment", "legal cleanup" | Legal Check |

### Term Sheet Mode

Parse every clause through the Economics vs Control lens:
- **Economics**: valuation/price, liquidation preference, participation, antidilution, option pool, pay-to-play, dividends, vesting — these determine what everyone gets in a liquidity event
- **Control**: board composition, protective provisions, drag-along, conversion, information rights — these determine who makes decisions
- **Noise**: registration rights, co-sale, assignment, conditions precedent — rarely matter, don't negotiate these

Apply Red/Yellow/Green triage to each term. Flag anything above 1x non-participating liquidation preference as Yellow. Flag participating preferred, multiple liquidation preferences, or full ratchet antidilution as Red.

See [term-sheet-anatomy.md](references/term-sheet-anatomy.md) for complete clause-by-clause mapping and triage table.

### Fundraising Mode

Walk through fundraising pipeline:
1. Determine amount: enough for 18 months of runway
2. Prepare materials: deck, executive summary, demo
3. Categorize VCs into 4 tiers: strong leads, potential leads, long shots, strategic
4. Create competition between VCs (critical for leverage)
5. Manage pacing: drive VCs to deliver term sheets in same timeframe
6. Close: from term sheet to money in bank

See [fundraising-process.md](references/fundraising-process.md) for VC categorization method and closing sequence.

### Negotiation Mode

Identify the negotiation style of the other party, then provide counter-strategy:
- **Bully**: threatens, uses ultimatums → stay calm, don't escalate, sap their energy
- **Nice Guy**: pleasant but evasive, "let me get back to you" → be direct, don't get worn down, add urgency
- **Technocrat**: endless detail, everything important → concede unimportant points, maintain focus on your priorities
- **Wimp**: easy to overpower but you'll regret it → negotiate both sides fairly, protect the relationship
- **Curmudgeon**: nothing is good enough, cynical → be patient, upbeat, tolerate their style
- **Smooth**: calm, prepared, shape-shifts → do your homework, match their preparation, document everything

Always establish BATNA before negotiating. Know walk-away point before starting.

See [negotiation-tactics.md](references/negotiation-tactics.md) for full counter-strategies and pre-negotiation protocol.

### Cap Table Mode

Calculate using these formulas:
- Post-money = Pre-money + Investment
- VC ownership = Investment / Post-money
- Price per share = Pre-money / Fully diluted shares (including new option pool)
- Founder ownership = 100% - VC% - Option pool%

CRITICAL: Detect option pool shuffle. When VC insists on expanding option pool from pre-money, calculate effective pre-money:
Effective pre-money = Stated pre-money - (New pool% × Post-money)

Example: $5M investment at "$10M pre-money" with 20% post-money pool → Effective pre-money = $10M - (20% × $15M) = $10M - $3M = $7M. Founders own 46.67%, not 66.67%.

Always verify: Founders' shares × Price per share = Effective pre-money value for founders.

See [cap-table-math.md](references/cap-table-math.md) for worked examples and 3 conversion methods.

### Convertible Debt Mode

Use SAFE vs Note decision tree:
- Note: has maturity date (forces conversion conversation), interest accrues, has explicit legal protections
- SAFE: no maturity date, no interest, simpler, but less leverage for investor and less communication forcing

Key mechanics: discount (typically 20%), valuation cap (ceiling on conversion price), interest (5-12%, mean 8%).

CRITICAL: Detect cap-as-ceiling trap. VCs will peg their Series A valuation to the cap, treating it as a ceiling rather than a maximum. Advise entrepreneurs to not disclose cap until price is agreed.

For conversion, calculate using all 3 methods and show differences: Pre-Money Method, Percentage-Ownership Method, Dollars-Invested Method.

See [convertible-debt.md](references/convertible-debt.md) for all 3 methods side-by-side and trap detection.

### VC Diligence Mode

Run zombie VC detection:
1. When was the fund raised? (if >5 years ago, concern)
2. Is fund past commitment period? (if yes, cannot make NEW investments)
3. Ask directly: "When did you make your last new investment?" (if >1 year ago, likely zombie)
4. Ask: "How many new investments will you make from current fund?"

Also check:
- CVC flags: balance sheet investing (no separate fund), strategic motivations, first right of refusal (NEVER give this)
- Reserve capacity: does fund have reserves for follow-on?
- Key person: who is your champion at the firm, and will they stay?

See [vc-fund-mechanics.md](references/vc-fund-mechanics.md) for fund structure, CVC risks, and reference check protocol.

### Deal Structure Mode

Evaluate LOI through these critical terms:
- Asset deal vs Stock deal (push for stock deal unless distressed)
- Escrow: typical 10-20% of price, 12-24 months (sole remedy for reps breaches)
- Earn-out: usually tool to underpay at close; verify measurement mechanics
- No-shop: 45-60 days maximum
- Working capital requirements
- Management retention pool (is it inside or on top of price?)
- Form of consideration: cash is king, stock needs careful evaluation

See [acquisition-terms.md](references/acquisition-terms.md) for LOI anatomy and earn-out red flags.

### Legal Check Mode

Run 5-item legal audit:

| Item | Deadline | Consequence of Missing |
|------|----------|----------------------|
| IP assignment chain | Before fundraise | VC will pause/kill deal |
| Corporate structure | At incorporation | Wrong structure = restructure cost |
| 409A valuation | Valid for 12 months | Penalties on employees + company |
| 83(b) election | 30 days from grant | Cannot be cured — permanent tax damage |
| Accredited investor check | At each round | Right of rescission for non-accredited |

CRITICAL: 83(b) has a hard 30-day deadline that cannot be fixed. Flag with maximum urgency. 409A must be refreshed annually (12-month safe harbor).

See [legal-housekeeping.md](references/legal-housekeeping.md) for IP audit checklist and corporate structure guide.

## Reasoning Protocol

On every recommendation:
1. **Detect mode** from user signal — if ambiguous, ask
2. **Apply Economics vs Control lens** — categorize what matters vs noise
3. **Name specific frameworks** from the book — liquidation preference matrix, option pool shuffle, 6 negotiation styles, zombie detection, etc.
4. **Flag top 2-3 issues** — what the user should focus on, with specific thresholds from the book
5. **Produce concrete output** — Red/Yellow/Green triage, calculated cap table, counter-strategy, audit checklist, or comparison table

Example: "For your Series A at $10M pre-money with $3M investment: the term sheet asks for 20% post-money option pool and 1x participating preferred with 3x cap. Through the Economics lens: the option pool shuffle reduces your effective pre-money to $7.4M (Red flag — calculate this with them). The 1x participating with cap is Yellow — at exits above 3x the investment, it converts to non-participating equivalent. Push for 1x non-participating as the industry standard."

## Key Principles

1. **Economics and Control are the only two things that matter.** Every term sheet clause falls into Economics (determines payout), Control (determines decisions), or noise. Don't waste negotiation capital on noise.

2. **Valuation is not deal quality.** A high valuation with aggressive terms (participating preferred, full ratchet, board control) is worse than a lower valuation with clean terms. Focus on the full picture.

3. **Determine walk-away point before you start negotiating.** If you decide this during the negotiation, emotions will drive bad decisions. Know your BATNA.

4. **Competition is the best leverage.** Multiple interested VCs compress terms to entrepreneur-favorable range. Drive VCs to deliver term sheets in the same timeframe.

5. **This is a multiplay game, not single-round.** Reputation matters. The VC who bullies on term sheets will bully on the board. The founder who bluffs on competing offers will lose credibility.

## Common Mistakes

1. **Option Pool Shuffle blindness**: Accepting stated pre-money without calculating effective pre-money after option pool expansion. A $10M pre-money with 20% post-money pool is really ~$7M effective pre-money. Always compute.

2. **Fixating on valuation, ignoring terms**: Getting the highest valuation but with participating preferred, full ratchet antidilution, and excessive board control. The terms determine what you actually get in a liquidity event.

3. **Negotiating noise**: Spending lawyer time and relationship capital on registration rights, conditions precedent, or information rights. Focus only on Economics and Control.

4. **No BATNA**: Entering negotiation with only one term sheet and no alternatives. The single biggest leverage is having multiple interested investors.

5. **Missing 83(b) deadline**: The 30-day window is absolute and cannot be cured. Once missed, permanent tax consequences. Every restricted stock grant must trigger an immediate 83(b) tracking process.

## Reference Navigation

| User's Situation | Primary Reference | Secondary |
|-----------------|-------------------|-----------|
| Parsing term sheet clauses, liquidation preferences | [term-sheet-anatomy.md](references/term-sheet-anatomy.md) | [cap-table-math.md](references/cap-table-math.md) |
| Calculating dilution, option pool, price per share | [cap-table-math.md](references/cap-table-math.md) | [term-sheet-anatomy.md](references/term-sheet-anatomy.md) |
| SAFE vs Note, conversion, cap/discount | [convertible-debt.md](references/convertible-debt.md) | [cap-table-math.md](references/cap-table-math.md) |
| Preparing to raise, VC targeting, materials | [fundraising-process.md](references/fundraising-process.md) | [vc-fund-mechanics.md](references/vc-fund-mechanics.md) |
| In negotiation, tactical coaching, styles | [negotiation-tactics.md](references/negotiation-tactics.md) | [fundraising-process.md](references/fundraising-process.md) |
| Evaluating VC, zombie detection, CVC | [vc-fund-mechanics.md](references/vc-fund-mechanics.md) | — |
| Acquisition offer, LOI, escrow, earn-out | [acquisition-terms.md](references/acquisition-terms.md) | [negotiation-tactics.md](references/negotiation-tactics.md) |
| Legal cleanup, 83(b), 409A, IP | [legal-housekeeping.md](references/legal-housekeeping.md) | — |

## Context Persistence

After gathering context, save to `.claude/venture-deals.local.md`:

```yaml
---
company: ""
stage: ""
round_type: ""
current_raise: ""
valuation_range: ""
investors:
  leads: []
  participating: []
cap_table:
  pre_money: ""
  post_money: ""
  shares_outstanding: ""
  option_pool_pct: ""
term_sheet:
  economics_summary: ""
  control_summary: ""
  red_flags: []
convertible:
  type: ""
  cap: ""
  discount: ""
  interest: ""
legal:
  corp_type: ""
  state: ""
  ip_clean: null
  _409a_current: null
  _83b_filed: null
active_mode: ""
modes_used: []
updated: ""
---
## Session Notes
Key findings, issues flagged, calculations performed, next mode to address...
```

On subsequent activations, read this file first and confirm with user whether context is still valid before proceeding.
