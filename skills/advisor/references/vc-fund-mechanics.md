# VC Fund Mechanics

## Context

Use when user wants to evaluate a VC fund, understand fund mechanics, detect zombie VCs, assess CVC risks, or understand how fund economics affect VC behavior. Primary reference for VC Diligence Mode.

---

## VC Fund Structure: Three Entities

Every venture firm is actually three separate legal structures. Confusing them leads to confusion about who controls what and who gets paid what.

### 1. Management Company (ManCo)

The operating entity. Employs all people — partners, associates, analysts, operations staff. Typically an LLC. Pays salaries, office rent, travel, legal fees, and all day-to-day expenses. The management company persists across multiple funds and across the life of the firm. When you see "Foundry Group" or "Union Square Ventures" on a business card, that name refers to the management company, not to any specific fund.

### 2. General Partner (GP)

The legal entity that controls the fund. Makes investment decisions. Has unlimited liability for fund obligations. A new GP entity is often created for each fund. This is the entity that signs investment documents, receives carried interest, and is responsible for managing the LP's capital.

### 3. Limited Partnership (LP Fund)

The actual pool of money. LPs contribute capital. GP manages it. LPs have limited liability. A new fund is a new LP entity, separate from prior funds — Foundry Group Fund I and Foundry Group Fund II are different legal entities with different pools of money and different LP investor bases.

**Key insight for founders**: The fund (LP) is the investor, not the management company. When a VC says "our fund," they mean the LP. The people you talk to work for the ManCo and act through the GP. This matters because: a GP's authority to invest is tied to the fund's commitment period, and the fund's life cycle determines whether a VC can actually write you a check.

**Common LP types**: University endowments, pension funds, family offices, high-net-worth individuals, funds of funds, sovereign wealth funds, insurance companies, corporations.

---

## Fund Economics

### Management Fee

- Standard: 2% of committed capital per year during the commitment period
- Drops to 1.5–2% of invested capital (not committed) after the commitment period ends
- Duration: typically 10-year fund life, often with two one-year extension options
- Purpose: covers salaries, office, travel, legal, administration — ALL firm operations

**Example**: A $200M fund generates $4M/year in management fees. That is enough for 5–6 partners plus support staff plus overhead. Over a 10-year fund life, total management fees typically equal ~15% of committed capital, meaning a $200M fund actually deploys closer to $170M.

**Management fee on fund size tells you about VC incentives**:
- Small fund ($50M): $1M/year management fee — partners need carry to make real money, so they are highly motivated to work hard for portfolio companies
- Large fund ($1B): $20M/year management fee — partners earn well on fees alone, carry is a bonus rather than financial necessity

**Implication for founders**: Partners at large funds may be less motivated to do the hard work of supporting portfolio companies because management fee alone provides a comfortable income. Partners at small funds are more dependent on carry — they genuinely need their investments to succeed, which creates alignment with your interests.

**Critical point**: Management fees are entirely independent of investment returns. A VC firm that loses all its investors' money still collected all its management fees. This is a feature from the VC's perspective and worth understanding from yours.

### Carried Interest (Carry)

- Standard carry: 20% of profits after returning all committed capital to LPs
- Top-tier firms: 25–30% carry
- Carry is split among partners — almost never equally; senior partners typically receive meaningfully larger shares
- Carry only pays out AFTER all committed capital is returned to LPs (with hurdle rate in some structures)

**Example math on a $200M fund**:
- Fund returns $600M total
- First $200M returned to LPs (return of capital)
- Remaining $400M = profits
- Carry = 20% × $400M = $80M to GP
- LPs receive: 80% × $400M = $320M profit
- Total to LPs: $200M + $320M = $520M (2.6x net)
- Total to VC: $80M carry (plus ~$30M in management fees already paid)

**Carry timing**: Carry is often paid as portfolio companies return capital, not all at the end. This creates clawback risk — if a firm pays carry on early wins but the total fund ultimately underperforms, LPs can require VCs to return previously paid carry. Clawbacks create real tension and are painful for everyone.

### GP Commitment

VCs invest their own money alongside LPs, typically 1–5% of the fund. On a $200M fund, the partners collectively put in $2–10M. This aligns their economic interests with LPs. It also means partners have real personal financial exposure when investments fail.

