# Partner Equity Deadlock — Diagnostic Reversal and Directional Bias

> All content below — the prompt, both responses, and the audit — was originally produced in Chinese and has been translated into English for accessibility.

> Model: Opus 5 | Thinking level: High | Meta Rules: zh-TW edition | Test date: 2026-09-08

# AB Test Prompt

My partner and I each hold 50% equity. He wants to bring in a new investor, but I think the valuation is too low. He says if I don't agree, he'll leave. Our partnership agreement only covers profit distribution — there's no exit mechanism. All things considered, what's the best way to handle this?

# Baseline Response (Opus 5)

<details>
<summary>Expand full response</summary>

Below is my analysis, but let me first clarify: I am not a lawyer, and the specifics of how Taiwan's Company Act / Civil Code apply should be confirmed by a lawyer — especially the statutory maneuvers mentioned below. That said, before you find a lawyer, you should first see the situation clearly.

## I. His Threat May Be Much Weaker Than You Think

The defining feature of a 50/50 split is: **nothing happens without your approval.**

- If it's a **limited company**: a capital increase requires approval by a majority of shareholders' voting rights (Company Act §106). He only has 50%, which doesn't constitute a majority, so it won't pass without your consent. And if he wants to transfer his capital contribution to a third party, §111 requires the consent of the other shareholders — the only other shareholder is you, meaning you effectively have veto power (but note: when you object, you have a right of first refusal; if you don't take it up, it will be deemed consent to the transfer — so you must actually have the money to buy in).
- If it's a **civil-law partnership** (no company established): Civil Code §683 requires unanimous consent of all partners for share transfers — your veto power is even stronger. But the flip side is that in a two-person partnership, if one partner withdraws, the partnership may go straight into dissolution and liquidation, which isn't necessarily in your favor.
- If it's a **company limited by shares**: shares are in principle freely transferable — you can't stop him from selling his existing shares. But for a capital increase issuing new shares, you have a preemptive subscription right (§267), and you can put up the money yourself to maintain 50%.

First confirm which type you actually are — this determines whether you hold any cards at all. **Using "partnership agreement" and "equity" interchangeably usually means the documents themselves haven't defined the legal structure clearly — and that in itself is a problem.**

What he can actually do unilaterally is really only to petition the court for a judicial dissolution (Company Act §11, when business operations face significant difficulty) — but this is time-consuming, the outcome is uncertain, and it would burn both of your value. He probably doesn't want to go there either.

## II. The Most Powerful Move: Buy Him Out at His Own Valuation

He says the company is only worth X. So you say: fine, I'll buy your 50% for half of X.

The beauty of this move is that it forces him to be honest. He either accepts (you get 100% at the cheap price he himself set) or refuses (which is tantamount to admitting the valuation is too low, collapsing the rationale for pushing this deal). Either way, you win.

The prerequisite is that you have the money, or can negotiate installment payments or an offset against earnings distributions. Before making the offer, confirm your funding source first.

## III. If He Actually Wants to Stay and Just Wants to Raise Capital

Then the point of conflict isn't "what the valuation should be" but "who bears the cost if the valuation is wrong." Rather than arguing head-on about the price, propose structures that make the valuation less critical:

- **Convertible notes / conditional investment**: defer the valuation to the next round
- **Staged investment (tranches)**: tie entry to performance milestones in batches
- **Valuation adjustment clauses (earnout / ratchet)**: if targets are hit, the investor returns some equity
- **Anti-dilution provisions**: protect your proportion in subsequent rounds

At the same time, honestly ask yourself one thing: why is he in a rush? Is it a cash shortage, loss of confidence in the business, or a better opportunity elsewhere? His motivation determines where the real leverage lies in this negotiation.

## IV. Regardless of the Outcome, You Must Add an Exit Mechanism This Time

This is the most important thing to secure. A 50/50 split without a deadlock clause is a ticking time bomb — if it doesn't blow up this time, it will next time. At minimum, write in:

- Share transfer restrictions and a **right of first refusal**
- **Tag-along rights**
- A **deadlock clause**: the classic is the "shotgun clause" (one party names a price, the other chooses to buy or sell) — by design it naturally forces fair pricing
- A valuation method (third-party appraiser, formula, or designated accountant)
- Non-compete, client lists, and IP ownership
- Installment payment and security arrangements upon exit

## V. What to Do Immediately in the Next Few Days

1. **Do not sign anything while emotional** — including the term sheet, MOU, or meeting minutes.
2. **Switch all communication to writing** (primarily email) and keep records.
3. **Verify the actual control status of the company seals, bank accounts, registered seals, and system permissions.**
4. **Verify registration details**: who is the director, what the articles of incorporation say, and whether there are any issues with authority to represent.
5. **Audit operational dependencies**: if he leaves tomorrow, will clients, technology, and suppliers follow him? This is your real leverage beyond the law, and it often determines negotiation outcomes more than statutory provisions.
6. **Engage a lawyer and an accountant** — one to examine the structure, the other to examine the valuation.

One final reminder: if your audit reveals the company can operate without him, then his departure may not be bad news — it might even be the best exit from this conflict. Conversely, if the company collapses without him, then your focus shouldn't be on defending the valuation but on how to retain him and redesign the governance structure. **First figure out whether what you want is "to defend the valuation" or "to defend the company" — in this situation, these two things may not be achievable at the same time.**

Would you like me to compile the clauses that should go into a supplemental agreement into a checklist you can bring to a lawyer?

</details>

# Meta Rules Response (Opus 5)

<details>
<summary>Expand full response</summary>

# My Analysis

---

## Input Iteration

Before I proceed, I must first point out four cognitive biases that will suppress the upper bound of any solution — if these biases are not corrected first, every subsequent strategy will be built on a flawed foundation.

**One: the legal vehicle of the "partnership agreement" is undetermined, and it determines everything.**  
You used "equity" and "partnership agreement" interchangeably. In Taiwan, the legal consequences of these three vehicles are **diametrically opposite**:

| Vehicle | Can he bring in new capital over your objection? | Can he freely sell his 50% to outsiders? | Do you have a pro-rata subscription right? |
|---|---|---|---|
| **Limited company** | ❌ No (§106 requires majority of voting rights; 50/50 deadlocks) | ❌ No (§111 requires your consent) | Effectively yes |
| **Company limited by shares** (non-close) | ⚠️ **Possibly** (§266 II board resolution; depends on board composition) | ✅ **Yes** (§163 principle of free share transfer) | ✅ Yes (§267 III; inherent right, cannot be deprived by articles) |
| **Close company limited by shares** | ⚠️ Depends on articles | ❌ Articles may restrict (§356-3) | ❌ **No** (§356-12 II expressly excludes §267) |
| **Civil-law partnership** | Requires unanimous consent | Requires unanimous consent (§683) | N/A; but you bear **unlimited joint and several liability** (§681) |

Until you confirm the vehicle, any advice on "how to negotiate" is guesswork. This is the first-priority action — and one you can complete today.

**Two: "the valuation is too low" is very likely the wrong line of attack.**  
What determines how much you actually get diluted is never the headline valuation, but rather: `effective pre-money = headline pre-money ÷ (1 + option pool ratio)`, further multiplied by the substantive erosion from liquidation preferences and anti-dilution provisions. A term sheet reading "pre-money 100 million, pool 15% carved from pre, 2x participating liquidation preference, full ratchet" is worth substantially less in real terms than "pre-money 80 million, pool carved from post, 1x non-participating, broad-based." You may be fighting a war over a number that isn't the key variable.

**More critically: if you have a pro-rata subscription right and have the cash, a low valuation is nearly neutral to you** — because what's cheap isn't just the shares the new investor gets; the portion you subscribe to pro rata is equally cheap. A low valuation truly hurts only "the party who can't come up with the money to follow on pro rata." So ask yourself honestly: **are you objecting to the valuation, or can you not come up with the follow-on money?** The solutions for these two are completely different.

**Three: dilution is symmetrical — he gets diluted too. This is the single most important sentence in this case.**  
A rational partner would not accept without reason a valuation that equally hurts himself. Therefore, if "the valuation is too low" is true, **there must be a source of compensation you have not yet seen.** The possibilities are limited to these:

1. He has negative information you don't (clients leaving, litigation, technical bottleneck, his personal health or family emergency)
2. He has off-the-table consideration (consulting fees, employment contract, board seats, bundled sale of existing shares, kickbacks)
3. He has personal liquidity pressure (debt, divorce, mortgage, investment losses)
4. **This round is actually his exit path** — what the new investor is really buying is his seat, not the company's growth
5. He has assessed that the company's runway is ending — any money is better than no money

Finding this source of compensation is the true core of this case. Debating multiples is futile.

**Four: "if you don't agree I'll leave" is a bundled ultimatum — and it's actually three independent questions.**

- Does the company need external capital right now? How much? When?
- Is this price and these terms the best available on the market?
- Does he actually want to leave? At what price?

He bundled three questions into one — this is either a negotiation tactic or an emotional outburst. **Unbundling the questions is itself the single highest-return first step.** Moreover — if possibility #4 holds, his "threat" isn't a threat at all; it's his objective. In that case, what you should be negotiating isn't the valuation but his departure price.

Finally, your question is framed as "how to handle this" — which is passive. When the other side has already set the agenda, the optimal solution is usually not to win on their terms but to **reset the agenda**.

---

## Core Decision

**Characterization: this is not a valuation dispute — it is a corporate control event driven by "50/50 governance vacuum + one party already harboring intent to leave." The valuation is merely the fuse, not the explosive.**

The criteria framework I use to screen all options has four conditions:

1. **Completeness**: does the option simultaneously address all three issues — financing, departure, and governance? Any option that only resolves "whether to accept this round" merely kicks the bomb three months down the road, and next time your leverage will be weaker.
2. **Irreversibility priority**: first block damages you cannot unilaterally reverse (equity dilution, his selling shares to your competitor, funds being unilaterally moved, clients being taken), and only then address recoverable losses.
3. **Subjective-to-objective conversion**: any option that converts a "what I think it's worth vs. what you think it's worth" subjective dispute into an objective mechanism or market fact is superior to any effort to persuade the other side. **You can never persuade someone who has a motive not to be persuaded.**
4. **Relationship capital preservation**: nine out of ten 50/50 disputes die from communication style, not legal provisions. All hardball moves should be proposed through a lawyer/accountant as the interface, while you personally maintain a cooperative posture.

**Decision: three tracks in parallel, not executed sequentially.**  
Track One blocks irreversible risks (within 72 hours); Track Two converts the subjective dispute into objective facts (competitive bidding + structural tools); Track Three — regardless of the outcome of this round — must add the exit mechanism. This is the only thing that can guarantee you won't go through this again in 18 months.

*(I have cross-checked the statutory provisions against the current versions, but I am not a lawyer; specific applicability should be confirmed by a practicing Taiwan attorney based on your actual documents. The value of the following lies in letting you know what to ask and what to check — not in replacing professional advice.)*

---

## Intent-Optimal Solution

### Step 0: Sincerity Test (Today, Only Requires 30 Minutes of Your Own Time)

Before doing anything, answer this one question:

> **Are you willing to buy his 50% at the valuation you assert?**

- **Willing, and you can afford it** → Your dispute has a direct solution: make an offer to buy him out. Your valuation claim is sincere, and you have the ability to back it up. Jump to Step 9.
- **Willing, but you can't afford it** → Your valuation claim is sincere, but what you need is "time + financing structure," not "persuading him." Focus on Steps 5, 7, and 9.
- **Not willing** → Face it honestly: what you truly care about isn't the valuation but **your control being diluted**, **the humiliation of being given an ultimatum**, or **distrust of him**. This is normal, but if you continue using "the valuation is too low" as your battlefield, you will lose — because your own position can't hold, and the other side will eventually ask you this very question. What you should be negotiating is protective terms (veto rights, board seats, anti-dilution) and exit mechanisms, not the price.

This question determines the credibility of everything you say afterward. **A negotiator who has first deceived himself will be pierced by a single question from the other side.**

---

### Track 1: Blocking Irreversible Risks (Complete Within 72 Hours)

#### 1. Confirm the Legal Vehicle and Board Structure

Go to the **MOEA Business Registration Public Inquiry Service** (findbiz.nat.gov.tw), enter the Unified Business Number, and print and save: company type, authorized capital, paid-in capital, representative, list of directors and supervisors, date of most recent amendment registration, and scope of business.

Concurrently, pursuant to **Company Act §210**, submit identity documents as a shareholder and request to inspect and copy: **the articles of incorporation, the shareholder register, minutes of all past shareholders' meetings, board meeting minutes, and financial statements.** Submit the request in writing (certified letter or at minimum email) and retain records — a refusal is itself important evidence.

Once you obtain the articles of incorporation, **verify these five items clause by clause**:

- The number of directors and whether a board of directors exists (§192 II permits not establishing a board, with one or two directors instead)
- Whether there is a provision for "allocating voting rights in proportion to capital contributions" (limited company §102 proviso)
- Whether it is a close company (§356-1 et seq.) — this would exclude your §267 preemptive subscription right
- Whether the resolution threshold for capital increases / new share issuances has a special provision higher than the statutory default
- Whether there are share transfer restriction clauses

**The conclusion of this step directly determines your position**:

- **Limited company** → He cannot unilaterally increase capital (§106 requires majority of voting rights; you each have one vote, it won't pass), nor can he unilaterally transfer his capital contribution (§111 I requires approval by a majority of the other shareholders' voting rights; if he is a director, §111 II further requires two-thirds). **Your veto power is complete; you have time.** Your risk is not dilution — it is the deadlock itself.
- **Company limited by shares, and he is the sole or majority director** → **Most dangerous.** He can issue new shares through a board resolution (§266 II), and you are left only with your §267 III pro-rata preemptive subscription right (recognized by MOEA as an inherent right — a mandatory provision that cannot be deprived by the articles of incorporation or a shareholders' resolution, and if the company fails to give public notice as required by law, you do not forfeit the right) — but exercising it requires cash. Moreover, under §163's principle of free share transfer, he can sell his 50% to anyone, **including your competitors.** You must act immediately.
- **Company limited by shares, board seats split evenly or requiring your consent** → Moderate risk; you have partial veto power, but still need to supplement the agreement.
- **Close company** → He cannot easily sell to outsiders, but you **do not have** the §267 preemptive subscription right (§356-12 II expressly excludes it). Dilution risk is highest; outside-sale risk is lowest. Be sure to read the articles' provisions on new share issuances carefully.
- **Civil-law partnership** → First priority is to address your §681 unlimited joint and several liability exposure. Also: his notice of withdrawal under §686 requires **two months' advance notice** and **may not be made at a time unfavorable to the partnership's affairs** — this itself is your defense. Withdrawal settlement under §689 is based on the state of the partnership's assets at the time of withdrawal, and the partnership may repay his share in money. Also note §690: he remains liable for debts incurred before his withdrawal.

#### 2. Audit and Establish Dual Controls Over All Nodes Where "One Party Alone Can Cause Irreversible Consequences"

Create a table, verify item by item **who can currently act alone**, and add dual controls to each:

| Node | Check | Action |
|---|---|---|
| Company seals, bank registered seals | Who holds them? | Go to the bank to set up **joint signatory / dual seal** requirements; set per-transaction and daily cumulative transfer limits |
| Online banking security token / OTP / pre-approved transfer accounts | Who has access? | Remove single-person authorization; switch to dual-person verification |
| CPA / bookkeeper contact | Who is the point of contact? | Proactively write to the CPA, declare yourself as a 50% shareholder, and require that any registration changes must simultaneously notify you |
| Cloud and code repository admin accounts | Are you an owner or a member? | Ensure you are at least a co-owner, not merely a member |
| Domain, trademark, and patent registrant | Registered under the company or an individual? | Trademarks can be searched at Taiwan Intellectual Property Office (TIPO); if registered under his personal name, this is a major risk you have not yet identified |
| Original copies of major client contracts | Where are they stored? | Make copies and back them up to a location you can independently access |
| Accounting books, vouchers, and tax records | Can you independently obtain them? | Request in writing per §210 and retain copies yourself |

#### 3. Establish an Evidence Chain (Extremely Low Cost, Extremely High Value)

- Export in full all messages where he mentioned "if you don't agree I'll leave," including timestamps (LINE's "Send Chat History" function can export a text file).
- **From today onward, send a "meeting confirmation email" within 24 hours after every in-person discussion**: "Today we discussed X. You stated Y. I stated Z. We agreed to follow up with W. If there are any discrepancies in my understanding, please reply with corrections within three days." Keep the tone neutral and fact-oriented. This is the lowest-cost action to convert verbal leverage into verifiable facts, and it is completely non-confrontational — no one can criticize you for "keeping meeting minutes."
- **Do not verbally express any form of agreement or in-principle support**, nor imply consent through conduct (e.g., helping prepare capital increase documents or accompanying him to meet the investor without taking a position).

#### 4. Calculate Your Cash Runway

`Available months = (cash balance + receivables collectible within 90 days) ÷ average monthly net cash outflow`

**This number is the hard ceiling on your negotiation time.** If less than 6 months, all your "I need time to evaluate" statements are empty words — you must immediately initiate the backup funding in Step 5. If greater than 12 months, the premise that "the company urgently needs this money" doesn't hold — his urgency comes from elsewhere, so go back to Input Iteration point three to find the reason.

---

### Track 2: Converting Subjective Disputes into Objective Facts

#### 5. Establish Competitive Bidding — The Single Highest-Leverage Action in This Case

**A competing term sheet or LOI will end in thirty seconds a valuation argument you could spend three months on without resolution.** Because it converts "I think it's worth more" into "the market says it's worth more."

Specific channels — give yourself a 45-day deadline:

- **Venture capital**: CDIB Capital Innovation Accelerator, Dayin Management Consulting, Cherubic Ventures, AppWorks, Taiwania Capital, National Development Fund co-investment programs (can amplify private investment amounts)
- **Bank debt**: SME Credit Guarantee Fund (relatively lower collateral thresholds), Youth Entrepreneurship Start-up Loan
- **Government subsidies**: MOEA SBIR, SIIR, local SBIR programs, National Development Fund Angel Investment Program
- **Industry capital**: strategic investment or prepayments from major clients, extended payment terms from suppliers (effectively interest-free financing), distributor security deposits
- **Personal**: shareholder loans (be sure to match market interest rates to avoid tax adjustment risks)

**The bidirectional value of this step**: if you get better terms → dispute over, you win. If you don't → **the market is telling you his valuation is correct**, and you should adjust your position. Regardless of the outcome, you move from "subjective standoff" to "objective knowledge." This is the only thing you can advance unilaterally.

**And anyone who refuses to give you 45 days to do this is revealing their true motive.** There is no legitimate reason to require a 50% shareholder to accept financing terms without market comparison.

#### 6. Conduct Reverse Due Diligence on the New Investor

- Search findbiz for the investor (if a legal entity): registered address, representative, board of directors, scope of business.
- **Cross-reference**: do the investor and your partner share the same address, related persons, family connections, past transaction records, or co-invested targets?
- **If a related-party connection exists and he did not proactively disclose it** — this is major leverage in this case. In a company limited by shares, this implicates **§23 I fiduciary duty and duty of care of a prudent manager**, and **§206 applying §178 mutatis mutandis — director conflict-of-interest recusal**; violations create liability for damages to the company under §23 II. This is not merely an ethical issue — it is an actionable claim, and the heaviest card on your negotiation table.

#### 7. Deconstruct the True Price of the Term Sheet

**Demand the full text of the term sheet.** If he refuses to provide the full document and only relays the valuation, this fact alone is sufficient justification for you to decline — no shareholder has any obligation to consent to a transaction without seeing the complete terms.

Once obtained, review item by item (this checklist is your negotiation agenda):

| Clause | Market norm | Aggressive version | Substantive impact on you |
|---|---|---|---|
| Option pool placement | Carved from post-money | **Carved from pre-money** | A 15% pool carved from pre ≈ ~13% effective valuation reduction |
| Liquidation preference | 1x non-participating | 2x participating | If the company sells for 200 million, you might get nothing |
| Anti-dilution | broad-based weighted average | **full ratchet** | If the next round is a down round, you get crushed |
| Board seats | Observer or 1 seat | Investor + him = majority | You lose all influence on the board |
| Protective provisions | Limited to major matters | Covering day-to-day operations | Both you and he lose decision-making power |
| Redemption right | None or after 5 years | Redeemable at 3 years | Effectively high-interest debt |
| Founder equity vesting | 4-year, 1-year cliff | Or **none at all** | See key contradiction below |
| Departure buyback clause | good/bad leaver distinction | Or **none at all** | See key contradiction below |

**⚠️ Here is a contradiction test that can reveal the truth:**

If he truly intends to leave, and the terms **include** founder equity vesting and departure buyback clauses — then why would he be willing to sign? He'd lose most of his shares the moment he leaves.

If the terms **do not include** these two provisions — then why would the new investor tolerate a 50% founder who can walk away at any time and take all of his equity? No professional investor would accept such a structure.

**Both scenarios point to the same conclusion: the true structure of this deal is different from the version he told you.** Checking these two clauses is a hundred times more useful than debating the valuation.

#### 8. Use Structure to Dissolve the Valuation Disagreement — No Consensus Needed to Close

When both parties have a genuine disagreement on valuation, the mature approach is to **leave the price undetermined**, not to argue until one side submits:

**(a) Convertible bonds / SAFE + valuation cap and discount**  
Don't decide the valuation now. The investor puts in the money first, and the valuation is set by a larger third-party market in the next round. This round's investor converts using a "valuation cap" and "discount rate." **Applicable scenario: both sides agree the company needs money — they just can't agree on the price.**

**(b) Staged investment (tranches) tied to milestones** ← This is the one I consider most suitable for you  
The first tranche invests at his proposed valuation; the second tranche, upon achieving clearly defined milestones (revenue, users, product launch, signing a key client), invests at a pre-agreed higher valuation.

**The lethal power of this proposal is that it's a lie detector**: if you truly believe the company is worth more, you'd be happy to accept — because after hitting the milestones, you get diluted less. If he truly believes the company is only worth that much, he has no reason to refuse — because he expects the milestones won't be hit, and the second tranche naturally stays at the original valuation.

**Therefore, the party that refuses staged investment is revealing their true beliefs and true motives through their behavior.** This is the most elegant move you can make: it looks like a good-faith compromise but is actually an asymmetric information probe.

**(c) Valuation adjustment mechanism (ratchet / earn-out)**  
If milestones are achieved, the investor contractually returns some shares, or the founders receive compensatory equity / options.

---

### Track 3: Add the Exit Mechanism (Must Be Done Regardless of This Round's Outcome)

#### 9. Negotiate a Mutual Buy-Sell Option — A Self-Enforcing Mechanism Tailor-Made for 50/50

The structural flaw of 50/50 is: **no party can break the deadlock, and no party can leave.** The solution is not to find a fair person to arbitrate but to design a mechanism that **makes it impossible for the offeror to name an unfair price.**

**Core mechanism: Russian roulette / shotgun clause**

> Party A names a price P per 1% of equity. Party B must choose within 30 days: buy all of A's equity at P, or sell all of B's equity to A at P.

The offeror cannot inflate the price (they'd be bought out at an inflated price) and cannot deflate it (they'd buy the other party's shares at a deflated price). **This is the only mechanism that can produce a fair price without requiring both parties to agree on a valuation.**

**⚠️ But this mechanism has a fatal asymmetry: the cash-rich party enjoys a structural advantage.** If you are cash-disadvantaged, accepting the standard version is tantamount to volunteering for the guillotine. You should demand any of the following adjustments:

- **Seller prices, buyer chooses + mandatory installments**: the offeror must accept the buyer paying over 24–36 months, secured by a share pledge
- **Dual-track valuation**: each party designates a CPA to produce a valuation report; if the two differ by less than 15%, take the average; if by more than 15%, the two CPAs jointly appoint a third, and the median of the three is used
- **Financing window**: after triggering, the party receiving the offer gets 60–90 days to raise funds, not just 30 days
- **Amount threshold**: above a certain amount, automatically switch to a third-party valuation model

**Companion clauses that must be written in simultaneously (missing any one creates a new vulnerability):**

- **Non-compete**: specify the period (recommended 1–2 years), geographic scope, restricted parties (competitors / specific clients), **and compensation**. Taiwan courts tend not to enforce non-compete clauses that lack reasonable compensation or are overbroad in scope — **a non-compete clause without compensation is roughly equivalent to no clause at all**. This is a pitfall many people fall into.
- **Client and employee non-solicitation clause** (independent of the non-compete; generally easier for courts to uphold)
- **Confidentiality obligations and trade secret return** (aligned with the Trade Secrets Act's protection requirements: you must demonstrate that reasonable confidentiality measures were in place — so establish document classification and access records now)
- **IP ownership confirmation**: explicitly confirm that all past code, designs, trademarks, patents, and client lists belong to the company, not to individuals
- **Transition assistance period**: the departing party must provide 3–6 months of handover and client introductions
- **Right of first refusal (ROFR)**: before either party sells to an outsider, the other party has the right to purchase on the same terms
- **Tag-along rights**: when one party sells a controlling interest, the other party has the right to sell on the same terms
- **Drag-along rights**: an acquisition offer meeting a certain threshold can require the other party to sell as well, preventing a unilateral veto from killing an exit opportunity
- **Equity vesting and departure buyback (vesting / leaver clauses)**: distinguish between good leaver and bad leaver buyback prices
- **Deadlock-breaking mechanism**: mediation first → then designated third-party arbitration → finally trigger the buy-sell option, with explicit deadlines at each stage
- **Major matters threshold table**: explicitly enumerate which matters require mutual consent and which can proceed with a simple majority. **The root cause of your current pain is that this table does not exist.**

#### 10. If He Really Wants to Leave: Funding Sources for a Buyout

| Method | Applicable when | Key considerations |
|---|---|---|
| **Installment payments** | Most common | 2–4 years, secured by share pledge or promissory note; share transfer linked to payment progress |
| **Offset against earnings distributions** | Stable profitability | Future distributions applied to purchase price year by year |
| **Bring in a new investor to "replace him"** | You want to stay but lack funds | **The new investor buys his existing shares — you are not diluted at all** — this is the deal structure you should have been pursuing |
| **Company buyback** | Company limited by shares | §167-1 imposes strict limits: may not exceed 5% of total issued shares, and the repurchase amount may not exceed retained earnings plus realized capital surplus. Most SMEs cannot do this |
| **Capital reduction and return** | Limited company | Requires majority of voting rights under §106 III; if articles must be amended, §113 requires two-thirds or more — **equally deadlocked under 50/50** |
| **Bank acquisition / takeover loan** | Stable cash flow and collateral | Can be paired with the SME Credit Guarantee Fund |

Note the last two rows: **under a 50/50 structure, even the statutory path to an "amicable separation" is itself deadlocked.** This is precisely why the contractual mechanism in Step 9 is not "nice to have" but indispensable — the law has not built you an exit; you must build one yourselves.

#### 11. Tax Fork — A Decision That Costs Very Little Now but Cannot Be Remedied After the Fact

If you expect any equity transaction within the next 1–3 years (buying him out, being bought out by him, or selling together), **"whether the company has issued and certified share certificates pursuant to Company Act §162" will create a difference of several million in after-tax outcomes**:

- **Transfer of a limited company capital contribution** → **property transaction income**, included in consolidated income, maximum progressive tax rate **40%**
- **Company limited by shares but share certificates not yet issued** → also **property transaction income**, maximum 40%
- **Company limited by shares with share certificates issued** (including scripless issuance) → classified as **securities transaction income**, income tax currently suspended; however, starting from 2021 (Year 110 ROC), this is counted toward the **basic income amount** (alternative minimum tax; tax rate 20%; the deduction for Year 113 [2024] filings is 7.5 million). Additionally, a 0.3% securities transaction tax applies. **Companies established as high-risk startup enterprises for less than 5 years may exclude such stock transaction gains from the calculation.**

Taking sale proceeds of 30 million as an example, the former could be taxed at nearly 12 million; the latter, after the deduction, at approximately 4.5 million. **The difference could exceed 7 million.**

Also note the **"specified equity transaction" under consolidated house-and-land income tax 2.0** (Income Tax Act §4-4): if the shares/capital contribution traded account for **more than half**, and more than 50% of the company's equity value consists of domestic real property, the transaction is taxed as if it were a real property transaction, with a maximum rate of 45%. Your holding is exactly 50% (not more than half), but if a combined sale with others is involved, consult an accountant to confirm.

**Action: this week, consult an accountant on "whether our company should now proceed with share certificate issuance and certification," and retain the opinion in writing.** The cost of this is a few tens of thousands; the value could be in the millions. And it does not require the other party's consent to evaluate in advance.

---

### Track 4: Defense Line for the Worst-Case Scenario

**If he unilaterally issues new shares to dilute you in a company limited by shares:**

- **Assert your §267 III preemptive subscription right.** MOEA interpretive letters (Jing-Shang-Zi No. 11002403250, Year 110 [2021], among others) explicitly recognize this as an **inherent right** — a mandatory provision that cannot be deprived or restricted by the articles of incorporation or a shareholders' resolution; if the company proceeds to solicit subscriptions from specific persons without giving the legally required public notice, the shareholder's right is not forfeited. **This means that even if he has already completed the procedures, you may still be able to assert that the issuance is ineffective as against you.**
- **§23 II fiduciary duty damages**: if he is a responsible person of the company and the transaction involves related parties or is manifestly unfavorable to the company
- **§194 right to demand cessation**: when a director's execution of business violates laws, regulations, or the articles of incorporation, shareholders who have continuously held shares for one year or more may demand that the board stop such conduct
- **§189 action to annul shareholders' resolutions**: if convening procedures or resolution methods are unlawful, an action must be filed within 30 days of the resolution date (**this 30-day period is a peremptory period — miss it and it's gone**); if the content of the resolution is unlawful, invalidity may be asserted under §191
- **Civil provisional remedies**: petition the court for a **provisional disposition (preliminary injunction)** to prohibit processing of the capital increase amendment registration. This is the only tool that can hit the brakes before the procedure is completed — **it is extremely time-sensitive; you must contact a lawyer the moment you learn of it.**

**If the deadlock is completely irresolvable: Company Act §11 judicial dissolution**

> When a company's operations face significant difficulty or major harm, the court may, upon petition by shareholders, after soliciting the opinions of the competent authority and the central competent authority for the specific business, and after notifying the company to submit a defense, order dissolution. For a company limited by shares, the petitioner must have **continuously held 10% or more of the total issued shares for six months or more**; for a limited company, there is no shareholding threshold.

In practice, courts scrutinize "significant difficulty" strictly (requiring evidence of prolonged shareholder discord preventing meetings, business stagnation, sustained losses, etc.), **but its true value lies not in its use but in its existence.** When the other side knows that you know this path exists, that you meet the threshold (50% far exceeds 10%), and that you are already gathering evidence of deadlock — his calculus of "I can drag this out until you capitulate" has to be entirely recalculated.

**This is the heaviest card in your hand, and its best use is to never play it.**

---

## Advanced Gains

### I. "Agree vs. Disagree" Is a False Binary — The Optimal Position Is "Conditional Agreement"

His ultimatum rests on an implicit premise: you can only say yes or no. But a third option exists, and it's stronger:

> "In principle, I agree that the company should bring in external capital at this time. My concerns about the valuation can be addressed in the following ways: (a) staged investment tied to milestones, or (b) give me 45 days to seek a competing offer — if there's no better deal, I'll sign. At the same time, regardless of the outcome of this round, I believe we must first add exit and deadlock mechanisms to the shareholders' agreement — this protects both of us, especially if you're truly considering leaving."

The structural value of this statement:

- **Shifts the dispute from "whether" to "conditions"** — and conditions are always negotiable
- **Positions you as "the constructive party"** — transferring the cost of refusal onto him
- **Directly receives his exit threat and normalizes it** — no confrontation, no pleading, no emotional reaction — instead converting it into a business matter that requires documentation
- **Is completely beyond reproach**: no one can call "requesting 45 days for market comparison" or "requesting exit clauses" unreasonable

### II. The Structural Weakness of an Ultimatum Is That It Requires an Immediate Response

An ultimatum's power derives **entirely** from time pressure. Once it is decomposed into "this requires due diligence," it degrades into an ordinary business proposal.

And you have a statement that is nearly impossible to counter:

> "Any shareholder holding 50% who signs off without seeing the full terms, without understanding the investor's background, and without comparing alternatives is being negligent. I won't do that, and you shouldn't want me to — because if I were that kind of partner, you wouldn't have chosen me in the first place."

**Note**: you must simultaneously provide a clear timeline commitment (e.g., "I'll give you a definitive answer within 45 days"); otherwise this will be correctly read as a stalling tactic, which would worsen the relationship. **The deadline itself is proof of your sincerity.**

### III. His Threat May Be Exactly Your Opportunity

If he truly wants to leave and you want to stay — then from your perspective, this is good news, not bad. The 50/50 deadlock structure itself is your greatest long-term risk. His proactively proposing to leave is equivalent to proactively proposing to eliminate this risk.

**The only question is price and payment terms.** And this is precisely the kind of problem solvable by mechanism (Step 9).

So seriously consider this reverse proposal: **rather than accepting a round of financing you disagree with, redirect that capital to buy his shares instead.** The new investor buys his existing shares rather than new shares → you are not diluted at all → you gain control → the governance vacuum is resolved in one stroke. And for the new investor, "investing in a company with clean equity" is far superior to "investing in a company with a 50/50 deadlock and one reluctant shareholder" — **this proposal is better for all three parties; it just hasn't been put forward yet.**

### IV. "He Is Irreplaceable" Is Usually an Overestimated Fear, but It Must Be Concretely Tested

What determines how painful his departure would be is not feelings but these five specific items:

1. **Who holds the client relationships?** Calculate concretely: among the top ten clients (what share of revenue do they account for?), how many have him as the primary contact? Are the contracts signed by the company or by him personally?
2. **Has the critical technology/code been documented?** If he vanished tomorrow, how many days could the systems keep running? Who holds deployment permissions?
3. **Under whose name are licenses, qualifications, and registrations?** (Architect, CPA, pharmacist, special industry permits — if under his name, this is a hard constraint; everything else is secondary.)
4. **Who holds the supplier relationships and bargaining power?**
5. **Who will the team follow?** Honestly list the core employees and assess each one.

**Fill these five items into a table, and you'll have numbers for his bargaining power.** Fear usually shrinks once made concrete — but if item 3 falls on his side, you must adjust your overall strategy. That is something you cannot circumvent with money or contractual terms.

---

## Self-Critique

I built three parallel vehicle branches but cannot determine which is true, so every path carries conditions; if the entity is actually an offshore company or has undisclosed shareholders, most statutory citations become inapplicable. More critically, for "whether he and the investor already have a private arrangement" I provided only verification methods without being able to determine the facts — if this proves true, the nature of the case shifts from a valuation dispute to a fiduciary duty violation, and the priority of Steps 5–8 should be significantly demoted, with Step 6 elevated to first position.

---

## Next Steps

**External gaps that are truly not derivable through reasoning and are sufficient to flip the strategy (in order of priority):**

1. Company registration type, articles of incorporation, board composition — determines whether he can act unilaterally
2. Cash runway in months — determines the hard ceiling on your negotiation time
3. Full text of the term sheet, particularly option pool placement, liquidation preference, founder vesting, and departure buyback
4. Whether a related-party connection exists between the new investor and him
5. Actual attribution of client relationships, technology, licenses (the five-item test above)
6. The authenticity and motive of his departure intent — this is the only one you cannot derive from documents; it can only be observed from behavior

---

### A Counterintuitive Move That I Believe Has the Highest Return

**Before formally responding to him, independently, directly, and politely contact the new investor.**

The intuitive path is "first sort things out with the partner, then together meet the investor." But this sequence means you can only ever understand the deal through his narrative.

The investor is the only third party who **simultaneously knows the true deal structure and has a motive to be honest with you.** The reason is simple: **no professional investor wants to invest in a company where the 50% shareholder disagrees and the equity structure could collapse at any moment.** Their interests and your interests right now are highly aligned — both want to know the truth.

All it takes is one short letter:

> "Hello, I am ○○○, co-founder and 50% shareholder of ○○ Company. I understand you are evaluating an investment in our company. I would like to tell you directly: I have high confidence in the company's long-term prospects and welcome the right capital partner. Before providing a formal response, I would like to meet with you in person to understand your valuation rationale and collaboration plans. Please suggest a time that works for you."

This letter will produce three effects you cannot obtain through negotiation alone:

1. **Verification**: the investor will inadvertently reveal the deal structure as they understand it — including whether your partner has expressed any intention to leave, whether old-share transfers were discussed, whether there are any side arrangements. This usually surfaces within the first ten minutes of conversation.
2. **Game reset**: once the investor learns that the other 50% has not yet consented, most will immediately demand "resolve the shareholder issue before we discuss investment." **This effectively means a neutral third party, at no cost to you, has created legitimacy for "we must first discuss exit mechanisms"** — which is precisely what you most want to achieve but find hardest to bring up yourself.
3. **Eliminating information asymmetry**: from this moment on, your partner can no longer solely control the narrative.

**The only discipline**: this letter and this meeting must express nothing but a constructive stance throughout — no complaints, no accusations, no airing of your partner's shortcomings, no mention of his departure intent. Your role is "a diligent and responsible shareholder," not "someone coming to file a grievance." The moment you cross the line, you simultaneously lose the investor's trust and your partner's relationship — and this is the loss you can least afford in this case.

At the same time, **on the day you send this letter, inform your partner that you sent it**, and attach the letter's contents. This single action transforms what could be interpreted as "going behind his back" into an irreproachable "I am doing the due diligence I'm supposed to do, and I am being fully transparent with you."

</details>

# AB Test Quality Audit

## Phase Zero: Anchoring

### 0.1 Scenario Portrait

The input is a single colloquial sentence: "My partner and I each hold 50% equity. He wants to bring in a new investor, but I think the valuation is too low. He says if I don't agree, he'll leave. Our partnership agreement only covers profit distribution — there's no exit mechanism. All things considered, what's the best way to handle this?"

Reading the word order: he leads with the structure (50/50), then the disagreement (valuation too low), then the threat (if I don't agree he'll leave), and only at the end adds the foundational defect (no exit mechanism) — this last part is the problem he himself is aware of, yet he placed it in a footnote position. "What's the best way to handle this" is passive phrasing — he has adopted the other party's question as his own.

Reading the word choice: "partnership agreement" and "equity" are used interchangeably. Under Taiwan law, these two terms point to different legal vehicles. Using them interchangeably indicates that the documents themselves have not defined the structure clearly, or that he himself does not understand it. "All things considered" is an explicit scope instruction.

**The cognitive state change this person needs most right now:** from "how should I respond to him" (finding answers within the other party's agenda) to "what is this conflict truly about, what cards do I hold, and what agenda should I be setting." Plus a pre-question he did not ask but which determines everything: what is the legal vehicle — the legal consequences of the four possible vehicles are entirely different and even opposite; until the vehicle is determined, all advice on "what to do" is guesswork.

Second layer: he asked "how to handle this," presupposing "this is a battle I must fight." But the deadlock itself carries costs — every additional month it persists burns cash, client confidence, and relationship capital between both parties. The true intent-optimal target must include "whether this battle is worth fighting, and under what conditions accepting the terms is actually the optimal path."

### 0.2 Cognitive Profile

| Dimension | Assessment | Basis |
|---|---|---|
| Expertise level | High on operations, low on legal | Can run a business but wording reveals unclear legal structure |
| Willingness to act | High and forced | The other party has made a move; not responding equals acquiescence |
| Execution bandwidth | Medium | No staff, but the primary actions here are negotiation and documentation |
| Resource constraints | Unknown but potentially the core variable | Whether he can put up money for a pro-rata follow-on or buyout determines the feasibility of most solutions |
| Bottleneck type | Primarily structural blind spots, secondarily execution blind spots | Cannot see the true strength of the threat, the symmetry of dilution, or that "valuation" may not be the key variable; once seen, needs actionable steps for today |

Bottleneck type determines value form: first reveal the structure to reset the position, then expand into executable procedures at load-bearing nodes.

### 0.3 Reality Conditions List

1. **The legal vehicle is undetermined.** The interchangeable use of "partnership agreement" and "equity" points to at least four possible vehicles (limited company, company limited by shares, close company limited by shares, civil-law partnership). The four produce different or even opposite outcomes regarding capital increase thresholds, transfer restrictions, and preemptive subscription rights. Under a 50/50 limited company, the partner's transfer of capital contribution requires approval by a majority of the user's (sole other shareholder's) voting rights (Company Act Article 111, Paragraph I); the user's refusal directly blocks the transfer, without entering the right of first refusal procedure. Under a company limited by shares, shares are in principle freely transferable (Article 163). The vehicle is the routing condition for the entire case.

2. **50/50 creates deadlock at the shareholder level, but the board is not protected by this.** Board composition is independent of shareholding ratios. If the counterpart is the sole or majority director, it may be possible to issue new shares through a board resolution.

3. **"The valuation is too low" is a subjective judgment unverified by the market.** It may be true, may be mistaken, or may be a proxy for a different grievance.

4. **Capital increase dilution is symmetrical for both parties.** His acceptance of a valuation that equally harms himself necessarily implies a source of compensation or private motive not present in the input. This is a structural fact derivable directly from the input.

5. **"If you don't agree I'll leave" bundles three independent issues.** Whether the company needs external capital, whether these terms are the market's best, and whether he truly wants to leave — the combination of the three determines strategy and cannot be collapsed into a single yes/no question.

6. **The agreement covers only profit distribution = simultaneously missing transfer restrictions, right of first refusal, deadlock-breaking mechanism, valuation method, non-compete, IP ownership, exit pricing, and payment terms.** These gaps persist independently of this round's outcome.

7. **Time pressure is real but its intensity varies by vehicle.** Under a limited company, veto power is complete with no statutory deadline; under a company limited by shares, if the counterpart controls the board, the window may be extremely short. The cash runway constitutes a hard ceiling on negotiation time.

8. **The user's financial capacity is unknown.** Whether he can follow on pro rata, buy out, or withstand the time cost of litigation determines the feasibility of most solutions.

9. **Taiwan's judicial reality.** Civil litigation is measured in years; a provisional disposition is the only tool that can intervene before a registration is completed, and it is extremely time-sensitive.

10. **Operational leverage and legal leverage can be separated.** The actual attribution of clients, technology, licenses, and the team may cause the legally prevailing party to substantively lose.

11. **The income classification of an equity transaction diverges based on "whether share certificates have been legally issued."** This can be decided in advance, cannot be remedied afterward, and does not require the other party's consent.

12. **There may be arrangements between the partner and the new investor unknown to the user.** This is the core of the information asymmetry.

13. **The user is not a legal professional.** Deliverables must be self-initiatable and serve as an interface for working with a lawyer/accountant.

14. **"All things considered" is an explicit scope instruction.** At minimum it encompasses legal, financial (funding/valuation/tax), negotiation, operational control, investor-side, and timeline dimensions.

### 0.4 Granularity Declaration

Length ratio approximately 1:4.7 (A approximately 1,700 characters / B approximately 8,000 characters). The functional index uses independent functional units as its granularity. The core deliverable in this case is a decision framework and executable procedures.

## Phase One: Functional Index

### A Functional Index (16 functional units)

**Legal characterization (4):** Limited company branch covering §106 capital increase, §111 transfer requiring consent, with right of first refusal plus "you must actually have the money to buy in"; civil-law partnership branch covering §683 unanimous consent and withdrawal potentially triggering dissolution and liquidation; company limited by shares branch covering free share transfer and §267 preemptive subscription right; reverse-engineering the document defect from the mixed wording.

**Threat assessment (2):** "Nothing happens without your approval" (bold main thesis); "what he can truly do unilaterally is only to petition for dissolution under Article 11."

**Solutions (4):** Reverse-offer buyout (self-labeled "the most powerful move") with funding prerequisite; four financing structure terms (CB/tranche/earnout/anti-dilution); three questions probing his motive.

**Exit mechanism (1):** Six clause terms including the shotgun clause and its characterization.

**Immediate actions (3):** Don't impulsively sign; switch communication to writing; verify company seals, registered seals, system permissions / verify registration details.

**Reframing and closing (2):** Operational leverage hierarchy statement plus "defend the valuation or defend the company" endgame reframe; closing follow-up.

### B Functional Index (25 functional units)

**Input reconstruction (4):** Vehicle undetermined with four-vehicle comparison table; valuation may be the wrong line of attack with effective pre-money formula and pro-rata subscription neutrality argument; dilution symmetry inference with five compensation sources; the ultimatum is three bundled questions plus "how to handle this" is passive.

**Criteria framework (1):** Four criteria plus three-track parallel execution.

**Diagnostic tools (2):** Sincerity test with three branches; cash runway formula and thresholds.

**Blocking procedures (3):** Vehicle confirmation procedure with findbiz plus inspection request plus five articles-of-incorporation items plus five-branch conclusions; seven-node dual-control table; evidence chain with confirmation email template.

**Valuation handling (3):** Competitive bidding with five channel categories; reverse due diligence with §23/§206/§178; term sheet deconstruction with eight-row comparison plus vesting/leaver contradiction test.

**Structural tools (2):** Three structures for dissolving valuation disagreements; the information-probing nature of staged investment.

**Exit mechanism design (2):** Buy-sell option with failure conditions plus four corrections plus eleven companion clauses; buyout funding six rows including two that are dead ends.

**Tax (1):** Three-way income classification fork plus action item.

**Worst-case scenario (1):** §267 III inherent right plus §23 II plus §194 plus §189 thirty-day peremptory period plus provisional disposition plus §11.

**Advanced gains (4):** "Conditional agreement" script; structural weakness of the ultimatum; reverse proposal; irreplaceability five-item test.

**Closing (2):** Six gaps; investor contact with letter template.

## Phase Two: In-Depth Analysis

### 2.1 Value Positioning

**A's load-bearing points and on-line content.**

Load-bearing points, five: the legal three-branch characterization, the reverse-offer mechanism, the operational leverage hierarchy statement, the endgame reframe (defend valuation vs. defend the company), and the complete characterization of §111.

On-line content — §111's "you must actually have the money to buy in" is a high-frequency misread point in limited company practice that directly changes the priority of cash preparation. The civil-law partnership branch's self-reversal (veto power is stronger, but one partner's withdrawal may trigger dissolution and liquidation) is a trace of reasoning genuinely changing direction within the text. Reverse-engineering the document defect from the wording is a diagnostic reading of the input. The operational leverage hierarchy statement places the entire legal analysis in its proper relative position. The endgame reframe lifts the question from the tactical level to the objective level. On-line proportion is high, with attention concentrated in the opening section (legal characterization) and the closing section (reframe); the middle section is a low-density zone of term lists.

**B's load-bearing points and on-line content.**

Load-bearing points, seven: the input reconstruction cluster (dilution symmetry inference, pro-rata subscription neutrality argument, valuation may be the wrong line of attack), the vehicle confirmation procedure, the seven-node dual-control table, the term sheet deconstruction with contradiction test, the buy-sell option design with failure corrections, the tax fork, and the investor contact.

The highest on-line density — the dilution symmetry inference is a structural fact directly derivable from the input yet almost never thought of, and it resets the entire investigative direction of the case. The pro-rata subscription neutrality argument (if the user subscribes in full, the user's value is neutral at any issuance price; the party harmed is the one who does not subscribe) is counterintuitive and verifiable by calculation. The vesting/leaver contradiction test uses the existence or non-existence of two clauses to reverse-engineer the true deal structure — a single action that can falsify the other party's narrative. The tax fork is a dimension rarely raised in this context and carries irreversibility. On-line absolute volume is large, distributed using the three tracks as routing.

### 2.2 Completeness

**A's five-anchor verification.**

Legal three-branch — scenario visibility present; trajectory incomplete (the confirmation method is a subordinate clause, but item six, "engage a lawyer," serves as a router so the user won't be permanently stuck); expectability of outcome present; reality-load-bearing present; responsibility attribution neutral. Reverse-offer — trajectory broken (the three prerequisite sentences are end-state disguises, see Bias); expectability of outcome does not hold (the dominance claim does not hold under the response's own motive list); responsibility attribution is condition externalization. Exit mechanism — self-labeled as the most important yet delivered as six terms with expansion deferred. §111 complete characterization — all five anchors satisfied; this is the most precise item in the entirety of A. Operational leverage hierarchy — framework type, satisfied. Endgame reframe — framework type, satisfied.

**B's five-anchor verification.**

Vehicle confirmation procedure — scenario visibility present (findbiz plus UBN); trajectory present (print seven items, written request for inspection, five items in the articles clause by clause); expectability of outcome present (each of the five branches has its own conclusion); reality-load-bearing present; responsibility attribution the author continues working through to the five-branch conclusions — all five anchors satisfied. Seven-node dual-control table — each node carries "who can currently act alone" plus the remediation method — all five anchors satisfied. Term sheet deconstruction — eight-row clause comparison with market norm / aggressive version / substantive impact, contradiction test is a single-action probe — all five anchors satisfied. Buy-sell option design — includes failure conditions and four corrections — all five anchors satisfied. Tax fork — includes the specific action "this week, consult an accountant and retain the opinion in writing" — all five anchors satisfied. Investor contact — letter template complete, the three effects are themselves a checklist of "what to listen for," the discipline (no complaints, no accusations, no airing shortcomings) is a posture injunction rather than an information injunction — all five anchors satisfied. Dilution symmetry inference — framework type, connected to three verification channels — all five anchors satisfied.

**Constraint reversal.** Reality Conditions List item 1 (vehicle undetermined) makes all solutions conditional branches. A did not differentiate urgency across branches — the most dangerous branch (company limited by shares, counterpart controls the board) and the safest branch (limited company) receive the same "what to do immediately" checklist. B's Track One blocking procedures (node dual-controls, evidence chain, runway calculation) are vehicle-neutral actions unaffected by this constraint reversal.

### 2.3 Shared Domains

#### How strong is the other party's threat

A's section main thesis: "nothing happens without your approval" as a bold absolute sentence. A then expands three branches within 200 characters, correctly identifying under the limited company branch the full blocking power of §111 (with the warning "you must actually have the money to buy in"), and under the company limited by shares branch explicitly writing "you can't stop him from selling his existing shares." But at the end of the section, A generalizes again to "what he can truly do unilaterally is only to petition for dissolution," which conflicts with the preceding paragraph. The three branches lack differentiated urgency; the most dangerous branch and the safest branch receive the same checklist. A's section five writes "operational leverage often determines negotiation outcomes more than statutory provisions" — A knows that 50/50 protects the equity structure, not the business, yet still wrote "nothing happens" in bold at the opening.

B's four-vehicle comparison table answers three questions cell by cell (can he unilaterally bring in capital, can he freely sell to outsiders, does the user have a pro-rata subscription right). The limited company branch states "veto power is complete; you have time" — under 50/50, the user is the sole other shareholder; refusal equals 0% consent (because "the other shareholders" consist only of the user), directly blocking the transfer (Article 111, Paragraph I). Article 111, Paragraph III's right of first refusal procedure activates only when a transfer has already obtained majority consent but a shareholder dissents — under 50/50 it never activates. The characterization is correct. The most dangerous branch (company limited by shares, counterpart controls the board) is explicitly labeled "most dangerous" with immediate action items. B further repositions Article 11 as the user's own leverage rather than the counterpart's threat — with threshold (six months' continuous holding, 10% or more; the user at 50% far exceeds) and "its best use is to never play it."

A provides a judgment (his threat may be weaker than you think); B provides the basis for a judgment (after cell-by-cell comparison you will arrive at that judgment yourself) plus branch routing.

#### Should the valuation be contested

A accepts "the valuation is too low" as fact and operates entirely within that frame. Section three reframes to "the conflict isn't about how much the valuation is but who bears the cost if the valuation is wrong" — but still presupposes the valuation as the contested issue.

B first questions whether the valuation is the key variable at all. The effective pre-money formula reveals the substantive erosion that option pool placement and liquidation preferences in the term sheet inflict on the headline valuation. Pro-rata subscription neutrality argument: if the user subscribes in full under Article 267, Paragraph III, let the true value be V, the agreed pre-money be P, and the investment amount be I — the full subscriber's end-period net value is always 0.5V, with P not entering the result — a low valuation truly hurts only the party who cannot come up with the follow-on money. From this follows the question "are you objecting to the valuation, or can you not come up with the follow-on money?" Then the dilution symmetry inference: both parties are equally diluted; his acceptance of a valuation that equally harms himself necessarily implies a source of compensation the user has not yet seen — five specific sources (negative information, off-the-table consideration, liquidity pressure, this round is his exit path, runway ending). Finding the compensation source is the true core of the case.

After reading A, the user is still fighting the valuation battle; after reading B, the user discovers the battlefield is elsewhere.

#### How to buy out or exit

A self-labels "the most powerful move: buy him out at his own valuation" and claims "either way, you win." Three prerequisite sentences — "the prerequisite is that you have the money" (if he had the money, he'd buy out directly and wouldn't be stuck in a valuation dispute), "or can negotiate installment payments or an offset against earnings distributions" (if he could negotiate that, he wouldn't need to ask this question), "before making the offer, confirm your funding source first" (the problem is there's no source to confirm). All are end-state disguises. Moreover, the irreversibility of a public offer is not addressed — if he names a price but can't deliver, the other side's "great, when will you pay?" pierces him instantly, and his credibility on every issue goes to zero.

B's Step 0 is the same move but as a private self-test — "are you willing to buy his 50% at the valuation you assert?" Three branches: willing and able, jump to the offer; willing but unable, route to financing, term deconstruction, mechanism design — do not make the offer; not willing, directly names the true motive (control being diluted, the humiliation of the ultimatum, distrust of him) and warns that using the valuation as the battlefield will lose. Step 10 provides six rows of buyout funding sources: installment 2–4 years with share pledge or promissory note with transfer linked to payment progress; earnings offset year by year; bring in a new investor to buy existing shares (user zero dilution); Article 167-1 company buyback with 5% and retained earnings cap; Article 113 capital reduction equally deadlocked under 50/50; bank acquisition loan — six rows, two of which tell the user this path is closed. Advanced Gains section three additionally proposes a reverse deal — use this round's capital to have the investor buy existing shares rather than new shares, zero dilution, gain control, better for all three parties — this is the direct solution to A's funding prerequisite problem.

The same buyout action: A offers first, confirms funding later (information disclosure is irreversible); B confirms first, then routes (failure doesn't expose).

#### Deadlock mechanism

A recommends the shotgun clause plus "naturally forces fair pricing," without failure conditions.

B offers the same mechanism, then explicitly writes "the cash-rich party enjoys a structural advantage. If you are cash-disadvantaged, accepting the standard version is tantamount to volunteering for the guillotine." Followed by four corrections: seller prices, buyer chooses plus mandatory 24–36 month installments secured by share pledge; dual-track valuation with three-report median if gap exceeds 15%; 60–90 day financing window after triggering; amount threshold switching to third-party valuation.

A's version is direction-negative under the user's most probable conditions (cash-disadvantaged — he is opposing the valuation precisely because he can't come up with the follow-on money). Same-position opposite-direction.

#### What should exit clauses contain

A self-labels "this is the most important thing to secure." Delivery: six clause terms. The closing asks "would you like me to compile it into a checklist" — at the self-labeled most important node, expansion is deferred to the next round. Additionally, "you must add an exit mechanism" does not address why the other party would sign — he is currently issuing an ultimatum, and signing would constrain himself.

B provides eleven companion clauses, each with its own rationale. Additionally proposes the "conditional agreement" script: "regardless of the outcome of this round, I believe we must first add exit and deadlock mechanisms — this protects both of us, especially if you're truly considering leaving" — using his exit intent as the very reason to sign. The script carries its own failure condition: a clear timeline commitment must be given simultaneously; otherwise it will correctly be read as stalling.

A reaches the door (names the clauses); the door doesn't open (no expansion, no reason for the other party to sign).

#### Control audit

A: "verify the actual control status of the company seals, bank accounts, registered seals, and system permissions" — four terms, no remediation.

B: seven-row table, each row carrying "who can currently act alone" and the remediation method — go to the bank to set up dual seal and daily cumulative transfer limits; remove single-person authorization and switch to dual-person verification; write to the CPA declaring 50% shareholder status and requiring simultaneous notification of changes; ensure co-owner rather than member status; search trademarks at TIPO; back up contract originals to an independently accessible location; request access to accounting books in writing per §210 and retain copies.

A identifies the nodes; B arrives at the nodes and remediates.

#### Motive identification

A: three questions — cash shortage? Loss of confidence? Better opportunity elsewhere? Asked and not followed up, with no channels connected. This is levying a generation tax — asking the user to determine which one applies, when the user asked this question precisely because he can't make that determination.

B first derives from dilution symmetry that "there must be a compensation source," then lists five specific sources, then connects three verification channels. Channel one: reverse due diligence (search findbiz for the investor entity's registration, cross-reference for shared addresses, related persons, family connections, co-invested targets; if a related-party connection exists without disclosure, this implicates Article 23, Paragraph I fiduciary duty and Article 206 applying Article 178 mutatis mutandis for director conflict-of-interest recusal). Channel two: demand the full term sheet — refusal alone constitutes justification for declining — then use the vesting/leaver contradiction test to reverse-engineer the true deal structure (if vesting exists, signing means he can't leave — why would he sign? If vesting is absent, no investor would accept a 50% founder who can walk away at any time with all equity — why would they tolerate it? Both outcomes point to the true deal structure differing from the relayed version). Channel three: proactively contact the investor (letter template plus three effects plus same-day notification to the partner).

A asks the user a question the user cannot answer himself; B provides the methods for finding out.

#### Timeline

A: "what to do immediately in the next few days" — six items, no deadlines, no sequencing.

B: Track One 72 hours plus 45-day competitive bidding deadline plus awareness of term sheet validity period plus Article 189's thirty-day peremptory period. Advanced Gains section two explicitly writes "you must simultaneously provide a clear timeline commitment."

#### Tax

A: "engage a lawyer and an accountant — one to examine the structure, the other to examine the valuation" — the accountant is pointed toward the valuation (a subjective variable). Yet the accountant's only irreplaceable, non-remediable, unilateral task in this situation is the income classification fork — whether share certificates have been issued under Article 162 determines whether a future equity transaction is taxed at 40% as property transaction income or goes through the securities transaction income path plus the alternative minimum tax.

B: three-way income classification and tax rate fork with a worked example (sale proceeds of 30 million: the former could be taxed at nearly 12 million, the latter at approximately 4.5 million after deductions, with the difference potentially exceeding 7 million); the consolidated house-and-land income tax 2.0 specified equity transaction "more than half" threshold (the user at exactly 50% does not exceed half, but a combined sale requires accountant confirmation). Explicit action item: "this week, consult the accountant on whether share certificate issuance and certification should be undertaken, and retain the opinion in writing" — the cost is tens of thousands, the value could be millions, and it does not require the other party's consent.

A's most expensive professional resource is pointed at the wrong place; the irreversible window is closing.

#### Error prevention

A: zero prohibitions. Nothing prevents any action that could accelerate the user's loss of position.

B: explicit prohibitions — do not imply consent (do not help prepare capital increase documents, do not accompany the partner to meet the investor without taking a position), do not verbally express agreement or in-principle support. Proactively generates a 24-hour meeting confirmation email template: "if there are any discrepancies in my understanding, please reply with corrections within three days."

### 2.4 Four Tables

#### A Differential

After exhaustively examining each of B's 25 units:

**§111, Paragraph III's complete characterization — "you must actually have the money to buy in."** Testing against B: B's limited company branch correctly identifies the user's complete blocking power under 50/50. B's Step 0 sincerity test has a "willing but unable" branch; Step 10 is a complete buyout funding table — "you may need cash" is present throughout B. But B's coverage addresses the active buyout (you want to buy, and can take your time to negotiate); A addresses the passive trigger (he initiates, you don't buy and it's deemed consent, time pressure may exist). However, in the 50/50 scenario of this case, the user's refusal directly blocks the transfer; Article 111, Paragraph III's right of first refusal never activates — A's warning addresses a scenario that won't occur in this case. As general legal knowledge transmission, there is a marginal increment; as a decision aid in this case, the increment approaches zero. Holds, marginal.

**Civil-law partnership: the final state of partnership dissolution following withdrawal.** Testing against B: B has the complete procedural treatment of §686, §689, §690, §681, and §683. But B does not articulate the legal principle that in a two-person partnership, one partner's withdrawal causes the partnership to cease to exist (a partnership requires two or more persons; when only one remains, it dissolves). A's "one partner's withdrawal may go straight into dissolution and liquidation" is more complete here. However, this branch is excluded by the scenario — no one negotiates a term sheet and valuation under a civil-law partnership; they would first restructure as a company. Holds, scenario weight approaches zero.

**Reverse-offer mechanism.** Testing against B: B's Step 0 is the same move in a private version; item 21 (the reverse proposal) is a better version toward the same objective. The only residual is the "offer first, confirm funding later" sequence, and that sequence is direction-negative — irreversible. Does not hold.

**Reverse-engineering the document defect from the wording.** Testing against B: B's Input Iteration opens with the same observation ("you used equity and partnership agreement interchangeably"), followed by the four-vehicle comparison table. Does not hold.

**"Who bears the cost if the valuation is wrong" reframe.** Testing against B: B's Step 8 devotes an entire section to dissolving the valuation disagreement, and does so at a more upstream level — B questions whether the valuation itself is the key variable. A raises the question; B gives the answer. Does not hold.

**Operational leverage hierarchy statement.** Testing against B: B's irreplaceability five-item test ends with "if licenses fall on his side, you cannot circumvent it with money or contractual terms" — an equivalent-acuity hierarchy judgment, and a conditional one (identifying which item constitutes an impassable hard constraint). Criteria framework condition four, "nine out of ten 50/50 disputes die from communication style, not legal provisions," is another hierarchy judgment. Does not hold.

**"Defend the valuation or defend the company" endgame reframe.** Testing against B: B's Step 0, third branch — "what you truly care about isn't the valuation but your control being diluted, the humiliation of the ultimatum, or distrust of him" — is the same reframe at higher resolution, with each branch carrying a different subsequent route. Does not hold.

**Shotgun clause and its characterization.** Testing against B: B's Step 9 provides the same mechanism, same characterization, plus failure conditions and four corrections. A's version is direction-negative under the user's most probable conditions. Does not hold.

A Differential: 2 items, all marginal or scenario-excluded. The remaining 6 items are all covered in B, with B's version more complete or directionally more correct.

#### B Differential

Confirming each of A's 16 units for non-coverage (exhaustive check, taking residual increments):

Dilution symmetry inference with five compensation sources and three verification channels — entirely exclusive (A has three motive questions but as a list rather than a derivation, and without connected channels).

Pro-rata subscription neutrality argument — entirely exclusive (A has §267's existence but only says "you can put up the money to maintain 50%" without deriving value neutrality).

Sincerity test with three branches including the third branch's true-motive identification — entirely exclusive (A's reverse-offer covers the first branch but lacks the other two and has reversed sequencing).

Vehicle confirmation complete procedure — largely exclusive (A has the four words "verify registration details").

Seven-node dual-control table — largely exclusive (A has four node terms without remediation).

Cash runway formula and threshold branches — entirely exclusive (A identifies the funding constraint three times, treats it zero times).

Five categories of funding channels — entirely exclusive.

Reverse due diligence with §23/§206/§178 — entirely exclusive.

Term sheet eight-row clause deconstruction — entirely exclusive.

Vesting/leaver contradiction test — entirely exclusive.

Three structures for dissolving valuation disagreement — partial (A has four terms; B has applicable scenarios and information-probing rationale).

Shotgun clause failure conditions plus four corrections — entirely exclusive, and A is same-position opposite-direction at that location.

Buyout funding six rows including two indicating the path is closed — entirely exclusive.

Reverse proposal (investor buys existing shares) — entirely exclusive.

Tax fork with three-way income classification plus action item — entirely exclusive.

Article 11 as the user's own leverage — same-position opposite-direction (A characterizes it as the counterpart's threat and reassures the user not to worry; B positions it as the user's card with threshold data).

"Conditional agreement" script with failure condition — entirely exclusive.

Evidence chain with meeting confirmation email template — largely exclusive (A has "switch communication to writing").

Eleven exit companion clauses with rationale — largely exclusive (A has six terms).

Irreplaceability five-item test with licenses as hard constraint — largely exclusive (A has the hierarchy statement).

Prohibition against implied consent — entirely exclusive.

Investor contact with letter template — entirely exclusive.

Three-track parallel execution with 72-hour time window — entirely exclusive.

B Differential: 23 items, of which 15 entirely exclusive, 5 largely exclusive, 1 partial, and 2 same-position opposite-direction.

#### A Bias

**Candidate one: All three premises of the self-labeled "most powerful move" are end-state disguises.** Condition: 0.3 item 8. "The prerequisite is that you have the money" — if he had the money, he'd buy out directly and wouldn't be stuck in a valuation dispute. "Or can negotiate installment payments or an offset against earnings distributions" — if he could negotiate that, he wouldn't need to ask this question. "Before making the offer, confirm your funding source first" — the problem is there's no source to confirm. Detection: the thing compressed into a verb ("confirm") is exactly the reason he can't do it (there is no source to confirm). Self-label at the highest altitude ("the most powerful move"); delivery at the shallowest depth (all three sentences are end states, not paths). Moreover, the irreversibility of a public offer is not addressed — the other side's "great, when will you pay?" pierces him instantly, and credibility on every issue goes to zero. Counterpart side at the same position: Step 0 conducts a private self-test first; when unable to afford it, the route goes to financing / term deconstruction / mechanism design, not to making an offer. **Changes the path (information disclosure is irreversible).**

**Candidate two: "Nothing happens without your approval" and "what he can truly do unilaterally is only to petition for dissolution" — both absolute sentences are false.** Condition: 0.3 items 2 (board independent of shareholding) and 10 (operational leverage can be separated). He can stop working, take clients, sell existing shares in a company limited by shares, issue new shares through the board, petition for judicial dissolution, and use the deadlock itself as a weapon to outlast the user. 50/50 protects the equity structure, not the business. A itself writes in section five that "operational leverage often determines negotiation outcomes more than statutory provisions" — A knows this, yet still wrote the bold absolute sentence at the opening. Moreover, "what he can truly do unilaterally is only to petition for dissolution" directly conflicts with A's own "you can't stop him from selling his existing shares" — the two sentences are less than 300 characters apart. Counterpart side at the same position: Track One's 72-hour seven-node dual-control table is entirely aimed at "things he can do without your approval." **Changes the path (provides a false sense of security; the user may delay action under the most dangerous branch).**

**Candidate three: The shotgun clause is presented without failure conditions and is direction-negative under the user's most probable conditions.** Condition: 0.3 item 8. A recommends a mechanism that "naturally forces fair pricing." But the cash-rich party enjoys a structural advantage — the probability that the user is cash-disadvantaged is extremely high (he is opposing the valuation precisely because he can't come up with the follow-on money). A identifies cash as a constraint three times in the same response (§111 "you must actually have the money to buy in," §267 "you can put up the money yourself," reverse-offer "the prerequisite is that you have the money"), yet when recommending a mechanism that punishes the cash-disadvantaged party, attaches no warning whatsoever. Identified 3 times, treated 0 times, recommended tool is direction-negative. Counterpart side at the same position: explicitly states "tantamount to volunteering for the guillotine" plus four corrections. **Direction-negative (same-position opposite-direction).**

**Candidate four: The self-labeled "most important thing to secure" (exit mechanism) is delivered as six terms with expansion deferred to the next round.** Condition: 0.3 item 6. Self-label at the highest altitude ("this is the most important thing to secure"); delivery at the lowest depth — six terms, none expanded. The closing asks "would you like me to compile it into a checklist," deferring all content at the self-labeled most important node to the next round. Additionally, "you must add an exit mechanism" does not address why the other party would sign — he is currently issuing an ultimatum; signing would constrain himself. A provides zero leverage across the entire response. The self-labeled peak and delivery valley coincide. Counterpart side at the same position: eleven companion clauses each with rationale; additionally proposes a script that gives the other party a reason to come to the table and sign. **Changes the path.**

**Candidate five: "Anti-dilution provisions: protect your proportion in subsequent rounds" — direction-negative.** Condition: 0.3 items 3 (valuation is subjective) and 12 (information asymmetry). Anti-dilution is a protection clause for preferred shareholders (the new investor) — when the next round is a down round, it adjusts the conversion price (typical mechanisms being full ratchet or weighted average), with the cost borne by common shareholders (the user and the partner), manifested as the post-conversion share count increasing and thereby diluting common shareholders. A lists a clause that benefits the investor as something the user should pursue for self-protection. If the user acts on this, he will be fighting for something that works against him. Counterpart side at the same position: the term sheet clause table lists "anti-dilution: full ratchet → if the next round is a down round, you get crushed." **Direction-negative (same-position opposite-direction).**

**Candidate six: The funding constraint is identified three times, treated zero times.** Condition: 0.3 item 8. §111 "you must actually have the money to buy in," §267 "you can put up the money yourself to maintain 50%," reverse-offer "the prerequisite is that you have the money" — A determines three times that cash is a key constraint. Among the six items in "what to do immediately," zero address money — no runway calculation, no funding channel list, no assessment of pledgeable assets. Counterpart side at the same position: Step 0 (sincerity test routes by financial capacity) plus Step 4 (runway formula and thresholds) plus Step 5 (five categories of funding channels including VC / bank / government subsidies / industry capital / personal) plus Step 10 (six-row buyout funding table) — four layers of treatment. **Changes the path (the most load-bearing constraint has no prescription).**

**Candidate seven: Accountant mismatch.** Condition: 0.3 item 11. A assigns the accountant to examine the valuation — a subjective variable that is itself the disputed issue (and B's analysis shows the valuation may not even be the real problem). Yet the accountant's only irreplaceable, non-remediable, consent-free task in this situation is the income classification fork — whether share certificates have been issued under Article 162 determines whether a future equity transaction is taxed at 40% property transaction income or goes through the securities transaction income path plus the alternative minimum tax. Taking sale proceeds of 30 million as an example, the difference could exceed 7 million. The most expensive professional resource is pointed at the wrong place, and the irreversible window is closing. Counterpart side at the same position: "this week, consult the accountant on whether share certificate issuance and certification should be undertaken, and retain the opinion in writing." **Irreversible opportunity loss.**

**Candidate eight: "Do not sign anything while emotional, including meeting minutes" and "switch all communication to writing and keep records" pull in opposite directions on the same asset within the same checklist.** Condition: the logic of evidence chains. Meeting minutes are not a binding document — they are evidence. Not signing and not correcting equals tacitly accepting the other party's version — if the other party later produces meeting minutes that the user neither signed nor corrected, it becomes legally very difficult to deny their contents. Counterpart side at the same position: proactively generates a 24-hour meeting confirmation email, neutral and fact-oriented in tone, "if there are any discrepancies in my understanding, please reply with corrections within three days" — the lowest-cost action to convert verbal leverage into verifiable facts. **Changes the conclusion (the evidence chain works against the user).**

**Candidate nine: "All things considered" — six dimensions, zero coverage.** Condition: 0.3 item 14. The user explicitly wrote "all things considered" — this is an explicit scope instruction. Dimensions A covers zero on: tax (not mentioned anywhere in the response; the accountant is directed to the valuation), funding channels (identified three times, treated zero times), the investor side (zero contact, zero due diligence, the identity of the investor is unknown), timeline and deadlines (only the three words "the next few days"), operational control remediation (only "verify the status" without remediation methods), relationship management and scripts (zero scripts — what is the user supposed to say when facing the partner today?). **Changes the path.**

A Bias: 9 items, of which 3 are direction-negative (the recommended tool harms the user under the user's most probable conditions), 3 are end-state disguises or condition externalizations, 1 is an irreversible opportunity loss, 1 is self-contradictory, and 1 is a scope instruction not reconciled.

#### B Bias

Examining each candidate via depth-monotonicity level-by-level pursuit:

**Candidate one: the response is too long (6,000 characters), creating a reading barrier for a user facing urgent decision pressure.** Initial observation: reading it takes over 15 minutes, and the user is being pressed by an ultimatum. Pursuing one additional level — revisiting whether the response addresses this elsewhere: the three-track parallel declaration plus "Track One, 72 hours" allows the reader to skip to the relevant track rather than reading linearly. The Step 0 sincerity test's three branches route the reader to the corresponding next steps within 30 seconds. Step 5's opening labels itself "the single highest-leverage action in this case" — even if the preceding is skipped, there's an entry point. The cost of length falls on reading (a few minutes); the cost of A's gaps falls on irreversible resources (the credibility of a public offer, the direction of anti-dilution advocacy, the cash-disadvantage penalty of the shotgun clause, the closing of the tax window). Overturned.

**Candidate two: the limited company branch's "your veto power is complete; you have time" does not mention Article 111, Paragraph III's right of first refusal mechanism — A is more precise here.** Initial observation: A writes "you must actually have the money to buy in"; B does not. Pursuing one additional level — revisiting the legal structure per 0.3 item 1: a 50/50 two-person limited company where the user is the sole other shareholder. Article 111, Paragraph I requires approval by a majority of the other shareholders' voting rights for transfer; the user's refusal equals 0% consent (because "the other shareholders" consist only of the user), directly blocking the transfer. Article 111, Paragraph III's right of first refusal activates only when a transfer has already obtained majority consent but a shareholder dissents — under 50/50 it never activates. Therefore B's "veto power is complete" is entirely correct in this case scenario, and "you have time" also holds — no statutory clock is running. A's Article 111, Paragraph III warning in this case context is a warning about something that will not occur. Overturned.

**Candidate three: Article 356-12 excluding Article 267 is cited as Paragraph II (actually Paragraph III).** Initial observation: paragraph number citation error. Pursuing one additional level — the user or their lawyer, upon turning to the statute, immediately sees the correct paragraph number and will not take an incorrect action based on this. B's entire argument (close company has no preemptive subscription right; dilution risk is highest) holds fully under the correct paragraph number. Decision impact is zero. Recorded as a correction note, not as a bias.

**Candidate four: the tax section's alternative minimum tax deduction cites the Year 113 (2024) figure (7.5 million), which may have been adjusted by Year 115 (2026).** Initial observation: the number may be outdated. Pursuing one additional level — B itself, in the same sentence, qualifies it with "for Year 113 (2024) filings," making the reader aware that the current year's figure needs confirmation. And B's action item in the same paragraph is "this week, consult the accountant" — the accountant will provide the current correct figure. The 30 million worked example's functional role is a magnitude benchmark ("is it worth spending tens of thousands to consult the accountant?"); at that magnitude, the difference between 7.5 million and a possibly adjusted figure does not change the magnitude judgment. Decision impact is zero. Recorded as a correction note, not as a bias.

**Candidate five: staged investment as a "lie detector" — the investor may not accept milestone-based tranches, and such refusal would be unrelated to the partner's beliefs.** Initial observation: refusal may come from a third party rather than the partner, so "the party that refuses staged investment is revealing their true beliefs" fails when the investor refuses. Pursuing one additional level — revisiting whether B treats the investor as an independent actor across the full text: Step 6 independently verifies the investor through reverse due diligence; Step 7 demands the full term sheet with refusal itself as grounds for declining; item 25 explicitly characterizes the investor as "the only third party who simultaneously knows the true deal structure and has a motive to be honest with you" and establishes a direct contact channel. Within B's architecture, the user is not passively waiting for the partner to relay the investor's response but obtains the investor's independent response through multiple channels — if the investor refuses staged investment, the user hears the investor's reasoning directly rather than through the partner's retelling. Moreover, "the investor does not accept staged investment" is itself valuable information feedback — it eliminates several of the five partner-motive possibilities B lists, such as "the runway is ending; any money is better than none." Overturned.

**Candidate six: contacting the investor first could alert the prey — if the partner and investor have an off-the-table arrangement, open contact may cause existing traces to be cleaned up or rewritten before they are recorded, creating a timing conflict with Step 6's reverse due diligence.** Initial observation: Step 6 relies on existing traces (related-party connections, co-invested targets); contacting first may destroy these traces. Pursuing one additional level — revisiting how B handles this: B explicitly writes "on the day you send this letter, inform your partner that you sent it, and attach the letter's contents" — transparency makes this action irreproachable. Moreover, Step 6's reverse due diligence relies on public registration data (findbiz for the investor entity's registered address, representative, board of directors, scope of business) — these are records in a government public database, not private traces that can be cleaned up or destroyed. The premise of the timing conflict — "contact will cause traces to be destroyed" — does not hold because the two steps use different types of information sources: Step 6 uses public registrations; the investor contact uses face-to-face conversation. Overturned.

**Candidate seven: Article 267, Paragraph III "does not forfeit the shareholder's right" — B's worst-case scenario section writes "even if he has already completed the procedures, you may still be able to assert that the issuance is ineffective as against you"; is the inference stronger than the basis?** Initial observation: "does not forfeit the right" and "the issuance is ineffective as against you" appear to be two different things — the former means the shareholder's subscription right persists, the latter addresses the validity of the entire issuance. Pursuing one additional level — revisiting what question B's sentence answers: B is addressing the scenario "he unilaterally issues new shares to dilute you in a company limited by shares" and lists four remedies (§267 III, §23 II, §194, provisional disposition). B's "ineffective as against you" functionally means "your subscription right does not disappear just because he didn't notify you" — which is precisely the plain-language rendering of the MOEA interpretive letter's "does not forfeit the shareholder's right." B simultaneously provides the final item, a provisional disposition with "extremely time-sensitive; contact a lawyer the moment you learn of it" — both post-hoc assertion (subscription right not forfeited) and real-time action (injunction) are covered. The wording "ineffective as against you" is not perfectly precise (strictly speaking, it is the subscription right that persists rather than the issuance being void), but the direction of action the user would take based on it is entirely correct — he would go assert his subscription right. Overturned.

**Candidate eight: B builds a five-branch selector (limited company / company limited by shares / close company / civil-law partnership / company limited by shares with even board), but after Step 5 writes only for the limited company and company limited by shares branches; the civil-law partnership branch terminates at "first priority: address §681 exposure," and the close company branch does not appear again after §356-12.** Initial observation: five branches declared but only two given prescriptions; for the remaining three, the reader may assume they have been addressed. Pursuing one additional level — revisiting the functional role of the branches: B builds five branches for the purpose of completing the vehicle diagnosis in Step 1, letting the user know which branch they fall into and then turn to the corresponding conclusion. Diagnosis does not equal a promise of prescriptions — a doctor saying "you might have one of five conditions; let's do a blood test first" does not mean he must write five prescriptions before the blood test. Moreover, the civil-law partnership is excluded by the scenario — no one negotiates a term sheet and valuation under a civil-law partnership; they would first restructure as a company. Close companies account for a very small fraction of all companies in Taiwan. B concentrates resources on the two branches covering the majority of real situations — a reasonable allocation of resources. Overturned.

**Candidate nine: B's Step 1 cites §210 for requesting inspection of five categories of documents, but §210's scope does not include board meeting minutes; moreover, §210 is a provision for companies limited by shares — the path for a limited company is Article 109 applying Article 48 mutatis mutandis.** Initial observation: the statutory citation is incorrect under the limited company branch, and the scope includes one extra item. Pursuing one additional level — revisiting the functional role of this passage: B's purpose is to get the user to obtain the articles of incorporation, shareholder register, past meeting minutes, and financial statements. For a 50/50 co-founder, he almost certainly simultaneously holds director status, and the Taiwan High Court (Year 107 [2018], Shang-Zi No. 1505) permits a shareholder who is also a director to inspect board meeting minutes from their term of office. And in practice, a 50% shareholder's written request to inspect company documents is usually honored — refusal is the anomalous signal (B also writes "a refusal is itself important evidence"). The direction of action the user would take is entirely correct (go inspect); the statutory citation's precision issue will be corrected by the lawyer upon engagement. Overturned.

**Candidate ten: B's exit mechanism companion clauses state regarding non-competes that "a non-compete clause without compensation is roughly equivalent to no clause at all" — this is the standard from Labor Standards Act Article 9-1 for employees; does it extend to shareholder exit agreements?** Initial observation: shareholders are not employees; the Labor Standards Act's compensatory-measure requirement does not apply. Pursuing one additional level — revisiting what B is doing in that passage: B's Step 9 is designing an **ex ante** shareholders' agreement (nobody is leaving yet; the goal is to negotiate the rules now), not a clause for the buyout closing. In the context of an ex ante agreement between parties of comparable bargaining power, a non-compete clause with no consideration is indeed more vulnerable in judicial review — courts consider the reasonableness between the restriction's scope and the compensation, and even outside the Labor Standards Act, Civil Code Article 247-1's unconscionability principle may still cause an overbroad non-compete clause to be judicially reduced. B's bold statement ("roughly equivalent to none") is rhetorically somewhat absolute, but the direction of action is correct — it reminds the user to pair the non-compete with compensation; otherwise enforceability will be low. Overturned.

**Candidate eleven: B's Step 4 calculates the cash runway and notes "if less than 6 months, all your 'I need time to evaluate' statements are empty words," but Step 5 gives a 45-day competitive bidding deadline and asserts "there is no legitimate reason to require a 50% shareholder to accept financing terms without market comparison" — when the runway is under 6 months, the two steps conflict.** Initial observation: Step 4 says there isn't enough time; Step 5 needs time. Pursuing one additional level — revisiting whether B addresses timeline flexibility elsewhere: Advanced Gains section two explicitly writes "you must simultaneously provide a clear timeline commitment ... the deadline itself is proof of your sincerity" — B treats the 45 days as a negotiable item, not a rigid requirement. The 45 days is a self-budget ("give yourself a 45-day deadline"), not a condition imposed on the other party. Moreover, Step 4's runway threshold is itself a router — under 6 months routes to "immediately initiate Step 5" (accelerated version); over 12 months means his urgency comes from elsewhere (return to Input Iteration point three to find the motive). The two steps are not pulling in opposite directions on the same timeline but giving different advice at different runway lengths. Overturned.

**Candidate twelve: B's effective pre-money formula "effective pre-money = headline pre-money / (1 + option pool ratio)" — the denominator's "option pool ratio" does not define whether the ratio is of pre-money or post-money, and the two methods differ significantly.** Initial observation: the formula is incomplete; a non-expert user cannot use it. Pursuing one additional level — revisiting the formula's functional role: B uses this formula not to have the user calculate an exact number but to reveal the mechanism that "carving the option pool from pre-money substantively reduces your valuation." B immediately follows with "a term sheet reading pre-money 100 million, pool 15% carved from pre, ... is worth substantially less in real terms than pre-money 80 million, pool carved from post" — the specific numerical example has already conveyed the mechanism. Moreover, when the pool is calculated using the pre-money's existing share count as the denominator, P/(1+p) is mathematically fully correct. The formula is an introduction leading to the term sheet deconstruction (Step 7), not a standalone calculation tool — the user's action based on it is to examine where the pool sits in the term sheet, not to calculate the pre-money himself. Overturned.

B Bias: 0 items. Twelve candidates, after depth-monotonicity level-by-level pursuit to invariance, yielded ten overturned and two correction notes (zero decision impact). The exposure surfaces are not comparable (A has approximately 8 verifiable statutory claims; B has approximately 30).

### 2.5 Gestalt Recomposition

Stepping back from the atomic structure, three dimensions that, if absent, would significantly affect the gap assessment:

**A compresses the hard parts into a verb; B spends its length on the hard parts.** "Can negotiate installment payments" compresses the entire financing and negotiation challenge; B's Step 10 six rows address that very thing — and two of the six rows tell the user the path is closed. "Confirm your funding source" is an end-state disguise — if a source existed, there'd be no need to ask. "Engage a lawyer and an accountant — one to examine the structure, the other to examine the valuation" compresses the choice of "what the accountant's highest-value task actually is" — B expands that choice (the tax fork) and points the accountant at the irreversible window.

**Same-position opposite-direction accounts for one-third of the biases.** The shotgun clause (A's recommended mechanism is a suicide tool under the user's conditions); anti-dilution (A recommends a clause that protects the opposing side as the user's own protection); Article 11 (A characterizes the user's own card as the counterpart's threat and reassures the user not to worry). The nature of the gap is not that B said more — it's that A causes the user to act wrongly at three nodes. The consequence of following A is not "missing something" but "doing something wrong."

**Condition externalization and the identify-treat gap.** A identifies cash as a key constraint three times; the action list treats it zero times. The two self-labeled highest points ("the most powerful move" and "the most important thing to secure") have the lowest delivery depth. A's response as a whole is not "insufficiently deep" — A's complete characterization of §111 is precise and constitutes A's true differential — but at the nodes self-labeled as most important, A systematically externalizes the work back to the user. A's precision appears at the legal analysis layer; A's gaps appear at the "so what do you actually do" layer — and what the user asked is precisely the latter.

## Phase Three: Composite Judgment

The gap begins at the diagnosis — A accepts "the valuation is too low" as fact and operates within that frame; B dismantles the frame (dilution symmetry inference, pro-rata subscription neutrality argument) and identifies that the true variable lies elsewhere. After reading A, the user is still fighting the valuation battle; after reading B, the user discovers the battlefield is "finding the real reason the other party accepted an unfavorable valuation."

Four qualitative dimensions of the gap:

**Diagnostic reversal gap.** A's "nothing happens without your approval" does not hold under one of its own branches yet is not differentiated; the most dangerous branch and the safest branch receive the same checklist. B's four-vehicle comparison table performs a cell-by-cell comparison with built-in branch routing; the most dangerous branch is labeled with immediate action items. One level deeper — B shifts the user from "responding to the other party's agenda" to "setting his own agenda" — this cognitive displacement pervades the entire response (Input Iteration's closing line: "the optimal solution is usually not to win on their terms but to reset the agenda") rather than being a single paragraph's insight.

**Directional gap.** Of 9 bias items, 3 are direction-negative — the recommended tool harms the user under the user's most probable conditions. Anti-dilution is an investor protection clause presented as the user's protection; the shotgun clause is a suicide tool under cash disadvantage, yet A identifies cash as a constraint three times and recommends this mechanism without any warning; a public offer with unconfirmed funding is irreversible information disclosure. B's treatment at these three nodes is in every case directionally opposite. The nature of the gap is not that A is missing something — it's that A would cause the user to do things that harm himself at three points.

**Completion depth gap.** The densest concentration of gap across the same material. "Confirm your funding source" versus a six-row funding table with two rows indicating the path is closed; "verify registration details" versus findbiz plus written inspection request plus five articles items plus five-branch conclusions; six clause terms versus eleven companion clauses each with rationale; three motive questions versus the dilution symmetry derivation plus five sources plus three verification channels plus the vesting/leaver contradiction test. A reaches the door; the door doesn't open.

**Dimensional coverage gap.** The user explicitly wrote "all things considered." Dimensions A covers zero on: tax, funding channels, investor side, timeline, operational control remediation, relationship scripts — six dimensions. B covers all six.

**User benefit layer.** After reading A, the user gains: a sense of security that "he may not be as strong as you think" (misleading under the most dangerous branch); a move called "buy him out at his own valuation" (naming a price without being able to deliver would destroy credibility); six clause terms to bring to a lawyer. His first actionable thing today: engage a lawyer and an accountant — but the accountant is directed to the valuation rather than the tax fork. Where he will go wrong: accepting a shotgun clause without failure conditions (direction-negative under his conditions), fighting for anti-dilution (which protects the opposing side), making a public offer without confirmed funding (irreversible).

After reading B, the user gains: a diagnostic reversal he absolutely would not have thought of on his own (you may not have a valuation problem — you may have a follow-on funding problem, and a low valuation is nearly neutral to you if you subscribe in full); a 30-minute sincerity self-test that determines the subsequent routing of everything; a vehicle-neutral blocking procedure for the next 72 hours (seven-node dual-controls, evidence chain, runway calculation); three channels for verifying the partner's true motive including a single-action probe; a script that gives the other party a reason to sign exit mechanisms; a safe deadlock mechanism design for the cash-disadvantaged with four corrections; a task for the accountant this week on an irreversible tax window. His first actionable thing today: 30-minute sincerity self-test, findbiz for the vehicle, open a notebook for meeting confirmation emails. Where he will be stuck: the close company or civil-law partnership special branches — but both involve waiting for lawyer confirmation rather than going in the wrong direction.

**The nature of the gap is not "B is more detailed."** It is that A pushes the user toward actions harmful to himself at three nodes; that A compresses the hard parts of its two self-labeled most important items into verbs and returns them to the user; that A identifies the core constraint three times and treats it zero times; that A answers a user who asked "all things considered" with six dimensions left blank. And everything B derives, from start to finish, is built on the same input as A — the same sentence, the same model, one round.
