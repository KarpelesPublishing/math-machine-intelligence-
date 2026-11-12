---
name: mmi-ch12-imagining-new
description: "Use the chapter's arithmetic for imagination: how a one-in-ten-thousand chance still occurs, the straight-line time of mental rotation, a world model run forward, a scorer that overstates the option it picks, sums on points in a learned space, the reported writers' study and a model of a narrower shared source. Say that novelty, usefulness and originality are three separate tests, that a machine that generates candidates is not shown to imagine as a brain does, and that a fit of outputs does not show matching inner experience."
---

# Imagining Something New

Use Chapter 12 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the candidates were generated from, what scores them, and what independent check exists in the setting where the idea will be used. Report novelty, usefulness and originality separately, say which was tested, and name the one that was not. Treat a model of the world as a source of candidates, not as the world, and expect its errors to grow with each step imagined.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **Is a one-in-ten-thousand move a move no human would play? (C12-D01):** If a move has a one in 10,000 chance each time a human faces the position, what is the chance that someone plays it across many tries?
- **How long does it take to turn a shape in the mind? (C12-D02):** If reaction time rises in a straight line from 1 second at no turn to 4 to 6 seconds at a half turn, what turning speed does the line imply?
- **How far can an imagined run be trusted? (C12-D03):** A model rolls an imagined ball forward step by step. If its rule is slightly wrong, how large is the error after many steps?
- **Why does the option a scorer picks look better than it is? (C12-D04):** A scorer ranks imagined options, and the highest score is chosen. How much does the chosen option's score overstate its worth?
- **How do sums on points make a smiling man? (C12-D05):** If smiling woman minus neutral woman plus neutral man gives a smiling man, why does the chapter say that averaging three faces per idea mattered?
- **What did machine ideas do for the writers? (C12-D06):** How much higher did readers rate stories written with machine ideas, and for which writers was the gain largest?
- **When does a shared source narrow what people write? (C12-D07):** If some writers build on ideas from one source, when does the whole pool of stories get narrower?

## Make the method fit the question

For a rare event, use C12-D01 with the stated chance and the number of tries, and say whether the tries are independent. For a time against angle, use C12-D02 and treat the rate as a summary of behavior. C12-D03 shows how a model's error compounds across imagined steps. C12-D04 shows why the option a scorer picks is claimed better than it is, and why the real setting is the check. C12-D05 is a constructed picture of sums on points. C12-D06 quotes the writers' study and C12-D07 is a model that shows when a shared source narrows a pool; say which is which.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A one-in-ten-thousand figure is AlphaGo's own estimate of how likely a human was to play one move in one position. It is not a count, and no source says no human had ever played such a move.
- Novelty, usefulness and originality are three claims. Move 37 has a number for the first, the game result for the second, and no test of the third.
- Mental rotation reaction times are behavior in eight adults, with reports of their own thinking that the authors treat with caution. They carry no brain data.
- The rollout, scorer, latent-sum and pool illustrations use constructed or disclosed made-up numbers. They are not measurements of any game, network or writer.
- The writers' percentages are the chapter's reported results from one online study. A similarity measure from a program is not a reading of how stories sound.
- One patient, MX, shows that passing imagery tests does not show that an image was experienced. A match in outputs cannot, by itself, show a match in inner experience.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> A system proposes 30 options and a scoring rule ranks them. The top-ranked one looks very strong on the score. How much of that strength should I expect to survive in the real setting?

A successful answer produces useful work for this request rather than only summarizing the chapter.
