# Chapter 9: Forming a Concept

A rule says whether a thing belongs; a summary says how well it fits, and what it keeps depends on the purpose.

Ask what the kind is for before choosing a summary. Then choose the matching card: the odd-number ratings to separate a rule from a rating, the prototype and exemplar comparison for averages against stored cases, the weighted distance for feature importance, the category support card for several partial matches, and the bottleneck toy for choosing what a compact code keeps. Report which assumption would change the answer, and test a candidate summary on held-out cases near the boundary.

Practical question: My classifier groups items by their nearest average, but a stored case I trust sits closer to another group. Which rule am I using, and what purpose should decide what the summary keeps?

## C09-D01: Why would students rate 3 as a better odd number than 447?

The rule for odd numbers gives 3 and 447 the same answer. What did students rate instead, and did they think rating made sense?

Both 3 and 447 leave a remainder of 1 when divided by two, so the rule cannot tell them apart. The students still rated 3 as a better example, at 1.6 against 3.7, a gap of 2.1 points. The second group is the surprising part: every one of the 21 said rating odd numbers by degree makes no sense, and still rated 3 at 1.0 and 447 at 1.9.

$$
n \bmod 2 = 1 \ \text{for every odd } n
$$

**Symbols:** n mod 2: the remainder when the whole number n is divided by two; every odd number leaves 1; rating: mean of students' ratings from 1 (a very good example) to 7 (a very poor one)

**Predict:** The rule gives every odd number the same answer. Before opening the second group, predict whether students who said rating makes no sense still graded 3 and 447 differently.

**Worked example:**
- Rule: remainder of 3 and of 447 on dividing by 2: 1 and 1
- Rating of 3, and of 447 (1 is best): 1.6 and 3.7
- Gap in mean rating, 447 minus 3: 2.1
- Said no to rating for odd number: 100 percent

The rule gives 3 and 447 the same answer, remainder 1. Yet experiment 1's students rated 3 at 1.6 and 447 at 3.7, a gap of 2.1 points on a 7-point scale. For odd number, 100 percent of a separate group of 21 students said grading makes no sense.

**Calculation:** 3 = 2 x 1 + 1 and 447 = 2 x 223 + 1, so both are odd. Mean ratings: 1.6 for 3 and 3.7 for 447, so 447 minus 3 = 2.1 rating points. Percent saying no for odd number: 100.

**Takeaway:** A membership rule asks whether something qualifies; a typicality rating asks how representative it seems. They can give different answers for the same item.

**What happens:** At Group of students = experiment 3, Kind shown on the right = odd number: All 21 students said it makes no sense to rate odd numbers, yet their means still ran from 1.0 for 3 to 1.9 for 447. Saying rating made no sense did not stop the grading. The authors suspected some students read 'odd' as peculiar, so this does not show why 3 came out ahead.

**Why it matters:** A system that applies an exact test and a system that ranks by typicality answer different questions. Treating a good rating as proof of membership, or a flat rule as proof that no ranking exists, mixes them up.

**In brains and behavior:** Students graded an exact kind. The authors suggested a core rule alongside a separate rough identification process; the study did not test why 3 came out ahead, and every result is behavior, not brain activity.

**In machines:** An exact test such as the remainder gives 3 and 447 the same answer. Any graded score a machine reports for them must come from some other computation, such as a summary of cases.

**Assumptions and limits:** The ratings are means of students' judgments of how well a number fits their idea or image of odd. The study measured behavior; it did not test why 3 came out ahead or what a mind stores, and it compared no storage models. The authors suspected some students read 'odd' as peculiar, so the grading may partly reflect that reading.

**Check:** In the chapter's first experiment, how large is the gap in mean rating between 447 and 3, and which of the six odd numbers was rated best after 3?

**Answer:** 447 minus 3 is 3.7 minus 1.6 = 2.1 rating points. After 3 (1.6) the best-rated was 7 at 1.9.

