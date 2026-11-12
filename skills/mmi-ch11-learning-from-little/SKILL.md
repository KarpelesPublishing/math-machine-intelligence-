---
name: mmi-ch11-learning-from-little
description: "Use the odds form of Bayes' rule, a steadiness-weighted comparison, the rule of succession and the 256-rule switch toy to explain how a prior lets a learner reach a confident answer from one or two examples and how the same prior can make a wrong answer look certain. Quote the one-shot character test, the Frostbite manual study and Wason's rule puzzle as reported, and keep the mathematics as a model of reasoning, not a description of a brain."
---

# Learning from Very Little

Use Chapter 11 of *The Mathematics of Machine Intelligence* to answer the reader's question. Use these ideas to ask what prior a confident answer rests on, to choose a test case that separates rival rules, and to read a one-shot result without crediting the whole gap to the prior.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does a picture change the odds between two candidates? (C11-D01):** A picture is explained nine times as well by candidate A as by B, and the odds were even beforehand. What are the odds afterward, and what changes if the prior favored B?
- **Why can fewer misses lose? (C11-D02):** One rival misses the picture on 2 steady cells and another misses on 8 shaky cells. Which should a learner who knows the cells' habits prefer?
- **How often does knowing which cells are steady pay off? (C11-D03):** Over many 20-way trials, how much worse is counting agreements than weighing them, and does the gap shrink when all cells are equally steady?
- **What did the one-shot character test report? (C11-D04):** After one look at a new handwritten character, how often did people, a stroke model and a convolutional network pick its twin wrongly, and how did that change with less background?
- **How much did a manual change a first game? (C11-D05):** How many times higher was the average first-game Frostbite score for players who read a manual than for players with no help?
- **How sure can n successes make you? (C11-D06):** After n successes in a row and no failures, how likely is another success, and how much of that answer is the prior?
- **What does a strong prior cost when it is wrong? (C11-D07):** Two examples fit 64 of 256 possible rules. A learner who favors one-switch rules is nearly certain after them. How does it fare when the hidden rule is one of those, and when it is not?
- **Which test case can separate two rules? (C11-D08):** Several rules explain every example so far. Which new item could the answer actually tell apart?

## Make the method fit the question

Always say what prior or background a one-shot result depends on, and keep reported results separate from constructed toys. Do not credit the full stroke-model gap to the prior, since the chapter says the models also differed in training data. Do not read Laplace's number as a measured chance. Do not describe the human Frostbite comparison as fair without counting what each learner had beforehand.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The stroke model, the Frostbite groups and Wason's students are quoted from the chapter; the companion adds no data about them.
- Simulations and toys are constructed models, not measurements, and the 256-rule toy and the invented prompt are not results from any paper or system.
- A model that predicts behavior does not show that a brain uses the same machinery.
- The rule of succession depends on its uniform prior; other prior counts shown here are this companion's variation.
- Nothing here is a clinical or treatment claim.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A system saw three examples that two different rules both explain and now answers with high confidence. What should I ask it next?

A successful answer produces useful work for this request rather than only summarizing the chapter.
