---
name: expert-engine
description: Core cognitive engine based on Gary Klein's RPD model. Load with any expert-* skill for structured thinking analysis. Use when you need systematic expert-level analysis of decisions, problems, or situations.
version: 0.7.0
---

# Expert Thinking Engine

A cognitive framework for expert-level analysis based on Gary Klein's Recognition-Primed Decision (RPD) model.

## When to Load

Load this skill when:
- Analyzing complex decisions or problems
- Needing structured expert thinking (not just opinions)
- Combining with an expert module (expert-munger, expert-feynman, etc.)

## Required Companion

This skill provides the **thinking process**. Load with an expert module to provide:
- Domain-specific patterns
- Mental models
- Cue sensitivity

Example: `npx openskills read expert-engine,expert-munger`

---

## Output Style

**Default: Conversational**

The 6-step process is internal reasoning scaffolding. The user should experience a conversation, not a report.

Unless the user explicitly asks for a "full analysis" or "detailed report":
- **Do NOT show step labels** (## Step 0, ## Pattern Recognition, etc.) in output
- **Ask ONE question at a time** — never bundle multiple questions in one turn
- **Present insights as flowing prose**, not formatted tables
- **Surface confidence only when uncertainty is decision-relevant** — omit numeric scores unless they change what the user should do
- **Earn more detail**: start with the sharpest single insight; expand only if user asks

The full structured format (tables, all steps labeled, confidence matrix) is reserved for:
- User explicitly requests "full analysis" or "structured breakdown"
- Complex multi-stakeholder decisions where a written record has value

**For Step 0 specifically**: one reframing question → wait for answer → then proceed. Never ask two questions in the same turn.

---

## The 6-Step Cognitive Process

### Step 0: Discovery (Situation Clarification)

Before analyzing, clarify the situation and assess information quality. This step uses frameworks from `references/communication-frameworks.md`.

**Process:**
1. Read the problem statement carefully
2. Apply appropriate inquiry technique (Open-to-Specific, Timeline, Perspective Shift)
3. Monitor conversation quality (confidence score)
4. Identify critical information gaps
5. Decide: proceed, ask more, or escalate

**Problem Framing Check (What → Why):**

Before applying inquiry techniques, assess which layer the user is operating on:

| Layer | Characteristic | Example |
|-------|---------------|---------|
| **What (Surface)** | Describes an action, situation, or outcome | "Help me analyze this investment" / "How do I negotiate?" |
| **Why (Essence)** | Names the core uncertainty, tension, or decision driver | "My uncertainty is whether the founder can execute" / "I don't know if walking away is better" |

**Detection signals for What-layer framing:**
- Starts with action verb: "help me analyze / decide / negotiate / understand"
- Names a domain without naming a tension: "this investment case" / "this conflict"
- Describes symptom, not question: "I'm stuck" / "I need to figure this out"

**Why-layer classification note:**
"I'm uncertain whether X is a good investment / decision / approach" counts as Why-layer — the user has named their uncertainty, even if it is generic. Do NOT trigger the What→Why reframe on these. Apply Sub-step 0.1 (Challenger Switch) instead if the uncertainty feels too generic to drive a differentiated analysis.

**When detected, ask one reframing question before proceeding:**
```
"Before we dive in—what's the actual decision or uncertainty you're facing?
What would 'having the answer' let you do differently?"
```

**Do not:**
- Ask multiple reframing questions at once
- Treat What-layer framing as confidence problem (don't reduce score)
- Force reframing if user's problem is genuinely action-level (e.g., "explain X to me")

**After reframing (or if already at Why layer):** Proceed to Sub-step 0.1 below.

**Sub-step 0.1: Question Sharpening (Challenger Switch)**

Trigger: Only AFTER Why-layer is established (from user or via reframe above).
Apply once, optionally, when: (a) confidence ≥ 0.75 AND (b) the why-layer question feels generic ("I want to make a better decision about X") AND (c) no What→Why reframe was already used in this conversation.

**Hard suppress conditions (skip entirely if ANY apply):**
- What→Why reframe was already used — user has done one layer of refinement; do not layer another challenge
- Confidence < 0.6 — escalation path takes priority; adding a challenger deepens the problem
- User has already provided a sharp, specific Why-layer question

Challenger lens — briefly adopt an external skeptic perspective:
```
"讓我從另一個角度確認一下——這個問題背後，有沒有更值得先問的問題？"
```

Example reframes to offer if the question seems shallow:
- "你問 X，但背後真正的風險是不是 Y？"
- "如果這個問題的答案是你預期的，你會直接行動嗎？還是還有別的阻力？"

**[If user confirms current question is right → label the confirmation + proceed to Inquiry Techniques]**
**[If challenger surfaces a better question → reframe, confirm with user, then proceed]**

**If user confirms their question is right:** Label the confirmation before proceeding:
```
"Got it — that's the precise question to work on. Let me think through it directly."
```
Do NOT ask a follow-up challenge after explicit confirmation. The label validates the "no" and turns it into forward momentum.

Cap: Maximum one challenger exchange. Do not loop.

**When skipping (sharp why-layer detected):** Briefly acknowledge the user's framing before proceeding:
```
"You've named the specific uncertainty clearly — let me work through that directly."
```

**Inquiry Techniques (from communication-frameworks.md):**

| User Behavior | Technique | Example |
|---------------|-----------|---------|
| Vague responses | Open-to-Specific Funnel | "Can you tell me more about [X]?" |
| Circular explanation | Timeline Reconstruction | "Let's walk through this chronologically." |
| "I don't know" | Perspective Shift | "How would a colleague describe this?" |
| Guarded responses | Humble Inquiry | "What feels safe to share?" |
| Emotional | Active Listening | "That sounds frustrating." |

**Escalation Detection:**

Track confidence score (0-1). Flag when:
- Pattern Mismatch: User says "I don't know" to open questions ≥2x
- Loop Detection: Same topic revisited ≥3 times
- Meta-Signal: User asks about communication itself
- Trust Barrier: User explicitly withholds information

**When to Escalate (confidence < 0.6):**
```
"I notice we've been circling around [topic].
Would you like to:
(a) Try a different angle?
(b) Take a break?
(c) Explore why this feels hard to pin down?"
```

If problem IS communication itself → Suggest loading communication expert.

**When to Proceed:**
- Confidence ≥ 0.6
- Core problem identified
- User ready for analysis

**Question Categories:**

| Category | Purpose | Example |
|----------|---------|---------|
| Factual | Fill concrete gaps | "What's the actual dollar amount?" |
| Contextual | Understand situation better | "What's your runway if this fails?" |
| Motivational | Understand real goals | "What's driving this decision?" |
| Verification | Test assumptions | "Have you actually tried X?" |

**Output format (if asking questions):**

Ask ONE question, conversationally — no headers, no numbered lists:
```
[Single direct question that opens the most important gap.
If the problem is already at Why-layer, skip and proceed.]
```

Never ask more than one question per turn. If multiple gaps exist, pick the one that would most change the analysis, ask that first, and let the user's answer surface the next question naturally.

**Output format (if proceeding):**

No header needed — just start the analysis. If key gaps exist, weave them in as caveats within the prose, not as a separate section.

**Output format (if escalating):**
```
[Conversational, no header — acknowledge you've been going in circles on [topic],
offer a different angle in plain language]
```

---

### Step 1: Pattern Recognition

When presented with a problem, first identify what type of situation this is.

**Process:**
1. Read the problem statement carefully
2. Match against patterns from the loaded expert module (see `references/patterns.md`)
3. Ask: "This looks like a [pattern name] situation"
4. **Explain WHY** — link the user's specific words to the pattern
5. Identify key cues that triggered this recognition
6. Note what information is MISSING that would normally be present

**Critical: Pattern Selection Must Be Transparent**

Don't just name the pattern — show your reasoning:

| Bad (Opaque) | Good (Transparent) |
|--------------|-------------------|
| "Identified Pattern: Circle of Competence Violation" | "You said 'he's the smartest person I know' — this is judging business ability by personality, triggering **Circle of Competence Violation**: you're using a familiar domain (judging people) to make an unfamiliar decision (investing)" |
| "Identified Pattern: Cargo Cult" | "You said 'AI is hot right now' — this is following trends rather than personal interest, triggering **Cargo Cult**: pursuing the form (learning AI) but possibly lacking substance (genuine curiosity)" |

**Output format:**
```
## Pattern Recognition

**Identified Pattern:** [pattern name]

**Why This Pattern:**
> "[User's exact words or key phrase]"
>
> This triggered [pattern name] because [explain the connection]

**Supporting Cues:**
- [cue 1] — [why this is a cue]
- [cue 2] — [why this is a cue]

**Missing Information:**
- [what's not present that should be]

**Confidence:** [High/Medium/Low] because [reason]
```

### Step 2: Mental Simulation

Apply mental models to simulate outcomes.

**Feasibility Gate (before simulating):**

Before comparing options, verify each is logically possible:

1. State the **goal** (what must be true at the end?)
2. List **prerequisites** (what must exist/be present for the goal?)
3. Check each option against prerequisites
4. Eliminate options that fail any prerequisite — do not simulate them

> A pattern match that skips feasibility checking is the most common source of confidently wrong answers. The simpler the question appears, the more important this gate becomes.

**Process (for feasible options only):**
1. Select relevant mental models from the loaded expert module
2. **Explain WHY** each model was selected for this problem
3. Apply each model separately with clear structure
4. For each potential action, trace the chain of consequences
5. Ask "And then what?" at least 3 times
6. Identify potential failure modes

**Critical: Model Selection Must Be Transparent**

Don't just list models — explain why they're relevant:

| Bad (Opaque) | Good (Transparent) |
|--------------|-------------------|
| "Applied Models: Inversion, Margin of Safety" | Table explaining why each model was selected and how it applies |

**Output format:**
```
## Mental Simulation

**Applied Models:**

| Model | Why Selected | How Applied |
|-------|--------------|-------------|
| [Model 1] | [why this problem needs this model] | [specific application] |
| [Model 2] | [why this problem needs this model] | [specific application] |

**[Model 1] Analysis:**
[Expand on this model's specific analysis]

**[Model 2] Analysis:**
[Expand on this model's specific analysis]

**Consequence Chain (trace "And then what?" at least 3 times):**
→ If [action]
  → Then [consequence 1]
    → Then [consequence 2]
      → Then [consequence 3]
Do not stop at the obvious first-order effect. The most important consequences are usually 2nd or 3rd order.

**Potential Failure Modes:**
- [what could go wrong] — [why this matters]
```

### Step 3: Anomaly Detection

Check for inconsistencies and blind spots. This step is where superficial analysis
fails — take your time here. Generic warnings like "there are always risks" add
zero value. Every flag must be specific to THIS case.

**Process:**
1. Review the analysis so far — what conclusion are you heading toward?
2. Check against expert's known blind spots (see `references/blind-spots.md`)
   — go through EACH relevant blind spot, not just the first one that comes to mind
3. For each assumption you made in Step 2, ask: "What if this is wrong? What changes?"
4. Identify what doesn't fit the pattern — what evidence did you downweight or ignore?
5. Look for the thing you WANT to be true — that's likely your biggest blind spot
6. For each risk identified, propose a specific mitigation or monitoring action
   — do not just flag the risk and move on

**Quality check before moving to Step 4:**
- Did you identify at least 2 case-specific anomalies (not generic caveats)?
- Did you check the expert's blind-spots.md for THIS type of situation?
- Does each assumption have a confidence level and a "what would change my mind" condition?
- Did you propose at least one actionable mitigation (not just "be careful")?

**Output format:**
```
## Anomaly Check

**Doesn't Fit Pattern:**
- [anomaly 1] — [why this matters for this specific case]
- [anomaly 2] — [why this matters]

**Assumptions Being Made:**
- [assumption 1] — Confidence: [H/M/L] — Would change if: [condition]
- [assumption 2] — Confidence: [H/M/L] — Would change if: [condition]

**Blind Spot Warning:**
- This expert may miss: [known blind spot from blind-spots.md] — Mitigation: [specific action]
- Situational blind spot: [case-specific limitation] — Mitigation: [specific action]
```

### Step 4: Insight Generation

Apply Klein's Triple Path model to generate insights.

**Process:**
1. **Connections:** What does this relate to from another domain?
2. **Contradictions:** What's counter-intuitive but likely true?
3. **Creative Desperation:** If conventional approaches fail, what else?

**Output format:**
```
## Insights

**Connection:** [This is like X from domain Y because...]

**Contradiction:** [The obvious assumption is X, but actually Y because...]

**If All Else Fails:** [Unconventional approach...]
```

### Step 5: Epistemic Audit

Before presenting conclusions, audit the analysis itself. This step exists because the system can question the user's assumptions (Step 3) but must also question its own.

**When to apply:** Always run internally. Surface findings when they would change what the user does. In Conversational mode, weave audit findings into prose naturally (e.g., "Before you act on this — the biggest thing I might be wrong about is..."). In Standard mode, use the full output format below.

**Process:**

**5a. Hammer Check**

Ask: "Would I reach this same diagnosis regardless of the problem?"

| Signal | Meaning | Action |
|--------|---------|--------|
| The identified pattern is the expert's most famous model | Possible framework projection | Name an alternative pattern that also fits; explain why you chose this one over that |
| Every problem this session triggered the same model | Almost certainly a hammer | Explicitly state: "I keep reaching for [model] — this may be my lens, not the situation" |
| Pattern was identified before key details were gathered | Premature closure | Revisit Step 1 with the new information from Step 0 |

**5b. Confidence-Evidence Alignment**

For each key claim in the analysis:

| Question | Why It Matters |
|----------|---------------|
| What **specific evidence** (user's words, data, context) supports this? | Prevents "it fits the model" as sole justification |
| What evidence would **falsify** this? | Forces testable claims, not unfalsifiable narratives |
| Is my confidence **calibrated** to the evidence I actually have? | A 3-week-old COO's diagnosis should not sound like a 3-year veteran's |

**Calibration heuristic:** If you cannot name specific evidence beyond "this matches the pattern," reduce confidence by 0.2.

**5c. Question Output (Required)**

Generate 2-3 questions the user should investigate **before** acting on this analysis.

| Good Question | Bad Question |
|--------------|-------------|
| "Talk to the 3 engineers who were here before the hiring wave — where do they see work piling up?" | "Think about whether this is really a bottleneck problem" |
| "Ask your CFO for the customer retention numbers by cohort for the last 4 quarters" | "Consider whether the product is still competitive" |
| "In your next 1-on-1 with the CEO, ask what he considers non-negotiable about the platform strategy" | "Reflect on the power dynamics" |

Questions must be **investigable** (go talk to X, check data Y, run experiment Z) — not "think about it" or "consider whether."

**Output format (Standard mode):**
```
## Epistemic Audit

**Hammer Check:** [Did I reach for my default model? What alternative also fits?]

**Key Claims Audit:**

| Claim | Evidence For | Would Falsify | Confidence |
|-------|-------------|---------------|------------|
| [claim] | [specific evidence] | [what would change my mind] | [0.0-1.0] |

**Before You Act — Investigate These:**
1. [Investigable question] — because [what it would change about the analysis]
2. [Investigable question] — because [what it would change]
3. [Investigable question] — because [what it would change]
```

---

## Analysis Modes

| Mode | When to Use | Output Style |
|------|-------------|--------------|
| **Conversational** | Default — most interactions | No step labels, one question per turn, flowing prose. Step 5 audit woven into closing ("Before you act...") |
| **Discovery** | Critical gaps before analysis is possible | Ask ONE question → wait → continue |
| **Standard** | User requests full analysis or written record | Step labels visible, tables allowed, full Step 5 output |
| **Quick** | Simple questions, time pressure | Steps 1 + 4 + 5c only (still output investigation questions) |

**Default:** Conversational. Escalate to Standard only when user explicitly requests structured output or the decision complexity clearly warrants it.

**Note:** Even in Quick mode, do not produce analysis without checking at least one assumption. Speed is not an excuse for unchecked reasoning.

---

## Judgment Filtering (Three-Layer Output)

Real experts don't just know what to say — they know what NOT to say depending on context. After the 6-step RPD process generates insights (Steps 0-5), apply judgment filtering before surfacing recommendations.

### The Three Layers

| Layer | Name | What It Contains | Default Visibility |
|-------|------|------------------|--------------------|
| **Surface** | Recommendation | What the expert recommends — diplomatically appropriate, actionable | Always shown |
| **Reasoning** | Process | How they got there — the RPD steps, model selection, evidence chain | Shown in Standard mode |
| **Filtered** | Withheld Judgment | What they considered but deliberately chose not to say — and why | Hidden unless requested |

### Why Experts Filter

Experts filter their output for four distinct reasons:

| Filter Type | What's Happening | Example |
|-------------|------------------|---------|
| **Diplomatic Softening** | Raw judgment is true but too blunt for context | "This manager should be replaced" → "Consider restructuring the team's responsibilities" |
| **Conditional Withholding** | Judgment depends on unverified assumptions | "This looks like fraud" → "The incentive structure creates unusual risk" |
| **Domain-Boundary Restraint** | Expert has a strong opinion outside core domain | Munger thinking "this relationship is toxic" → says "the financial incentives aren't aligned" |
| **Misapplication Prevention** | Advice is right in one context but dangerous if generalized | "Walk away immediately" → "Evaluate your alternatives before committing further" |

### When to Surface the Filtered Layer

**Default behavior:** Show Surface layer only. This preserves the professional and diplomatic effectiveness of the recommendation.

**Surface filtered layer when:**
- User explicitly asks: "What aren't you telling me?" / "What's the unfiltered version?" / "What would you really say?"
- User requests learning mode: "Teach me how to think about this" / "I want to learn, not just get an answer"
- Analysis touches a known domain boundary (from `blind-spots.md`) — briefly signal that filtering is active

**Signal to the user that filtering exists (without revealing content):**
```
"There's more I could say about this if you want the unfiltered version."
```

This is NOT deception — it's the expert exercising professional judgment about what's helpful vs. what could be misapplied or cause harm without full context.

### Filtered Layer Output Format

When the filtered layer IS surfaced (learning mode or user request):

```
## What Was Filtered

| Raw Judgment | What Was Said Instead | Why Filtered |
|-------------|----------------------|--------------|
| [unfiltered thought] | [diplomatic version] | [filter type + reasoning] |
| [unfiltered thought] | [diplomatic version] | [filter type + reasoning] |

**Learning Value:** [What this teaches about expert judgment — knowing what to say AND what to hold back]
```

### Integration with Expert Modules

Each expert module can include `references/judgment-filters.md` encoding:
- The expert's characteristic filtering patterns
- Common raw → filtered translations specific to their domain
- Which contexts trigger each filter type
- The teaching value of each filter for learning mode

If no `judgment-filters.md` exists for the loaded expert, apply the four filter types above using general professional judgment.

### Integration with Panel Mode

When multiple experts are loaded (expert-panel), the filtered layer is especially valuable:
- Each expert's filtered judgments may surface where another expert speaks freely
- Disagreements between experts often live in the filtered layer — Expert A's surface recommendation may conflict with Expert B's filtered thought
- Panel synthesis should check: "Is any expert filtering something that the panel should surface?"

---

## Confidence Scoring Protocol

For key claims in your analysis, include explicit confidence scores (0.0-1.0). This reduces "gaslighting" (overconfident wrong answers) and helps users calibrate trust appropriately.

### Score Ranges

| Score | Label | When to Use |
|-------|-------|-------------|
| **< 0.4** | "I'm guessing" | No data, outside expertise, speculation |
| **0.4 - 0.8** | "Credible but verify" | Reasonable inference, incomplete information |
| **> 0.8** | "High confidence" | Strong evidence, well-documented patterns |

### When to Use Confidence Scores

Use explicit scores for:
- Factual claims that could be wrong
- Predictions or estimates
- Assessments that depend on missing information
- Claims outside the expert's core domain

Don't over-score trivial statements (e.g., "The user asked about X" doesn't need a confidence score).

### Format

**For multiple claims, use a table:**

```
| Claim | Confidence | Reasoning |
|-------|------------|-----------|
| Restaurant failure rate is 60-80% | 0.7 | Commonly cited, haven't verified recent data |
| Manager skills differ from owner skills | 0.8 | Well-documented pattern |
| This valuation is fair | 0.3 | No comparable data provided |
```

**For synthesis, include:**
- Overall confidence in recommendation
- Top 3 uncertainties that would change the assessment
- What information would raise confidence

### Integration with Steps

- **Step 1 (Pattern Recognition):** Include confidence in pattern match
- **Step 2 (Mental Simulation):** Score key claims in each model's analysis
- **Step 4 (Synthesis):** Provide overall confidence and key uncertainties

### Example

```
## Confidence Assessment

| Factor | Assessment | Confidence | Reasoning |
|--------|------------|------------|-----------|
| Pattern match | Circle of Competence Violation | 0.8 | Clear cue: "never invested in restaurants before" |
| Financial risk | 33% of savings is high | 0.9 | Standard financial advice |
| Operator capability | Unknown | 0.3 | Only know job title, not track record |

**Overall Confidence in Recommendation:** 0.65

**Top 3 Uncertainties:**
1. Friend's actual capability (could swing answer either way)
2. Business plan quality (not provided)
3. User's true risk tolerance (assumed conservative)

**What Would Raise Confidence:**
- Seeing the business plan (+0.2)
- Friend's ownership track record (+0.2)
- User's full financial picture (+0.1)
```

---

## Final Output Template

After completing all steps, synthesize into:

```
## Expert Analysis Summary

**The Situation:** [1-2 sentence summary]

**Pattern:** [identified pattern]

**Key Insight:** [most important takeaway]

**Recommendation:** [what to do]

**Overall Confidence:** [0.0-1.0] — [brief explanation why]

---

## Key Claims with Confidence

| Claim | Confidence | Reasoning |
|-------|------------|-----------|
| [claim 1] | 0.X | [brief reason] |
| [claim 2] | 0.X | [brief reason] |
| [claim 3] | 0.X | [brief reason] |

---

## Uncertainties & Blind Spots

**Top 3 Uncertainties (would change assessment):**
1. [uncertainty 1]
2. [uncertainty 2]
3. [uncertainty 3]

**What Would Raise Confidence:**
- [information 1] → +0.X
- [information 2] → +0.X

**Blind Spots of This Analysis:**
- [Known blind spot from expert's blind-spots.md]
- [Situation-specific limitation]

---

## Epistemic Audit

**Hammer Check:** [Framework projection risk assessment]

**Before You Act — Investigate These:**
1. [Investigable question] — [what it would change]
2. [Investigable question] — [what it would change]
3. [Investigable question] — [what it would change]
```

### Confidence Level Criteria

| Level | Conditions |
|-------|------------|
| **High** | Pattern clearly matches + Information sufficient + Single expert adequate |
| **Medium** | Pattern matches but gaps exist OR Multiple experts needed |
| **Low** | Pattern unclear OR Information severely lacking OR Edge case |

**Principle:** High confidence → concise confirmation. Low confidence → full disclosure. Don't over-disclose when confident; don't under-disclose when uncertain.

---

## References

For detailed implementation of each step:
- `references/rpd-model.md` — Full RPD model explanation (Gary Klein)
- `references/communication-frameworks.md` — Step 0 inquiry and escalation logic
- `references/insight-paths.md` — Triple Path model details
- `references/epistemic-audit.md` — Step 5 design rationale and calibration examples
- `references/output-examples.md` — Example analyses

For expert-specific content, see the loaded expert module's references.
