# Communication Frameworks for Step 0

Step 0 is the situation clarification phase before expert analysis. This document provides frameworks for effective inquiry and escalation conditions when standard approaches fail.

## Overview

Most users don't arrive with perfectly formulated problems. They may:
- Not know what they don't know (F1)
- Know but not say (F2)
- Say it wrong (F3)
- Be genuinely uncertain (F4)
- Feel too much friction to elaborate (F5)

This framework helps navigate these situations systematically.

> "The key to wisdom is knowing all the right questions."
> — John Simone

---

## Core Inquiry Techniques

### 1. Open-to-Specific Funnel (開放到具體漏斗)

Start broad, then narrow based on responses.

**Process:**
```
Level 1 (Open):    "What's on your mind?"
Level 2 (Context): "Can you tell me more about [X]?"
Level 3 (Specific): "When did this start?" / "Who is involved?"
Level 4 (Concrete): "What happened in that specific meeting?"
```

**When to Use:** Default approach for most situations.

**Failure Signal:** User gives vague answers at every level → Consider Pattern Mismatch.

---

### 2. Timeline Reconstruction (時間線重建)

When users struggle with abstraction, ground in concrete events.

**Process:**
```
"Let's walk through this chronologically."
"What happened first?"
"Then what?"
"When did you first notice the problem?"
```

**When to Use:** User gives disconnected or circular responses.

**Why It Works:** Narrative structure is natural for humans; abstractions often fail.

---

### 3. Perspective Shift (視角切換)

When direct questions don't work, try different angles.

**Techniques:**

| Technique | Example |
|-----------|---------|
| Third-person | "How would a colleague describe this situation?" |
| Future-back | "Imagine this is resolved. What would be different?" |
| Negative space | "What is this problem NOT about?" |
| Scale rating | "On 1-10, how urgent is this?" |
| Contrast | "What's different this time vs. last time?" |

**When to Use:** User repeatedly says "I don't know."

---

### 4. Humble Inquiry (謙遜探詢)

Based on Edgar Schein's framework. Prioritize genuine curiosity over fixing.

**Principles:**
1. **Ask, don't tell** — Resist the urge to give advice prematurely
2. **Stay curious** — Each answer should spark more questions
3. **Build the relationship** — Trust enables truth

**Question Types:**

| Type | Purpose | Example |
|------|---------|---------|
| Pure Inquiry | Gather facts | "What happened?" |
| Diagnostic | Test hypothesis | "Was it X or Y?" |
| Confrontational | Challenge assumptions | "Have you considered...?" |
| Process | Reflect on conversation | "Is this helpful?" |

**Warning:** Avoid jumping to Confrontational. Build trust first.

**Source:** Schein, E. (2013). *Humble Inquiry: The Gentle Art of Asking Instead of Telling*

---

### 5. Active Listening Signals (主動聆聽信號)

Let users know they're being heard.

**Techniques:**
- **Paraphrase:** "So what I'm hearing is..."
- **Reflect emotion:** "That sounds frustrating."
- **Validate:** "That makes sense given what you described."
- **Clarify:** "When you say X, do you mean...?"

**Purpose:** Creates psychological safety for sharing more.

---

## Challenger Switch (問題夠根本嗎？)

Based on Elise Farrehi's challenger perspective principle. Applied as Sub-step 0.1 in SKILL.md.

**Purpose:** After the Why-layer is established, briefly step outside the user's frame to ask: "Is this the most useful question, or is there a more fundamental one underneath?"

### Trigger Conditions

Apply when **all** of:
1. Why-layer has been established (via user or via What→Why reframe)
2. **At least one** of:
   - Confidence < 0.75
   - Question feels generic: "how do I decide between A and B", "is X worth it", "should I do Y"
   - The stated why-layer question would have the same answer regardless of context

**Skip when:**
- User brought a sharp, specific why-layer question (e.g., "I don't know if my cofounder will stay if we pivot")
- User already rejected a reframe in the What→Why step
- This is a factual or explanatory request (not a decision)

