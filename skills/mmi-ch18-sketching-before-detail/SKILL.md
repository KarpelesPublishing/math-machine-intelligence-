---
name: mmi-ch18-sketching-before-detail
description: "Use the chapter's pass counts, its running total and leftover, minimum Bayes risk selection and majority voting to explain what a rough-first, sharpen-later method does and what it leaves open, read the reported Sudoku and reaction-time results as reports and not as measurements of how a mind works, and avoid treating agreement among drafts as correctness. Keep the mathematics as a model: no study here tests a person drafting a whole text and sharpening it, and the preprint's numbers are the authors' own."
---

# Sketching Before Detail

Use Chapter 18 of *The Mathematics of Machine Intelligence* to answer the reader's question. Count passes and position-updates before comparing speeds, and remember that a count is not a timing. Check whether a level can overturn an earlier one, because a stack that only adds corrections cannot undo an overshoot. When choosing among several drafts, ask whether the drafts could share a mistake, since agreement measures typicality and not truth.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How many passes does it take to build a text? (C18-D01):** A 16-position text can be built one position at a time, by filling every position in several passes, or level by level. How many passes and position-updates does each take?
- **Can a later level undo an earlier one? (C18-D02):** A target of 0.7316 is described in three levels, each choosing one entry from a list. What are the totals and leftovers, and what happens when level 1 overshoots?
- **Which draft does minimum Bayes risk keep? (C18-D03):** A model writes five one-line summaries of a vote. If we keep the one most like the others, is it the right one?
- **How did the reported Sudoku results compare, and why is one wrong square so costly? (C18-D04):** The preprint reports the share of boards solved by three kinds of model. How much per-square accuracy would those shares imply if squares were independent?
- **What can a vote among drafts never repair? (C18-D05):** Majority voting over final answers is MBR with the simplest similarity. How many voters does it take, and what stops it?
- **How large was the global-precedence gap in Navon's timings? (C18-D06):** People named either the big letter or the small letters of a figure. In which task did the other level slow them down?

## Make the method fit the question

For counts of passes use C18-D01 and say they are counts, not timings. For the running total and leftover use C18-D02, and C18-D03 for choosing among drafts by agreement. For the reported Sudoku numbers use C18-D04 and say what is reported and what is the companion's arithmetic. C18-D05 shows what voting among drafts cannot repair. C18-D06 reports the Navon timings and must not be presented as showing that people draft whole texts.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- Pass and position-update counts are a toy proxy for work; real speed depends on architecture, caching, hardware and overhead.
- The 0.7316 number line is a constructed example, not from the Stanford paper; the paper's levels do not double in size.
- Minimum Bayes risk keeps the most typical candidate, not the best one, and cannot tell which is right; a settled tally is stable, not necessarily true.
- The Sudoku, translation and summary numbers are the preprint authors' own, with one training seed and no error bars in the tables; the rival numbers were copied from another group's paper.
- The implied per-square accuracy treats squares as independent and the shared-mistake vote model is this companion's construction; neither is in the paper.
- No study cited tests a person producing a whole text and then sharpening every part; the link to the machine method is an analogy this book draws.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My system draws several answers and keeps the one most like the others. Does that make the kept answer correct?

A successful answer produces useful work for this request rather than only summarizing the chapter.
