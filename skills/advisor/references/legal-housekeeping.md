# Legal Housekeeping

## Context

When user needs to audit legal hygiene before a fundraise or acquisition, or asks about a specific legal item — IP assignment, 83(b) elections, 409A valuations, corporate structure, or accredited investor status. Primary reference for Legal Check Mode. Also relevant any time due diligence surfaces a potential legal issue.

---

## The 5-Item Legal Audit

These are the five legal items that most commonly delay, reduce the value of, or kill venture financings and acquisitions. A clean company has all five in order before it starts raising money or engaging with acquisition interest. Missing any of them creates a liability that either kills the deal or shifts bargaining power to the other side.

| # | Item | Key Deadline | Consequence if Missed |
|---|---|---|---|
| 1 | IP Assignment Chain | Before fundraise | VC pauses or kills deal; acquisition reps trigger escrow claims |
| 2 | Corporate Structure | At incorporation | Requires restructuring (costs $5-15K+, takes weeks) |
| 3 | 409A Valuation | Valid every 12 months | Tax penalties on employees; carve-out from escrow cap in acquisition |
| 4 | 83(b) Election | 30 days from grant date | Cannot be cured; ordinary income tax on all future vesting |
| 5 | Accredited Investor Status | At each financing | Right of rescission — permanent liability on company books |

---

## 1. IP Assignment Chain

### What It Means

Every piece of intellectual property the company uses must have a documented chain of ownership leading unambiguously back to the company. Any gap — any code, patent, trademark, or trade secret without a clear assignment — is a potential claim on your IP by someone outside the company.

### The Four Common Gaps

**Gap 1: Pre-incorporation work**

Founders write code, draft designs, or develop the initial product before the company is formally incorporated. That work is owned by the founders as individuals, not by the company, because the company did not yet exist.

Fix required: A written IP assignment agreement from each founder, specifically transferring all pre-incorporation work to the company. This should be signed at or immediately after incorporation. Investors will ask for this document in due diligence.

**Gap 2: Contractor work**

You hired a contractor, paid them, received deliverables, and assume you own the work. You almost certainly do not. Under US copyright law, work created by an independent contractor is NOT "work for hire" unless the contract explicitly says so in those terms AND the work falls into one of the statutory categories for work made for hire.

Fix required: Every contractor agreement must include (a) a specific work-for-hire clause using statutory language, and (b) a backup IP assignment provision transferring ownership to the company for any work that does not qualify as work for hire. Having only one of these is insufficient.

**Gap 3: Prior employer IP obligations**

A key engineer or executive signed an IP assignment agreement and a non-compete with their previous employer. The prior employer may have a legitimate claim that work your employee created at your company belongs to them — particularly if the work is in a related technology area or if the work was begun during the overlap period.

Fix required: Review every key employee's prior employer obligations before they start work. In California, overly broad non-competes are unenforceable, but IP assignment provisions can still apply. In other states, non-competes may be enforceable and complicate the picture substantially. Get employment counsel involved for any senior hires coming from competitors or from companies in adjacent technical areas.

**Gap 4: Open Source Contamination**

GPL (GNU General Public License) and certain other copyleft licenses require that any derivative work also be licensed under the same terms. If your core product incorporates GPL-licensed code, you may be legally required to open-source your proprietary codebase.

This is not theoretical. A few lines of GPL code in the wrong place can trigger a disclosure obligation on your entire product. Acquirers and sophisticated VCs always check for this.

Fix required: Conduct an open source audit of your entire codebase before any significant financing or acquisition. Map every open source library, identify its license, and determine whether any copyleft licenses create disclosure obligations. Tools like FOSSA, Black Duck, and WhiteSource automate much of this process.

### IP Audit Checklist

