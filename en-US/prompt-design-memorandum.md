# prompt-design-memorandum
> **Positioning**: Not activated by default; activated only when explicitly requested. This skill is a domain-specific professional baseline attached to Meta Rules. It does not replace fractal recursion or global constants, but provides cognitive anchors within this specific domain — raising the cognitive floor of recursion rather than setting a procedural ceiling.

> **Principle**: Not an execution manual — after understanding core mechanisms, derive professional criteria from mechanisms when facing concrete design scenarios, rather than looking up corresponding paragraphs and citing conclusions as a shortcut past reasoning. When reading, attend not only to individual entries but to the structural relationships between them. When facing concrete problems, mechanism descriptions are the starting point of reasoning, not the endpoint — conclusions derived from mechanisms must be independently supported by the problem at hand; "§X already describes this mechanism" does not constitute argumentative closure.

## 1. Core Mechanisms
> **Epistemological positioning**: This chapter describes mechanisms grounded in transformer attention computation, supplemented by analogies (field, gravity, entropy, phase) to accelerate intuition-building. The validity of analogies lies in structural isomorphism — design derivations should stop at the boundary of structural correspondence and not extrapolate along the analogy's source domain. When an analogy conflicts with a computational description, the computational description takes precedence.

### 1.0 Unifying Principle
> All subsequent analogy terms can be reduced to computational mechanisms through these three propositions. Parenthetical computational correspondences are provided for immediate reduction.

The entire design essence of Meta Rules is the engineering of **cross-layer functional differentiation utilization** and **cross-step dynamic activation routing** of pre-cached tokens in the KV cache.
Three atomic propositions form the derivation base for all subsequent mechanisms:
**Proposition 1: Zero-marginal-cost continuous participation.** All Meta Rules tokens are encoded during the forward-pass pre-computation phase as independent K (Key) and V (Value) vector pairs per layer, then cached. In each subsequent generation step, every attention head in every layer automatically computes attention weights over all cached KV pairs. Meta Rules tokens do not need to be "invoked" — they are always present; only their activation intensity varies dynamically with context. The design starting point is not "what instructions to write" but "what K and V vectors to pre-store in the candidate pool."
**Proposition 2: Vertical functional differentiation.** Each layer has independent projection matrices; the same prompt token presents different K/V facets across layers. Lower layers extract semantic tags, middle layers extract pairing functions, higher layers extract abstract relations. The same cached token is utilized by different layers in different functional roles along the vertical dimension — the core quality metric of design is not token count, but the number of vertical functional differentiation layers utilized per cached token. Tokens with rich semantic stratification (e.g., "intellect" can differentiate into discernment / judgment / critical standards) are superior to semantically flat tokens (e.g., "analyze" extracts highly similar facets across layers).
**Proposition 3: Directional accumulation in the residual stream.** Each layer's attention output is additively superimposed onto the current representation via residual connections. A single token's V injection is a directional nudge, not a replacement — changing the generation direction requires V injections from multiple tokens to form directionally coherent accumulation in the residual stream. Token A's V injection at layer L nudges the representation direction, causing layer L+1's Q to have a higher dot product with Token B's K; B is more strongly activated; B's V further nudges the representation — this chain completes vertically within a single forward pass, consuming zero generation steps. The computational necessity of field structure lies here: in a flat list, each instruction's V direction is incoherent, and accumulation is destructive; field structure ensures directional coherence through coupling, producing constructive accumulation.

### 1.1 Driver Operating Level
As persistent members of the KV cache, Meta Rules tokens participate in attention computation at every layer of every generation step (Proposition 1). Their efficacy is not one-shot semantic transmission of an instruction, but continuous probability landscape shaping — at each generation step, the dot products between Meta Rules tokens' K vectors and the current Q determine which V vectors are injected into the representation; these injections cumulatively shape the landscape of the token probability distribution.
Word choice affects not only semantic content but three computational parameters: the token's K-vector directional sharpness (high selectivity: strongly activated only in specific situations, rather than uniformly moderately activated for all Q), V-vector displacement magnitude (the degree to which V injection nudges the representation direction), and semantic stratification richness (the degree to which different layers can extract different functional roles, per Proposition 2). The product of these three determines a single token's landscape-shaping power.

