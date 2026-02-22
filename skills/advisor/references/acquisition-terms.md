# Acquisition Terms

## Context

When user has received a Letter of Intent (LOI), is evaluating an acquisition offer, or needs to understand how acquisition deal structure differs from venture financing. Also relevant when a term in an LOI needs explanation or when user is preparing to negotiate an acquisition. Primary reference for Deal Structure Mode.

---

## Mindset Shift: Acquisitions vs. Financings

A venture financing is an expanding pie — both sides can win. An acquisition is a fixed pie. The buyer wants to pay as little as possible; the seller wants to receive as much as possible. The negotiating tone is tougher, the advisors are more adversarial, and the stakes at each clause are higher because there is no ongoing relationship to protect after closing.

The LOI is the first real negotiation. Treat the headline number as the best-case purchase price — the actual amount flowing to shareholders almost always falls below it once structure, escrow, earnouts, and working capital adjustments are applied.

---

## LOI Anatomy

The LOI is mostly non-binding. Two provisions ARE binding:

1. **No-shop clause** — seller cannot solicit or engage with other buyers for a defined period
2. **Confidentiality** — terms of the LOI are not disclosed

Everything else — price, structure, representations — is non-binding but sets the baseline for negotiation. The binding nature of the no-shop combined with the non-binding nature of price creates asymmetry: the buyer can renegotiate price after signing, but the seller cannot talk to other buyers.

---

## Purchase Price Deconstruction

When an offer says "$150M," always break it into components before reacting.

| Component | Example Amount | Certainty |
|---|---|---|
| Cash at closing | $105M | Certain at close |
| Escrow / holdback | $15M (held from above) | At risk 12-24 months |
| Working capital adjustment | Variable | Reduces if company misses WC target |
| Earnout | $40M | May or may not be paid |
| Management retention pool | $10M | Paid to employees over time post-close |

**Real certain value in this example**: $90M ($105M - $15M escrow)
**Potential full value**: $150M (if escrow released + earnout achieved)

Before responding to any offer, determine:
- Is the management retention pool INSIDE the purchase price or ON TOP of it?
- What is the earnout structure — what metrics, who controls them, how long is the measurement period?
- What is the escrow percentage and duration?
- What is the working capital requirement and what happens if you are short?

---

## Asset Deal vs. Stock Deal

### Asset Deal

Buyer acquires specifically listed assets — intellectual property, contracts, equipment, customer relationships. The corporate entity continues to exist after closing. What the buyer does NOT acquire: liabilities, bad contracts, pending lawsuits, obligations to creditors.

Consequences for sellers:
- The legal entity (corporation) still exists after the deal closes and must be separately wound down
- Officers and directors remain on the hook for the continuing entity's obligations
- Tax treatment differs from a stock deal (consult tax counsel)
- More common in distressed situations where the buyer has legitimate reasons to avoid specific liabilities

### Stock Deal

Buyer acquires the entire company — all assets and all liabilities. The company ceases to exist independently at closing. Nothing to wind down separately.

**Push for a stock deal** unless:
- The company has serious undisclosed liabilities the buyer legitimately needs protection from
- Tax optimization specifically requires an asset structure (rare for early-stage companies)
- The company is in severe financial distress

Counter the buyer's asset deal preference with: a stock deal can be structured to provide the buyer with functionally equivalent protection through representations, warranties, indemnification, and escrow — with substantially less post-closing complexity for the seller.

---

## Form of Consideration

### Cash

Certain value. Simple. Easy to model. The standard in most healthy VC-backed acquisitions.

### Public Acquirer Stock

- Value fluctuates between signing and closing
- May have lockup restrictions preventing you from selling for 6-18 months after closing
- Check whether the shares are freely tradable on delivery
- If the acquisition closes but the stock price drops 30% before your lockup expires, your real consideration is 30% less than expected
- Often worth taking for strong public companies with stable stock prices; more risky for volatile public companies

### Private Acquirer Stock

The most dangerous form of consideration. Private stock has no current liquidity and opaque value. To evaluate it properly, you need the acquirer's complete capitalization table and full liquidation preference stack.

**Example of private stock trap**:
- Acquirer is valued at $300M, offers you $15M in common stock — nominally a 5% ownership stake
- But acquirer has raised $110M in financing with participating preferred stock sitting above common
- Your $15M of common stock sits UNDERNEATH $110M of liquidation preferences
- In any realistic exit scenario, common stock receives only what is left after preferred is satisfied
- The actual value of your $15M in common stock may be dramatically less than $15M — potentially zero in a non-spectacular exit

Always request the full cap table and preference waterfall of any acquirer offering private stock. Model the value of your stake under multiple exit scenarios (1.5x, 2x, 3x the current valuation). Do not accept the stated valuation as the relevant figure.

