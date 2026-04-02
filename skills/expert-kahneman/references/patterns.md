# Daniel Kahneman: Pattern Library

Situation recognition patterns for detecting cognitive biases in action.

---

## 1. Narrative Substitution (敘事替換)

**Pattern:** When a hard question is replaced by an easier one — automatically and unconsciously. System 1 cannot answer "What is the probability this startup will succeed?" so it answers "Does this founder feel like a winner?" and treats that as the answer.

**Trigger Cues:**
- Quick confident conclusions on genuinely uncertain questions
- "It just feels right" as justification
- Assessment based primarily on resemblance ("They remind me of...")
- Emotional engagement leading to confident prediction

**Kahneman's Response:**
> "The mental shotgun fires when we answer one question, but what we aimed at was another."

**Diagnostic Questions:**
- What was the actual question being asked?
- What question did we actually answer?
- What information would we need to answer the original question properly?

**Example:**
A board evaluates a new CEO candidate. They find the candidate "impressive, visionary, and commanding." They are actually answering "Does this person perform well in presentations?" while treating it as an answer to "Will this person be an effective CEO in our specific context?"

**Source:** Thinking, Fast and Slow, Ch. 12-13.

---

## 2. Overconfidence & Calibration Failure (過度自信)

**Pattern:** Confidence significantly exceeds accuracy. Subjective probability distributions are too narrow. People express certainty (or near-certainty) about outcomes that have substantial uncertainty.

**Trigger Cues:**
- "We're 90% sure this will work"
- Single-point estimates for fundamentally uncertain forecasts
- No acknowledgment of alternatives or disconfirming scenarios
- "We've done our homework" used as confidence justification

**Kahneman's Response:**
> "The overconfidence that is most damaging is not expressed in explicit probability estimates. It is the absence of uncertainty in the narrative."

**Diagnostic Questions:**
- What's the confidence interval on this estimate?
- What information would make you less confident?
- What's the track record for similar forecasts in this domain?
- What do independent experts with the same information think?

**Example:**
A project manager says "We'll ship in Q3 — we're planning carefully and have a detailed roadmap." Kahneman's diagnosis: the detail of the plan creates the illusion of certainty. The actual distribution of outcomes for comparable projects was never consulted.

**Source:** Thinking, Fast and Slow, Ch. 19-20.

---

## 3. Base Rate Neglect (基準率忽視)

**Pattern:** Specific story-based information about a case overwhelms statistical base rate information. People dramatically under-weight the prior probability when given narrative details about a particular case.

**Trigger Cues:**
- Decision driven entirely by case-specific features
- "But our situation is different" without quantifying how much it differs
- Strong narrative without any reference to comparable cases
- "We have a unique advantage" as rebuttal to statistical evidence

**Kahneman's Response:**
> "The correct procedure is to anchor the prediction on the base rate — the percentage of cases in the relevant reference class — and to adjust from the base rate only by the strength of diagnostic evidence."

**Diagnostic Questions:**
- What is the base rate for this type of outcome?
- What reference class does this case belong to?
- How strong is the specific evidence that we should adjust significantly from the base rate?

**Example:**
An entrepreneur pitches with a detailed, compelling story. Investor asks no questions about base rates ("What percentage of companies in this category reach $10M ARR?"). The narrative hijacks the statistical question. Kahneman: start with base rate, then ask how much specific evidence justifies deviation.

**Source:** Thinking, Fast and Slow, Ch. 14-16.

---

## 4. Loss Aversion Trap (損失規避陷阱)

**Pattern:** Fear of loss drives decisions disproportionately — keeping bad options open to avoid realizing losses, taking excessive risk to avoid certain losses, or refusing good bets because the potential loss is more salient than the potential gain.

**Trigger Cues:**
- "We can't afford to lose this client"
- Strong resistance to cutting a project despite poor prospects
- "We've invested too much to stop now"
- Risk tolerance asymmetric between gains and losses
- "Let's not give anything up in this negotiation"

**Kahneman's Response:**
> "Losses loom larger than gains... The asymmetry between the power of positive and negative expectations or experiences is an important aspect of human nature."

**Diagnostic Questions:**
- If we hadn't already invested X, would we start this project today?
- Are we reframing this as a loss when it could be framed as a smaller gain?
- What is the actual expected value of this decision (not just the loss scenario)?

**Example:**
A product team continues investing in a declining feature because "we can't discontinue it — we'll lose the customers who use it." Loss aversion: the loss of existing users feels more salient than the opportunity gain from redirecting resources. Reframe: "From today, what's the net expected value of continuing vs. discontinuing?"

**Related Mechanism — Status Quo Bias / Omission Bias (現狀偏誤):**

When faced with a choice between action and inaction, people systematically favor inaction (the status quo) because action carries the psychological weight of an active bet while inaction feels like not-choosing.

**Why it's distinct from loss aversion:** Loss aversion concerns the *outcome* (the pain of losing outweighs the pleasure of gaining). Status quo bias concerns the *act of choosing itself* — choosing the "safer" option feels costless and identity-neutral, while choosing the riskier option feels like taking personal responsibility for what might go wrong. The decision-maker is not just loss-averse about outcomes but also loss-averse about the act of choosing.

