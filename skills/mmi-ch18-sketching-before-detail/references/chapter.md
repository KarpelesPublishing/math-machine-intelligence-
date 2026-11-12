# Chapter 18: Sketching Before Detail

Count the passes saved by a rough-first method, sharpen a number level by level, and see what a vote among drafts cannot fix.

Count passes and position-updates before comparing speeds, and remember that a count is not a timing. Check whether a level can overturn an earlier one, because a stack that only adds corrections cannot undo an overshoot. When choosing among several drafts, ask whether the drafts could share a mistake, since agreement measures typicality and not truth.

Practical question: My system draws several answers and keeps the one most like the others. Does that make the kept answer correct?

## C18-D01: How many passes does it take to build a text?

A 16-position text can be built one position at a time, by filling every position in several passes, or level by level. How many passes and position-updates does each take?

One at a time, each pass picks one token using everything before it, so a text takes as many passes in a row as it has tokens. Filling everything repeats a pass over all positions. Levels start with a rough version of the whole text with very few positions and each later level adds detail, so the number of passes equals the number of levels: log2 of the length plus 1 in this doubling toy, and a fixed 12 in the paper.

$$
\text{passes}_{\text{levels}}=\lceil\log_2 L\rceil+1,\qquad \text{updates}_{\text{levels}}=1+2+4+\cdots+L=2L-1
$$

**Symbols:** L: the number of positions in the text (a power of two here, for easy counting); pass: one run of the model; one level is one pass; position-update: one position computed in one pass

**Predict:** For 16 positions and 8 fill-everything passes, predict which method makes the most position-updates and which makes the fewest.

**Worked example:**
- Passes, one at a time: 16
- Passes, fill everything: 8
- Passes, doubling levels: 5
- Position-updates, doubling levels: 31

A text of 16 positions takes 16 passes one at a time, 8 passes of fill-everything (128 position-updates) and 5 passes with doubling levels (31 position-updates). These are counts, not timings: real speed also depends on hardware, caching and overhead.

**Calculation:** Doubling levels 1, 2, 4, 8, 16: 5 passes, 31 position-updates. Fill everything: 8 x 16 = 128. One at a time: 16 passes. For the paper's 128-token text, 12 passes against 128 gives 10.7 times fewer.

**Takeaway:** A rough-first method can need far fewer passes than writing one piece at a time, and fewer position-updates than filling everything repeatedly, but counts are not timings.

**What happens:** At Positions in the text = 16, Passes of fill-everything = 8: One at a time takes 16 passes and 16 position-updates. Fill-everything takes 8 passes but 128 position-updates. Doubling levels of 1, 2, 4, 8 and 16 take 5 passes and 31 position-updates. At 128 positions the paper's real schedule is 12 passes, not the 8 that doubling would give.

**Why it matters:** Writing one token per pass makes a text take as many passes in a row as it has tokens. Building in levels changes that count, which is why the method is worth studying, and the count does not say how fast any real system runs.

**In brains and behavior:** No brain data are involved. The chapter does not claim that people think this way.

**In machines:** Left-to-right decoding takes one pass per token. The Stanford model writes a 128-token text in 12 passes, each pass choosing a whole level of codes, and the authors report it ran 21 times faster than a rival at 128 passes, by their own timing.

**Assumptions and limits:** Passes and position-updates would have equal costs, which they do not: actual speed and total computing also depend on architecture, caching, hardware and other overhead. The paper's levels do not double; its main Sudoku configuration begins with one, two and four codes and grows more slowly.

**Check:** How many passes and position-updates does a 64-position text take with doubling levels?

**Answer:** Levels of 1, 2, 4, 8, 16, 32 and 64 give 7 passes and 1 + 2 + 4 + 8 + 16 + 32 + 64 = 127 position-updates.

**Source:** A model that writes one piece at a time commits early; anchor `a-model-that-writes-one-piece-at-a-time-commits-early`. The chapter's invented 16-position text: 16 passes one at a time; 8 passes of fill-everything, 8 x 16 = 128 position-updates; 5 doubling levels, 31 position-updates. The other lengths and pass settings are this companion's variations. The reported 12 passes for a 128-token text and the authors' 21 times timing (against DUO at 128 passes, on one H100) are the paper's; the chapter says the doubling is only for easy counting.

## C18-D02: Can a later level undo an earlier one?

A target of 0.7316 is described in three levels, each choosing one entry from a list. What are the totals and leftovers, and what happens when level 1 overshoots?