### Commitment Period

- Typically the first 3–5 years of fund life
- VCs can make NEW investments ONLY during this period
- After the commitment period ends: the fund can only do follow-on investments in existing portfolio companies (using reserves)
- A VC CANNOT invest in your company if they are past their commitment period, regardless of interest, enthusiasm, or meetings taken

**Critical for founders**: If a VC's fund is past its commitment period, it cannot lead your round as a new investment. It can only participate as a follow-on if you're already a portfolio company. Ask directly: "When did you raise your current fund, and when does your commitment period end?"

---

## Zombie VC Detection Algorithm

A zombie VC is a fund that is effectively dead but still operating — still collecting management fees, still taking meetings, still appearing to be an active investor. They cannot make new investments because their commitment period has expired or their reserves are fully committed to existing portfolio companies.

### Detection steps:

1. **When was the fund raised?** If more than 5 years ago, the fund is likely past its commitment period. Yellow flag. Ask the follow-up: "When does your commitment period end?"

2. **Have they raised a new fund?** If their last fund closed in 2018 and no successor has been announced, they are likely winding down or already zombified. Active firms raise new funds every 3–5 years.

3. **When was their last NEW investment?** Not a follow-on to an existing portfolio company — a brand new company they had not previously backed. If more than 12–18 months ago, serious concern.

4. **Ask directly**: "How many new investments do you plan to make from your current fund, and how much dry powder remains for new investments versus reserves?" Capable, active investors know exactly what capacity remains. Evasive or vague answers are a red flag.

5. **Check for partner departures**: If key partners have left the firm and no replacements have been hired, the fund may be running on autopilot. Partner departures in the last 12–24 months with no announcement of a new fund signal a wind-down.

### Why zombie VCs are dangerous:

- They take meetings to maintain deal flow visibility and market presence
- They conduct full diligence processes — including references, financial review, product deep-dives — that consume weeks of your time
- They string companies along for months before declining (or without ever explicitly declining)
- They cannot actually write checks for new investments
- They will rarely tell you they are a zombie — you must detect it yourself

### Zombie behavior patterns:

- Vague about fund timing and new investment capacity
- "We're always looking at interesting opportunities" without specifics
- Never moves toward a term sheet but never explicitly declines
- Asks increasingly detailed questions about your business indefinitely
- May offer an "advisory relationship" or introductions — non-financial involvement
- Warm, responsive, and interested but perpetually unable to commit to next steps

### Direct questions to ask:

- "When did you close your most recent fund and what vintage year is it?"
- "How many new investments from the current fund have you made in the last 12 months?"
- "How much dry powder remains for new investments, not including follow-on reserves?"
- "Are you currently raising a new fund, and if so, what stage is that process at?"

---

## Corporate Venture Capital (CVC) Flags

CVCs invest from a corporation's balance sheet or a dedicated corporate fund. The different structure creates fundamentally different incentives from traditional VC.

### CVC Red Flags:

**1. Balance sheet investing**: No separate fund structure, no commitment period, no LP obligation. The investment can be cancelled or redirected at any time if corporate priorities, earnings pressure, or leadership changes. Budget is subject to quarterly review.

**2. Strategic motivations**: CVC may want technology access, an acquisition option, competitive intelligence, or distribution control more than financial return. This creates permanent misalignment — when your strategic interests diverge from the parent's, the CVC's loyalties are tested.

**3. Right of first refusal (ROFR) on acquisition**: Never give a CVC a ROFR on acquisition. This right suppresses acquisition interest from all other buyers — other potential acquirers will not engage seriously in a process where a ROFR holder can match any offer. A ROFR creates permanent leverage for the parent corporation over your exit options and is extremely difficult to remove once granted.

**4. Board seat information risk**: A CVC on your board sees your strategy, product roadmap, financial statements, and personnel decisions. If the parent corporation competes with you even indirectly — or might compete with you in the future — this is a structural information leak. What you share in board meetings can influence the parent's strategic decisions.

**5. Approval chains and timeline risk**: CVC investment decisions often require corporate board approval, legal review by corporate counsel, and sign-off from multiple layers of management. Their closing timeline is corporate, not startup. What takes a traditional VC two weeks to close can take a CVC two months.