**Source:** Chapter 9: Forming a Concept; anchor `chapter-9-forming-a-concept`. Reported results quoted from the chapter's account of Armstrong, Gleitman and Gleitman (1983): the 31 students' mean ratings of six odd numbers, the 21 students' percentages saying rating by degree makes no sense, and the two Table 6 means for odd number (3 at 1.0, 447 at 1.9). Only those two Table 6 means are given in the chapter.

## C09-D02: Should a new case be judged by an average or by every stored case?

Kind A has cases at 2, 3 and 4 and kind B at 1 and 7. Where do the two rules disagree about a new case?

The prototype rule keeps only one number per kind. The exemplar rule keeps every case and lets a nearby stored case count a lot. A new case at 0 sits close to B's single case at 1, so the exemplar rule favors B even though A's average is nearer. Moving the new case along the line shows two stretches where the rules answer differently.

$$
\text{prototype: nearest average},\qquad \text{exemplar: } S_K(x)=\sum_{c\in K}\left(\tfrac13\right)^{|x-c|}
$$

**Symbols:** x: the position of the new case on the line; c: a stored case of kind K; S_K(x): the exemplar support for kind K: each stored case counts a third as much for each step of distance

**Predict:** A new case at 0 is far from both averages (3 and 4). Predict which kind each rule picks.

**Worked example:**
- Prototype rule answers: A (distances 3 and 4)
- Exemplar rule answers: B (supports 0.16 and 0.334)
- Do the rules agree?: they disagree

A new case at 0 goes to A by the average and to B by total closeness to stored cases, so they disagree. The same cases can get two labels, so graded ratings alone cannot say which rule a mind uses.

**Calculation:** Averages: A = (2 + 3 + 4)/3 = 3, B = (1 + 7)/2 = 4. Distances from 0: 3 and 4. Support = sum of (1/3)^distance over stored cases: A 0.16, B 0.334.

**Takeaway:** The same stored cases can give two different labels, so graded ratings alone cannot say which rule a mind uses.

**What happens:** At Position of the new case = 0: At 0 the average of A (3) is nearer than the average of B (4), so the prototype rule says A. The exemplar rule says B: its case at 1 is one step away and counts about 0.33, against about 0.16 in total from A's three cases.

**Why it matters:** Few-shot machine classifiers that label a new input by its nearest class average use the first rule; a system that compares with every stored case uses the second. Knowing which one is in use predicts where it will disagree with the other.

**In brains and behavior:** Whether a mind keeps one average or each case is open. Graded ratings fit a prototype account but do not prove one, and the odd-number studies compared no storage models.

**In machines:** In prototypical networks (Snell and colleagues, 2017) a class's prototype is the average of its embedded cases and a new input goes to the nearest one. The word is borrowed from psychology and the authors do not claim to model human concepts.

**Assumptions and limits:** One line, two kinds with fixed cases. The prototype rule uses the plain average; the exemplar rule adds closeness over every stored case with a fixed one-third decay. Real studies of people compared no storage models.

**Check:** For a new case at 5, which kind does the prototype rule pick, and which does the exemplar rule pick?

**Answer:** Distances to the averages are 2 (A at 3) and 1 (B at 4), so the prototype rule says B. The exemplar support is (1/3)^3 + (1/3)^2 + (1/3)^1 = 0.481 for A and (1/3)^4 + (1/3)^2 = 0.123 for B, so the exemplar rule says A.

**Source:** Would a rating make sense for odd numbers? Twenty-one students said no; anchor `would-a-rating-make-sense-for-odd-numbers-twenty-one-students-said-no`. The chapter's constructed example (not data): cases at 2, 3, 4 and 1, 7, a new case at 0, and a stored case counting a third as much for each step. The sweep over other positions is the companion's own use of the same two rules.

## C09-D03: How does a feature weight change which stored case is nearest?

A new case differs from stored case P mostly in size and from stored case Q mostly in angle. Which is nearer as the weight on size changes?

