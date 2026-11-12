# Chapter 20: Acting Through a Body

Plan a move from a prediction, correct only what matters, and see what a delay or a changed world does to the plan.

Ask for the delay, the gain, and what the predicted feedback is. For a plan from a remembered target, subtract the estimated last move. For a gap between prediction and sensor, say that the residual alone cannot name its cause. For late feedback, compare the plain loop with a loop that models the delay, and for a changed world use an error-driven update and check the aftereffect. Quote counts with their exact range.

Practical question: My controller corrects strongly from a sensor that reports 200 ms late and it swings. What does a model of the delay change, and what would a leftover gap between prediction and sensor not tell me?

## C20-D01: How does a mind aim the second jump before the first has been seen to land?

If a second eye jump is planned as the remembered target minus the estimated first jump, how far does it miss when part of the first-jump signal is lost?

The eye starts at the origin and makes a first jump. The target for the second jump was seen before the move, so it is remembered relative to the start. The jump still needed is that target minus where the eye now is. If the estimate of the first jump is too small, the subtraction removes too little, and the planned jump is too large by the missing part.

$$
m_2=r_2-\hat s_1,\qquad \hat s_1=(1-d)\,s_1,\qquad \text{miss}=d\,s_1
$$

**Symbols:** m_2: the planned second jump, a pair of numbers (across, up); r_2: the remembered second target, measured from where the eye started; s_1 and its estimate: the first jump actually made, and the brain's estimate of it; d: the share of the first-jump signal lost, from 0 (none) to 1 (zero is substituted); miss: how far the end point is from the target (the companion's step: with d lost, the plan overshoots by d times the first jump)

**Predict:** Before moving anything: if the eye jumped 10 units and the signal were totally lost, where would the second jump be aimed, and what is the miss?

**Worked example:**
- Planned second jump (across, up): (1.9, 8)
- Needed second jump (across, up): (0, 8)
- Miss of the end point (units): 1.9
- Share of the total-loss miss: 0.19

A first jump of 10 units with 0.19 of its signal lost makes the planned second jump (1.9, 8) instead of the needed (0, 8). The end point misses by 1.9 units, 0.19 of the 10-unit miss that total loss would cause.

**Calculation:** Estimate = (1 - 0.19) x 10 = 8.1. Plan = target - estimate = (10 - 8.1, 8 - 0) = (1.9, 8). Needed = (10 - 10, 8) = (0, 8). Miss = 0.19 x 10 = 1.9.

**Takeaway:** A missing first-jump estimate shows up as a second jump that misses by exactly the lost share times the first jump.

**What happens:** At Share of the first-jump signal lost = 1.0, First jump (units across) = 10: With the whole signal lost, the first-jump estimate is zero, so the plan is the full remembered target (10, 8) as if the eye had not moved. The end point lands 10 units too far across. The reported partial shortfalls, 10 and 19 percent, correspond to 1 and 1.9 of those units.

**Why it matters:** A controller that plans one move from the last has to know how far the last move went. The subtraction makes the dependence visible, and the shift measures how much of the estimate is being used.

**In brains and behavior:** In two monkeys, a drug in a thalamic relay shifted second jumps in the direction that losing the signal predicts, while single jumps to a lone target were barely affected. The subtraction is the book's model of what the signal does, not a recorded calculation.

**In machines:** A saccade planner or robot arm can compute the subtraction exactly from its own motor command, a specification and not a model of a monkey.

**Assumptions and limits:** The target stays still and is remembered exactly. The first jump is estimated as a fixed share of itself. The relay in the study was partly inactivated, never shown to be off, and other pathways may carry the signal.

**Check:** The first jump is 15 units across and half the signal is lost. What is the planned second jump, and how far does it miss?

**Answer:** The estimate is 7.5, so the plan is (10 - 7.5, 8) = (2.5, 8) against the needed (10 - 15, 8) = (-5, 8). The end point misses by 0.5 x 15 = 7.5 units.

**Source:** Where a prediction could come from: a relay and the cerebellum; anchor `where-a-prediction-could-come-from-a-relay-and-the-cerebellum`. The subtraction m2 = r2 - s1-hat is the chapter's equation (notation added by the book). The target (10, 8), the jump sizes and the units are made up. The chapter reports the shortfall as a share: 19 percent in 11 clear cases and about 10 percent across all 22, which the authors measured as the observed shift divided by the largest shift a total loss would cause; here that share is the slider d.

## C20-D02: If sensed feedback differs from the prediction, was it a push or a bad prediction?

