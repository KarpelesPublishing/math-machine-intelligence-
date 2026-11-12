---
name: mmi-ch32-question-experience
description: "Use the chapter's formulas and reported counts to read a complexity score, an entropy, the false-negative share of a test and the cost of computing a theory's score, and to see why matching outputs do not reveal the inside of a system. Treat every score as a model of a test, never as a measurement of experience, and keep the four links of the chapter's checklist (pattern, bridge, transfer, rivals) in view."
---

# The Question of Experience

Use Chapter 32 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the signal is, what ties it to reports of experience in known cases, whether the tie transfers to the new case, and which rival explanations were tested. For a negative result, ask for the test's sensitivity before reading the silence. For a score, ask how its cutoff was chosen. For a machine, say that no test of experience has been validated against reports for any machine.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does a count of new patterns become a score? (C32-D01):** A response is a grid of 32 on-or-off entries. How do the count of new patterns and the mix of ones and zeros set its score?
- **Why divide by what a random string would need? (C32-D02):** How do real counts of new patterns behave for random strings of different lengths, and for a string that just repeats?
- **What do the reported counts say, and how much doubt do they carry? (C32-D03):** How large are the shares behind the chapter's three reported studies, and how different are their sample sizes?
- **How fast does a theory's score become impossible to compute? (C32-D04):** Rings of simple gates took about 1 second, 16 seconds and 2.75 hours as they grew from 3 to 5 to 7 gates. What does that say about a system as large as a brain?
- **Can two machines give the same answers and be wired differently? (C32-D05):** A recurrent adder keeps a running total. An unrolled chain does the same with one unit per input. Do their outputs ever differ?
- **How much does a negative leave open? (C32-D06):** A test flags some share of cases and catches some share of those with the property. What share of its negatives still has the property?
- **What does 48 of 48 correct leave open? (C32-D07):** A decoding method read 48 of 48 answers from healthy volunteers correctly, and 5 of 5 decodable answers from one patient. Does a perfect record mean a perfect method?

## Make the method fit the question

For a response complexity score, use C32-D01 with the counts the reader actually has; do not invent counts. C32-D02 shows that scores from random strings depend on length and that repetitive strings score lower. C32-D03 holds the counts the chapter reports and puts a sampling interval on each, labeled as the companion's own. C32-D04 reports how long the theory's score took for three ring sizes. C32-D05 shows two differently wired systems with identical outputs. For a negative test result use C32-D06 and require a sensitivity. C32-D07 shows what a perfect record such as 48 of 48 does and does not establish. Never say a score shows what an experience is like.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A score, a scan or a pattern of activity is evidence about a signal. None of the demonstrations here measures experience, in a patient or a machine.
- The complexity score formula is run here on constructed strings and counts. The chapter's example counts are hypothetical, and the grid entries are not individual neurons.
- The false-negative formula assumes the test never flags a case that lacks the property, and it needs a sensitivity the studies do not report for patients with no bedside response.
- Intervals shown on the reported counts are the companion's own and cover sampling noise only. The samples were not random samples.
- The adder example is a constructed toy of the unfolding argument, not a result in the cited paper. Critics replied that brain measures can still test such theories.
- Nothing here is clinical guidance or a statement about any person.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A detector flags 10 of 100 cases and I think it catches about half the cases that have the property. How many cases did it miss, and what share of its negatives is that?

A successful answer produces useful work for this request rather than only summarizing the chapter.
