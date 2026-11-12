---
name: mmi-ch28-editing-learned-mind
description: "Executable demonstrations of Chapter 28: storing a pair as an outer product, the ghosts that overlapping keys leave, weakening and restoring, the one-outer-product insert and its damage, edits that pile up, the direction-removal dial and what a rise in a score can and cannot show."
---

# Editing a Learned Mind

Use Chapter 28 of *The Mathematics of Machine Intelligence* to answer the reader's question. Check an edit against the old pairs it was not meant to touch, and against a test it was not tuned on, before believing it taught anything.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Why does asking the table return more than one answer? (C28-D01):** If every pair is stored by adding a product, what comes back when one key is asked?
- **Can a connection weakened by one step be restored by another? (C28-D02):** What do a weakening step and a strengthening step do to a table, and what does the toy miss that the rats showed?
- **How much do old pairs feel one new fact? (C28-D03):** When one outer product writes a new pair exactly, how much do the old pairs change, and can a better choice of z shrink it?
- **What happens to a layer after many edits? (C28-D04):** If the insert is repeated 20 times, how far does the layer drift, and do the earlier inserts survive?
- **What does subtracting a direction do at different strengths? (C28-D05):** How does the dial c in the Astra-style edit change what a layer writes along a chosen direction?
- **Can overshoot calm one loop and break another? (C28-D06):** If a layer's output is fed back as input, what does the dial do to a part that grows each round?
- **How much of a 40-point gain is new skill? (C28-D07):** The edited small model rose from 7.9 to 48.1 percent on MATH-500. What do the other reported scores say about where that came from?

## Make the method fit the question

Answer from the chapter and its demonstrations. A toy table is not a language model and not a brain; say which numbers are constructed. Never say the edit taught math.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The table is a linear stand-in for a layer, with no language in it.
- The Astra result is an early blog post with logs, not a peer-reviewed paper; outside checks are also unreviewed.
- No study here wrote a specific fact or skill into a person. Brain results are small and narrow.
- No medical or clinical claim is made.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> Use when a reader wants to see how a key-value table is written to and what an edit does to the pairs already in it.

A successful answer produces useful work for this request rather than only summarizing the chapter.
