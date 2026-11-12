---
name: mmi-ch14-learning-consequences
description: "Use the temporal-difference error and its update to revise a forecast, see value credit move back along a chain of cues, show why a cue added to an already predicted outcome is learned poorly, apply the Q-learning update, recognize that taking the best-looking noisy estimate overrates it, normalize a game score against random play and a human tester, and read a set of channels with different optimism as a spread of forecasts. Treat the match to dopamine recordings as a model comparison, not a finding that the brain runs one equation."
---

# Learning from Consequences

Use Chapter 14 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask for the forecast, the outcome, what follows the situation, and the learning rate. Then choose the matching card: the prediction error and update for a single forecast, the chain card when value must travel back to an earlier cue, the blocking card when a new cue arrives with an outcome that is already predicted, the Q-learning card when the learner chooses actions, the overestimation card when it picks the best-looking estimate, and the score card when comparing a game score with random play and a human tester. State that a reward is a number the task supplies and that a good update rule does not solve exploration or say whether the score counts what a person wants.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How much should a surprise change a forecast? (C14-D01):** A monkey that has learned a light predicts juice gets juice, or does not. What is the prediction error, and how far does the forecast move?
- **How does credit travel back from the juice to the light? (C14-D02):** If a reward follows the sixth of six cues, how many trials pass before the first cue gains value?
- **Why does a cue added to a predicted outcome teach so little? (C14-D03):** If a noise already predicts a shock, how much does a light added to it learn in eight pairings?
- **How does a learner revise the value of an action? (C14-D04):** Moving left is valued at 2, earns 1, and the best next option is valued at 3. What is the new estimate?
- **Why does trusting the best-looking estimate overrate an action? (C14-D05):** If every action is equally good but the estimates are noisy, how much does the best-looking one overshoot?
- **How good is a game score, counted over random play? (C14-D06):** On Frostbite the 2015 network scored 328.3, random play 65.2 and a human tester 4,335. What share of the human gain is that?
- **Why would many forecasting channels have different reversal points? (C14-D07):** If some channels weigh good news more and others bad news, where does each settle, and which reward sizes flip its sign?

## Make the method fit the question

For one forecast and one outcome, use C14-D01 and report the error, its sign and the new forecast; do not call the error a probability or a feeling. For credit moving back to an earlier cue use C14-D02; for a new cue added to a predicted outcome use C14-D03 and say it shows what blocking would look like, not that animals follow the rule. For a learner choosing actions use C14-D04, and C14-D05 when the best estimate is trusted. C14-D06 normalizes a game score against random play and a human tester. C14-D07 uses constructed reward sizes, not the mice's amounts; it shows why channels with different optimism would have different reversal points. Never present these as evidence that the brain runs one equation.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A match between prediction error and dopamine firing is in sign and timing only; the error has no real units, and the book names a mismatch with early juice.
- The credit chain, blocking and channel pictures are constructed models. They show what the rules do, not that animals or neurons follow them.
- The Rescorla-Wagner rate and the channel step are disclosed made-up constants; the animals' suppression ratios are not fitted.
- The overestimation picture is a statistical illustration with made-up noise, not a measurement of any deep Q-network.
- The Frostbite figures are one game's reported scores; the network's result on other games is quoted from the chapter, not recomputed.
- A reward is a stand-in for a goal. The score a learner raises may not count what a person wants.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A learner forecast 0.4 and then got 1. With a learning rate of 0.5, what is its error and its new forecast, and what would make the update go wrong?

A successful answer produces useful work for this request rather than only summarizing the chapter.
