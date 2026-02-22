# Convertible Debt & SAFE

## Context

Use this reference when the user is structuring a seed round, choosing between SAFE and convertible notes, setting specific note terms, or preparing for conversion mechanics in an upcoming Series A. This is the primary reference for Convertible Debt Mode. Convertible instruments look simple but contain several traps — most notably the cap-as-ceiling problem and the conversion method ambiguity addressed in cap-table-math.md.

---

## What Convertible Debt Actually Is

A convertible note is a loan. Not equity. Until conversion, it sits on the company's balance sheet as a liability. In most early-stage startups, this means the company is technically insolvent: total liabilities (the note) exceed total assets. This creates meaningful legal risk that is almost universally ignored.

The insolvency point matters because it triggers a potential shift in fiduciary duties. In some states, when a company is insolvent, the board's duties extend to creditors — not just shareholders. Directors may face personal liability for decisions that favor equity holders over creditors. This is not theoretical; it has been litigated.

The investor accepts this structure because the conversion discount compensates for the risk of lending to an early-stage company rather than investing in equity at a negotiated price. Both parties are deferring the valuation conversation to a later date when there is more information.

---

## SAFE vs. Convertible Note: Decision Framework

SAFEs (Simple Agreement for Future Equity) were designed by Y Combinator in 2013 to streamline seed financings. They are not debt instruments — they are warrant-like agreements that convert upon a future equity event.

| Dimension | Convertible Note | SAFE |
|-----------|-----------------|------|
| Legal form | Debt (loan) | Warrant-like instrument |
| Balance sheet treatment | Liability (creates insolvency risk) | Not debt |
| Maturity date | Yes — typically 12-24 months | No maturity date |
| Interest rate | Yes — typically 5-12% per year | No interest |
| Conversion trigger | Qualified financing OR maturity | Next priced equity round |
| Investor leverage | Maturity date forces conversation | Investor has less structural leverage |
| Amendment complexity | Requires noteholder majority to amend | Simpler amendment |
| Legal cost | $5,000-$15,000 | $2,000-$5,000 |
| Ecosystem fit | Traditional investors, larger amounts | YC ecosystem, angels, small amounts |

**Use a convertible note when**:
- The investor is a traditional institution or family office that is uncomfortable with a non-debt instrument
- The amount is substantial (typically $500K+) and the investor wants structural protection
- The parties want maturity date as a forcing function to either convert or repay
- State law makes SAFE treatment uncertain (some non-Delaware states)

**Use a SAFE when**:
- Speed is critical — SAFEs can close in days vs. weeks for notes
- The stage is very early (pre-revenue, pre-product)
- The amount is smaller (seed checks of $25K-$250K)
- The investor is in the YC or angel ecosystem familiar with SAFE mechanics
- You want to eliminate insolvency risk from the balance sheet

For most founder-friendly seed rounds in 2019 and forward: SAFE is the better default, full stop. The legal cost savings and absence of insolvency risk are significant. The only reason to choose a note is investor preference or deal size.

---

## Economic Terms: Discount

The discount is the primary compensation mechanism for early-stage risk. The investor who lends money at the seed stage before there is much information, traction, or proof gets rewarded when the Series A price is set by a market-rate process.

**Standard range**: 10%-30%
**Most common**: 20%

How conversion works at a 20% discount:
```
Series A price: $1.00 per share
Note conversion price: $1.00 × (1 - 20%) = $0.80 per share
$100,000 note → $100,000 / $0.80 = 125,000 shares
New Series A investor paying $1.00 → $100,000 / $1.00 = 100,000 shares
```

The note investor receives 25% more shares than a new investor putting in the same amount. That extra 25% compensates for the additional risk of investing earlier.

**Red flag**: Discount AND warrants in the same note. Warrants give the investor additional shares on top of the discounted conversion. This is double compensation for the same early-stage risk. Push back — the standard is one compensation mechanism, not both.

**Negotiating the discount**: 15-20% is reasonable for most seed notes. 25-30% is aggressive investor-side. If an investor demands 30%, explore whether a higher cap would be an acceptable alternative, since caps and discounts serve overlapping economic purposes.

---

## Economic Terms: Valuation Cap

The cap puts an upper limit on the conversion price regardless of how high the Series A valuation is. Without a cap, a highly successful company's note investors may convert at an implied valuation far above what they risked capital for.