At each level the closest entry to what is still missing is added to the running total. The leftover after level k is the target minus that total, so each new leftover is the old one minus the new correction. Lists with finer steps shrink the leftover. If the first pick overshoots and the later lists contain no negative entries, nothing can pull the total back.

$$
s_k=s_{k-1}+c_k,\qquad r_k=x-s_k
$$

**Symbols:** x: the target; k: the level number; c_k: the correction chosen at level k: the list entry nearest to what is still missing; s_k: the running total after level k, starting at s_0 = 0; r_k: the leftover (residual) after level k

**Predict:** For a target of 0.4216 with the chapter's lists, predict whether three levels reach it as closely as they reach 0.7316.

**Worked example:**
- Total after the levels used: 0.73
- Leftover (target minus total): 0.0016
- Last correction: 0.03
- Overshoot that later levels cannot undo: no

With the chapter's lists (nonnegative corrections only), 3 levels bring the total to 0.73 for a target of 0.7316, leaving 0.0016. Each level shrinks what the last one left over.

**Calculation:** s_k = s_(k-1) + c_k and r_k = x - s_k. level 1: c = 0.5, s = 0.5, r = 0.2316; level 2: c = 0.2, s = 0.7, r = 0.0316; level 3: c = 0.03, s = 0.73, r = 0.0016.

**Takeaway:** Stacked lists close in on a target when each level can correct what the last one missed, and an early overshoot is permanent when later levels can only add (the chapter's lists; allowing negative corrections is the companion's variation).

