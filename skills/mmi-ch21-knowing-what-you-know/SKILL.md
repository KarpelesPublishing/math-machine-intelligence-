---
name: mmi-ch21-knowing-what-you-know
description: "Use the two checks on any stated confidence: sorting (does it put right answers above wrong ones) and calibration (do its numbers match the hit rate), the distance-to-the-line model of confidence, the Brier score as an honest scoring rule, a single-number rescaling of a classifier's scores, and the cost of declining hard cases. Say that a score is a model of behavior and that no study here shows brains use these calculations."
---

# Knowing What You Know

Use Chapter 21 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask for the stated confidences and the outcomes on held-out cases. Compute the sorting score (chance a right answer gets higher confidence than a wrong one, ties half) and compare stated confidence with the hit rate in groups of similar confidence. Choose the fix to match the failure: a rescaling for a calibration gap, a better model for weak sorting. When answers are declined, report accuracy together with the share answered. Say what the numbers do not show.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How sure should an answer be, given how far the evidence is from the line? (C21-D01):** If the evidence lands one unit from the decision line and d-prime is 1.5, what chance should the answer be right?
- **Did Peirce's zero marks carry any information? (C21-D02):** Peirce marked zero (no preference) on 706 judgments and 436 were right. Could a true hit rate of one half produce that?
- **Can confidence sort perfectly and still be wrong about its numbers? (C21-D03):** Ten answers, six right and four wrong. How do sorting and calibration behave as you change the confidence given to each group?
- **Why does an honest probability score best? (C21-D04):** A forecaster believes the chance of rain is 0.7. What does reporting 0.5 or 0.9 cost her, compared with reporting 0.7?
- **Can one number repair a network's overconfidence? (C21-D05):** If a classifier's scores are too sharp, what happens to its calibration error and its predictions when every score is divided by one temperature?
- **When a model declines the hard questions, what does its accuracy mean? (C21-D06):** A model gets 70 of 100 right. If it declines some questions, how does its accuracy on the rest change?

## Make the method fit the question

Use C21-D01 for how confidence should depend on distance from a decision line and d-prime. Use C21-D02 only to read Peirce's printed tallies; it is not a re-analysis. Use C21-D03 to separate sorting from calibration on any list of confidences and outcomes. C21-D04 shows why the Brier score rewards honest probabilities and compares it with log loss. C21-D05 is a seeded simulation of one-number rescaling: say it is constructed. C21-D06 shows why accuracy on answered cases must be paired with the share answered.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The distance-to-the-line formula assumes equal-scatter bell-shaped evidence, equal prior chances and a line halfway between; it is a model, and Peirce and Jastrow fitted a different formula to their marks.
- A confidence number can sort well and be miscalibrated, or be calibrated and sort nothing; check both.
- A proper scoring rule rewards honest reports in expectation. It does not guarantee a system reports honestly or believes accurately.
- The temperature-scaling simulation is built so that one temperature is correct; it shows the mechanism, not how any real network behaves, and the 16.53 to 1.26 percent figures are Guo and colleagues' reported results.
- Accuracy on answered cases says nothing without the share answered.
- No study in the chapter shows that brains and machines make confidence the same way.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A classifier says 90 percent on every case it gets right and 80 percent on every case it gets wrong, and it is right 6 times in 10. Is its confidence trustworthy?

A successful answer produces useful work for this request rather than only summarizing the chapter.
