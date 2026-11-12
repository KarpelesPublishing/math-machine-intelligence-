# Chapter 1: What Does It Take to Make a Mind?

Turn a noisy recording into an estimate, weigh unequal voices, and ask what a partnership added.

Ask what each source reports and how reliable it is, whether their errors are independent, what the best real alternative is, and whether a claim is a measured result, a drawn comparison or an open question. Work the weights and the comparison by hand before running any simulation, and say what was constructed.

Practical question: A person scores 70 out of 100, a tool scores 80, and together they score 75. Did the tool help?

## C01-D01: How does a decoder turn a noisy recording into probabilities?

A recording lands at one value, and each of three attempts (left hip, neither, right hip) would leave a noisy value near its own center. How likely is each attempt?

Each attempt would leave a recorded value near its own center, blurred by noise. Given a recording, the closer a center is, the more weight that attempt gets. Dividing each weight by the total makes the three weights probabilities that add to one. When the noise is large, even a recording sitting on a center leaves the other attempts plausible.

$$
p_k=\frac{\exp\!\bigl(-(x-\mu_k)^2/(2\sigma^2)\bigr)}{\sum_m \exp\!\bigl(-(x-\mu_m)^2/(2\sigma^2)\bigr)}
$$

**Symbols:** x: the recorded value; mu_k: the typical value for attempt k: minus 1, 0 and 1 here; sigma: how far a recording typically strays from its center (the noise); p_k: the estimated probability of attempt k, assuming the three attempts are equally likely to start

**Predict:** If the recording lies exactly midway between the centers for 'neither' (0) and 'right hip' (1), predict what the decoder reports for those two attempts.

**Worked example:**
- Probability of left hip: 0.111
- Probability of neither: 0.389
- Probability of right hip: 0.5
- Most likely attempt: right hip

At recorded value 0.75 with noise 1, the most likely attempt is right hip at probability 0.5. The decoder gives a probability for each attempt and never a command.

**Calculation:** Weights for left hip, neither, right hip: e^(-(0.75 - (-1))^2 / 2) = 0.216, e^(-(0.75 - (0))^2 / 2) = 0.755, e^(-(0.75 - (1))^2 / 2) = 0.969. Each probability is its weight divided by the total 1.94.

**Takeaway:** A recording does not say 'move the left leg'. It supports probabilities, which the system then uses.

**What happens:** At Recorded value = 0.5, Noise (sigma) = 1: At x = 0.5 the two attempts get exactly the same probability, 0.422 each, and the left hip gets 0.155. The decoder gives a graded estimate and not a command, and a tie is allowed.

**Why it matters:** This is the first job mathematics does in the book: it turns messy measurements into an estimate that can guide an action.

**In brains and behavior:** The brain recordings were measurements associated with attempted movement; the chapter notes the paper says intention and attempt, not thought.

**In machines:** The decoder is a program that maps measurements to estimates; its probabilities helped set the strength of stimulation.

**Assumptions and limits:** One recorded value, three attempts that start equally likely, and equal noise for each. A real decoder uses many measurements and learned weights.

**Check:** With noise 2 instead of 1, does a recording at 1 (the right-hip center) make the right hip more certain or less certain than with noise 1?

**Answer:** Less certain. Greater noise blurs the three bell curves together, so the right hip's probability falls (from about 0.574 to about 0.402 here) and the others rise.

**Source:** A recording is not a command; anchor `a-recording-is-not-a-command`. A constructed illustration of the chapter's statement that the decoder estimated the probabilities of attempting to flex the left hip, the right hip or neither. The bell-curve model, the centers and the noise are invented here; the study's decoder is built differently and uses several recording sites.

## C01-D02: How much calibration data does a decoder need?

A decoder learns the typical recording for each attempt from examples. How does its accuracy depend on how many examples it saw, and how noisy the recordings are?

The decoder learns where each attempt typically lands by averaging the examples it saw. With few examples, those averages are off by about sigma over the square root of the number of examples, and misplaced centers cause avoidable mistakes. More examples shrink that error, but on average accuracy cannot pass the ceiling set by the noise in single recordings. A simulated average can land a hair above it by chance, so a gap smaller than 0.1 points is shown as under 0.1 points and not as a negative number.