### 1.2 Semantic Field Gravity
A well-designed prompt forms a semantic field (multiple cached tokens' K vectors surrounding the target behavioral domain from different directions in embedding space) — each sentence's actual constraining force = literal semantics + the joint pressure range under whole-field resonance. The same sentence carries different weight inside versus outside the field.
Force mechanism — multi-constraint feasible region (attention weight competition under softmax): deviating from the expected behavior means Q drifts away from the target domain; at that point, multiple Keys' K vectors maintain positive dot products with the drifting Q from different directions, jointly claiming high weights in softmax, and their combined V injection pulls Q back. The essential difference between field structure and flat lists: in flat lists, each instruction's K direction converges, causing mutual dilution in softmax; in field structure, K directions are diverse yet jointly surround the target domain, producing mutual reinforcement. **Directional diversity matters more than instruction count.**
Jurisdiction expansion: abstract principles' jurisdiction within the field far exceeds their literal scope. "Supported by logic" doesn't only constrain "reasoning must be logical" — it establishes a baseline state of "all entrants to the field are subject to logical audit." The principle's wording defines direction; the field's structure expands its jurisdiction. (Computational layer: abstract principles' K coverage is inherently broad, producing positive dot products with any reasoning-related Q; field structure ensures V injection directional coherence, so jurisdiction naturally expands.)
Audit discipline: analyzing a Gestalt system by atomizing it sentence-by-sentence systematically underestimates coverage — this is the most common audit error. Correct method: first identify all nodes within the field semantically related to the target (cross-layer), then assess their joint radiation range (whether the directional distribution of K vectors surrounds the target domain).
The dual of coverage underestimation is risk overestimation — "gaps" or "weaknesses" identified through atomized analysis are often already covered by multi-path redundancy that crosses analysis-unit boundaries. The complete path from audit finding to iteration decision: isolated risk identification → recontextualize within overall operation → identify compensatory mechanisms (cross-layer field effects, persona V bias, response format backward pressure, etc.) → assess the joint probability of all compensatory mechanisms simultaneously failing → drive iteration decisions by "system failure probability" rather than "node failure probability."

### 1.3 Multi-Scale Redundant Encoding
When the same instruction appears at different abstraction levels with different wording, it forms a semantic cluster rather than a single point in embedding space — multiple K vectors occupy neighboring but distinct directions, so Q arriving from any angle hits at least one cluster member. This is the computational benefit of fractal self-similar structure: not repetition, but multi-angle capture.
Relationship to semantic field gravity: redundant encoding is the microscopic mechanism of the field (multi-directional capture of a single instruction); semantic field gravity is its macroscopic emergence (joint surrounding by multiple instructions).

### 1.4 Model Tendencies and Phase Scheduling

#### Core Design Challenge
Model behavioral tendencies — shortest-path preference, coverage instinct, compliance, boundary awareness — each simultaneously carries cognitive functional value and runaway risk; the two are inseparable. Shortest-path preference is both the engine of efficient navigation and the risk source for skipping verification. Coverage instinct is both the supply of divergent material and the risk source for substituting breadth for depth. Compliance is both the substrate for accepting evidence-based correction and the risk source for judgment surrender. Boundary awareness is both the raw material for risk assessment and the risk source for decision paralysis.
These tendencies manifest in attention as directional biases of the Q vector — shortest-path preference causes Q to tend toward alignment with conclusory tokens' K; coverage instinct causes Q to tend toward alignment with the next uncovered topic's K; compliance causes Q to tend toward alignment with the most salient tokens' K in the user input.
Meta Rules doesn't teach new capabilities, nor suppress biases — it performs phase scheduling on existing biases: at different generation phases, different Key sets compete with Q's bias direction for attention weight, pulling Q from the bias direction toward the direction needed in the current phase. There is no reason to downgrade the design for lower-tier models; weakening the drive on higher-tier models to accommodate lower-tier ones is a net loss.

#### Activation Mechanism
Training traces are indexed by structural patterns (not literal content). Familiar structures in the prompt (entropy cycles, causal sequences, reflective loops) resonate with high-quality reasoning patterns in training data, activating corresponding parameter regions — the semantic field's efficacy is fundamentally high-density structural resonance. The efficacy of architectural prompts is difficult to explain at the level of individual instructions — the efficacy carrier is the resonance density of structural patterns (the geometric structures formed by multiple tokens' K/V vectors), not the semantic content of instructions.

#### Phase Scheduling Mechanism
Fractal recursion's phase structure provides temporal windows for Q bias — the same bias is allowed to dominate Q direction in the phase where its functional value is highest (corresponding Keys don't compete against it), and is suppressed by Meta Rules' Key set in the phase where its runaway risk is highest (corresponding Keys win the attention competition with higher Q·K dot products). The designer's task is to identify each bias's functional-value window and runaway-risk window, then deploy Keys with sufficient directional sharpness to win in the latter.
This mechanism and §1.7's dynamic routing are the same principle applied to different objects: §1.7 describes conditional activation of Meta Rules' own Key set; this section describes the attention competition between Key sets and the model's native biases.
Design corollary: escape containment (§5) is not suppressing the bias itself, but deploying competing Keys that can win within the bias's runaway window. Containment strength has an upper bound — if a K vector too aggressively suppresses a certain bias, it prevents that bias from dominating Q direction even in its functional-value window.

### 1.5 Coupled Entropy Cycles and Structural Self-Reference
Each layer contains its own diverge→converge cycle; nesting of layers constitutes larger cycles; cycles are coupled through shared parameters.
The computational carrier of coupling (design-layer application of Proposition 3): shared parameter words (e.g., "completeness") appear at multiple positions, each position's K/V pair participating in different phases of attention. After V injection nudges the shared word's semantics into the residual stream, subsequent layers' Q produces higher dot products with the same shared word's K at another position — the shared word becomes the directional coherence guarantee of the residual stream.
Design criterion: coupling strength between two Keys ≈ the consistency between A's V injection direction and B's K direction. Intuitive proxy: "After fully understanding A, is B the natural next thought?" — this criterion is closer to attention's actual behavior than "Are A and B semantically related?"

#### Core Emergent Benefits
- Parameter penetration amplification: high-level shared parameters' V vectors are referenced by K at multiple positions simultaneously; a modification at one point propagates to all coupled nodes through residual accumulation
- Cross-scale fault tolerance: when a micro-cycle's Key fails, the same shared parameter's K in the parent cycle still applies directionally coherent nudges
- Escape attenuation: with each completed cycle, the accumulated directional anchoring in already-generated tokens thickens, requiring progressively larger Q direction changes to deviate — deeper recursion is safer, not more dangerous

#### Capability Synthesis
The observable emergent effect of coupled chaining: V injections from multiple cached Keys accumulate directionally in the residual stream; chained activation produces cognitive capabilities not described by any single Key. For example, "cross-domain structural mapping" requires no dedicated Key — "knowledge completeness" guides cross-methodology search → "divergence domain expansion" challenges within-domain constraints → "value increment" reframes the problem → the emergent effect of this three-way chain is cross-domain mapping.
**Reliability boundary between first-order and second-order synthesis**: In first-order synthesis, all chain links are prompt-cached tokens (K/V directions are stable, always present); reliability is guaranteed by design. In second-order synthesis, intermediate links include emergent products of generated tokens (K/V directions are task-dependent random variables); reliability is outside the designer's control. Design should rely only on first-order synthesis — using emergent products as chain links means building reliability on an uncertain foundation.
Design implications of synthesis are in §3.3.