A body sends a command, predicts the feedback, and senses something else. How much of that gap is an outside disturbance?

The residual is a single number, but it is the sum of two unknowns, an outside push and a prediction error. Any pair adding to the residual fits. Even a residual of zero can hide a push exactly cancelled by an opposite prediction error.

$$
e=s_{\mathrm{obs}}-f(c)=w+\left[\rho(a)-f(c)\right]
$$

**Symbols:** e: the residual, sensed feedback minus predicted feedback; f(c): the predicted feedback for a copy of the command c; rho(a): the sensory effect of the movement a actually made; w: an outside disturbance added to the feedback; rho(a) - f(c): the prediction error, how far the prediction missed the movement's own effect

**Predict:** Observed 8, predicted 6. A friend says the residual of 2 proves something pushed the arm. Predict whether that is right before moving the sliders.

**Worked example:**
- Observed feedback: 8
- Predicted feedback: 6
- Residual (observed minus predicted): 2
- Prediction error left over: 0

Observed 8 against predicted 6 leaves a residual of 2. With an outside push of 2, the prediction must be off by 0. The same residual comes from an outside push with a perfect prediction, from no push with a prediction error, or any mix.

**Calculation:** e = 8 - 6 = 2. e = w + [rho(a) - f(c)], so 2 = 2 + 0.

**Takeaway:** One residual fits a whole line of causes, so a gap alone cannot say whether the world or the prediction was off.

**What happens:** At Outside push w = 0, Residual (observed minus predicted) = 2: With no push at all, the residual of 2 is entirely a prediction error: the model expected 6 and the movement's own effect was 8. The point sits at the top left of the line, and moving along the line changes the cause but not the residual.

**Why it matters:** A controller that reacts to a residual has to know whether to correct the world or its own model. The residual by itself cannot tell, so extra information is needed.

**In brains and behavior:** The additive split is a constructed explanation, not a measured equation for a circuit; the chapter reports no brain test of it.

**In machines:** A robot comparing a command's predicted sensor value with the actual reading faces the same ambiguity. Logging a second sensor or a repeated trial is the extra information.

**Assumptions and limits:** Feedback is the movement's effect plus an additive outside push. Nothing else enters. The predicted feedback is fixed at 6.

**Check:** The observed feedback is 10 and the predicted is 6. If the outside push is 1, what is the prediction error?

**Answer:** The residual is 10 - 6 = 4, so the prediction error is 4 - 1 = 3.

**Source:** Where a prediction could come from: a relay and the cerebellum; anchor `where-a-prediction-could-come-from-a-relay-and-the-cerebellum`. The decomposition is the chapter's equation, called there a constructed explanation and not a measured equation for a brain circuit. The values observed 8 and predicted 6 (residual 2) are the chapter's example; the other residuals are chosen to show a zero and a larger gap.

## C20-D03: Why does strong correction from late news make a controller swing?

If the report on position arrives 0.2 s late, how strongly can a plain feedback loop correct before it swings, and what does a model of the delay change?

The plain loop pushes toward the target with a strength proportional to how far the delayed report says it is. While the report is old, the controller keeps pushing after the target is passed, and a strong push turns the overshoot into a growing swing. The Smith loop adds what the plant has moved since the report: x(t) minus x(t minus the modelled delay). If the model is right, the loop sees the present position.

$$
x'(t)=g\,\bigl(1-x(t-\delta)\bigr)\ \text{(plain)},\qquad g\,\delta<\tfrac{\pi}{2}\ \text{to settle}
$$

**Symbols:** x: position of a simple plant whose speed equals the command; g: correction strength, the gain, per second; delta: the delay of the report, 0.2 s here; Smith loop: feedback = late report + x(t) - x(t - modelled delay); the plant model is taken as exact

**Predict:** The plain loop stops settling above a gain of about 7.85 per second. Predict whether the delay-modelling loop will tolerate a gain of 10 when its delay model is exactly right.

**Worked example:**
- Plain loop: does not settle
- Plain overshoot (percent): undefined (does not settle)
- Smith loop: settles
- Smith overshoot (percent): 0

At gain 10 per second with a 0.2 s delay, the plain loop does not settle and the Smith loop with its delay model 0 ms off settles. The plain loop's limit is gain pi/(2 x 0.2) = 7.85.