- [ ] All founders signed IP assignment for pre-incorporation work
- [ ] All employees signed a Proprietary Information and Inventions Agreement (PIIA) at hire
- [ ] All contractor agreements contain both work-for-hire language and IP assignment backup
- [ ] Prior employer obligations reviewed for all key technical employees
- [ ] Open source audit completed for core product components
- [ ] No pending IP disputes, claims, or demands from third parties

---

## 2. Corporate Structure

### The Right Structure for VC-Backed Companies

A Delaware C-Corporation is the only practical structure for a company intending to raise venture capital.

**Why Delaware specifically**:
- The most developed body of corporate law in the US
- Court of Chancery is a specialized court with judge-only proceedings (no juries), focused exclusively on business disputes
- Enormous body of precedent providing predictability on governance, fiduciary duty, and shareholder rights
- Standard VC documents are drafted for Delaware law — using another state's law creates legal friction at every step

**Why C-Corp specifically**:
- Allows multiple classes of stock — required for preferred stock, which is the foundation of all VC deal structures
- No limit on number of shareholders
- Required for institutional investors, employee option plans, and public markets

### Why Not Other Structures

**S-Corp**: Single-level taxation (a genuine advantage for small businesses), but cannot have more than 100 shareholders, cannot have non-US shareholders, and cannot have multiple classes of stock with different economic rights. The moment you want a preferred/common stock split, S-Corp status is automatically lost.

**LLC**: Uses membership units rather than shares of stock. Employee option plans are awkward with LLC interests. Tax treatment of carried interests from LLC equity can be complex for VC investors. Some institutional investors (pension funds, university endowments) have restrictions on investing in pass-through entities. In practice, virtually no VC-backed company remains an LLC.

**Foreign corporations or other state incorporations**: California is the most common mistake — California corporate law is significantly more restrictive than Delaware on many governance matters, and the default rules are less favorable to the flexibility that venture-backed companies require.

### Restructuring Cost

Converting from an LLC or S-Corp to a Delaware C-Corp after raising angel money or starting operations costs $5,000-15,000+ in legal fees, takes 2-6 weeks, and may trigger a taxable event for existing equity holders. Incorporating correctly from the start costs nothing extra. Fix this at day zero.

---

## 3. Section 409A Valuations

### The Core Requirement

Section 409A of the Internal Revenue Code requires that stock options be granted at no less than fair market value (FMV) of the common stock on the grant date. Before 409A (pre-2004), boards set FMV themselves — often at 10% of the preferred price. Now, a valid FMV determination requires either an independent appraisal (the "safe harbor") or the company bearing the burden of proving its own valuation was correct.

The safe harbor means: hire a qualified independent appraiser, follow the required methodology, and the IRS must prove your valuation was wrong (their burden). Without the safe harbor, you must prove it was right (your burden). Take the safe harbor.

### Validity Window and Required Updates

A 409A valuation is valid for 12 months. You must obtain a new valuation:
- When the prior valuation expires (12 months)
- After any "material event" that would affect FMV — examples: a new financing round, a term sheet for acquisition, significant change in revenue trajectory, key customer win or loss, completion of a major product milestone

During a material event review period, you cannot legally grant options until the new 409A is complete. This creates practical scheduling problems if you are not tracking expiration dates.

### Current Pricing Realities

Early-stage common stock is typically valued at 20-30% of the most recent preferred price. (Before 409A, it was often 10%.) A company that raised a Series A at $2.00 per share of preferred will typically receive a 409A common stock valuation of approximately $0.40-0.60 per share.

Higher exercise prices mean less option profit for employees at exit. This is one of the reasons later-stage option grants are often less valuable than early-stage grants — strike prices are higher, and the spread to an exit value is narrower.

### Cost and Providers

- Traditional 409A firms: $5,000-15,000 per valuation
- Platform-based providers (Carta, Pulley): often included in equity management subscription pricing
- Timing: typically 1-2 weeks from engagement to delivery

### Consequences of Non-Compliance

