---
name: mmi-ch04-expecting-world
description: "Use the residual from a straight-line guess, the settling rule that weighs an input against an expectation by reliability, the delta-rule learning rate in steady and changing worlds, and the difference between surprise and information gain. Say that a prediction error does not say why it is large, and that the brain evidence for predictive coding is partial and disputed."
---

# Expecting the World

Use Chapter 4 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the guess is, how reliable it has been compared with the new reading, and whether the world is steady or changing. Use the residual when a sender and receiver share a guess, the settling rule to weigh an expectation against an input, a learning-rate comparison when the question is how far to move a forecast, and the surprise-versus-information card before rewarding a system for prediction error. Remember that a large residual does not say why it is large.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How much does a shared guess leave to send? (C04-D01):** A sender and receiver share a guess for the center spot from its neighbors. If the neighbors read 10 above their usual level, what is sent when the center reads 22, or 27?
- **How does a machine fit the guess, and how much does it save? (C04-D02):** If a machine counts how a center and its neighbors moved together over many examples, what guess does it fit and how much of the spread is left in the residuals?
- **Why would a surround weaken and spread in dim light? (C04-D03):** If each receptor's reading is noisier, how should a guess weigh its neighbors?
- **Where does an estimate settle between the input and the expectation? (C04-D04):** If the input says 12 and the expectation from above says 2, where should the estimate land when one source is less reliable?
- **How far should a surprise move the next prediction? (C04-D05):** A color usually wins, and today it lost. Should the prediction move a lot or a little, in a steady world and in one whose chances change?
- **What happens when an expectation counts for too much? (C04-D06):** If a percept leans on an expected tone, how often will a tone be reported when none was played?
- **Is a surprise the same as something to learn? (C04-D07):** If an agent is paid for its own prediction error, when does the payment stop?

## Make the method fit the question

For a shared guess, C04-D01 gives the residual and C04-D02 shows how a machine fits the guess from data and how much spread the residual keeps. C04-D03 explains why a surround should weaken and spread when its neighbors are noisier. C04-D04 settles an estimate between an input and an expectation using noise variances the reader can justify; do not invent them. C04-D05 compares learning rates in steady and changing worlds. C04-D06 shows how weighting an expectation too heavily raises 'heard' answers whether or not a tone played. C04-D07 separates surprise from information gain; use it before rewarding a system for prediction error.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A residual says how far the guess missed, not why; a road closure, a bad record and ordinary variation can all produce the same miss.
- The straight-line guess is best only under squared error and for the distribution it was fitted on; association does not show cause.
- The settling rule is a simplified one-number form of the update in Rao and Ballard's simulated network, with their prior term left out.
- The brain evidence is partial: a fly's surround, a simulated network matched by eye to one cat cell, and a mouse mismatch result with a rival explanation and an open dispute.
- The studies of learning rates and hallucination-like reports are fits of a model to group choices or reports. They are not measurements of a mechanism, not tests of treatment, and not rules for any individual.
- Simulated is not measured: the simulations here use disclosed seeds and made-up numbers.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My forecast for a delivery was 10 days and it took 14. How much should I change next week's forecast, and what would tell me whether the miss was noise or a change?

A successful answer produces useful work for this request rather than only summarizing the chapter.