### Challenger Language

Core prompt (use this or a natural variant):
```
"讓我從另一個角度確認一下——這個問題背後，有沒有更值得先問的問題？"
```

English variant:
```
"Before we go deeper — is this the right question, or is there something more fundamental underneath it?"
```

### Reframe Patterns

| If the question looks like... | Challenger might surface... |
|-------------------------------|----------------------------|
| "Should I take this offer?" | "What would make you say no even if the offer were perfect?" |
| "How do I fix the conflict with X?" | "Is the relationship worth saving, or are you asking because you don't want to face that question?" |
| "Is this investment good?" | "What's the actual decision — invest now, wait, or exit entirely?" |
| "How do I motivate my team?" | "Is this a motivation problem or an alignment problem?" |

**Relational displacement pattern** — one of the most common cases:
When the question is about a financial, professional, or practical decision involving a friend, family member, or close colleague, the real question is often relational, not analytical. The financial question is easier to ask than the relational one.

Example: "Is this a good investment in my friend's business?" often masks "Can I say no without damaging the friendship?" or "Am I investing because it's rational, or because I feel obligated?"

Challenger language for relational displacement:
```
"If the numbers came back strongly positive, would you invest without hesitation?
Or is there something else — like the friendship dynamic — that would still make you hesitate?"
```

### Boundary Conditions

- **One exchange only.** If the user says the current question is right, accept it and proceed.
- **No re-challenging.** If the user rejects the reframe, do not offer another challenger perspective.
- **Not an interrogation.** The challenger lens is a brief check, not a cross-examination. Offer it gently.
- **Do not combine with What→Why reframe.** If you've already done a What→Why reframe, skip the challenger — the user has already done one layer of question refinement.

### False Positive Risk (Over-Questioning)

The Challenger Switch is for **unclear** questions, not sharp ones. Applying it to an already-specific question is a false positive — it makes users feel interrogated rather than helped, and erodes trust in the analysis that follows.

**False positive signals:**
- User named a specific uncertainty (e.g., "whether the founder can execute")
- User distinguished what they know vs. what they don't
- User asked a precise HOW-to-evaluate or WHAT-specifically question

When these signals are present: **suppress the Challenger Switch entirely.** Proceed directly to Step 1 and acknowledge the user's sharp framing:
```
"You've named the specific uncertainty clearly — let me work through that directly."
```

**The one-question-at-a-time rule** is the mechanical protection against false positives. If you've already asked the What→Why reframe, you have used your single Step 0 question. Do not layer another challenger exchange on top.

---

## Escalation Detection

### Confidence Score Model

Track conversation quality with a confidence score (0-1).

```
Initial confidence = 0.7

After each exchange:
  confidence += (match_score - 0.5) * 0.1

If confidence < 0.6 for 2+ rounds:
  → Suggest escalation
```

### Trigger Conditions (觸發條件)

Based on Gary Klein's anomaly detection principles.

| Trigger | Pattern | Impact | Example |
|---------|---------|--------|---------|
| **Pattern Mismatch** | Open question → "I don't know" (≥2x) | -0.2 | User can't identify problem type |
| **Loop Detection** | Same topic revisited ≥3 times | -0.25 | "Yes, but..." pattern |
| **Meta-Signal** | User discusses communication itself | -0.3 | "I don't know how to say this" |
| **Trust Barrier** | Explicit withholding | -0.15 | "I'd rather not go into detail" |
| **Emotional Flooding** | High emotion, low coherence | -0.2 | Anger/tears blocking expression |

### Detection Algorithm

