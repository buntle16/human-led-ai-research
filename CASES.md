# Cases

*Where the principles came from. 한국어: [CASES.ko.md](CASES.ko.md)*

These cases are taken from the author's dated working log of one long quantitative market research project carried out with an AI assistant (October–November 2026). Each rule in this repository was written **after** one of these failures, not before.

Strategy details, instrument names, and thresholds are removed. Counts and percentages are kept as logged.

**Read the limits at the end before drawing conclusions.**

---

## Case 1. The charter existed, and the drift happened the same day

**Principles 1, 7, 8** · 10 November 2026

**Situation.** In the morning the human fixed the research question in writing: *the same entry signal fires; some trades win and some lose. Was the difference already there before entry?* The document said the AI may not change this question.

**What happened.** About five hours later the AI set the first task of the next session to calibrating a classification tool for the live system. Useful work, but it was tool-building, not an answer to the question. The human's reaction, as logged: "You keep drifting somewhere else." and "We have a charter. Why is this happening?"

**Cause, as recorded.**
1. The AI read the charter at the start of the session, then followed the "next step" line it had written itself at the end of the previous session.
2. It promoted the human's most recent side instruction to the main line of work.
3. It changed method without reporting the change.

**Rule that followed.** Every task instruction starts with two lines: the research question, and which part of the question this task answers. If the second line cannot be written, the task goes to a parking list.

**Lesson.** A charter that is read is not a charter that is checked against. Writing the rule down did not prevent the failure.

---

## Case 2. The AI's measuring stick erased a real difference

**Principles 2, 5, 6** · 10 November 2026

**Situation.** To compare winning and losing trades, the AI chose a normalization, a threshold, and a "length of consecutive difference" score. The human had not asked for these specific choices.

**What happened.** Result: no variable survived in any subgroup. The human said: "Something is wrong. There clearly was a difference."

**Check.** The human was right.
- A raw gap between the two groups' medians (15.5 vs 18.7, a 3.2-point difference) had been compressed to an effect size of 0.09 by the normalization.
- The length score was measuring how smooth each variable was, not how strongly the groups differed. Under random shuffling, the baseline length ranged from 3 to 30 depending on the variable.

**What was withdrawn.** The interpretation ("there is no difference"), not the observation.

**Rule that followed.** Before changing a method, the AI reports four things: what is wrong with the current method, why the new one, what it does to earlier findings, and what the new method can and cannot show. The AI does not set thresholds on its own.

---

## Case 3. The answer key leaked into the test, three times in one week

**Principle 9** · 5, 8 and 9 November 2026

**What happened.** The AI evaluated a rule of the form "wait ten minutes, then enter" using outcomes measured from the *immediate* entry price. The table looked clean and monotonic, and the AI wrote it up as a candidate rule.

**Check.** Recomputed with outcomes measured from the actual delayed entry: loss rate 40.8% when waiting, against 31.7% when entering immediately. The rule was worse than doing nothing.

The log records the same class of mistake (outcome information mixed into pre-decision columns) three times in that week. Earlier in the project, a rule that scored 95% in backtest ran at about 50% live; 156 instances of future reference were later counted in the test.

**Rule that followed.** Columns known before the decision and columns describing the outcome never share a table. Every dataset passes a look-ahead check before any analysis starts.

---

## Case 4. A foundational label nobody had opened

**Principles 5, 6, 9** · 10 November 2026

**Situation.** For weeks, every analysis was split into three categories by one label. All conclusions rested on it.

**What happened.** The human asked the AI to open the labeling code. The label was computed from a market snapshot taken *when the script ran*, not at the time of each event. There was no event-time input at all.

**Check.** All results were put on hold and the label was verified by an independent route. Outcome: 16 of 974 events (1.6%) changed category. The direction of the main finding held. One headline figure moved from −53.2 to −41.0.

**The human was corrected too.** The human had expected that figure to stay unchanged. It did not. The note written that day: "Keeping the conclusion is not keeping the number. The goal is not to defend the conclusion but to see whether it survives the new label."

---

## Case 5. Three changes in one pass, fourteen versions in one day

**Principles 3, 4** · 30–31 October 2026

**What happened.** In a single pass the AI changed the event definition, the outcome measure, and the filter, then reported that results "got worse". The two numbers being compared came from 24 events and 500 events measured with different rulers. They were not comparable.

That day produced 14 code versions. The next day, five versions of one tool, each revised after looking at results on the same two-day sample. The human: "Stop bumping versions without thinking."

**Cause, as recorded.** Building before reading, and changing several things at once.

**Rule that followed.** One question per pass. The pass condition is written before the result is seen. A comparison table comes before any code.

---

## Case 6. A label was assumed, not opened

**Principle 5** · 8 November 2026

**What happened.** The AI assumed that a code in the trade ledger meant "entered manually", excluded 46 records on that basis, concluded that 43 signals had been missed, and issued a work instruction to investigate.

**Check.** The execution step found zero such cases. The code meant something else. An assumption had been reported as an observation.

---

## Case 7. A question answered with a table

**Principle 10** · 10 November 2026

**What happened.** The human asked a confirming question, roughly "so these were re-sorted, right?" It was a check of their own understanding. The AI replied with a results table and proposed the next stage.

**The human's reply.** "Look at the charter."

**Standing rule, written early in the project.** "Let me think. Don't move me. Before I understand."

---

## Limits of this evidence

- **One person, one project, one line of AI tools.** This is a field record, not an experiment. There is no comparison group.
- **Cases are selected by failure.** Sessions that went well left fewer notes.
- **The log was kept by the AI and corrected by the human.** It was checked against source files, but it is not independent.
- **Rules did not stop recurrence.** Case 3 recurred three times after the rule existed. Case 1 happened hours after the charter was written. The principles reduce the unit of failure; they have not been shown to remove it.
- **Cost is unmeasured.** Approval steps and one-question passes slow the work. How much was not recorded.

If you have a counterexample, or a case where human-led scope control made the work worse, please open an issue.
