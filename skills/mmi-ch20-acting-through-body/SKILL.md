---
name: mmi-ch20-acting-through-body
description: "Use the second-jump subtraction, the residual split, a delay-aware controller, minimal-intervention control, error-driven adaptation and exact counts to reason about acting when feedback is late and the body or world changes. Say that the brain-side fits are models, that the Oskam paper reported no forward model, and that tiny counts cannot separate nearby rates."
---

# Acting Through a Body

Use Chapter 20 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask for the delay, the gain, and what the predicted feedback is. For a plan from a remembered target, subtract the estimated last move. For a gap between prediction and sensor, say that the residual alone cannot name its cause. For late feedback, compare the plain loop with a loop that models the delay, and for a changed world use an error-driven update and check the aftereffect. Quote counts with their exact range.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does a mind aim the second jump before the first has been seen to land? (C20-D01):** If a second eye jump is planned as the remembered target minus the estimated first jump, how far does it miss when part of the first-jump signal is lost?
- **If sensed feedback differs from the prediction, was it a push or a bad prediction? (C20-D02):** A body sends a command, predicts the feedback, and senses something else. How much of that gap is an outside disturbance?
- **Why does strong correction from late news make a controller swing? (C20-D03):** If the report on position arrives 0.2 s late, how strongly can a plain feedback loop correct before it swings, and what does a model of the delay change?
- **Why does a skilled hand correct some errors and let others go? (C20-D04):** If a controller pays for effort and for missing the task, how much does it correct a direction that hardly matters?
- **Why do reaches bend the other way when a force is switched off? (C20-D05):** If a controller builds a model of a push from its errors, how closely does the aftereffect mirror the first miss, and how does that depend on practice?
- **What can 2 successes in 10 trials tell us? (C20-D06):** If a robot hand completed a task in 2 of 10 real trials, how well does that pin down its success rate, and what would 0 of 10 tell?

## Make the method fit the question

For planning a second move from a remembered target, use C20-D01. For a gap between predicted and sensed feedback, use C20-D02 and say the residual cannot name its cause. For control with late feedback, C20-D03 compares a plain loop with a delay-modelling loop; its plant and delay are constructed. For which errors a controller should fix, C20-D04; for adaptation and aftereffects, C20-D05. For small counts such as 2 of 10, C20-D06 gives the exact range. Never describe the Oskam system as containing a forward model.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The second-jump subtraction is a specification of a plan; the monkey study shows partial changes with a drug that only partly quieted a relay, and other pathways may carry the signal.
- The Oskam paper reports a decoder that times stimulation to his intended step. It reports no forward model, no sensory-loop test and no measure of agency.
- The delay demonstration uses a constructed integrator plant and a delay of 0.2 s; it does not reproduce the 1993 simulation and no cerebellum was tested.
- The minimal-intervention model has made-up weights and no fitted parameters; the reported hand spreads are the chapter's, and the model is not a fit to them.
- The adaptation rule is a constructed error-driven update, not the model of the 1994 paper, which infers a model from behavior.
- Exact ranges for counts describe the trials run; they do not say the trials were representative.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My controller corrects strongly from a sensor that reports 200 ms late and it swings. What does a model of the delay change, and what would a leftover gap between prediction and sensor not tell me?

A successful answer produces useful work for this request rather than only summarizing the chapter.
