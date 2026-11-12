# Chapter 8: Knowing How Things Relate

Store a fact in one direction, then ask whether it can be read from the other end.

Ask how each fact is stored: with head, relation and tail marked, or as a bare association. If the facts live in a graph, flip the grid and check whether the reversed relation is the one intended (has mother is not child of). If the facts live in a trained model, test both directions on held-out wordings, and compare reported scores only when the scoring rule is the same. Say which of the three the system relies on: direction kept by design, recovered by training on reversed text, or built into the geometry.

Practical question: My system answers 'who wrote X?' correctly but fails on 'what did Y write?' for the same fact. What should I check?

## C08-D01: Do equal averages show that a word pair is stored both ways?

If students recall about 57 percent of pairs from either end, what would the pair-by-pair record have to look like to count against two independent links?

A pair can be recalled from both ends, one end or neither. If recall from each end were independent, the share recalled both ways would be the product of the two averages, 0.569 x 0.565. When the ends go together, that share rises while the two averages stay put. Yule's Q turns the two-by-two table into one number from 0 (no tie) toward 1.

$$
Q=\frac{ad-bc}{ad+bc},\qquad a=p_fp_b+\phi\sqrt{p_f(1-p_f)\,p_b(1-p_b)}
$$

**Symbols:** p_f, p_b: share of pairs recalled forward and backward on the first test; phi: how closely recall from the two ends goes together, pair by pair; 0 means independent; a, b, c, d: shares of pairs recalled both ways, forward only, backward only, and neither; Q: Yule's Q, a tie between two yes/no outcomes: 0 for none, near 1 when they go together

**Predict:** The averages are 56.9 and 56.5 percent. If the two ends were independent, what share of pairs would students recall from both ends? Then move the correlation up and watch that share.

**Worked example:**
- Recalled from both ends: 32.1 percent
- Expected if independent: 32.1 percent
- Yule's Q: 0
- Forward and backward averages: 56.9 and 56.5 percent

Forward and backward recall average 56.9 and 56.5 percent in every state of this table, so the averages cannot tell the views apart. At correlation 0, 32.1 percent of pairs come back from both ends, against 32.1 if the ends were independent, giving Q = 0.

**Calculation:** Both ways = 0.569 x 0.565 + 0 x sqrt(0.569 x 0.431 x 0.565 x 0.435) = 0.3215. Forward only 0.2475, backward only 0.2435, neither 0.1875. Q = (a d - b c) / (a d + b c) = 0.

**Takeaway:** Equal forward and backward averages are the same under independence and under strong ties; only the pair-by-pair record separates them.

**What happens:** At Which pairs = all pairs, first test, Correlation between the two ends (pair by pair) = 0.6: At correlation 0.6, 46.9 percent of pairs come back from both ends, against 32.1 percent under independence, and Q is 0.884, about the size of the reported .88. The two averages never moved.

**Why it matters:** A system can look symmetric on average and still store two unrelated links. The test that decides is whether recall from one end predicts recall from the other for the same pair.

**In brains and behavior:** Fifteen students studied random noun pairs. Pair by pair, recall from one end tended to go with recall from the other, which weighs against independent links under the paper's assumptions. The pairs were not facts, and the neural mechanism is not shown.

**In machines:** A pair table with equal strengths in both directions returns the partner from either cue. That is a specification of a table, not a measured mechanism in the students.

**Assumptions and limits:** The curve is a construction: it fixes the two averages and varies the tie between them. The reported .88 and .91 come from retests of the same pairs, so they are reference marks, not points on this curve. Equal averages fit both a symmetric link and two independent links, as the paper says; they do not show a mechanism in the students' brains.

**Check:** In the studied-once table the averages are 32.9 and 33.6 percent. With correlation 0, what share of pairs is recalled from both ends?

**Answer:** 0.329 x 0.336 = 0.1105, so 11.1 percent. At correlation 0.8 the share is 28.8 percent, although the two averages are unchanged.

**Source:** Fifteen students recalled new random noun pairs about equally well from either end; anchor `fifteen-students-recalled-new-random-noun-pairs-about-equally-well-from-either-end`. Reported averages from the chapter's source note on Kahana (2002): first-test forward .569 and backward .565, and the once and five-times values .329, .336 and .732, .718. The chapter and its note give Yule's Q near unity (.88 and .91) for retests; the pair table at each correlation and the Q curve are this companion's own construction on those averages.

## C08-D02: How does flipping a grid read a fact from the other end?

If a grid stores who is mother of whom, what does the flipped grid answer, and what does a two-way pair table lose?

