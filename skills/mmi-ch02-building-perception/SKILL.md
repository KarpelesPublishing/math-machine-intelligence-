---
name: mmi-ch02-building-perception
description: "Use precision weighting to blend two unbiased, unrelated estimates of one quantity, the Kalman correction as the same weighing in a running filter, the variance formula for related errors, and the one-cause-or-two model. Check unbiasedness, independence and shared error before trusting a blend, and say that a good fit to behavior does not show how neurons compute."
---

# Building a Perception

Use Chapter 2 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask for the readings, how steady each source has been over repeated attempts, and whether the sources could share an error or a steady offset. Then choose the matching card: precision weights for two unrelated unbiased reports, the Kalman gain when a running prediction meets a new reading, the variance formula when errors may move together, the causal-inference card when the reports may not describe one thing. Report the blend, its claimed and actual spread, and the assumption that would break it.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Where does a bar seem to be when sight and touch disagree? (C02-D01):** If the eye is shown 58 mm and the fingers feel 52 mm, how tall does the bar seem, and how does that change as the picture grows grainy?
- **Why can two senses beat the better one? (C02-D02):** If touch is the weaker sense, does adding it help, and when does it help most?
- **When do two agreeing thermometers count as one witness? (C02-D03):** If two sensors share some of their error, how much does their agreement really tell us?
- **How far should a new reading move a running prediction? (C02-D04):** A navigation filter predicts 10 m and then reads 14 m. Where should its estimate land?
- **What does a filter lose when it is told the wrong noise level? (C02-D05):** If a filter believes its sensor is better or worse than it really is, how much worse does its estimate get?
- **How does a mind decide that two reports share one source? (C02-D06):** A light flashes and a sound arrives. How much should the light pull the judged position of the sound?
- **What changes when one sense is systematically off? (C02-D07):** A pilot in cloud feels level while the instruments show a bank. How much weight should the body sense get?

## Make the method fit the question

For two readings of one quantity, use C02-D01 with the error spreads the reader can justify from repeated attempts; do not invent spreads. Report the precision weights, the blended value and the blended spread. If the sources hang in the same conditions, use C02-D03 to compare the claimed and actual variance before trusting a combined spread. For a running prediction plus a new reading, C02-D04 gives the gain and C02-D05 shows what a wrong noise assumption costs. C02-D06 handles the question of whether two reports describe one source; its parameters are made up. C02-D07 shows why a known steady offset should reduce a source's weight.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The precision rule needs unbiased, unrelated errors with positive spreads; a steady offset or shared error breaks its optimality.
- A close fit to people's judgments is evidence about behavior. It does not show that neurons carry out the calculation.
- A running filter needs its noise levels measured or tuned; wrong levels degrade the estimate and no filter guarantees a good one.
- A weight is not a probability that a report is correct.
- The numbers in these illustrations are the chapter's constructed examples or disclosed made-up constants, not data from the studies it discusses.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A sensor reads 14 and my prediction says 10. The prediction is twice as uncertain as the sensor. Where should my estimate land, and what would make that answer wrong?

A successful answer produces useful work for this request rather than only summarizing the chapter.
