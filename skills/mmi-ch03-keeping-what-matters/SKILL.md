---
name: mmi-ch03-keeping-what-matters
description: "Use the entropy ceiling log2 M, the share-at-or-below response rule, a squared-error alternative, a curve that rescales with its input, the sparse-coding objective with its soft-threshold special case, and the sensitivity and specificity arithmetic behind the mammography results. Say what each rule assumes and what the chapter's studies did and did not show."
---

# Keeping What Matters

Use Chapter 3 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask how many distinguishable levels the channel has, how the inputs are distributed, and what the next stage does with the signal. Use the entropy ceiling for the most bits, the share-at-or-below rule when the goal is to tell inputs apart, the squared-error layout when a later stage must rebuild the input, and the sparse objective when few active elements are wanted. For a screening or alerting tool, convert reported rates into counts before judging it.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How many bits can ten steps carry, and when do they carry them all? (C03-D01):** A cell can signal ten distinguishable levels. If most readings crowd into a narrow band, how much of the 3.32 bits does an evenly spaced layout waste?
- **What does the share-at-or-below rule buy over evenly spaced steps? (C03-D02):** If contrast is mostly small, how does a response built from the share of readings at or below each contrast compare with one spaced evenly across the range?
- **Does telling inputs apart give the same layout as rebuilding them? (C03-D03):** If a later stage must rebuild each contrast closely, where should the step boundaries go compared with the equal-use layout?
- **Why must a response curve stretch when the spread of its input changes? (C03-D04):** If a cell's velocity input doubles in spread, what does it do to a curve that was best before?
- **When does a less exact rebuild beat a more exact one? (C03-D05):** One code rebuilds a patch more exactly but uses many elements; another is less exact but sparse. Which does the objective prefer?
- **What does the sparsity penalty do to a patch's coefficients? (C03-D06):** Given the strength each element would need to rebuild a patch exactly, how many elements stay active as the penalty grows?
- **What do reported sensitivity and specificity mean in counts? (C03-D07):** If marks on a mammogram change sensitivity by 2 points and specificity by 3, how many cancers and how many recalls change per 100,000 exams?

## Make the method fit the question

For a channel with M levels, C03-D01 gives the ceiling log2 M and the bits lost to uneven use. C03-D02 compares evenly spaced steps with the share-at-or-below rule for a stated input distribution; do not assume the distribution. C03-D03 shows that a rebuild goal gives a different layout from an equal-use goal. C03-D04 shows that only the ratio of curve width to input spread matters. C03-D05 and C03-D06 explain the sparse-coding trade and its soft-threshold case. C03-D07 turns reported sensitivity and specificity into counts per 100,000 exams; quote the chapter's observational caveats.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The share-at-or-below rule assumes a continuous input, equal-sized response steps, equal steadiness at every response level, a stable mix of inputs and information as the only goal.
- Laughlin compared curves by eye in six cells of one class in one species; he counted no bits and gave no fit statistic.
- The Laplace world, the logistic curve and the toy patch here are constructed; they are not Laughlin's, Brenner's or Olshausen and Field's data.
- A match between a cell and a code does not show that they use the same algorithm.
- The mammography figures are observational associations from two studies of the software of its era. The screening arithmetic here converts rates into counts and is not advice about any screening decision.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A sensor can report only 8 distinguishable levels and most of its inputs fall in a narrow middle band. Where should it put its levels, and how many bits can it carry at best?

A successful answer produces useful work for this request rather than only summarizing the chapter.
