---
name: mmi-ch01-making-mind
description: "Use the chapter's first ideas: a decoder turns noisy recordings into probabilities, calibration data limits how well it can do that, two unequal sources should be weighted by reliability and not averaged equally, a pair should be compared with its best member, and a rule earns trust by making predictions that people then test. Keep the mathematics as a model of the brain and as a specification of the machine, and never treat a fit to behavior as proof of mechanism."
---

# What Does It Take to Make a Mind?

Use Chapter 1 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what each source reports and how reliable it is, whether their errors are independent, what the best real alternative is, and whether a claim is a measured result, a drawn comparison or an open question. Work the weights and the comparison by hand before running any simulation, and say what was constructed.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does a decoder turn a noisy recording into probabilities? (C01-D01):** A recording lands at one value, and each of three attempts (left hip, neither, right hip) would leave a noisy value near its own center. How likely is each attempt?
- **How much calibration data does a decoder need? (C01-D02):** A decoder learns the typical recording for each attempt from examples. How does its accuracy depend on how many examples it saw, and how noisy the recordings are?
- **Why not give every voice an equal say? (C01-D03):** A person and a machine estimate the same quantity and one is steadier. What does an equal share do to the error spread, and what does a reliability weight do?
- **What did the partnership add? (C01-D04):** A person scores 70 out of 100, a machine scores 80, and together they score 75. Did the machine help?
- **How does a prediction tell two rules apart? (C01-D05):** Sight and touch both judge a bar's height, and the picture can be made grainier. What does each combination rule predict about leaning toward touch, and about how finely the two senses together discriminate?

## Make the method fit the question

For a decoder or a probability from a recording, C01-D01 gives the three-way estimate by hand; C01-D02 shows how calibration data limits accuracy. For two unequal sources, C01-D03 compares equal share with reliability weights and states the assumptions. For any pair-versus-solo comparison, C01-D04 gives the three differences against the best real alternative. C01-D05 shows what predictions a combination rule makes, and why a fit to behavior is not a mechanism.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The decoder, calibration and rule demonstrations are constructed illustrations; none uses the study's decoder, recordings or numbers.
- The reliability-weight rule assumes no steady bias and independent errors; shared errors or a consistent bias can change the answer.
- The 70, 80 and 75 scores are invented, not a study's results.
- The chapter's mathematics for a brain is a model: a close fit to behavior is good evidence about behavior, not proof of how neurons produce it.
- The study of Oskam involved one participant, did not isolate every component, and was not offered as a cure; nothing here is a clinical claim.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A person scores 70 out of 100, a tool scores 80, and together they score 75. Did the tool help?

A successful answer produces useful work for this request rather than only summarizing the chapter.