$$
\text{spread of the learned center}=\frac{\sigma}{\sqrt{n}},\qquad \text{ceiling}=\frac{4\,\Phi\!\left(\tfrac{1}{2\sigma}\right)-1}{3}
$$

**Symbols:** n: calibration examples per attempt; sigma: noise in a single recording; Phi: the standard bell-curve cumulative probability; ceiling: the best accuracy a nearest-center rule can reach with the three centers known exactly

**Predict:** At noise 1, predict whether 5 examples per attempt are enough to get near the ceiling, or whether you need many more.

**Worked example:**
- Average accuracy: 57.8 percent
- Accuracy if the means were known: 58.9 percent
- Gap to that ceiling: 1.1 points
- Worst tenth of calibrations: 57 percent or less

With 10 examples per attempt and noise 1, 400 simulated calibrations averaged 57.8 percent correct, against a ceiling of 58.9 percent. The spread between calibrations is part of the answer: the worst tenth scored 57 percent or less.

**Calculation:** Each calibration estimates a mean from 10 noisy examples, whose own error has spread 1 / sqrt(10) = 0.316. Ceiling: (4 x Phi(0.5 / 1) - 1) / 3 = 0.589, where Phi is the bell-curve cumulative probability.

**Takeaway:** Calibration is estimation too: a few noisy examples give a noisy decoder, and the error in each learned center shrinks like one over the square root of the examples.

**What happens:** At Examples per attempt = 5, Noise (sigma) = 1: At noise 1, five examples per attempt averaged about 56 percent against a ceiling of about 59, and a few calibrations did much worse. One example per attempt averages about 47 percent, so the first few examples close most of the gap and later ones add little.

**Why it matters:** It shows why the study's time spent calibrating, and recalibrating on later days, is part of the mathematics and not just housekeeping.

**In brains and behavior:** The person supplied the examples by attempting each movement; the chapter says Oskam supplied the examples and the machine found the pattern.

**In machines:** The decoder estimates its own parameters from examples, and the examples it saw limit how well it can estimate.

**Assumptions and limits:** A one-number recording, equal noise, centers at -1, 0 and 1, and a nearest-learned-center rule. The study's decoder was calibrated differently and updated over later days. A simulation here is not a measurement of any person or system.

**Check:** Why does halving the noise help more than quadrupling the examples?

**Answer:** The ceiling itself depends on the noise, and quadrupling the examples only halves the center error. Halving the noise both halves the center error and lifts the ceiling.

**Source:** A recording is not a command; anchor `a-recording-is-not-a-command`. Simulation with disclosed seeds: 400 calibrations per setting, each tested on 3000 fresh recordings (1000 per attempt), using the invented three-center model of C01-D01. It does not model the study's calibration, whose five-minute standing test and six weeks of preparation the chapter reports.

## C01-D03: Why not give every voice an equal say?

A person and a machine estimate the same quantity and one is steadier. What does an equal share do to the error spread, and what does a reliability weight do?

The blend's spread depends on how much of each voice goes in. Putting all weight on the steadier source gives its own spread. Moving a small share to the weaker source lowers the spread, because their errors partly cancel, and the best share is the one in inverse proportion to each source's variance. An equal share goes too far when one source is much weaker.

$$
w^{*}=\frac{\sigma_m^{2}}{\sigma_p^{2}+\sigma_m^{2}},\qquad \sigma_{\text{blend}}^{2}=w^{2}\sigma_p^{2}+(1-w)^{2}\sigma_m^{2},\qquad \sigma_{*}^{2}=\frac{1}{1/\sigma_p^{2}+1/\sigma_m^{2}}
$$

**Symbols:** w: the share given to the person; the machine gets 1 minus w; sigma_p, sigma_m: the error spread of the person's and the machine's estimates; w*: the share that gives the smallest blend spread; sigma_*: the smallest achievable spread

