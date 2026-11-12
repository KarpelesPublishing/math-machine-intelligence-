# Chapter 26: Where the Starting Structure Comes From

Find a starting design by search, and see what choosing can and cannot do without people.

Ask who supplied the candidates, who said which was good, and whether the test that picked the winner is separate from the test that reports it. Use the odds card for how hard a single good setting is to find, the choosing-and-copying split to see whether a change came from reweighting what was there or from new variation, and the replicator card to check whether the best kind was in the pool at all. Report the score with the size of the test and the choices people made.

Practical question: A search over 1,000 recipes picked one that scored 52 percent on a 250-problem test, and the best starting model scored 30. Is that a trustworthy gain, and what did people supply?

## C26-D01: How hard is it to stumble on the one good wiring?

A creature's 20 connections are each present or absent, and only one pattern is good. If its fixed genes are all right and some switches are left open, how likely is it to find the good wiring by random tries in a lifetime?

One try sets k open switches at random, so it hits the good setting with chance 1 in 2^k. The chance of missing on every one of G tries is the leftover chance multiplied by itself G times, and one minus that is the chance of finding it.

$$
P=1-\bigl(1-2^{-k}\bigr)^{G}
$$

**Symbols:** k: the number of open switches (genes marked ?) the creature sets at random on each try; G: the number of tries in a lifetime; 2^(-k): the chance that one random try sets all k open switches right

**Predict:** Predict how the chance changes if the open switches go from 10 to 20, with 1,000 tries in both cases.

**Worked example:**
- Chance of finding it: 0.624
- Settings of the open switches: 1,024
- Tries for even odds: 710
- Wirings in all (20 switches): 1,048,576

A creature with 10 open switches and all its fixed genes right finds the good wiring in up to 1,000 tries with chance 0.624. The chapter's two cases are 10 open switches (about 62 in 100) and 20 (under 1 in 1,000) at 1,000 tries.

**Calculation:** P = 1 - (1 - 2^(-10))^1000 = 1 - (1 - 0.0009766)^1000 = 0.624. One random try on 20 switches succeeds with chance 2^(-20) = 9.54e-07.

**Takeaway:** A few open switches make the good wiring easy to find in a lifetime, and many make it nearly hopeless, so how many genes are already right matters more than the number of tries.

**What happens:** At Open switches (?) = 10, Tries in a lifetime = 1000: With 10 open switches, up to 1,000 tries find the good wiring about 62 times in 100. With 20 open switches the chance falls to under 1 in 1,000, since there are 1,048,576 settings to wander through and only 1,000 looks.

**Why it matters:** This is why learning could help evolution only for creatures whose inherited genes were mostly right. Choosing among creatures then rewards the ones whose open switches are few.

**In brains and behavior:** The brain side is a possibility: an inherited capacity to learn could smooth evolution's search. The simulation did not measure that process in brains.

**In machines:** In a machine search the same arithmetic gives the cost of random trials in a space with 2^k settings.

**Assumptions and limits:** The creature's fixed genes are all right, each try sets every open switch independently at random, and tries are independent. A creature with a wrong fixed gene can never succeed.

**Check:** With 5 open switches and 100 tries, is finding the good wiring likely, and about how many tries give even odds?

**Answer:** Very likely: 1 - (31/32)^100 is about 0.96. Even odds need about 22 tries.

**Source:** Learning that no child inherited still changed who had children; anchor `learning-that-no-child-inherited-still-changed-who-had-children`. Book arithmetic built on the chapter's setup (20 connections, one good wiring, up to 1,000 tries). The chapter gives the two cases, 10 open switches (about 62 in 100) and 20 (under 1 in 1,000); they are the book's arithmetic, not results in the Hinton and Nowlan paper. The other values are this companion's variations.

## C26-D02: What happens to the genes when only the choosing of parents changes?

1,000 creatures each carry 20 genes of 1, 0 or ?. They learn by random tries, and the quick learners leave more children. What do the gene shares do over 50 generations, though nothing learned is written into a gene?

A creature with any 0 gene never finds the good wiring and gets the baseline weight. One with no 0 genes and few ? genes often finds it early, and the earlier the more weight. Parents are drawn in proportion to weight and cross their genes, so the 0 alleles are removed and the 1 alleles rise.