**Example without cap**:
- $100K note with 20% discount
- Series A closes at $20M pre-money, $1.00/share
- Note conversion at $0.80/share (20% discount applied to $1.00)
- Implied note valuation: $20M × (1 - 20%) = $16M — very high for seed stage

**Same note with $4M cap**:
- Note converts at effective valuation of $4M, not $16M
- $4M implied = $0.20/share (if Series A is at $1.00 with 2M shares pre-A)
- $100K / $0.20 = 500,000 shares (vs. 125,000 without cap)

The cap always applies when: `Cap price per share < Discount price per share`

Breakpoint formula — the Series A valuation above which the cap takes effect:
```
Break-even Series A valuation = Cap / (1 - Discount)
Example: $4M cap, 20% discount → $4M / 0.80 = $5M
```

At any Series A valuation above $5M, the $4M cap produces a lower conversion price than the 20% discount, so the cap governs.

**Setting the cap**: The cap should represent the "fair" valuation of the company at the time of the note, plus a margin to reward early commitment. If today's rough fair value is $3M-$4M, a $5M-$6M cap is reasonable. Caps below current fair value are unfair to founders; caps far above are unfair to investors.

---

## The Cap-as-Ceiling Trap

This is one of the most consequential and least-discussed risks of convertible notes. It is a structural problem that arises from information disclosure during Series A fundraising.

**How the trap works**:

1. Company raises $500K seed note with $4M cap.
2. Company grows: revenue triples, team builds, product proves out.
3. Company begins Series A fundraising — the company is genuinely worth $8M-$10M.
4. VC asks during diligence: "What are your existing note terms?"
5. Founder discloses the $4M cap.
6. VC thinks: "If the seed investors negotiated a $4M cap, that was the market consensus on this company's value at seed. I shouldn't pay dramatically more for the Series A."
7. VC offers $5M pre-money — barely above the cap — instead of $8M-$10M.

The note cap — intended as a ceiling on note conversion price — has become a floor on the Series A negotiation, suppressing the valuation well below what the company has earned.

**Mitigation strategies**:

Strategy 1: Do not disclose note terms until Series A price is verbally agreed.
Most founders disclose caps in the data room or during diligence before price is discussed. Reverse this. Get the VC to name a valuation or react to your ask before revealing note details. Once the VC has said "we're thinking $9M pre-money," the $4M cap is less relevant context.

Strategy 2: Set the cap higher than current fair value at time of note.
A $4M cap on a company worth $2M at seed is tighter than it needs to be. A $6M-$8M cap gives meaningful protection to investors while being harder to anchor a Series A valuation to.

Strategy 3: Frame the cap in context when disclosure is unavoidable.
"Our seed investors received a $4M cap reflecting the pre-product stage we were at 18 months ago. Since then we've hit [milestones]. We believe the appropriate valuation today is [X]." This reframes the cap as historical context, not current valuation evidence.

Strategy 4: Structure as SAFE without cap disclosure in data room.
Some founders give SAFEs to seed investors and only disclose them to Series A investors after price agreement. Ask your attorney about confidentiality provisions.

---

## Interest Rate

**Range**: 5%-12% annually
**Most common**: 8%
**Minimum allowable**: Applicable Federal Rate (AFR) — IRS minimum to avoid imputed interest income tax issues. Check current AFR; as of 2019 it was approximately 2-3% for short-term instruments.

The interest accrues on the note balance and converts alongside principal. At 8% interest, a $100K note outstanding for 12 months converts as $108K.

Practical significance of interest rate: low. The delta between 6% and 10% on a $200K note over 18 months is $8,000. The discount and cap will dwarf this economically. Do not spend significant negotiating capital on interest rate — agree to 8% and move on.

What matters more: whether the interest rate is simple or compound, and whether it starts from execution date or funding date. In most notes, interest is simple and starts from funding.

---

## Conversion in an Acquisition (Merger)

If the company is acquired before the note converts in a priced round, what happens?

This scenario is almost always underspecified in note documents and regularly leads to disputes. Three possible outcomes should be explicitly agreed to in the note:

**Option 1: Return of principal plus interest**
The note is treated as debt. Investor receives face value plus accrued interest in cash at closing. This is the technical legal default. Investors often reject it because they lose all equity upside.

**Option 2: Multiple on principal**
Investor receives a defined multiple of their principal (typically 1.5x-2x) plus interest. This is the most common negotiated outcome for acquisition-before-conversion scenarios. It gives investors some equity upside without requiring conversion mechanics to work in an M&A context.

