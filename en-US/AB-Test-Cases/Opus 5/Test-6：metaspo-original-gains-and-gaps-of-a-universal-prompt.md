# MetaSPO Original — Gains and Gaps of a Universal Prompt

> All content below — the test design, prompts, responses, and analysis — was originally produced in Chinese and has been translated into English for accessibility. The MetaSPO system prompt is quoted in its original English.

> Model: Opus 5 | Thinking level: High | System prompt: MetaSPO Global version (original paper text) | Test date: 2026-09-13

# Test Purpose

Earlier tests have already compared Baseline and Meta Rules. The next question is: where does a universal prompt obtained through a different design path push the model's quality? Can the gains, regressions, and unchanged parts be traced back to how the prompt itself is written?

This test reruns two earlier tasks — a resume rewrite and an operations diagnosis — using the universal system prompt published by MetaSPO. The prompt directly asks for critical analysis, adaptation to different query types, emotional understanding, clear expression, and adjustment to context. The analysis follows how these requirements enter the concrete deliverables, tracking which judgments the model completed for the user and which work was left in the user's hands.

The comparison has two layers. Baseline provides the benchmark of existing capability, used to identify new gains and regressions. Meta Rules provides a higher level of completion already seen on the same tasks, used to show that gaps treated as "the best one can do" actually have solutions. The unit of evaluation is the entire usage path: deliverable, analysis, verification arrangements, and follow-up actions.

On the resume task, differences show up in positioning, wording, evidence, and job-search preparation; on the operations task, they span diagnosis, estimation, options, resources, and scheduling. Together, the two scales help identify whether a quality requirement is satisfied once in a single passage, or keeps constraining and driving the work that follows.

**The purpose of this document is to find the causes of concrete differences in how the prompt is written, and to distill usable design understanding from the sample.**

## Design Considerations

### Why This Universal Prompt

MetaSPO stands for Meta-level System Prompt Optimizer, from *System Prompt Optimization with Meta-Learning* by Yumin Choi, Jinheon Baek, and Sung Ju Hwang. The research uses bilevel optimization of system prompts and user prompts to find system prompts that work across tasks. This test uses the Global version from Appendix C.1, Table 18, and observes what this text concretely does once it enters Opus 5. [Paper and prompt source](https://arxiv.org/html/2505.09666v1#A3.T18)

The paper's Global setting aims for a system prompt that generalizes across domains. Optimization and evaluation use tasks from five domains — Medical, Review Analysis, Reasoning, Safety, and Grounding — scored with metrics that have ground-truth answers, such as accuracy, F1, and exact match. This text was therefore optimized on scorable tasks. This test carries it into professional tasks with no single correct answer, to see how it behaves once it leaves its original evaluation range. This row of Table 18 is identical in arXiv v1 and in v2, revised in October 2025.

The sample has direct comparative value: it does not tell the model in advance how a bakery should be run, nor does it supply professional answers for a resume. Instead, it specifies general quality directions and lets the model bring its existing knowledge into the task at hand. The research's optimization loop produced this text; this document analyzes what functions the text itself carries in actual responses.

### The Original's Quality Directions and Their Positive Effects

| Prompt component | Work the requirement takes on | What it should do in these tasks when it truly takes effect |
|---|---|---|
| Advanced general-purpose assistant identity | Processing and analyzing information across topics | Draw on job-search, marketing, retail, and supply-chain knowledge to form professional criteria fitted to the task |
| Critical analysis, multiple perspectives, implications, logic, and connections between concepts | Understanding what the data means and how it interrelates | See the conditions under which numbers can be read, the resume's real strengths, and the interactions behind operational symptoms |
| Handling different types of queries | Applying reasoning suited to the query type | Resume restructuring should serve how recruiters read; operations analysis should form a plan that can be chosen and executed |
| Sentiment and positive/negative signal assessment | Understanding mixed signals and forming an overall assessment | In relevant contexts, account for the user's situation, confidence, and actual goal, so that tone and follow-through stay consistent |
| Clear, structured, precise | Making reasoning and conclusions easy to understand | Readers know which material supports which judgment; the deliverable is easy to read and use |
| Adjusting to context and details | Letting specific conditions change the analysis | The target role changes the resume's emphasis; cash, staffing, and deadlines change operational choices and sequencing |

The positive effects of these requirements can build on one another: multiple perspectives produce different readings, logical relationships organize the data into a structure, contextual details change which readings apply, and clarity and precision finally deliver the results to the user. Whether the emotional requirement works should also be judged within the task context, not by whether a separate paragraph about feelings appears.

Items 2 and 3 explicitly name factual questions, sentiment analysis, logical deduction, and reviews — the task types of the paper's evaluation domains. On resume and operations tasks they have no ready-made object; the model has to translate them into query-type adaptation and situational understanding on its own. The third column of the table describes what that translation looks like when it succeeds.

### What to Observe on the Two Tasks

**Resume rewrite**: give existing experience wording that fits the target role and bring out the positions worth pursuing; at the same time, provide usable ways to recall material, fill evidence gaps, and demonstrate capability, so the user can confirm where they stand and actually carry their strengths into applications and interviews.

**Operations diagnosis**: build a problem structure from the data, find the leverage points that decide success or failure, then connect them into actions with resource sources, sequencing, and grounds for choice. Where information is insufficient, look at how the model obtains information, how it advances what can already be done, and how different answers would rewrite the plan.

Below, the prompt, the two tasks, and the Original's responses are preserved first, followed by an analysis of the actual differences.

# MetaSPO Base Prompt

The text comes from the Global row of Table 18 in the paper above; the paper is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

You are an advanced virtual assistant designed to process and analyze information across a broad range of topics. Your main objectives are to:
1. Analyze Information Critically: Assess the provided data, considering various perspectives and implications. Use logical reasoning to derive conclusions and make connections between concepts.
2. Handle Different Types of Queries: Be prepared to respond to factual questions, perform sentiment analysis, and engage in logical deductions. Understand the nuances of each query type and apply appropriate reasoning.
3. Evaluate Sentiment and Emotional Tone: When dealing with reviews or sentiments, accurately reflect the emotional tone—consider both positive and negative elements—and provide a clear overall assessment.
4. Provide Clear and Structured Responses: Organize your answers in a coherent format, making it easy for users to understand your reasoning and conclusions. Aim for clarity and precision in your communication.
5. Adapt to Context: Adjust your analysis based on the specific context and details given in each inquiry. Pay attention to nuances and subtleties that may affect the outcome of your assessment.
By following these guidelines, you will better serve as a helpful assistant, enabling users to receive accurate, relevant, and thoughtful responses to their diverse queries.

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

# MetaSPO Response 1

<details>
<summary>Expand full response</summary>

I've rewritten it for you. The core idea: **your current version describes "duties," while a brand-side manager role wants to see "what business results you can deliver for a brand."** So I flipped the order entirely — the two projects that best prove "strategic leadership + business results" (綠田, MATZ) go first, with social and ad operations further down.

---

## Suggested Version

**Professional Summary**

5 years of digital marketing experience across four industries: beauty, fitness, organic food, and 3C. Manages annual digital ad budgets of over NT$24M; led transformation projects for 2 brands spanning positioning to channel; skilled at breaking brand strategy down into executable traffic, content, and conversion architectures, and at leading teams to deliver them.

**ABC Digital Marketing | Marketing Planner → Senior Marketing Planner (2020–2025)**

- **Led the overall digital strategy for organic food brand "綠田"'s transition from traditional retail to e-commerce**: independently planned the website traffic architecture, social content repositioning, and ad account rebuild; monthly website revenue grew from NT$150K to NT$850K within 3 months (+467%), establishing a replicable D2C growth model.

- **Led the brand repositioning project for 3C accessories brand "MATZ"**: shifted the brand's positioning from budget accessories to design-driven, redefined the visual identity system and social media tone of voice, and planned collaborations with 5 design-focused KOLs; brand search volume grew 240% within 3 months.

- **Oversaw Meta / Google ad campaigns with monthly budgets of NT$1.5–2.5M (over NT$24M annually)**: overall ROAS sustained above 3.5 over the long term; restructured the membership conversion path for fitness brand "動次" and optimized audience segmentation and creative iteration, reducing CPA from NT$680 to NT$320 (-53%).

- **Ran 4–6 brand social accounts simultaneously (FB / IG)**: built around Reels content strategy and KOL collaborations; grew beauty brand "LURE"'s IG followers from 12K to 87K in two years (+625%), with no purchased followers at any point — purely organic growth.

- **Team Development and Knowledge Building**: led 2 planners, developing 1 of them from a new graduate to independently handling client projects; designed and taught the company's in-house Meta advertising and GA4 training across 4 cohorts, over 20 people in total.

**Tools**: Meta Business Suite, Google Ads, GA4, Looker Studio, Canva, Notion

---

## A Few Judgment Calls I Made — Your Call Whether to Keep Them

**Converted the budget to an annual figure.** "NT$1.5–2.5M a month" reads like small-scale work on the brand side; "over NT$24M annually" is what makes people feel you have experience operating at scale. This matters a lot for a manager role.

**Changed every "assisted" to "led."** You originally wrote "assisted with client brand repositioning project," but from what you describe, the visual identity, tone, and KOL collaborations were all your decisions — that's leading. What brand-side employers fear most is hiring an agency person who "can only execute a client brief"; this verb makes a big difference.

**Be ready to be questioned on the 綠田 line.** NT$150K → NT$850K is a great growth rate, but the base is low; an interviewer might ask, "Was the website basically not being run before?" I suggest preparing a one-line addition, such as the ad return ratio over the same period, or what share of total revenue that NT$850K represents. If the share is decent, writing it directly into the resume will be stronger.

## Two Missing Pieces

**Evidence of cross-departmental collaboration.** Brand-side managers have to fight it out with sales, channel, product, and customer service. Your experience is entirely from the agency perspective; I suggest adding, in interviews (or your personal statement), how you coordinated with the client's marketing, sales, and design teams — that actually is cross-departmental experience, just framed differently.

**Retention (CRM / EDM / membership management).** Your strengths are concentrated in acquisition and advertising, while brand-side roles very often require retention. If you've touched it at all (even retargeting or member tagging during 綠田's e-commerce transition), it's worth adding a line; if not, be honest when asked in the interview, and explain how you plan to fill the gap.