**Calculation:** Plant x' = u, report x(t - 0.2). Plain: u = gain x (1 - x(t - 0.2)), which settles only when gain x delay is below pi/2, so gain below 7.85. Smith with the right delay model: the loop sees x(t) itself, so x(t) = 1 - exp(-gain x t), settling for every gain. Euler steps of 0.005 s; a loop settles if the last 2 s of a 12 s run stay within 0.01 of the target. That test is stricter than the exact bound: a swing that decays slowly, as the plain loop's does for gains near 7, is not settled by 12 s, so the figure's plain curve crosses the 0.01 line near gain 7 and not at 7.85; such a loop is labeled 'settles slowly' if a 60 s run settles. In this plant a delay model 100 ms too long settles up to about gain 15, and one 100 ms too short settles over the whole slider range, unlike the 1993 simulation as the chapter reports it, which became unstable with a model 100 ms wrong.

**Takeaway:** A model of the delay allows strong correction in this constructed plant and tolerates a modest delay-model error here, but a large enough gain still fails when the delay model is 100 ms too long. The chapter's source simulation was less forgiving: a delay model wrong by 100 ms made it unstable.

**What happens:** At Correction strength (gain per second) = 10, Error in the delay model (ms) = 0: At gain 10 the plain loop swings out of range, while the loop that models the delay correctly rises to the target without overshoot. Now move the delay-model error to plus 100 ms: at gain 14 the swing is slow to die away, and at gain 20 the delay-modelling loop fails too (the limit with this error is roughly 15 per second). The chapter says a delay model wrong by 100 ms made the 1993 simulation unstable; this constructed plant tolerates that error at lower gains, so it does not reproduce that result.

**Why it matters:** Strong correction from old data is the cause of the swing. A controller that holds a prediction of the present can act on it and use the late report as a check, which is what the cerebellum proposal says might happen.

**In brains and behavior:** The 1993 paper proposed, with a simulation and no experiment, that the cerebellum holds a forward model and a delay model. A 2007 magnetic-pulse experiment fits a hand estimate 138 ms old, but nothing here tests a cerebellum.

**In machines:** A Smith predictor is an engineering controller for processes with long delays. It is a specification, not a model of any brain.

**Assumptions and limits:** A pure integrator plant, no noise, an exact plant model, and a delay model that is exactly right or off by 100 ms. The plain loop settles only when gain times delay is below pi/2. Real delays and plants differ. In this plant a delay model that is 100 ms too long still settles at gains up to about 15 per second, and one 100 ms too short settles over the whole slider range. The 1993 simulation, as the chapter reports it, became unstable with a delay model 100 ms wrong; this constructed integrator is more forgiving, so its tolerance is not a result about that paper or about any brain.

**Check:** The report is 0.2 s late. What is the plain loop's largest gain that still settles?

**Answer:** Gain times delay must be below pi/2, so the gain must be below pi/(2 x 0.2) = 7.85 per second.

**Source:** Where a prediction could come from: a relay and the cerebellum; anchor `where-a-prediction-could-come-from-a-relay-and-the-cerebellum`. The shower story and the Smith predictor idea are the chapter's. The plant, the 0.2 s delay (the low end of the chapter's 200 to 250 ms upper estimate for sight-guided reaches), the gains and the simulation are constructed here and are not the 1993 paper's simulation, and they give a different answer for a 100 ms delay-model error: the chapter reports that error made the 1993 simulation unstable, while here it is tolerated up to about gain 15 (model too long) or at every slider gain (model too short). Euler steps of 5 ms.

## C20-D04: Why does a skilled hand correct some errors and let others go?

If a controller pays for effort and for missing the task, how much does it correct a direction that hardly matters?

Each step, a push moves the state. The controller can undo a share K of the error at an effort cost. If the error does not affect the task, the weight q is small, K is small, and the error is allowed to drift to a larger long-run spread. With zero weight there is no correction and the spread grows without a long-run limit.

$$
P=\frac{q+\sqrt{q^{2}+4qr}}{2},\qquad K=\frac{P}{P+r},\qquad \operatorname{Var}=\frac{\sigma^{2}}{K(2-K)}
$$

**Symbols:** q: weight on missing the task in one direction; r: cost of the correcting effort; P: the steady-state cost-to-go weight of the standard scalar solution; K: the share of the error corrected each step; Var: long-run variance, with a push of variance sigma^2 = 1 added each step

**Predict:** If a direction carries no weight at all, how large is its long-run spread? And does giving it the same weight as the other direction equalize the two?

**Worked example:**
- Gain, direction that matters: 0.618
- Gain, direction that matters little: 0.27
- Spread, direction that matters: 1.17
- Spread ratio (matters little / matters): 1.83

A direction weighted 0.1 gets gain 0.27 and spread 2.14, against gain 0.618 and spread 1.17 for the direction that matters. The ratio is 1.83; at equal weights it is 1. The model is constructed, not fitted to the study.

