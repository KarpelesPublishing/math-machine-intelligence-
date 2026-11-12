---
name: mmi-ch34-abilities-work-together
description: "Use the chapter's multiply-and-rescale update, its seed-field ledger, the effective size of reports that share errors, the synergy yardstick and the reported 106-experiment split to reason about what abilities achieve together. Say that a shared formula carries mathematics and not mechanism, that a zero weight stays zero, that related reports count for less than their headcount, and that a pair is judged against its better member."
---

# How the Abilities Work Together

Use Chapter 34 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what options are on the list and whether the right answer could be missing, whether reports share a source, and which comparison is fair for the pair. Compute the effective size before multiplying evidence, compare a pair with its better member and with a relevant alternative, count costs, and say what a study did not test. The mathematics does not say whether a machine experiences anything.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does one clue reweight two explanations? (C34-D01):** Two explanations start with weights. A clue fits one better. What happens when each weight is multiplied by its fit and the weights are rescaled to total one?
- **What does the same update do to a field of seeds? (C34-D02):** Round, wrinkled, speckled and striped seeds leave 1, 2, 4 and 10 offspring per plant. What happens to their shares under repeated multiply-and-rescale?
- **How many independent reports are eight related reports worth? (C34-D03):** If reports share errors, how much does a headcount overstate the evidence, and what caps what more reports can add?
- **Did the pair add anything beyond its better member? (C34-D04):** A person, an AI and the pair take the same task. How is the pair's score judged against the two working alone?
- **How can an average of minus 0.23 hide gains and losses? (C34-D05):** Across 106 experiments pairs trailed the better member by 0.23 on average, yet the pair gained when the person was better alone. How do those fit together?
- **How many questions could a proposed test need? (C34-D06):** The chapter sketches a test on 200 yes-or-no questions with a target gain of five points, and says 200 may be too few. Under what assumptions is it too few?

## Make the method fit the question

For an update from evidence, use C34-D01 and say that a zero weight cannot recover, and that likelihoods must be right and not double counted. C34-D02 repeats the update on the seed ledger. For reports that may share errors, use C34-D03 to compute the effective size before pooling. For a pair against its members, use C34-D04 and compare with the better solo score. C34-D05 reads the reported 106-experiment split. C34-D06 shows how many questions a proposed test needs under stated assumptions; do not present it as a result.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The seed ledger, the 70, 80 and 75 scores, the 200-question test and its assumed accuracies are constructed illustrations, not data.
- A shared formula carries its mathematics and not its mechanism. The match between selection, inference and machine weights is arithmetic, and whether any brain computes this step is open.
- The share-weighted mean of the reported subgroup effects is the companion's own arithmetic; the review pools 370 effect sizes by meta-analysis, so it is not a decomposition of the reported average.
- The power calculation uses a normal approximation and assumed accuracies and correlations. It shows how a proposed design depends on its assumptions, not what any real test would find.
- The assistive-device study discussed in the chapter is not simulated, and nothing here is a claim about any person or a treatment.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> Eight equally noisy reports have error correlation 0.3. How many independent reports are they worth, and what happens if I multiply their evidence as if they were independent?

A successful answer produces useful work for this request rather than only summarizing the chapter.
