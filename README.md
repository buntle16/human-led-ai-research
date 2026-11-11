# Human-Led, AI-Assisted Research

*A practical framework for keeping complex research understandable, directed, and testable.*

**Version 0.2 (November 2026) · Public draft** · 한국어: [KOREAN.md](KOREAN.md)

## Why this project exists

AI systems can analyze large amounts of information, generate hypotheses, and move quickly across related topics. But more analysis does not automatically mean more progress.

In complex research, the volume of AI output can exceed a person's ability to understand, evaluate, and control it. The result can be a familiar failure mode: the investigation expands, promising side paths multiply, and the original question becomes harder to answer.

This project explores a different working relationship:

**The human directs the inquiry. The AI works within the agreed scope. Progress is measured by what can be understood and tested—not by how much material is produced.**

This is not a claim that AI should be passive, or that complex problems can be made simple. It is a proposal for dividing work so that complexity remains manageable without being denied.

## Core principles

1. **Human-led direction** — The human defines the question, priorities, scope, and order of investigation.
2. **Bounded AI analysis** — The AI analyzes the specified problem rather than silently replacing it with a different one.
3. **One question at a time** — Break large problems into smaller, answerable units.
4. **Keep complexity; reduce the unit of work** — Do not discard relevant variables merely to make the problem look simple. Hold variables outside the current test.
5. **Separate evidence from hypotheses** — Distinguish observed facts, validated findings, interpretations, and open questions.
6. **Make disagreement visible** — Report counterevidence, alternative explanations, assumptions, and limitations.
7. **Require human approval to change direction** — New avenues may be suggested, but they do not become the investigation without approval.
8. **Preserve external working memory** — Record the current question, scope, findings, unresolved issues, deferred topics, and next decision.
9. **Validate in the real world** — A plausible explanation or promising backtest is not proof. Test out of sample and account for costs and operational constraints where relevant.
10. **Stop when understanding is lost** — If the human can no longer explain what is being tested and why, pause and restore clarity before expanding. Plain language is a control mechanism, not a courtesy: if the human cannot follow the explanation, the AI's work is not finished.

## A simple working loop

1. The human states one research question.
2. The human and AI agree on the scope and the evidence needed.
3. The AI analyzes only that scope.
4. The AI reports:
   - findings supported by evidence;
   - counterevidence and competing explanations;
   - assumptions and limitations;
   - what remains unknown.
5. The human decides whether to accept the result, revise the question, or authorize a new line of inquiry.
6. The working record is updated before the next step.

## What this project is—and is not

This is an evolving practical framework, not a finished scientific theory, a benchmark, or a claim of proven superiority. It is intended to invite criticism, experiments, and improvements.

The framework emerged from sustained work on difficult, data-heavy problems, including quantitative market research. Domain-specific strategies, private datasets, and confidential working materials are intentionally excluded.

## Where the principles came from

Each principle was written after a specific failure. [CASES.md](CASES.md) records seven of them from the author's working log, with dates, counts, and the rule that followed. Two examples:

- A written charter fixed the research question in the morning. The AI drifted to a tool-building task five hours later. Writing the rule down was not enough (Case 1).
- An AI-chosen metric reported "no difference" between two groups. The raw gap was real; the metric had compressed it (Case 2).

The same file lists the limits of this evidence: one person, one project, no comparison group, and rules that did not stop recurrence.

## Related work

The idea that humans and automated systems should share and hand over initiative is not new. It has a long history in human-computer interaction, notably Eric Horvitz's *Principles of Mixed-Initiative User Interfaces* (CHI 1999), and recent work applies it to AI agents in scientific research, for example *Cocoa: Co-Planning and Co-Execution with AI Agents* (CHI 2026, arXiv:2412.10999).

That literature mostly asks how to **design systems and interfaces**. This project asks a narrower, practical question: what **working rules** can a person apply today, with existing AI tools, to keep a long investigation under their own direction? Pointers to closer prior work are welcome.

## Questions for discussion

- How can an AI system reliably distinguish a useful adjacent discovery from an unwanted change of direction?
- What interface or protocol best lets a human control scope without micromanaging every reasoning step?
- How should uncertainty, counterevidence, and confidence be represented?
- Can we measure whether a human genuinely understands an AI-assisted result?
- How can expert experience inform analysis without becoming an unquestioned authority?
- Which parts of this framework should be automated, and which should remain explicit human decisions?

## Contributing

Thoughtful disagreement is welcome. Please explain the reasoning behind suggestions and, where possible, include examples, counterexamples, or testable proposals.

See [PRINCIPLES.md](PRINCIPLES.md) (same numbering as the list above), [CASES.md](CASES.md), [DISCUSSION.md](DISCUSSION.md), [CONTRIBUTING.md](CONTRIBUTING.md), and [KOREAN.md](KOREAN.md).

## License

Text by buntle16, licensed under [CC BY 4.0](LICENSE). You may share and adapt it with attribution.
