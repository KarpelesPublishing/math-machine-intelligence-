---
name: mmi-ch33-what-counts
description: "Use the chapter's formulas and reported figures to read a benchmark score: how a level score and an environment score are built, why one model has two scores under two harnesses, how weights decide a ranking, how a one-factor table can arise with no shared cause, and how a shortcut can inflate a test. Treat every total as an estimate under rules someone chose, and say what must travel with it: the set, the setup, the date and the profile."
---

# What Counts as Intelligence?

Use Chapter 33 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask which tasks, with what weights, on which set, under which harness and effort, on which date. Ask for the profile before the total. Check whether a part of the input alone predicts the answer, whether scores that rise together could come from overlapping causes, and whether the comparison with people was matched. Say that a total is not the thing it names.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **What does a level score reward? (C33-D01):** If a human baseline is 20 moves on a level, how does the agent's move count set its level score?
- **Why is an environment score the smaller of two averages? (C33-D02):** In a five-level environment weighted by level number, how do finishing fewer levels and using fewer moves combine?
- **Can one model have two scores on the same set? (C33-D03):** GPT-6 Astra scored 62.7 and 99.95 percent on the same set. How do the harness and the effort setting each enter?
- **Can the order of two children flip with no change in their scores? (C33-D04):** Two children, P and Q, have made-up scores on two groups of tasks. How does the weight on each group decide who leads?
- **Can a one-factor table arise with no shared die? (C33-D05):** Tests that are sums of overlapping dice correlate. Can the correlations look like one common factor even when no die is common to every test?
- **What does a classifier that never read the premise reveal? (C33-D06):** A classifier that saw only the hypothesis got 67.0 percent right. How does that split a test into Easy and Hard, and what does the split do to a model's overall score?

## Make the method fit the question

For a benchmark score, use C33-D01 and C33-D02 to rebuild it from move counts and weights, and C33-D03 to attach the harness and effort setting to any number quoted for one model. For a total built from groups, use C33-D04 to show how the weights set the order. For scores that rise together, C33-D05 shows that a one-factor table can arise with no common die. For a test whose items may leak the answer, C33-D06 uses the chapter's blind-classifier figures. Always state the set, setup and date with a benchmark number.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The 2026 ARC-AGI-3 figures are quoted from the chapter and its source note as of 2 November 2026, each a single run; standings move, and the companion did not check them against the live leaderboard.
- The five-level environment, the 20-move baseline, children P and Q and the dice tables are constructed or made-up illustrations, not data and not Thomson's tables.
- The weighted-average check of the Easy and Hard scores is the companion's own arithmetic on the chapter's numbers.
- A score near 100 on a benchmark shows high completion and action efficiency under its scoring rule, not general intelligence.
- Scores that rise together fit a common factor, overlapping causes and mutual benefit alike; a model is not a measurement of what is behind them.
- Nothing here is a claim about any person's intelligence.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A leaderboard shows one model at 99.95 percent and 62.7 percent. What must I know before saying which is its score?

A successful answer produces useful work for this request rather than only summarizing the chapter.
