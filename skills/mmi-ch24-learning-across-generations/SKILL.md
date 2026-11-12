---
name: mmi-ch24-learning-across-generations
description: "Use the chance a rare answer is missing from a sample, Bayes' rule for an odd clause read by a best-guess or a sampling reader, and the arithmetic of a chain of such readers to say what a chain of learners can lose, keep or settle on. Read the reported chain results (Bartlett's story, a small model retrained on its own text, nine-student chains) at their stated limits, and keep the two-state chain and the copier simulation as the chapter's constructed illustrations, not data."
---

# Learning Across Generations

Use Chapter 24 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask how large each sample is, how rare the detail is, and whether each step sees only the last step's output or can return to the original. Use the missing-answer formula for one step. Use the reader comparison to ask whether the step keeps the likeliest version or samples in proportion to the weights. Report the chance of loss, say that the sample-only copier cannot get the detail back, and name what restores it: links back to the original.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How likely is a rare answer to vanish in one handoff? (C24-D01):** A rare answer has a 1 in 100 chance on each draw, and the next learner trains on 100 draws. How likely is the answer to be missing from the sample?
- **Why does a page carrying the clause favor no clause? (C24-D02):** A reader sees a page with the odd clause. Before reading, the clause was 0.2 likely to be held. Writers copy a held clause 7 times in 10 and add an absent one 3 times in 10. What does the reader believe?
- **Where does a chain of readers end up? (C24-D03):** If every writer sees a page from the writer before and rebuilds a belief, does the clause persist down the chain, and does it matter whether readers take the likeliest version or sample?
- **Does a chain of copiers lose a rare answer, and can the original bring it back? (C24-D04):** A rare answer starts at 1 in 100. Each copier trains on a sample of the one before. How many chains lose it entirely, and what changes if part of each sample comes from the original?
- **What did a model do to its own text, and how bad was the score? (C24-D05):** A small model was retrained again and again on text written by the one before. How did its score on real text change, and what changed when some original data was kept?
- **How many of the 32 chains really moved toward a rising line? (C24-D06):** 28 of 32 chains of students ended on a rising line. Eight chains began on one. How strong is the evidence of a pull toward it?

## Make the method fit the question

For the chance a rare detail is lost in one step, use C24-D01 with the sample size the reader actually uses. For why a minority detail disappears under a likeliest-version rule, use C24-D02 and C24-D03, and state that the numbers are the chapter's constructed ones. C24-D04 shows how often a copier chain loses a rare answer and how drawing on the original helps, as a seeded simulation. C24-D05 and C24-D06 quote reported results: say what each study could not show.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The missing-answer formula assumes independent draws and a copier that produces only answers present in its sample.
- The ghost-clause numbers (prior 0.2, fidelity 0.7) are the chapter's own arithmetic. Nothing was fitted to people.
- The settling result for sampling learners is exact only under stated conditions: every learner samples its belief, all share one prior, and each learner's guess about how data are made is correct.
- The chain of copiers here is a constructed simulation with disclosed seeds. It is not the model-collapse study and not a measurement.
- The perplexity values 60, 52 and 37 are read by eye from a figure; the paper shows one prompt, so its example is a sample of the drift and not a rate.
- The student chains were consistent with a pull toward a rising line; the study did not fit a model to the students and says more data would be needed to confirm convergence.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> I summarize interviews with a model, then summarize the summary. A qualification shows up in about 1 passage in 100, and each step keeps a 100-passage sample. How likely is it to be gone after one step, and what would help?

A successful answer produces useful work for this request rather than only summarizing the chapter.
