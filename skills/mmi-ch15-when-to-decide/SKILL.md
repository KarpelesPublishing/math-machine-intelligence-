---
name: mmi-ch15-when-to-decide
description: "Use Bayes' rule to read a positive report against a rare condition, signal detection to separate how clear the evidence is from how readily to say yes, a cutoff computed from the costs of each error, an evidence total that drifts to a bound, a lead rule against a fixed count, the reward rate that prices waiting, and a sampler that stops when its tally settles. Say that a settled tally is stable and not necessarily true, and that fits to monkeys' behavior and firing are fits to a model."
---

# When to Decide

Use Chapter 15 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask for the prior (how common the event is where the test is used), the hit and false-alarm rates for that population, the cost of each kind of error and the price of waiting. Then choose the matching card: Bayes' rule for what a positive report means, the cost cutoff for where to draw the line, a lead rule or a bound for how long to keep collecting evidence, the reward rate for how the price of time moves the bound. Report the answer, the assumption it depends on, and who supplied the costs.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Why are most positive reports false when the test finds four cancers in five? (C15-D01):** If a test finds 79.2 percent of cancers and wrongly flags 9.6 percent of healthy cases, what share of its positive reports are real when the condition is rare?
- **What does moving the cutoff change, and what does it leave alone? (C15-D02):** If a yes depends on both how clear the evidence is and how readily the judge says yes, which of the two does a looser cutoff change?
- **Where should the cutoff go when a miss costs more than a false alarm? (C15-D03):** A classifier gives a probability that a case is real. If a miss costs 9 times a false alarm, at what probability should it say yes?
- **How does a noisy running total decide when to stop? (C15-D04):** If evidence drifts toward an answer with random jitter, when does it reach the bound, and how often does it reach the wrong one?
- **Can stopping at a lead beat counting a fixed number of votes? (C15-D05):** Judges vote one at a time. Does stopping when one answer leads by three beat taking nine votes and counting them?
- **How does the price of time change the best bound? (C15-D06):** A careful setting and a quick setting each earn correct answers. Which earns more per second, and does it depend on the delay between trials?
- **When does a sampler stop, and does a settled tally mean it is right? (C15-D07):** A language model is asked one question again and again. How many samples does a settle-and-stop rule draw, and how often does it stop on the wrong answer?

## Make the method fit the question

For a screening or alarm question, use C15-D01 with the prior and the rates for the population in question; report the share of positives that are real, not the test's hit rate. Use C15-D02 to separate evidence quality from the cutoff. Use C15-D03 to compute a cutoff only from costs and a probability the reader can defend as calibrated; do not invent costs. For a stopping question use C15-D04 for the drift-to-bound picture, C15-D05 for a lead rule against a fixed count, and C15-D06 to show how the delay between trials moves the best setting. C15-D07 shows a settle-and-stop sampler; its estimate is a stated reading, and it cannot detect a shared mistaken source. Always name who sets the costs and the bound.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- Bayes' rule needs a prior and rates that describe the population under consideration; an individual clinical judgment needs rates and context that fit that person, and nothing here is medical advice.
- The detection curves assume two bell-shaped evidence heaps of equal width; outside that model the sharpness number can depend on the cutoff.
- A cost cutoff is only as good as the stated costs and the claim that the probabilities are calibrated.
- A drift-diffusion model is a theory fitted to summarize behavior and firing. The monkey recordings are correlations, and nothing here shows that the brain computes a bound or runs Wald's test.
- The lead rule and the sampler are simplified toy versions. Wald's optimality proof covers two simple hypotheses with independent identically distributed observations, and the sampler's estimate here is the companion's reading of the chapter's description.
- A tally that settles is stable, not necessarily true: votes that share one mistaken source repeat the mistake.
- The numbers are the chapter's quoted figures or disclosed constructed values, not data from the studies it cites.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A screening test finds 79 percent of cases and flags 9.6 percent of healthy people, and the condition affects 1 person in 100. A positive report arrives. How much should it change my mind, and what would change the answer?

A successful answer produces useful work for this request rather than only summarizing the chapter.
