---
name: mmi-ch08-knowing-things-relate
description: "Use the flipped grid to read a stored relation from the other end, the translation score f = |h + r - t| for relations as steps, and the reported numbers on the reversal curse to ask whether a system keeps, recovers or has built in the direction of a fact. Treat the word-pair memory study, the model results and the toy computations as separate kinds of evidence, and say that the mathematics of memory in people is a model."
---

# Knowing How Things Relate

Use Chapter 8 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask how each fact is stored: with head, relation and tail marked, or as a bare association. If the facts live in a graph, flip the grid and check whether the reversed relation is the one intended (has mother is not child of). If the facts live in a trained model, test both directions on held-out wordings, and compare reported scores only when the scoring rule is the same. Say which of the three the system relies on: direction kept by design, recovered by training on reversed text, or built into the geometry.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Do equal averages show that a word pair is stored both ways? (C08-D01):** If students recall about 57 percent of pairs from either end, what would the pair-by-pair record have to look like to count against two independent links?
- **How does flipping a grid read a fact from the other end? (C08-D02):** If a grid stores who is mother of whom, what does the flipped grid answer, and what does a two-way pair table lose?
- **What did the reversal-curse experiment actually score? (C08-D03):** A fine-tuned model scored 96.7 percent in one direction and 0.1 in the other. What was scored, on which facts, and what does that leave open?
- **What does adding reversed copies of the text buy? (C08-D04):** If the training text includes a reversed copy of every passage, how much of the reversed-question score returns, and for which kind of fact?
- **Why can a model learn A to B and still miss B to A? (C08-D05):** In a tiny lookup with separate input and output vectors, what happens to the reversed question as the forward fact is learned, and what does a reversed copy change?
- **How does a step on a line read a relation, and how does negating it read it backward? (C08-D06):** If next town east is a step of one stride, what gap does the fact score, what happens when head and tail swap, and what does negating the step do?
- **What does a hits-at-k score count? (C08-D07):** If a model ranks every town as a candidate tail, how often does the true tail land in the top k, and how fast does that fall as the learned positions blur?

## Make the method fit the question

For two facts and a question about who is whose mother, C08-D02 shows the flipped grid and the two-way table that cannot keep roles. For the word-pair study, C08-D01 shows why equal averages do not decide between symmetric and independent links. C08-D03 and C08-D04 quote the reported scores and must never be compared across the two scoring rules. C08-D05 is a constructed toy; do not describe it as a finding about language models. C08-D06 gives the translation gap f for a head, a step and a tail, and C08-D07 shows what a hits-at-k number counts on a constructed road.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The word-pair study used random nouns learned within the hour, not facts with roles; equal recall from both ends does not show how people reverse facts.
- A symmetric pair table returns a partner from either cue but cannot say which role each played.
- Flipping a grid reads the same relation from the other end. It does not give child of, which would also cover a father's children.
- The reversal-curse numbers are fine-tuning results on invented facts from 2023 and 2024 preprints and papers; they do not say how today's models behave, and exact-match and soft-match scores are not like for like.
- The toy lookup and the town road are constructed. Nothing here shows that language models or brains represent relations as steps.
- A relation that holds both ways, such as sibling of, breaks the single-step rule: an exact fit both ways forces the step to zero.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My system answers 'who wrote X?' correctly but fails on 'what did Y write?' for the same fact. What should I check?

A successful answer produces useful work for this request rather than only summarizing the chapter.
