---
name: mmi-ch30-modeling-yourself
description: "Executable demonstrations of Chapter 30: the leftover after subtracting a predicted effect of a movement, why a leftover cannot name its own cause, a sketch of the delayed-touch finding, a forecast-and-senses blend, what a reported shift of felt location would imply, and a surprise reward in raw and learned features."
---

# Modeling Yourself

Use Chapter 30 of *The Mathematics of Machine Intelligence* to answer the reader's question. When a system subtracts a prediction of its own move, check the prediction's gain and show the operator both the prediction and the observation before treating the leftover as the world.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How much motion does a wrong prediction gain invent? (C30-D01):** A camera turns while nothing outside moves. If its prediction of the turn is scaled wrong, how much phantom motion is left over?
- **Can the leftover tell a collision from a bad prediction? (C30-D02):** A system that flags contact when its leftover passes a threshold (here a camera, in degrees; a real arm compares torques) can be fooled. What else produces the same leftover?
- **Why would a late touch feel more ticklish? (C30-D03):** If a self-made touch is turned down in proportion to how well it matches a prediction, how should ticklishness change as the touch is delayed?
- **How should a forecast and the senses share a hand's position? (C30-D04):** A forecast from commands puts the hand at 10 cm and the senses put it at 20 cm. Where does the blend land?
- **What would a shift in felt location mean as a weighting? (C30-D05):** After synchronous stroking, 14 people drifted about 24 cm toward a body seen 2 metres ahead. What weight on the seen body would a blend need?
- **Why does an explorer rewarded for surprise need the right features? (C30-D06):** An agent is paid for prediction error. What happens to its reward when part of its view is static it can never predict?

## Make the method fit the question

Answer from the chapter. Keep the prediction gain (a multiplier on a command's expected effect) apart from the Kalman gain (the share given to the senses). The leftover alone cannot name its cause. The brain side is a proposal and a model.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The camera, the alarm threshold, the delay sketch, the felt-location weight and the reward curves are constructed or the companion's own readings; the studies make none of those claims.
- The ratings, scans and stimulation do not show subtraction, and none of these studies establish experience in a robot or a simulation.
- The delay study reports rank ratings with no values in the chapter; the sketch is a model, not a fit.
- No clinical claim is made about the patient, the stimulation or any treatment.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> Use when a reader wants to see what a system can compute about its own movement and why the leftover needs something else to read it.

A successful answer produces useful work for this request rather than only summarizing the chapter.
