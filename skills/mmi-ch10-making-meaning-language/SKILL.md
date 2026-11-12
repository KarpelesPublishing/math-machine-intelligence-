---
name: mmi-ch10-making-meaning-language
description: "Use the SCAN rulebook and the chapter's reported scores to explain compositional generalization: decode a command from word meanings and rules, read why a random split can hide a failure, see how binding words to places keeps order, compare people and machines on the colored-circle task, see why shuffled practice episodes force a model to read the study examples, and see what a length split tests. Keep the mathematics as a model: the rulebook is a specification, the networks are dated 2018 and 2023 results, and no result says a brain and a network compose alike."
---

# Making Meaning with Language

Use Chapter 10 of *The Mathematics of Machine Intelligence* to answer the reader's question. Hold out a combination of known parts (a new pairing, a new arrangement, a longer input), score the answer against an independently specified correct output, and keep the held-out test separate from a random split. State which network and which split each score belongs to, and do not combine them. Passing one held-out combination does not establish competence on every arrangement.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does a short rulebook decode a command it never saw? (C10-D01):** A command joins 'jump twice' and 'walk left' with 'after'. What are the actions, in order, and why does the second part come first?
- **Why does a score of 99.8 percent not settle whether a network composes? (C10-D02):** A network scores 99.8 percent on a random split of the commands. What would you expect it to score on commands that compose a word it saw only alone?
- **How can a sum of word codes remember order? (C10-D03):** Two commands use the same two words in opposite order. Does a plain sum of word codes tell them apart, and what changes if each word is tied to its place first?
- **How close did machines come to people on the colored-circle task? (C10-D04):** People mostly gave the rule-based answer. A model was trained on a mixture set near 80 percent rule-based. Predict whether it scored below, near or above the people, and how GPT-4 did.
- **How much does a correlation from ten items settle? (C10-D05):** A model's score on each of ten instructions tracked how hard people found them, with a correlation of 0.788. If that came from ten items, what range of true correlations is still plausible?
- **Why does shuffling word meanings make a model read the examples? (C10-D06):** If 95 percent of practice episodes reassign what six words mean, how often is a word's usual meaning right, and what does a learner have to do instead?
- **What does a length split hold out? (C10-D07):** Train on commands that need up to 22 actions and test on the rest. How many commands is that on each side, and does the cut matter?

## Make the method fit the question

For decoding a command by the rulebook, use C10-D01. For the reported SCAN scores and what each held-out test means, use C10-D02, and never merge the bars into one score. For order in a sum of word codes, use C10-D03. For people versus machines on the colored-circle task, use C10-D04, and for how little ten items settle, C10-D05. For why shuffled meanings push a model to read the examples, use C10-D06. For the length split, use C10-D07. Say that no result shows that a brain and a network compose alike.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- SCAN is a small artificial language, not a model of natural language, and the rulebook describes the artificial language, not how a brain represents grammar.
- The scores are 2018 recurrent networks and 2023 transformers on specific held-out sets; each bar has its own best network, and there is no combined score.
- No people were tested on SCAN. The colored-circle study had 25 people online, with no brain measurement, and nothing shows that people and models err for the same reasons.
- The people-study model was trained on a mixture chosen to approximate human accuracy, so its closeness to people is by design.
- The shuffling demonstration is a constructed illustration with disclosed seed and an assumed uniform one-to-one reassignment (the paper's Methods use random permutations; uniform is the companion's reading); it is not the paper's training procedure.
- The rules for 'thrice', 'opposite' and 'around' are reconstructed by the companion and checked against the chapter's counts; the interval around 0.788 is the companion's own illustration.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A model answers every test sentence I give it smoothly. How do I tell whether it composes new combinations or has seen them?

A successful answer produces useful work for this request rather than only summarizing the chapter.