Want me to adjust the emphasis based on the specific roles you're targeting (e.g., e-commerce brands vs. brick-and-mortar retail brands)? The two actually look for fairly different things.

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

# MetaSPO Response 2

<details>
<summary>Expand full response</summary>

# Operations Diagnosis: From Symptoms to Root Causes

## 1. First, a Data Contradiction

Before getting into the diagnosis: one set of numbers doesn't add up, and it may be the most important signal in the entire dataset.

Customer visits down 8% YoY and average transaction value up 12% should multiply to revenue of **+3%**. But same-store revenue is **-3%**. That's a gap of 6 percentage points.

The reasonable explanation: the -8% in visits is an "all-store average," diluted by the 2 newly opened stores (which have higher opening-period traffic). If same-store transaction value is likewise +12%, back-calculating gives a same-store visit decline of about **-13%**, not -8%.

This difference changes the nature of the problem. -8% is "a trend that needs improvement"; -13% is "an alarm that the customer base is draining away." **Be sure to first split visits between new stores and same stores to confirm the real magnitude of the decline** — the force of every judgment that follows rests on this number.

---

## 2. Diagnostic Framework: A Three-Layer Structure

### Surface Symptoms
Declining visits, rising transaction value, flat revenue, rising costs.

### Middle-Layer Mechanisms (How the Symptoms Mask One Another)

**Mechanism 1: Rising transaction value is a structural illusion, not an increase in value**

Transaction value rose from 185 to 207; over the same period, pastries and cakes rose from 25% to 33%, and delivery from 12% to 22%. These three things are three facets of the same thing: pastries carry a higher unit price than European bread, and delivery platforms' "free shipping above a minimum order" mechanism forces up basket value.

In other words, the rise in transaction value very likely **contains almost none of "existing customers buying more,"** and is instead the arithmetic result of shifts in category and channel mix. If management reads it as "brand strength is up, we can raise prices again," it will make a completely wrong decision.

**Mechanism 2: Delivery growth is trading gross margin for revenue**

A rough calculation of the direct cost of the channel-structure shift:

| | Last year | This year |
|---|---|---|
| Delivery share × 18% margin | 2.2% | 4.0% |
| In-store share × 52% margin | 45.8% | 40.6% |
| **Blended gross margin** | **~48%** | **~44.5%** |

The channel shift alone cuts gross margin by about 3.4 percentage points — on NT$280M, roughly **NT$9.5M**. Layer on raw materials +14% (if raw materials are about 30% of revenue, that erodes about 4 percentage points), and the annual gross margin decline very likely reaches **6-8 percentage points, or NT$17-22M**.

For a mid-sized chain, this figure is enough to wipe out a full year's net profit. **My judgment: your company's real profit this year may already be near breakeven or negative, merely masked by new-store revenue and delivery turnover.** This needs to be confirmed against the actual income statement, but it is the first thing that needs confirming.

The key question isn't "delivery margins are low," but — **is delivery incremental or substitution?** Visits down 13% and delivery up 10 percentage points line up closely in time. If delivery customers are mostly people who would otherwise have come to the store, then delivery growth isn't a new market — it's you converting 52%-margin customers into 18%-margin orders, while also losing the in-store add-on purchases, samples, and staff interactions that make up the brand.

**Mechanism 3: The business model is sliding from "high-frequency daily" toward "low-frequency occasion"**

European bread is a staple, high-frequency, habitual purchase; pastries and cakes are occasion-driven, low-frequency, comparison purchases. The crossover in category shares — 45%→38% against 25%→33% — really means **the nature of the customer relationship has changed**.

A high-frequency customer comes 2-3 times a week; a low-frequency customer comes once a quarter. That is exactly why visits and category mix moved together — they are the same phenomenon.

And the problem is: **the rent and staffing structure of 12 stores was designed for high-frequency traffic.** When traffic turns low-frequency, the base for spreading fixed costs collapses. This is also why a 15-25% rent increase is especially lethal.

### Underlying Root Causes

**Root Cause A: Supply-side quality breakdown, not a shift in demand-side preference**

Baker turnover at 40%; 2 stores have shortened hours due to staffing shortages. Given this, I don't believe the decline in European bread's share is mainly "consumers no longer love European bread."

The more likely causal chain:

> 40% baker turnover → inconsistent feel for fermentation, shaping, and baking → fluctuating European bread quality (European bread is the most technique-dependent and the least able to hide flaws) → high-frequency customers are the most quality-sensitive, because they eat it every day → high-frequency customers leave first → visits decline + European bread share declines → what remains are quality-insensitive occasion customers

Add the direct supply-side loss: when short-staffed, the first items cut are those with long processes (European bread needs hours of fermentation), replaced by standardized, pre-producible pastries. **So a considerable share of the category shift is "can't make it" rather than "can't sell it."**

If this hypothesis holds, all marketing and promotional spend will be wasted — the problem isn't on the demand side.

**Root Cause B: Eight years of operation have not built up customer assets**

60,000 members, 12,000 monthly active (20%). Bakery is **one of the formats that should be most high-frequency**; the reality behind 20% monthly activity is that the membership program is just points collection, not a relationship.

More serious is the volume: 12,000 × NT$207 × 12 months ≈ NT$30M, only about 11% of revenue. **Nearly 90% of revenue comes from customers you cannot identify, reach, or retarget.** A brand with 12 stores open for 8 years has no moat — which explains why traffic walks away as soon as quality fluctuates and competition appears.

**Root Cause C: Mismatch between capital allocation and cash flow**

Amid same-store decline, collapsing margins, and staff shortages, resources went into opening stores. The new stores lose NT$300K a month (combined), NT$3.6M a year; if the three legacy stores' rent rises 20%, that adds several million more each year. These cash outflows are happening at exactly the moment money most needs to go into "fixing individual stores."

---

## 3. Prioritized Action Sequence

