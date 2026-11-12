---
name: mmi-ch16-discovering-causes
description: "Use the chapter's tally of explanations, the difference between seeing and setting, the back-door adjustment, Cornfield's bound, a test of when a stand-in score is safe to push, and a seeded experimenting-agent simulation to say what a record can and cannot tell a mind about what a change would do. Keep the mathematics as a model: the children, the machines and the agents are examples, and none of the studies measures these computations in a brain."
---

# Discovering What Causes What

Use Chapter 16 of *The Mathematics of Machine Intelligence* to answer the reader's question. Before using a record to say what a change would do, ask what else could have set both the cause and the effect, whether the cause was assigned by chance or by something that also touches the outcome, and which variable you would actually set. Work the weighted average by hand when a grouping variable is recorded, and treat a stand-in score as a bet that needs the allowed behaviors named.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Which explanations survive three watched events? (C16-D01):** Block B alone does nothing, block A alone lights the machine, and A with B keeps it lit. Which of four possible explanations are left, and which block should a child take off?
- **Why can identical logs hide different effects of setting a switch? (C16-D02):** Two machines keep the same log of a switch and a light. If you set the switch by hand, does the light follow in both?
- **How much of a risk ratio is the gene? (C16-D03):** Smokers look five times as likely to get cancer when everyone is lumped, but a gene feeds both smoking and cancer. What does adjusting by the gene give?
- **How common must a hidden trait be to explain away a risk ratio? (C16-D04):** Suppose smoking did nothing and one yes-or-no trait caused the whole association. How common would it have to be among smokers?
- **When is it safe to push a stand-in score? (C16-D05):** A boat-racing game scores target hits, but the goal is to finish. Which sets of allowed behaviors let pushing the score hurt the goal?
- **How much does being allowed to set variables help an agent? (C16-D06):** An agent has five steps to explore a five-variable world, then is told which variable to push as high as possible. Does setting variables beat only watching?

## Make the method fit the question

For the children's three events use C16-D01. For why identical logs can hide different effects of setting a variable, use C16-D02. For adjusting by a recorded group, use C16-D03, and for a hidden trait nobody recorded, C16-D04. For the proxy and the lagoon, use C16-D05 and never claim the toy proves a result about a real system. C16-D06 compares an agent that sets variables with one that only watches in a constructed world, and must not be quoted as the paper's result.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A record can estimate what setting a variable would do only when its causal assumptions hold; the formula is only as good as the diagram.
- The four-explanation tally is a toy with independent triggers; it describes a machine and does not show how the children reasoned.
- The hidden-coin machines, the gene example and the quiz of behaviors are constructed, not data.
- Cornfield's bound covers one yes-or-no trait, and his group argued from many lines of evidence.
- The safe-or-hackable check applies the definition to a made-up set of behaviors; it is not the finite-policy theorem, and it says nothing about any deployed system.
- The experimenting-agent simulation uses random linear diagrams and simple rule-based explorers, not the paper's trained networks, and it is not a measurement of any agent.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> Two logs of a switch and a light look identical. Does that mean setting the switch will do the same in both?

A successful answer produces useful work for this request rather than only summarizing the chapter.
