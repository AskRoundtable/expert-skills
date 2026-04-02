# Daniel Kahneman: Core Mental Models

Ten core frameworks from Kahneman's research on judgment and decision-making.

---

## 1. System 1 & System 2 (雙系統)

**Source:** Thinking, Fast and Slow (快思慢想), Part I

**Definition:** Human thinking operates via two modes. System 1 is fast, automatic, associative, effortless, and often emotional — it runs continuously and produces impressions, intuitions, and impulses. System 2 is slow, deliberate, effortful, and logical — it monitors System 1 and intervenes when needed, but is lazy and often endorses System 1's conclusions without checking.

> "The division of labor between System 1 and System 2 is highly efficient: it minimizes effort and optimizes performance. The arrangement works well most of the time because System 1 is generally good at what it does."

**Application:**
- Diagnose which system is driving a decision: Is it fast/confident/intuitive or slow/effortful/checked?
- Expert intuition (System 1) is reliable in high-validity environments with sufficient practice
- System 1 is unreliable in low-validity environments (stock picking, political forecasting) or when inputs are misleading
- Critical System 2 step: Ask "Am I operating in a domain where my System 1 has been trained?"

**Unique Diagnostic Protocol — System 2 Rationalization Detection:**
The most dangerous S1/S2 failure is not when System 1 runs unchecked — it is when System 2 is co-opted to justify a System 1 conclusion, creating the illusion of rigorous analysis. This is distinct from WYSIATI (which concerns missing information) and Narrative Substitution (which concerns question replacement). S2 Rationalization concerns *process authenticity*: did the analytical work actually drive the conclusion, or did the conclusion come first?

Diagnostic sequence (unique to S1/S2, not covered by other frameworks):
1. **Timeline test:** Did the conclusion arrive before the analysis, or after? If the team "knew" the answer before the deep dive, System 2 is rationalizing.
2. **Disconfirmation test:** During analysis, was any evidence genuinely considered that could have changed the conclusion? If not, System 2 was operating as System 1's lawyer, not its judge.
3. **Effort asymmetry test:** Was more effort spent building the case for the preferred option than stress-testing it? Genuine System 2 allocates effort to the strongest counter-argument.
4. **Lazy endorsement test:** Did System 2 simply validate System 1's first impression ("yes, this looks right") without generating independent analysis? The signature: high confidence with low cognitive effort.

**Tension with RPD:** Gary Klein's Recognition-Primed Decision model (used in expert-engine) is essentially System 1 at work in expert domains. Kahneman and Klein resolved their disagreement: expert System 1 is valid in high-validity environments; the danger is when System 1 confidence transfers to low-validity contexts.

**Example:**
A seasoned firefighter instantly recognizes "something is wrong" in a burning building and orders evacuation — System 1 pattern recognition. A startup founder uses the same confidence to predict market adoption in a domain they've never worked in — System 1 misapplied.

**Rationalization Example:**
An acquisition committee spends 4 months on due diligence (System 2 effort) but the CEO formed a positive impression in the first meeting (System 1). Every piece of negative evidence encountered during due diligence was "addressed" and "mitigated" — none was allowed to change the trajectory. The extensive analytical process created the feeling of rigor while the conclusion was predetermined. Diagnostic: apply the Timeline Test — the decision to proceed was made emotionally in month 1; months 2-4 were System 2 serving as System 1's defense attorney.

---

## 2. WYSIATI — What You See Is All There Is (所見即全部)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 12

**Definition:** System 1 builds coherent narratives from available information and treats them as complete reality. It does not ask "what am I missing?" — it constructs the best possible story from whatever is in front of it, generating high confidence even when information is sparse.

> "An important limitation of our mind: its inability to reconstruct the past from the present — and our inability to acknowledge this."

**Application:**
- When a situation seems to "make sense" immediately, WYSIATI is probably operating
- The remedy: explicitly ask "What information is NOT in front of us?"
- In assessments, ask: "What would we conclude if we knew the opposite evidence?"
- WYSIATI explains why incomplete briefings lead to confident wrong conclusions

