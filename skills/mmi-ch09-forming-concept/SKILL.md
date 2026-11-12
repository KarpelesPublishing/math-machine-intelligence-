---
name: mmi-ch09-forming-concept
description: "Separate a membership rule from a typicality rating, compare keeping one average with keeping every case, see how feature weights change which stored case is nearest, add partial matches into a category's support, and score compact summaries against a chosen purpose with the information bottleneck toy. Treat the mathematics of a brain here as a model fitted to behavior."
---

# Forming a Concept

Use Chapter 9 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the kind is for before choosing a summary. Then choose the matching card: the odd-number ratings to separate a rule from a rating, the prototype and exemplar comparison for averages against stored cases, the weighted distance for feature importance, the category support card for several partial matches, and the bottleneck toy for choosing what a compact code keeps. Report which assumption would change the answer, and test a candidate summary on held-out cases near the boundary.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Why would students rate 3 as a better odd number than 447? (C09-D01):** The rule for odd numbers gives 3 and 447 the same answer. What did students rate instead, and did they think rating made sense?
- **Should a new case be judged by an average or by every stored case? (C09-D02):** Kind A has cases at 2, 3 and 4 and kind B at 1 and 7. Where do the two rules disagree about a new case?
- **How does a feature weight change which stored case is nearest? (C09-D03):** A new case differs from stored case P mostly in size and from stored case Q mostly in angle. Which is nearer as the weight on size changes?
- **Can a category win without any single decisive match? (C09-D04):** Category A has matches of 0.6 and a second one; category B has a single match. How does a category's share come out, and when does the total disagree with the best single match?
- **What should a compact summary keep: shape or color? (C09-D05):** An object has a shape bit and a color bit. Which of four summaries scores lowest when the target is shape, and what happens if the target or the trade-off weight changes?
- **Why is the middle level of a name called basic? (C09-D06):** Students listed attributes for names at three levels. Which step adds the most shared attributes?

## Make the method fit the question

To separate a rule from a rating, use C09-D01 and say that the rule gives 3 and 447 the same answer while students rated them differently; do not claim why. For averages against stored cases use C09-D02, whose cases are made up. For feature weights use C09-D03 and for several partial matches C09-D04; both use constructed numbers. For choosing what a compact summary keeps, use C09-D05 and always ask for the purpose first. C09-D06 quotes the chapter's reading of one study and does not show that a mind computes a trade-off. Never claim brain mechanisms.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The studies of people reported here measured ratings, lists and choices. None measured brain activity, and a graded rating does not show what a mind stores.
- Prototype and exemplar rules are two models; the odd-number studies compared no storage models and cannot tell which a mind uses.
- Feature weights in the semicircle model were estimated from choices and attention was never manipulated, so they describe a pattern without showing a cause.
- The bottleneck example is constructed: the object, the four summaries and the trade-off weight are chosen by hand and no data stand behind them.
- The attribute averages 3.5, 9.05 and 11.07 are the book's averages of the paper's raw tallies, not figures the paper prints.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My classifier groups items by their nearest average, but a stored case I trust sits closer to another group. Which rule am I using, and what purpose should decide what the summary keeps?

A successful answer produces useful work for this request rather than only summarizing the chapter.
