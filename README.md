# Mental Atlas

**Map any discipline with mental models — in hours, not months.**

A Claude Code skill that applies a four-layer learning framework to any material: book, article, URL, file, or domain name. Instead of summarizing *what* a text says, it extracts *how the domain thinks* — the mental models, schemas, and explanatory frameworks that experts have internalized.

---

## The Problem

Most people read without learning. They collect information — facts, anecdotes, quotes — but can't apply any of it when they face a new situation in the same domain. Reading 10 books on behavioral economics doesn't mean you can predict behavior.

The difference is *structure*. Experts don't know more facts. They have better mental models.

> *A MIT grad student compressed an entire semester of coursework into 48 hours using this method. He never attended a lecture. He passed the exam — and could talk to his advisor.*

## The Framework

Learning = Compression. The higher the compression ratio while retaining predictive power, the better the knowledge.

```
Data/Signal
    ↓
Information (reduces uncertainty)
    ↓
Representation (internal map of the domain)
    ↙              ↘
Schema              Mental Model
(pattern template)  (runnable mechanism)
    ↘              ↙
  Explanatory Framework
  (systematic view of the whole domain)
    ↓
Prediction / Decision / Action
    ↓
Feedback & Revision
```

**Four layers, from atomic to systemic:**

| Layer | What it answers | Example |
|-------|----------------|---------|
| **Representations** | What are the key concepts and their relationships? | "Loss aversion", "reference point", "prospect theory" |
| **Schemas** | What patterns does an expert instantly recognize? | "Endowment effect activation pattern" |
| **Mental Models** | How does it actually work? (input → mechanism → output) | Hyperbolic discounting: why your future self betrays you |
| **Explanatory Framework** | What do the major schools disagree on, and why does it matter? | Kahneman vs Gigerenzen on whether biases are errors or adaptations |

---

## Installation

Requires [Claude Code](https://claude.ai/code).

```bash
# Clone into your Claude skills directory
git clone https://github.com/BhackerJ/mental-atlas ~/.claude/skills/mental-atlas

# The skill is auto-detected by Claude Code
```

Or copy `SKILL.md` manually into any folder inside `~/.claude/skills/`.

---

## Usage

```
/distill behavioral economics
/distill [paste any article or book chapter]
/distill ~/path/to/paper.pdf
/distill https://example.com/article
```

### Output Structure

Every `/distill` run produces 6 sections:

1. **材料定位** — One sentence: what is this, and what layer does it operate at?
2. **Representations** — Key concept table (6–12 terms, definitions, relationships)
3. **Schemas** — 3–7 named patterns (trigger → implication)
4. **Mental Models ×5** — The MIT method: 5 core models every expert has internalized, each with mechanism / key variables / feedback loops / failure conditions
5. **Explanatory Framework** — 3 major disputes, strongest arguments from each side, practical implications
6. **The Compression** — Exactly 3 sentences. The essential structure of the domain.

Plus **10 test questions** that require *applying* mental models — not recalling facts.

---

## Example Output

<details>
<summary><strong>/distill behavioral economics</strong> (excerpt)</summary>

### Mental Models ×5

**Mental Model 1: Dual Process (System 1 / System 2)**
- **Mechanism**: Two parallel processing systems — System 1 (fast, automatic, pattern-matching) and System 2 (slow, deliberate, resource-intensive). Most decisions are System 1; System 2 intervenes only when stakes feel high.
- **Key variables**: Cognitive load, time pressure, emotional arousal, task familiarity
- **Failure conditions**: Experts aren't immune — their System 1 is just faster and more domain-specific, not unbiased

**Mental Model 2: Prospect Theory Value Function**
- **Mechanism**: Utility isn't a function of absolute wealth, but of *change from a reference point*. Loss curves are steeper than gain curves (λ ≈ 2.25).
- **Key variables**: Reference point position, loss aversion coefficient, probability weighting
- **Failure conditions**: λ is not universal — varies by culture, individual, and emotional state

*(3 more models + full output in the skill...)*

### The Compression

Behavioral economics' core contribution is not that people are "irrational" but that their deviations are *systematic and predictable* — which transforms cognitive errors from moral failures into engineering problems. Its practical power lies in a counterintuitive insight: changing environments is more effective than changing people, because behavior is always a joint output of the cognitive system and the choice architecture, not a pure expression of internal preferences. Mastering behavioral economics at its highest level means using it to identify *when and where you yourself are most predictably deceived* — which requires metacognition, not a checklist.

</details>

---

## The MIT Method

The skill encodes this specific workflow used by a MIT graduate student who compressed a full semester into 48 hours:

1. Ask: *What are the 5 core mental models every expert in this field has internalized?*
2. Ask: *What are the 3 biggest disputes in the field, and what are the strongest arguments on each side?*
3. Generate 10 application questions and find answers in the source material
4. When wrong, understand *why* — not just what the right answer is

This is the difference between reading *about* a field and learning to *think in* it.

---

## Why This Approach

Most reading produces information. This skill extracts knowledge — the kind that transfers to new situations.

| Information | Knowledge |
|------------|-----------|
| "Kahneman won the Nobel Prize" | Prospect theory predicts when people prefer sure losses over risky ones |
| "Behavioral economics challenges rational choice" | The dual-process model explains *when* to trust intuition and when to slow down |
| Story about a specific experiment | A reusable mental model that works in new contexts |

---

## License

MIT