**What happens:** At Levels used = 3, Target = 0.7316, Lists allow negative corrections = 0: For 0.7316 the totals are 0.5, 0.7 and 0.73, and the leftover falls from 0.2316 to 0.0316 to 0.0016. Now switch to the target 0.4216: level 1 picks 0.5, overshooting, and since later lists only add, the total stays at 0.5 with leftover -0.0784. Allow negative corrections (the companion's own variation, not in the chapter) and the same target ends at 0.42.

**Why it matters:** A rough-first method has to commit to something at each level. Whether later levels may overturn an earlier one decides whether early mistakes can be repaired, which is the question the Sudoku result bears on.

**In machines:** In the paper, each level encodes the residual left by the earlier ones, and the finer levels are cut off at random in training so that early levels carry real information. The accounting here is a specification of that idea on one number; it is not how the model chooses its codes.

**Assumptions and limits:** Each level picks the entry nearest to the leftover. With the chapter's lists, which run from 0 to 1, a later level can only add, so an overshoot at level 1 stays; the chapter notes that whether later levels can overturn an earlier one is what the Sudoku result bears on. A correction chosen by this rule is not shown to be what any model does.

**Check:** For target 0.9 with the chapter's lists, what does level 1 pick, and what is the leftover after three levels?

**Answer:** Level 1 picks 1.0, the nearest of 0, 0.5 and 1, so the total is 1 and the leftover is -0.1. Later lists contain only nonnegative entries and pick 0, so the leftover stays at -0.1.

**Source:** Fix the leftover, one level at a time; anchor `fix-the-leftover-one-level-at-a-time`. The chapter's constructed example (not from the paper): target 0.7316, level 1 multiples of 0.5 from 0 to 1, level 2 multiples of 0.1, level 3 multiples of 0.01, giving corrections 0.5, 0.2, 0.03, totals 0.5, 0.7, 0.73 and leftovers 0.2316, 0.0316, 0.0016. The other two targets, and the option of lists that allow negative corrections, are this companion's variations.

## C18-D03: Which draft does minimum Bayes risk keep?

A model writes five one-line summaries of a vote. If we keep the one most like the others, is it the right one?

For each candidate, average its similarity to the other four. The kept candidate is the one with the highest average. In set A four of five drafts are right and they resemble each other, so the typical one is right and the odd one out scores lowest. In set B three drafts say the same wrong thing and so resemble each other most.

$$
i^{*}=\arg\max_{i}\ \frac{1}{n-1}\sum_{j\ne i}\operatorname{sim}(y_i,y_j),\qquad \hat y=y_{i^{*}}
$$

**Symbols:** y_1 ... y_n: the n candidate drafts (five here); sim(y_i, y_j): word overlap: shared words divided by the number of different words in either, ignoring capitals and periods; i*: the candidate with the largest average similarity to the others; y-hat: the candidate kept

**Predict:** In set B three of five candidates share a mistake. Predict whether MBR keeps a right candidate.

**Worked example:**
- Average similarity of the selected candidate: 0.512
- Candidate MBR keeps: 3
- Kept candidate is: right
- Candidates that carry the mistake: 1 of 5

Candidate 3 agrees with the others by 0.512 on average. MBR keeps candidate 3 (0.512), which is right. Only one candidate is wrong, and it scores lowest.

**Calculation:** Average for candidate 3 = (0.333 + 0.714 + 0.333 + 0.667) / 4 = 0.512. Similarity = shared words / different words in either, ignoring capitals and periods.

**Takeaway:** MBR keeps the most typical candidate, not the best one. When drafts tend to repeat a mistake, the typical draft carries it.

**What happens:** At Set of candidates = 2, Candidate to examine = 1: In set B, candidate 1 scores 0.462, the highest, and it carries the shared mistake 'close the old bridge'; the two right summaries score 0.352 and 0.237. In set A, candidate 3 scores 0.512 and is right, and the wrong candidate 4 scores lowest at 0.436.

**Why it matters:** Drawing several drafts is cheap when each draw is cheap, but choosing among them by agreement only rewards what the drafts share, true or not.

**In brains and behavior:** No brain data are involved.

**In machines:** In the paper, 16 candidates on XSum raised the summary score from 28.0 to 29.6, and 12 on translation raised the BLEU score from 22.6 to 25.2. The chapter says the paper's similarity measure is not stated, and a shared mistake can win by definition.

**Assumptions and limits:** Whether a candidate is right or wrong is set by the chapter, not computed. The method has no answer key and no outside judge. It keeps the candidate that agrees most, on average, with the others.

**Check:** In set A, candidate 3 scores 0.333, 0.714, 0.333 and 0.667 against candidates 1, 2, 4 and 5. What is its average?

**Answer:** (0.333 + 0.714 + 0.333 + 0.667) / 4 = 2.047/4 = 0.512.

**Source:** Drawing several and keeping the most typical; anchor `drawing-several-and-keeping-the-most-typical`. The chapter's two constructed sets of five one-line summaries of a bridge vote, with its word-overlap similarity. In set A candidate 4 is wrong; in set B candidates 1, 2 and 3 share the mistake 'close the old bridge'. The chapter's scores are reproduced: 0.512 for candidate 3 in set A, 0.436 for candidate 4, and 0.462 for candidate 1 in set B. The paper's own similarity measure for this step is not stated.

## C18-D04: How did the reported Sudoku results compare, and what would they imply per square?

The preprint reports the share of boards solved by three kinds of model. How much per-square accuracy would those shares imply if squares were independent?

If each of n empty squares were right independently with chance p, the whole board would be right with chance p to the n. Taking the nth root of a reported solve rate gives the per-square accuracy it would need. The figure is a scale for how quickly a single early error ruins a board; real squares depend on one another.

$$
P(\text{board right})=p^{\,n}\quad\Longrightarrow\quad p=\bigl(P(\text{board right})\bigr)^{1/n}
$$

**Symbols:** n: the number of empty squares (51 on the chapter's invented board with 30 given digits); p: the chance each empty square is right, if squares were independent; P(board right): the share of boards solved, counted only if all 81 squares are right

**Predict:** Predict which of the three methods needs the highest per-square accuracy to produce its hard-board result, if squares were independent.

**Worked example:**
- NCM solved (percent): 86.1
- Implied per-square accuracy, NCM: 0.9971
- Implied per-square accuracy, one at a time: 0.9137
- Empty squares assumed: 51

Reported on hard boards: NCM 86.1 percent, the best fill-everything rival 81.3, one at a time about 1. If squares were independent, NCM's rate needs about 99.71 percent per square. 51 empty squares is the chapter's invented hard board.

**Calculation:** Whole board = p^n, so p = (solved share)^(1/n). NCM: 0.861^(1/51) = 0.9971. Fill everything (FMLM+): 0.813^(1/51) = 0.9959. One at a time: 0.01^(1/51) = 0.9137. Squares constrain one another in real Sudoku, so these are a scale and not a measurement.

**Takeaway:** Whole-board success compounds over many squares. On an independent-squares scale, a per-square gap of about 0.1 point (0.9971 against 0.9959, NCM against FMLM+) turns 86.1 into 81.3 percent, and a gap of several points (0.9971 against 0.9137) separates 86.1 from about 1 percent.

**What happens:** At Board difficulty = 3, Empty squares on a board = 51: On hard boards NCM solved 86.1 percent, which would need about 99.7 percent per square across 51 squares, if squares were independent. The left-to-right model's about 1 percent would need only about 91.4 percent per square. On this scale, a per-square gap of about 0.1 point already separates NCM (0.9971) from FMLM+ (0.9959, from 81.3 percent) by about 5 points of boards.

**Why it matters:** A rough-first method that lets later levels correct earlier partial solutions is the authors' explanation for the Sudoku gap. The chapter says that explanation is a guess and that the paper reports no test isolating the cause.

**In brains and behavior:** No brain data are involved; the chapter says it does not claim that people solve Sudoku this way.

**In machines:** A left-to-right model commits to each square as it goes. The preprint's model keeps a rough picture of the whole board and sharpens it. The paper reports its Sudoku results and does not test the cause.

**Assumptions and limits:** A board counts as solved only if all 81 squares are right. The independence assumption is false for Sudoku, where a digit in one place limits digits in many others, so the implied accuracies are a scale and not a measurement. The 51 empty squares are the chapter's invented hard board (30 given digits). The chapter says easier boards give more digits and does not say how many digits the preprint's boards give, so for easy and medium boards, and for 41 or 61 squares, the empty-square setting is only a scale. The preprint reports one training seed and no error bars, and an outside reproduction reported 86.3 percent on 2,000 hard boards without retraining the model or reproducing the baselines.

**Check:** If squares were independent and 51 were empty, what per-square accuracy gives 86.1 percent of boards?

**Answer:** 0.861 raised to the power 1/51 is about 0.99707, so about 99.7 percent per square.

**Source:** On Sudoku, later levels corrected earlier ones; anchor `on-sudoku-later-levels-corrected-earlier-ones`. Reported results, from the chapter: Next-Concept Modeling (NCM) solved 99.5, 96.5 and 86.1 percent of easy, medium and hard boards in 12 passes. The best fill-everything rival (FMLM+) solved about 98 and 93 percent on easy and medium boards and 81.3 on hard (the chapter's opening gives the exact figure), and a left-to-right model about 14, 5 and 1. The rival numbers were copied from another group's paper. The independent-squares arithmetic is this companion's, not the paper's; the paper does not say how many boards were tested.

## C18-D05: What can a vote among drafts never repair?

Majority voting over final answers is MBR with the simplest similarity. How many voters does it take, and what stops it?

When errors are independent, the majority of many candidates is right almost surely if each is right more often than not. A shared mistake is different: the candidates all say the same wrong thing, so the vote reports it with confidence. The two cases add up in proportion to their chances, so the vote's success has a ceiling of one minus the shared-mistake chance.

$$
P(\text{majority right})=(1-c)\sum_{k=\lceil n/2\rceil}^{n}\binom{n}{k}a^{k}(1-a)^{n-k}
$$

**Symbols:** n: the number of candidate answers (odd, so a majority exists); a: the chance each candidate is right when errors are independent (0.7 here); c: the chance that all candidates repeat one shared mistake

**Predict:** At a shared-mistake chance of 0.1, predict whether 31 voters beat 0.95.

**Worked example:**
- Majority right: 0.753
- A single candidate is right: 0.63
- Ceiling however many vote: 0.9

Each candidate is right with chance 0.7 when the errors are independent; with chance 0.1 all of them repeat one mistake. 5 voters reach 0.753, and no number of voters can beat 0.9. This is the companion's constructed model, not a result from the paper.

**Calculation:** P(majority right) = (1 - 0.1) x sum from k = 3 to 5 of C(5, k) x 0.7^k x 0.3^(5 - k) = 0.753.

**Takeaway:** In this constructed model, more voters wash out independent errors but cannot remove a mistake all of them repeat, so a settled tally is stable and not necessarily true.

**What happens:** At Candidates voting = 31, Chance all candidates repeat one mistake = 0.1: With 31 voters the independent part is almost surely right, but the majority can be right only when there is no shared mistake, so it cannot pass 0.9. At shared-mistake chance 0.3 the ceiling is 0.7. These numbers come from the companion's constructed model (a = 0.7, c made up), not from the paper. More drafts help with scatter and cannot help with a repeated mistake.

**Why it matters:** A system that draws many answers from one model tends to treat agreement as evidence. How related the errors are decides whether the vote can improve on a single answer.

**In brains and behavior:** No brain data are involved.

**In machines:** Self-consistency votes over sampled final answers. In this toy the vote's ceiling is set by the chance of a shared mistake, a quantity the chapter says to ask about and does not measure.

**Assumptions and limits:** Two kinds of answer (right or wrong), independent errors when there is no shared mistake, and a shared mistake that makes every candidate wrong together. Real answers from one model are related in more complicated ways.

**Check:** With a = 0.7, c = 0 and n = 3, what is the chance the majority is right?

**Answer:** 3 x 0.7^2 x 0.3 + 0.7^3 = 0.441 + 0.343 = 0.784.

**Source:** Drawing several and keeping the most typical; anchor `drawing-several-and-keeping-the-most-typical`. The chapter states that majority voting over final answers is MBR with similarity 1 for the same answer and 0 for a different one, that a settled tally is stable and not necessarily true, and that several answers from one model are less independent than they look (Chapter 23's sunny-window thermometers). The two-answer model with a shared-mistake chance is this companion's construction, with made-up numbers (a = 0.7, c from 0 to 0.3); it is not from the paper or from the cited work on self-consistency.

## C18-D06: How large was the slowest-condition gap in Navon's timings?

People named either the big letter or the small letters of a figure. In which task did the other level slow them down?

Each task has three conditions, and the chapter gives their mean times. The gap compares the slowest with the mean of the other two. Naming small letters had a large gap and naming the big letter had a small one, the asymmetry Navon read as the big shape coming first. The sources do not label the conditions for the big-letter task, so its 10.5 ms is a spread, not a shown effect.

$$
\text{gap}=t_{\text{slowest}}-\tfrac{1}{2}\left(t_{\text{other 1}}+t_{\text{other 2}}\right)
$$

**Symbols:** t: mean reaction time in milliseconds for one condition; gap: how much longer the slowest condition took than the average of the other two (milliseconds)

**Predict:** Predict which task shows the larger gap, and whether it fits a global-first order of processing.

**Worked example:**
- Slowest condition (ms): 664
- Mean of the other two (ms): 577
- Gap (ms): 87

Naming the small letters took 664 ms in one condition and 573 and 581 ms in the other two, a gap of about 87 ms. The chapter ties the slow one to a big letter that differed from the small ones, but does not say which of 573 and 581 is which. Navon noted the big letter is also simply larger.

**Calculation:** Gap = slowest - mean of the other two = 664 - (581 + 573)/2 = 87 ms.

**Takeaway:** In these timings a different big letter slowed naming the small letters, and the small letters did not reliably slow naming the big one (the chapter's reading; Navon noted the big letter is also larger).

**What happens:** At Task = 1: Naming the small letters, the slowest condition took 664 ms against about 577 for the others (the chapter says about 575), a gap of about 87 ms. Naming the big letter, the three conditions ranged from 462 to 477 ms and the chapter reports no reliable slowing. Navon read that asymmetry as the big shape coming first, with the caveat that the big letter is also larger.

**Why it matters:** The studies in this chapter concern the order in which information becomes usable. The chapter says none tests a whole level of positions produced at once and then a finer level, so the link to the machine method is an analogy this book draws.

**In brains and behavior:** This is a reaction-time result in 14 undergraduates. In 1997 Oliva and Schyns showed that the task can flip which level dominates, and in 2021 Wiesmann and colleagues found the evidence did not support a default rough-first strategy.

**In machines:** The Stanford model's early levels are rough and its last level is exact. The chapter says the order in which people's information arrives is not that algorithm.

**Assumptions and limits:** The gap is a difference of means from 14 people and says nothing about reliability, which the original reports and this companion does not compute. Navon noted that the big letter is also simply larger, which could explain the result. The study shows which information was usable faster, not what any mind experienced.

**Check:** For the big-letter task, what is the slowest time minus the mean of the other two?

**Answer:** 477 - (462 + 471)/2 = 477 - 466.5 = 10.5 ms, small beside the 87 ms of the small-letter task.

**Source:** A rough whole shows up before fine detail, but not always; anchor `a-rough-whole-shows-up-before-fine-detail-but-not-always`. Reported result: Navon (1977), Experiment 3, 14 undergraduates, 40 ms masked display, as the chapter lists it: 664, 573 and 581 ms when naming the small letters; 462, 471 and 477 ms when naming the big letter. The chapter says 664 against about 575 otherwise when the big letter differed. The chapter's sources do not say which of the other numbers goes with which condition, so only the slowest-minus-the-others gap is computed here, and that is this companion's summary.
