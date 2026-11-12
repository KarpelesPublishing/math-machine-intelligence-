---
name: mmi-ch22-another-mind
description: "Use Bayes' rule to score goals by how well observed steps fit them, the softmax choice rule to turn option values into chances, and a pass-rate comparison to see how much a test result separates rival explanations. Treat a model of another mind as a fit to behavior, check what the agent could have known before reading a choice as a preference, and say that the invented fleet and constructed examples are illustrations, not data."
---

# Understanding Another Mind

Use Chapter 22 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the observed agent could see or know, what options it had, and what a choice rule with some noise would predict. Then score the candidate goals with Bayes' rule, using the chance of each step under each goal. Before reading a choice as a preference, compare the readings that fit with and without missing knowledge. When a test result is offered as proof of understanding, compare how likely a pass is under each rival explanation, and say that a good fit to behavior does not establish a private motive or belief.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How do steps point to a goal? (C22-D01):** If one step is four times as likely under goal A as under goal B, where does belief in A land, and how fast does it grow as more such steps are seen?
- **Is a skipped road a dislike or never known? (C22-D02):** If two roads cost the same but one draws far fewer trips, does that show drivers dislike tolls?
- **How unlikely is 21 right out of 24 by guessing? (C22-D03):** Sarah picked the problem-solving photograph on 21 of 24 trials. How often would a guesser do that, and what does that rule out?
- **How much does one pass tell you? (C22-D04):** A tracker passes a standard false-belief story 95 times in 100 and a pattern-matcher 90. How far does one pass move belief that the test-taker tracks beliefs?
- **What do the printed correlations say? (C22-D05):** A model correlates 0.97 with people's ratings in one study and 0.78 in another. How different are those, and what do they not show?
- **How many pairs does a ranking give, and how noisy is a choice? (C22-D06):** A rater ranks several outputs. How many pairs of preferences does that produce, and what reward gap would make two raters agree about as often as the labelers in the study did?

## Make the method fit the question

For reading a goal from steps, use C22-D01 with the step chances the user can justify, and say the prior and action model are assumptions. For a choice that might reflect ignorance, use C22-D02: compute the shares with and without the unknown option before inferring a preference, and note the fleet is invented. C22-D03 gives the exact chance of a count of right answers under a flat chance and says what it does not decide. C22-D04 shows how little a pass moves belief when a rival also passes. C22-D05 reads the chapter's printed correlations with their stated bases. C22-D06 counts pairs from a ranking and shows a noisy two-option choice rule; the agreement arithmetic is the companion's own.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A goal score depends on the assumed prior and on the model of how a goal produces a step; a different action model gives a different answer.
- The toll fleet, its drivers, costs and the 40 percent figure are invented illustrations, not data.
- A softmax weight is a chance of choosing under the model, not a measure of what someone knew or wanted; ignorance and dislike can produce the same choice share.
- Sarah's 21 of 24 rejects a flat chance of 0.5, but it cannot choose among physical matching, associationism, empathy and theory of mind; the paper says so itself.
- A good fit of a model to people's ratings is a statement about behavior, not proof that people or machines run that calculation.
- The reward gap and two-rater agreement in the ranking demonstration are the companion's own illustration under assumed identical raters; the study did not report them.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A driver keeps taking the slow road. How do I tell whether they dislike the toll or never knew about the fast road, and what would I need to ask first?

A successful answer produces useful work for this request rather than only summarizing the chapter.