**Calculation:** P = (q + sqrt(q^2 + 4 q r))/2 and gain K = P/(P + r). For q = 1, r = 1: K = 0.618. For q = 0.1: K = 0.27. Spread = 1/(K(2 - K)) = 1.17 and 2.14. At some settings the ratio lands near the chapter's 0.26/0.14 = 1.86 only by coincidence; the weights are made up and nothing is fitted.

**Takeaway:** A controller that charges for effort corrects the direction that matters hard and the other loosely; at equal weights the two are equal.

**What happens:** At Weight on the direction that matters little = 0.1, Effort cost r = 1.0: At weight 0.1 against 1, the spread in the direction that matters little is about 1.83 times the other, near 1.86, the ratio of the chapter's two five-target variances, 0.26 over 0.14. The nearness of 1.83 to 1.86 is a coincidence of a tidy number, not a fit: the weights are made up and the study's spreads are not what this model computes. Set the weight to 1 and the two spreads are equal, the analogue of the 21-target condition where every point on the path was a target.

**Why it matters:** Perfect correction everywhere is costly. A controller that corrects only what interferes with the task spends effort where it pays, so a looser hand between targets is a prediction, not a defect.

**In brains and behavior:** Todorov and Jordan present this as a theory with simulations and experiments. It names no circuit and does not explain how skill is acquired.

**In machines:** An optimal feedback controller is a specification: choose the cost, and the gain follows. A robot arm can be built to correct only what the task needs.

**Assumptions and limits:** A one-number state, a push of fixed size each step, a quadratic cost and a controller that knows the state. Real reaches have many joints, delayed noisy senses and no single weight. In the study, the 21-target comparison no longer detected a significant difference. The study's spreads are of hand position at points along a reach, while the model's ratio compares two long-run directions of a one-number state, so the two ratios are different kinds of quantity.

**Check:** At effort cost 1 and weight 1, K = 0.618. What long-run variance does that give?

**Answer:** Var = 1/(0.618 x (2 - 0.618)) = 1/(0.618 x 1.382) = 1.17.

**Source:** Which errors to fix, and how a body model is repaired; anchor `which-errors-to-fix-and-how-a-body-model-is-repaired`. The principle (correct deviations only when they interfere with the task) and the spreads 0.14 and 0.26 square centimeters with five targets, and 0.18 and 0.18 with 21, are quoted from the chapter's account of Todorov and Jordan (2002). The scalar model, its weights and its noise are constructed here; nothing is fitted to the study, and the ratio 0.26/0.14 = 1.86 of the chapter's two five-target variances is drawn only as a reference line.

## C20-D05: Why do reaches bend the other way when a force is switched off?

If a controller builds a model of a push from its errors, how closely does the aftereffect mirror the first miss, and how does that depend on practice?

Each reach corrects the estimate by a share of the miss. With the field on, the miss shrinks as the estimate approaches the push. When the field is removed, the estimate is still near the old push, so the arm compensates for a push that is no longer there, and the miss has the opposite sign.

$$
b_{n+1}=b_n+\eta\,(B-b_n),\qquad b_n=B\bigl(1-(1-\eta)^{n}\bigr),\qquad \text{aftereffect}=-b_N
$$

**Symbols:** B: the strength of the push of the world, taken as 1; b_n: the controller's estimate of the push after n reaches; eta: learning rate, the share of the error corrected in the estimate each reach; N: the number of practice reaches with the field on

**Predict:** After practice with a learning rate of 0.1, what is the first miss when the field is switched off, compared with the very first miss?

**Worked example:**
- First miss (field on): 1
- First reach after the field goes off: -0.985
- Aftereffect as a share of the first miss: 0.985
- Miss left on the last practice reach: 0.0164

With learning rate 0.1 and 40 practice reaches, the model's field estimate reaches 0.985 of the true field. The first reach after the field is removed misses by 0.985, on the opposite side from the first miss of 1. This is a constructed update rule, not the paper's model.

**Calculation:** Estimate after n reaches = 1 - (1 - 0.1)^n. After 40: 1 - 0.9^40 = 0.985. Miss with the field on = 1 - estimate; first miss with it off = 0 - estimate = -0.985.

**Takeaway:** The better the estimate of the push, the more nearly the aftereffect mirrors the first miss; the mirror is a sign of what was learned.

**What happens:** At Learning rate = 0.1, Practice reaches with the field on = 40: After 40 reaches at learning rate 0.1 the estimate has reached 98.5 percent of the push, so the first reach with the field off misses by almost exactly the size of the first miss, on the opposite side. With 5 reaches the mirror is only 41 percent.

