---
name: mmi-ch31-making-information-available
description: "Executable demonstrations of Chapter 31: the arithmetic of exact-match scoring, how much a zero among 655 electrodes can rule out, what a Bayes factor does to odds, the reported effect of workspace slot counts, and what changes when tokens are not independent."
---

# Making Information Available

Use Chapter 31 of *The Mathematics of Machine Intelligence* to answer the reader's question. Before reading a zero or a sudden jump, ask what the method could have found and whether a smoother score tells the same story.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Why does a whole answer jump when each piece improves steadily? (C31-D01):** If each token of a ten-token answer is right with the same chance, how does the chance of a whole right answer change as that chance rises?
- **How much can a zero among 655 electrodes rule out? (C31-D02):** None of 655 front electrodes matched the predicted burst. If each had the same small chance of a detected match, how likely is that?
- **What does a Bayes factor of 5 to 9 do to the odds? (C31-D03):** The electrodes' Bayes factors, 5.11 to 8.65, favored no orientation signal in the front. How much do they move a belief?
- **Did a shared workspace help, and what did the slot count do? (C31-D04):** In one software design, how did the number of workspace slots change a ball-separation score?
- **What happens to the leap if tokens are not independent? (C31-D05):** The formula p to the power L treats tokens as independent. What if tokens sometimes go together, all right or all wrong?

## Make the method fit the question

Answer from the chapter. A zero is evidence against high rates under a model, not proof. Keep the paper's claims apart from the book's arithmetic. Never say a theory was refuted or confirmed.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The Cogitate paper named no winner and the chapter reports it as mixed. A zero rules out only high detected-match rates under the stated model.
- The chance calculation, the Bayes factor reading and the correlated-token mixture are the companion's own, not the papers'.
- The workspace slot result is one design on one bouncing-ball task. No study here measures a slot count in a brain.
- Whether a system that makes information available also experiences it is a separate question, and no result here speaks to it.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> Use when a reader wants to see how a test's design and scoring rule limit what its result can show, on the brain side (a zero count) and the machine side (a jump in a score).

A successful answer produces useful work for this request rather than only summarizing the chapter.
