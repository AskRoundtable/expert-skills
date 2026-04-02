# Step 5: Epistemic Audit — Design Rationale

## Why This Step Exists

The RPD process (Steps 0-4) is optimized to produce expert-quality analysis. But expert-quality analysis has a failure mode: **it is convincingly wrong**. The better the framework, the more persuasive the output — regardless of whether the diagnosis is correct.

Step 5 exists to break this cycle. It forces the system to question its own analysis with the same rigor it applies to the user's situation.

**Origin:** This step was designed after observing that multi-expert panel analyses (expert-panel) consistently produce smooth, coherent narratives that feel authoritative but may contain:
- Framework projection (experts seeing their own models everywhere)
- Premature closure (diagnosing before sufficient information)
- Coherence fallacy (smoothing over contradictions to create a compelling story)
- Unearned confidence (high-conviction claims based on thin evidence)

## The Three Sub-Steps

### 5a. Hammer Check

**Problem it solves:** Abraham Maslow's Law of the Instrument — "If the only tool you have is a hammer, everything looks like a nail." Every expert module has 5-10 core models. The system will naturally match problems to these models, even when the fit is poor.

**How to detect:**

| Red Flag | Example |
|----------|---------|
| Pattern identified in Step 1 is the expert's most famous model | Munger always finding "incentive misalignment"; Taleb always finding "fragility" |
| Same model triggered across very different problems in one session | Three consecutive problems all diagnosed as "Circle of Competence violation" |
| Pattern match happened before Step 0 (Discovery) completed | Expert "knew" the answer before asking clarifying questions |
| No alternative patterns were considered | Only one pattern was evaluated; others dismissed without explanation |

**Mitigation:** Name at least one plausible alternative pattern. Explain why you chose the primary pattern over the alternative. If you cannot articulate why, your confidence should drop.

### 5b. Confidence-Evidence Alignment

**Problem it solves:** AI systems (and human experts) are often confidently wrong because confidence is driven by internal coherence ("this story makes sense") rather than external evidence ("I verified this claim").

**Calibration rule of thumb:**

| Evidence Type | Max Justified Confidence |
|--------------|------------------------|
| User's exact words + verifiable data | 0.9 |
| Reasonable inference from context | 0.7 |
| Pattern match without specific evidence | 0.5 |
| Speculation informed by framework | 0.3 |
| Pure framework projection | 0.1 |

**The falsification question:** For each key claim, ask "What would I need to see to abandon this diagnosis?" If you cannot answer this, the claim is unfalsifiable — and unfalsifiable claims should carry low confidence regardless of how well they fit the framework.

### 5c. Question Output

**Problem it solves:** The system's natural output is recommendations ("do X"). But recommendations are only as good as the information they're based on. When information is incomplete — which it almost always is in real decisions — the most valuable output is often "go find out Y before doing X."

**What makes a good investigation question:**

| Good | Bad | Why |
|------|-----|-----|
| Specific action the user can take | Abstract reflection prompt | Investigation questions must be actionable |
| Would change the analysis if answered | Confirms what we already believe | Questions should test assumptions, not validate them |
| Addresses the highest-uncertainty claim | Addresses a peripheral detail | Prioritize by impact on the overall diagnosis |

**Examples by domain:**

| Domain | Investigation Question | What It Tests |
|--------|----------------------|---------------|
| Business operations | "Ask your QA lead: how many PRs are waiting for review right now?" | Whether the bottleneck hypothesis is correct |
| Team dynamics | "In your next skip-level, ask 2 ICs: what's the one thing that slows you down most?" | Whether the Diminisher diagnosis matches ground truth |
| Strategy | "Pull your customer churn data by segment for Q3-Q4 — is churn concentrated in one segment?" | Whether the product-market fit is broad or narrow |
| Competition | "Check if the competitor's price cut applies to new customers only, or renewals too" | Whether this is acquisition strategy or retention war |

## Integration with Panel Mode

When expert-panel runs Step 5 across multiple experts, look for:

1. **Shared hammer risk:** If all experts on the panel identified patterns from their most famous models, the entire panel may be projecting. The Missing Chair test (anti-coherence check) partially addresses this, but Step 5a catches it at the individual expert level.

2. **Divergent falsification conditions:** If Expert A's claim would be falsified by condition X, and Expert B's claim would be falsified by the opposite of X — this is a high-value investigation target. One question can decisively resolve the disagreement.

3. **Question deduplication:** Multiple experts may generate similar investigation questions from different angles. Deduplicate and present the strongest version.