If options are granted at below-FMV:
- Employees owe a 20% excise tax on the entire option gain (not just the discount) in the year the option vests
- Plus interest on delayed payment
- California imposes an additional state-level penalty
- In an acquisition: buyers carve out 409A risk as a fundamental representation with potentially unlimited escrow exposure

This is one of the few legal items where the consequence flows primarily to your employees rather than to you as a founder. Non-compliance is a direct financial harm to the people you hired.

---

## 4. Section 83(b) Elections

### The Underlying Tax Rule

Restricted stock (common stock subject to vesting) is taxed as ordinary income when it vests — not when it is granted. Without an 83(b) election, each vesting event is a taxable transaction at the then-current fair market value.

As the company grows and common stock FMV increases, each vesting event creates a larger and larger ordinary income tax bill — on stock you may not be able to sell.

### What 83(b) Changes

An 83(b) election tells the IRS: "Tax me now, today, on the current value of this stock. I accept this tax in exchange for treating all future appreciation as capital gains."

**Without 83(b) — founder with 1,000,000 shares at $0.001, 4-year vesting**:
- Year 1: 250,000 shares vest. FMV is now $0.50/share. Ordinary income: $124,750. Tax due at ~37%: ~$46,000. In cash. On stock you cannot yet sell.
- Year 2: 250,000 shares vest. FMV is now $1.00/share. Ordinary income: $249,750. Tax due: ~$92,000.
- Year 3: 250,000 shares vest. FMV $2.00. Tax: ~$185,000.
- Year 4: 250,000 shares vest. FMV $2.00. Tax: ~$185,000.
- Total ordinary income taxes paid: ~$508,000

**With 83(b) — same scenario**:
- Day of grant: 1,000,000 shares at $0.001 = $1,000 of value. Ordinary income tax: ~$370.
- All subsequent appreciation is taxed as long-term capital gains (20% or less), not ordinary income (up to 37%)
- No taxable event at each vesting date
- Total ordinary income taxes paid: ~$370

The 83(b) election saves hundreds of thousands of dollars in ordinary income taxes in virtually every successful startup outcome.

### The Absolute 30-Day Deadline

The 83(b) election must be filed with the IRS within 30 days of the stock grant date.

This deadline is:
- Absolute — no extensions, no exceptions, no reasonable cause exceptions
- Cannot be cured after it passes — there is no late-filing option, no petition, no remedy
- Retroactive correction is impossible even with court intervention

This is the one startup legal requirement where missing the deadline creates a permanent, uncorrectable problem.

### How to File

1. Complete the IRS 83(b) election form (standard template available from any startup attorney)
2. Mail to the IRS Service Center where you file your personal tax return — within 30 days of the grant date
3. Use certified mail with return receipt — keep the receipt as proof of timely mailing
4. Attach a copy to your personal tax return for the year of the grant
5. Provide a copy to the company for its records
6. Keep a copy in your own permanent files

The company should also track every restricted stock grant and proactively remind recipients of the 30-day deadline. Build this into your equity grant process as a standard step.

### War Stories

From Feld and Mendelson directly: "We have had multiple firsthand experiences with a missed 83(b) filing, and it's a bummer when you are in the middle of an acquisition and you realize the 83(b) election is unsigned under a pile of papers on someone's desk."

In an acquisition, the buyer requires the company to represent that all employees and service providers who received restricted stock filed timely 83(b) elections. If they did not, the missing election creates a current or future tax liability for that individual — and that liability either comes off the acquirer's retention pool for that person or must be disclosed to all parties. It disrupts closings and creates friction at the worst possible moment.

Create a system. Assign a specific person to track every grant. Set a calendar reminder for day 25 post-grant. Follow up until the election is filed and confirmed. This is not complex, but it requires discipline.

---

## 5. Accredited Investor Verification

### The SEC Definition