The grid has a 1 where a stored fact holds. Flipping it across its diagonal swaps heads and tails, so the same ones now answer the reverse question. Multiplying the grid by itself chains two facts into a grandmother fact. A table that fills in both directions loses the roles, so Bea's row lists her mother and her children together.

$$
A_{r^{-1}}=A_r^{\top}
$$

$$
(A_r^{2})_{ik}=\sum_j (A_r)_{ij}(A_r)_{jk}
$$

**Symbols:** A_r: grid with a 1 where the row person is mother of the column person, and 0 elsewhere; A_(r inverse): the relation read from the other end: has mother; top: the flip across the diagonal: rows become columns; A_r^2: the grid times itself: a 1 where two mother of facts chain, a maternal grandmother

**Predict:** After the flip, how many ones are in the grid, and which person's row of the flipped grid can never hold more than one 1?

**Worked example:**
- Ones in this grid: 2
- Stored mother of facts: 2
- Most answers for one person: 1
- Roles kept: yes

The grid has a 1 where the row person is mother of the column person, 2 ones in all. Each fact is stored with its head, relation and tail, so the roles are marked.

**Calculation:** Stored: Ana is mother of Bea; Bea is mother of Cy. A(head, tail) = 1 for each; every other entry is 0.

**Takeaway:** The flip reads each fact from tail to head with nothing new stored; the two-way table answers any row but cannot say who is the mother.

**What happens:** At Family = Cy is also mother of Dee, Which grid = has mother (flipped): With Cy mother of Dee added, the flipped grid has Dee's row pointing to Cy. It holds the same 3 ones as the original and stores no new fact.

**Why it matters:** The graph keeps direction because a designer built the roles in. A symmetric association retrieves a partner but erases which end played which part.

**In brains and behavior:** Whether people reverse facts through something like a flipped grid is not established. The chapter says the neural mechanism for retaining paired facts and their roles remains unresolved.

**In machines:** A knowledge graph is a specification: facts stored as head, relation and tail triples, and a flip reads them backward by design.

**Assumptions and limits:** Every fact is stored with its head, relation and tail marked. The flip gives has mother, not child of, which would also cover a father's children. In this family each child has one mother, but a mother may have many children; someone has to say which holds.

**Check:** In the Bea-has-two-children family, how many ones does the flipped grid have, and how many does a two-way pair table hold?

**Answer:** The flipped grid has 3 ones, the same as the 3 stored facts. The two-way table has 6 ones, since each fact appears in both directions, and Bea's row lists Ana, Cy and Dee with no way to tell the mother from the children.

**Source:** A knowledge graph and the flipped grid; anchor `a-knowledge-graph-and-the-flipped-grid`. Book equation and the chapter's made-up family (Ana, Bea, Cy). The extra rows for Dee follow the chapter's practice question and one constructed variant; nothing here is data.

## C08-D03: What did the reversal-curse experiment actually score?

A fine-tuned model scored 96.7 percent in one direction and 0.1 in the other. What was scored, on which facts, and what does that leave open?

For a description-first fact the trained order gives the description and asks for the name; the reverse gives the name and asks for the description. Exact match marks an answer right only if it equals the target, which is easier for names than for descriptions. That is why name-first facts score lower even in the trained order.

$$
\text{exact match}=\frac{\text{answers equal to the target}}{\text{questions asked}}
$$

**Symbols:** exact match: an answer counts as right only if it equals the target; trained order: the question is asked in the order the fact was shown in training; reverse order: the same fact asked from the other end

**Predict:** Name-first facts scored 50.0 percent in the trained order. Predict the reverse score before you choose that fact kind.

**Worked example:**
- Selected score: 96.7 percent
- Same facts, other order: 0.1 percent
- Drop from trained to reverse: 96.6 points
- Model: GPT-3, 175 billion parameters

On description-first facts the fine-tuned model scored 96.7 percent asked in the trained order and 0.1 percent asked from the other end. These are exact-match scores on the paper's invented facts, so the 96.6-point drop describes that test, not people or all models.

**Calculation:** Reported (Table 1 of the paper, as quoted in the chapter): trained order 96.7, reverse 0.1. Drop = 96.7 - 0.1 = 96.6 points. Exact match counts an answer only if it equals the target.

**Takeaway:** The model answered well only when the question matched the order of training, on invented facts, with an exact-match score.

**What happens:** At Fact kind = description-first, Order of the question = reverse order: On description-first facts the reverse order scored 0.1 percent, against 96.7 in the trained order, a drop of 96.6 points. On name-first facts the reverse score was 0.0.

**Why it matters:** A fact stored in a model is not automatically stored with its roles reversible. Any test of a system's knowledge should ask the question from both ends.