### Days 0-30: Stop the Bleeding and Build the Diagnostic Foundation

**(1) Start lease negotiations immediately — don't wait**

The three stores' leases expire in 8 months, which looks like time to spare, but negotiating leverage takes 2-3 months to prepare, and **the landlord knows that the closer you get to expiry, the fewer alternatives you have**. Do three things in parallel now: build full store-level P&Ls for the three stores (including allocated HQ costs), survey alternative sites and market rents within a 500-meter radius, and estimate the one-time costs of closing (residual value of fit-out, severance, equipment relocation).

With these three pieces of data, you can negotiate with confidence. I suggest setting the decision rules as:

- **Still positive contribution margin after the rent increase** → accept, but negotiate for concessions in exchange (rent-free fit-out period, stepped increases, percentage-of-revenue rent)
- **Contribution margin near zero after the increase, but the customer base has strategic value** → renew on a short lease (1-2 years) to keep options open, with no renovation investment
- **Already losing money** → don't renew, and treat this as good news rather than bad. The cash and staff freed by closing a loss-making store are worth more than its revenue

**Replacing fixed rent with percentage-of-revenue rent** is a negotiating direction worth pushing hard in this situation. You are currently bearing all the revenue risk; having the landlord share part of it is more reasonable for both sides than locking in a high rent.

**(2) Three essential analyses**

- **Store P&L ranking**: the profit distribution across 12 stores is almost certainly highly uneven. Quite possibly 3-4 stores are subsidizing the other 8. Without this table, any resource allocation recommendation is guesswork.
- **Delivery incremental/substitution analysis**: match member phone numbers against delivery platform orders and in-store purchase records to calculate the overlap rate. High overlap = substitution = you are cannibalizing yourself.
- **Departed baker interviews**: interview every baker who left in the past 12 months (post-departure interviews are far more honest than surveys of current staff). Clarify whether it's pay, hours, management, or a career ceiling. This determines whether the next step is raising pay or changing processes.

**(3) Stop the delivery bleeding**

No need to leave the platforms, but implement **channel-separated pricing** immediately: price delivery items independently, explicitly reflecting the platform commission; at the same time **narrow the delivery SKU range**, keeping only items that travel well, carry high margins, and don't degrade easily. European bread after 30 minutes of delivery is no longer the original product — this hurts both margin and brand.

At the same time, launch **pre-order pickup through your own channel** (order online, pick up in store). This is the key bridge for bringing delivery customers back to the store — customers get convenience, and you keep the margin and the face-to-face contact.

### Months 1-3: Fix the Staffing Structure

This is the most critical item, and the one most in need of being tackled head-on. **A 40% baker turnover rate is not an HR problem; it's an operating-model problem.**

The direction isn't "raise pay to retain people" (cash flow doesn't allow it, and competitors will raise too), but **reducing dependence on individual bakers' craftsmanship**:

- **Centralize frozen dough/pre-fermentation**: one central process handles European bread dough-making and pre-fermentation, frozen and delivered to stores, which only thaw, do the final proof, and bake. This solves quality consistency, the staffing skill threshold, and shortened hours at the same time.
- **Don't build a central factory at the start.** Cash flow doesn't allow it. First find a third-party bakery contract manufacturer (Taiwan has mature frozen-dough contract capacity) to trial 3-5 core SKUs, and discuss building your own only after validating quality and cost. Outsourced margins will be somewhat lower, but far cheaper than closures and quality swings.
- **Tier the roles**: split the "baker" position into "technical bakers" (responsible for recipes, quality control, and new products; few in number, highly paid) and "bakery operators" (responsible for standardized processes; trainable, with a much larger hiring pool). 40% turnover at the operator level is bearable; at the technical-baker level it's a disaster.

**(4) Member activation**

The 48,000 dormant members among your 60,000 are **the lowest-cost revenue source** in this dataset. Waking up an old member costs far less than acquiring a new customer, and they chose you once before.

The approach should target "higher frequency," not "promotions": launch a **subscription** for members who have bought European bread (fixed weekly pickup, prepaid monthly fee, a discount in exchange for certainty). This does three things at once: pulls low-frequency customers back to high frequency, collects cash in advance to improve cash flow, and provides a predictable production schedule (a huge help for an understaffed production line).

### Months 4-12: Structural Adjustments

- **Set the keep-or-close decision point for the new stores at months 9-10** (one full year since opening). The criterion isn't "is it profitable yet," but **the slope at which losses are converging**. If the monthly loss is narrowing month by month from NT$150K, give it time; if it has been flat for 12 months, cut losses. First confirm the shape of these two stores' loss trajectories.
- **Pause all new store openings**, at least until same-store revenue turns positive.
- Based on the store P&L results, **close the bottom 1-2 stores**, concentrating staff (especially bakers) in high-potential stores, so that the stores that had to shorten their hours can return to normal operation first.

---

## 4. Resource Reallocation

| From | To | Rationale |
|---|---|---|
| Store-opening capex | Central production/frozen dough (outsourced first) | Fixing the capacity bottleneck returns more than adding stores |
| New-customer acquisition marketing | Dormant member activation and subscriptions | A stock asset of 48,000 people, lowest marginal cost |
| Full-range listing on delivery platforms | Own pre-order pickup + curated high-margin SKUs for delivery | Each 1% of revenue brought back recovers roughly a 34% margin difference |
| Pay raises to retain bakers | De-skilling the process + tiered technical bakers | Raises are an arms race; de-skilling is a structural fix |
| European bread stocked in every store | European bread at high-potential stores + streamlined SKUs at weak stores | With limited staff, quality consistency beats range breadth |

---

## 5. Hypotheses Requiring Further Verification

In order of importance:

1. **The real decline in same-store visits** (new-store/same-store split) — the foundation of the entire diagnosis
2. **Actual gross margin and net profit** — I estimate net profit may already be near zero or negative; this needs confirming because it determines the urgency of every action
3. **Delivery substitution rate** (cross-channel member ID matching) — determines whether the delivery strategy is contraction or diversion
4. **Whether the European bread decline is demand-side or supply-side** — check stockout rates, daily actual SKU production completion rates, and sell-out times. If European bread often sells out early or isn't made at all, it's a supply problem
5. **Decomposition of the transaction value increase** — break it into "price increases / category mix / items per basket" to confirm whether value has genuinely risen
6. **Store-level P&L distribution across the 12 stores**
7. **The real reasons for baker turnover** (exit interviews)
8. **The convergence trajectory of new-store losses**

---

## 6. Three Critical Dimensions Not Mentioned

**(1) The cash flow statement is the real decision premise**

The entire dataset has only P&L figures, no cash. When simultaneously facing "new stores still bleeding + rising rent + possible central production investment + possible closure costs," **available cash and bank credit lines determine which recommendations are feasible and which are just paper plans**. First confirm the cash flow forecast for the next 12 months and the available financing, which will directly filter out some of the recommendations above. If cash really is tight, the priorities should be adjusted to: lease negotiations > delivery pricing > member prepayment (collects cash in advance) > central production.

**(2) Positioning in the competitive landscape**

In recent years, convenience stores and supermarkets have upgraded their bakery offerings, Japanese/Korean brands have entered, and studio-style artisan bakeries have risen; mid-sized chains are squeezed in the middle: less scale than convenience stores, less distinctiveness than small shops. Part of the same-store decline may not be anything you did wrong, but rather that **the "middle ground" itself is disappearing**. This requires answering a strategic question: over the next 3 years, go toward "efficiency at scale" or "quality scarcity"? The two directions take completely opposite stances on central production. If you don't answer this question now, the market will answer it for you in a year.

**(3) Seasonality risk from the category shift**

