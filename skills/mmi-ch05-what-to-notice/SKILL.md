---
name: mmi-ch05-what-to-notice
description: "Use the softmax rule and its spare-slot variant, the divisive-normalization formula with attention gains, and the reported position and look-alike results to reason about how attention is shared out. Say that a weight is a share and not a probability of truth, and that the correspondence between normalization and softmax is mathematical and not evidence of a shared mechanism."
---

# Choosing What to Notice

Use Chapter 5 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what is being weighed, what each score or drive is, whether anything can give weight to nothing, and who supplies the gain: a cue or goal in the cortex models, the model's own comparison in a transformer. Use the softmax card for shares of a budget of one, the spare-slot card to see what changes when 'none of these' is allowed, the normalization card for gains and a constant, and the reported-result cards for position and look-alike effects. Say that a weight is a share, not a probability of truth.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Is turning a stream down the same as dividing a budget? (C05-D01):** If an ignored stream is turned down by a gain, what happens to the attended stream, and what happens when a softmax does the shrinking?
- **What changes when a head gets a spare slot? (C05-D02):** If every available score is poor, can the weights say so, with plain softmax and with a spare slot?
- **How does attention divide a response among rivals? (C05-D03):** Two inputs compete for one response. What happens to each when attention boosts the weaker one?
- **How far did attention move a monkey's cell toward the attended bar? (C05-D04):** One V4 cell fired 11.75 to a vertical bar, 17.80 to a tilted bar and 13.81 to both. How was the pair's response read, and what did attention do to the weights?
- **Why does attention sometimes act like extra contrast and sometimes like a raised ceiling? (C05-D05):** The normalization model predicts that attention can act like extra contrast or like a raised ceiling. How does one formula give both?
- **Why would look-alikes cost more than random passages? (C05-D06):** If one passage holds the answer and the others score near it, how much of the weight does the answer keep?
- **Where in a long prompt did the answer fare worst? (C05-D07):** A model answered 75.8 percent of questions when the answer passage came first among 20 and 53.8 when it came tenth. How large are those gaps against having no passages at all?

## Make the method fit the question

C05-D01 contrasts turning a stream down by a gain with dividing a budget of one. C05-D02 shows plain softmax against a spare slot for equal scores and says what a common score shift does to each. C05-D03 uses the chapter's drives 4 and 1; set sigma to 0 for the softmax limit. C05-D04 quotes the monkey cell and the pooled weights and says what they do not show. C05-D05 shows how one attention gain acts as extra contrast or a raised ceiling depending on how much of the competing pool it covers, in a constructed pool. C05-D06 gives the softmax arithmetic behind the look-alike suggestion without testing it. C05-D07 quotes the position results with a rough noise band that is the companion's own arithmetic.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A weight is a share within one calculation, not the probability that a passage is true; other heads, layers and operations also shape what a model says.
- Divisive normalization turns into softmax when sigma is zero, every gain is 1 and each drive is e to a score. That is a mathematical correspondence, not evidence that a transformer is built like cortex.
- Treisman's slips are consistent with a turned-down ignored stream and with other accounts. Nothing in these studies says a brain uses a gain.
- The monkey result is three monkeys, one weighted-average fit with an offset allowed, and no person or machine data; the pooled weights are not one cell's weights.
- Lost in the middle is one model tested in 2023 at five positions; the study measured answers, not attention weights, and established no single cause.
- The look-alike arithmetic is a suggestion; Cuconasu and colleagues did not test it and could not separate it from a plausible wrong answer.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A language model is given 20 passages and only one contains the answer. How much of its attention weight can the answer passage keep if the others score close to it, and what would tell me the weights are not enough?

A successful answer produces useful work for this request rather than only summarizing the chapter.