Each feature's gap is squared, scaled by its weight and added. P differs only in size, so its distance is 4 times the size weight. Q differs a little in size and a lot in angle, so its distance shrinks as the angle weight falls. At small size weights P is nearer; once size dominates, Q is.

$$
d_w^2(x,z)=\sum_k w_k\,(x_k-z_k)^2,\quad \sum_k w_k=1,\quad w_k\ge 0
$$

**Symbols:** d_w^2(x,z): the weighted squared distance between cases x and z; k: a feature; here size and angle; w_k: the weight on feature k, nonnegative, all weights add to one; x_k, z_k: the two cases' values on feature k

**Predict:** P is 2 steps off in size only. Q is 1 step off in size and 2 in angle. Predict the weight on size at which they are equally near.

**Worked example:**
- Squared distance to P: 2
- Squared distance to Q: 2.5
- Nearer stored case: P
- Size gap counts this many times an equal angle gap: 1

With weights 0.5 on size and 0.5 on angle, the squared distances are 2 to P and 2.5 to Q, so P is nearer. Changing what counts can change which stored case is nearest.

**Calculation:** Gaps: P differs by 2 in size and 0 in angle, Q by 1 and 2. d^2(P) = 0.5 x 4 + 0.5 x 0 = 2. d^2(Q) = 0.5 x 1 + 0.5 x 4 = 2.5.

**Takeaway:** What counts as alike depends on how much each feature is weighted, so the nearest stored case can change when the weights change.

**What happens:** At Weight on size = 0.8: At weights 0.8 and 0.2 a size gap counts four times an equal angle gap, as in the chapter. P then scores 3.2 and Q only 1.6, so Q is nearer. The swap is at a size weight of 4/7, about 0.571, not at one half: P is nearer for every size weight below that and Q for every weight above it.

**Why it matters:** A distance with fixed weights bakes in a view of which features matter. Changing the purpose can change the weights and with them the answer.

**In brains and behavior:** In the semicircle study the fitted weights followed the task: where size alone decided the kind, the weight on angle fell to nearly zero. That is a model fitted to choices of two paid observers.

**In machines:** A task weight over features is fixed for a task. Transformer attention, by contrast, is worked out afresh for each input, so the machine parallel is only partial.

**Assumptions and limits:** Two features, weights adding to one. The cases are made up. The weights in Nosofsky's study were estimated from choices; attention was never manipulated, so they describe a pattern without showing a cause.

**Check:** With a size weight of 0.5, what are the squared distances to P and to Q?

**Answer:** d^2(P) = 0.5 x 4 + 0.5 x 0 = 2. d^2(Q) = 0.5 x 1 + 0.5 x 4 = 2.5. P is nearer.

**Source:** Sixteen semicircles, and weights that followed the task; anchor `sixteen-semicircles-and-weights-that-followed-the-task`. The chapter's weighted-distance equation. The positions (new case at 2, 2; P at 4, 2; Q at 3, 4 on a four-by-four grid like the 16 semicircles) are constructed by the companion; they are not Nosofsky's stimuli or data.

## C09-D04: Can a category win without any single decisive match?

Category A has matches of 0.6 and a second one; category B has a single match. How does a category's share come out, and when does the total disagree with the best single match?

Each category's support is the sum of the similarities to its stored cases, and dividing by the sum over both gives a share. With two partial matches A reaches 0.8 and B's single 0.4 gives it only a third of the total. Raising B's match to 0.8 ties the totals. At 0.7, B owns the best single match, but A's two matches still add to more.

$$
\text{support}(K)=\sum_{c\in K}s(c),\qquad P(A)=\frac{\text{support}(A)}{\text{support}(A)+\text{support}(B)}
$$

**Symbols:** s(c): the similarity of the new case to stored case c; support(K): a category's total similarity over its stored cases; P(A): A's share of the total, when no category is given extra bias

**Predict:** A has 0.6 and 0.2 and B has 0.4. Predict how large B's single match must be before A's share falls to one half.

**Worked example:**
- Total for A: 0.8
- Total for B: 0.4
- A's share: 0.667
- Winner by total (by best single match): A (A)