**Why it matters:** A controller that adapts has built a model, and a model keeps predicting a push that is gone. The aftereffect is therefore read as a sign of the model, inferred from behavior.

**In brains and behavior:** The authors read the aftereffect as a sign that the controller gradually built a model of the field. That is an inference from behavior, not a recorded model.

**In machines:** A robot arm can run the same error-driven update on a force estimate; the update rule is a specification.

**Assumptions and limits:** The miss is proportional to the gap between the true push and the estimate, the estimate is updated from the last miss only, and the field is one steady push. Real reaches have trial-to-trial noise and several forces.

**Check:** At learning rate 0.2 and 10 practice reaches, how close is the estimate to the push?

**Answer:** 1 - 0.8^10 = 1 - 0.107 = 0.893, so the aftereffect is 89 percent of the first miss.

**Source:** Which errors to fix, and how a body model is repaired; anchor `which-errors-to-fix-and-how-a-body-model-is-repaired`. The sequence of events (early distortion, practice back to near free-space paths, aftereffects that were approximately mirror images) is the chapter's account of Shadmehr and Mussa-Ivaldi (1994), which it draws as a schematic. The update rule, the learning rates and the trial counts are constructed here; nothing is a measurement or the paper's model.

## C20-D06: What can 2 successes in 10 trials tell us?

If a robot hand completed a task in 2 of 10 real trials, how well does that pin down its success rate, and what would 0 of 10 tell?

For each possible true rate, the chance of seeing a given count is a binomial probability. A rate is ruled out when it would make the count of 2 or fewer, or 2 or more, rare. The rates that survive form an interval. The exact interval is wide because ten trials contain little information.

$$
P(X\le k\mid p)=\sum_{i=0}^{k}\binom{n}{i}p^{i}(1-p)^{n-i}
$$

**Symbols:** n: number of trials, 10; k: number of successes; p: the underlying success rate, unknown; range: the rates not ruled out at 95 percent, found by exact search

**Predict:** With 0 successes in 10 trials, predict whether a true success rate of 25 percent is ruled out.

**Worked example:**
- Share of trials: 0.2
- Low end of the 95 percent range: 0.0252
- High end of the 95 percent range: 0.556
- Width of the range: 0.531

2 successes in 10 trials is a share of 0.2, but rates from 0.0252 to 0.556 remain plausible at 95 percent. The range is 0.531 wide, so ten trials cannot separate nearby rates.

**Calculation:** Exact (Clopper-Pearson) range: the lowest rate that gives 2 or more successes with chance at least 0.025 is 0.0252; the highest rate that gives 2 or fewer with chance at least 0.025 is 0.556.

**Takeaway:** Ten trials leave a wide range of rates plausible, so the two reported counts are consistent with a wide range of true rates, including some in common.

**What happens:** At Successes in 10 trials = 2: Two of ten gives a share of 0.2, but rates from about 0.025 to 0.556 remain plausible at 95 percent. Move to 0 of 10: the high end falls to about 0.31, so 25 percent is not ruled out, but 50 percent is.

**Why it matters:** A system that is evaluated on a handful of real trials cannot be told apart from many nearby rates. The honest report is the count and its range, not the share alone.

**In brains and behavior:** The chapter's brain-side counts are also small: one participant in the walking study, eight men in the unseen-hand test, two monkeys in the eye-jump study, and eight people in the reaching-variance test. The same caution applies to any share computed from them.

**In machines:** A robot test on 10 trials is a measurement with this much uncertainty. The 2019 preprint's hand-tuned simulation settings are a separate matter.

**Assumptions and limits:** The 10 trials are independent with one success rate each. The ranges describe those trials only; they do not say the trials were representative of other starts or sequences. The chapter's other numbers are likewise from small samples.

**Check:** For 0 successes in 10, the high end of the range is 1 - 0.025^(1/10). What is it?

**Answer:** 0.025^(0.1) = 0.6915, so the high end is 1 - 0.6915 = 0.308.

**Source:** Which errors to fix, and how a body model is repaired; anchor `which-errors-to-fix-and-how-a-body-model-is-repaired`. The counts come from the chapter's account of the 2019 Rubik's cube preprint: in 10 real trials starting with a solved cube and one fixed scrambling sequence, the hand completed it in 2 of 10 with a cube carrying its own sensors and in 0 of 10 when the cube's state was estimated from cameras. The preprint's own tests are not reproduced; the exact ranges are computed here from those counts.
