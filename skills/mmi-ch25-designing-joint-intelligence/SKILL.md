---
name: mmi-ch25-designing-joint-intelligence
description: "Use the review's standardized gaps, a routing rule that sends each case type to the partner better placed to answer it after the cost of asking, and the arithmetic of overrides to judge whether a person and a machine together beat the better one alone. Read the reported trials and rule-versus-professional counts at their stated limits, and say that no division of roles guarantees a gain: the whole arrangement has to be tested, with its costs, against each partner alone."
---

# Designing a Joint Intelligence

Use Chapter 25 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the person alone, the machine alone and the pair each score on comparable cases, what asking the person costs, and how many cases the two disagree on. Use the routing card to compare the partners case type by case type, and the override card to say whether the person wins more than half of the disagreements. Report the whole arrangement against each partner alone, and say which numbers were estimated under the conditions of use.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Did pairs beat their better member on average? (C25-D01):** Across 106 experiments, how did a person and an AI together compare with the better of the two alone, and with the person alone?
- **When should a case go to the person? (C25-D02):** A model is right 0.95 of the time on clear cases and 0.60 on hard ones. A counselor is right 0.90 and 0.70, and asking costs 0.05. Which cases should go to the counselor, and does the system beat the better solo score?
- **How often must a person win an override for it to pay? (C25-D03):** A counselor and a rule disagree on 150 of 1,000 students. The counselor is right on 60 of them. If the counselor overrides every disagreement, what happens to accuracy?
- **Did doctors with a chat model beat the chat model alone? (C25-D04):** Four trials gave doctors, or the public, a chat model and also scored the model alone. How big was the gain from the model, and how far did the people using it fall short of the model alone?
- **How often did a fixed rule match or beat the professional? (C25-D05):** In 136 studies that set a fixed rule against a trained professional, the rule did clearly better in 64, about equal in 64, and worse in 8. What does that say, and how does the headline change with how ties are counted?
- **Why did a copy of a psychologist do as well as the psychologist? (C25-D06):** Clinical psychologists rated 861 patients from their questionnaire scores. An equation tuned to each psychologist's own ratings did slightly better on the recorded diagnosis. What do the correlations say?

## Make the method fit the question

For a gap reported on the review's scale, use C25-D01 and say what the comparison group was. For a routing decision, use C25-D02 with the reader's own estimated success rates and asking cost; do not use the made-up numbers as real. For whether an override pays, use C25-D03. C25-D04 to C25-D06 quote reported results: state the scoring and what each study could not show.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- The review's standardized gaps are averages over the studies collected; no general rule favors combining, so a pair has to be tested task by task.
- The routing numbers (0.95, 0.90, 0.60, 0.70, the 0.05 asking cost, four clear cases in five) are made up for illustration. Neither hand-off paper tested a design with people.
- The 1,000-student override example is the chapter's constructed illustration, not data.
- The trials are scored differently and cannot be pooled. The doctor-versus-model comparisons were in some cases exploratory or untested directly, and the public trial's models received the whole scenario.
- A count of studies cannot say why a fixed rule won; steadier use of the cues and better weights both fit the facts.
- The probability reading of a gap g, and the r squared values, are this companion's arithmetic under stated assumptions, not statistics from the papers.
- Nothing here is clinical advice or evidence about any treatment.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My team lets a reviewer override a scoring rule. The two disagree on 150 of 1,000 cases and the reviewer wins 60 of them. Is the override helping, and what should we log?

A successful answer produces useful work for this request rather than only summarizing the chapter.