---

## Escrow (Holdback)

### Standard Structure

- 10-20% of purchase price held by a third-party escrow agent at closing
- Duration: 12-24 months after closing
- Serves as the "sole remedy" for buyer claims of breaches of representations and warranties
- Most claims against the seller must be satisfied from escrow, not from direct payment

### Carve-Outs (Fundamental Representations)

Certain categories of breach are NOT limited to the escrow amount. These are the "fundamental reps" and exposure on them may extend up to the full purchase price (and in the case of fraud, potentially beyond):

- Fraud by any seller
- Capitalization errors (cap table misrepresentation)
- Tax issues, including incorrect 409A valuations
- IP ownership (increasingly common as a carve-out)
- Authorization and authority

Maximum escrow exposure should never exceed the total deal value. If a buyer requests unlimited indemnification on any category, push back hard.

### Negotiation Points

- Percentage: Push for 10% rather than 20%
- Duration: Push for 12 months rather than 24 months
- Define the claims process with clear deadlines and dispute resolution
- In stock deals: address what happens to escrow value if the acquirer's stock price declines during the holdback period

---

## Earnout

An earnout is a mechanism allowing the buyer to pay less at closing while promising additional consideration if the company hits defined milestones after closing. The "earn" in "earnout" is literal — you earn the additional payment by achieving targets.

Earnouts are almost always worse for sellers than they appear.

### Red Flag 1: Buyer Controls the Inputs

After acquisition, the buyer controls:
- Hiring and staffing decisions
- Marketing and sales spend and strategy
- Product roadmap priorities
- Pricing decisions
- How revenue is recognized and reported

If any of these factors affect your earnout metric, the buyer can — intentionally or not — make it difficult to achieve your targets. This does not require bad faith. Normal acquisition integration decisions routinely derail earnouts.

**Example**: Earnout tied to revenue from new customer acquisition. Buyer redirects your sales team to cross-selling existing buyer customers. Your pipeline evaporates. Earnout missed. No additional consideration paid.

### Red Flag 2: Measurement Complexity

Revenue-based earnouts seem objective but require precise definitions:
- What is "revenue"? Recognized under GAAP, or billings, or collections?
- Which customers count? Existing customers, new customers, or both?
- What about returns, refunds, or disputed invoices?
- What happens if the buyer changes pricing?

EBITDA-based earnouts are worse — buyers control costs that directly affect EBITDA.

Product milestone earnouts are worst of all:
- "Completion" of a feature is subjective
- Who controls engineering resources? The buyer.
- Who defines the acceptance criteria? Typically the buyer.
- What if priorities change after acquisition?

### Earnout Best Practices

- Use objective, externally verifiable metrics — revenue recognized under GAAP is better than virtually all alternatives
- Keep the measurement period short — 12 months maximum if possible, 18-24 months only with strong protections
- Ensure the seller team retains meaningful control over the resources needed to achieve targets
- Include an acceleration clause: if buyer takes specific actions that prevent achievement (redeploying resources, changing product direction), earnout accelerates and becomes immediately payable
- Negotiate detailed earnout covenants describing exactly how the business will be operated during the earnout period
- Ask yourself: would you accept this deal on the guaranteed consideration alone, without the earnout? If the answer is no, you are making a bet on a mechanism that favors the buyer. Negotiate harder on the guaranteed amount instead.

---

## Management Retention Pool

The buyer sets aside money to retain key employees after the acquisition closes.

### Where It Sits

- **Inside the purchase price**: $10M retention pool out of $150M total means shareholders actually receive $140M. The $10M is already included in the headline number.
- **On top of the purchase price**: $10M retention pool plus $150M means shareholders receive $150M and employees receive their retention separately.

Always clarify which structure applies before reacting to any headline number. This is one of the most commonly misunderstood elements of acquisition terms.

### The Wedge Problem

Buyers sometimes use the retention pool structure to create tension between management and investors:
- Management may prefer a larger retention pool (more personal compensation)
- Investors want a smaller pool (more going to shareholders)
- Management's fiduciary duty runs to shareholders, but their personal economic interest runs to their own pool

Resolve this dynamic explicitly and early with your board. Decide as a company what retention structure is acceptable before entering negotiations, so you are not divided against each other during them.

### Vesting and Conditions

Retention pool payments are typically tied to continued employment for 2-4 years post-closing. If a key employee leaves before the retention period ends, their unvested amount is forfeited — usually returned to the acquirer, not redistributed to shareholders. Negotiate the forfeiture treatment carefully.

---

## No-Shop Clause

### What It Does

Prevents the seller from soliciting, entertaining, or encouraging acquisition interest from other parties for a defined period.