$$
w=1+\frac{19\,n}{G},\qquad n=G-t
$$

**Symbols:** w: a creature's weight as a parent; 1 if it never finds the good wiring; t: the try on which it first finds the good wiring; G: the tries available (1,000); n: tries left after the finding, which sets how much extra weight it earns

**Predict:** Predict what happens to the share of 0 genes, and whether the ? genes disappear, though no learned setting reaches a gene.

**Worked example:**
- Share of 1 at generation 50: 0.768
- Share of 0 at generation 50: 0
- Share of ? at generation 50: 0.232
- Open switches per creature, start to end: 10 to 4.64

In seeded run 1, the share of 1 genes goes from 0.252 to 0.768 in 50 generations and the share of 0 genes from 0.247 to 0, with no learned setting ever written into a gene. Many ? genes remain, so the good wiring is not yet inherited.

**Calculation:** Each creature draws its first successful trial from a geometric law with chance 2^(-open switches), or never succeeds if any gene is 0. Parent weight = 1 + 19 n / 1000, n the trials left. Single-point crossover, no mutation, 1,000 creatures, 20 genes.

**Takeaway:** Learning changed who had children, and that alone shifted the inherited genes toward the right settings, although every child started over.

**What happens:** At Seed of the run = 1: The share of 0 genes drops to zero within about 10 generations in this seeded run because a creature with a 0 gene can never find the good wiring, and 1 genes spread. The share of ? genes shrinks more slowly, and many remain at generation 50, so the right wiring is not yet inherited.

**Why it matters:** This is the Baldwin effect in a toy: a trait that first needs learning can come to be built in. The chapter's caution is that the plotted run did not show the right wiring becoming fully innate.

**In brains and behavior:** A possibility, not a measurement: an inherited capacity to learn could smooth evolution's search.

**In machines:** The simulation is a specification of a search, with the reward for quick learners fixed by the experimenters.

**Assumptions and limits:** Learning is the blunt rule in the chapter: random settings of the open switches on each try, frozen once the good wiring is found. Nothing learned is inherited. The case is extreme and unrealistic, as the authors say, and the simulation did not measure any process in brains. The paper does not fully specify some details, so the companion's choices may differ.

**Check:** Why does the share of 0 genes fall so much faster than the share of ? genes?

**Answer:** A single 0 gene rules a creature out of ever finding the good wiring, so selection removes 0 strongly. A ? gene only lowers the chance of finding it, and the effect fades as other ? genes become 1, so ? genes go away slowly.

**Source:** Learning that no child inherited still changed who had children; anchor `learning-that-no-child-inherited-still-changed-who-had-children`. Seeded reimplementation by this companion, built from the chapter's description of Hinton and Nowlan (1987): 1,000 creatures, 20 genes started at 1, 0 or ? with chances a quarter, a quarter and a half, up to 1,000 random tries, parent weight 1 + 19n/1000, single-point crossover, no mutation. Eight seeded runs. It is not the authors' code, and the paper shows one typical run without a run count, so these runs are not a reproduction of its figure.

## C26-D03: How often does the right wiring end up fully built in?

Run the 1987 simulation until the correct wiring fixes in every creature, or until a wrong or open setting fixes and the right wiring becomes impossible. How often does it fix, and does the number of tries matter?

Each run follows the population until some position is fixed. If every position is fixed on 1 the run is a success. If some position is fixed on a 0 or a ? the right wiring cannot become innate without mutation, so the run is a failure. The share of successes estimates the chance of full fixation.

$$
\hat p=\frac{\text{runs where the right wiring fixed}}{\text{runs}}
$$

**Symbols:** p-hat: the share of runs in which every creature ends up carrying the right wiring; G: the trial budget per lifetime

**Predict:** Predict whether more tries per lifetime always raise the share of runs that end with the right wiring built in.

**Worked example:**
- Right wiring fixed: 19 of 200
- Share (95 percent interval): 0.095 (0.062 to 0.14)
- Mean generations per run: 492
- Reported at 1,000 tries: 0.167 (16.7 percent)