A holds 0.8 from its matches and B 0.4, so A's share is 0.667. By total support the winner is A; by the single best match it is A.

**Calculation:** A: 0.6 + 0.2 = 0.8. B: 0.4. Share of A = 0.8/(0.8 + 0.4) = 0.667. This is the equal-bias case, with no response-bias weights.

**Takeaway:** Adding similarities over every stored case can pick a different category from the single best match.

**What happens:** At Similarity of B's one match = 0.7, Similarity of A's second match = 0.2: B's match of 0.7 is higher than any single match of A (0.6), yet A's total of 0.8 still wins, with a share of 0.533. A category can win through several partial matches even when no single case is decisive.

**Why it matters:** A rule that reads only the single closest case and a rule that sums over all cases behave differently near a boundary. Which one a system uses decides how it treats one strong lookalike against several moderate ones.

**In brains and behavior:** The semicircle model fit well, accounting for between about three quarters and nearly all of the pattern in the choices. It is a fitted model of two observers' behavior.

**In machines:** A system that sums similarity over stored cases is computing this rule as a specification; whether a given trained model does so internally is a separate question.

**Assumptions and limits:** Equal response bias for the two categories, as in the chapter. The similarities are chosen by hand and no data stand behind them.

**Check:** With A's matches 0.6 and 0.2, what share does A hold when B's one match is 0.8?

**Answer:** A's total is 0.8, B's is 0.8, and A's share is 0.8/(0.8 + 0.8) = 1/2.

**Source:** Sixteen semicircles, and weights that followed the task; anchor `sixteen-semicircles-and-weights-that-followed-the-task`. The chapter's constructed example: A has partial matches of 0.6 and 0.2, B has one of 0.4, and A's share is about 0.67. The practice question (B rising to 0.8 gives a share of 1/2) is in the book's back matter. Other values are the companion's own variation.

## C09-D05: What should a compact summary keep: shape or color?

An object has a shape bit and a color bit. Which of four summaries scores lowest when the target is shape, and what happens if the target or the trade-off weight changes?

Each summary pays one point per bit it keeps about the object and earns beta points per bit it keeps about the target. With a large enough weight, keeping the target wins. With weight 0 the target earns nothing, so keeping nothing wins. At weight 1 keeping shape and keeping nothing tie, and the rule alone does not choose between them.

$$
\min_T\; I(X;T)-\beta\,I(T;Y)
$$

**Symbols:** X: the input, here the object with its shape bit and color bit; T: the summary; its cost is the bits it keeps about X; Y: the target, the signal the summary must predict (shape or color); beta: the trade-off weight, zero or more, chosen first

**Predict:** At weight 2 and target shape, predict the lowest score and which summary reaches it. Then predict what happens at weight 0.

**Worked example:**
- Lowest score: -1
- Winner: keep shape only
- Score of keeping both: 0
- Score of keeping nothing: 0

With target shape and weight 2, the lowest score is -1, won by keep shape only. Changing the target or the weight changes the winner, because the purpose decides what is worth keeping.

**Calculation:** Score = bits about the object - 2 x bits about shape. Keep both: 2 - 2 x 1 = 0. Keep shape only: 1 - 2 x 1 = -1. Keep color only: 1 - 0 = 1. Keep nothing: 0.

**Takeaway:** A summary is good for a purpose, and the purpose is the target: change it and the winner changes.

**What happens:** At Target = shape, Trade-off weight (beta) = 2: Keeping shape only scores 1 - 2 = -1, below keeping both (0), color only (1) and nothing (0). No summary can score below -1 at this weight, since shape carries one bit and keeping shape reaches that bound.

**Why it matters:** A compact code that keeps color and drops a faint marking can score well on average and still miss the cases that matter. Someone has to name the purpose before the summary can be judged.

**In brains and behavior:** The toy does not explain the odd-number ratings and the bottleneck paper has no brain evidence. It is a way to say what a concept keeps, not a claim about what a mind keeps.

