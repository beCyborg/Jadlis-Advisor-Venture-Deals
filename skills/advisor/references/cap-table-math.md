# Cap Table Math

## Context

Use this reference when the user needs to model ownership, calculate dilution, understand the option pool shuffle mechanics, convert notes into equity, or verify a proposed cap table. This is the primary reference for Cap Table Mode. The calculations here are exact — use them to produce precise outputs, not estimates. Always verify by checking that all ownership percentages sum to 100% and that shares × price per share equals the correct valuation.

---

## Foundational Formula

```
Price per share = Pre-money valuation / Fully diluted shares outstanding
```

"Fully diluted" is the most important term in this formula and the most commonly misapplied.

Fully diluted shares includes ALL of the following:
- All common stock (founders, employees, past exercises)
- All preferred stock on an as-converted-to-common basis (1:1 in most cases)
- All options and warrants outstanding (granted, whether or not vested)
- All ungranted options in the existing option pool
- The NEW option pool expansion required by the term sheet (this is the shuffle)

The new pool expansion is included in the denominator BEFORE the investor's shares are added. This means the pool dilutes only founders and existing holders, not the incoming investor.

---

## Complete Cap Table Walk-Through

**Scenario**: 2,000,000 founders' shares outstanding. Term sheet: $5M investment at $10M pre-money valuation. VC requires 20% post-money option pool.

### Step 1: Determine Post-Money

```
Post-money = Pre-money + Investment
Post-money = $10M + $5M = $15M
```

### Step 2: Determine VC Ownership

```
VC ownership = Investment / Post-money
VC ownership = $5M / $15M = 33.33%
```

### Step 3: Determine Option Pool Size (post-money percentage)

Pool must be 20% post-money. The pool is created from the pre-money — it dilutes the pre-money holders before the VC arrives.

```
Pool dollar value = Post-money × Pool%
Pool dollar value = $15M × 20% = $3M
```

### Step 4: Determine Founders' Effective Value

```
Founders' value = Pre-money - Pool dollar value
Founders' value = $10M - $3M = $7M

Founders' ownership = Founders' value / Post-money
Founders' ownership = $7M / $15M = 46.67%
```

### Step 5: Calculate Price Per Share

```
Total pre-money value = Founders' shares value + Pool value
$10M = (Founders' shares × Price) + (Pool shares × Price)
$10M = (2,000,000 + Pool shares) × Price
```

Since the pool represents $3M of value:
```
Pool shares = $3M / Price
2,000,000 × Price + $3M = $10M
2,000,000 × Price = $7M
Price = $3.50 per share
```

### Step 6: Calculate Pool and VC Shares

```
Pool shares = $3M / $3.50 = 857,143 shares
VC shares   = $5M / $3.50 = 1,428,571 shares
```

### Step 7: Final Cap Table

| Stockholder | Shares | Ownership | Implied Value |
|------------|--------|-----------|---------------|
| Founders | 2,000,000 | 46.67% | $7,000,000 |
| Option Pool | 857,143 | 20.00% | $3,000,000 |
| VC (Series A Preferred) | 1,428,571 | 33.33% | $5,000,000 |
| **Total** | **4,285,714** | **100.00%** | **$15,000,000** |

### Verification

```
(Founders + Pool) × Price = Pre-money
(2,000,000 + 857,143) × $3.50 = 2,857,143 × $3.50 = $10,000,000 ✓

VC shares × Price = Investment
1,428,571 × $3.50 = $5,000,000 ✓

All ownership: 46.67% + 20.00% + 33.33% = 100.00% ✓
```

---

## The Option Pool Shuffle

This is the valuation trap that Feld and Mendelson identify explicitly. Founders agree to a headline pre-money number but do not realize that the option pool expansion reduces their effective pre-money.

**What founders think they agreed to**: $10M pre-money → founders own $10M of value
**What actually happened**: Founders own $7M of value (pre-money minus pool)

The VC's stated "$10M pre-money" is technically correct — the pre-money is $10M. But the founders are measured against the post-money: they own 46.67%, not 66.67%.

The investor's percentage is unaffected by pool size. The pool comes entirely from founders (and any existing investors). This is the shuffle: value is shuffled from founders to future employees before the VC arrives.

### Negotiating the Shuffle

**Approach 1: Build an option budget**