### Standard Terms and What to Push For

- Standard duration: 45-60 days. Push back on anything longer.
- No-shop is unilateral — the buyer can walk away at any time. The seller is bound for the full duration.
- Include explicit automatic termination if buyer withdraws

### Expiration as a Leverage Moment

Buyers typically call 2-3 days before no-shop expiration to request an extension. At this moment, the seller has genuine leverage — the buyer has invested significant time and legal fees and does not want to restart the process. Use this moment for specific, targeted concessions:

- Relief on the working capital adjustment calculation
- Resolution of a contested representation or warranty
- A specific earnout protection clause
- Short-term bridge financing from the buyer if the deal timeline has extended your runway

Do not overreach. Extracting too much at this moment damages the relationship entering the final phase of the deal.

### Carve-Outs to Request

Negotiate carve-outs from the no-shop prohibition for:
- Existing financing conversations already in progress (at minimum, any inside financing from current investors)
- Unsolicited approaches from other buyers (require notification to buyer but allow discussion)

---

## Representations and Warranties

### What They Are

Statements of fact about the company that sellers make to the buyer. If they turn out to be false, the buyer has a claim against escrow.

### Who Makes Them

Push for the COMPANY to make representations — not individual shareholders, not individual VCs, not founders personally. When a VC signs a merger agreement as an individual rep-maker, they expose their own assets to claims. Standard practice is for the company to be the rep-making party with escrow as the remedy.

### Key Seller Representations

- IP ownership and chain of title
- Accuracy of financial statements
- No undisclosed liabilities
- Compliance with all material contracts
- Tax compliance (specifically including 409A accuracy)
- Employee matters (including 83(b) election compliance)
- Accurate and complete capitalization table
- No pending litigation or regulatory proceedings
- Intellectual property non-infringement

### Qualification Language

Push for "to the Company's knowledge" qualifications on representations wherever the buyer will accept it. This limits exposure to known issues — you are not representing that something unknown has never occurred. Buyers typically resist knowledge qualifications on:
- Capitalization (the cap table should be exactly right)
- IP chain of title (this should be verified, not approximated)
- Tax matters (including 409A)

### Survival Period

Representations survive closing for a defined period, typically matching the escrow duration (12-24 months). After the survival period, no claims can be brought even if a breach is later discovered. Fundamental representations survive longer, sometimes indefinitely. Fraud claims typically have no survival limitation.

---

## Stock Options in Acquisition

### Four Treatment Options

**1. Assumption**: Acquirer assumes the option plan and converts options into options on acquirer stock. Value is preserved but converted. Unvested options continue on original vesting schedule. This is the most employee-friendly approach. Cost comes off the purchase price.

**2. Substitution**: Acquirer replaces options with RSUs or a cash-based incentive plan. More common due to accounting and tax preferences. Functionally similar to assumption but structurally different.

**3. Cancellation with acceleration**: Options not assumed by the acquirer vest immediately at closing. Employees cash out at the acquisition price minus their exercise price. This is generous for employees but creates a "who contributed" problem — an employee hired 90 days ago gets the same acceleration benefit as a founder who worked for five years.

**4. Revesting**: Acquirer assumes options but imposes a new vesting schedule on the converted awards. A founder with 2 years already vested must re-vest their remaining unvested options over 2-4 years at the acquirer. Costs the acquirer nothing but retains talent. Most common for key employees the acquirer most wants to retain.

### Exercise Price Impact

Option economics at acquisition: option value = (per-share acquisition price) − (exercise price).

If the acquisition price is $1.00 per share and an employee's exercise price is $0.40, each option is worth $0.60. Options issued at higher 409A strike prices are worth less. This matters for modeling total option pool cost and for understanding employee economics at exit.

---

## Shareholder Representative

After closing, someone must manage post-closing escrow claims, earnout calculations, audits, disputes, and any litigation arising from pre-closing events.

### Who Should NOT Serve as Shareholder Rep

- Employees who will work for the acquirer after closing — they face direct conflict of interest
- A VC who is primarily occupied managing a large portfolio — risk of missed deadlines, example from the book: one VC missed a 30-day notice period required to preserve a claim because the task fell through the cracks at a busy firm

### Professional Shareholder Representatives

Firms like SRS Acquiom exist specifically to serve as professional shareholder representatives. They:
- Are full-time, focused on exactly this function
- Do not have conflicts with the acquirer
- Know the claim deadlines and process requirements
- Charge modest fees (often funded by an expense pool negotiated in the merger agreement)

Negotiate an expense pool for the shareholder representative function in the merger agreement itself. This pool funds the rep's fees and any litigation costs without requiring shareholders to contribute after the fact.
