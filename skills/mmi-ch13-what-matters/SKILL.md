---
name: mmi-ch13-what-matters
description: "Use four value rules to see what a chosen scoring scheme assumes: a logarithm of wealth, a reference point with a value curve, a score that depends on bodily state, and a comparison rule that learns scores from a person's choices. Check what the scheme builds in, which part of it does the work, and say that fitting choices does not show that a brain computes the rule or that a machine feels the score."
---

# What Matters to a Mind?

Use Chapter 13 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the outcomes are measured from (wealth, a reference point, a bodily state, or a person's comparisons), then choose the matching card: the logarithm when the same gain should matter less to someone who has more, the reference-point curve when framing as gain or loss may change the choice, the drive model when the body's needs change a goal's worth, the comparison rule when only a person can say which of two outcomes is better. Say which part of the rule does the work, what the person or designer chose, and what choices would show the rule is wrong for this case.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Why does the same gain count for less when you already have more? (C13-D01):** A gain of 1,000 ducats scores differently at different starting wealth, and so does a ticket that pays 0 or 20,000. How does the logarithm make the same ticket worth more to some holders?
- **Which part of the model makes a loss frame choose the gamble? (C13-D02):** Two groups face the same final amounts but one hears gains and the other losses. A curve measured from a reference point can reproduce the majority choices, and the question is which of its features does the work.
- **How can the same food be worth something, nothing, or less than nothing? (C13-D03):** A model body scores an outcome by how far it moves the body toward its set points. What does three units of food score when the body is hungry, full, or thirsty?
- **How do two scores become a predicted preference? (C13-D04):** A model gives clip A a score of 2 and clip B a score of 1. What chance does it give that a person prefers A, and what happens if every score shifts?
- **How much comparing does it take to recover a score gap? (C13-D05):** Learning runs the other way from the preference rule: given a person's comparisons, the system adjusts scores to account for them. How close does a score gap get as comparisons accumulate?

## Make the method fit the question

For how much the same gain matters at two wealth levels, use C13-D01 and say the logarithm and its steepness are assumptions. For a gain versus loss framing, use C13-D02 and report which choice comes from the reference point and the curve's bend and which from the loss weight. For a need that changes a goal's worth, use C13-D03 with the stated set points and say the model is a specification, not a claim about a body. For preferences between two options, C13-D04 gives the predicted chance from two scores and C13-D05 shows how a score gap is estimated from comparisons and how slowly the error shrinks. Never describe the scores as the person's feelings.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A score is a designer's choice. Fitting a curve to choices does not show that a brain computes it, and no demonstration here measures feeling.
- The wealth and prize figures, the square-root value curve and the drive example are the chapter's constructed illustrations, not data and not fitted to the studies it discusses.
- The ticket worth is the companion's computation from the chapter's logarithmic rule. It is not a figure from Bernoulli, whose argument was not a recorded sale.
- The framing study gave different questions to different people with hypothetical money, so it does not show one person reversing a choice.
- The comparison simulation has one made-up score gap. It does not reproduce the hopper study, which trained a reward model with a neural network on clips.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A system must rank outcomes for different people or for one body in different states. Which value rule fits, what does it assume, and how would I find out whether it is wrong?

A successful answer produces useful work for this request rather than only summarizing the chapter.