**Option 3: Conversion into acquirer stock**
The note converts at the cap/discount price and the resulting shares are exchanged in the merger like all other shares. This is complex and acquirers often resist it because it creates unknown equity obligations. Possible only in stock-for-stock acquisitions.

Feld and Mendelson recommend always addressing this explicitly. The default (Option 1) is bad for investors and creates misaligned incentives — if founders know investors will get nothing but principal in an acquisition, investors have no reason to support an otherwise acceptable sale.

---

## MFN (Most Favored Nation) Clause

If the company issues subsequent convertible instruments with better terms (higher discount, lower cap, additional rights), MFN clauses give earlier note investors the automatic right to upgrade their terms to match.

**Example**:
- First note: $500K, 20% discount, $5M cap
- Second note (3 months later): $250K, 25% discount, $4M cap
- First note investor with MFN: automatically gets 25% discount AND $4M cap

MFN clauses are common in SAFE structures and reasonable in notes for small angel checks. They protect early investors from being disadvantaged if the company improves its terms to attract subsequent investors.

**Negotiating MFN**: Accept it for small seed investors whose relationship you want to preserve. Consider whether to exclude: (a) any note issued to an investor providing non-financial value (advisor, strategic partner), or (b) instruments with different structures (e.g., an MFN on discount/cap terms should not apply to pro rata rights or board observer seats).

---

## Pro Rata and Super Pro Rata Rights

**Standard pro rata**: The note investor may participate in the Series A round up to their pro-rata ownership percentage (based on post-conversion shares). Reasonable and standard.

**Super pro rata**: The investor can purchase a larger-than-proportional stake in the Series A. Defined either as a fixed percentage of the round (e.g., "10% of Series A") or as a multiple of their implied ownership (e.g., "2x pro rata").

Super pro rata creates problems in Series A:
- It may conflict with the lead VC's expected ownership
- It can prevent the lead VC from achieving their minimum ownership threshold
- It commits future financing capacity to seed investors before Series A terms are set

**Advice**: Agree to standard pro rata for all seed investors. Resist super pro rata unless the investor is providing extraordinary non-financial value (e.g., a domain expert or key customer reference). If super pro rata is granted, cap it at a specific share count (e.g., 100,000 shares maximum) rather than a percentage of the round.

---

## Amendment Mechanics and the Majority-Holder Problem

Convertible notes — especially multiple notes issued over time — require majority (or sometimes supermajority) holder consent to amend. This creates an underappreciated governance risk.

**The voting math problem**:
- $300K note from Investor A
- $200K note from Investor B
- Amendment requires majority by principal: Investor A (60%) can amend without Investor B's consent
- Amendment requires supermajority (67%): Same — Investor A alone is sufficient
- Amendment requires unanimity: Either investor has veto power

**Why this matters**: When the Series A requires amending note terms (changing the conversion trigger, extending maturity, adjusting cap), founders need to know in advance whether they can get the required consent. A 60/40 split between friendly and unfriendly investors can hold the Series A hostage.

Negotiate standard amendment threshold as majority of principal (not unanimity) before you issue the first note. Unanimous consent provisions should be avoided in multi-investor note rounds.

---

## Red Flags and Deal Structure Summary

**Red flags in note terms**:
- Discount >25% without compensating cap adjustment
- Cap anchored below current fair value
- Discount AND warrants (double compensation)
- No address of acquisition scenario
- Unanimity required for amendments
- Super pro rata >10% of next round
- Interest compounding (not simple)
- MFN that applies to board seats or non-economic terms

**Output format when advising on a specific note**:

```
CONVERTIBLE INSTRUMENT ANALYSIS — [Company]

Instrument type: [Note / SAFE]
Principal: $[amount]
Discount: [X]%
Cap: $[Y]M (or "uncapped")
Interest: [Z]% [simple/compound] (Note only)
Maturity: [N] months from [execution/funding] (Note only)
MFN: [Yes / No / Partial]
Pro rata: [Standard / Super pro rata — describe]
Acquisition treatment: [Option 1/2/3 or "not specified — flag"]
Amendment threshold: [Majority / Supermajority / Unanimous]

Break-even Series A valuation (cap governs above this): $[Cap / (1-Discount)]M

Key risks:
- Cap-as-ceiling risk: [High if cap is below current fair value estimate]
- Maturity pressure: [Note maturity date; months to Series A target]
- Insolvency concern: [Summarize balance sheet position]
- Conversion method: [Specified / Not specified — recommend addressing]

Recommendation: [Specific prioritized advice]
```