With 1,000 trials per lifetime, the right wiring fixed in 19 of 200 seeded runs, a share of 0.095. The chapter reports 0.167 at 1,000 trials for Fontanari and Santos; this reimplementation is not their code, so close agreement is not claimed.

**Calculation:** Share = 19 / 200 = 0.095. 95 percent Wilson interval 0.0617 to 0.144, which treats the runs as independent.

**Takeaway:** With learning, the right wiring fixed in roughly one run in ten here and about one in six in the chapter's report, against an estimated 1 in 10 million without it. How often it fixes depends on settings such as the trial budget.

**What happens:** At Trials per lifetime = 1000: At 1,000 tries the right wiring fixed in 19 of 200 seeded runs, about 1 in 10, a little below the chapter's reported 16.7 percent (the interval runs from about 0.06 to 0.14). More tries are not always better: 100 and 300 tries fixed it more often, about 0.27, and 3,000 less often.

**Why it matters:** The 1987 plot showed learning being selected, not the right wiring becoming innate. Counting how runs end is the test the chapter says Fontanari and Santos applied.

**In brains and behavior:** A model of evolution, not a measurement of any brain.

**In machines:** A search with a fixed supply of variation: no mutation, so a version of a gene missing from the first generation could never appear.

**Assumptions and limits:** Runs stop as soon as a wrong or open setting fixes at any position (a failure) or the right wiring fixes everywhere (a success); a 20,000-generation cap would count as unfinished. The intervals treat the 200 runs as independent. For budgets other than 1,000 the weight is 1 + 19n/G, which is the companion's choice.

**Check:** Why would a run be counted as a failure if every creature carries a ? at one position, even though many creatures learn the good wiring?

**Answer:** With no mutation, the ? at that position cannot become a 1 by crossover, since every parent carries ?. The wiring can still be learned but is never fully inherited, which is the outcome the test excludes.

**Source:** Running the 1987 simulation to the end: about one run in six; anchor `running-the-1987-simulation-to-the-end-about-one-run-in-six`. Seeded reimplementation by this companion (200 runs per budget, the same rules as the previous demonstration), compared with the value the chapter reports from Fontanari and Santos (2017): 16.7 percent with learning at 1,000 trials, and an estimated 1 in 10 million without learning, read from a fitted curve. The chapter says the book's own rerun gave 0.164 (standard error 0.004); this reimplementation is not that rerun and has not been tuned to match.

## C26-D04: How much of a change in the average came from choosing, and how much from copying?

Four seeds have hook lengths 0, 1, 2 and 3 mm and leave 1, 1, 2 and 2 seedlings. D's seedlings come out 0.3 mm shorter than D. How much does the average hook change, and from which source?

The covariance of offspring with trait is how much the seeds with more offspring differ in hook length, scaled by the average offspring. The second term averages how much seedlings differ from their parents, weighted by the offspring each seed leaves. Together they are the whole change.

$$
\Delta\bar z=\underbrace{\frac{\operatorname{Cov}(w,z)}{\bar w}}_{\text{choosing}}+\underbrace{\frac{\operatorname{E}(w\,\Delta z)}{\bar w}}_{\text{copying}}
$$

**Symbols:** z: a seed's trait (hook length in mm); w: offspring left by that seed; w-bar: the average offspring; Delta z: how a seedling's trait differs from its parent's

**Predict:** Predict the sign of the net change when D's seedlings come out 0.3 mm shorter, and whether it is bigger or smaller than choosing alone.

**Worked example:**
- Choosing: +0.333 mm
- Copying: -0.100 mm
- Net change: +0.233 mm
- Average hook, before to after: 1.50 to 1.73 mm

Choosing lifts the average hook by 0.333 mm, copying changes it by -0.100 mm, and the net is +0.233 mm. The two parts add up exactly to the change in the average.

**Calculation:** Mean offspring = 1.500. Choosing = Cov(offspring, hook) / mean offspring = 0.333. Copying = average of (offspring x change in hook) / mean offspring = -0.100. Sum = +0.233.

**Takeaway:** Choosing reweights the seeds the field already holds, while copying changes what the seedlings are, and the two add exactly to the change in the average.

