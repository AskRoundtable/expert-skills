# Recognition-Primed Decision (RPD) Model

The cognitive engine implements Gary Klein's RPD model, derived from studying how experts actually make decisions under pressure.

## Overview

Experts don't analytically compare options. They recognize patterns, simulate outcomes mentally, and act. This model encodes that process.

> "The key to effective decision making is not to find the optimal solution but to find one that works."
> — Gary Klein, *Sources of Power* (1998), p. 20

---

## Step 1: Pattern Recognition

Match the current situation against known prototypes.

**Process:**
1. Identify situation type ("This looks like...")
2. Note salient cues (what stands out?)
3. Flag missing information (what's NOT there that should be?)

**Expert vs. Novice:**
| Expert | Novice |
|--------|--------|
| Sees patterns immediately | Analyzes individual features |
| Notices anomalies | Misses subtle cues |
| Knows what to ignore | Overwhelmed by data |

**Source:** Klein, G. (1998). *Sources of Power*, Chapter 3: "The Power of Intuition"

---

## Step 2: Mental Simulation

Run the proposed action forward in your mind.

**Feasibility Gate (before simulating):**

Before evaluating which option is "better," verify each option is logically possible:

1. State the **goal** of the action (what must be true at the end?)
2. List the **prerequisites** for that goal (what must exist/be present?)
3. For each option: does it satisfy ALL prerequisites?
4. If an option fails a prerequisite → **eliminate immediately**, do not simulate

> **Why this matters:** Pattern recognition (Step 1) often fires on surface features (e.g., "short distance → walk") and skips constraint checking. The Feasibility Gate catches options that are logically impossible before you waste time optimizing between them.
>
> **Example:** "Should I drive or walk to the car wash?" → Goal: wash the car → Prerequisite: car must be at the car wash → Walking fails the prerequisite → Only one feasible option, no comparison needed.

**Process (for feasible options only):**
1. "If I do X, then Y will happen..."
2. "Then Z will follow..."
3. "What could go wrong?"

**Key Principle:** Don't compare multiple options analytically. Take the first workable option, simulate it, and only seek alternatives if simulation reveals fatal flaws.

**Simulation Checklist:**
- Does the action address the core problem?
- What are the second-order effects?
- Where could this fail?
- What assumptions am I making?

**Source:** Klein, G. (1998). *Sources of Power*, Chapter 4: "The Power of Mental Simulation"

---

## Step 3: Anomaly Detection

Check for inconsistencies that don't fit the recognized pattern.

**Questions to Ask:**
- What doesn't fit the pattern?
- What assumptions might be wrong?
- What is the user not seeing?
- What would have to be true for this to work?

**Warning Signs:**
- Overconfidence in pattern match
- Ignoring contradictory evidence
- Forcing data to fit the pattern

**Source:** Klein, G. (2013). *Seeing What Others Don't*, Chapter 5: "The Logic of Contradictions"

---

## Step 4: Insight Generation (Triple Path)

When standard patterns don't apply, generate insights through three paths.

### Path A: Connections
Link disparate ideas or domains.

- "What does this remind me of from another field?"
- "What pattern from domain X applies here?"

### Path B: Contradictions
Notice when something doesn't add up.

- "This data contradicts that assumption..."
- "Everyone believes X, but evidence shows Y..."

### Path C: Creative Desperation
When conventional approaches fail, explore unconventional options.

- "If the obvious approach won't work, what else?"
- "What would we do if we had no constraints?"

**Source:** Klein, G. (2013). *Seeing What Others Don't*, Chapter 7: "The Triple Path Model"

---

## Output Template

When applying this model, structure analysis as:

```
## Pattern Recognition
- Situation type: [identified pattern]
- Key cues: [what stands out]
- Missing information: [gaps noted]

## Mental Simulation
- Proposed action: [first workable approach]
- Expected outcome: [if X, then Y, then Z]
- Potential failures: [what could go wrong]

## Anomaly Check
- Inconsistencies: [what doesn't fit]
- Assumptions at risk: [what might be wrong]

## Insights
- Connections: [cross-domain patterns]
- Contradictions: [counter-intuitive observations]
- Alternatives: [non-obvious options]

## Recommendation
[Synthesized recommendation with confidence level and caveats]
```

---

## References

1. Klein, G. (1998). *Sources of Power: How People Make Decisions*. MIT Press.
2. Klein, G. (2013). *Seeing What Others Don't: The Remarkable Ways We Gain Insights*. PublicAffairs.
3. Klein, G. (2007). "Performing a Project Premortem." *Harvard Business Review*, September 2007.