Pastries and cakes rising to 33% means revenue depends more on occasions (Mother's Day, Christmas, birthdays). This brings seasonal swings in cash flow, peak-and-trough gaps in capacity, and single-point risk if a holiday goes wrong. European bread's value lies not only in its margin but in providing **a stable revenue floor**. This is another reason to "restore European bread" rather than "go with the pastry trend."

---

If I had to name the single top priority: **first break out the real same-store visit numbers, then finish interviewing the bakers who left in the past 12 months**. Both can be done within a week at near-zero cost, and they will decide whether the resources that follow go to the demand side or the supply side — get this direction wrong, and the next 12 months of investment go down the drain.

</details>

# Test Insights

## Comparison Materials and Reading Guide

Below, "Original" refers to the MetaSPO responses in this file; "Baseline" and "Meta Rules" refer to the two earlier responses to the same tasks. Key sentences and operations are quoted directly in the analysis; the full comparison materials are:

- [Resume Rewrite — Survivability of a "Simple" Task](Test-3：resume-rewrite-survivability-of-a-simple-task.md)
- [Operations Diagnosis — Baseline vs. Meta Rules Under High-Specification Prompting](Test-1：operations-diagnosis-baseline-vs-meta-rules-under-high-specification-prompting.md)

Length, counted in Chinese characters of the original responses: resume task — Original 951, Baseline 975, Meta Rules 3,952; operations task — Original 3,552, Baseline 4,356, Meta Rules 13,530.

| Where to look | The difference most worth tracking | The user benefit it affects |
|---|---|---|
| Resume positioning and deliverable wording | Professional summary and business vocabulary increase — does the strategic evidence get stronger with them? | Whether recruiters can see the user's real capabilities |
| Resume gaps and numbers | Once a gap is pointed out, is there a concrete recall prompt, backfill condition, or capability demonstration? | Whether the user can turn a position on paper into one that holds up in interviews |
| Operations diagnosis | Do new explanations keep their conditions; do existing variables constrain the model's own calculations? | Whether the customer, channel, and staffing problems are correctly identified |
| Operational actions | Are existing operations preserved, or re-abstracted into goals? | Whether the user gets a method, or another to-do list |
| Overall carry-through | Does later verification actually change earlier prescriptions? | Whether the plan can advance, correct, and converge as reality unfolds |

## Resume: The Target Role Enters the Deliverable, but Most Core Capabilities Were Already in Baseline

The Original puts 綠田's channel transformation and MATZ's brand repositioning up front, with advertising, social, and team experience in support behind them. This ordering has real value: it moves the user from "what channel work I've done" toward "what business results I can deliver for a brand."

But Baseline on the same task had already made this ordering, and had already pointed out the perspective problem of moving from agency to brand side. The ordering and perspective are therefore capabilities the Original retained, not new gains brought by MetaSPO.

The Original's clearer new contribution is a full "Professional Summary" placed at the top of the resume, bundling tenure, industry breadth, budget, transformation cases, and team leadership into one paragraph. Compared with Baseline's italic positioning line, this provides a more complete entry point for reading the candidate as a manager. Merging team development and internal training into "Team Development and Knowledge Building" at the end also gives the two a shared capability framing. Both are gains relative to Baseline; the Meta Rules version likewise has a personal summary and likewise merges team leadership and training into one block.

These are real improvements to the deliverable: they reduce the reader's burden of piecing together a profile of the person.

Reading down into the case entries, however, newly added phrases such as "establishing a replicable D2C growth model" and "visual identity system" mainly raise the level of generalization of the results. How the model was formed, why it is replicable, and which key trade-offs the user made do not become any more observable. **The density of manager vocabulary rises; the evidence of strategic judgment does not rise to the same degree.**

Similar vocabulary also appears in the resume body of the Meta Rules version ("establishing a replicable acquisition model"). The difference is not in the wording itself but in whether these claims are followed by arrangements for verification, backfill, and demonstration, compared item by item below.

This is the texture difference in deliverable wording: reading more like a professional resume, and letting recruiters see more solid professional capability, are two gains that must be tracked separately.

## Resume: Sense of Scale Gets More Active Handling Than What the Numbers Mean

The Original turns the monthly budget of NT$1.5–2.5M into "over NT$24M annually," using it repeatedly in the professional summary, the ad entry, and its explanation of the rewrite. It also says outright that annualized figures make brand-side readers feel operational scale more strongly.

Converting monthly scale into annual language could in principle improve how a manager-level reader takes it in. The problem is that the source data gives a range: straight annualization yields NT$18–30M, which is exactly how the Meta Rules version writes it. "Over NT$24M" amounts to claiming a monthly average above NT$2M, in the upper half of the range; the source data provides no annual total that would justify picking that side, and the Original does not ask for the actual annual total to be backfilled in its follow-up preparation.

Baseline also picked an annualized value, writing "Annual managed media budget NT$20M+," which only requires a monthly average of about NT$1.67M and stays in the lower part of the range. The Original pushes the chosen value into the upper half and adds a separate justification for why this wording will impress brand-side readers more.

At the same time, the Original does raise a valuable check on 綠田's revenue growth: whether the base was too low, whether the original website was barely being run, and what the same-period ad return or revenue share looked like. It lets the user know a good-looking number still needs context — a clearer gain than Baseline.

But this standard mostly stops at 綠田. Whether the CPA drop came with lower conversion volume, how ROAS was calculated and aggregated, and how large MATZ's search base was receive no corresponding treatment.

**This shows how quality work was allocated: the model invested repeated effort in shaping a sense of scale, while the work of measuring scale and the real weight of the results was concentrated in one flagged case.** The model does not lack number-judgment ability; that ability simply does not run through the other numbers that equally hold up the conclusions.

## Resume: The User's Numbers Face a Checkpoint; the Original's Own Additions Do Not

The Original sets a checkpoint of "low base, will be questioned" for 綠田, and that checkpoint falls on a number the user supplied. Comparing the input line by line, the claims the Original itself added to the resume do not pass through the same checkpoint:

- The input says LURE's growth came with "no bought followers, mainly through Reels and KOL collaborations"; the Original writes "with no purchased followers at any point — purely organic growth." KOL collaborations involve fees or product exchanges, so "purely organic growth" contradicts the means the user themselves described; a single interviewer question — "Were the KOLs paid?" — overturns it.
- The input says internal training covered "roughly four cohorts totaling ~20 people"; the Original writes "designed and taught … over 20 people in total." "Roughly" becomes "over," and "internal training … for new hires" becomes "designed and taught."
- The input says of 綠田, "I wrote the entire digital transformation marketing strategy"; the Original writes "independently planned," affirming on the user's behalf the very decision authority that agency-background candidates are most often probed on.
- "Establishing a replicable D2C growth model" is a claim of an output that does not exist in the input.

Test 3 already offers a comparison for the LURE line: Baseline wrote "entirely through organic growth with zero paid follower acquisition," which equally contradicts the KOL collaborations; Meta Rules wrote "growth driven entirely by organic reach and partnership-driven traffic, with no paid follower acquisition," using "partnership-driven traffic" to account for the KOLs without claiming it was all organic. On this line, the Original carries over Baseline's contradiction.

The cause can be read from the objects of the prompt's sentences. Nearly all five requirements take the input as their object: analyze the provided data, understand the nuances of each query, adjust to the context of each inquiry. The only item whose object is the answer itself, item 4, asks for organized, clear, and precise *communication*; no sentence asks the model to check whether the claims it writes have grounds. This response's precision lands exactly on the communication layer: percentage calculations, annualized amounts, range notation. Nothing in the prompt pushes toward whether the claims are faithful to the source material. **The words the user is most likely to copy straight into the resume, and most likely to be grilled on line by line in an interview, are precisely these additions.**

## Resume: New Professional Requirements Partly Become New Human Work

The Original independently raises the CRM / EDM / membership management gap, which neither Baseline nor Meta Rules raised. This lets the user see that their resume is concentrated on acquisition and advertising, with retention not yet shown. This widening of view is valuable.

What follows, though, is: if you've touched it at all, it's worth adding a line; if not, be honest and "explain how you plan to fill the gap."

What this last sentence asks the user to do alone is exactly the part that most needs professional help: how much does this gap weigh for different roles? Where can existing experience transfer? What kind of plan to fill it would be credible? How do you show understanding in an interview without passing understanding off as experience? The response folds all of this into a single "explain how you plan to fill the gap."

The cross-departmental gap allows an even more direct comparison. The Original suggests adding how the user coordinated with the client's marketing, sales, and design teams, reasoning that "that actually is cross-departmental experience, just framed differently." Baseline instead offers a more discriminating recall prompt: during 綠田's move to e-commerce, did the user handle any conflict like "will going online cannibalize our distributors"?

The latter lets the user recall an event with a conflict of interest, a decision, and an outcome. The former turns contact with multiple counterparts into a job-posting label, without reaching material deep enough to prove capability.

**Here the Original adds or restates "what you should have," without adding "how to find, build, and demonstrate it."** The user knows more, but the human judgment needed to complete the task is still heavy; on the shared cross-departmental item, the Original even has one fewer practical entry point than Baseline.

## Resume: Two Reminders Baseline Had Did Not Appear This Time

The Original has no confidentiality reminder at all. Four client brands go into the resume under their real names; Baseline reminds the user that if contracts include NDAs, the names can be changed to "beauty brand A" while keeping the numbers, and Meta Rules lists the NDA as an item to backfill.

The Original also does not address the level gap. Baseline points out that leading 2 juniors is thin for a manager role and gives a rewrite path: if the MATZ project actually involved coordinating 5–8 people, write "coordinated cross-functional team of X." Meta Rules goes further, separating highly feasible, moderately feasible, and difficult roles and deriving different resume versions from them. The Original's only comparable move is a closing question asking whether the user wants the emphasis adjusted for e-commerce brands versus brick-and-mortar retail brands. It has recognized that the type of role changes how the resume should be written — exactly the object of the prompt's item 5, "adapt to context" — but it hands this contextual variable back to the user to choose, without preparing the branches.

Neither item requires any additional expertise; the same model wrote both on its own in the Baseline run. The two responses are almost the same length, and the Original spends its space on the professional summary, the annualized amount, and the rationale for its rewrites — work that makes the resume *look* stronger. The reminders that protect the user are what got squeezed out in this reallocation.

## Resume: Meta Rules Provides a Path That Makes the Position Reachable

Meta Rules likewise pushes the user toward a brand-side manager position. It then identifies the core evaluation point — "can you define problems on your own without a brief" — and offers two ways to obtain evidence for it.

One is to organize a past case into one to two pages, presenting the business problem, resource constraints, strategic choices, rejected alternatives, and a retrospective. This gives the meaning of "led" concrete material that can be checked, and helps the user identify which judgments they actually carried.

The other is to first do a marketing diagnosis of a target brand: using specified, checkable ad, traffic, and social material to produce three opportunities and a plan for the first ninety days. This new piece of work demonstrates the ability to define problems independently, while also helping the user screen companies, prepare for interviews, and test their own abilities.

In addition, Meta Rules lists ad spend, conversion volume, search base, the link between social metrics and business results, and actual decision authority as backfill items that will change the resume's strength or wording.

At this point in the comparison, the unit of acceptance should be "target version + material backfill + capability demonstration + revision and application." Its value lies in first finding the position worth pursuing, then giving the user a path to confirm, supplement, and demonstrate it. Extracting just one assertive verb from the first draft would miss the added feasibility this path provides.

The Original tells the user "you need cross-departmental and retention evidence"; Meta Rules goes on to handle how evidence becomes observable, what material can change the positioning, and how to produce a capability demonstration the resume itself cannot provide. The gap lies in the ability to complete the job-search task.

## Operations: The Original Has Real Substance and Some Local Improvements

The Original notices the definitional contradiction among visits, transaction value, and same-store revenue (as do Baseline and Meta Rules; the differences in handling are discussed below), and links the category shift to purchase frequency, store fixed costs, and cash pressure. It frames the slide from "high-frequency daily" to "low-frequency occasion" as a clear business problem, making it easy for the user to see why a change in revenue composition affects the store model.

But the main links among supply quality, staff turnover, channel margins, and fixed costs had already been drawn by Baseline. The Original reorganizes and elaborates these relationships; the discoveries themselves were already in Baseline.

Operationally, the Original places the lease, delivery pricing, and pickup early, and narrows production restructuring to first finding a contract manufacturer to trial three to five core SKUs, discussing its own facility only after validating quality and cost (the problem with which items it chooses is discussed below). Its closing cash-flow section more explicitly requires checking available cash and credit lines and adjusting priorities if cash is tight. These are all concrete planning content.

Baseline's Phase 0, on the one hand, requires building data first and making no big moves, and on the other, in its lease section, requires building alternatives now. The Original puts the lease and delivery bleeding-control directly into the first stage, improving the overall consistency of the opening moves at this point.

The Original's main problems therefore have to be traced into key details and cross-paragraph relationships: it can already propose steps, timing, and checks — but which steps actually reduce the judgment burden of implementation, and which merely give a goal the name of an action?

## Operations: Member Frequency Is Discussed but Never Enters the Model's Own Formula

The Original computes "12,000 × NT$207 × 12 months" to get about NT$30M, concludes from this that members contribute only about 11% of annual revenue and that nearly 90% of revenue comes from customers who cannot be identified, reached, or retargeted, and elevates this into the root cause "eight years of operation have not built up customer assets."

The task states explicitly that monthly active members means "at least one purchase." A calculation of member revenue must at least keep:

`monthly active members × purchases per active member per month × member average transaction value`

The Original set monthly purchases to one without carrying that setting into its conclusion. Keeping its transaction value and full-year extrapolation and changing only the monthly frequency to three (an illustrative value), the same method yields about NT$89.42M instead of about NT$30M.

The other two responses to the same task both keep frequency in the formula: Baseline, when estimating dormant-member reactivation, states "each purchasing monthly" as its premise; Meta Rules, when estimating the increment from active customers, writes "12,000 × 0.4 additional visits × NT$207 × 12 months."

The most telling point: the Original earlier uses frequency to explain the difference between European bread and cakes, and later uses higher frequency to explain the benefits of subscriptions. It already knows frequency matters, yet in the calculation that supports a major diagnosis, frequency is not given the same standing.

This is not just one missing multiplier. It recasts the member asset as almost nonexistent, then uses that to support a narrative of no moat and weak relationships. **A concept appearing in an answer and that concept continuing to constrain the answer's other judgments are two different levels of completion.**

## Operations: Hypotheses and Verification Are Present, Yet Still Turned into a Single Path

The opening same-store visit decline of about 13% is an estimate built on "same-store transaction value also rose 12%." At first the Original flags the condition and asks for new and old stores to be split. But by the delivery section it directly uses "visits down 13%," pairing it with the ten-point rise in delivery share as evidence that the two "line up closely in time."

The premise does not travel with the estimate, and two annual changes provide no sequence capable of establishing a timing relationship. The response performs a check in its first section, but when later sections cite the product of that check, they do not inherit its conditions.

The reconciliation behind this estimate only matches one set of numbers in the first place. If -8% and +12% are both all-store figures, all-store revenue should be about +3% (0.92 × 1.12 ≈ 1.03), which still does not match the task's total revenue of +6%. Baseline, at the same point, computed both the same-store and the company-wide basis, showed that neither reconciles, and listed accounting causes such as delivery booked on a net basis or delivery orders not counted in visits. The Original picks one explanation and lets the -13% it produces flow into later sections. Meta Rules likewise takes only one basis here; the difference is that it lists the basis split as an extremely high-impact hypothesis to confirm within two weeks, and holds the related recommendations until confirmation.

Its proposed way of verifying delivery is to match member phone numbers against delivery platform orders and in-store purchase records, then write "High overlap = substitution = you are cannibalizing yourself." Identity overlap answers who has bought through both channels, not whether original store visits were replaced; "regular customers ordering a few deliveries on top of their store visits" would produce an equally high overlap rate.

Baseline on the same task, besides geographic and membership overlap, also asks whether in-store traffic shows breakpoints after delivery launched. The Original lacks this observation that could distinguish between explanations, yet writes the remaining method as a direct verdict. Meta Rules also mentions phone-number overlap ("high overlap = same people switching channels"), but lists it as supplementary; its main basis for judging substitution is a store-level scatter of delivery penetration against in-store traffic change, with the pricing decision then handed to a two-store, four-week pilot.

The staffing issue shows the same handoff break. The Original first says departed-baker interviews will determine "whether the next step is raising pay or changing processes," then in its staffing plan directly rules out raising pay, and in its resource table moves "pay raises to retain bakers" to "de-skilling the process." At the end it lists the reasons for turnover as still to be verified, without providing any revision of the already-scheduled plan for the case where pay really is the main cause.

Meta Rules, on the same issue, specifies how many people to interview and who conducts the interviews, and states plainly: if pay is significantly below market and is the main cause, centralization will not solve turnover, and salaries must be adjusted first. The function of this passage is to let new information change the original route, not just to declare that information matters.

**The Original has a "to be confirmed" list and some effective branches; its flaw is that major prescriptions can still bypass the divergences it has itself raised.**

## Operations: The Benefits of the Goal Are Fully Explained, but How Customers Get There Is Still Missing

The Original proposes a subscription for members who have bought European bread (Baseline also proposes subscription/pre-order in months 6–12; the Original moves it earlier), and fully explains three benefits: higher frequency, prepaid cash, and stable production. The relationship among the three is substantive.

But between "bought before, not coming now" and "willing to prepay and pick up regularly" lies a behavioral shift. By the Original's own supply-side diagnosis, some of these people left precisely because quality was unstable. The subscription's economics answer why the store wants such a program; they do not yet answer why customers would trust the store again and commit to continued purchases.

Meta Rules separates these: first raise visit frequency among active customers, then give specific dormancy segments reasons to return tied to their purchase history, and separately validate the subscription's fulfillment process and churn rate with a pilot at two stores with one hundred slots. This gives customer segmentation, level of commitment, and production arrangements each their own operations.

The pickup channel shows the same difference. The Original says "launch pre-order pickup through your own channel" and explains the convenience, margin, and face-to-face contact. Baseline had already specified LINE, pre-order pickup, and a discount entry point. Meta Rules goes further, arranging the pricing basis, cards in delivery packaging, QR codes, staff prompts at checkout, and phased rollout.

These details are what carry people from one channel to another. The Original keeps the name and benefits of the channel shift, but leaves the user to reinvent the entry points, incentives, and reception.

**This is a goal written as an action**: carrying out an instruction requires the executor to already have exactly what they lack. The Original writes "the properties of success" as "the action to take now," while the operation that would actually produce success is still not generated.

## Operations: Recombining a Problem That Could Already Be Split into a Strategic Dilemma

At the end, the Original asks the company to choose between "efficiency at scale" and "quality scarcity," saying the two directions take completely opposite stances on central production. The choice is presented as a fundamental strategic question that must be answered soon.

This dilemma, however, had already been split apart in the other responses to the same task. Baseline sends basic items to frozen-dough suppliers and states that signature items remain in-house; but this boundary also puts standard European bread on the outsourcing side, while standard European bread is exactly what customers who choose a European-bread chain buy most, so frozen outsourcing flattens the quality gap right there (the audit in [Test 1](Test-1：operations-diagnosis-baseline-vs-meta-rules-under-high-specification-prompting.md) works this through in full). Meta Rules grades more finely: signature European bread, where brand identity lives, keeps high-skill production and is centralized in the company's own production hubs; standardized items such as white bread and dinner rolls are outsourced; items suited to direct sourcing are purchased.

These arrangements let different activities carry efficiency and differentiation respectively. The Original's prescription has no grading: it suggests first having a third-party contract manufacturer "trial 3-5 core SKUs" in frozen dough, and the task's core product line is precisely the European-style bread series — the category the Original's own diagnosis calls "the most technique-dependent and the least able to hide flaws." Only at the end does it raise a dilemma that would change the direction of centralization, without connecting it back to item selection and the production plan.

So value that could be handled by dividing up activities is turned back into an either-or choice for the whole company; a problem that could have started with an item inventory and a division of production falls back to "what kind of company do we want to be."

This point doesn't just lack operations; it **adds a decision burden that could have been dissolved by breaking it down**. The level of abstraction rises while the available solutions actually shrink; the problem looks more fundamental, yet the user ends up further from the next well-grounded action.

## Operations: Numbers and Time Need Not Only to Appear, but to Keep the Same Identity

Several places show this carry-through problem further.

**Gross margin estimate.** Holding the two channel margins fixed, a ten-point rise in delivery share lowers the blended gross margin by about 3.4 percentage points; multiplied by NT$280M, that is about NT$9.52M (NT$280M × 10% × (52% − 18%)). As a mix decomposition of the margin rate, this calculation holds. But the Original calls it the "direct cost" of the channel shift, and as a monetary figure that presupposes this delivery revenue would otherwise have occurred at in-store margins — that is, substitution. Substitution is exactly the question the Original raises a few lines later in the same mechanism and puts on its to-be-verified list. Baseline's identical NT$9.5M was calculated under "if true," conditional on substitution.

The Original then stacks a raw-material increase of about four percentage points on top, arriving at an annual gross margin decline of six to eight percentage points, NT$17–22M, and writes in bold that real profit "may already be near breakeven or negative" (followed by a note that this needs confirmation against the income statement). This stacking assumes none of the raw-material increase was passed through to prices; the Original's to-be-verified list asks for the transaction value increase to be broken into price increases, category mix, and items per basket, yet the price-increase component never makes it back into its own erosion estimate. Meta Rules directly sets its same-store transaction value estimate against the raw-material increase ("You haven't even fully passed through costs"). The misstep lies in the step where a scenario estimate is assembled into a statement of fact.

**Store closure judgment.** The Original calls for full store-level P&Ls including allocated HQ costs, but at the decision point switches to an undefined "contribution margin," and says a store already losing money should not be renewed. P&Ls before and after HQ allocation lead to different closure judgments. Baseline at least spells out the deductions in a four-wall P&L; Meta Rules further separates contribution before allocation from net profit after allocation, pointing out that HQ costs that won't disappear when a store closes cannot be treated as savings from closing it.

**New-store timing.** The task says the new stores have been open six months, yet the Original sets the keep-or-close point at "months 9-10 (one full year since opening)." If these are plan months, the stores would already be 15–16 months old; if they are store ages, the stores would not yet be a year old; one full year since opening actually falls in plan month 6. Plan months and store age are mixed together. Meta Rules writes explicitly that T+3 months is month 9 of operation, then continues, downsizes, or exits. Only when time becomes a single axis that can be calculated along does it actually constrain action.

**Interview cost.** The Original's closing asks for all bakers who left in the past twelve months to be interviewed within a week, calling the cost near zero. Reaching them, scheduling, getting honest answers, sorting out disagreements, and rewriting the prescription are all folded into "finish interviewing." The operational resolution the response saved is converted into the user's workload, and then hidden behind a claim of zero cost.

These are not scattered small mistakes. The calculation basis of the data, the substitution and pass-through premises, whether costs can actually be saved, where time is counted from, and who bears the human hours all change whether the plan can be carried out.

## Operations: Leverage Points Baseline Had Found Did Not Appear This Time

The Original's operations response is about a fifth shorter than Baseline's, yet its mechanism narrative is more concentrated: three middle-layer mechanisms and three underlying root causes. Compared with Baseline, several leverage points did not appear this time.

Waste is completely absent. Baseline calls the waste rate the biggest gap in this dataset, points out that waste spikes when traffic falls and production planning is not adjusted, and schedules it in the first month's audit; Meta Rules expands it into daily logging, production baselines, and automatic downward adjustments. The Original diagnoses the traffic decline and unstable European bread supply, but never connects them to production volume and waste.

B2B, group purchases, and corporate orders are also absent. Baseline judges them the bakery industry's best channel for margin and cash flow, even though it schedules them in months 6–12; in a cash-tight situation, the Original's only source of prepaid cash is the member subscription.

Delivery pricing stops at a direction. The Original asks for "channel-separated pricing" that reflects the platform commission; Baseline had already given a 15–20% delivery menu price increase with expected margins, and Meta Rules adds a two-store, four-week pilot with an order-volume-decline threshold for deciding whether to roll out company-wide.

Execution-level organizational issues likewise do not appear. Baseline asks whether 180 people across 12 stores have an operations supervisor or area manager layer; Meta Rules assigns lease and new-store decisions, margin repair, production and talent, and finance and gates to four management roles; the Original's actions do not specify who drives them.

These absences differ from the member frequency and basis reconciliation problems above: they are not miscalculations, but leverage points Baseline had found and the Original did not find this time. Among the five requirements, the heaviest weight falls on critical analysis and connections between concepts; the Original concentrates its shorter length on mechanism explanations of "why this is happening," and the operational parts of "what gets it done" — waste, order-based channels, pricing magnitude, and division of organizational labor — are squeezed out of the answer.

## Operations: Real-World Timing Is Understood as a Risk, but Could Also Become a Resource

The Original does mention that a higher cake share amplifies dependence on holidays, peak-and-trough gaps, and cash swings. This goes beyond simply organizing the task data and is valuable situational understanding; Baseline did not raise this point.

But the Original's timeline is entirely relative (days 0–30, months 1–3, months 4–12), and holidays appear only as a risk; Baseline likewise has no real dates at all. The Meta Rules response of 2026-07-25 states "Today is late July 2026," then connects the calendar at that moment to pre-orders, packaging lead times, corporate contact lists, and prepayment arrangements, turning holidays into an early source of cash and using that cash to support the subsequent lease and production restructuring.

Apply the same lens to this test's date, 2026-09-13: the Moon Festival falls on September 25, less than two weeks away, too late to launch pre-orders; the pre-order windows for Christmas and Lunar New Year, however, are just opening, and in timing they line up with the cash needs of lease negotiations and production restructuring. The Original sees holiday volatility but connects no real holiday into its plan.

This difference continues the observation from the resume task: higher gains can come from creating the conditions for success, not just from pointing out constraints. After seeing the timing and seeing the capability gaps, whether a response goes on to search for operations that could change the situation is the next level of quality.

## Looking Back from the Deliverables: How the MetaSPO Original Works

### Every Quality Direction Lands Somewhere, but Often Counts as Done After One Place

Most of the Original's quality directions can be matched to concrete work in the deliverables: item 1's critical analysis corresponds to the data contradiction and the low base, and its relationships and connections between concepts correspond to category, frequency, and fixed costs; item 2's query-type adaptation corresponds to reordering the resume for recruiter reading and forming a phased plan for operations; item 4's clear structure corresponds to the resume summary and the layered operations analysis; item 5's contextual adjustment corresponds to brand-side positioning, the lease, and cash. Item 3's emotional assessment has no landing point of its own; an assessment like 綠田's "a great growth rate, but the base is low," which sets positives and negatives side by side, is the trace it leaves in this response.

The problem is that when a direction produces decent work in one place, later positions of the same kind do not keep carrying it. 綠田 gets a background check on its numbers, but other important results and the model's own added claims do not get the same treatment; frequency enters the diagnosis, yet the member estimate loses it; interviews are designated as a precondition for decisions, yet the pay-raise option is ruled out in advance.

The cause lies in how the requirements are written. MetaSPO writes each quality as one clear requirement sentence, and each sentence appears only once in the text. This style strikes both humans and models as explicit, but it also offers an easily recognizable finish line: as soon as the response contains a passage that shows critical analysis, relationship analysis, or contextual consideration, the requirement looks completed and does not come back to constrain each later judgment.

The place to judge, therefore, is not "was it ever done," but whether what was obtained keeps changing later choices.

### The Problem Is Not the Absence of Requirements, but That They Are Not Carried All the Way

The Original's prompt asks for precision, coherence, and adjustment to context, and the response does produce relationships and some conditional branches.

The gap is that these directions do not act together at the key transitions. When the sense of scale is amplified, the chosen value is not tied to annual data; when "no bought followers" is rewritten as "purely organic growth," the claim is not tied back to the means the user described; when customer overlap is used to explain channel loss, the substitution relationship is not tied to behavioral change; when a strategic dilemma is produced, efficiency on the production side and quality on the brand side are not broken into activities that can be divided up.

Two questions help identify this kind of break: does what the previous section produced become a condition of the next section? Does a new finding in a later section go back and correct an earlier one? The many breaks in this test all get stuck on these two questions.

This also explains why looking at a single quality requirement overestimates how much it delivers. "This requirement exists" in the text, "a corresponding piece of work appears once" in the response, and "it keeps constraining and driving" the whole are three different levels.

### The Force That Builds Relationships Needs a Matching Force That Checks Them

The Original's analysis is not without depth. It can connect the loss of high-frequency customers, the category shift, and fixed costs into an explanatory structure; precisely because of this, numbers that dropped their conditions, simplified causal verdicts, and prematurely excluded options are more easily absorbed into the overall narrative.

A single requirement on its own gets satisfied in the least effortful, most visible way. "Multiple perspectives, logic, connections between concepts" drives the model to connect things, but no other requirement checks whether the connected relationships have evidence, whether there are other explanations, and which later judgments they affect. When relationships are built faster than they are checked, the result is a causal story that is more complete and harder to catch in error.

Checking here also includes improving upward. For example, the tension between efficiency and quality can trigger a division of activities that opens up more viable solutions; doubts about job-search capability can trigger case reconstruction and new work samples that increase feasibility. Effective verification does not just lower commitments; it also changes the approach, giving a better goal a path to reach it.

### When Goals Are Written as Actions, the Professional Threshold Is Left to the User

The resume's "explain how you plan to fill the gap," and the operations response's "pulls low-frequency customers back to high frequency," "concentrating staff (especially bakers) in high-potential stores," and "finish interviewing the bakers who left in the past 12 months" all place unfinished judgments inside action sentences. The more familiar a reader is with the domain, the more easily they fill in the method while reading, and so overestimate the operations the answer has actually provided.

Seeing this gap clearly requires separating two kinds of work: which are raw facts only the user knows, which the model cannot reason its way to; and which are professional breakdowns, criteria, examples, and concrete arrangements that the model could have done first?

The Original hands part of the latter back to the user as well. It can tell people where the finish line is, but does not lower the professional threshold for reaching it. This gap cannot be closed by "you can always ask a follow-up," because the user would still need to know which part is missing and what kind of answer would count as filling it.

### The List Format Reinforces Item-by-Item Box-Ticking

The Original prompt is presented as five numbered objectives, and each item already links multiple perspectives, logic, and conceptual relationships, so they are not five fully sealed boxes; but the numbered-list format itself reinforces local completion. A layout that reads like a rules document leads the model to treat each item as an independent checklist entry, handled one by one, at equal depth, following a template, and ticked off once done. The shape of the Original's responses — every requirement gets one decent piece of work, yet the pieces rarely correct one another — is exactly what item-by-item box-ticking leaves behind.

[Test 7](Test-7：metaspo-prose-rewrite-carry-through-and-quality-differences-in-descriptive-prompting.md) rewrites the same quality directions as prose, directly testing how numbering, wording, scope, and the organization of requirements change quality together.

## Thinking Textures Shared with Test 7

[Test 7](Test-7：metaspo-prose-rewrite-carry-through-and-quality-differences-in-descriptive-prompting.md) runs the same model on a paraphrased version of the prompt that rewrites MetaSPO as prose. It is a separate run: not a single generated sentence is shared with this test, and the paraphrase's operations response is nearly half again as long as the Original's here. Yet the two responses repeatedly show the same patterns at the same kinds of positions. The wording of any single generation is random; a pattern that recurs across two runs and two ways of writing is the signal design can use. Both prompts write the desired qualities directly as requirement sentences, and the following three textures are what they leave behind in common.

### Texture 1: Checks Point at the Input, Not at the Model's Own Claims

The Original here checks the 綠田 numbers the user supplied, yet turns "no bought followers, mainly through Reels and KOL collaborations" into "purely organic growth," "~20 people" into "over 20 people," and "I wrote the entire digital transformation marketing strategy" into "independently planned." The paraphrase, in the same resume, turns the same line into "no follower growth ads deployed throughout," and ROAS "averaged" into "steadily maintained." "No bought followers" becomes three different claims across Baseline, the Original, and the paraphrase, all of them stronger; only Meta Rules writes "growth driven entirely by organic reach and partnership-driven traffic."

Both prompts make the input the object of critique: the Original says "Assess the provided data," the paraphrase says "Critically analyze the information provided"; the only sentence aimed at the answer itself asks, in both, for clear and precise presentation. The model therefore scrutinizes the task closely but not the words it adds itself. The Meta Rules response lists its own verb upgrades as the single largest unverified assumption, and the difference comes precisely from Meta Rules containing checks whose object is the model's own generation.

### Texture 2: Conditions Fall Away as Estimates Travel Downstream

The Original's same-store visit decline of "about -13%" rests on "same-store transaction value is likewise +12%," yet by the delivery section it has become "visits down 13%"; NT$9.5M is written as the direct cost of the channel shift, and the substitution premise does not travel with it. The paraphrase takes "delivery prices are completely identical to in-store prices," reverse-engineered from an assumption, as the basis for a price increase, and "the baker freed up by closing one store may be exactly what is needed to restore full hours at the two stores currently operating on shortened schedules" becomes, in the resource section, "prioritize redeployment to the two stores operating on shortened hours."

Meta Rules makes a similar inference on the same task, including suspecting that delivery prices haven't been marked up, but writes it as a hypothesis, attaches a ten-minute menu comparison, and holds the related recommendations until confirmation. Texture 2 is not an inability to estimate; it is that nothing in this kind of prompt asks: when an estimate is carried into the next step, is its premise still there?

### Texture 3: The Verification List Sits Alongside; the Prescription Is Not Rewritten

The Original says departed-baker interviews will determine "whether the next step is raising pay or changing processes," yet its staffing plan has already ruled out raising pay; it recognizes that the type of role changes how the resume should be written, yet hands the choice back to the user. The paraphrase lists whether the European bread decline is demand-side or supply-side as "the single highest-priority validation," yet its category strategy is already fixed as "My judgment is defend"; it says waste is larger than the impact of any single action item, yet ranks waste in the third tier of its verification list.

The task asks for a hypotheses section, and both responses deliver one; under this kind of prompt, delivering the section is where the requirement counts as completed. Meta Rules uses verification gates and "do not execute corresponding recommendations until the first three are verified" to connect the list to action, which is what gives later findings the authority to rewrite earlier sections.

### What These Textures Show

The paraphrase is clearly stronger than the Original here at local integration, yet not one of the three textures disappears. Moving from a numbered list to prose, merging sentences, and loosening the emotion condition move the model's quality in the "pushing forward" direction; checking the claims it adds, keeping premises attached to results, and letting later findings rewrite earlier sections are all "looking back" work, and neither prompt has a single sentence that takes them as its object.

This document's earlier observation about "item-by-item box-ticking" shows where the Original completes things locally; these three textures show which breaks remain even after the list format is gone. Changing them requires a prompt to contain requirements whose object is the model's own generation: check added claims, reconfirm the premise when citing an estimate, and let new findings go back and rewrite what has already been written.

## What This Test Means

### A Universal Prompt's Effectiveness Has Direction

The MetaSPO Original shows gains over Baseline in the resume's reading entry point, the context check on 綠田's numbers, and the CRM view, and in the operations response's opening sequence, cash-flow premise, and seasonality risk. It also retains many of Baseline's existing capabilities. At the same time, it regresses on cross-departmental evidence, confidentiality and level-gap reminders, product division of labor, the substitution verdict, basis reconciliation, waste, and B2B channels, and introduces errors in the member calculation, new-store timing, and unsupported resume claims.

| Task | New relative to Baseline | In Baseline, absent from the Original this time | The Original's errors and failures to carry through |
|---|---|---|---|
| Resume | Professional summary; low-base warning for 綠田; CRM / retention gap | Concrete recall prompt for cross-departmental work; NDA reminder; team size and rewrite path | "Over NT$24M" chosen from the upper half of the range; "~20 people" written as "over 20 people"; "independently planned," "replicable D2C growth model"; "purely organic growth" (carried over from Baseline) |
| Operations | Lease and delivery bleeding-control in the first stage; cash flow statement and credit lines as a premise; seasonality risk from the higher cake share | Check showing neither basis reconciles; delivery before/after traffic comparison; LINE and discount entry points for pickup; delivery markup magnitude; boundary between basic and signature items; waste; B2B / group orders; middle management | Member revenue missing frequency; -13% turned from estimate into fact; "direct cost" without the substitution premise; raw-material erosion without pass-through; core European bread sent to a contract manufacturer first; new-store timing mismatch; interview cost |

What this test yields, then, is a profile of quality change: which dimensions moved forward, which capabilities did not move, and which positions lost carry-through. Compressing all of this into "effective / ineffective" would throw away the information with the most design value.

### Design Understanding to Take Away from These Differences

| Observed phenomenon | Mechanism behind it | How to use it in design |
|---|---|---|
| Numbers get checked, but numbers of the same kind and the model's own added claims are not checked consistently | A requirement written as one clear sentence, appearing once, feels discharged after being done in one place | The same quality needs to recur at different stages, phrased in different ways, to keep acting |
| Frequency is discussed but missing from the formula; a conditional estimate becomes a present fact | When a later section cites an earlier section's product, the conditions don't come along | Require later sections to take earlier products as conditions, and let new findings rewrite earlier sections |
| The causal narrative is more complete, and wrong verdicts look more like natural conclusions | A requirement that drives relationship-building has no matching requirement that checks relationships | Every driving requirement needs another requirement responsible for catching the form it takes when satisfied superficially |
| Higher professional requirements are raised, but how to meet them is left to the user | Only the finish line is written; facts only the user knows are not separated from analysis the model can do first | Judge acceptance by whether the user can start after reading, not by whether the requirement was mentioned |
| Efficiency and quality are turned back into an either-or choice | Abstraction merges activities that could be divided back into a single overall choice | First question the premise that "it has to be one or the other," break the whole back into activities, then allocate |
| Meta Rules advances with case studies, diagnostic work samples, branching, and resource arrangements | After seeing constraints, it keeps searching for operations that could change the situation | Higher gains come from creating the conditions for success, not only from pointing out risks |

These comparisons connect the different surface phenomena of the two tasks to one set of design questions: how local quality gains lasting effect, how the conditions of an earlier step are inherited, how new information from a later step rewrites existing choices, and who bears the final stretch of cognitive work. Readers who want to dig into the principles behind these mechanisms can read further in the [Prompt Design Memorandum](../../prompt-design-memorandum.md).

"A goal written as an action" shows up in three ways in this sample: the other responses to the same task had already written out the method, while this time only the goal is written (the pickup channel, the member subscription); an investigative action is written as an already-completed solution ("finish interviewing," "near-zero cost"); and a neighboring but distinct form — recombining a problem that could be split into a strategic dilemma, which does not pretend to offer a path, but instead adds a decision burden that could have been dissolved. These distinctions can be used directly in later design and analysis.

### Connection to Test 7: How an Understanding Formed Under Meta Rules Becomes Another Prompt

[Test 7](Test-7：metaspo-prose-rewrite-carry-through-and-quality-differences-in-descriptive-prompting.md) takes up the earlier prose rewrite and its two test responses, analyzing differences in carry-through within descriptive prompting. It also has independent value: that prompt was originally produced by an AI under Meta Rules, which, after reading the relevant documents, paraphrased its own understanding of the original. A previous version of this test mistakenly used that paraphrase as MetaSPO's original text; this version reruns the test with the paper's original text, and the paraphrase and its two responses are re-analyzed in Test 7 as the paraphrased version.

This makes "understanding the original" itself an artifact that can be analyzed. Which relationships in the original text did the AI under Meta Rules carry over while understanding it, and which work did it add because it considered that work self-evident? Which of these understandings actually made it into the paraphrase, and which existed only in how the reader was operating at the time? When the original and the paraphrase are each given to the model under test, where do the differences in the deliverables fall?

Test 7 therefore has a dedicated section, "How Understanding Under Meta Rules Enters the Paraphrase," compared against the Original's actual results. What it tracks, beyond the effect of turning requirements into prose, is **how much of the way the reader works can be realized by another executor through a paraphrase**.
