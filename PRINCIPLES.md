# Principles for Human-Led, AI-Assisted Research

*Version 0.1. The numbering matches the ten core principles in [README.md](README.md).*

## 1. Human-led direction

The human is responsible for choosing what matters, defining the question, setting priorities, and deciding when the investigation changes direction.

The AI may identify overlooked factors or propose alternative questions. It must label these as suggestions, not quietly substitute them for the agreed task.

## 2. Bounded AI analysis

Scope is an explicit agreement. At the beginning of each analysis, state:

- **Question:** What exactly are we trying to find out?
- **Scope:** Which data, variables, period, and methods are included?
- **Out of scope:** What will not be investigated in this pass?
- **Decision sought:** What decision will the result help the human make?

When the scope changes, make the change explicit and obtain approval.

Inside the agreed task the AI should be ambitious: inspect evidence, compare explanations, identify anomalies, calculate, summarize, and challenge assumptions. But it should not treat its ability to generate more analysis as authority to expand the project.

## 3. One question at a time

Break a large problem into smaller units that can each be answered. Finish, or deliberately park, the current unit before opening the next.

Several questions bundled into one pass produce results that nobody can attribute to a single cause.

## 4. Keep complexity; reduce the unit of work

Complex systems contain interacting variables. Simplifying the system by ignoring those relationships can create false confidence.

Instead, reduce the size of each investigation. Examine the variables necessary for the current question, while recording other relevant variables as held, deferred, or not yet tested.

A variable deferred from the current analysis is not declared irrelevant.

## 5. Separate evidence from hypotheses

Use clear labels:

- **Observed:** Directly present in the data or source material.
- **Verified:** Checked against an appropriate source or procedure.
- **Interpretation:** An explanation of what the observations may mean.
- **Hypothesis:** A proposition that still needs testing.
- **Unknown:** Information that is unavailable or unresolved.
- **Contradictory evidence:** Evidence that challenges the current interpretation.

Do not present an interpretation as an observation or a hypothesis as a finding.

## 6. Make disagreement visible

Counterevidence is part of the answer. For each material conclusion, ask:

- What evidence would weaken or disprove it?
- What alternative explanation fits the same observations?
- Which assumptions are doing the most work?
- What relevant evidence is missing?
- Could selection effects, leakage, measurement error, or hindsight explain the result?

The goal is not to manufacture balance. The goal is to expose the strongest relevant challenge to the conclusion.

## 7. Require human approval to change direction

During analysis, the AI may find an adjacent pattern or a potentially important new question. A new discovery does not automatically change the task.

It should place that discovery in a separate section:

**Side finding — not investigated in this pass**

Include why it may matter and what evidence would be needed. Do not pursue it until the human approves.

## 8. Preserve external working memory

For each work session, record:

1. Current question
2. Agreed scope and exclusions
3. Data and methods used
4. Findings and their evidence status
5. Counterevidence and limitations
6. Hypotheses still under test
7. Deferred topics
8. Decision made by the human
9. Next authorized step

The record should be concise enough to be used, not so exhaustive that it becomes another unmanageable dataset.

## 9. Validate in the real world

A pattern found in historical data is a discovery candidate, not proof of a durable effect.

For quantitative or predictive work, validation may require pre-specified tests, out-of-sample evaluation, realistic fees and slippage, robustness checks, and operational testing. The exact protocol depends on the domain.

Do not confuse a high win rate, an attractive chart, or a plausible narrative with positive real-world value.

## 10. Stop when understanding is lost

A result is not operationally useful merely because the AI can describe it.

Before moving on, the human should be able to state, in their own words:

- what was tested;
- what the evidence showed;
- what it did not show;
- what remains uncertain;
- why the next step follows.

If this cannot be done, reduce the explanation, revisit the evidence, or pause.

---

**The governing rule: AI may widen the human's view, but it must not take ownership of the direction.**
