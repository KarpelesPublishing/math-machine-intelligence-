---
name: mmi-ch23-several-minds-help
description: "Use the variance of an average of correlated estimates and the effective panel size to say how much a crowd or an ensemble is worth, choose between a plain average, a median and a geometric mean when errors are lopsided, add an independent check by inverse-variance weighting, and read the evidence on language models that pick the same wrong option and on majority voting over sampled answers. Treat every correlation in these illustrations as chosen, not measured."
---

# When Several Minds Help

Use Chapter 23 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask for the guesses or scores, how each was produced, whether the members learned from the same sources, and how lopsided the errors look. Then pick the card: the variance formula and effective size for how much an average will vary, a median or geometric mean when a few guesses are wildly off, inverse-variance weighting when one source is independent of the rest, and a check on whether the vote's members share the same wrong answer. Report the pooled answer, the effective size under a stated correlation, and the assumption that would break it.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How steady is an average when the guessers share a lean? (C23-D01):** If each guesser's error has variance 1 and any two errors correlate, how much does the panel's average still vary, and what do extra guessers stop being able to fix?
- **How many independent guessers is a crowd worth? (C23-D02):** If 787 guessers share a small error correlation of 0.021, how many independent guessers do they equal, and what happens when a thousand more join?
- **Which average survives a few wildly wrong guesses? (C23-D03):** When a few guesses are off by a whole size class, how far does the plain average move compared with the median and the geometric mean?
- **Why can social influence narrow a crowd without making it more right? (C23-D04):** If every member moves part of the way to the crowd's average, what happens to the crowd's own error and to the members' average error?
- **What does an independent check add that a tenth look-alike cannot? (C23-D05):** For nine models with error variance 1 and error correlation 0.4, what does a tenth similar model buy, and what does an independent check buy?
- **Can independent models agree on a wrong answer by temptation alone? (C23-D06):** If two models never see each other's answers but one wrong option tempts both, how often do they pick the same wrong option?
- **When does a majority vote over sampled answers help? (worst case) (C23-D07):** If a model samples many chains of reasoning and the most common answer wins, when does the vote beat one chain, and when does it make things worse if all wrong chains agree?

## Make the method fit the question

For how much an average will vary, use C23-D01 with the error variance and a stated correlation, and C23-D02 to turn a headcount into an effective size; say the correlation is an assumption. When guesses are lopsided or span orders of magnitude, C23-D03 compares the arithmetic mean, geometric mean and median on a constructed sample. C23-D04 shows why moving toward the crowd lowers the average individual miss without changing the crowd's. C23-D05 gives the variance of a panel and of a panel plus an independent check. C23-D06 shows how independent models can match on wrong options through shared temptation, though not enough to reach the reported figure, and C23-D07 shows the worst case for majority voting, in which every wrong chain gives the same wrong answer. Never present a chosen correlation as a measurement.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The variance formula assumes equal weights, equal error variance and one shared pairwise correlation. It describes how much an average varies across repeated panels, not a bias that all members share.
- The correlation values in these illustrations (0.2, 0.021, 0.4, and neurons' 0.12) are chosen or reported for other purposes. Nothing in the chapter measures the error correlation of Galton's guessers, of a model ensemble, or of a mixed panel of people and machines.
- The reported 60 percent match of wrong options is an average over model pairs on questions both got wrong. It is not the error correlation in the formula and cannot be dropped into it.
- The voting demonstration is a worst case: a vote counts as right only if more than half the chains are right, which is what happens when every wrong chain gives the same wrong answer. Real self-consistency takes the most common answer, so scattered wrong answers can still lose to a right answer with fewer than half the votes. Samples from one model also share its strengths and biases.
- The guess samples and voting populations here are constructed with disclosed seeds and constants. They are not data from the studies the chapter discusses.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> I have 20 model answers to one question and plan to average them. How do I tell whether 20 answers are worth 20 independent opinions?

A successful answer produces useful work for this request rather than only summarizing the chapter.