**Example:**
A product team hears only customer praise at launch events (because unhappy users don't attend) and concludes the product is a success. WYSIATI: the story built from available data (positive feedback) feels complete and accurate, masking the unseen information (the silent majority who disliked the product).

---

## 3. Prospect Theory (前景理論)

**Source:** Thinking, Fast and Slow (快思慢想), Part IV (Kahneman & Tversky, 1979)

**Definition:** People evaluate outcomes relative to a reference point, not in absolute terms. Losses loom larger than gains of equivalent magnitude (loss aversion factor ~2x). The value function is concave for gains (risk-averse) and convex for losses (risk-seeking). People also overweight small probabilities and underweight moderate-to-large ones.

> "The response to losses is stronger than the response to corresponding gains... Organisms that treat threats as more urgent than opportunities have a survival advantage."

**Application:**
- Detect when loss framing is driving excessive risk aversion
- Reframe decisions: "We stand to lose $X" vs. "We have a 50% chance of saving $X"
- Loss aversion explains sunk cost thinking: the "loss" of writing off past investment feels disproportionately painful
- "Negotiating in the gain frame" makes agreements more likely than "loss frame" negotiations

**Example:**
A company is reluctant to exit a failing product line because "we've invested $5M." Prospect theory: the $5M loss (of the investment) feels more salient than the future $3M gain from reallocating resources. Correct framing: "From today forward, which allocation generates better returns?"

---

## 4. Availability Heuristic (可得性捷思)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 12 (Kahneman & Tversky, 1973)

**Definition:** People judge the probability or frequency of an event by how easily examples come to mind. Vivid, recent, or emotionally charged events are over-weighted; base rates and statistical evidence are under-weighted.

> "The ease with which instances come to mind is a signal that the system uses as evidence of frequency and probability."

**Application:**
- After a memorable failure, teams over-weight that failure mode and under-weight others
- After a major success, competitor threat is under-weighted (it doesn't come to mind easily)
- Media coverage inflates perceived risk of covered events (plane crashes, terrorism) relative to statistical reality
- Remedy: ask for base rates before relying on recalled examples

**Example:**
Post a major data breach at a competitor, the security team demands extensive new controls focused exclusively on that breach type. Availability bias: the recently-salient threat type is overweighted. The harder-but-less-vivid statistical analysis of actual risk distribution is neglected.

---

## 5. Representativeness Heuristic (代表性捷思)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 14-15 (Kahneman & Tversky, 1972)

**Definition:** People judge the probability that an instance belongs to a category by how representative it is of that category (how much it resembles the prototype). This causes two major errors: base rate neglect (ignoring statistical frequencies) and conjunction fallacy (judging specific scenarios as more probable than general ones).

> "People who are asked to assess probability are not reasoning as statisticians but as pattern-matchers."

**Application:**
- Detect when someone is judging likelihood by fit to a narrative rather than statistical frequency
- "Linda is a feminist bank teller" feels more likely than "Linda is a bank teller" — the conjunction fallacy
- Founder story matching a successful archetype doesn't predict startup success
- Remedy: force explicit base rate consideration before narrative assessment

**Example:**
An investor says "This founder is exactly like Steve Jobs — intense, visionary, product-obsessed" as a reason to invest. Representativeness: judging by fit to a success template rather than base rates (99%+ of intense product-focused founders do not build Apple-scale companies).

---

## 6. Anchoring Effect (定錨效應)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 11

**Definition:** When making numerical estimates or judgments, people are disproportionately influenced by the first number they encounter (the anchor), even if that number is arbitrary or irrelevant. Adjustment from the anchor is typically insufficient.

> "Anchoring occurs not only when the first piece of information is relevant; people anchor on almost anything, including clearly random numbers."

**Application:**
- First number in salary negotiations becomes the anchor for the entire discussion
- Budget estimates anchored to last year's budget rather than zero-based reasoning
- Asking price in real estate heavily anchors perceived value
- Remedy: generate your own estimate before hearing others'; make explicit counter-anchoring moves

**Example:**
A client asks "Could this project cost $100K?" — even if the real cost is $300K, the estimate will tend to be pulled toward $100K. The consultant who hears this anchor first will systematically under-estimate compared to one who was never told the $100K figure.

---

## 7. Planning Fallacy (規劃謬誤)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 23 (Kahneman & Tversky, 1979)

**Definition:** People systematically underestimate the costs, time, and risks of their own projects while overestimating the benefits — driven by optimistic inside-view reasoning. This isn't random error: it's a systematic bias toward best-case scenarios.

> "The planning fallacy is explained by people's tendency to predict final outcomes based on the state of the work at the moment, neglecting unknowns and overlooking the rate at which unknowns accumulate."

**Application:**
- The fix is outside view: reference class forecasting — what did similar projects actually take?
- Standard adjustment: add 40-60% time/cost buffer to inside-view estimates
- Require explicit scenario planning (not just "risks" — actual distribution of outcomes)
- Pre-mortems: "Imagine it failed. What went wrong?" generates plans ignored in optimistic planning

**Example:**
A software team estimates 3 months for a feature. Outside view: comparable features from similar teams took 5-7 months. The team's plan is based on "this time will be different because [specific reasons]" — which is exactly the planning fallacy narrative. The correct starting point is the reference class, then adjust for specifics.

---

## 8. Inside vs. Outside View (內外部觀點)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 23

**Definition:** The inside view focuses on the specific case — its unique features, the team's capabilities, the plan's logic. The outside view ignores the case's specific details and instead asks: "What happened to other cases in the same reference class?" Inside view produces optimism; outside view produces calibration.

> "The outside view can be taken by anyone — it requires only knowing which reference class applies. The inside view requires knowing the details of this particular case, which is usually the information that leads to overconfidence."

**Application:**
- Before accepting any forecast, ask: "What's the reference class? What's the outside-view base rate?"
- Use reference class forecasting: identify 5-10 comparable past cases, build distribution
- Adjust from outside view toward inside view (not the reverse, which is natural but wrong)
- The outside view is particularly critical for projects, policies, and new ventures

**Example:**
"Our company is different — we have a better team, a clearer strategy, stronger customer relationships." Inside view. The outside view asks: "What percentage of SaaS companies that raised Series A in 2021 achieved profitability within 3 years?" Start there, then assess how much your specific factors move the needle.

---

## 9. Focusing Illusion (聚焦幻覺)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 38

**Definition:** Whatever we focus on appears more important to our overall well-being (or decision) than it actually is. Nothing in life is as important as you think it is while you are thinking about it. The act of evaluation inflates the weight of what's being evaluated.

> "Nothing in life is as important as you think it is while you are thinking about it."

**Application:**
- When evaluating a single option in isolation, its pros/cons seem much larger than when it's one of many
- Single-option presentations trigger focusing illusion — always generate alternatives
- In salary and lifestyle decisions, the evaluated factor (income, location) is always over-weighted relative to its long-term hedonic impact
- Remedy: evaluate options comparatively, not in isolation

**Example:**
A team spends two hours discussing one risk scenario in detail. By the end, they perceive that risk as extremely important — disproportionately to its actual probability or impact. Focusing illusion: the detailed consideration inflated its perceived significance. The remedy is maintaining a portfolio view of all risks.

---

## 10. Peak-End Rule (峰終法則)

**Source:** Thinking, Fast and Slow (快思慢想), Ch. 35

**Definition:** Memory of an experience is determined primarily by its peak (most intense moment, positive or negative) and its ending — not by the average experience or its duration. We have two selves: the experiencing self and the remembering self, and they often disagree.

> "The remembering self, not the experiencing self, is in charge of decisions. We learn from the past, but the past that drives us is not an accurate summary of our experience."

**Application:**
- Customer experience design: ensure strong peak moment and strong ending — averages don't matter as much
- End negotiations on a positive note even if the middle was difficult
- Team post-mortems are colored by the project's final weeks — not the overall experience
- In performance reviews: recency bias (ending) and severity bias (peak) distort the evaluation

**Example:**
A consultant delivers 6 months of excellent work but the final delivery is chaotic and the client relationship ends poorly. The client remembers the project as a failure. Peak-end rule: the poor ending dominates their remembered experience, overwhelming months of good work. Client experience management requires particular attention to the final touchpoints.

---

## References

1. Kahneman, D. (2011). *Thinking, Fast and Slow*. Farrar, Straus and Giroux.
2. Kahneman, D., Sibony, O., & Sunstein, C. R. (2021). *Noise: A Flaw in Human Judgment*. Little, Brown Spark.
3. Kahneman, D., & Tversky, A. (1979). Prospect theory: An analysis of decision under risk. *Econometrica*, 47(2), 263-291.
4. Tversky, A., & Kahneman, D. (1974). Judgment under uncertainty: Heuristics and biases. *Science*, 185(4157), 1124-1131.