List every planned hire over the next 12-18 months and the equity grant each requires. If the plan calls for 300,000 options total, ask for a 15% pool (give a buffer), not 20%. VCs who insist on 20% without reviewing your budget are adding unwarranted dilution.

Example defense: "Our hiring plan for the next 18 months requires 350,000 options. At today's fully diluted count that's approximately 12% of the company. We're asking for a 15% pool to give us a reasonable buffer."

**Approach 2: Ask for higher pre-money**

"We'll accept 20% post-money pool if you increase the pre-money to $12M." Run the math — at $12M pre-money with 20% pool: founders get $12M - ($17M × 20%) = $12M - $3.4M = $8.6M effective value. That's better than $10M pre-money with 15% pool where founders get $10M - ($15M × 15%) = $10M - $2.25M = $7.75M.

**Approach 3: Propose post-money pool** (rarely accepted)

Pool expansion comes from post-money, shared proportionally with the VC. VCs refuse this because it dilutes their ownership and defeats the purpose of requiring a pre-financing pool. Propose it once; if refused, move to Approach 1.

---

## Three Convertible Note Conversion Methods

When convertible notes convert in a Series A, there are three distinct mathematical methods. The method determines who absorbs the dilution from the discount. This is almost never specified in the term sheet — raise it explicitly before signing.

**Assumptions for all three methods**:
- Agreed pre-money: $8M
- Agreed new investment (Series A): $2M
- Existing outstanding notes: $1M (principal + accrued interest)
- Note discount: 30%
- Existing shares outstanding: 1,000,000

---

### Method 1: Pre-Money Method (Most Common)

The pre-money valuation is fixed. Note conversion happens at the discounted price. Series A investors get whatever percentage results.

```
Series A price = $8M / 1,000,000 = $8.00 per share
Note conversion price = $8.00 × (1 - 30%) = $5.60 per share
Note shares = $1,000,000 / $5.60 = 178,571 shares
Series A shares = $2,000,000 / $8.00 = 250,000 shares
```

| Stockholder | Shares | Ownership |
|------------|--------|-----------|
| Founders | 1,000,000 | 70.0% |
| Noteholders | 178,571 | 12.5% |
| Series A | 250,000 | 17.5% |
| **Total** | **1,428,571** | **100.0%** |

Series A receives 17.5%, not 20%. Both founders AND Series A are diluted by note conversion.
Implied post-money: $8M + $2M + $1M × ($8/$5.60) = $11.43M

This method is best for founders — the dilution from the note discount is shared.

---

### Method 2: Percentage-Ownership Method

The Series A percentage is fixed at what it would be without notes (20%). Everything is solved backward from that constraint. Founders absorb ALL dilution from the note discount.

Solving for price per share such that Series A gets exactly 20%:

```
Let x = price per share for Series A
Note conversion price = 0.70x

Total shares = 1,000,000 + ($1M / 0.70x) + ($2M / x)
Series A ownership = ($2M / x) / Total shares = 20%

Solving: x ≈ $6.57 per share
Note price: $6.57 × 0.70 = $4.60 per share
Note shares: $1M / $4.60 = 217,391 shares
Series A shares: $2M / $6.57 = 304,348 shares
```

| Stockholder | Shares | Ownership |
|------------|--------|-----------|
| Founders | 1,000,000 | 65.71% |
| Noteholders | 217,391 | 14.29% |
| Series A | 304,348 | 20.00% |
| **Total** | **1,521,739** | **100.0%** |

Founders bear all the dilution from the note discount. Implied pre-money: $6.57M (not $8M as agreed). This is effectively repricing the deal post-agreement.

Founders should flag this as a material deviation from the negotiated pre-money. It can reopen valuation discussions.

---

### Method 3: Dollars-Invested Method (Compromise)

Post-money is defined as pre-money + ALL dollars invested, including converting notes. Note conversion is treated as an additional investment dollar-for-dollar.

```
Post-money = $8M + $2M + $1M = $11M

Solve for price: Let x = price per share
Total shares = 1,000,000 + ($1M / 0.70x) + ($2M / x)
Total shares × x = $11M

Solving: x ≈ $7.57 per share
Note price: $7.57 × 0.70 = $5.30 per share
Note shares: $1M / $5.30 = 188,679 shares
Series A shares: $2M / $7.57 = 264,151 shares
```

| Stockholder | Shares | Ownership |
|------------|--------|-----------|
| Founders | 1,000,000 | 68.83% |
| Noteholders | 188,679 | 12.99% |
| Series A | 264,151 | 18.18% |
| **Total** | **1,452,830** | **100.0%** |