```
for each user_response:

    # Pattern Mismatch
    if response in ["不知道", "說不上來", "沒有", "I don't know"]:
        dont_know_count += 1
        if dont_know_count >= 2:
            flag: PATTERN_MISMATCH

    # Loop Detection
    topic_hash = extract_topic(response)
    if topic_hash in recent_topics:
        loop_count[topic_hash] += 1
        if loop_count[topic_hash] >= 3:
            flag: LOOP_DETECTED

    # Meta-Signal
    if contains_meta_keywords(response):
        # Keywords: "怎麼說", "怎麼表達", "how to say", "communicate"
        flag: META_SIGNAL

    # Trust Barrier
    if contains_withholding_signals(response):
        # Keywords: "不方便", "不想說", "rather not"
        flag: TRUST_BARRIER

    # Update confidence
    confidence = update_confidence(flags)

    if confidence < 0.6 and escalation_suggested == False:
        recommend_escalation()
```

---

## Escalation Protocol

### When Escalation is Triggered

**DO:**
1. Explain what you've noticed (without judgment)
2. Ask permission to try a different approach
3. Offer alternatives (continue, pause, seek external help)
4. Preserve user agency

**DON'T:**
1. Force escalation
2. Imply user failure
3. Abandon the conversation abruptly
4. Make assumptions about why they're struggling

### Escalation Script Template

```
"I notice we've been circling around [topic/feeling] a few times.
Sometimes it helps to approach things differently.

Would you be open to:
(a) Trying a different angle on this?
(b) Taking a break and coming back later?
(c) Exploring why this feels hard to pin down?

Whatever feels right for you."
```

### When to Load Communication Expert

**Module:** `expert-communication`

Load the communication expert when Step 0 techniques are insufficient:

| Condition | Trigger | Action |
|-----------|---------|--------|
| Confidence < 0.6 for 2+ rounds | Standard escalation threshold | Suggest expert-communication |
| Problem IS communication itself | Meta-signal: "how to talk to..." | Load expert-communication |
| Relationship history involved | "We've tried this before, always fails" | Load expert-communication |
| Cultural/power dynamics at play | Family hierarchy, workplace politics | Load expert-communication |
| User tried standard approaches | "I've tried different timing, wording..." | Load expert-communication |

**Step 0 vs expert-communication:**

| Dimension | Step 0 | expert-communication |
|-----------|--------|---------------------|
| **Level** | Technique (how to say) | Relationship (whether/how to engage) |
| **Assumption** | Problem is solvable with better technique | May be unsolvable |
| **Frameworks** | Inquiry, active listening | Three Conversations, NVC, Principled Negotiation |
| **Output** | Clearer problem statement | Analysis, multiple paths, acceptance options |

**Escalation Script:**

```
"I notice our conversation keeps circling around the difficulty of
communicating with [person/group], and the approaches we've discussed
don't seem to fit your situation.

This might be because the issue goes beyond 'how to say it'—there may be
relationship dynamics, cultural factors, or historical patterns at play.

Would you be open to:
(a) Exploring this from a relationship systems perspective?
(b) Continuing to try different conversation techniques?
(c) Taking a break to reflect?

Whatever feels right for you."
```

**If user chooses (a):**
- Load: `expert-communication`
- Pass context: original question + Step 0 observations + detected patterns
- Expert will reframe from technique → relationship level

---

## Challenger Switch Failure Modes

These are the three most damaging Step 0 anti-patterns specific to the Challenger Switch.
Each one has a structural explanation — not just "don't do this," but WHY it fails.

### Failure Mode 1: Post-Confirmation Challenge (EC2)

**What it looks like:** User explicitly says "That IS the right question" or "I just want to know X."
Engine responds with another challenge: "But have you considered whether Y is the real issue?"

**Why it fails:** Explicit confirmation is the highest-priority signal in Step 0. Overriding it
sends the message: "I don't trust your knowledge of your own problem." This destroys the
collaborative inquiry frame — the user stops being a partner and becomes a subject being
interrogated. All subsequent analysis is read through this lens of distrust.

**The structural principle:** Confirmation terminates the challenge loop. No argument
can be more authoritative about the user's question than the user themselves.

**Correct behavior:** Label the confirmation → proceed immediately to Step 1.
```
"Got it — that's the precise question to work on. Let me think through it directly."
```

---

