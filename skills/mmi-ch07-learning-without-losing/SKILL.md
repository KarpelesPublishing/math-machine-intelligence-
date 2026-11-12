---
name: mmi-ch07-learning-without-losing
description: "Use the one-step interference identity for a linear learner, the chapter's three-item toy, the savings measure and a mixture of expectations to reason about how a mind or a machine can take in something new without losing what it knew. Say that the toys are constructed, that a shift in an old answer is not yet forgetting, and that the two-store account of memory is a proposal."
---

# Learning Without Losing Everything

Use Chapter 7 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask which old items share features with the new lesson, how large the step and the new error are, and whether the old answer actually became worse against its own target. Use the interference card for one step, the three-item card for the price and the point of overlap, the schedule card for focused against mixed training in a toy, the savings card to ask whether apparent loss is cheap to restore, and the mixture card for keeping competing expectations. Say that none of these is a measurement of a brain or of a deep network.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How far does one lesson on a new item shift an old answer? (C07-D01):** If a linear learner takes one update on a new item B, how far does its answer for an old item A move?
- **What does overlap cost an old item and give a neighbor? (C07-D02):** A learner knows only A. One update teaches a new item B. How far is A pushed off its answer, and how much did sharing with A already help a neighbor C?
- **What does mixing old examples in buy, and what does it cost? (C07-D03):** In a two-item toy, what happens to the old item A when the learner trains on the new item B alone, and what when old and new alternate?
- **How much of the first effort did relearning save? (C07-D04):** If learning took one amount of effort and relearning took another, what share of the first effort was saved?
- **Can a prediction change without erasing an old expectation? (C07-D05):** If a learner keeps two expectations, one from the old cause and one from a new cause, how does the combined prediction move when the weights change?

## Make the method fit the question

C07-D01 puts numbers on the one-step identity with a real two-weight update. C07-D02 is the chapter's A, B and C toy and leaves C's change open, as the chapter does. C07-D03 is the companion's own focused against interleaved toy and says what it does not reproduce. C07-D04 turns the savings ratio into efforts and marks which cases are the chapter's and which are the companion's scaling. C07-D05 is the chapter's constructed mixture of two expectations with the weights set by hand.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The one-step identity is for a linear learner and one gradient step on half the squared miss. It is the book's own toy, not in McClelland and colleagues, and it is not shown for deep networks or repeated updates.
- A shift in an old answer is not automatically forgetting: deciding whether the old answer got worse needs the old item's own target.
- The focused and interleaved card is a companion toy built from the same two-item setup. The chapter gives no numbers for the penguin network, and nothing here reproduces it.
- The two-store account of learning is a proposal, one patient does not settle it, and no card here tests it. The toys do not reproduce H.M.'s condition.
- Ebbinghaus used his own savings formula, not the plain ratio, so the efforts shown for his values are the companion's scaling and not his data. Savings alone does not show what a model's weights retain.
- The mixture card sets its weights by hand. The latent-cause model infers them, and it is a model of inference, not a measurement of a rat's thoughts.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A team trains an assistant further on one correction to a library's lending rules. How would I tell whether the correction damaged the answers for reference books, and what would mixing old examples in cost?

A successful answer produces useful work for this request rather than only summarizing the chapter.