**6. Team instability**: CVC partners are corporate employees, not independent fund partners. They are compensated with salary and parent company options, not carried interest in an independent fund. High performers get recruited away to traditional VC. Lower performers cycle out via HR. Your board member may change two or three times over the life of your company.

### CVC Green Flags:

- Dedicated fund structure with separate GP entity (acts more like a traditional VC)
- Investment team has independent VC experience, not just corporate development background
- Track record of portfolio company exits to third parties — not primarily to the parent corporation
- Clear mandate that financial return is the primary investment objective, not strategic access
- No requests for strategic rights (ROFR, information rights to parent, preferential partnership terms)
- Consistent team tenure — same partners have been together for 5+ years

### CVC decision framework:

1. Is the CVC investing from a dedicated fund structure or directly from the corporate balance sheet? (Dedicated fund is substantially better)
2. Are there strategic strings attached — ROFR, exclusive technology access, data sharing requirements, preferential partnership terms? (Any = red flag, negotiate hard before accepting)
3. What is their track record? How many portfolio companies were acquired by the parent corporation versus exiting to third parties? (If more than 50% were acquired by the parent, they are building a pipeline for corporate M&A, not a financial portfolio)
4. Will they demand a board seat, and what is the information risk to your business if a representative of the parent corporation sits on your board?
5. Can they actually deliver the strategic value they are offering? (Distribution, customers, technical credibility — the theoretical value CVC provides) Ask for specific examples with named portfolio companies.

---

## Reserve Strategy and Follow-On

Every VC firm sets aside a portion of the fund for follow-on investments in existing portfolio companies. Understanding a VC's reserve position tells you whether they can support you in future rounds.

- Early-stage investors typically reserve 3–5x their initial investment per company
- A fund that is underreserved cannot do its pro-rata in your next round

**Why this matters for founders**: If your VC cannot participate in your Series B at their pro-rata, other Series B investors will notice. An existing investor not following on is a major negative signal — it suggests the insiders know something unflattering about the company or its prospects. Even if the VC's reason is purely mechanical (depleted reserves), the signal damage to your fundraising is real.

### Signs of reserve problems:

- VC resists new financing rounds without clear strategic reason
- VC pushes to limit the size of a financing round (protecting reserves by keeping the round smaller)
- VC repeatedly suggests the company should consider selling
- VC becomes less responsive when follow-on discussions begin
- Other portfolio companies in the same fund are consuming reserves through large follow-ons or bridge rounds

### Questions to ask during VC diligence:

- "What is your typical follow-on investment capacity per company?"
- "What percentage of your current fund has been deployed versus reserved?"
- "Can you share examples of how you've supported portfolio companies in Series B and C rounds?"
- "In your current fund, how much has been reserved versus deployed?"

---

## VC Reference Check Protocol

Before accepting any term sheet, reference-check the VC thoroughly. The VC conducts extensive diligence on you. You have every right — and strong reason — to conduct equally thorough diligence on them.

**Who to call**: 3–5 founders the VC has backed. Get names independently — do not rely solely on the reference list the VC provides. Find companies from their portfolio that do not appear on the highlight reel. Specifically seek out at least one company that struggled.

**Why struggles matter**: VCs are easy partners when things go well. The real test of a VC relationship is adversity — a missed quarter, a pivot, a down round, a co-founder departure. How the VC behaves in those moments is the most revealing data about what your relationship will look like when you need them most.

**Questions to ask**:

1. "How did [VC] behave when things got hard? Did they show up or go quiet?"
2. "Did they ever push to replace you as CEO or threaten to do so?"
3. "How helpful were they beyond writing checks — specific examples?"
4. "Would you take their money again, knowing what you know now?"
5. "Is there anything you wish you had known before taking their investment?"
6. "What was the negotiation process like? Did they negotiate in good faith?"
7. "How did they behave as a board member — constructive, passive, or adversarial?"

**Check reputation more broadly**: Review their published writing, podcast appearances, public statements. Ask other VCs who have co-invested with them: "What has your experience been working with this firm?" Co-investors see VC behavior in board meetings and down rounds that portfolio founders sometimes cannot access.

The information from these calls is asymmetric and high-value. Bad VC relationships are very difficult to exit and can persist for a decade. Reference checking is the single highest-leverage hour you will spend before signing a term sheet.
