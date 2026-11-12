# Chapter 13: What Matters to a Mind?

Give a machine a way to value outcomes, and see what each way builds in.

Ask what the outcomes are measured from (wealth, a reference point, a bodily state, or a person's comparisons), then choose the matching card: the logarithm when the same gain should matter less to someone who has more, the reference-point curve when framing as gain or loss may change the choice, the drive model when the body's needs change a goal's worth, the comparison rule when only a person can say which of two outcomes is better. Say which part of the rule does the work, what the person or designer chose, and what choices would show the rule is wrong for this case.

Practical question: A system must rank outcomes for different people or for one body in different states. Which value rule fits, what does it assume, and how would I find out whether it is wrong?

## C13-D01: Why does the same gain count for less when you already have more?

A gain of 1,000 ducats scores differently at different starting wealth, and so does a ticket that pays 0 or 20,000. How does the logarithm make the same ticket worth more to some holders?

Taking each small gain as worth less in proportion to what you hold adds up to a logarithm of the wealth ratio. The same 1,000 ducats is a doubling at 1,000 and a one percent rise at 100,000. For the ticket, averaging the scores of the two final wealth amounts and finding the certain amount that scores the same gives a worth that climbs toward the 10,000 average prize as wealth grows.

$$
y=b\ln\frac{x}{x_0}
$$

$$
\ln(w+p)=\tfrac12\ln w+\tfrac12\ln(w+20000)\ \Rightarrow\ p=\sqrt{w\,(w+20000)}-w
$$

**Symbols:** x_0, x: wealth before and after the gain, both above zero; y: the score of the gain, in arbitrary units (b = 1 here); w: the holder's wealth, not counting the ticket; p: the certain amount that scores the same as holding the ticket

**Predict:** At 1,000 ducats a 1,000 ducat gain scores 0.693. Predict how it scores at 100,000 ducats, and at what wealth the ticket is worth exactly 9,000, before moving the slider.

**Worked example:**
- Score of a 1,000 ducat gain: 0.693
- Wealth after the gain (ducats): 2000
- Worth of the ticket (ducats): 3583
- Worth against 9,000: below 9,000: selling at 9,000 is no mistake

Starting from 1,000 ducats, a 1,000 ducat gain scores 0.693. The ticket, which pays 0 or 20,000 with equal chances, is worth 3583 certain ducats to this holder, below 9,000: selling at 9,000 is no mistake.

**Calculation:** Gain score = ln((1,000 + 1,000)/1,000) = 0.693. Ticket worth p solves ln(w + p) = 0.5 ln(w) + 0.5 ln(w + 20,000), so p = sqrt(w (w + 20,000)) - w = 3583.

**Takeaway:** A rule that makes a gain matter less as wealth grows gives the same outcome different worth to different holders, with no change in the outcome itself.

**What happens:** At Starting wealth (ducats) = 100000: At 100,000 ducats the same gain scores 0.00995, about 70 times less than at 1,000. The ticket is worth about 9,540 there. It is worth exactly 9,000 at 40,500 ducats: holders with less would sell at 9,000, and holders with more would buy.

**Why it matters:** A program given outcomes and a curve will price one ticket differently for two people. The price comes from the chosen curve and the wealth supplied, not from the outcome, so both must be checked against the person.

**In brains and behavior:** Bernoulli argued that a poor holder could sell at 9,000 without error and a rich one would buy. It was an argument, and nothing here says a brain computes a logarithm.

**In machines:** A program supplied with a wealth figure and this curve computes the worth directly. The designer chose what it counts and how sharply the curve bends; the calculation does not show the curve fits a given person.

**Assumptions and limits:** A gain's worth is inversely proportional to existing wealth, which gives the logarithm. Both wealth amounts must be above zero. The score is not a measurement of anyone's happiness, and other curves predict the same direction.

**Check:** A holder has 1,000 ducats. What certain amount is the ticket worth under the rule, and is 9,000 above or below it?

**Answer:** p = sqrt(1,000 x 21,000) - 1,000 = 4,583 - 1,000, about 3,583 ducats. So 9,000 is far above its worth to this holder, and selling at 9,000 is no mistake.

**Source:** Wealth changes the value of a gain; anchor `wealth-changes-the-value-of-a-gain`. Book formula (Bernoulli's rule as the chapter presents it). The 1,000 and 100,000 ducat wealth figures are the chapter's constructed examples. The ticket worth p is this companion's computation from the chapter's rule, using the chapter's ticket (0 or 20,000, equal chances) and the 9,000 price; the chapter states neither the formula for p nor the 40,500 ducat figure, and Bernoulli's argument was not a recorded sale.

## C13-D02: Which part of the model makes a loss frame choose the gamble?

Two groups face the same final amounts but one hears gains and the other losses. A curve measured from a reference point can reproduce the majority choices, and the question is which of its features does the work.

Measured from the gift, the extra 500 is a gain for one group and a loss for the other. Square roots bend both sides, so a sure thing beats a gamble among gains and a gamble beats a sure thing among losses. Making losses count more multiplies every loss score by the same number, so it does not reorder two loss options, but it makes an even chance of gaining or losing the same amount look bad.

$$
v(x)=\begin{cases}\sqrt{x}, & x\ge 0,\\ -\lambda\sqrt{-x}, & x<0.\end{cases}
$$

**Symbols:** x: the change from the reference point, in pounds (positive for a gain, negative for a loss); v(x): the score, in arbitrary units; lambda: the loss weight: 2 in the chapter's curve, and 1 means no extra weight on losses

**Predict:** Set the loss weight to 1 in the loss frame. Predict whether the model still prefers the gamble, then try the even bet and ask what the weight does there.

**Worked example:**
- Score of the certain option: 22.4
- Score of the gamble: 15.8
- Model picks: the certain option
- Majority in the study: certain gain (84 percent of 70 chose it)

With loss weight 2, the certain option scores 22.4 and the gamble 15.8, so the model picks the certain option. The curve is the chapter's constructed illustration, not fitted to the respondents.

**Calculation:** sqrt(500) versus half of sqrt(1,000): 22.4 against 15.8. Scores are averaged with the stated chances, with no probability weighting.

**Takeaway:** The reference point and the curve's bend produce the gain and loss framing reversal; the loss weight does its own, separate work in a bet that mixes gains and losses.

**What happens:** At Problem = loss frame, Loss weight = 1: With no extra weight on losses the certain loss still scores about -22.4 against -15.8 for the gamble, so the gamble still wins. Raising the weight scales both loss scores by the same positive number and cannot reverse their order. The weight matters only in the even bet.

**Why it matters:** A machine that records only final amounts has already lost the framing. Giving it a reference point restores the distinction, and checking which feature produces which effect keeps a designer from crediting the wrong one.

**In brains and behavior:** The 1979 study measured hypothetical choices of different groups. It did not identify neurons computing this curve, and a program with no variable for fear or relief still produces the gain and loss pattern.

**In machines:** The machine implements the arithmetic exactly. That shows a limited computational capability, not that emotion is irrelevant to people or that the machine experiences the scores.

**Assumptions and limits:** A reference point (the gift) and a curve that bends the same way on both sides. The study measured stated choices of different people, not neurons or one person reversing. Matching the direction of the majority does not predict the percentages or explain how people choose their reference points.

**Check:** In the even bet, at what loss weight does the model score the gamble at exactly zero, the same as the certain change of zero?

**Answer:** The gamble scores half of sqrt(500) minus half of the weight times sqrt(500), which is zero only when the weight is 1. Any larger weight scores it below zero, so the certain zero is preferred.

**Source:** Measure the change; anchor `measure-the-change`. The curve is the chapter's own constructed illustration, chosen for easy arithmetic and not estimated from the respondents. The choice problems are the 1979 hypothetical questions: 70 respondents with a gift of 1,000 pounds (84 percent chose the certain gain) and 68 with a gift of 2,000 (31 percent chose the certain loss). The even bet is the chapter's own illustration and was not put to respondents. Scores average outcomes by their chances, with no probability weighting.

## C13-D03: How can the same food be worth something, nothing, or less than nothing?

A model body scores an outcome by how far it moves the body toward its set points. What does three units of food score when the body is hungry, full, or thirsty?

Drive adds up how far each need is from its set point. An outcome is scored by how much it shrinks that total. Food that fills a gap shrinks it, food added to a full body opens a new gap and grows it, and food does nothing to a gap in water. So reward depends on what the body lacks now.

$$
D(H_t)=\Big(\sum_{i=1}^{N}|h_i^*-h_{i,t}|^{n}\Big)^{1/m},\qquad r(H_t,K_t)=D(H_t)-D(H_t+K_t)
$$

**Symbols:** h_i^*, h_i: set point and current level of need i (food and water here, set points 10); D: drive: the combined gap from the set points; n, m: positive numbers that set how gaps combine; n = m = 1 is the chapter's illustration; K_t: the change an outcome causes (3 units of food, or of water); r: reward: drive before minus drive after

**Predict:** Predict what the model scores for 3 units of food at food 10 and water 10, and whether water scores higher when water is at 4.

**Worked example:**
- Drive before: 6
- Reward of 3 units of food: 3
- Reward of 3 units of water: -3
- Higher reward: food

At food 4 and water 10 the model body's drive is 6. Three units of food score 3 and three units of water -3, so food scores higher. This is a constructed model, not a fit to any animal.

**Calculation:** Set points 10 and 10; n = m = 1, drive is the sum of the gaps. Drive now = 6. After food: (7, 10) gives 3, reward 6 - 3 = 3. After water: (4, 13) gives 9, reward -3.

**Takeaway:** Once the score depends on the body's state, the same outcome can reward, do nothing, or penalize, because value is the change in drive and not a fixed number attached to food.

**What happens:** At Current food level = 10, Current water level = 10, Drive form (1: n = m = 1; 2: n = 3, m = 2) = 1: A model body at both set points scores 3 units of food at -3 (drive goes from 0 to 3). A hungry one (food 4, water 10) scores it at +3. The same outcome has opposite scores when the starting state differs.

**Why it matters:** A machine that gives food a fixed score cannot represent a changing need through that score alone. Supplying a state description and letting the score depend on it is one way to do so.

**In brains and behavior:** Rats that had learned a Y-maze with food on one side and water on the other tended to choose the side that fit their test need. The only source is a 1940 conference abstract with no counts, and the model paper did not test that maze, so this is a resemblance in direction, not a fit.

**In machines:** The equations are a specification of a designed system: given levels and set points they return a score. A designed system that scores departures from a target does not establish that a brain uses this formula.

**Assumptions and limits:** Two needs, a fixed set point for each, and a reward defined as reduction in drive. Overshooting a set point can give a negative score. The model specifies internal levels; it does not say how a body senses or regulates its own state.

**Check:** A model body has food 10 and water 4, set points 10, with n = m = 1. What do 3 units of food and 3 units of water score?

**Answer:** Drive now is 6. Food takes the body to (13, 4): gaps 3 and 6, drive 9, reward 6 - 9 = -3. Water takes it to (10, 7): drive 3, reward +3. Water scores higher.

**Source:** Need changes the goal; anchor `need-changes-the-goal`. Book formula (the Keramati and Gutkin homeostatic reward as the chapter presents it). The set points of 10 and the 3-unit outcome follow the chapter's constructed example, whose hungry case (food 4, water 10) gives drive 6 to 3 and reward 3, and whose full case gives drive 0 to 3 and reward -3. The second drive form (n = 3, m = 2) is the paper's regime n > m > 1, evaluated here by this companion; the chapter's n = m = 1 relaxes that restriction.

## C13-D04: How do two scores become a predicted preference?

A model gives clip A a score of 2 and clip B a score of 1. What chance does it give that a person prefers A, and what happens if every score shifts?

Raising both scores by the same number multiplies the top and bottom of the fraction by the same factor, so it cancels. A gap of 1 gives 73 percent for the higher option, a gap of 3 gives 95 percent, and no gap gives one half. Random responses mix in a coin flip and keep the chance away from 0 and 1.

$$
P(a\succ b)=\frac{e^{r_a}}{e^{r_a}+e^{r_b}}
$$

**Symbols:** r_a, r_b: the model's scores for options a and b; e: the constant 2.718...; P(a > b): the predicted chance that a person prefers a

**Predict:** Predict the chance A is preferred when the scores are 2 and 1, then predict it when both scores are 12 and 11.

**Worked example:**
- Score gap (A minus B): 1
- Chance A is preferred: 0.731
- Chance B is preferred: 0.269
- Same with 5 added to both scores: 0.731

Scores 2 and 1 give a gap of 1 and a predicted chance of 0.731 that A is preferred. Adding the same number to both scores leaves the chance at 0.731, because only the gap matters.

**Calculation:** Without random responses: e^2 / (e^2 + e^1) = 0.731. With a share 0 of fair-coin responses: (1 - 0) x 0.731 + 0 x 0.5 = 0.731.

**Takeaway:** Only the gap between two scores sets the predicted preference, so scores have no fixed zero, and equal scores give exactly one half.

**What happens:** At Score of A = 2, Score of B = 1, Share of random responses = 0: The chance is e^2/(e^2 + e^1), about 0.731, and the right panel shows the same chance whenever the gap is 1, whatever the zero. Turning on 10 percent random responses pulls it toward 0.5, to about 0.708.

**Why it matters:** A reward learned from comparisons is determined only up to a shift. Knowing that tells a designer what the numbers can and cannot mean.

**In brains and behavior:** A person who is asked which of two clips is better produces an answer. The rule predicts the pattern of answers, not how the person's brain reaches them.

**In machines:** A reward model uses scores for clips and this rule to score its own fit to the comparisons it receives; the agent is then trained against the learned scores.

**Assumptions and limits:** The model's scores summarize which option a person tends to choose. The rule is a model of answers, not an established account of how the brain makes them.

**Check:** Scores of 3 and 0. What chance does the rule give that A is preferred, and what is it with 10 percent random responses?

**Answer:** e^3/(e^3 + 1) = 20.09/21.09, about 0.953. With random responses it is 0.9 x 0.953 + 0.05, about 0.907.

**Source:** A machine can learn from human comparisons; anchor `a-machine-can-learn-from-human-comparisons`. Book formula with the chapter's constructed scores (2 and 1, not scores of any hopper clip). The 10 percent random-response option follows the chapter's remark that the training method allowed a 10 percent chance of a random response; reading that as a fair coin, so P is 0.9 times the rule plus 0.05, is this companion's, not the chapter's formula.

## C13-D05: How much comparing does it take to recover a score gap?

Learning runs the other way from the preference rule: given a person's comparisons, the system adjusts scores to account for them. How close does a score gap get as comparisons accumulate?

The share of comparisons that favor A is the data, and the gap that best explains that share is the log of its odds. Few comparisons leave the share noisy, and if all go one way the best gap is infinite, so the estimate is undefined. More comparisons narrow the spread, and larger gaps are easier to see because the shares are further from one half.

$$
\hat g=\ln\frac{f}{1-f},\qquad \text{typical error}\approx\frac{1}{\sqrt{n\,p(1-p)}}
$$

**Symbols:** g-hat: the estimated score gap between two options; f: the share of the n comparisons in which the first option was preferred; p: the true chance the first option is preferred, from the rule in the previous demonstration; n: the number of comparisons

**Predict:** Predict whether 10 comparisons recover a gap of 1 as well as 100 do, and how much 900 improve on 100.

**Worked example:**
- Share preferring A (this run): 0.65
- Estimated score gap: 0.619
- True score gap: 1
- Typical error (formula): 0.226

After 100 simulated comparisons the preferred answer won 65, giving an estimated gap of 0.619 against a true gap of 1. The formula puts the typical error at 0.226; this is a simulation with a made-up true gap, not a measurement.

**Calculation:** Estimated gap = ln(f / (1 - f)) with f = 65/100 = 0.65. Typical error = 1/sqrt(n p (1 - p)) with p = 0.731, n = 100: 0.226. Repeating 2000 runs gave an rms error of 0.23.

**Takeaway:** A score is learned from comparisons by raising the likelihood of the answers received, and the error shrinks slowly, in proportion to one over the square root of the number of comparisons.

**What happens:** At True score gap = 1, Comparisons = 100: With 100 comparisons and a true gap of 1 the typical error is about 0.23. Nine times the comparisons cut it by a factor of 3, so 900 comparisons leave an error of about 0.075.

**Why it matters:** A person can judge examples without assigning every clip a number, and the machine can use those judgments. But how many are needed depends on how large the difference is, and the learned scores say nothing beyond the person's answers.

**In brains and behavior:** A person supplies the comparisons. The simulation has no person, only a coin with a chosen bias, so it says nothing about how people judge.

**In machines:** The estimate is a computation on the comparisons received. A system that matches a person's comparisons has learned a score for their answers, which does not show that it understands or experiences the goal.

**Assumptions and limits:** One pair of options, independent comparisons, a fixed true gap and no random responses or mislabeling. A learned score can fail on behavior unlike what the person evaluated, which this demonstration does not test.

**Check:** The true gap is 2, so A is preferred with chance 0.881. About how large is the typical error after 100 comparisons?

**Answer:** 1/sqrt(100 x 0.881 x 0.119) = 1/sqrt(10.5), about 0.31.

**Source:** A machine can learn from human comparisons; anchor `a-machine-can-learn-from-human-comparisons`. A seeded simulation of this companion's, with a made-up true gap (0.5, 1 or 2) and the rule of the previous demonstration. The estimate is the maximum likelihood gap for one pair, and the error formula is the standard large-sample one; neither is stated in the chapter. It is a simulation, not a measurement, and not the hopper study, which reported that 900 queries in under an hour taught a backflip by training a reward model with a neural network on clips.
