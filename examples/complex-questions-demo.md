# Expert System Complex Questions Demo

This document demonstrates the types of complex, high-stakes questions that the Expert Roundtable system can analyze using structured cognitive frameworks.

## Single-Expert Questions

### expert-munger (Investment & Business Strategy)

1. **Multi-factor investment analysis:**
   "A SaaS company has 200% YoY revenue growth but only 60% customer retention, valued at 50x ARR. Three VCs have already invested. Should I invest?"
   - Triggers: Incentive Misalignment, Social Proof Cascade, Circle of Competence
   - Models: Inversion, Margin of Safety, Second-Order Thinking

2. **Incentive structure diagnosis:**
   "My sales team consistently hits quota but customer churn is rising. What's wrong with my incentive design?"
   - Triggers: Incentive Misalignment pattern
   - Models: Inversion ("what would bad incentives produce?"), Second-Order Thinking

3. **Lollapalooza detection:**
   "The entire board unanimously supports this acquisition. Should I be worried?"
   - Triggers: Lollapalooza Effect, Social Proof Cascade
   - Models: Inversion, Common Sense

### expert-naval (Career, Wealth & Life Design)

1. **Career leverage analysis:**
   "I'm a senior engineer earning $150K. Should I pursue management, start a company, or become a content creator?"
   - Triggers: Leverage type identification, Specific Knowledge mapping
   - Models: Principal vs Agent thinking, Wealth vs Status games

2. **Wealth vs. status trade-off:**
   "I have high status at a big company but I'm not learning. A startup offers half the salary but I'd build specific knowledge. How do I decide?"
   - Triggers: Status Game vs Wealth Game distinction
   - Models: Specific Knowledge, Compound Interest of skills

3. **Long-term skill investment:**
   "Which skills will still compound in value 10 years from now given AI advancement?"
   - Triggers: Leverage analysis, technology disruption assessment
   - Models: Specific Knowledge identification, Accountability leverage

### expert-feynman (First Principles & Understanding)

1. **System understanding from scratch:**
   "What fundamental problem does blockchain consensus actually solve? Explain from first principles."
   - Triggers: Cargo Cult detection, First Principles decomposition
   - Models: Feynman Technique, Hidden Assumptions surfacing

2. **Cargo cult detection in ML:**
   "Our ML model has 99% accuracy in testing but performs terribly in production. Where is our cargo cult thinking?"
   - Triggers: Cargo Cult Science pattern, Hidden Assumptions
   - Models: First Principles, Nature Cannot Be Fooled

3. **Complexity simplification:**
   "Why can quantum computing speed up certain problems? Explain so a smart 12-year-old would understand."
   - Triggers: Feynman Technique application
   - Models: Multiple Representations, Honest Ignorance

### expert-kahneman (Decision Quality & Bias Detection)

1. **Sunk cost audit:**
   "We've spent 2 years building this product. Data shows the market doesn't exist, but the team wants to continue. Is this sunk cost fallacy?"
   - Triggers: WYSIATI, Commitment escalation
   - Models: System 1/2 distinction, Prospect Theory (loss aversion)

2. **Confidence calibration:**
   "I'm 90% confident revenue will triple next year. Is my confidence calibrated to the evidence?"
   - Triggers: Overconfidence detection, Planning Fallacy
   - Models: Reference Class Forecasting, Pre-mortem technique

3. **Base rate neglect:**
   "What's the base rate survival for startups like ours? Are our reasons for being 'different' actually valid?"
   - Triggers: Outside View application
   - Models: Reference Class Forecasting, WYSIATI

### expert-graham (Startups & Growth)

1. **Idea validation:**
   "I want to build an AI-powered legal document platform. Is this a tarpit idea?"
   - Triggers: Tarpit Idea detection, Schlep Blindness
   - Models: Do Things That Don't Scale, Market validation

2. **Scaling timing:**
   "We have 50 paying users with high NPS. Should we start scaling or keep doing things that don't scale?"
   - Triggers: Premature Scaling pattern
   - Models: Do Things That Don't Scale, Product-Market Fit signals

3. **Schlep blindness discovery:**
   "What valuable problems are people avoiding because they seem too tedious or unglamorous?"
   - Triggers: Schlep Blindness pattern
   - Models: Earnestness, Organic vs Forced ideas

---

## Multi-Expert Complex Questions

These questions benefit from loading multiple experts simultaneously:

### Question 1: Career Crossroads

> "I'm 35, earning $250K at a big tech company, and I have a B2B SaaS idea. I have 2 years of runway saved. Should I quit and start the company?"

| Expert | Analysis Angle |
|--------|---------------|
| **Munger** | Opportunity cost analysis, Circle of Competence check, Margin of Safety |
| **Naval** | Specific Knowledge vs generic skills, leverage type, Principal thinking |
| **Graham** | Tarpit test, schlep blindness detection, founder-market fit |
| **Kahneman** | Overconfidence audit, base rate survival, planning fallacy check |
| **Feynman** | "Do you truly understand the customer's problem?" First principles test |

### Question 2: Market Disruption Assessment

> "Our industry leader just launched an AI product that does 80% of what we do at 10% of the cost. We have 500 enterprise customers. What's our strategic response?"

| Expert | Analysis Angle |
|--------|---------------|
| **Munger** | Moat analysis, Inversion (how do we lose?), Second-Order effects |
| **Graham** | What would we build if starting fresh today? Pivot vs persist |
| **Kahneman** | Status quo bias, loss aversion in strategy, outside view on disruption |
| **Feynman** | What does the AI actually do vs what people think it does? |

### Question 3: Hiring Strategy Under Uncertainty

> "We raised Series A. Should we hire 20 engineers fast or 5 carefully? Our competitors are growing teams rapidly."

| Expert | Analysis Angle |
|--------|---------------|
| **Munger** | Social Proof Cascade (copying competitors), Incentive Misalignment risk |
| **Naval** | Leverage through people vs code vs media, Principal-Agent problems at scale |
| **Graham** | Do Things That Don't Scale first, premature scaling patterns |
| **Kahneman** | Planning Fallacy in hiring projections, anchoring to competitor actions |

---

## What Makes These Questions "Complex"

The expert system excels when questions have these characteristics:

1. **Multiple valid perspectives** — No single right answer
2. **Hidden assumptions** — Surface beliefs that may be wrong
3. **Cognitive bias risk** — Emotions and biases cloud judgment
4. **High stakes** — Consequences of being wrong are significant
5. **Interconnected factors** — Multiple domains interact (finance + psychology + strategy)
6. **Time pressure vs. information scarcity** — Must decide before all facts are known

---

## System Capabilities

- **Confidence calibration**: Every claim scored 0.0-1.0 with explicit reasoning
- **Blind spot detection**: Each expert flags where their frameworks don't apply
- **Epistemic audit**: The system audits its own reasoning for framework projection bias
- **Judgment filtering**: Three layers (surface recommendation, reasoning, filtered/withheld)
- **Investigable questions**: Always produces 2-3 concrete next steps, not vague advice

## Usage

```bash
# Load engine + one expert
npx openskills read expert-engine,expert-munger

# Load engine + multiple experts for complex cross-domain questions
npx openskills read expert-engine,expert-munger,expert-kahneman,expert-graham
```
