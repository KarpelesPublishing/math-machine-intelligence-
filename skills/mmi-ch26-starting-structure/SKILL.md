---
name: mmi-ch26-starting-structure
description: "Use the chance of finding one good setting among about a million, the 1987 learning-guides-evolution simulation, the exact split of a change into choosing and copying, and the replicator step to say what a search can do and what it needs people to supply: candidates, a verdict on them, and a test that fits the goal. Read the machine-merge result at its stated limits, and keep the brain side a possibility: the simulation did not measure any process in brains."
---

# Where the Starting Structure Comes From

Use Chapter 26 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask who supplied the candidates, who said which was good, and whether the test that picked the winner is separate from the test that reports it. Use the odds card for how hard a single good setting is to find, the choosing-and-copying split to see whether a change came from reweighting what was there or from new variation, and the replicator card to check whether the best kind was in the pool at all. Report the score with the size of the test and the choices people made.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How hard is it to stumble on the one good wiring? (C26-D01):** A creature's 20 connections are each present or absent, and only one pattern is good. If its fixed genes are all right and some switches are left open, how likely is it to find the good wiring by random tries in a lifetime?
- **What happens to the genes when only the choosing of parents changes? (C26-D02):** 1,000 creatures each carry 20 genes of 1, 0 or ?. They learn by random tries, and the quick learners leave more children. What do the gene shares do over 50 generations, though nothing learned is written into a gene?
- **How often does the right wiring end up fully built in? (C26-D03):** Run the 1987 simulation until the correct wiring fixes in every creature, or until a wrong or open setting fixes and the right wiring becomes impossible. How often does it fix, and does the number of tries matter?
- **How much of a change in the average came from choosing, and how much from copying? (C26-D04):** Four seeds have hook lengths 0, 1, 2 and 3 mm and leave 1, 1, 2 and 2 seedlings. D's seedlings come out 0.3 mm shorter than D. How much does the average hook change, and from which source?
- **Why does a seed the field does not hold never appear by choosing? (C26-D05):** A field has round, wrinkled and speckled seeds leaving 1, 2 and 4 offspring each, and no striped seeds, which would leave 10. What does one round of choosing do, and what would bring striped seeds in?
- **How much should a 52 percent score on 250 problems be trusted? (C26-D06):** A search merged three models into one that scored 52.0 percent on 250 held-out Japanese math problems, against 9.6, 18.4 and 30.0 for the sources. What do the scores say, and what could a 250-problem test tell apart?

## Make the method fit the question

For the odds of a single good setting, use C26-D01 with the number of open switches; say its assumptions. C26-D02 and C26-D03 are seeded reimplementations, so report their results as the companion's runs and give the reported 0.167 as a reference, not a target. C26-D04 splits a change exactly into choosing and copying, and C26-D05 shows why a kind that starts at zero stays at zero under choosing alone. C26-D06 quotes the merge scores and adds sampling bars for the 250-problem test.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The creatures in the 1987 simulation exist only as numbers. The authors call their case extreme and unrealistic; the simulation did not measure any process in brains.
- The chance of finding the good wiring assumes the creature's fixed genes are all right. It is the book's arithmetic, not a result in the paper.
- The seeded reimplementation here is the companion's own, built from the chapter's description. It is not the authors' code and does not reproduce their figures exactly.
- Choosing can only reweight what the pool already holds; the replicator step cannot create a missing kind. The copy-error step is the companion's addition.
- The merge result is one test, in one language, with 250 problems. People chose the three source models, the method and the test, and a score on the test cannot say whether the test captured the wider goal.
- The 95 percent bars on the merge scores assume the test problems are a random sample, which they are not; they show only how finely 250 problems can tell.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A search over 1,000 recipes picked one that scored 52 percent on a 250-problem test, and the best starting model scored 30. Is that a trustworthy gain, and what did people supply?

A successful answer produces useful work for this request rather than only summarizing the chapter.
