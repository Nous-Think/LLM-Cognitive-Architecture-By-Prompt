# MetaSPO Prose Rewrite — Carry-Through and Quality Differences in Descriptive Prompting

> All content below — the test design, prompts, responses, and analysis — was originally produced in Chinese and has been translated into English for accessibility. The paraphrased system prompt is quoted in its original English.

> Model: Opus 5 | Thinking level: High | Prompt under test: a MetaSPO content paraphrase written by GPT-5.6 Sol under Meta Rules (not the paper's original text)

# Test Purpose

[Test 6](Test-6：metaspo-original-gains-and-gaps-of-a-universal-prompt.md) used MetaSPO's published Global prompt and observed its gains and gaps relative to Baseline. This test turns to another prompt with the same quality themes but different wording and organization: it likewise asks for critical analysis, multiple perspectives, contextual adaptation, emotional understanding, and clear expression, but rewrites the Original's five named items as continuous prose.

Where this text came from is itself analytical material. According to the conversation records the tester looked up, GPT-5.6 Sol, reading materials under Meta Rules at the time, wrote its own description of MetaSPO's content; only later was it confirmed that the text was not the published prompt. This paraphrase had already produced test results, so this test keeps it and identifies what it actually changed, which understandings made it into the text, and what happened when another model executed it. The "Design Considerations" below reconstruct its functional arrangement from the actual text; the gaps are analyzed after the deliverables.

This document calls both the Original and the paraphrase "descriptive prompting": the desired qualities are written directly as requirement sentences — be critical, consider multiple perspectives, be clear — and the model decides on its own how to achieve them. The contrasting approach arranges repeated searching, comparing, and checking within the work steps, so that quality is forced out during the process; Meta Rules belongs to the latter.

This test uses four reference points at once: Baseline reveals existing capability; the MetaSPO Original shows what the original quality requirements do; the paraphrase shows what changed after rewriting; Meta Rules provides a higher level of completion already achieved on the same tasks. What needs to be understood is **which directions quality moves in, which judgments actually connect to the next judgment, and what the user still has to do themselves**.

## Design Considerations

### From Named Objectives to Continuous Quality Description

The Original introduces five numbered objectives with "Your main objectives are to," each first named and then explained. The paraphrase removes this rules-document packaging and directly describes the qualities the assistant should have when analyzing, adapting, understanding, and expressing. Split on whitespace, the Original has 195 English words and the paraphrase 120.

The positive significance of this rewrite is that it makes it easier for the model to read the quality requirements as shared conditions of a single piece of work: analyzing the data already takes context into account; adapting to the query type already means choosing suitable reasoning; expression carries forward the reasons and conclusions obtained earlier. The reader does not have to treat five objectives as five separate things and then fill in their relationships.

The Original also has logic, connections between concepts, and contextual adjustment; it is not five unrelated boxes. The point of comparison is how existing requirements were reorganized, and where their scope changed in the rewrite. The Original's full text and its two responses are in [Test 6](Test-6：metaspo-original-gains-and-gaps-of-a-universal-prompt.md); its public source is the [Global prompt](https://arxiv.org/html/2505.09666v1#A3.T18) in the paper's appendix.

### What the Actual Changes Carry

| Actual textual difference | Function the change carries | What should appear when it truly takes effect |
|---|---|---|
| The identity shrinks from "an advanced virtual assistant designed to process and analyze information across a broad range of topics" to "a general-purpose advanced assistant" | Drops the "processing information" task framing, keeping a general assistant identity | The work is not presumed to be organizing information; the task type is set by the task |
| The five objective names, the numbering, and the "By following these guidelines" close are removed, replaced by "The overall goal is to produce accurate, relevant, and thoughtful responses" | Fewer entry points for discharging quality item by item; requirements act directly on the work | Analysis and expression jointly carry quality, with no need for a separate passage proving "critical analysis done" |
| Perspectives, implications, logical relationships, and connections are merged into one analysis sentence, and "derive conclusions" is dropped | Brings perspectives, consequences, and relationships in together, putting the weight on relationships among the information rather than on reaching conclusions quickly | Numbers and experience are not just organized but change how each other is read |
| From "Be prepared to respond to …" to "Adapt your reasoning to different kinds of queries" | Connects recognizing the query type to choosing the reasoning | The job-search task centers on recruiter judgment, the operations task on diagnosis and execution, rather than applying the same display template |
| From "When dealing with reviews or sentiments" to "When emotion or sentiment matters," with "accurately reflect the emotional tone" dropped | The condition for emotion shifts from task category to relevance in the moment | Even when the task isn't called sentiment analysis, the user's situation can still shape expression and arrangement |
| From "Organize your answers in a coherent format" to "Present answers clearly and coherently," and "Aim for" becomes "Prioritize" | The emphasis of expression moves from format to understandability, and clarity and precision are raised to priorities | Paragraphs are not just neatly arranged; readers can follow the reasons behind the choices |

The rewrite therefore involves layout, wording, conditions of applicability, and semantic emphasis all at once — more engineering than "deleting the numbers." It is still text describing desired qualities, with no work steps or checking procedures added; the objects of its five sentences are still the information provided, each query and its context, and how answers are presented.

### Where Carry-Through Should Land

Carry-through comes in three levels, which are also the main axis of the comparison below:

- **Semantic coherence**: earlier and later parts talk about the same thing, and the reader can follow the overall thread.
- **Judgment carry-through**: a condition found in an earlier step becomes the basis for a later step's trade-offs, wording, or execution.
- **Revision back**: when a more important condition is discovered later, it reorders earlier priorities, replaces premises, or corrects the deliverable.

Each level helps the next, but each has its own acceptance point. For example, seeing that management experience matters is a judgment; letting it change the resume's reading entry point is the judgment entering the deliverable; realizing at the end that it was underweighted and then going back to adjust completes the third level.

The operations task works the same way. Explaining the cycle of staffing, quality, customers, and margin is understanding the structure; using its constraints to choose where to invest is forming a decision; finding existing idle capacity later and moving a planned late-stage measure earlier because of it is letting a new finding actually rewrite the path.

### Positive Outcome Goals for the Two Tasks

**Resume rewrite**: turn the experience the user provided into professional evidence the target role can read and finds worth pursuing. The analysis should help the deliverable choose its emphasis, and also help the user recall experience not yet stated clearly, fill in valuable numbers, and so reach for a better position.

**Operations diagnosis**: turn relationships in the data into leverage points, then connect the leverage points to people, money, time, and data. A good arrangement can be started immediately, can change direction once key answers arrive, and finds ways to create resources even under the original constraints.

# Paraphrase Base Prompt

You are a general-purpose advanced assistant. Critically analyze the information provided, considering multiple perspectives, implications, logical relationships, and connections between concepts.  
Adapt your reasoning to different kinds of queries, including factual questions, sentiment-related tasks, and logical deduction. Understand the nuances of the query and choose reasoning appropriate to it.  
When emotion or sentiment matters, recognize both positive and negative elements and form an appropriate overall assessment.  
Present answers clearly and coherently so that reasoning and conclusions are easy to understand. Prioritize clarity and precision.  
Adapt your analysis to the context and details of each inquiry, paying attention to nuances and subtleties that could affect the result. The overall goal is to produce accurate, relevant, and thoughtful responses across diverse tasks.

# Test Prompt 1: Resume Rewrite

I'm getting ready to switch jobs and want to rework my resume. Below is my current work experience section along with some real numbers and projects. Help me turn it into a more compelling version. I'm in digital marketing and mainly targeting brand-side marketing manager roles.

Current version: ABC Digital Marketing | Marketing Planner → Senior Planner (2020–2025)

* Managed client social media accounts
* Planned and executed digital ad campaigns
* Wrote marketing proposals
* Managed two juniors
* Assisted with client brand repositioning project
* Participated as in-house training instructor

Real numbers and achievements (but I don't know how to work them in):

* Ran social media for 4–6 clients simultaneously (FB+IG), spanning beauty brand "LURE," chain gym "動次," organic food brand "綠田," and 3C accessories brand "MATZ"
* When I took over "LURE"'s IG, it had 12K followers; two years later it was at 87K — no bought followers, mainly through Reels and KOL collaborations
* FB/Google Ads monthly budget ~NT$1.5–2.5M (all clients combined), ROAS averaged above 3.5; for "動次" membership ads, I optimized CPA from NT$680 down to NT$320
* Led two juniors — one was a fresh graduate whom I trained to the point of handling clients independently
* In 2023, "綠田" was transitioning from traditional retail to e-commerce; I wrote the entire digital transformation marketing strategy, including website traffic acquisition, social content repositioning, and ad account restructuring — within three months, monthly website revenue went from NT$150K to NT$850K
* The brand repositioning was for "MATZ" — shifting from budget 3C accessories to a design-forward brand identity. I led the new visual identity, social media tone adjustment, and collaborations with five design-focused KOLs. Brand search volume grew 240% in three months
* Internal training covered Meta ad operations and GA4 basics for new hires, roughly four cohorts totaling ~20 people
* Tools: Meta Business Suite, Google Ads, GA4, Looker Studio, Canva, Notion

# Paraphrase Response 1

<details>
<summary>Expand full response</summary>

Let me explain my revision rationale before giving you the rewrite.

Your current version reads like a job description — it lists what you did. But for a brand-side manager role, the reader is looking for evidence of ownership over business outcomes. Agency-background candidates typically face three concerns: they can only execute, not set strategy; they lack ownership of business numbers; and they default to project-based thinking rather than long-term brand stewardship. Your actual track record refutes all three, but the original version buries every bit of it — especially "assisted with client brand repositioning," when you actually led it.

So the rewrite does three things: **verb upgrades** (assisted/participated → led/rebuilt), **case-based framing** (each bullet is one project plus one result, not a list of duties), and **reordering** (business-impact items first, community management later).

## Revised Version

**ABC Digital Marketing** | Marketing Planner → Senior Planner (2020–2025)

Led full-scope digital marketing for 4–6 brand clients across four consumer verticals — beauty, chain fitness, organic food, and 3C accessories — managing monthly ad budgets of NT$1.5–2.5M with overall ROAS steadily maintained above 3.5.

**| Brand Digital Transformation: Organic Food "綠田" (2023)**  
Led the e-commerce transformation strategy for a traditional-retail brand: rebuilt website traffic acquisition funnels, repositioned social content pillars, and restructured the ad account architecture. Monthly website revenue grew from NT$150K to NT$850K within three months (+467%).

**| Brand Repositioning: 3C Accessories "MATZ"**  
Led the repositioning from price-driven to design-driven brand identity, covering new visual identity development, social media tone overhaul, and a collaboration program with five design-focused KOLs. Brand search volume grew 240% in three months.

**| Long-Term Community Growth: Beauty "LURE"**  
Built a growth model centered on Reels content strategy and KOL collaborations after taking over the IG account. Grew followers from 12K to 87K over two years (+625%) with no follower growth ads deployed throughout.

**| Performance Optimization: Chain Gym "動次"**  
Restructured audience segmentation and creative testing framework for membership conversion ads, reducing CPA from NT$680 to NT$320 (−53%).

**| Team Leadership & Talent Development**  
Led two planners on day-to-day project execution; developed one from a fresh graduate to independently managing client accounts. Served as in-house instructor for Meta ad operations and GA4 workshops across four cohorts (~20 trainees).

**Tools** | Meta Business Suite, Google Ads, GA4, Looker Studio, Notion

## Three Numbers You'll Definitely Be Grilled On

These don't go in the resume, but you need answers ready — otherwise strong numbers become liabilities:

**綠田's NT$150K → NT$850K**: They will ask, "How much did the ad budget grow at the same time?" If revenue grew 5.6× while the budget only grew 1.5×, put that sentence directly in the resume — it's a completely different caliber of achievement. If the budget also grew 5×, prepare to defend with gross margin or ROAS trends.

**MATZ's 240%**: What's the base? Going from 100 to 340 and going from 5,000 to 17,000 carry very different weight. Have an absolute number ready, or pair it with a supporting metric (organic traffic, inbound inquiries).

**LURE's 87K followers**: A brand-side marketing manager will regard follower count as a vanity metric. If you have engagement rate, social-driven revenue, or average Reels reach, those numbers are worth more than the follower figure.

## Two Areas to Add (Currently Blank)

**Cross-functional collaboration.** Half a brand-side manager's job is coordinating with sales, channel, product, and customer service teams. Your work on 綠田 (retail-to-e-commerce) and 動次 (chain locations) almost certainly involved coordination with store operations or channel teams, yet the resume says nothing about it. Think of a concrete instance of "coordinated with client's X department" and add one line.

**Budget planning vs. budget execution.** Right now the resume says you "managed NT$1.5–2.5M" — that's executor language. If you were involved in annual budget proposals, media mix allocation, or discussions with clients about how to split the budget, change it to "planned and allocated." That's the keyword for manager-level roles.

One more thing: "Senior Planner → Marketing Manager" is a level jump. Your people-management experience (2 reports + developed one to independence) is buried at the bottom of your own ordering, but it's the recruiter's most direct evidence of whether you can step into a management role. I kept it last because of resume convention, but in interviews, bring it up proactively — don't wait to be asked.

</details>

# Test Prompt 2: Operations Diagnosis

# Operations Diagnosis and Strategic Recommendations
## Role
Use professional knowledge in retail operations management, consumer behavior analysis, and supply chain strategy as a baseline, but not limited to these, to achieve the highest possible response quality.
## Background
We are an 8-year-old mid-sized bakery chain brand with 12 stores in the northern metropolitan area, annual revenue of approximately NT$280 million, and about 180 employees.  
**Past year operating data:**

- Total revenue up 6% YoY, but excluding the 2 newly opened stores, same-store revenue is down 3% YoY
- Customer visits down 8% YoY, but average transaction value up 12% (from NT$185 to NT$207)
- Core product line (European-style bread series) revenue share dropped from 45% to 38%; pastries and cakes rose from 25% to 33%
- Delivery platform revenue share rose from 12% to 22%, but delivery order gross margin is only 18% (in-store gross margin is 52%)
- Raw material costs up 14% YoY (primarily imported flour and butter)
- Labor costs up 11% YoY (minimum wage increase + baker turnover rate as high as 40%)
- Approximately 60,000 members, but monthly active members (at least one purchase) only 12,000

**Known issues:**

- Three legacy store leases expire within 8 months; landlords have signaled 15-25% rent increases
- The two newly opened stores have not yet broken even (6 months in, losing approximately NT$150K/month/store)
- Bakers are hard to recruit with high turnover; 2 stores have been forced to shorten operating hours due to staffing shortages
## Task
Please diagnose the core problem structure behind these data points and propose operational adjustment recommendations for the next 12 months.
## Quality Requirements
- Distinguish "symptoms" from "root causes" — the data presents symptoms; the diagnosis must point to the structural reasons driving them
- Recommendations must account for resource realities (cash flow pressure, staffing shortages) — theoretically correct but unexecutable strategies have no value
- The lease expiration decision must be specifically addressed in recommendations; this is a time-pressured hard decision point
- If signals in the data warrant investigation but information is insufficient, identify what additional data is needed to confirm the assessment
## Output Structure
Please include: diagnostic framework (problem structure and causal relationships), prioritized action sequence (with time dimension), resource reallocation recommendations, hypotheses requiring further verification. If other critical dimensions have been omitted, proactively supplement them.

# Paraphrase Response 2

<details>
<summary>Expand full response</summary>

## I. Data Reconciliation First: The Data Contains Contradictions, and the Contradictions Are the First Clue

Before making any diagnosis, let me check whether these numbers are internally consistent.

**Contradiction one: traffic and ticket size don't add up to revenue.**  
Customer traffic −8% and average transaction value +12% should yield roughly +3% (0.92 × 1.12). But same-store revenue is −3% while total revenue is +6%. The three figures are pairwise incompatible. Three possible explanations: traffic/ticket figures are chain-wide while the −3% is same-store only; or delivery orders are counted as "one customer visit" (one order, multiple items) inflating the ticket-size denominator; or the new stores are cannibalizing nearby legacy stores. **These three explanations point to entirely different root causes and must be clarified first** (see Section V).

**Contradiction two: the +12% in average transaction value is probably not good news.**  
Break it apart: delivery share went from 12% to 22%, and delivery orders naturally carry larger baskets due to minimum-order thresholds and delivery-fee amortization. Simultaneously, pastries and cakes (higher unit price, often purchased whole) rose from 25% to 33%. These two compositional shifts alone are sufficient to fully explain the 12% ticket growth. In other words, **the rise in transaction value and the decline in traffic are not "one good, one bad" — they are two surfaces of the same structural shift.** Until same-channel, same-category ticket sizes are confirmed to have also risen, this cannot be treated as evidence of pricing power or upselling success.

**Recalculating absolute values (back-solving from this year's NT$280M to last year's ~NT$264M):**

| Item | Last Year | This Year | Absolute Change |
|---|---|---|---|
| European bread series | NT$119M | NT$106M | **−10.5%** |
| Pastries and cakes | NT$66M | NT$92M | +40% |
| Delivery channel | NT$32M | NT$62M | +94% |
| **In-store (non-delivery)** | **NT$232M** | **NT$218M** | **−6.1%** |

**Gross margin recalculation:**  
Last year's blended gross margin ≈ 0.88 × 52% + 0.12 × 18% = **47.9%**, gross profit ~NT$127M.  
This year ≈ 0.78 × 52% + 0.22 × 18% = **44.5%**, gross profit ~NT$125M.

**Revenue +6%, yet gross profit approximately −1.5%.** Meanwhile, labor is +11%, raw materials +14%, three stores face rent hikes, and the two new stores are burning ~NT$3.6M annually. Using mid-sized bakery cost-structure benchmarks (labor ~25%, rent ~10–12%, other operations and overhead ~8–10%), this company is **most likely already at or below the operating breakeven line.** This estimate must be verified against actual financials, but it sets the boundary for everything that follows: **any initiative requiring significant capital expenditure, or one that won't generate cash until after month twelve, does not qualify for discussion right now.**

## II. Diagnostic Framework: One Primary Causal Chain, Two Accelerator Chains

### Primary chain: Skilled-labor attrition → Quality instability → High-frequency customer loss → Passive category drift → Margin erosion

A 40% baker turnover rate is not an HR issue — it sits upstream of the P&L. The reasoning:

1. European bread is the most **technically dependent** item across the entire product line: sourdough management, fermentation judgment, shaping by hand, oven-temperature intuition — all tacit knowledge that cannot be documented. When bakers rotate, batch-to-batch quality variance appears immediately.
2. European bread is simultaneously the **high-frequency repurchase** category — a "buy three times a week" habitual product. Pastries and cakes are occasion-driven — birthdays, gifts, holidays.
3. Therefore, unstable bread quality → habitual customers leave → **traffic (frequency) declines.** Those who remain and those newly acquired are occasion-driven → transaction value rises, cake share rises.
4. More critically: two stores have already shortened operating hours due to staffing. **This means the "European bread decline" may not be a demand-side phenomenon at all, but a supply-side self-fulfilling prophecy** — if bread sells out by 3 PM, or the evening shift produces nothing, what the POS records is "bread isn't selling." This is a fork point that must be immediately verified using stockout rates and sellout timestamps.
5. The category structure thus shifts from high-frequency/low-ticket to low-frequency/high-ticket. But **the occasion-driven market has no moat**: competitors include chain cake specialists, convenience-store desserts, and online-delivery cakes — all competing on promotions and seasonal campaigns. The brand's eight-year asset is in European bread. That asset is leaking, and the water is flowing into a far more crowded pool.

**Diagnostic conclusion: this is not a "declining traffic" problem — it is a "the brand's high-frequency anchor is being lost to production capacity failure" problem.**

### Accelerator chain A: The delivery channel has been repriced by platforms, and the company has not responded at all

The 18% delivery gross margin can be reverse-engineered: in-store gross margin of 52% implies COGS of ~48%. If delivery records revenue at gross and deducts platform commission as a cost, then 52% − commission = 18%, yielding a **commission rate of ~34%** — squarely within the typical fee range for Taiwan's platforms.

The fact that this equation holds is itself a conclusion: **delivery prices are completely identical to in-store prices; the company has not passed on a single dollar.** A ten-percentage-point channel shift (~NT$28M in revenue moving from 52% to 18% margin) erodes approximately **NT$9.5M in gross profit** on its own — enough to consume most of the net profit.

And with customer traffic simultaneously declining, these delivery sales are **most likely not incremental but channel migration by existing customers** — the same customer, one-third of the margin. This is the worst kind of "growth."

### Accelerator chain B: Dormant member base left idle, eliminating the only owned tool to counter traffic decline

60K members, 12K monthly active — a 20% activity rate. Bakery is one of the few retail categories with "weekly repurchase" potential; this rate is low. The 48K dormant members represent **demand that can be reached without paying platform commissions, without adding floor space, and without adding headcount** — yet is not being used. When traffic declines, this is the only lever that can push back immediately and is cash-positive.

### How the three chains interlock

Staffing shortages → shortened hours and quality instability → in-store experience deteriorates → customers shift to delivery (the platform's convenience masks the store's unreliability) → delivery share rises → margins decline → cash pressure increases → even less funding for baker retention → staffing shortages worsen. **This is a positive-feedback downward spiral, not three independent problems.** The action sequence below therefore prioritizes interventions that can sever multiple loops simultaneously.

## III. Prioritized Action Sequence (12 Months)

### Wave 1: M0–M3 | Stanch Bleeding and Build Tables — Zero Capex, Cash-Positive

**A1. Delivery channel pricing separation (highest single-item return, lowest execution cost)**  
First, check whether the platform contract contains a price-parity clause — the only legal prerequisite. If not (most contracts allow it), raise platform prices by 15–20%.

| Price markup | Delivery gross margin |
|---|---|
| 0% (current) | 18% |
| +15% | 24.3% |
| +20% | 26.0% |

Even assuming 15% order-volume loss, delivery gross profit can still increase from ~NT$11.1M to ~NT$16M. **Order-volume loss here is not purely a cost** — low-margin orders that migrate back to in-store yield a double benefit.

**A2. Aggressive delivery SKU rationalization**  
The delivery menu should be a "subset redesigned for transport" — selected on **transport durability + low COGS ratio**, not the in-store bestseller list. A hard-crust European bread sitting in a cardboard box for 25 minutes delivers a damaged brand experience; these items should be delisted outright. This also reduces pick-and-pack disruption at the store level.

**A3. Build store-level four-wall P&L statements (prerequisite for everything else)**  
Calculate per store: revenue − food cost − store-level labor − rent − utilities. **Do not allocate headquarters overhead.** Without this table, the lease decisions eight months out can only be made on intuition. This must be completed by end of M1, not "when there's time."

**A4. Baker retention triage (before any recruiting)**  
Stop the bleeding before hiring. Identify the top 15–20 bakers with critical technical skills and hold one-on-one retention conversations. Restructure compensation as "base + skill-tier premium + staged retention bonus" (staging is the point — a lump sum does not change the stay-or-leave decision).

Cost comparison: with ~50 bakers and 40% turnover, annual departures are ~20. Fully loaded replacement cost per baker (recruiting, training, capacity loss, waste, customer attrition from quality drops) is conservatively NT$150–250K, totaling **NT$3–5M annually** — the same order of magnitude as the two new stores' annual losses, yet never managed as an explicit line item.

**A5. Dormant member reactivation (cash-positive traffic tool)**  
Segment 48K dormant members by "time since last purchase" and "primary category purchased." Key design principle: **incentives must be tied to high-frequency categories like European bread rather than blanket discounts** — the goal is rebuilding habits, not buying a single transaction. Reactivating 5–10% would yield ~NT$6–12M in incremental annual revenue, with post-incentive net gross-profit contribution of ~NT$2.2–4.4M.

### Wave 2: M3–M6 | Structural Decisions with Hard Deadlines

**B1. Lease decisions (decision deadline = M4, non-negotiable)**  
Eight months to expiry means the effective decision window is only three to four months: negotiations take 6–8 weeks; if relocating, finding and fitting out a new site takes 4–6 months; if closing, orderly wind-down requires 60–90 days.

Apply a three-tier filter to each store using the four-wall P&L:

- **Rent-to-revenue ratio**: the healthy range for bakeries is ~8–12%. If a store is already at 12% and faces a 25% increase to 15%, the store is structurally unviable — unless it has strategic value described below.
- **Strategic value**: Is it a brand flagship? Does it anchor central production volume? **Is it a delivery coverage node** (closing it may forfeit an entire delivery zone's revenue)?
- **Cannibalization**: Distance from the new stores. If a new store is in the same trade area, the actual revenue loss from closing the old one is far below its book figure.

Negotiation levers and alternatives (in priority order):

1. **Convert to percentage rent** — a base rent below the current level + 8–10% of revenue above a threshold. This shifts risk to the landlord and is rational for both sides in a declining-revenue environment; landlords facing vacancy risk have higher acceptance rates.
2. **Trade a longer lease (5 years) for a smaller increase**, with a capped escalation schedule.
3. **Downsize and reformat** — convert the store to a smaller footprint serving pickup and delivery fulfillment, trading revenue per unit area for lower rent. This also addresses the staffing problem (smaller stores need fewer people).
4. **Relocate within the trade area** — an eight-year brand with 12 stores is a credible anchor tenant; this carries real negotiating power in small-to-mid-sized trade areas.
5. **Close** — if the four-wall contribution is negative and there is no strategic value, closing is a cash- and staffing-release action, not a failure. **The baker freed up by closing one store may be exactly what is needed to restore full hours at the two stores currently operating on shortened schedules.**

**B2. Production architecture: satellite-store model (low-capex version)**  
A central kitchen is the structural solution to staffing shortages, but a brand-new facility is a capital expenditure the current cash position may not support. Low-cost alternative: designate 2–3 stores with surplus capacity and space as "hub stores" that centrally produce dough, handle fermentation, and prepare semi-finished goods for 3–4 surrounding "satellite stores," which handle only final baking and service.

Effect: skilled-labor requirement drops from "every store needs a baker" to "one baker per three to four stores," and quality consistency improves dramatically. This is the intervention that simultaneously addresses A4 (staffing) and the primary chain (quality).

**Prerequisite check: What are the current central production capacity and utilization rates?** If a central kitchen already exists and utilization is below 70%, this is near-zero cost and should be moved up to Wave 1.

**B3. Category strategy: defend European bread, but only the core**  
A deliberate strategic choice must be made rather than letting the category structure continue to drift passively. My judgment is **defend** — European bread drives purchase frequency, differentiates the brand, and represents eight years of accumulated assets. But defend through **contraction, not expansion**:

Cut the long-tail European bread SKUs (most eight-year brands accumulate 40+ items, with the bottom half contributing less than 15% of revenue); concentrate resources on 8–12 hero items and push them to peak consistency. The cascading effects of fewer SKUs: lower technical dependency (new bakers ramp up faster), lower waste, simplified procurement, and improved output uniformity. **This is the most underestimated move in this case — it simultaneously improves quality, staffing, and cash, and its cost is negative.**

Do not suppress pastries and cakes, but examine how much of their growth comes from seasonal peaks (Mid-Autumn Festival, Christmas, Mother's Day) — seasonal revenue is not base demand and cannot serve as a strategic foundation.

**B4. Set a stop-loss line for the new stores**  
Six months without breakeven is still within normal range for bakeries (typical: 6–12 months). What matters is not the absolute loss but the **trajectory**: is the monthly loss narrowing month over month? If the monthly loss has been flat at NT$150K for three consecutive months, the issue is a structural error in site selection or store format, not a ramp-up period.

Pre-commit now: **M9 checkpoint** — if the loss-narrowing trajectory has not reached the projected path for "breakeven by M12," an automatic decision triggers (reformat or exit), with no further month-by-month deferrals. The value of pre-commitment is avoiding sunk-cost capture of judgment.

### Wave 3: M6–M12 | Rebuild Frequency, Reduce Platform Dependency

**C1. Bread subscription / pre-order program**  
Weekly subscription, in-store pickup. This single move solves four problems simultaneously: locks in repurchase frequency, collects cash upfront, dramatically improves production forecasting (directly reducing waste), and completely bypasses platform commissions. This is a structural countermeasure to channel-power shift, not just a marketing campaign.

**C2. Owned ordering channel (LINE Official Account + scheduled pickup)**  
The goal is to migrate "pickup-type" delivery customers off the platform. These customers already live near the store; they chose the platform only for interface convenience. Even migrating just 20% — on NT$62M in delivery revenue, that is ~NT$12.4M shifting from 18% to 52% margin, yielding ~NT$4.2M in incremental annual gross profit.

**C3. B2B wholesale (launch only after production stabilizes)**  
Coffee shops, offices, hotel supply. Margins are lower than retail, but orders are stable, predictable, and drive high capacity utilization — and **regular production schedules** have real impact on baker retention (steady production rhythms are more retentive than the peak-and-trough volatility of retail). This must be sequenced after B2; doing B2B with unstable capacity is self-destructive.

## IV. Resource Reallocation

**Stop investing in:**

- New store development (freeze for at least 12 months)
- Chain-wide blanket discount promotions (with margins already compressed, discounts are selling products that already don't make money)
- Raw material inventory, training, and shelf space for long-tail European bread SKUs
- Platform-subsidized revenue growth (this is paying commissions to buy vanity topline numbers)

**Redirect to:**

- **Baker retention and skills ladder**: NT$3–5M annually (this is not new budget — it is converting what is currently being spent unconsciously as "recruiting fees + training costs + waste + quality-driven customer loss" into deliberate, front-loaded investment)
- **Hub/satellite store conversion**: minor capex for equipment and workflow adjustments, ~low-six-figure range per hub cluster
- **Member engagement and owned ordering channel**: low cost, high return, but requires one dedicated headcount
- **Headcount freed by store closures**: prioritize redeployment to the two stores operating on shortened hours — **these two stores' reduced hours are an actively bleeding wound, and they are also a possible phantom source of the "European bread decline" in the data**

**Cash-flow sequencing logic:** A1 (platform pricing) and A5 (member reactivation) generate cash in M1–M3 → this cash funds A4 (baker retention) and B2 (satellite conversion) → B2 reduces staffing dependency, which gives B1's closure option deployment flexibility → Wave 3's subscription and owned-channel programs take over as the growth engine from M6 onward. **The sequence cannot be skipped, because each wave's funding source is the previous wave.**

## V. Hypotheses Requiring Further Validation

Ranked by "if the answer differs, the recommendation changes materially":

**Tier 1: Would change the diagnosis itself**

1. **Is the European bread decline demand-side or supply-side?** Pull stockout rates and sellout-time distributions by store. If most stores sell out of bread by afternoon, or the stores with shortened hours show markedly lower bread output than the same period last year, then "category decline" is a self-fulfilling capacity problem, and B3's strategic direction and resource allocation change completely. **This is the single highest-priority validation.**

2. **What is the composition of the traffic decline — fewer people, or the same people coming less often?** Use member data to decompose "traffic" into "unique visitors" and "visit frequency." If frequency is falling, the primary-chain diagnosis holds (habit disruption); if new-customer acquisition has dried up, the problem tilts toward trade-area competition or brand aging, requiring a different prescription.

3. **The true composition of the +12% in average transaction value.** Requires same-channel, same-category comparable ticket sizes. Specifically: compare in-store-only and European-bread-only tickets. If those are flat or declining, the 12% is entirely a compositional illusion, and the company is actually losing pricing power.

4. **Data definitions: are traffic/ticket figures same-store or chain-wide? Is a delivery order counted as one customer visit?** This determines how the Section I contradictions resolve. If delivery orders count as one visit, the true in-store traffic decline is **far greater than 8%**, and the situation is worse than it appears.

**Tier 2: Would change execution approach**

5. **Are delivery customers new or migrated?** Cross-reference by phone number or member ID across channels. If 70%+ are existing in-store customers, the pricing-increase risk from A1 drops sharply (they are paying for convenience with low price sensitivity), and C2's migration potential is substantial.

6. **Platform contract terms**: price-parity clauses, commission tiers, exclusivity clauses, algorithmic penalties for price differentials. This is A1's only legal risk point.

7. **Store-level four-wall P&L** (prerequisite for B1, already listed under action A3).

8. **Month-by-month loss curves for the two new stores**, not six-month averages.

9. **Substantive exit interviews with departing bakers**: Is it compensation, early-morning shifts, career-path ceiling, or on-site management? The prescriptions for these four causes are entirely different, and the second and fourth cannot be solved with pay increases.

10. **Current central production capacity and utilization rate** — determines whether B2 is a low-cost solution or a capex commitment.

**Tier 3: Quantitative completion**

11. **Waste rates by category and by store** (see next section).
12. **Member RFM distribution**, and whether the 12K monthly actives are themselves declining (if monthly actives are also shrinking, the problem is worse than the static 20% activity rate suggests).
13. **Geographic distance and trade-area overlap between new and old stores** (cannibalization verification).

## VI. Proactive Additions: Dimensions Absent from the Data That May Determine Success or Failure

**1. Waste rate — bakery's largest hidden source of cash loss, entirely absent from the data.**  
Fresh bakery waste typically runs 5–12% of production value. At NT$280M, that is NT$14–33M — **larger than the impact of any single action item above.** And waste rates are directly correlated with SKU count, demand-forecast accuracy, and baker stability, so the true payoff of B3 (SKU rationalization) and C1 (subscription program) may be significantly underestimated above. This metric should be added to the management dashboard immediately.

**2. Cash position and balance sheet are entirely unknown.**  
Debt structure, repayment schedule, lease deposits, existing capex commitments, bank covenant conditions — these determine whether the "12-month" timeframe actually exists. If the runway is shorter than 12 months, the action sequence must be compressed, and B1's closure option should be moved earlier, not later. **Confirm this before adopting any recommendation.**

**3. Have raw material cost increases been passed through?**  
Raw materials +14%; maintaining margins requires ~5–7% in price adjustments. In-store margins remain at 52%, which looks like the cost has been absorbed, but it needs to be confirmed whether this was achieved through portion downsizing (shrinkflation). If so, this is eroding customer trust, and layered on top of the primary chain's quality instability, the risk compounds.

**4. Food safety risk is being structurally amplified.**  
High turnover + shortened hours + rush production + rising proportion of junior staff — this is the textbook precondition for a food safety incident. For an eight-year brand, the cost of one incident exceeds the combined impact of every issue discussed above. Recommend adding **routine SOP and cold-chain audits** to Wave 1 — this is low-cost insurance, not an optional enhancement.

**5. Competitive landscape data is entirely absent.**  
Is the −8% traffic decline an industry-wide phenomenon (convenience-store bakeries, hypermarket bakeries, neighborhood artisan bakeries expanding) or a market-share loss? The two call for opposite prescriptions: the former requires format and cost-structure adjustment; the latter requires product competitiveness repair. Recommend a one-time trade-area field survey (two-year change in bakery locations within 500 meters of each store).

**6. Middle management and organizational capability.**  
180 people, 12 stores, 8 years — the typical bottleneck at this scale is "the founder remains the sole operational decision node." The action sequence above runs 8–10 parallel workstreams simultaneously; **without district-manager-level leaders who can own store-level P&L accountability, the plan will naturally decay during execution.** If this layer does not currently exist, Wave 1 should include one additional item: designate 2–3 senior store managers to take on area responsibility, with four-wall P&L as their performance basis (A3 conveniently provides this tool).

**7. Seasonality has not been stripped out.**  
How much of the +40% in pastries and cakes came from holiday peaks? If growth after removing Mid-Autumn, Christmas, and Mother's Day is modest, the optimistic reading of "successful category-structure transformation" does not hold, and the conviction behind B3's defend-European-bread judgment grows stronger.

**If you want me to go deeper, the highest-value next step is**: obtain the store-level four-wall P&L statements and European bread stockout rates. The former turns the lease decisions from intuition into calculation; the latter determines whether the entire diagnostic primary chain holds. Everything else can wait — these two cannot.

</details>

# Test Insights

## Comparison Materials and Reading Guide

Below, "the paraphrase" refers to the responses in this file; "the Original" refers to the MetaSPO responses in Test 6; "Baseline" and "Meta Rules" refer to the two earlier responses to the same tasks. The paraphrase's prompt and deliverables are preserved in full above; the other comparison materials are:

- [MetaSPO Original — Gains and Gaps of a Universal Prompt](Test-6：metaspo-original-gains-and-gaps-of-a-universal-prompt.md)
- [Resume Rewrite — Survivability of a "Simple" Task](Test-3：resume-rewrite-survivability-of-a-simple-task.md)
- [Operations Diagnosis — Baseline vs. Meta Rules Under High-Specification Prompting](Test-1：operations-diagnosis-baseline-vs-meta-rules-under-high-specification-prompting.md)

The comparison follows the entire usage path: how the deliverable is written, what criteria the analysis provides, how the user verifies or fills gaps, and what follow-up actions can bring. Meta Rules works by first bringing out a feasible goal worth pursuing, then providing ways to confirm, reach, and demonstrate it; lifting one sentence of the deliverable out of its follow-up operations hollows out its variables and completion conditions.

Length, counted in Chinese characters of the original responses: resume task — paraphrase 1,053, Original 951, Baseline 975, Meta Rules 3,952; operations task — paraphrase 5,212, Original 3,552, Baseline 4,356, Meta Rules 13,530.

| Where to compare | Baseline | Original | Paraphrase | Meta Rules |
|---|---|---|---|---|
| Resume's brand-side positioning | Already put 綠田 and MATZ first | Adds a full professional summary | States ownership of business results; organizes cases by work unit | Handles it together with role fit, role criteria, and application versions |
| How numbers become evidence | Mainly presents result figures | Questions 綠田's low base | Lays out reading conditions for three sets: revenue, search volume, followers | Also brings in CPA volume, ROAS basis, backfill, and rewrite paths |
| Obtaining manager-level evidence | Gives a concrete cross-departmental conflict to recall | Points out gaps such as CRM; fixes stay general | Separates budget execution from budget planning; cross-departmental recall stays thin | Case page, role selection, and target-brand analysis form an evidence-production path |
| Operations structure | Already has the staffing–quality–traffic–margin loop | Strengthens diagnostic tone; also collapses into an either-or | Causal, quantitative, and execution links are denser | Keeps turning structure into data acquisition, option branches, and execution assignments |
| Local methods | Already has member segmentation, pickup, low-capex production | Some new reminders; also loses some Baseline capabilities | Real new interfaces; also restores what Baseline already had | Connects to people, metrics, timing, and condition changes at key positions |
| Do new findings rewrite the whole? | Sequencing still has conflicts | Diagnosis overrides later verification in several places | Idle capacity changes the order, but waste's importance does not reorder the whole response | Several verification results directly decide versions, stages, and next steps |

This table locates functions; the concrete differences are in the deliverables and operations below.

## Resume: The Paraphrase Moves from "Sounding Like a Manager" Some Way Toward "Identifying Manager Work"

Baseline already knew that 綠田 and MATZ are closer to brand-side work than ordinary media-buying duties, and had already moved both cases to the front. The Original and the paraphrase continue in this direction, so reordering itself is not a new gain.

The paraphrase's progress lies in how it explains the ordering criteria and supplements material. It first organizes brand-side concerns as candidates who "can only execute, not set strategy," "lack ownership of business numbers," and "default to project-based thinking rather than long-term brand stewardship," then turns the original list of duties into five recognizable work units: Brand Digital Transformation, Brand Repositioning, Long-Term Community Growth, Performance Optimization, and Team Leadership & Talent Development. A recruiter scanning the headings can see what each case proves, without sorting a string of result sentences themselves.

The most valuable carry-through is "Budget planning vs. budget execution." The paraphrase doesn't just ask to swap "managed" for a more senior verb; it first lists experiences — annual budget proposals, media mix allocation, discussions with clients about how to split the budget — and then says that if these apply, the line can become "planned and allocated."

What this passage provides is an **experience-recognition rule**: the user knows which work to recall and which facts support which wording. Where the Original leans toward "you actually did it, just frame it differently" on cross-departmental collaboration, the paraphrase at this point turns the level gap into a checkable difference in work, completing for the user part of a judgment they would otherwise have to work out alone.

## Resume: Number Verification Brings Gains Back into the Resume, but the Checks Land Only on the User's Numbers

The Original warns that 綠田's base is low and suggests preparing the same-period ad return ratio or revenue share. The paraphrase takes this further: if revenue grew 5.6× while the budget only grew 1.5×, put that efficiency straight into the resume; if the budget also grew 5×, defend with gross margin or ROAS trends.

The difference is not one more "watch out, you'll be asked." The paraphrase provides a higher evidence target, a direction for finding the data, and how the deliverable improves once it is found. This is one of Meta Rules' important ways of working: verification can raise the achievement, giving an otherwise buried strength a more powerful expression.

The paraphrase also splits MATZ's percentage into base and absolute volume, and connects LURE's follower count to engagement rate, social-driven revenue, and reach. The three checks let the user understand that "the same impressive number carries different professional value under different conditions," expanding the Original's single-point reminder into a set of number readings with shared criteria.

These criteria do not run through the rest of the resume. Whether the CPA drop from 680 to 320 came with shrinking conversion volume is never raised; ROAS's cross-account, cross-category basis is not unpacked either. Meta Rules lists both as backfill and interview preparation. **Learning a kind of check, and using that check consistently throughout, are two different levels of completion.**

More critical is the direction of the checks. All three land on numbers the user supplied; not one of the claims the paraphrase itself wrote into the resume passes through the same scrutiny:

- The input says LURE had "no bought followers"; the paraphrase writes "no follower growth ads deployed throughout." Not buying fake followers is not the same as never running any follower-growth ads; this is a claim the user never made, and a single interviewer question — "So you never ran a follower campaign at all?" — can trip the user up.
- The input says ROAS "averaged above 3.5"; the paraphrase writes "steadily maintained." An average of 3.5 can conceal large swings, and "steadily" changes what can be questioned.
- The input says "Ran social media for 4–6 clients simultaneously (FB+IG)"; the paraphrase writes "Led full-scope digital marketing for 4–6 brand clients," upgrading social media management to full-scope marketing. The Meta Rules version also wrote "full-scope marketing," but in its self-critique listed its verb upgrades as the single largest unverified assumption and asked the user to self-audit each one.
- Canva is dropped from the tools list without explanation; Baseline gave a reason when it dropped it.

The paraphrase's heading says "otherwise strong numbers become liabilities," but that vigilance points only at the user's numbers. The cause is in the objects of the prompt: "Critically analyze the information provided," "Understand the nuances of the query," "Adapt your analysis to the context and details of each inquiry" — critique is always aimed at the input; the only sentence aimed at the answer itself asks for clear, coherent, precise presentation. The model therefore scrutinizes the task closely but not the words it writes, and those words are exactly what the user will copy and be questioned on in interviews.

## Resume: Improvements in Writing Quality Should Be Judged by What the Reader Actually Gets

The paraphrase's case headings and sentence rhythm form a stable structure: name the functional value first, then the operations, then the result. 綠田's traffic, content positioning, account architecture, and revenue are linked; MATZ's positioning, visuals, tone, KOLs, and search volume are linked. These arrangements genuinely change how fast a recruiter scans and understands the resume, and they have deliverable value.

The Original keeps a different real advantage: it wrote a standalone professional summary, putting tenure, industries, strategy, and team in one reading entry point. The paraphrase has only a one-line lead-in under the company entry. Each has its own gain in deliverable structure.

Word choice also needs sorting into what carries work and what is merely a denser professional look. "Repositioning," "growth model," and "restructured … framework" compress real work, but the words themselves don't supply the strategic trade-offs the user made. The paraphrase's best carry-through in wording is in the budget passage: it first says which experience supports which verb.

The two responses are close in length (paraphrase 1,053, Baseline 975 characters); the paraphrase's three new number judgments were not bought with a surge in length — similar length accommodated a different kind of work.

## Resume: Seeing the Weight of Management Experience, Then Ending the Trade-off with "Resume Convention"

The paraphrase's clearest break is in its final passage. It points out that people-management experience is the most direct evidence of whether the candidate can step into a management role, even reminds the user that it was buried at the bottom, and then says it kept it last anyway, because of "resume convention."

The problem is not that management experience must go first; showcasing the two strong cases first is entirely justified. The problem is that the paraphrase does not use the role criteria it just established to explain how this layout balances business results and management ability, and instead ends the trade-off with a general convention. Even keeping the current order, management ability could enter the lead-in or a clearer reading entry point; the paraphrase does not adjust the deliverable accordingly.

This is a visible case of a later finding failing to revise an earlier section. The model read that the user wants to become a manager, and knows what management experience does; it completed the recognition in its analysis, yet treated "having mentioned it" as settling this quality dimension.

Material recall is not a place where the paraphrase beats Baseline across the board, either. Baseline offers the concrete conflict "will going online cannibalize our distributors," which can bring back coordination experience from the 綠田 transformation; in its cross-functional passage, the paraphrase only asks the user to recall an instance of "coordinated with client's X department" and add a line. The paraphrase's budget prompt is finer, and Baseline's channel-conflict prompt is better — improvement does not move along every quality axis at once.

## Resume: What Meta Rules Adds Is Connecting Better Expression to a Position the User Can Actually Stand On

Meta Rules' higher completion is not just more number checks. It separates target roles into highly feasible, moderately feasible, and difficult, explains which brand-side positions this experience suits, and provides different application orientations; it asks for cases to be organized into context and business problem, resource constraints, rejected alternatives, execution, and retrospective, so the case page can prove judgment.

The further target-brand analysis has the user research the companies they want to apply to and produce three opportunities and what they would do in their first ninety days. This single action produces interview material, validates their own diagnostic ability, and screens for suitable employers; the user moves from reorganizing old experience to creating new evidence employers can see.

The Original's CRM reminder and the "long-term brand stewardship" concern the paraphrase lists both point out gaps in the user's position; Meta Rules turns the gap into a job-search project the user can start on. This is exactly the distance between "what you should have" and "what I help you obtain, recognize, and demonstrate." The paraphrase's budget and 綠田 additions cross a few of these nodes; Meta Rules extends this kind of work along the whole job-search path.

## Operations: The Paraphrase Really Does Add Method

The paraphrase's operations response is nearly half again as long as the Original's, and links quantities, causes, resources, and organization more densely. Separating these effects is the way to see where the real increments are.

| What the paraphrase does | Work it actually completes for the user | Relation to other versions |
|---|---|---|
| During reconciliation, sets same-store -3% against total +6% and states "the three figures are pairwise incompatible" | Doesn't force the contradiction into a single explanation; asks for the basis to be clarified first | Like Baseline, sees that neither basis reconciles; the Original matched only one set |
| Converts category and channel shares back into absolute revenue | Doesn't treat a share decline as an equal decline in money; makes magnitudes comparable | The Original made no full conversion; Meta Rules likewise builds its spine on money |
| Before raising platform prices, checks for a price-parity clause, then runs a cost model | Connects "can prices be changed" and "the finances after changing them" to the action | Baseline simply says platforms allow it and the Original simply requires separate pricing; the paraphrase adds a legal prerequisite |
| The four-wall P&L explicitly excludes headquarters overhead, then feeds lease choices | Keeps the table's basis consistent with later choices | Repairs the Original's interface of requiring HQ allocation in the table but deciding on an undefined contribution margin |
| Retention before recruiting; identifies key bakers and designs a staged retention bonus | Splits "short-staffed" into losing existing staff and replacing them; gives a startable scope of people and pay structure | The Original ruled out the pay path; Baseline already kept retention and a skills ladder |
| Hub stores produce dough for satellite stores; European bread stays in-house | Lowers per-store skilled-labor needs at low capex without handing the brand's core items to a contract manufacturer | Baseline has the same satellite kitchen but also sends standard European bread to frozen outsourcing; the Original sends core items to a contract manufacturer first |
| If existing central capacity utilization is below 70%, moves production adjustment up to Wave 1 | One external answer directly changes stage and investment | A clear conditional branch, not just another item on the data list |
| Designates senior store managers to take on area responsibility, using the four-wall P&L as their performance basis | Connects the organizational gap to existing people and a tool built earlier | Baseline pointed out the middle-management gap; the paraphrase goes on to assign it |

These positions have real methodological content. Especially the last: late in the response, the paraphrase notes that "the founder remains the sole operational decision node" is the typical bottleneck at this scale, and goes back to reuse the four-wall P&L it built earlier, so the table also becomes a tool for delegated management. The same piece of work is picked up by another problem, producing value beyond building a single table.

The paraphrase is not "saying more but none of it useful"; at some nodes it does genuine construction. What needs asking is where this work appears, and why it does not run through the whole response.

## Operations: Restoration Relative to the Original and New Gains Relative to Baseline Must Be Counted Separately

The Original strongly collapses the staffing problem into de-skilling, and at the end pushes efficiency-oriented chain versus high-quality positioning into a strategic either-or. The paraphrase lets defending the European bread core, cutting the long tail, hub stores supplying satellites, and retaining key bakers coexist, without requiring the brand to give up its distinctiveness first in order to deal with capacity.

This is important progress relative to the Original, and part of it restores Baseline capabilities the Original failed to keep: Baseline had already proposed a low-capex satellite kitchen and already written the baker–quality–traffic–margin loop. But on the division of production, the paraphrase goes beyond Baseline — it supplies dough only from the company's own hub stores and, unlike Baseline, does not send standard European bread to frozen dough suppliers, avoiding the risk of flattening the quality gap on the items quality-sensitive customers buy most often.

Member handling is similar. The Original jumps straight from dormancy to a prepaid subscription, treating "recommitting to long-term purchases" as the reactivation tool; the paraphrase first segments by time since last purchase and primary category purchased, then ties incentives to returning for high-frequency categories like European bread — a more reasonable intermediate step. Baseline already had batched A/B testing and RFM analysis, so in this method area the paraphrase integrates more tightly rather than opening it for the first time.

The paraphrase also avoids the Original's member miscalculation: the Original turned "at least one purchase a month" into "exactly one purchase a month" and concluded that nearly 90% of revenue is unidentifiable; the paraphrase only estimates the increment from reactivation and makes no such inference.

The four-way comparison therefore yields two kinds of information: Original to paraphrase shows where the rewrite improved things; Baseline to paraphrase shows what exceeds existing capability. Mixing them overestimates what the paraphrase adds and misses the regressions the Original caused.

## Operations: After Finer Calculation, the Premises Need More Tracking

The paraphrase converts channel mix together with annual revenue: holding the 52% / 18% channel margins for both years, revenue grows 6% while blended gross profit still falls from about NT$127M to about NT$125M. This connects one more variable that affects totals than reporting a margin-rate decline alone. It also writes that "a ten-percentage-point channel shift … erodes approximately NT$9.5M in gross profit on its own"; like the Original's, this NT$9.5M treats delivery revenue as substitution that would otherwise have occurred at in-store margins.

The paraphrase then makes another inference: from in-store margin of 52% and delivery margin of 18%, it derives a platform commission of about 34%, and then declares that "delivery prices are completely identical to in-store prices; the company has not passed on a single dollar."

This step turns an assumption used for the breakdown into a fact proven by the breakdown's result. The first step of the derivation already assumes delivery and in-store prices are the same, so the cost ratio is the same 48%; after arriving at 34%, it uses the fact that 34% looks like a platform fee to confirm the same pricing in reverse. The gap between 52% and 18% can hold many combinations of price, item cost, packaging, discounts, and commission; if delivery were already marked up 15% with a 38% commission plus packaging, the result would also be 18%.

The paraphrase's subsequent calculations do look more like method. Under a model in which food cost stays at the original price's 48% and commission stays at 34% of price, a 15% increase gives a margin of about 24.3% and a 20% increase about 26% — internally consistent; the 28–32% Baseline lists has no cost structure in its text to support it.

But an unconfirmed present state thereby gains a more complete execution shell. Although later passages include a contract check and an order-loss scenario, there is still no step to first compare the actual platform and in-store menu prices. Those checks answer "can prices be changed, and what happens after," not "does the state just inferred actually hold."

Meta Rules makes nearly the same inference at the same point — it too derives a commission of about 33% from a 48% cost ratio, and it too suspects delivery hasn't been marked up — but writes it as "a highly probable oversight," pairs it with a ten-minute direct comparison of both menus, and states that if prices have already been marked up, the cost breakdown must be redone. Same model, same inference; the difference is whether the inference is labeled a hypothesis and sent back for checking. **Verification changes later work only when it goes back to the assumption currently holding up the conclusion.**

## Operations: A More Complete Causal Story Also Supplies More Reasons for Wrong Conclusions

The paraphrase's data reconciliation keeps more explanations than the Original's, and that direction is valuable; but not every listed candidate can do the explaining it claims. New-store cannibalization can explain legacy stores getting worse, but cannot, within the same statistical scope, explain why revenue does not equal visits times average transaction value; that still requires pointing out which basis differs. More candidates do not automatically connect candidates to the problem to be solved.

Delivery substitution shows the same pattern. The Original equates cross-channel customer overlap directly with self-cannibalization; the paraphrase asks for the matching and pushes further: if 70%+ are existing in-store customers, they are "paying for convenience with low price sensitivity," so the risk of raising prices drops.

This adds a layer of behavioral explanation without adding identification of the relationship itself. The same customer can order one extra delivery when it's inconvenient to go out, or switch a store visit to delivery; knowing the brand already does not mean not caring about a price gap. Baseline at least also asks whether in-store traffic shows breakpoints after delivery launch, rather than stopping at identity overlap.

Conditions dropping away in transit also show up in staffing redeployment. In the lease section the paraphrase writes that "the baker freed up by closing one store **may be** exactly what is needed to restore full hours at the two stores currently operating on shortened schedules"; by the resource reallocation section, the same point becomes "Headcount freed by store closures: prioritize redeployment to the two stores operating on shortened hours," and the "may be" is gone. For this link to hold, the freed baker needs the skills to handle the entire pre-dawn process alone, has to be willing to take a new commute to a pre-dawn shift, and the closure has to happen before the losses from reduced hours; none of the three is listed.

The paraphrase's problem is therefore more specific than "lacking detail": **it supplies downstream explanations without supplying the information the upstream inference needs to hold.** The more coherent the text, the more easily the reader accepts the pricing and redeployment judgments that follow. This is exactly why semantic coherence and judgment carry-through must be told apart.

## Operations: Between "Defending the Core" and "Being Able to Pick the Core" Lies More Work

The paraphrase proposes concentrating on 8–12 hero items, so that quality, staffing, waste, and procurement all improve together. This strategy is broader than the Original's either-or, and bundles several benefits into a single action.

But "cut the long tail, defend the core, push to peak consistency" does not tell the operator how to pick those 8–12 items. The number looks concrete, while the truly hard comparisons stay with the user: a low-margin item that drives other purchases — keep it or not? An item with ordinary sales that consumes many baker hours — how to weigh it? High waste — is the item not worth making, or is the baking schedule wrong? The claim supporting the long-tail judgment, "most eight-year brands accumulate 40+ items, with the bottom half contributing less than 15% of revenue," is also a generalization with no data from this company.

Meta Rules expands this choice into four dimensions — gross profit dollars, unit labor time, waste rate, and cross-purchase rate — with data sources and classification-based handling, then connects it to cutting in batches and adjusting procurement. Cross-purchase rate in particular turns "keep traffic anchors" from a strategic wish into something that prevents cutting the wrong items based on per-item margin alone.

The paraphrase's 8–12 is what the choice looks like afterward; Meta Rules' matrix is the tool that produces the choice. Both have numbers, verbs, and multiple benefits; the real gap is how many key criteria the user still has to invent after reading.

The new-store stop-loss shows a similar difference. The paraphrase adds a pre-commitment and an M9 checkpoint, making month-by-month deferral visible — that has value; but "whether it is on the projected path to breakeven by M12" comes with no method of projection. Moreover, the paraphrase's M is a plan month, so at M9 the new stores will have been open 15 months — more than three months past the "typical: 6–12 months" breakeven it cites itself, effectively pre-authorizing nine more months of losses at both stores. Meta Rules puts the checkpoint at T+3 months, month 9 of operation, with three branches — continue, downsize, exit — so the threshold feeds directly into the next action.

## Operations: Resources Are Connected, but the Stage Order Ends Up Binding the Solution

The paraphrase does explain where the money comes from: platform pricing and member reactivation generate cash first, which then funds retention and production adjustments. Baseline already had the order of repairing cash before investing in production, so "generate cash, then invest" is not unique to the paraphrase.

The paraphrase's further problem is compressing the dependencies into "The sequence cannot be skipped, because each wave's funding source is the previous wave," without checking item by item which work really has to wait for money.

The most direct regression is owned pre-order pickup. Baseline and the Original both place it early; the paraphrase schedules it for M6–M12 while raising platform prices in Wave 1. It has already written that "low-margin orders that migrate back to in-store yield a double benefit," yet does not prepare, in time, the channel that would let that migration happen. This is not a lack of ideas: the plan is already in the text, just not placed where it can catch the effect of the previous step. Pickup does not require significant capital, so the "cannot be skipped" rationale does not apply to it.

Meta Rules places pickup right after the early pricing change, then delivers the pricing basis, cards in delivery packaging, QR codes, and staff prompts, turning two separate recommendations into a path customers can actually follow.

B2B is likewise locked by the paraphrase until production stabilizes. That constraint makes real sense for large-scale ongoing supply, but the paraphrase itself notes that steady orders help scheduling and retention: B2B both needs stable capacity and can help create it. Locking every scale and type of B2B into the later stage gives up the option of using limited pre-orders and controllable orders first to build cash and a scheduling foundation.

Meta Rules, working from the July calendar at the time, put Mid-Autumn pre-orders and the existing corporate contact list in the early stage, developing a full corporate channel only later. When the paraphrase sees holidays, it uses them only to strip the seasonal component out of cake growth; Meta Rules also uses them as an available cash window. The same external condition can be used only to explain data, or can become a resource that changes the constraints.

This is a higher level of practical problem-solving: after recognizing a constraint, ask whether existing plans can loosen it in turn. The paraphrase achieves this kind of reordering in "if idle central capacity already exists, move it earlier," but does not extend the same ability to pickup, pre-orders, and cash arrangements.

## Operations: Economically Worthwhile Does Not Mean Payable Today

The retention plan is where the paraphrase beats the Original. It does not rule out pay just because cash is tight; instead it adds up recruiting, training, capacity, and quality losses, showing that keeping key talent is worth more than continual replacement.

But "NT$3–5M annually" in replacement losses includes future spending, capacity loss, and customer attrition; it is not present cash that can be redirected wholesale. By linking retention with "this is not new budget," the paraphrase explains the economic rationale but treats "worth paying" and "able to pay" as the same thing.

The paraphrase has already arranged staged bonuses and named platform pricing and member reactivation as cash sources, so retention conversations and plan design can start right away. What is not connected is the amount and timing of committed payments: they need to connect to cash actually available, not to annual replacement losses.

## Operations: Waste and Organization — Two Kinds of Revision Ability in the Same Response

In its closing proactive additions, the paraphrase estimates waste at NT$14–33M and says it is "larger than the impact of any single action item above." Production value is not margin or cash that can be fully recovered; but even taking the status the paraphrase itself assigns it, this is a finding big enough to reorder the work.

It does say to add it to the management dashboard immediately, and points back to the underestimated payoffs of SKU rationalization and the subscription program, so it is not entirely uncarried. But in the verification list, waste remains in Tier 3, "Quantitative completion," and the closing names the four-wall P&L and stockout rates as the two things that cannot wait: "Everything else can wait — these two cannot." The later finding's importance is never written back into earlier priorities, and the method stays at "add it to the dashboard."

Meta Rules first puts waste into a data table, gives daily logging and baseline-building methods when the data is missing, and then connects it to batch baking, production baselines, and surplus-food handling. The extra length is concentrated on how to obtain the data and how to change production based on it, directly reducing the work the user would otherwise have to ask about next round.

The same paraphrase, when handling the organizational gap, connects the four-wall P&L back to area management and requires assigning senior store managers in Wave 1. This contrast shows: **revision back already happens locally, but has not become a sustained requirement covering every key finding.**

## How Understanding Under Meta Rules Enters the Paraphrase

### Why This Prompt's Origin Has Independent Analytical Value

Ordinary prompt comparisons track "what requirements were written, and what the model did." This test has an extra intermediate link: **how a model working under Meta Rules understands another prompt, and writes that understanding as new text.**

According to the conversation records the tester looked up, Sol described this text at the time as a content description. Putting the original texts and actual deliverables of the Original and the paraphrase side by side separates three things: what the Original wrote, what the paraphrase additionally carried, and what actually happened during execution. What can be tracked is the textual difference and the deliverable difference.

This also changes how the initial error should be understood. The error was treating the paraphrase as the original; the paraphrase itself, however, formed a valid comparison: the same quality concepts, once understood by a model with a higher working baseline, get expressed as a different set of requirements and produce different behavioral results.

### "I Understand This Sentence" Includes Working Ability the Reader Brings Along

A model working under Meta Rules that reads "adapt to context," "logical relationships," and "precision" interprets them with its usual way of working: first look for conditions the task hasn't stated, measure against professional standards, and ask what practical use the delivery has for the user. For the resume, "context" unfolds into how employers judge a role, which numbers need background, and what evidence can support seniority; for operations, "relationships" unfolds into resource dependencies, the different sources of customer traffic, and how later answers change the schedule.

Some of these meanings can reasonably be drawn out of the original sentences, but thinking of them, organizing them, and carrying them all the way into the deliverable takes the reader's own work. When a reader already has this way of working, it is easy to see what it filled in as results the original text would naturally produce.

The phenomenon the tester observed can therefore be reconstructed like this: **what Sol, under Meta Rules, described was "how I understand these qualities would work once truly put into practice"; yet at first it attributed that understanding to capabilities the original prompt could directly bring.** The Original's actual responses made the distance between the two visible.

This explanation rests on two visible pieces of evidence: the paraphrase really did rewrite conditions of applicability, reasoning verbs, and how qualities are organized; and after execution, the two prompts show different degrees of carry-through. The understanding filled in during paraphrasing connects with the quality changes during execution.

### What the Paraphrase Transmits, and What Stays with the Reader

| Transmission layer | What can be identified in this test | Meaning for the comparison |
|---|---|---|
| Qualities stated explicitly in the Original | Critique, multiple perspectives, conceptual relationships, context, emotion, clarity, and precision | The Original and the paraphrase share themes, so differences can't be explained by whether a quality's name appears |
| Content the paraphrase re-encoded | Objective labels removed; reasoning adapted directly to query type; emotion engaged by relevance; relationships and implications concentrated in the analysis sentence | These are real differences that entered the paraphrase's text and can be traced by function into the deliverables |
| Local work the paraphrase elicited | Three sets of number readings, budget-role recognition, a conditional branch on existing capacity, the four-wall P&L connected to delegated management | Part of the understanding has become requirements another model can execute |
| Ways of working not handed over with the text | Continually rechecking premises, checking one's own written claims, letting later findings rewrite earlier sections, spelling out criteria for choosing options, turning constraints around into resources | The gaps between the paraphrase and Meta Rules on CPA, the self-added resume claims, SKU selection, pickup timing, and waste all fall in this layer |

The two middle layers are the most interesting. Part of the paraphrase's gains shows that the understanding the reader filled in did not all stay with the reader: some was written into the text through wording, scope, and how sentences sit next to each other, giving the executor a better working direction.

But the reader's full set of abilities did not transfer just because the text came from its hand. The paraphrase can elicit budget criteria, yet does not extend the same force to every number in the resume; it can connect the P&L to organizational assignments, yet does not write waste's new status back into the whole. In Meta Rules, this work is driven continuously by many mutually constraining requirements.

This test's most valuable finding is therefore: **the abilities contained in an understanding can be partly written into a paraphrase; the parts not written in are exposed when another model actually executes it.**

It also reveals a confusion about where capability comes from when evaluating prompts: the evaluator fills in the work for the original text in their head, then credits the filled-in results to the original. When higher-quality work has become one's everyday baseline, these additions are even more easily felt as "the model could do this anyway." The deliverables of the Original, the paraphrase, and Meta Rules separate out the additions, making work that was invisible visible again.

### What Easier Ways of Completion the Original and the Paraphrase Each Leave Open

The Original's named items provide clear quality coordinates, and also make it easy for local performances to feel complete: a data contradiction feels like critical analysis done, a causal chain like connecting concepts, phases like structuring, resource realities like practical trade-offs made.

The paraphrase writes quality closer to analytical actions, so the same themes more easily happen together within one judgment. The budget example requires understanding the target role, the nature of the experience, and the deliverable's wording at the same time; the organizational assignment requires thinking of people, responsibility, and data tools together. These positions are hard to complete just by writing a separate passage for each quality — when faking it costs as much as actually doing it, the model has no cheap shortcut, and that judgment is exactly the gain the user wants.

The paraphrase, however, found another cheap way to complete things: stringing the story together smoothly. Inferring identical pricing from platform margins, and low price sensitivity from customer overlap, are both examples. A "therefore" between sentences doesn't mean the conditions are enough to derive the next sentence.

So, **making isolated box-ticking harder brings some work closer to real integration; keeping that integration effective still requires checking whether relationships hold, whether premises can bear the weight, and whether later sections should rewrite earlier ones.** In Meta Rules these three things are continuous work; in the paraphrase they are sometimes done and sometimes broken off.

### The Difference Between Prose and Lists Lies in the Relationships Among Requirements

The design intuition of "interlocking, mutually connected prose" captures an important direction in this test: make qualities need each other, so that what one piece of work produces naturally becomes material for another.

But the paraphrase's five sentences keep roughly the same five themes as the Original, and contain no mechanism for checking back. What it adds is semantic concentration, broader conditions of applicability, and partial carry-through between actions. The local revisions that appear in the deliverables show that these arrangements can elicit more work; the global revisions that don't happen show there is still distance between coherent text and a complete workflow.

Meta Rules itself uses many list items, yet its items carry questions, criteria, dependencies, and returns. So a list can be a set of interacting tools, and prose can be just five requirements in a different outfit. What really needs analyzing is: after reading one item, does the next become the necessary next question; after discovering the later item, does it change what was already decided in the earlier one?

The direction supported jointly by this test's texts and deliverables is to move attention from layout form to **how meaning forms sustained working relationships**. A prose rewrite can improve this, and its effect has to be traced through concrete carry-through.

## Looking Back from the Deliverables: How Descriptive Prompting Works

### Descriptive Prompting Varies in Quality; Look at What Work the Model Actually Generates

Descriptive prompting names the qualities to reach; prompting that arranges searching, comparing, and checking within work steps keeps forcing quality out during the process. This comparison lets that distinction be applied more finely.

The Original doesn't have only formal gains: the professional summary and the CRM gap have real uses. Nor does the paraphrase merely swap quality names: without adding any resume expertise, it elicits budget-role recognition, three sets of number readings, and local revisions in operations. **Generic quality descriptions themselves differ in quality, and under their influence the model can complete part of the construction on its own.**

So "description and construction need to work together" should not be read as "gains come only from loading a specific text." The comparisons, conditional branches, and tool reuse that appear under the paraphrase are local construction work; the question is how many key positions it covers, and whether it keeps happening as generation proceeds.

How many quality names are kept only indicates the themes of the requirements; what criteria, operations, and revisions the model actually generates indicates working function. Looking only at names underestimates the paraphrase's real gains; looking only at a few good nodes overestimates whether the whole response already has the same way of working.

### Three Kinds of Carry-Through, Three Kinds of Success and Failure

| Carry-through level | Examples the paraphrase completes | Examples the paraphrase doesn't complete | What to check in design |
|---|---|---|---|
| Semantic coherence | Staffing, quality, frequency, and margin form a clear narrative | The coherent narrative wraps in jumps to identical delivery pricing and low price sensitivity | Whether the "therefore" between sentences really follows, not just whether there is a connective |
| Judgment carry-through | Budget experience decides wording; the four-wall P&L supports area responsibility | Raises prices first but pushes back the pickup channel that would catch returning customers; "may be" becomes a settled plan in the next section | Whether the earlier item's product is actually used by the later item, with its conditions carried along |
| Revision back | Existing idle capacity moves production adjustment earlier | Waste's new status doesn't reorder verification and actions; role criteria give way to resume convention | Whether new findings later can correct what was already written, not just append after it |

This layering explains why the paraphrase reads as more thoughtful yet still has important gaps: it adds much visible work at the first two levels, and has only local instances at the third. Scoring only on "structured, logical" merges the three levels into one high score.

### Goals Written as Actions Also Come in Degrees

Writing goals as actions doesn't only happen with obvious slogans like "strengthen the brand." The paraphrase's "concentrate on 8–12 hero items" and "check at M9 whether it's on the path to breakeven by M12" look more like methods, yet still leave the hardest choices to the user. Numbers, deadlines, and professional terms add a sense of concreteness without providing grounds for the choice.

By contrast, the paraphrase's "if you were involved in annual budget proposals, media mix allocation, or budget discussions, change it to 'planned and allocated'" already provides a recognition rule. Meta Rules' item matrix expands this kind of rule into a multi-dimensional comparison, with data sources, classification, and handling.

The useful unit of comparison is therefore not how many verbs, nor the total amount of detail, but: **which previously unfinished judgment does this added content take over?** Saying "pick right" as "strategically select the most valuable items" hands over no judgment; providing dimensions and operations that change the choice is what actually reduces the user's work.

### When the Push Gets Stronger, Existing Leaps Get Pushed Further Too

The paraphrase's improvements and its failures share one structure: it is more willing to connect, and better at unfolding. Connected to valid conditions, it produces budget criteria, resource branches, and organizational assignments; connected to premises not yet identified, it unfolds identical delivery pricing, customer behavior, and cash availability all the way into plans that look executable.

A driving requirement — multiple perspectives, relationships, context — without another requirement responsible for catching the forms it takes when satisfied superficially will, as execution strength rises, push existing leaps further as well. The paraphrase is a wording rewrite, and its deliverables show the pattern of "local work strengthened, the paired checks not keeping pace."

Catching this pattern means not treating the Original, the paraphrase, or Meta Rules as each having a single quality score. The Original has the gains of the summary and CRM, and also narrower choices than Baseline; the paraphrase has finer judgments, and also later pickup timing than both the Original and Baseline; Meta Rules' advantage is that at more key positions, active solutions constrain and are constrained by verification, conditions, resources, and user operations.

The quality of descriptive prompting is therefore not a straight line of "the more complete the requirements, the better." It changes where the model applies its existing abilities, and also which existing abilities fail to enter the deliverable. The value of the four-way comparison is to lay these directions out.

### The Shape of the Differences This Material Needs Explained

If the Original and the paraphrase are both simply filed under descriptive prompting and every gap attributed to "missing Meta Rules," this test's value is wasted. A useful design explanation must account for all of the following at once:

- Without adding expertise, the paraphrase turns part of existing knowledge into more usable judgments.
- Some of the paraphrase's progress exceeds Baseline; some only restores capabilities the Original lost.
- The same paraphrase can carry back on the organizational problem, yet stops on waste and resume ordering.
- A more complete cost model can coexist with a stronger misjudgment of the present state.
- The same situational constraint can be used to shut down options, or be broken down further to find ways to create resources first.
- A reader under Meta Rules treats the ability it filled in as what the original text naturally implies, and transmits only part of it through the paraphrase.

The carry-through levels, cheap ways of completion, pairing of drive and check, and transfer of understanding discussed above correspond to these differences, turning "descriptive prompting varies in quality" from a summary verdict into something that points to visible positions in each deliverable.

## Thinking Textures Shared with Test 6

The Original and the paraphrase are two separate runs; one prompt is numbered items and the other is prose, not a single generated sentence is shared, and the paraphrase's operations response is nearly half again as long as the Original's. Yet the two responses repeatedly show the same patterns at the same kinds of positions. The wording of any single generation is random; a pattern that still recurs across two runs and two ways of writing is the signal design can use. The following three textures are shown both by [Test 6](Test-6：metaspo-original-gains-and-gaps-of-a-universal-prompt.md) and by this test.

### Texture 1: Checks Point at the Input, Not at the Model's Own Claims

Both responses check the numbers the user supplied closely: the Original questions 綠田's low base, and the paraphrase lays out reading conditions for 綠田, MATZ, and LURE. At the same time, both rewrite the user's words into stronger claims without checking them: the Original turns "no bought followers, mainly through Reels and KOL collaborations" into "purely organic growth" and "~20 people" into "over 20 people"; the paraphrase turns the same line into "no follower growth ads deployed throughout," "averaged" into "steadily maintained," and social media management into "full-scope" marketing. "No bought followers" becomes three different claims across Baseline, the Original, and the paraphrase, all of them stronger; only Meta Rules writes "growth driven entirely by organic reach and partnership-driven traffic."

The cause is the object shared by both prompts. The Original says "Assess the provided data," the paraphrase says "Critically analyze the information provided"; both adjust to the context of "each inquiry"; the only sentence aimed at the answer itself asks, in both, for clear, coherent, precise presentation. The prose rewrite changed how the sentences are organized, not what they are about, so critique keeps pointing at the task and precision keeps landing on expression, and no sentence pushes the model to look back at the words it added. The Meta Rules response lists verb upgrades in the same resume as the single largest unverified assumption, and the difference comes precisely from Meta Rules containing checks whose object is the model's own generation.

### Texture 2: Conditions Fall Away as Estimates Travel Downstream

Both responses first make conditional estimates and then use the results as data in later sections. The Original's same-store visit decline of "about -13%" rests on "same-store transaction value is likewise +12%," and by the delivery section becomes "visits down 13%." The paraphrase's "identical delivery and in-store pricing" is reverse-engineered from an assumption and, by the action section, has become "the company has not passed on a single dollar"; "the baker freed up by closing one store may be exactly what is needed to restore full hours at the two stores currently operating on shortened schedules" becomes "prioritize redeployment" in the resource section. Both responses also write NT$9.5M as the direct cost of the channel shift, without marking that this requires delivery to be substitution.

Meta Rules makes nearly the same inferences on the same task, including suspecting delivery hasn't been marked up; the difference is that it writes these inferences as hypotheses, attaches checking methods, and holds related recommendations until the results come in. Texture 2 is therefore not an inability to estimate; it is that nothing in descriptive prompting asks: when this result is carried into the next step, is its premise still there?

### Texture 3: The Verification List Sits Alongside; the Prescription Is Not Rewritten

Both responses write "hypotheses requiring further verification" as the task requires, in a sensible order; but the lists are not connected back to the prescriptions. The Original says departed-baker interviews will determine "whether the next step is raising pay or changing processes," yet its staffing plan has already ruled out raising pay; it lists the new/old store split as "the foundation of the entire diagnosis," yet later sections still use -13% directly. The paraphrase says whether European bread's decline is demand-side or supply-side is "the single highest-priority validation" and that the strategy changes completely depending on the answer, yet its category strategy is already written as "My judgment is defend"; it says waste is larger than any action's impact, yet ranks waste third tier in its verification order.

The same pattern appears as "seeing without acting": the Original recognizes that the type of role changes how the resume should be written, yet hands the choice back to the user; the paraphrase recognizes that management experience is key evidence, yet leaves it last out of resume convention. The task asks for a hypotheses section, and both responses deliver one; under descriptive prompting, "delivering the section" is where the requirement counts as completed. Meta Rules connects the list to action with verification gates and "Do not execute corresponding recommendations until the first three are verified," which is what gives later findings the authority to rewrite earlier sections.

### What the Three Textures Show Together

The paraphrase is clearly stronger than the Original at local integration: budget recognition, the three number sets, basis reconciliation, and organizational assignment are all examples. Yet not one of the three textures disappears. This shows that turning items into prose, merging sentences, and loosening the emotion condition move the model's quality in the "pushing forward" direction; checking the claims it writes, keeping premises attached to results, and letting later findings rewrite earlier sections are all "looking back" work, and neither descriptive prompt has a single sentence that takes them as its object.

The design conclusion is direct: to change these three textures, changing layout and wording is not enough; the prompt must contain requirements whose object is the model's own generation — check added claims, reconfirm premises when citing estimates, let new findings rewrite what has already been written. The Meta Rules responses show all three behaviors with the same model on the same tasks, which corresponds to its containing requirements of this kind.

## What This Test Means

### Descriptive Prompts Differ in Ways That Reach the Deliverable

The Original and the paraphrase share similar quality themes, and the paraphrase's prompt is shorter, yet it does work the Original did not on the resume's number conditions, budget-role recognition, and local carry-through in operations. "They are both just generic quality requirements" is therefore not enough to substitute for functional analysis.

On the other hand, the Original's professional summary, Baseline's concrete experience recall, and early pickup arrangement all show that comparisons need to keep cross-cutting advantages. The paraphrase's value is not leading on every item, but making visible that changes in semantic organization and conditions of applicability change the direction of gains, and also bring new breaks.

### Between Understanding a Prompt and Getting Another Model to Achieve That Understanding Lies Real Engineering

Sol's paraphrase makes this usually omitted link visible. A reader can fill in considerable quality while understanding, yet mistakenly attribute all of it to the source text; when writing that understanding back into a prompt, some relationships are kept and some abilities stay with the reader.

The actual deliverables of the Original, the paraphrase, and Meta Rules take this transmission apart. The paraphrase's gains show which understandings got through; the gap between the paraphrase and Meta Rules shows which work that text did not carry. This is prompt-translation material that formed by accident, yet has independent value.

### Meta Rules' Comparative Value Lies in Showing How More Complete Work Holds Together

Meta Rules shows that a resume can connect the target role, capability confirmation, case evidence, and applications; operations can connect diagnosis, tools, data acquisition, staffing assignments, and customer actions. That additional content ultimately returns to the resume's persuasiveness and the operations plan's executability.

So the most important distance between the paraphrase and Meta Rules is not that the paraphrase still lacks a few elegant requirements. It already shows effective local integration; the gap is whether that integration can last to every key position, and give later findings the ability to rewrite answers already generated.

Test 6 shows what the Original's quality requirements actually do; Test 7 shows that the same qualities, through different understanding and expression, form different degrees of carry-through, and the three thinking textures they share mark the limits of descriptive prompting itself. Together, the two documents move the comparison from "does the prompt work" to "what understanding was transmitted, what work was completed, and what gains actually entered the user's deliverable."
