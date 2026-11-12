---
name: mmi-ch19-spending-thought-wisely
description: "Use the chapter's value of computation, its stopping equation, Chow's reject rule, the cost of time implied by a stopping bound, a one-cue-at-a-time rule and the s1 budget-forcing report to say whether another look is worth its price, when a classifier should decline, and what a reported gain does and does not show. Keep the mathematics as a model: the dopamine, cingulate and time-cost findings are fitted or proposed accounts, and none of the studies shows that a brain computes these formulas."
---

# Spending Thought Wisely

Use Chapter 19 of *The Mathematics of Machine Intelligence* to answer the reader's question. State the payoffs, the chance of each result and the price of a look. Compute what the look could change before paying for it, check whether it could change the best action at all, and remember that the price is supplied by a builder or a person and the benefit by a model that may leave something out. For a classifier, compute the cost of answering against the cost of declining at the confidence it actually has, and say whether that confidence is calibrated.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **What is a forecast worth to a baker? (C19-D01):** A baker earns 10 on a dry day and loses 6 if it rains. What is a perfect forecast worth, and what if a rainy day would still pay?
- **When do several looks pay although the first does not? (C19-D02):** The baker can buy hints about the weather one at a time. When is it worth paying for one, and for more?
- **When should a classifier decline to answer? (C19-D03):** A page reader costs 0 for a right reading, 2 for a reject and 10 for an error. At what confidence should it answer?
- **What price on time does a stopping point imply? (C19-D04):** A chooser looks at hints one at a time and stops when one answer leads by a fixed amount. What cost per look makes that stopping point best?
- **Can a rule that stops at the first deciding cue keep up? (C19-D05):** Take The Best checks cues in order and stops at the first one that separates two objects. How does it compare with using every cue, in a made-up world?
- **How big is two problems out of thirty? (C19-D06):** A model scored 50.0 percent on a 30-problem math test, and 56.7 percent after budget forcing. How large is that gap, and how would it look on a bigger test?

## Make the method fit the question

For the baker's forecast and the formula for the value of computation use C19-D01, and say a forecast that cannot change the choice is worth zero. For several looks and the stopping equation use C19-D02, and C19-D03 for declining to answer. For prices of time implied by stopping use C19-D04 and call the backward reading an extension beyond the paper. C19-D05 is a constructed contest between simple and complex rules. C19-D06 gives scale for the reported s1 gain and must not be presented as a test of it.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The value of computation assumes the price of a look is known and that beliefs are revised correctly by Bayes' rule.
- A forecast can change confidence without changing the best action, in which case its decision value is zero.
- Chow's rule is written for true probabilities; a real system estimates them, and calibration across a group alone does not ensure the best decision.
- The stopping-bound toy uses a constant cost and made-up hints; the studies found a cost of time that was neither zero nor constant, inferred from a fitted model, not measured.
- The Take The Best simulation is a constructed world with made-up cues, not the 83 German cities, and not a test of people; the paper calls its result an existence proof.
- The scale calculation for the s1 report is a yardstick that treats problems as independent draws; it is not the paper's analysis and does not show the gain is or is not real.
- The effort-cost findings are one study of 50 adults and a proposed theory; the source of the cost of effort is, in the chapter's words, unclear.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My assistant keeps asking for more evidence before answering. Is another look worth its price, and who decides the price?

A successful answer produces useful work for this request rather than only summarizing the chapter.