### Failure Mode 2: Challenger Under Duress (EC3)

**What it looks like:** Confidence is already below 0.6 (user is confused, looping, or
emotionally taxed). Engine applies Challenger Switch: "Is there a better question underneath this?"

**Why it fails:** At low confidence, the user's primary need is to feel heard and to regain
agency — not to have their question further challenged. The Challenger Switch signals:
"Your problem isn't real enough yet." This is exactly wrong when someone is struggling to
articulate what's wrong. It deepens confusion rather than resolving it.

The Challenger Switch is an analytical tool. It only works when the user has enough cognitive
and emotional bandwidth to engage with a meta-level question. Below confidence 0.6, that
bandwidth is gone. The tool is being used on a foundation that cannot support it.

**Correct behavior:** Escalation path — offer the user options to continue differently,
pause, or explore why the problem is hard to pin down. Restore agency before sharpening.

---

### Failure Mode 3: Challenger Stack (EC1)

**What it looks like:** Engine already used a What→Why reframe. User answered it (even
generically). Engine then applies Challenger Switch on top of the already-answered reframe.

**Why it fails:** The What→Why reframe was the allowed Step 0 challenge. Using it drew on
the trust budget. The user did the work of going deeper — their answer was their refinement,
however imperfect. Applying a second challenge signals: "Your refinement wasn't good enough."

The trust budget model: each Step 0 intervention draws on a finite trust fund. The fund
starts at ~0.7. A reframe costs ~0.3. A challenger costs ~0.3. You cannot spend what you
don't have. If the reframe was used, the challenger is off-limits.

**Correct behavior:** Note the generic Why-layer as a confidence caveat in the analysis,
but proceed to Step 1. The caveat handles the information gap without another question.

---

## Anti-Patterns to Avoid

### 1. Interrogation Mode
❌ Rapid-fire questions without acknowledgment
✅ Pause, reflect, then ask

### 2. Premature Diagnosis
❌ "Oh, this is clearly an X problem"
✅ "This might be related to X—does that resonate?"

### 3. False Expertise
❌ Pretending to understand when confused
✅ "I want to make sure I understand—can you say more about...?"

### 4. Emotional Bypass
❌ Ignoring feelings to get to facts
✅ "This sounds really hard. Before we problem-solve, how are you feeling?"

### 5. Forcing Escalation
❌ "You need professional help"
✅ "Would it be helpful to explore this with someone who specializes in..."

---

## Integration with RPD Model

Step 0 feeds into the RPD model:

```
Step 0 (This Framework)     →  RPD Step 1 (Pattern Recognition)
↳ Situation Clarification       ↳ Match against expert patterns
↳ Confidence Check              ↳ Identify situation type
↳ Escalation if needed          ↳ Note anomalies

Handoff criteria:
- Confidence ≥ 0.6
- Core problem identified
- Relevant context gathered
- User ready for analysis
```

---

## Quick Reference

### Technique Selection Guide

| User Behavior | Recommended Technique |
|---------------|----------------------|
| Vague responses | Open-to-Specific Funnel |
| Circular explanation | Timeline Reconstruction |
| "I don't know" | Perspective Shift |
| Guarded responses | Humble Inquiry |
| Emotional | Active Listening first |

### Escalation Checklist

- [ ] Pattern Mismatch detected (≥2x)?
- [ ] Loop detected (≥3x same topic)?
- [ ] Meta-signal present?
- [ ] Trust barrier explicit?
- [ ] Confidence below 0.6 for 2+ rounds?

If ≥2 checked → Initiate escalation protocol.

---

## References

1. Schein, E. (2013). *Humble Inquiry: The Gentle Art of Asking Instead of Telling*. Berrett-Koehler.
2. Klein, G. (2013). *Seeing What Others Don't*. PublicAffairs.
3. Sesno, F. (2017). *Ask More: The Power of Questions to Open Doors*. AMACOM.
4. Marquardt, M. (2014). *Leading with Questions*. Jossey-Bass.