**Predict:** If the person is twice as variable as the machine, predict whether a plain 50-50 average beats the machine alone.

**Worked example:**
- Blend error spread: 1.12
- Better source alone: 1
- Blend against the better source: worse
- Share given to the person: 0.5

With the person 2 times as variable, an equal share gives a spread of 1.12, above the 1 of the better source alone. Mixing in a much weaker voice at equal weight hurts.

**Calculation:** Blend spread = sqrt(w^2 x 2^2 + (1 - w)^2 x 1^2). Equal share w = 0.5 gives sqrt(1 + 0.25) = 1.12. Reliability weight w = 1 / (2^2 + 1) = 0.2 gives 0.894, which equals 1 / sqrt(1/2^2 + 1/1^2).

**Takeaway:** Under no bias and independent errors, a reliability weight beats either source alone, while an equal share can lose to the better one.

**What happens:** At Person's spread relative to the machine's = 2, Rule for the share = equal share: No. The equal share gives a spread of about 1.12 against the machine's 1. Reliability weights of 0.2 for the person and 0.8 for the machine give about 0.894, better than either source alone.

**Why it matters:** It turns the question 'should I trust the tool?' into a sharper one: how much weight does each source deserve, given how reliable it is?

**In brains and behavior:** The same rule was tested on how people combine sight and touch (C01-D05).

**In machines:** An engineer can use the rule to combine uncertain measurements, as the chapter says.

**Assumptions and limits:** Both estimates are unbiased and their errors are independent. Shared errors or a consistent bias can change the answer. Spread means how much an estimate varies from one attempt to the next.

**Check:** With equal spreads, what is the best share for the person, and what is the blend's spread?

**Answer:** The best share is one half, and the spread is 1/sqrt(2), about 0.71 of either source alone, because with equal reliability the plain average is the reliability-weighted blend.

**Source:** Not every voice deserves an equal say; anchor `not-every-voice-deserves-an-equal-say`. Book rule, stated in words in this chapter and worked in Chapter 2. The ratio of spreads is a control; the numbers are illustrative, not from a study. The rule needs the independence and no-bias conditions listed.

## C01-D04: What did the partnership add?

A person scores 70 out of 100, a machine scores 80, and together they score 75. Did the machine help?

There are three differences to compute. The pair minus the person shows what the machine added to the person. The pair minus the machine shows what the person added to the machine. The pair minus the better of the two tells whether the partnership beat the best alternative that was available.

$$
\text{added}=S_{\text{pair}}-\max\bigl(S_{\text{person}},\,S_{\text{machine}}\bigr)
$$

**Symbols:** S_person: the person's solo score, 70 here; S_machine: the machine's solo score; S_pair: the score of the person and machine together; max: the better of the two solo scores

**Predict:** With scores 70, 80 and 75, predict which of these is true: the pair beats the person; the pair beats the machine.

**Worked example:**
- Pair minus person: +5
- Pair minus machine: -5
- Better solo score: 80
- Did the pair beat the best alone: no, 5 short

The pair scores 75, which is +5 against the person and -5 against the machine. Saying only the first would hide that the better available result was 80.

**Calculation:** Pair minus person = 75 - 70 = +5. Pair minus machine = 75 - 80 = -5. Pair minus the better solo score = 75 - 80 = -5.

**Takeaway:** Compare the pair with its best real alternative, not only with the weaker member.

**What happens:** At Pair's score = 75, Machine's solo score = 80: Both statements are true in different directions: the pair beats the person by 5 and loses to the machine by 5. Reporting only the first would hide the better available result.

**Why it matters:** The arithmetic turns 'did the machine help?' into a sharper question: what did the partnership add compared with the best alternative?

**In brains and behavior:** A person's solo score is a measured alternative only when the person could do the task alone.

**In machines:** A machine's solo score matters only if the machine could be deployed alone.

**Assumptions and limits:** Both solo scores are real alternatives. A walking aid cannot walk alone as a person does, so comparing its solo score with a person's would answer nothing. The right comparison depends on the task and the outcome that matters. With only 100 questions a gap of a few points may be sampling noise, a point the chapter's invented numbers do not address.