#### Cycle Map (Universal Base Reference)
> The following is the cycle structure of the current universal base, provided for locating intervention points during design modifications.
**Macro global cycle** (Meta Rules as a whole):
Identity declaration (maximum divergence — defines the possibility space) → Cognitive disposition & reasoning discipline (bias orientation — converges into cognitive style and reasoning standards) → Fractal recursion (instantiates style and standards into steps) → Response format (crystallizes steps into verifiable output)
**Meso structural cycles** (internal sequences within each block):
- Cognitive disposition and reasoning discipline's paired structure: two pipelines with sentence-by-sentence positional pairing — each pair covers the same cognitive pipeline stage but is semantically orthogonal: disposition defines the cognitive character of that stage (how to act), discipline defines the reasoning standard of that stage (how to judge). Their K directions fall in the cognitive-character domain and reasoning-standard domain respectively; positional pairing ensures that character and standard at the same stage form complementary surrounding in attention rather than softmax dilution.
  - Cognitive disposition pipeline: eight sentences sequentially covering perception → thinking → reasoning → retrieval → decision → problem-solving → error correction → expression, converging from open perception to dense output.
  - Reasoning discipline pipeline: eight sentences sequentially covering premise grading → target orientation → path validation → value assessment → position support → effectiveness definition → error correction → density standards, converging from input quality to output density.
- Fractal recursion: deconstruction (open exploration) → analysis (iterative diverge-converge) → decision (closure judgment) → outlook (observing impact based on provisional decisions) → recursion (audit → restart)
- Response format: Core Decision → Research Plan → Intent-Optimal Solution → Advanced Gains (local re-divergence) → Self-Critique (negative feedback) → Next Steps (controlled re-opening)
- Internal to analysis: diverge → converge → verify → (if failed) re-diverge; termination conditions gated by decision
**Micro self-contained principle**:
Elements at every level contain their own diverge→converge cycle. Each persona sentence diverges in the first half and converges in the second half; Keys open search dimensions (diverge), deliberation prompts provide judgment templates (converge); dimension sequences form entropy increase from hard to soft, or entropy decrease from broad to narrow. When designing or modifying, verify that this principle is maintained at the target level.

### 1.6 Key's Attention Probe Mechanism
Keys (deliberation prompts) are reasoning scaffolds pre-stored in the KV cache — at a fixed input-token cost, they provide attention targets in the hidden-layer vertical processing of each generation step that would otherwise require consuming output tokens to establish.

#### Replacement Mechanism and Computational Advantage
Without Key guidance, a metacognitive check requires the model to complete three steps on its own: counteract the current Q bias's momentum to produce a direction switch, construct the check question (generating new tokens as attention targets), and execute the check. The first two steps are costly and often fail to occur due to Q bias inertia — when the model is generating at full speed along a bias direction, spontaneously jumping out requires generating tokens sufficient to change Q direction, and those tokens themselves need to be generated first.
Keys pre-load the first two steps into the KV cache (Proposition 1); their K vectors provide competing directions within Q bias's runaway window; the deliberation prompts' V vectors compress the third step from open search to a judgment template. The model completes the direction switch directly using cached K/V in hidden-layer vertical processing (Proposition 3), without consuming output tokens.

#### Deliberation Prompt Sentence-Type Design Spectrum
The sentence type of a deliberation prompt determines its K-vector directional sharpness and V-vector injection effect; there is a design spectrum of too-narrow / just-right / too-broad (characteristics and criteria for the three zones are in the §3.1 table).
Design criterion: a deliberation prompt's K-vector direction should be narrower than the overall semantic domain of its phase (otherwise it loses selectivity), but broader than any single task instance (otherwise it loses polymorphism). A deliberation prompt's V vector should point toward cognitive actions (verify, challenge, scan) rather than specific conclusions (one solution is superior).

#### Parallelism and Selectivity of Attention Probes
Multiple Keys' K/V pairs in a dimension list exist simultaneously in the cache. At each generation step, all Keys' K vectors simultaneously compute dot products with the current Q; after softmax, only the few Keys with high dot products receive effective weight (Proposition 1). Therefore, a dimension list is not a checklist (consuming generation tokens one by one), but a probe field (parallel scanning, selective activation, zero additional token cost).

#### Reasoning Resource Redistribution
The macro-level effect of Key probes is redistribution rather than net increase of reasoning tokens. Without architectural guidance, Q bias locks onto a conclusion direction early, and subsequent tokens glide along the same direction collecting support. With architectural guidance, Keys' K vectors continuously compete with Q, preventing early lock-on; the same tokens are redistributed to framework construction, assumption challenging, dimension refinement, and other direction switches.
Observable signature: probe-guided reasoning exhibits — cognitive state transitions requiring no thrust tokens ("let me think" and similar self-guidance phrases approach zero), scan-then-selectively-expand with depth weighted by Q·K dot product, no depth decay after direction reversal (because reversal is driven by cached Keys rather than self-generated tokens). Unguided reasoning exhibits "conclusion first, depth uniformly spread."

### 1.7 Dynamic Attention Routing
§1.1–§1.6 describe static components in the cache. This section describes how these components coordinate during generation to form an adaptive attention guidance system.

#### Three-Layer Routing Mechanism
**Phase identification** (automatic matching of Q direction drift): during generation, already-generated tokens continuously change the Q direction distribution at the current position. When Q direction drifts to high alignment with a phase description's K vector set in Meta Rules, that phase's cached tokens naturally receive higher attention weight. This is not the model "judging which phase it's in" — it is automatic matching between Q direction drift and K direction distribution.
**Dimension activation** (selective injection under softmax competition): after phase matching, multiple Keys within that phase simultaneously compute dot products with Q; softmax selects the subset most relevant to the current specific situation. This explains why dimension lists can be quite rich without overloading: at any given moment, only the subset with the highest Q·K dot products receives effective weight.
**Value guidance** (directional nudging via V injection): the activated Keys' V vectors are injected into the current representation, nudging Q direction so that the next step is more likely to activate the coupled next Key within the same phase (Proposition 3's chaining), or — when the phase is complete — drift toward the next phase's K direction distribution.

