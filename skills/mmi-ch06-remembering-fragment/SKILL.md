---
name: mmi-ch06-remembering-fragment
description: "Use the Hopfield vote rule, storage rule and energy to explain how a partial or damaged cue can settle on a stored pattern and when it does not, estimate how many patterns a network can hold, turn match scores into shares with a sharpness setting, and see that one modern Hopfield step is an attention step. Keep the mathematics as a model: the mouse and rat studies do not show that a brain follows Hopfield's update rule."
---

# Remembering from a Fragment

Use Chapter 6 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what is stored, what the cue is, and how similar the stored items are. For a small network, work the vote, the storage sums and the energy by hand before running any simulation. For a retrieval question, compute shares from match scores at the setting actually used and say that a share is a weight, not a chance of being right. Check whether the intended item could be missing from the candidates, and whether two items share the details the cue contains.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does one unit decide by a vote? (C06-D01):** A unit hears three neighbors, two saying plus one and one saying minus one. What does it do, and what does it do when the votes cancel?
- **How do stored patterns become links? (C06-D02):** Two units agree in three stored patterns and disagree in one. How strong is the link between them, and what does one more pattern do?
- **How far from a stored pattern can the start be? (C06-D03):** If a pattern is damaged in a few units and the network updates, how often does it finish the pattern?
- **Why must units update one at a time? (C06-D04):** Does the network always come to rest, and what goes wrong if every unit updates at the same instant?
- **How many memories can a network hold? (C06-D05):** As more patterns are stored in the same units, when does recall from an exact stored pattern begin to fail?
- **What does the sharpness dial do to a best match? (C06-D06):** Two stored records match a fragment with scores 3 and 2. How much say does each get, and what does the dial change?
- **How is a memory step the same as an attention step? (C06-D07):** If shares come from match scores and the new state is their weighted average, does a sharper dial recall a damaged cue better than a plain vote?
- **How much of a preference survives when most cues are removed? (C06-D08):** In mice with impaired CA3 plasticity, search in the target quadrant fell from 66.4 to 44.6 percent when three of four cues were removed. What does that say, compared with chance?

## Make the method fit the question

For a vote question, C06-D01 gives the total vote and the tie rule; for stored patterns, C06-D02 builds the link by the storage rule and shows each pattern's contribution. For how often a damaged cue is completed, C06-D03 reports seeded runs, and C06-D04 shows why one-at-a-time updating guarantees a stable end while simultaneous updating can cycle. C06-D05 gives recall against load and the crosstalk estimate. For candidate scores and a sharpness setting, use C06-D06 and C06-D07, and never present a share as a probability of correctness. C06-D08 reads the reported mouse percentages against the 25 percent chance level.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A settled state is not necessarily the intended memory, and the basic model has no built-in warning that it settled wrongly.
- The energy guarantee needs symmetric links, no self-links and one-unit-at-a-time updates; simultaneous updates can cycle forever.
- The 0.15 N capacity rule of thumb is for random patterns in the classical network, and the modern network's capacity grows much faster with size.
- A softmax share is a weight, not a probability that a record is correct; raising the sharpness setting adds no evidence.
- The mouse and rat results are consistent with pattern completion in general; neither shows that a brain region follows Hopfield's update rule, and no model was fitted to the mice.
- The simulations here use random or constructed patterns with disclosed seeds, not text or real memories.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My lookup tool scored two candidate records 3 and 2 and then reported the first at 99 percent after I raised a setting. Did the evidence change?

A successful answer produces useful work for this request rather than only summarizing the chapter.