An accredited investor is:
- An individual with net worth exceeding $1 million, excluding the value of a primary residence, OR
- An individual with income exceeding $200,000 in each of the prior two years (single) or $300,000 combined with a spouse, with a reasonable expectation of the same in the current year
- An entity with total assets exceeding $5 million, OR an entity in which all equity owners are individually accredited

### Why It Matters

Selling securities to non-accredited investors without compliance with specific SEC regulations (Regulation CF, Regulation A+, or registration) is a federal securities law violation.

A non-accredited investor who purchased your stock has a statutory RIGHT OF RESCISSION — they can demand that the company buy back their shares at the original purchase price, at any time, for as long as the statute of limitations allows. This is a permanent liability on the company's balance sheet that does not go away unless the investor waives it (rare) or the statute of limitations runs (varies by state, often several years).

In an acquisition or IPO, all outstanding rescission rights are surfaced and become an adjustment to the purchase price or a condition of closing.

### Practical Rules

- Verify accreditation status BEFORE accepting any investment, no matter how small or informal
- Keep documentation of your verification method
- Do not accept investment from people who cannot qualify as accredited investors under the SEC definition
- "But they're a friend/family member" is not an exception
- "But it's only a small amount" is not an exception

The right of rescission does not have a minimum investment threshold. A $10,000 investment from a non-accredited investor creates exactly the same legal problem as a $500,000 investment.

### Post-JOBS Act Complexity

The JOBS Act created limited pathways for non-accredited investors to participate in startup financings (Regulation CF crowdfunding, Regulation A+). Most VC-backed companies do not use these pathways. If you are considering crowdfunding as a financing mechanism, engage specialized securities counsel before proceeding — these regulations have their own compliance requirements and are separate from standard VC financing practice.

---

## Pre-Fundraise Full Legal Checklist

Run through this before beginning any institutional fundraise:

**IP**
- [ ] All co-founders signed IP assignment for pre-incorporation work
- [ ] All employees signed PIIA at hire
- [ ] All contractor agreements contain work-for-hire and IP assignment provisions
- [ ] Open source audit completed for core product
- [ ] No outstanding IP disputes or third-party claims

**Structure**
- [ ] Delaware C-Corp with sufficient authorized shares of common and preferred stock
- [ ] Articles of incorporation and bylaws properly adopted with board approval

**Valuations**
- [ ] Current 409A valuation (within 12 months and post any material events)
- [ ] All existing options granted at or above the then-current 409A FMV

**83(b)**
- [ ] All restricted stock recipients filed timely 83(b) elections
- [ ] Company has copies of all elections on file

**Investors**
- [ ] All existing investors verified as accredited investors
- [ ] Documentation of accreditation on file

**Employment**
- [ ] All employees are at-will (or have written agreements specifying terms)
- [ ] All employees are correctly classified (employee vs. contractor — misclassification creates tax and labor law liability)
- [ ] No key employees have non-compete or IP obligations to prior employers that could affect the company

**Governance**
- [ ] Cap table is accurate and complete
- [ ] Board is properly constituted
- [ ] Minutes exist for all board and shareholder actions
- [ ] All option grants are properly authorized by board resolution

---

## When Legal Issues Surface in Due Diligence

**In fundraising**: A VC's counsel will examine all of these items. If they find an IP gap or a missing 83(b) election, the deal pauses. In the best case, you fix the issue and continue. In the worst case, it poisons the diligence process and the VC loses confidence.

**In acquisition**: The buyer's legal team will be more thorough than the VC's. Any representation breach after closing can become an escrow claim. 409A non-compliance is typically carved out as a fundamental representation — meaning it is NOT capped by the escrow amount and creates unlimited personal exposure. Missing 83(b) elections surface as employee-level tax liabilities that complicate retention pool negotiations.

**The arithmetic is simple**: fixing these issues proactively costs legal fees measured in hundreds to low thousands of dollars. Fixing them reactively during a deal process costs delays, goodwill, and often money — potentially much more. Fixing them after closing (if that is even possible) costs more still. Prevention is the only rational choice.