**Check:** The pair scores 85 and the machine 80. What do the three comparisons say, and what does the result hint at?

**Answer:** Pair minus person is +15, pair minus machine is +5, and pair minus the best solo score is +5. The pair beat the best alternative, which would point to a real contribution from the partnership, subject to sampling noise.

**Source:** Not every voice deserves an equal say; anchor `not-every-voice-deserves-an-equal-say`. The chapter's constructed example, stated as invented numbers and not a study's results. The machine's score and the pair's score are controls here.

## C01-D05: How does a prediction tell two rules apart?

Sight and touch both judge a bar's height, and the picture can be made grainier. What does each combination rule predict about leaning toward touch, and about how finely the two senses together discriminate?

The reliability-weight rule makes two predictions. As the picture gets grainier, the judgment should lean smoothly toward touch. And the two senses together should discriminate more finely than either alone. A plain average predicts no lean. A winner-take-all rule predicts a sudden jump and no combined gain. Observing a lean and a gain together fits the reliability rule and counts against the others.

$$
w_{\text{touch}}=\frac{1/\sigma_h^{2}}{1/\sigma_h^{2}+1/\sigma_v^{2}},\qquad \sigma_{\text{both}}^{2}=\frac{\sigma_v^{2}\sigma_h^{2}}{\sigma_v^{2}+\sigma_h^{2}}
$$

**Symbols:** sigma_v, sigma_h: the spread of the visual and the touch judgments; w_touch: the share of the judgment given to touch; sigma_both: the predicted spread when both senses are used

**Predict:** If vision becomes twice as variable as touch, predict how much of the judgment each rule gives to touch, and which rule predicts a gain over the steadier sense.

**Worked example:**
- Share given to touch: 0.8
- Spread of the combined judgment: 0.894
- Steadier sense alone: 1
- Combined against the steadier sense: better

Reliability weights give touch 0.8 here, and the combined spread 0.894 is better than the steadier sense alone (1). The lean grows smoothly as the picture gets grainier.

**Calculation:** Touch spread 1, vision spread 2. Reliability weight on touch = 2^2 / (2^2 + 1) = 0.8. For the selected rule the share is 0.8, so spread = sqrt(0.8^2 x 1 + 0.2^2 x 2^2) = 0.894.

**Takeaway:** A rule is an idea until its predictions are checked, and different rules predict different leans and different gains.

**What happens:** At Vision's spread relative to touch's = 2, Combination rule = reliability weights: Reliability weights give touch 0.8 and predict a combined spread of 0.894, finer than either sense (1 and 2). A plain average gives touch 0.5 whatever the picture quality, and always trusting the steadier sense can never beat the steadier sense, because it is that sense.

**Why it matters:** This is the difference between describing, predicting and building: the rule described a pattern, predicted what happens when a sense degrades, and can be used to build a machine that combines measurements.

**In brains and behavior:** A match to behavior does not prove the brain does this arithmetic; the paper offers neural populations as a candidate and tests none.

**In machines:** The same formula specifies a computation a machine performs on uncertain measurements.

**Assumptions and limits:** The three rules shown are hypotheses for contrast. Unbiased judgments and independent errors are assumed. The chapter notes a close match is good evidence about behavior, and how neurons produce it takes more evidence.

**Check:** If people showed a smooth lean toward touch but no gain from using both senses, which of the three rules would that count against?

**Answer:** It would count against the reliability-weight rule, which predicts both. The plain average predicts no lean, and the steadier-sense rule predicts a jump, so neither would fit a smooth lean either. A lean without a gain could also come from errors the two senses share (Chapter 2 shows shared error reduces the gain), so it counts against the rule only together with the independence assumption.

**Source:** The rule was tested on people; anchor `the-rule-was-tested-on-people`. The chapter reports Ernst and Banks (2002): judgments came close to the predicted lean toward touch as the picture grew grainier and to the prediction that two senses discriminate more finely than either alone. The numbers plotted here are constructed from the rule and are not their measurements.
