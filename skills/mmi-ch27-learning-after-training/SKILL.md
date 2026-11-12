---
name: mmi-ch27-learning-after-training
description: "Use the low-rank adapter update, the penalty that slows the loss of an old skill, and a small network that forgets and is protected in three ways to compare what each way of changing a trained model costs. Read the taxi-study figures at the limits the chapter gives, keep the brain side as one reported structural result and a proposed model, and say that a deployed chat model does not change its weights when you talk to it."
---

# Learning After Training

Use Chapter 27 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what must be kept (old examples, old weights and sensitivity numbers, or the adapter), what is lost (new skill, old skill, or time), and whether the change can be undone. Use the adapter card for sizes, the penalty card for how far each weight moves, and the toy card for the direction and price of each fix in a small case. Say that the toy is not a published study and does not show that real adapters forget more.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **What does a column times a row add to a layer? (C27-D01):** A layer W is the 3 by 3 grid with top row (1, 2, 3). An adapter adds the column (1, 2, 0) times the row (1, 0, -1). What is the adapted layer, and how many numbers did the adapter hold?
- **How small is a rank-8 adapter on a real layer? (C27-D02):** A square layer with 4,096 rows holds over sixteen million numbers. How many numbers does a rank-8 adapter hold, and when would an adapter stop saving anything?
- **How far does each weight move when a penalty guards the old task? (C27-D03):** Both weights sit at 2 after task A. Task B alone would pull both to 0. The first weight mattered to A (Fisher number 4) and the second hardly did (0.25). With lambda 1, where does each weight settle?
- **What did the taxi trainees' training look like, and what could the scan show? (C27-D04):** Of 79 men starting the training for London taxi licensing, 39 qualified and 20 who returned did not. The qualified men showed more gray matter in the back of the hippocampus. How different was the training of the two groups?
- **In a toy network, what does each fix save, and what does it cost? (C27-D05):** A small network learns task A, is trained on task B (the same cards with the 16 measurements shuffled), and forgets A. Which of replay, a penalty and a small adapter protects A, and at what price?

## Make the method fit the question

For an adapter question, use C27-D01 for the arithmetic of W plus B A and C27-D02 for sizes at real width; an adapter saves numbers only below half the layer width. For protecting an old skill with a penalty, use C27-D03. C27-D04 quotes the taxi-study figures and says what MRI could not show. C27-D05 is the book's toy: report its averages, the price of each fix, and that it is a toy.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A deployed chat model does not change its weights during conversation as far as the public record shows; a note or a retrieved memory changes what the model reads, and retraining changes the weights on a company's schedule.
- The adapter and penalty examples are constructed. The penalty example uses two weights with Fisher numbers 4 and 0.25 and is not a large model.
- The toy network is the book's own simulation, ported here with its protocol. It is not a published result, and its adapter result does not show that real adapters forget more.
- The taxi study measured gray matter in men with MRI. It does not show which cells changed, covers one city and one skill, and a 2013 review questioned part of its analysis.
- Nothing here is a claim about how any brain learns. The brain side is one reported structural result and a proposed mechanism with thin evidence.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A team wants to teach a deployed model a correction without losing what it already does well. They are choosing between a stored note, a small adapter, and retraining with old examples mixed in. What does each cost?

A successful answer produces useful work for this request rather than only summarizing the chapter.