**In machines:** A designer or user has to decide what the system should preserve. In the toy the chosen purpose decides the winner.

**Assumptions and limits:** A summary keeps whole properties. Each property is one independent fair bit. The target is named before the summary is chosen, and the weight is set by hand; the paper itself says there is no single right solution for the trade-off.

**Check:** Target shape, weight 1. Which summaries tie for the lowest score?

**Answer:** Scores are 1 (both), 0 (shape only), 1 (color only) and 0 (nothing), so shape only and nothing tie at 0.

**Source:** A toy summary that keeps shape and drops color; anchor `a-toy-summary-that-keeps-shape-and-drops-color`. The chapter's constructed example (not data): two independent fair bits, four summaries and a weight set by hand to 2. The practice questions (weights 0 and 1) are the same toy at other weights. The paper behind the idea (Tishby, Pereira and Bialek) contains no data and no shape-and-color case.

## C09-D06: Why is the middle level of a name called basic?

Students listed attributes for names at three levels. Which step adds the most shared attributes?

Going from the broad name to the middle name adds 5.55 shared attributes. Going on to the most specific name adds only 2.02 more. The specific name still has the highest total, which is why the basic level is chosen by the size of the jump and not by the largest count.

$$
\text{share of the rise}=\frac{A_{\text{basic}}-A_{\text{super}}}{A_{\text{sub}}-A_{\text{super}}}
$$

**Symbols:** A_super, A_basic, A_sub: average shared attributes at the superordinate, basic and subordinate levels: 3.5, 9.05 and 11.07

**Predict:** The most specific level holds the most shared attributes. Predict what share of the whole rise comes in the first step, from the broad name to the middle name.

**Worked example:**
- Shared attributes at this level: 9.05
- Added by the step that reaches it: 5.55
- Share of the whole rise reached: 0.733
- Whole rise, top to bottom: 7.57

At the basic level the average is 9.05 shared attributes. The first step, from 3.5 to 9.05, adds 5.55, which is 0.733 of the whole rise of 7.57. That is why the middle level is called basic.

**Calculation:** Rise = 11.07 - 3.5 = 7.57. First step = 9.05 - 3.5 = 5.55, and 5.55/7.57 = 0.733. Second step = 11.07 - 9.05 = 2.02.

**Takeaway:** The middle level is basic because the largest gain in shared attributes comes there, even though the most specific level holds the most in total.

**What happens:** At Level = basic: The first step adds 5.55 of the whole 7.57, about 0.73, roughly three quarters. The second step adds only 2.02. The biggest jump comes at the middle level.

**Why it matters:** A name that buys a lot of shared structure at a small cost is useful for a mind or a system that must label things cheaply. Counting where the gain is largest, not where the total is largest, picks that level.

**In brains and behavior:** The students' lists are behavior. The chapter notes a related result on color words in 111 languages scored against a best possible trade-off, but the paper does not show that speakers compute a trade-off.

**In machines:** A system with a bottleneck cost could look for the level where one label buys the most for its cost. That is the chapter's interpretation, not a result of the study.

**Assumptions and limits:** The counts are attributes listed by at least six of 20 students. The study counted attributes; it fit no trade-off to these counts, and reading the middle level as a good trade is the chapter's interpretation, not the paper's.

**Check:** What share of the whole rise from 3.5 to 11.07 happens in the first step?

**Answer:** The whole rise is 11.07 - 3.5 = 7.57, the first step is 9.05 - 3.5 = 5.55, and 5.55/7.57 = 0.733.

**Source:** Names favor a middle level, and color words sat near a best trade-off; anchor `names-favor-a-middle-level-and-color-words-sat-near-a-best-trade-off`. Reported result, quoted from the chapter's account of Rosch and colleagues (1976): 200 students, 90 object names in nine taxonomies. The averages 3.5, 9.05 and 11.07 are the book's averages of the paper's raw tallies over six taxonomies (trees, fish and birds left out), not figures printed in the paper. The ratios computed here are the companion's arithmetic on them.