**What happens:** At Change in D's seedlings (mm) = -0.3, Seedlings D leaves = 2: Choosing alone lifts the average hook by one third, from 1.5 to about 1.83 mm. D's shorter seedlings pull it down by 0.1. The net rise is about 0.23 mm, and the two parts add up exactly.

**Why it matters:** A change in what a pool holds can come from picking among candidates or from making new ones. A search that only picks can never leave what the pool already contains.

**In brains and behavior:** Price's identity is bookkeeping for any trait, including genes. It says nothing about how a brain learns.

**In machines:** In a model search, choosing is the rule that keeps high-scoring candidates and copying is the variation that proposes new ones.

**Assumptions and limits:** One generation, a fixed list of seeds, and copying changes only for D's seedlings. The split is an exact bookkeeping identity for any trait, so it describes the change without explaining a mechanism.

**Check:** If D left 3 seedlings and its seedlings came out 0.3 mm shorter, what is the net change?

**Answer:** Choosing is 0.5 (offspring 1, 1, 2, 3; mean 1.75) and copying is 3 x (minus 0.3) / 4 / 1.75 = minus 0.129, so the net is about plus 0.371 mm.

**Source:** A field of seeds, and a striped seed that stays at zero; anchor `a-field-of-seeds-and-a-striped-seed-that-stays-at-zero`. Book formula and worked example (George Price's 1970 split). The chapter's four-seed field and its numbers (choosing 1/3, copying minus 0.1, net about 0.23) are reproduced at the reveal state. The other shifts and offspring counts for D are this companion's variations.

## C26-D05: Why does a seed the field does not hold never appear by choosing?

A field has round, wrinkled and speckled seeds leaving 1, 2 and 4 offspring each, and no striped seeds, which would leave 10. What does one round of choosing do, and what would bring striped seeds in?

Multiply each kind's share by its offspring and divide by the total so the shares add to one again. Striped has a share of zero, so its product is zero and its next share is zero. Moving some speckled offspring into striped each round puts a nonzero share in, after which striped's 10 offspring let it spread.

$$
x_i'=\frac{x_i\,f_i}{\sum_j x_j\,f_j}
$$

**Symbols:** x_i: the share of kind i now; x_i': its share next round; f_i: the offspring left by each member of kind i

**Predict:** Predict the striped share after one round, then after 12, when it starts at zero and nothing copies it in.

**Worked example:**
- After round 1 (round, wrinkled, speckled, striped): 0.25, 0.25, 0.5, 0
- Striped share after 12 rounds: 0
- Round share after 12 rounds: 1.19e-07

Round falls to a quarter, wrinkled holds at a quarter, speckled doubles to a half, and striped stays at zero however well it would have done. Zero times anything is zero, so no number of rounds brings it back.

**Calculation:** New share = share x offspring / sum of (share x offspring). From (0.5, 0.25, 0.25, 0) with offspring (1, 2, 4, 10): products 0.5, 0.5, 1.0, 0, total 2, new shares 0.25, 0.25, 0.5, 0. The copy-error step is this companion's addition.

**Takeaway:** Choosing can only reweight what the pool holds. A kind with a share of zero stays at zero, and even a tiny nonzero share can take over if its offspring are numerous.

**What happens:** At Speckled offspring that come out striped = 0.0, Striped share at the start = 0.0: One round gives round 0.25, wrinkled 0.25, speckled 0.5 and striped 0. Zero times anything is zero, so striped stays at zero however many rounds pass. With a small copy error or a small starting share, it takes over within a dozen rounds.

**Why it matters:** A search that picks among candidates needs a source of candidates. In 1987 the starting pool already held the right piece at every position, so learning only had to help choosing combine them.

**In brains and behavior:** Nothing here measures a brain. The replicator rule keeps the books for a pool without showing the mechanisms match.

**In machines:** In the merge search, the random nudges and the people who chose the sources supply the candidates.

**Assumptions and limits:** A fixed list of kinds and a positive total. Choosing alone, with no copy error, cannot add a kind. A nonzero starting share or a copy error changes that. The step form does not show that any real mechanism matches the arithmetic.

**Check:** If striped starts at 0.01 with no copy error, does it ever appear in the next round's shares, and does it take over?

**Answer:** Yes: its share is 0.01 x 10 divided by the new total, about 0.047 after one round, and it grows each round and takes over within a dozen. Starting above zero matters.

**Source:** A field of seeds, and a striped seed that stays at zero; anchor `a-field-of-seeds-and-a-striped-seed-that-stays-at-zero`. Book formula (the replicator rule in its step form, from Taylor and Jonker 1978) and constructed ledger: shares 0.5, 0.25, 0.25 and 0, offspring 1, 2, 4 and 10, which hold no real data. The copy-error step, where some speckled offspring come out striped, and the nonzero starting shares are this companion's variations, in the spirit of the chapter's note that variation in copying can introduce a missing type.

## C26-D06: How much should a 52 percent score on 250 problems be trusted?

A search merged three models into one that scored 52.0 percent on 250 held-out Japanese math problems, against 9.6, 18.4 and 30.0 for the sources. What do the scores say, and what could a 250-problem test tell apart?

Each score is a share of 250 problems. A test of that size can only separate scores that differ by more than about the width of the bars, which is wider for small tests and for scores near one half. The merge's lead over its best source is much larger than that width at 250 problems.

$$
\text{problems correct}=\frac{\text{percent}}{100}\times 250
$$

**Symbols:** 250: the held-out test problems, kept out of the 1,069 that drove the search; 95 percent bar: the Wilson interval for a score if the problems were a random sample of a larger pool (the companion's addition)

**Predict:** Predict the smallest test size at which the interval around the merge no longer overlaps the best source's.

**Worked example:**
- Reported score: 52 percent
- Problems correct at 250: 130 of 250
- 95 percent bar at 250 problems: 45.8 to 58.1
- Merge bar clear of the best source's?: yes

Searched merge scored 52 percent, which is 130 of 250 problems. If the test problems were a random sample, a test of 250 would put its score between 45.8 and 58.1. The bars say nothing about the people who chose the sources, the method and the test.

**Calculation:** 52 percent of 250 = 130 problems. Wilson 95 percent bar at n = 250: 45.8 to 58.1. Merge 52.0 against the best source 30.0: separated at this size.

**Takeaway:** Sampling alone does not explain the gap between 52.0 and 30.0 on 250 problems, but the result still depends on what people supplied and on one test.

**What happens:** At Which model = merge, Problems in the test = 250: The merge's 52.0 is 130 of 250. At 250 problems its 95 percent bar, roughly 46 to 58, sits clear of the best source's, roughly 25 to 36. With 50 problems the bars overlap, and they separate by 100. The bars show only how finely a test of that size can tell; they say nothing about who chose the sources, the method and the test.

**Why it matters:** A search can explore recipes and score them, but it cannot find a candidate outside the space it was allowed to try. A person can change that space or the test while the machine explores the alternatives.

**In brains and behavior:** No brain is involved. The sources, the search space and the test were all chosen by people.

**In machines:** The search used a random-sampling method (CMA-ES) around a changing center, scored each candidate on the 1,069 training problems, and checked the chosen recipe on the 250 held-out ones.

**Assumptions and limits:** One test, in one language. People chose the three sources, the merging method and the test. The intended criterion needed a correct number and Japanese reasoning, scored by imperfect automatic checks. If designers kept changing recipes after seeing the 250 answers, that set would become part of selection. The bars treat the problems as a random sample, which they are not.

**Check:** How many of the 250 problems did the best source get right, and is the merge's lead there beyond the sampling bars?

**Answer:** 30.0 percent of 250 is 75 problems, against 130 for the merge. The merge's lower bar (about 46) is above the best source's upper bar (about 36), so sampling alone does not explain the lead. Other limits remain.

**Source:** A search merged three models into a better one; anchor `a-search-merged-three-models-into-a-better-one`. Reported scores quoted in the chapter from Akiba and colleagues (2025): the three sources scored 9.6, 18.4 and 30.0, and the merge the paper labels PS scored 52.0 on 250 test problems, after 1,000 trials of CMA-ES on 1,069 training problems. The counts correct and the sampling bars are this companion's arithmetic. No simulation.
