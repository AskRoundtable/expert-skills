[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

# Expert Skills

**Expert Roundtable** encodes how domain experts actually think — not their personality, but their cognitive process: the patterns they recognize, the mental models they apply, and the blind spots they carry.

Built on Gary Klein's Recognition-Primed Decision (RPD) model.

> Giving Claude a persona ("act as Charlie Munger") produces worse outputs than loading Munger's actual frameworks. The persona is decoration. The framework is the mechanism.

---

## Performance

Evaluated against baseline Claude (no modules, temperature=0) using a 4-dimension rubric across 3 real-world cases per expert.

| Expert | Domain | Delta vs Baseline |
|--------|--------|-------------------|
| expert-graham | Startups / Growth | +38% to +83% |
| expert-feynman | First Principles / Learning | +38% to +57% |
| expert-naval | Career / Wealth / Life | +38% to +57% |
| expert-kahneman | Behavioral Economics / Decisions | +31% to +63% |
| expert-munger | Investment / Business | +18% to +41% |

---

## Quick Start

**Claude Code:**
```bash
npx openskills read expert-engine,expert-munger
```

**Cursor / Windsurf / any SKILL.md-compatible tool:**
Add the skill files to your context. Always load `expert-engine` alongside an expert module.

**Manual (paste into system prompt):**
Copy the contents of `skills/expert-engine/SKILL.md` and `skills/expert-{name}/SKILL.md` into your system prompt.

---

## Experts

| Module | Domain | Best for |
|--------|--------|---------|
| **expert-munger** | Investment / Business | Investment decisions, business strategy, avoiding costly mistakes |
| **expert-naval** | Career / Wealth / Life | Career decisions, building leverage, long-term thinking |
| **expert-feynman** | First Principles / Learning | Breaking down complex problems, learning new domains, teaching |
| **expert-kahneman** | Behavioral Economics | Decision-making under uncertainty, recognizing cognitive biases |
| **expert-graham** | Startups / Growth | Early-stage startup decisions, founder judgment, growth strategy |

---

## How It Works

Two-layer architecture: a cognitive engine that runs the RPD process, and expert modules that supply domain-specific content.

```
┌──────────────────────────────────────────┐
│              expert-engine               │
│      Gary Klein's RPD: 6-step process    │
│                                          │
│  Pattern Recognition → Mental Simulation │
│  → Anomaly Detection → Insight           │
│  → Epistemic Audit                       │
└──────────────────┬───────────────────────┘
                   │ loads domain content from
        ┌──────────┼──────────┐
        ▼          ▼          ▼
  expert-munger  expert-naval  expert-feynman
  patterns.md    models-core   blind-spots.md
  models-core    blind-spots   ...
```

The engine runs every time. Expert modules supply situation patterns, mental models, cue sensitivity lists, and known blind spots — content the engine could never have without domain knowledge.

---

## More Experts

This repo contains 5 experts. The full system has 85+ experts covering strategy, negotiation, systems thinking, management, health, writing, and more.

→ [askroundtable.com](https://askroundtable.com)