**In brains and behavior:** People were not tested. Kahana's students recalled word pairs about equally from both ends, but those were not facts, so the comparison stays open.

**In machines:** This is a behavior measured on one family of fine-tuned models. The authors leave the cause open; a 2024 proof applies to a toy model under stated assumptions.

**Assumptions and limits:** The facts were invented and the model was fine-tuned through an API in 2023. The chapter says the paper does not tell whether the results describe models as they are today, and that people were not tested; its authors say they know of no such stark ordering effect in humans. When the fact and three worked examples were placed in the prompt, the models reversed it at or near 100 percent, which is a different thing from fine-tuning.

**Check:** Name-first facts scored 50.0 percent in the trained order and 0.0 in reverse. Can this be read as a smaller reversal problem than for description-first facts?

**Answer:** No. The drop is 50.0 points against 96.6, but the trained-order score is lower partly because exact match is harder for descriptions. Both reverse scores are close to zero.

**Source:** GPT-3 learns facts in one order only; anchor `gpt-3-learns-facts-in-one-order-only`. Reported results quoted in the chapter from Berglund and colleagues (2023, ICLR 2024), Table 1: GPT-3 with 175 billion parameters fine-tuned on invented facts, 96.7 and 0.1 percent for description-first facts, 50.0 and 0.0 for name-first facts. No computation is run here.

## C08-D04: What does adding reversed copies of the text buy?

If the training text includes a reversed copy of every passage, how much of the reversed-question score returns, and for which kind of fact?

Standard fine-tuning shows the model each passage once. Reverse training adds a copy with the order changed, so the model sees an answer before its cue. Reversing every word barely helped in a smaller test. Keeping names intact worked for name-first facts; cutting text into random chunks helped on both kinds.

$$
\text{gain}=\text{score}_{\text{method}}-\text{score}_{\text{standard fine-tuning}}
$$

**Symbols:** score: soft match: right if the target appears near the start of the reply; names kept: reverse the words but keep each name in its original order; random chunks: cut the tokens into chunks of random length and reverse the order of the chunks

**Predict:** Name-first reversed questions scored 0.0 percent under standard fine-tuning. Predict the score with names kept in order, then with random chunks, and whether description-first facts behave the same way.

**Worked example:**
- Reversed-question score: 0.0 percent
- Standard fine-tuning, same facts: 0.0 percent
- Gain over standard: 0.0 points
- Forward accuracy: 78.3 to 80.3 percent

On name-first facts, reversed questions scored 0.0 percent with standard fine-tuning, against 0.0 with standard fine-tuning. These are soft-match scores from one preprint on invented facts, not like for like with the exact-match scores of the previous demonstration.