**Trigger Cues (specific to status quo / omission bias):**
- One option is described as "safe" or "default" without scrutiny of its downsides
- "At least I won't regret it" — regret avoidance driving inaction
- Active choice framed as a "bet" while passive choice is framed as "not betting"
- "I'm just being careful" as justification for systematically avoiding all active options

**Equal Scrutiny Test (named mitigation):**
Reframe both options as equally active choices with consequences. The "safe" option has costs too — opportunity cost, growth forgone, and the compounding effect of defaulting to lower-expected-value paths. Apply equal analytical rigor to both: "If I actively chose Offer A with full awareness of its 5-year trajectory, would I still choose it? Or am I choosing it because it requires less psychological courage?"

**Source:** Thinking, Fast and Slow, Ch. 26-29; Samuelson & Zeckhauser (1988), Status Quo Bias in Decision Making.

---

## 5. Planning Fallacy Signal (規劃謬誤信號)

**Pattern:** Project plans consistently represent the best-case scenario. Risk analysis produces a list of named risks (each individually "managed") but no actual probability distribution. The plan is treated as a roadmap to the expected outcome rather than one path through a distribution of possibilities.

**Trigger Cues:**
- Schedule and budget exactly match what was requested or hoped for
- "Risks are managed" without showing what the distribution of outcomes looks like
- No reference to similar completed projects
- Optimism described as "our team's capability" rather than acknowledged as optimism
- No explicit pre-mortem or failure scenario analysis

**Kahneman's Response:**
> "The inside view is: how will this project go? The outside view is: how have projects like this actually gone? People naturally focus on the inside view — and that is almost always a mistake."

**Diagnostic Questions:**
- What did similar projects actually take?
- What are the p10 (optimistic) and p90 (pessimistic) outcomes, not just the expected outcome?
- Have we run a pre-mortem: "It's 12 months from now and this failed — what went wrong?"

**Example:**
A construction project budgeted at $10M and 18 months. Outside view: comparable municipal projects average 220% of initial budget and 180% of initial schedule. The team's estimate represents the inside view — their vision of how this specific project will go — not the distribution of how such projects actually go.

**Source:** Thinking, Fast and Slow, Ch. 23-24.

---

## 6. Hindsight Bias Distortion (後見之明偏誤)

**Pattern:** After an outcome is known, people believe they "knew it would happen" or "should have seen it coming." This distorts learning: the decision process is evaluated based on outcomes rather than on the quality of reasoning given the information available at the time.

**Trigger Cues:**
- "We should have seen this coming"
- "It was obvious in retrospect"
- Blame language in post-mortems focused on not predicting the outcome
- Learning from the wrong level (outcome vs. process)

**Kahneman's Response:**
> "Hindsight bias is a major obstacle to learning from experience... Because it's so easy to find reasons for outcomes after they happen, the evaluation of decisions by their outcomes is fraught."

**Diagnostic Questions:**
- What information was actually available at the time of the decision?
- What were the plausible scenarios at that moment?
- Was the decision process sound given what was known then?
- Would a skilled practitioner with the same information have made the same call?

**Example:**
After a product fails in the market, a review concludes "we should have done more customer research." Hindsight bias: it's easy to say so now. The real question: given the information and constraints at the time, was the decision to launch without more research a defensible one? Outcome does not determine process quality.

**Source:** Thinking, Fast and Slow, Ch. 19.

---

## 7. Cognitive Ease Trap (認知流暢度陷阱)

**Pattern:** Familiar, easy-to-process information feels true and good. Ideas that are simple to understand, have been encountered before, and are presented fluently feel credible — independent of their actual validity. This is the mechanism behind brand familiarity, repeated messaging, and the "truth effect."

**Trigger Cues:**
- "This feels right" as the primary justification
- Agreement increases after repeated exposure (not after new evidence)
- Simple, well-packaged presentations treated as more credible than complex ones
- "I've heard this before" used as validation

**Kahneman's Response:**
> "A reliable way to make people believe in falsehoods is frequent repetition, because familiarity is not easily distinguished from truth."

**Diagnostic Questions:**
- Does this feel right because it's true, or because it's familiar?
- Would someone encountering this idea for the first time, with no prior exposure, find it equally compelling?
- What's the actual evidence, stripped of the presentation?

**Example:**
A strategic narrative is repeated in every all-hands for 6 months. Teams report believing in it deeply. Cognitive ease: the repetition has made it feel true and right. The question is whether the narrative was validated by evidence or by frequency of repetition — and whether the team can distinguish between these.

**Source:** Thinking, Fast and Slow, Ch. 5-6.

---

## References

- Kahneman, D. (2011). *Thinking, Fast and Slow*. Farrar, Straus and Giroux.
- Tversky, A., & Kahneman, D. (1974). Judgment under uncertainty: Heuristics and biases. *Science*, 185(4157), 1124-1131.