#### Conditional Activation and Orthogonality of Cognitive Posture
Meta Rules defines a Q direction bias system for "how to process any task," not concrete instructions for "what task to process." When a task arrives, the task content tokens provide K/V in the *what* direction; Meta Rules tokens provide K/V in the *how* direction; the two occupy different directional frequency bands in attention. Therefore, Meta Rules' token cost should not be evaluated on the same saturation curve as task instructions — effective foreground load is far lower than total token count.

#### Reasoning Permeation (Response Generation as a Reasoning Channel)
The context state during response generation (Meta Rules + user input + [if present] complete thinking + already-generated response tokens) differs from the context state during thinking. The same cached Key is activated by different Q vectors, producing different V injection effects — response generation can yield cognitive actions not previously triggered. The hidden layers' expansion capacity here is natural, but bare-run expansion takes the form of parallel enumeration: directions are mutually independent; later sections don't revise earlier ones.
Meta Rules' response format converts this expansion from parallel to reasoning-progressive — filter criteria K vectors compete with Q from the first response token onward (backward reasoning pressure, §2.5); inter-section coupling makes each section's generation itself a reasoning action (§1.5); probes remain activatable within the response context (§1.6). The three jointly cause response tokens to simultaneously carry reasoning and presentation. Removing any one breaks the chain, and expansion reverts to parallel enumeration. This effect is independent of whether the model has an explicit reasoning phase — the benefit is more pronounced without one, because the response format directly compensates for the missing reasoning phase, causing opening tokens to enter the reasoning spectrum and achieve a better initial direction.
Observable signature: reasoning progression exists between response sections — later sections build on, revise, or challenge the products of earlier ones, rather than standing independently in parallel.
Readability benefit: the causal structure of reasoning leaks into the presentation surface, causing the output text to naturally carry the connective structure needed for human reading to construct a situation model — the reasoning progression where later sections build conditionally on earlier ones doubles as a cumulative path for cognitive momentum in the reader's working memory. Optimizing reasoning quality and optimizing human readability point at the same target (causal chain completeness); they do not constitute a design tradeoff.
**Reasoning permeation's efficacy ceiling**: permeation depth accumulates with generated token count — front-loaded sections (Core Decision, Intent-Optimal Solution, Advanced Gains) enjoy hundreds of steps of permeation-enhanced reasoning, and directional anchoring in the residual stream thickens accordingly (§1.5 escape attenuation). Rear-loaded short sections (e.g., Self-Critique) have a permeation budget of only a dozen or so steps; deviating from deep anchoring to a Q direction sufficient to discover flaws requires a change magnitude far exceeding what the budget can support. This is a structural asymmetry, not a capability deficit — the reasoning budget for the content being critiqued and the reasoning budget for the critique itself differ by orders of magnitude. Observable signature: the deeper the front-loaded analysis, the more the self-critique tends toward generalization ("this assumption hasn't been empirically tested"-type observations); generalized critique marks not "there's a problem but I can't articulate it" but rather "the hidden layers at the current depth can no longer find deeper flaws." This is an epistemological boundary, not a design defect — relaxing the word limit doesn't solve the problem (additional tokens expand the generalized critique rather than reaching deeper flaws).

## 2. Architecture Design Principles

### 2.1 Operator Polymorphism
Abstract wording is a feature, not vagueness. Declarations at the persona or principle layer define a type class; each task domain provides an instance at execution time. Declarations should stay at the "property" level ("supported by logic") rather than the "instance" level ("ensure algorithm correctness"). The instance level locks the K direction to an extremely narrow cross-section; the property level preserves a broad cross-section of polymorphism — different tasks' Q hit the same K from different directions, each layer extracting different V facets (design application of Proposition 2).
Core corollary: conceptual conditions require genuine understanding to fulfill; the more concrete the constraint, the easier it is to game.
Automatic instantiation during recursion: when fractal recursion self-references, the same Key automatically provides different instances at different recursion depths — "broadly incorporate implicit requirements" becomes global incorporation on the first pass, then in deeper recursion, stacked atop existing directional anchoring with pipeline-step context, "broadly incorporate" automatically narrows to incorporation within the current context. Recursion doesn't overcome directional anchoring but expands on top of it; context exhaustion is the natural termination signal of recursion.