**Calculation:** Reported scores (the chapter's Figure 8.5): name-first facts, standard fine-tuning: 0.0. Gain = 0.0 - 0.0 = 0.0 points. The number of facts and runs behind the table is not stated.

**Takeaway:** Reversed copies repaired the symptom on name-first facts, but the gain depended on the kind of fact and the grain of reversal.

**What happens:** At Fact kind = description-first, Training = names kept in order: On description-first facts, keeping names in order moved the score only from 4.0 to 6.0 percent, while random chunks reached 70.0. Name-first facts jumped from 0.0 to 89.7 and 99.0.

**Why it matters:** Giving a system the reverse direction in its training data is one way to supply direction. The cost is that every passage is used twice, and the repair is reported for a particular test, not for every kind of knowledge.

**In brains and behavior:** Nothing in this experiment concerns people.

**In machines:** A behavior measured on one 7B model in one preprint. The reversal sketched on the left shows the mechanical idea only.

**Assumptions and limits:** A preprint, not peer reviewed in the chapter's account. The number of facts, runs and spread behind the table is not stated. Soft match is more generous than exact match, so these scores are not like for like with the previous demonstration. Forward accuracy of 78.3 to 80.3 percent is quoted for the name-first rows only in the chapter's source note.

**Check:** How many points does random-chunk training gain over standard fine-tuning on description-first facts?

**Answer:** 70.0 - 4.0 = 66.0 points, against 6.0 - 4.0 = 2.0 points for names kept in order.

**Source:** Training on reversed copies of the facts; anchor `training-on-reversed-copies-of-the-facts`. Reported results quoted in the chapter from Golovneva and colleagues (2024 preprint, Table 6): a 7-billion-parameter Llama-2 model on invented facts, reversed questions, soft match. The sentence shown on the left is the chapter's own invented fact; the reversal shown is this companion's sketch of the operation as the chapter describes it, with words standing in for tokens.

## C08-D05: Why can a model learn A to B and still miss B to A?

In a tiny lookup with separate input and output vectors, what happens to the reversed question as the forward fact is learned, and what does a reversed copy change?

Each entity has two vectors, one used as the question and one as an answer. Learning that b answers a moves the question vector of a and the answer vector of b. The reversed question starts from the question vector of b, which was not moved, so its answer stays near chance. A reversed copy trains those parameters directly.

$$
p(y\mid x)=\frac{e^{\mathbf u_x\cdot\mathbf v_y}}{\sum_j e^{\mathbf u_x\cdot\mathbf v_j}}
$$

**Symbols:** u_x: input vector of entity x, used when x is the question; v_y: output vector of entity y, used when y is a candidate answer; p(y | x): the toy's chance of answering y when asked about x

**Predict:** After 50 steps on forward facts only, will the reversed question be answered better than chance? Then add reversed copies and predict again.

**Worked example:**
- Forward question: 96.5 percent
- Reversed question: 3.9 percent
- Chance level: 5.0 percent
- Facts trained: 5, each as a to b

After 50 steps of forward facts only among 20 entities, the toy answers the forward question 96.5 percent of the time and the reversed one 3.9 percent, against 5.0 by chance. This is a constructed toy with a seeded start, not a language model and not a theorem.

**Calculation:** Each entity has an input vector and an output vector (8 numbers each, seed 2026). A question about x gets chance exp(u_x . v_y) / sum over j of exp(u_x . v_j) for answer y. Training moves only the vectors involved, 5 facts, step size 0.1, 50 steps.

**Takeaway:** In this toy the reverse direction is a separate lookup that forward training never touches, and training on the reversed copy supplies it.

**What happens:** At Training text = forward facts only, Entities in the toy = 20, Training steps = 50: After 50 steps the forward question is answered about 96 percent of the time and the reversed one about 3.9 percent, a little below the 5 percent chance level. Adding reversed copies lifts the reversed question to about 96 percent too.

**Why it matters:** It gives a concrete way to see why a system can hold a fact in one direction only: the parameters that serve the reverse question are different parameters. A repair has to reach them.

**In machines:** A seeded toy of the mechanism the chapter's references discuss. No claim about how real models store facts follows from it.

**Assumptions and limits:** A simulation is a computation, not a measurement. The toy has no language, no paraphrases and no pretraining. A question about b uses the input vector of b, which the forward facts never moved, so the reversed question can only change through small side effects; the chapter says nothing about how large models are organized.

**Check:** Why is the reversed answer not exactly at chance after training on forward facts only?

**Answer:** Training also pushes the answer vectors of other entities away from the trained question vectors. That shifts every answer slightly, so the reversed chance drifts a little below 5 percent instead of staying exactly there.

**Source:** GPT-3 learns facts in one order only; anchor `gpt-3-learns-facts-in-one-order-only`. Constructed toy, in the spirit of the chapter's mention of a 2024 proof about a simple model where the A to B link grows while the B to A link stays small. It is this companion's own simulation, seed 2026, step size 0.1, 8 numbers per vector; it is not the proof, not their model, and not a language model.

## C08-D06: How does a step on a line read a relation, and how does negating it read it backward?

If next town east is a step of one stride, what gap does the fact score, what happens when head and tail swap, and what does negating the step do?

The step takes the head point to a landing point. The fact fits when the landing point is the tail. If you swap head and tail but keep the step, the landing point is a stride past the old head, so the miss is twice the step. Negating the step on the swapped pair always reproduces the original gap, since |t - r - h| = |h + r - t|.

$$
f(h,r,t)=\lVert \mathbf h+\mathbf r-\mathbf t\rVert
$$

**Symbols:** h, t: the head and tail towns as points on the road (Ash at 0, Birch at 1); r: the relation step, here one stride east, +1; f: the gap between where the head plus the step lands and the tail; 0 is a perfect fit

**Predict:** With Birch as head and Ash as tail, what is the gap for the eastward step, and what is it after you negate the step?

**Worked example:**
- Gap f (strides): 0
- Step lands at: Birch
- Fits exactly: yes
- Swap head and tail, same step: 2 strides

From Ash at 0, a step of +1 lands at 1, and the tail Birch is at 1, so the gap is 0 strides. Swapping the roles with the same step gives a gap of 2 strides; negating the step on the swapped pair always gives back 0.

**Calculation:** f = |h + r - t| = |0 + (1) - 1| = 0. Swapped, same step: |1 + (1) - 0| = 2. Swapped with the negated step: |1 + (-1) - 0| = 0.

**Takeaway:** Swapping head and tail with the same step misses by twice the step; negating the step reads the relation backward and the miss closes.

**What happens:** At Head town = Birch, Tail town = Ash, Relation step = one stride east: With Birch as head and Ash as tail the eastward step lands at Cedar, 2 strides past the tail, so the gap is 2. Switch the step to one stride west and the gap closes to 0.

**Why it matters:** A translation score builds direction into the geometry: the fact fits one way, and the reverse costs a sign. The cost is that a relation true in both directions cannot keep a nonzero step.

**In machines:** TransE is a published model for scoring facts in a knowledge base; the line of towns is an illustration. The reversal by negating the step follows from the algebra, not from the paper.

**Assumptions and limits:** Each relation is one fixed step, and an entity has the same point as head or as tail. A relation that holds both ways, such as sibling of, breaks the trick: an exact fit both ways forces the step to zero and puts the two entities at the same point. Nothing here shows that language models represent relations this way.

**Check:** With Ash as head, Cedar as tail and the eastward step, what is the gap?

**Answer:** Ash at 0 plus 1 lands at 1, the tail Cedar is at 2, so the gap is 1 stride.

**Source:** A relation became a step, and reversing the step read it backward; anchor `a-relation-became-a-step-and-reversing-the-step-read-it-backward`. Book equation (the TransE score of Bordes and colleagues, 2013) and the chapter's town example: Ash at 0, Birch at 1, an eastward step of 1. Cedar at 2 is added by this companion as a third constructed town. The paper does not discuss reading a relation backward; the negated step is the chapter's own short algebra.

## C08-D07: What does a hits-at-k score count?

If a model ranks every town as a candidate tail, how often does the true tail land in the top k, and how fast does that fall as the learned positions blur?

For each head, every other town is ranked by its gap to where the head plus the step lands. The true tail is rank 1 when positions are exact. As each position is blurred, other towns can land nearer, and the true tail slides down the ranking. Hits at k is the share of tests that stay in the top k.

$$
\text{hits at }k=\frac{\text{tests where the true tail ranks in the top }k}{\text{tests}}
$$

**Symbols:** rank: 1 plus the number of other candidates with a smaller gap f than the true tail; k: the cutoff: the true tail counts if its rank is at most k; noise sd: spread of the error added to each learned position, in strides

**Predict:** With 29 candidates, what hits-at-10 would pure guessing give? Then predict how large the error in each position must be before the true tail falls outside the top 3 in half the tests.

**Worked example:**
- Hits at 3: 99.2 percent
- Chance level: 10.3 percent
- Median rank of the true town: 1
- Tests: 5800 (200 blurs x 29 towns)

With each learned position blurred by sd 0.5 strides, the true next town ranks in the top 3 in 99.2 percent of tests, against 10.3 by chance among 29 candidates. This is a constructed road of 30 towns, not a benchmark, and its numbers do not compare with the paper's.

**Calculation:** Rank of the true tail = 1 + the number of other towns whose gap |h + 1 - t| is smaller than the true gap. Hits at 3 = tests with rank <= 3 divided by 5800. Positions are the integers 0 to 29 plus normal error with sd 0.5, seed 2026.

**Takeaway:** Hits at k measures whether the true answer is near the top of a ranking, so it is read against the chance level k over the number of candidates.

**What happens:** At Error sd in each learned position (strides) = 1, Cutoff k = 3: At an error sd of 1 stride, equal to the spacing between towns, the true tail ranks in the top 3 in 83.1 percent of tests but is the single best guess in only 38.1 percent. Chance for k = 3 is 10.3 percent, and at sd 0 every test is a hit at 1.

**Why it matters:** A hits number means little until you know the candidate list and the chance level. It also says nothing about reading a relation backward, which the benchmark did not test.

**In machines:** The ranking by the gap f is the specification from the chapter; the benchmark numbers are 2013 results against 2013 competitors.

**Assumptions and limits:** A simulation is not a measurement. The road is a single relation with exact steps plus normal error, so it is far easier than a knowledge base with many relations, and its percentages do not compare with the paper's. With one true tail per head, the filtered and unfiltered rankings agree here.

**Check:** With 29 candidates, what share of tests would random ranking put in the top 10?

**Answer:** 10 / 29, about 34.5 percent. A hits-at-10 score is only informative once it is read against that level.

**Source:** A relation became a step, and reversing the step read it backward; anchor `a-relation-became-a-step-and-reversing-the-step-read-it-backward`. The metric is the chapter's: hits at 10 in the filtered evaluation, 89.2 percent on WordNet and 47.1 percent on FB15k in 2013 benchmarks. Those figures are not recomputed. The road of 30 towns and its blurred positions are this companion's constructed simulation, seed 2026, 200 blurs.
