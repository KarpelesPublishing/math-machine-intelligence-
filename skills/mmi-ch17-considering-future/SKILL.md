---
name: mmi-ch17-considering-future
description: "Use the chapter's value equation, A star score, successor visit table, value-of-a-look arithmetic and a search blind-spot calculation to explain how a machine can weigh a future inside a model before it acts, what changes when only the reward changes, and what a search cannot weigh. Keep the brain side as evidence about rats and a model, not a mechanism: the maze and place-cell studies do not show that a hippocampus runs these computations."
---

# Considering a Future

Use Chapter 17 of *The Mathematics of Machine Intelligence* to answer the reader's question. Ask what the model holds, what the score ranks, and what each look costs. Work a value or a route score by hand on a small map before trusting a search, check whether a first look can look worthless while two looks pay, and ask a planner to list the constraints it assumed so that missing ones show. A search can only weigh the futures its model contains.

## Select the useful mathematics

Read [the chapter guidance](references/chapter.md) for the selected example and [equation cards](references/equations.json) for exact formulas, assumptions, domains, and book anchors. Load only the material needed for the request.

- **How does the value of a place come from what happens next? (C17-D01):** A place pays 1 now and leads to a place worth 5 later. What is it worth when later rewards count for less?
- **Which towns does A star explore, and when does it reach D through C? (C17-D02):** Which towns does a search explore on a four-town map, and what route does it return?
- **What goes wrong if a search will not reopen a place? (C17-D03):** A place is closed at one cost and a cheaper way to it turns up later. Does the search still return a cheapest route?
- **Can a table of expected visits be re-scored when only the goal moves? (C17-D04):** A walker steps right through three rooms and stops in room 3. If the reward moves from room 3 to room 2, what changes in the table and what changes in the values?
- **Why can a first look be worth nothing while two looks pay? (C17-D05):** A player can pass for a sure 0.75 or answer a coin-flip question. Hints are right 7 times in 10. What is each look worth?
- **How many looks does it take to find a move a toy search rates as rare? (C17-D06):** In a toy search that tries moves in proportion to a starting weight, how many looks does a move with weight one in ten thousand need before it is ever tried?

## Make the method fit the question

For the value of a place under a fixed rule use C17-D01. For routes and what a guess does, use C17-D02, and for why reopening matters use C17-D03. For what happens when only the goal changes, use C17-D04, and never call the visit table a map. For pricing looks use C17-D05, where the first look can be worth nothing and two looks worth 0.055. C17-D06 is a toy about unexamined moves; it must not be presented as how AlphaGo works or why it erred.


## Use it with the reader

1. Identify whether the request needs an explanation, calculation, comparison, or evidence check. Infer the reader's level from the request; ask only for missing information that affects the result.
2. For numeric inputs, identify units, meanings, ranges, and relevant assumptions. If a requested calculation lacks inputs, ask for the necessary values or offer a clearly labeled illustrative example. Never invent measurements. Qualitative questions do not require invented numeric inputs.
3. Choose the relevant equation card. For a calculation, state the formula in readable notation and explain its symbols. For a conceptual question, explain the relevant relationship or assumption without requiring algebra. Match the depth to the request.
4. Open [the illustrated chapter](assets/reader.html) at the chosen demonstration's fragment when it helps. Inspect the demonstration's named controls, available values, and fixed quantities before suggesting a selection or change. Use only available control values in the saved reader. If its toy inputs differ from the request, disclose the differences and supply the requested example separately as a calculation or table, or as an illustration genuinely generated with available tools. The saved reader is self-contained. If a visual cannot be opened, use the card's disclosed worked example when helpful; do not claim a notebook was executed.
5. Return the explanation, calculation, comparison, or evidence check that answers this question, together with its source chapter/section and relevant limits. Do not add a calculation solely to satisfy a response format.
6. For learning requests, offer one prediction or transfer question. For a direct calculation, answer without imposing a quiz.

## Boundaries that matter

- A value equation evaluates one fixed rule for choosing actions; finding the best rule needs a comparison of actions as well.
- A star is engineering proved on paper and is not a model of how people search; its guarantee needs a guess that never exceeds the true cost left, and a search that may reopen places.
- The visit table assumes one fixed rule, and re-scoring that rule is not finding a new best route.
- The quiz and the three-room corridor are constructed illustrations, not findings.
- The blind-spot calculation draws moves in proportion to their starting weight and is not AlphaGo's algorithm; the accounts cited do not establish why AlphaGo erred at move 79.
- Four rats in one arena are a correlation; the studies do not show that a hippocampus does anything like planning from a stored model.
- For a brain, the mathematics is a model: a close fit to behavior is not proof of how neurons do it, and nothing here settles whether any system has experience. Say which of the three questions a result answers: does the model match behavior, does evidence support its mechanism, does evidence establish experience.
- Separate what the book computes (an equation specifying what a machine does), what it models (a description that generates predictions), and what a study measured. Never present a simulation in this companion as a measurement.
- Give no clinical, diagnostic or treatment advice. A study the chapter discusses is evidence about its own participants and conditions only.
- Check a theorem's assumptions before applying it. A finite illustration is not a proof of a general result.
- Disclose illustrative parameters and seeds, and distinguish them from book values and reader inputs.
- Claims about a particular product, current model performance, or facts outside the book need separate evidence. Cite only what the chapter itself cites.

## Practical starting point

> My planner scored a route as best, but a move nobody listed won the game. Was the search wrong, or was the model missing something?

A successful answer produces useful work for this request rather than only summarizing the chapter.