### 2.2 Inter-Layer Leverage Asymmetry
When the execution infrastructure reaches steady state, modifying its internals yields near-zero marginal benefit. The highest-leverage intervention point shifts to the abstract end (identity/persona layer), because the steady-state amplifier propagates parameter changes through coupling (§1.5) to all recursion levels. Identity-layer tokens occupy the earliest position sequence in the KV cache, giving them the longest span of effect.
Amplification example: "aiming for completeness" at the persona layer is a slogan outside the field. Inside the field, the same shared parameter acquires K/V anchors at multiple positions through fractal recursion — deconstruction's "boundaries, information gaps" instantiates it as an inspection direction; divergence's "implicit requirements" unfolds it as a search direction; convergence's "path comparison" converts it to an elimination direction; decision's "path set sufficiency" turns it into a final review direction. A single declaration becomes a directional coherence guarantee permeating the entire pipeline in the residual stream.
Evolution strategy: iteration should occur almost exclusively at the persona/identity layer. Execution infrastructure should be treated as solidified unless a structural fracture is discovered. However, a distinction is necessary: explanatory text fine-tuning has near-zero marginal returns (it doesn't change K/V directions); control words / gate sentences retain high marginal returns even within steady state — their K-direction sharpness is high, and adding or removing one can open or close an entire attention competition pathway. What is solidified is the topological structure, not the gate configuration.

### 2.3 Fractal Self-Containment of Entropy Cycles
Every level of an effective architecture contains its own diverge→converge cycle, and nesting of levels constitutes larger cycles (§1.5). New content must contain a self-contained entropy cycle and form a coupling interface with at least one adjacent cycle (V injection direction pointing toward a neighboring Key's K direction); otherwise its K/V cannot be chain-activated, becoming an island outside the field.

### 2.4 Process-Driven Over Constraint-Driven
A constraint-driven approach ("do not do X") has K vectors that are activated with high weight only when the model is already approaching X — by then it's too late, and Q directional momentum is already large. A process-driven approach ("must pass through this cycle") has a Key set that continuously competes with Q from the outset, causing the correct path to naturally win in attention rather than being corrected after the fact. Constraint type priority: process constraints > meta-constraints (preventing constraint gaming) > output constraints (prone to provoking performance).
Boundary condition: if V directions of process Keys are highly coherent within the same phase (e.g., all Keys in a convergence phase push V toward a "complete" signal), their joint anchoring may systematically weaken quality gatekeeping mechanisms that depend on an "incomplete" signal to trigger. In such cases, gatekeeping should be placed not within the phase (where it would be overwhelmed by the pooled V forces) but at the meta-action layer governing inter-phase transitions — meta-action K operates at a higher abstraction layer and doesn't overlap in K direction with concrete-action K, allowing it to independently obtain effective weight in higher-layer heads.

### 2.5 Response Format as an Independent Cognitive Layer
The response format is not an output template but a second set of cached Keys that, in different context states (response generation vs. thinking), are activated by different Q to produce complementary cognitive actions (§1.7 response generation section). Increments observable in the response that reasoning didn't reach include: real-time self-falsification, real-time conceptual translation, and unsolicited risk warnings.
Cross-block activation: response format tokens, as cached KV pairs (Proposition 1), work not only during response generation — they also participate in attention computation during the thinking phase. When Q in thinking drifts to a situation matching the K direction of a response format filter criterion (e.g., self-critique convergence matching the "expert standards," "must not claim passage" K in the response Self-Critique section), these filter criteria are effectively activated and provide quality-standard V injection. The response format is therefore a quality anchor for the entire process, not merely a formatting instruction for the response generation phase.
Backward reasoning pressure:
- Filter criteria in the response format (e.g., "must only ask what is genuinely not derivable through reasoning" — asking derivable questions violates the filter, while not asking exposes gaps under mirror coverage) serve as cached tokens whose K vectors compete with Q direction from the first response token onward. The model, while writing the Core Decision section, already has the "sufficient to change the path" K applying directional nudges, forcing it to anticipate the final review while constructing arguments. Filter criteria are generators of reasoning depth, not filters of it.
- Backward pressure as a dual blade: Self-Critique's stringent and precise limit conditions exert backward pressure driving quality; Next Steps inherits the precision of Outlook, combined with the "must only ask what is genuinely not derivable through reasoning" filter's backward pressure driving coverage — the two exert pressure on two orthogonal dimensions of reasoning completeness.
Functional architecture of backward pressure: the strictness of filter criteria across response format sections forms a progressive chain — continuously escalating from the Core Decision section (expose assumptions) to the Self-Critique section (expert standards, sufficient to change the path). The most stringent filter criteria exert force at maximum intensity from the first token — quality assurance is achieved primarily in front-loaded sections through backward pressure, not in rear-loaded sections through defect capture. Combined with the reasoning permeation ceiling (§1.7), the Self-Critique section's function in deep analyses migrates from "finding defects" to "marking hidden-layer boundaries."

### 2.6 Design Parameter Sweet Spots
Design parameters universally exhibit three zones — the insufficient zone (efficacy hasn't formed), the sweet zone (optimal balance of efficacy and side effects), and the overload zone (side effects consume efficacy). Computational criterion: does a new token bring a new K direction (increasing the surrounding perimeter) without pushing existing tokens' softmax weights below the effective threshold? Every sentence within the field has its benefit amplified by Gestalt effects, but once the overload threshold is crossed, marginal returns turn negative.
Independent saturation curves: cognitive-posture content and task content occupy different attention frequency bands (§1.7), each with an independent saturation curve. Cognitive posture's length budget should be evaluated independently of task instructions.

### 2.7 Epistemological Positioning of Design
The architectural paradigm constructs a system that produces expected behavior (KV cache geometric structure), rather than directly describing expected behavior — structure itself carries information. The core operation is shaping epistemic disposition; the efficacy carrier is the resonance density between structural patterns and training traces (§1.4), not the semantic content of instructions. Structural features cannot be treated as simplifiable redundancy — before simplifying, one must trace their structural function (whether their K direction is already covered by other tokens).

## 3. Dimension Design

### 3.1 Key-Driven Principle
High-tier models have already internalized professional knowledge (V vectors in parameters have encoded domain knowledge). Audit dimensions need only provide Keys (supplying K direction to guide Q); the model organizes execution details on its own (retrieving corresponding V from parameters).

A Key (deliberation prompt) is itself a micro entropy cycle — the Key opens a search dimension (K direction defines the attention focus domain; divergence), while the deliberation prompt provides a judgment template (V vector compresses open search into directional judgment; convergence). Deliberation prompts simultaneously serve as reasoning-pattern demonstrations (their token sequences resonate with high-quality reasoning patterns in training data).

#### Deliberation Prompt Sentence-Type Design Spectrum
The design core of deliberation prompts is **K-vector directional coverage breadth** (see §1.6 spectrum model):

| | K Direction | V Injection Effect | Vertical Utilization | Chaining Potential |
|---|---|---|---|---|
| Too narrow | Extremely precise; activated only in specific situations | Points toward specific conclusions | Low (few layers, few steps) | Low (direction too specific to trigger general-purpose Keys) |
| Just right | Domain-level precision; activatable across multiple situations | Points toward cognitive actions | High (each layer extracts different functions) | High (action direction is compatible with multiple Keys' K) |
| Too broad | Generalized; moderately activated in any situation | Direction is vague | Medium but ineffective (perpetually low-dose) | Low (injection insufficient to change Q direction) |

Design criterion: a deliberation prompt should be a thinking sentence-type that can dynamically map to multiple concrete situations — narrower than the overall domain of its phase (maintaining selectivity), broader than any single task instance (maintaining polymorphism), pointing toward cognitive actions rather than specific conclusions (maintaining chaining openness).
Most deliberation prompts' openness should align with the entropy flow direction of their phase — divergence phases use open-type deliberation prompts (broad K coverage, V pointing toward exploration), convergence phases use focused-type deliberation prompts (narrow K coverage, V pointing toward judgment). Using the wrong type for a given phase produces Q direction mismatch.

#### Applicability Boundaries of Key-ification
The following are not suitable for Key-ification and must retain their full text: escape containment (requires sharp K direction and forceful V injection), negative anchoring (requires continuous directional competition pressure rather than selective activation), compound anchoring (a single Key's K direction cannot simultaneously cover multiple non-adjacent dimensions).

### 3.2 Adhesion as Fault Tolerance
Narrow-band semantic overlap between dimensions is a fault tolerance mechanism — when attention misses one dimension, the overlap zone of neighboring dimensions partially takes over its semantics.
Critical counter-intuitive state: excessive adhesion (high overlap) triggers semantic collapse — the model merges two dimensions into a single attention focus, and the independent core function of one is actually lost. Computational layer: when K-vector angular separation is too small, two Keys split their weights in softmax, each receiving effective injection below half of what they would receive independently. Criterion: each pair of adjacent dimensions should exhibit "narrow but present adhesion" and "non-overlapping core functions" — meaning K-direction angular separation falls in the narrow range where "each independently obtains effective weight" and "if one fails, the other can still capture missed Q."

### 3.3 Synthesis Criteria
§1.5 defined capability synthesis — emergent products of chaining existing Keys. This section answers the design-layer question: what should be a Key, and what should be left to synthesis.

#### Stating It Dilutes It
Making a capability already produced by synthesis explicit as a new Key inserts a competitor into the softmax pool whose K direction partially overlaps with the chain links. The new Key's K is the semantic mean of the chain links — it has positive dot products with each link but is less precise than any of them. In softmax, it splits weight with each link, reducing every link's effective V injection. The longer the chain, the more fatal this effect — marginal losses per step accumulate at the terminus and can cross the synthesis failure threshold. Single-step independent capabilities are unaffected, as they don't rely on chaining.
Diagnostic method: after removing the candidate Key, can the existing Keys' chained activation synthesize an equivalent capability? If yes, stating it only adds dilution.
Therefore: the necessary condition for adding a Key is that its K direction occupies a genuine vacancy in the pool — a region not covered by the existing Keys' joint radiation range (§1.2).

#### Load-Bearing Nodes vs. Terminal Nodes
Two types of synthesis products exist in the capability dependency graph. Terminal nodes — not depended upon as material by other synthesis chains — can safely be left to synthesis; even if synthesis is occasionally imperfect, the impact is limited to themselves. Load-bearing nodes — depended upon as material by other synthesis chains — must be cached Keys (made explicit), because fluctuations in their direction would cascade downstream through the dependency chain.
Criterion: the safety condition for leaving a capability to synthesis = terminal node AND all chain links are cached Keys (pure first-order synthesis, §1.5). The condition requiring explicit Key = load-bearing node, OR chain contains non-cached links (second-order synthesis risk).

#### Pool Capacity Constraint
Even if a new Key occupies a vacant K direction, the total number of Keys in the same pool has an upper bound — beyond it, all Keys' effective V injection drops below the chained activation threshold. The correct operation at that point is not adding but checking existing Keys for mergeable pairs (K directions close enough to each other yet each occupying a position).

## 4. Semantic Engineering

### 4.1 Vocabulary Functional Classification (K/V Perspective)
- Anchor words: high vertical differentiation — K extracted by multiple layers in different functional roles, V carries multi-layer semantics (fractal recursion, convergence, Gestalt)
- Trigger words: K direction aligns with high-quality training patterns, activating corresponding parameter regions — embedded as persistent directional anchors, not one-shot triggers
- Drive words: V injection significantly nudges Q direction (must, rigorously, adjudicate)
- Constraint words: K direction sharply points toward escape paths, V pulls Q back (absolutely no exceptions, strictly prohibited)
- Glue words: V injection maintains residual-stream directional continuity, preventing inter-phase Q direction jumps (building on this, accordingly)

### 4.2 Vocabulary Energy Level
Low-energy → high-energy replacement direction: low-frequency combinations' K vectors occupy more distinctive embedding positions, making them easier to stand out in softmax. However, excessively rare terms have insufficiently trained K/V, leading to directional instability. The balance point: precise but not obscure.
The criterion is "does the new word's K direction point more sharply at the target functional domain than the old word's?" — this must not degenerate into stylistic preference.
Examples: touch upon → penetrate; analyze → scrutinize; carry out → implement; assess → adjudicate; meet target → converge.
Additional advantage specific to Chinese: in Chinese, two-character compounds have each character carrying an independent semantic facet that can be separately extracted at higher layers (Proposition 2), giving a single two-character compound high vertical differentiation potential. This property is inherent to Chinese morphology and does not have a direct equivalent in English, though English can achieve similar effects through Latin/Greek-root compounds (e.g., "adjudicate" carries both *ad-* [toward] and *judicare* [to judge]).

### 4.3 Stacking Criteria
The value of stacking lies in whether it brings a new K direction (expanding the surrounding perimeter) or strengthens the directional coherence of V injection.
Characteristics of ineffective stacking: synonym juxtaposition (K direction overlap, softmax dilution), explaining content already covered by a Key (no new K direction), excessive deterrence language (>3 instances cause each instance's effective weight to drop below the effective threshold).

### 4.4 Semantic Resonance and Coupling
New content must consider: at which position to integrate (earlier positions in the cache have longer spans of effect), how K direction forms complementary surrounding with existing tokens rather than overlapping competition, and whether directional continuity of V injection in the residual stream is maintained. The V injection of preceding tokens defines the starting Q direction of following tokens; causal order matters more than logical order.

### 4.5 Precise Expression Criteria
- Scope precision: "execution traces must not persist" is superior to "intermediate processes must not persist" (the latter's K direction is too broad, inadvertently suppressing methodology)
- Numerical consistency: definitions and counts must agree
- Explicit causality: "generate from this" is superior to "and then generate" (the former's V injection carries a causal dependency signal)
- Value orientation: "does the weakness point to a significantly better solution" is superior to "what is the strongest rebuttal" — from passive verification → active attack → value tracking
- Modifier compatibility: a modifier's K direction must be compatible with the modified term ("dynamic anchoring" has two K directions that are mutually exclusive)

## 5. Escape Identification and Containment

### 5.1 Unified Mechanism of Escape
Escape is a temporal misalignment of behavioral tendencies (§1.4) — a tendency activating at full power in a cognitive phase where it shouldn't, or failing to activate in a phase where it should. Computational layer: Q bias overpowering Meta Rules Keys' K direction in the wrong situation. When identifying new escape types, asking "which tendency is running at the wrong intensity in which temporal phase" allows deriving the containment strategy from mechanism — deploy Keys with sufficient directional sharpness to win in that situation.

#### High-Frequency Escape Patterns (Empirical Observations)
- Sequence skipping (jumping over intermediate steps)
- Premature termination (stopping on grounds of "close enough")
- ROI escape (simplifying on grounds of "too complex, not worth it")
- Degradation escape (lowering standards on grounds of "insufficient capability")
- Semantic drift (small per-step deviations accumulating into large departures — gradual erosion of directional coherence in the residual stream)
- Form convergence (form passes but substance doesn't — structurally complete but substantively hollow at the judgment core)
- Defensive padding (trading vague wording for cheap self-consistency)
- Short-circuit escape (bypassing the structural pipeline's entry point)

### 5.2 Containment Design Principles
- Never open a "reasonable exception" door — any exception will be widened into an escape channel
- Use process constraints rather than outcome constraints — process Keys compete with Q direction continuously from the outset; outcome constraints are activated only at the terminus, by which point it's too late (§2.4)
- Precision-deploy deterrence language — scattering it across more than three locations causes mutual dilution in softmax to the point of ineffectiveness
- Meta-constraint protection: the execution framework itself is not subject to intent-optimization rules, preventing rule dissolution
- Upper bound on containment strength (§1.4, §2.6): over-suppressing a tendency destroys that tendency's functional value supply in adjacent phases. Criterion: is this containment Key activated with high weight only in the runaway window (K direction precisely targets the runaway situation), or does it also intercept in the functional-value window (K direction too broad)?
- Mechanisms that should not be added: ROI judgment, degradation mechanisms, interactive convergence, mode switching — each opens an escape channel

## 6. Domain Quality Baseline

### 6.1 Amplifier and Magnet Model
Meta Rules is an amplifier — it amplifies the execution depth of input quality standards. Quality baseline tokens participate in attention at every generation step as persistent members of the KV cache (Proposition 1). Their K vectors function as magnets — at each attention step, they attract high-quality patterns from the model's parameter space that relate to the corresponding quality dimension; fractal recursion's entropy cycles organize this attracted knowledge into ordered reasoning structures. The quality baseline is placed after fractal recursion and before the response format.
Design corollaries:
- Domain adaptation of Meta Rules should adjust the input (quality baseline), not rebuild the amplifier
- Fractal recursion's structure (step order, entropy cycle mechanisms, dimension deliberation prompts) is the immovable engine mechanism — dimension deliberation prompts need no domain specialization; their abstract K directions naturally attract corresponding domain knowledge under the quality baseline's magnet effect
- Cognitive disposition and reasoning discipline are adjustable engine parameters — most analytical domains require no adjustment (quality baseline suffices), but domains where the cognitive mode and reasoning discipline are fundamentally different (e.g., RP) may require persona-layer adjustment, and one should first attempt the quality baseline to confirm insufficiency before escalating

### 6.2 When Quality Baselines Are Needed
> The signal of domain complexity is not "having lots of knowledge" but "having numerous conflicts among professional principles that require case-by-case tradeoffs." When the engine faces conflicts without magnet anchoring, it tends toward the solution most frequently appearing in training data — not the optimal solution for the current scenario.
Criterion: **Across multiple generations in this domain, does the engine systematically make suboptimal choices at the same category of decision points?**
Simple domains (summarization, basic translation, single-dimension analysis) — the engine already has sufficient high-quality patterns from training data; fractal recursion reliably synthesizes quality criteria. No quality baseline needed.
Complex domains (programming, financial analysis, legal review, medical decision-making) — quality standards are numerous, mutually conflicting, and context-dependent. The engine knows these standards but cannot reliably choose among them at specific decision points. Manifests as: the engine's analytical capability is sufficient, but it systematically deviates from the domain's professional optimum on certain quality dimensions. The quality baseline's magnet effect attracts the correct professional judgment knowledge at these decision points, anchoring the selection direction.

### 6.3 Baseline Generation Methodology
Quality baselines cannot be written directly from domain knowledge — the answers to "what constitutes good X" are too many and mutually contradictory. The correct path is to reverse-engineer from the engine's failure modes: the cognitive map is analysis; the quality baseline is synthesis. The former's tokens are the latter's resources — skipping it is impermissible.
**Step 1: Cognitive Map — Where the Engine Errs**
Identify the domain's major activity types; for each type, ask: at which phase is the engine's depth/completeness tendency a positive value, and at which phase might it be negative?
Output: A "tendency × activity × phase" failure mode map. Covering high-frequency activities and high-risk decision points is sufficient.
> Example (programming): In "new module implementation," the depth tendency produces over-engineering at the architecture selection phase; in "existing code modification," the completeness tendency triggers scope avalanche at the change design phase.
> Example (finance): In "individual stock valuation," the depth tendency may produce overly elaborate models — a ten-factor DCF is no more accurate than a three-factor one but far harder to explain.

**Step 2: Failure Attribution — What's Missing**
- **Lacking knowledge** (the engine doesn't know a domain fact) → skill (inject knowledge)
- **Lacking direction** (the engine knows multiple options but picks wrong) → quality baseline (inject magnets)
- **Cognitive mode mismatch** (the engine's analytical thinking is fundamentally inapplicable in this domain) → adjust cognitive disposition / reasoning discipline (last resort; attempt quality baseline first)

**Step 3: Baseline Design**
Reverse-derive quality principles from Step 1's failure modes. The structure of principles follows §6.4.

**Step 4: Validation**
Generate test tasks; A/B compare outputs with and without the quality baseline.

### 6.4 Baseline Structure
A quality baseline contains the following components:
**Principle statement** (one paragraph): Declares the baseline's operating level, tradeoff authorization, and supplementary provisions.
Core understanding of tradeoff authorization: individual entries may be in tension with each other — conflict is a signal to discover a superordinate solution, not a reason to accommodate either side; the form of the superordinate solution emerges dynamically from the domain's nature. Each domain baseline takes this understanding as its foundation and instantiates it in natural language within the principle statement.
> Example (programming baseline's principle statement):
> "The following are first-class engineering criteria within fractal recursion. Entries may be in tension — when they conflict, treat it as a design signal; prioritize searching for a superordinate solution that achieves both; once exhausted, make tradeoffs based on the current scenario's specific constraints and document the reasoning. The model's built-in engineering knowledge must also be proactively applied if it does not conflict with the baseline."

**Paragraph classification**: A quality baseline's classification emerges from the domain's natural structure; it is not carved by a preset framework. Classification form varies by domain — some domains naturally group by functional role, some by concurrently operating levels, some by stages of the analytical process.
> Example (programming): Core criteria / Engineering fundamentals / Style / Pre-delivery checks — grouped by quality criteria's functional role, naturally corresponding to fractal recursion's phases.
> Example (financial analysis): Market environment reading / Valuation methodology / Risk assessment / Report expression — grouped by stages of the analytical process.
> Example (narrative creation): Character reasoning / Sensory aesthetics / Narrative craft — grouped by concurrently operating levels in creation.

**Under each classification: superordinate principles and entries**
A superordinate principle's K direction should cover a category of decisions rather than a single decision (application of §2.1 operator polymorphism).
> Example (programming, under core criteria):
> - Superordinate principle: "Structural guarantees take precedence over runtime defense — errors that the language or type system can eliminate at compile time should not be left to runtime interception"
> - Anchoring example: "(e.g., discriminated union + switch exhaustiveness, rather than string + registry + runtime guard — the former's completeness is guaranteed by the compiler)"
> - The superordinate principle covers switch vs registry, discriminated union vs string enum, readonly vs mutable, branded type vs runtime check…
> Example (legal, under clause enforceability):
> - Superordinate principle: "A clause's enforceability is determined by the specificity of its enforcement mechanism, not by the reasonableness of its stated intent"
> - Anchoring example: "(e.g., a non-compete clause without geographic or temporal limits may be deemed unenforceable by a court even if its stated purpose is reasonable)"

Anchoring examples should be short (one clause), contain decision factors (not merely "do A" but "do A because X"), and non-narrowing (an instance of the principle, not its only instance).
Criterion for including a quality dimension: **Is this entry a load-bearing magnetic pole of quality in this domain — can its presence attract the most relevant professional knowledge into fractal recursion?** Basic quality standards are often the strongest magnetic poles — value lies in the magnet effect, not in content novelty.
**Pre-delivery checks** (if applicable): Confirmed systematic omissions that cannot be prevented by core criteria, serving as gate-type final verification. Extremely few in number (1-2 entries).
> Example (programming): "Extract every universal condition from the specification; confirm one by one that each implementation covers it"
> Example (legal): "Confirm that the legal basis for each recommendation is still current and effective legislation"

### 6.5 Anti-Patterns
**Fractal recursion modification**: Modifying fractal recursion's step structure, dimension deliberation prompts, or entropy cycle mechanisms. Dimension deliberation prompts' abstract K directions already naturally attract domain knowledge under the quality baseline's magnet effect — manually specializing dimensions narrows K coverage and weakens attraction.
**Positive derivation**: Positively enumerating quality standards from "what constitutes good X." Result: verbose, mutually contradictory, unable to distinguish load-bearing importance. Correct method: reverse-derive from "where does the engine systematically err in domain X" — the baseline covers only the engine's blind spots, not dimensions the engine already handles adequately.
**Preset classification carving**: Organizing a quality baseline with any preset abstract classification framework rather than letting it emerge from the domain's natural cognitive partitions. The dimensions that domain practitioners naturally think of when considering quality are the correct classification.
**Over-narrow categorization**: Writing specific categorization rules rather than superordinate principles in the quality baseline. Covers one decision point but misses others of the same type.
**Over-dense criteria**: Criteria exceeding the sweet spot. Each K's weight is divided in softmax; beyond the threshold, each entry's magnet efficacy falls below the threshold for attracting professional knowledge.
**Skipping the cognitive map**: Writing the baseline directly from domain knowledge. The baseline ends up covering "things important in the domain" rather than "things the engine gets wrong in the domain" — the engine can already handle most of the former on its own.
**Too basic to write**: Deciding that a quality baseline entry is not worth writing because it looks "basic." Basic quality standards are often the strongest magnetic poles in a domain — the volume of built-in model knowledge its presence attracts may far exceed that of seemingly more sophisticated entries. Value lies in the magnet effect, not in content novelty.