Founders absorb MOST but not all of the note discount dilution. Series A gets slightly less than 20%. A middle-ground that both sides can usually accept.

---

### Choosing the Right Method

| Method | Dilution from notes absorbed by | Series A % | Founder-friendly? |
|--------|--------------------------------|------------|-------------------|
| Pre-Money | Founders AND Series A (shared) | <20% | Most |
| Dollars-Invested | Mostly founders, slightly Series A | ~18% | Middle |
| Percentage-Ownership | Founders entirely | Exactly 20% | Least |

Practical advice: Founders should push for Method 1 (Pre-Money). If the VC insists on Method 2, treat it as reopening the pre-money valuation negotiation. If neither party wants to reopen the deal, Method 3 is the natural compromise.

Most importantly: Specify the method explicitly in the term sheet or note amendment before the Series A closes.

---

## Antidilution Weighted Average Calculation

When a down round occurs, broad-based weighted average antidilution adjusts the conversion price of existing preferred shares.

```
NCP = OCP × (CSO + CSP) / (CSO + CSAP)

NCP  = New conversion price (after adjustment)
OCP  = Old conversion price (pre-adjustment)
CSO  = Fully diluted shares outstanding before down round (all common + preferred + options)
CSP  = Shares that would have been issued at old price with the new money raised
CSAP = Shares actually issued in the down round
```

**Example**:
- Series A price: $5.00/share
- Fully diluted shares before down round: 2,000,000
- Down round: raises $1.5M at $3.00/share → 500,000 new shares

```
CSO = 2,000,000
CSP = ($1.5M at $5.00) = $1,500,000 / $5.00 = 300,000 shares
CSAP = 500,000 shares

NCP = $5.00 × (2,000,000 + 300,000) / (2,000,000 + 500,000)
NCP = $5.00 × 2,300,000 / 2,500,000
NCP = $5.00 × 0.92
NCP = $4.60
```

Series A conversion price adjusts from $5.00 to $4.60. On conversion, Series A investors receive $5.00/$4.60 = 1.087 shares per original preferred share — an 8.7% increase in share count.

**Full ratchet comparison**: Would reprice from $5.00 to $3.00 — investors would receive $5.00/$3.00 = 1.667 shares per original preferred share — a 66.7% increase. Massively dilutive to founders and common.

The denominator in broad-based includes all options (granted and ungranted). Narrow-based uses a smaller denominator (typically just common shares outstanding), producing a lower NCP and more dilution. Know which you have.

---

## Multi-Round Dilution Modeling

For founders who want to model total dilution through multiple financing rounds:

**Ownership after each round**:
```
Post-round ownership = Pre-round ownership × (1 - New investor %)
```

Example: Starting at 80% after Series Seed:
- Series A (25% to new investors): 80% × 0.75 = 60%
- Series B (20% to new investors): 60% × 0.80 = 48%
- Series C (15% to new investors): 48% × 0.85 = 40.8%

This approximation assumes no other dilution. In reality, option pool expansions at each round add additional dilution (each typically 5-10% post-money).

**More accurate multi-round formula with pools**:
Each round: new founder ownership = old founder ownership × (1 - VC%) × (1 - Pool%)

Using 20% VC + 10% pool each round from 80% starting point:
- Post Series A: 80% × 0.80 × 0.90 = 57.6%
- Post Series B: 57.6% × 0.80 × 0.90 = 41.5%
- Post Series C: 41.5% × 0.80 × 0.90 = 29.9%

Three rounds of institutional financing typically takes a founding team from 100% to roughly 25-35% ownership, depending on pool sizes and round economics.

---

## Verification Checklist

After any cap table calculation:

1. All percentage ownership sums to exactly 100.00%
2. (Total shares) × (Price per share) = Post-money valuation
3. (Founders' shares + Option pool shares) × (Price per share) = Pre-money valuation
4. VC shares × Price per share = Investment amount
5. Option pool is calculated as a percentage of POST-money, sourced from PRE-money
6. All notes are converted at the correct discount and/or cap (whichever is lower price)
7. Note conversion method is explicitly agreed and applied consistently
8. Antidilution adjustments use the agreed formula (broad-based vs. narrow-based)
9. Price per share is consistent to 4+ significant digits before rounding
10. Fully diluted share count includes unissued pool shares, not just granted options
