# Causal Inference in Economics: Evidence from Health and Health Care
slug: causal-inference-in-economics-evidence-from-health-and-health-care
level: Advanced undergraduate / first-year graduate economics; assumes regression, expectations and basic probability, but every design is built up from scratch before any algebra
language: English
notation: One notation throughout. D_i ∈ {0,1} is the treatment (default meaning: individual i has health insurance coverage). Y_i is the outcome (default: a health or spending outcome). Potential outcomes Y_i(1) and Y_i(0); observed outcome Y_i = D_i·Y_i(1) + (1−D_i)·Y_i(0); individual effect τ_i = Y_i(1) − Y_i(0). ATE = E[τ_i], ATT = E[τ_i | D_i = 1], LATE = E[τ_i | complier]. Z_i is an instrument or assignment (default: winning the Oregon lottery). X_i are covariates. Groups indexed by g, time by t; treatment timing g* in the DiD lectures. Estimates carry hats (τ̂), standard errors in parentheses. Always say 'percentage points' for level changes and 'percent' for relative changes. Diagrams: treated units in solid outline, untreated in dashed; time always runs left to right.
example: The Oregon Health Insurance Experiment: in 2008 Oregon had money to expand Medicaid to about 10,000 adults, roughly 90,000 people signed up, and the state allocated slots by lottery — about 30,000 names drawn, and only about a quarter of those drawn ended up enrolled. Every lecture returns to this one study: as the model of a randomized trial, as the source of the intention-to-treat versus LATE distinction, as an instrument, as a benchmark against which observational designs (DiD on ACA Medicaid expansions, RD at Medicare age 65, synthetic control) are judged, and as a case study in reading a null result.

Health care is where causal inference gets hard and where it matters most: sick people buy more insurance, hospitals that treat the toughest cases post the worst survival rates, and the states that expand coverage are not like the states that don't. This course builds the standard toolkit — potential outcomes, randomization, instrumental variables, difference-in-differences, regression discontinuity, synthetic control — around one running thread, Oregon's 2008 Medicaid lottery.

---
## What makes a question causal?
What exactly is being compared when we say 'health insurance improved her health' — and why can that comparison never be observed for one person?
Why is the fundamental problem of causal inference a missing-data problem rather than a statistics problem?
What does the Oregon lottery let us see that a survey of insured and uninsured Oregonians never can?
#long #basic #english #why #question #female #calm #parts=4

---
status: done · id: 7fce1053-998d-4f04-a347-44be72d4e6a4 · file: what-makes-a-question-causal.yaml · 2026-08-29
## Why insured people can look sicker: selection bias, decomposed
If we simply subtract mean outcomes, E[Y|D=1] − E[Y|D=0], what two terms is that difference actually made of?
Which way does selection bias run when the sick are the ones who sign up for coverage — and can it flip the sign of the true effect?
Why does 'we controlled for age, income and prior conditions' not make the second term disappear?
#long #english #provoke #socratic #male #rich #parts=4

---
status: done · id: 4e1a14d0-ed16-4d7e-9be8-e6674759017f · file: why-insured-people-can-look-sicker-selection-bias-decomposed.yaml · 2026-08-29
## The Oregon lottery: what randomization actually buys you
What does random assignment make true about Y(1) and Y(0) that nothing else does?
How do we check that a lottery worked, and what would a failed balance table look like?
What did Oregon find in the first two years on health care use, financial strain, and depression — and what did it not find?
#long #facts #english #female #quiz #parts=5

---
status: done · id: 5d0b0826-1558-4c85-83cd-ec59371a2b55 · file: the-oregon-lottery-what-randomization-actually-buys-you.yaml · 2026-08-30
## The RAND Health Insurance Experiment: randomizing the price of care
What did RAND randomize between 1974 and 1982, and why randomize coinsurance rates rather than coverage itself?
What happened to spending when care was free, and what happened to measured health?
Why is 'more care did not improve average health' the most misread sentence in health economics?
#long #history #story #english #male #calm #parts=4

---
status: done · id: 6b6f889a-089e-43c7-a2cd-bc59903a7efc · file: the-rand-health-insurance-experiment-randomizing-the-price-of-care.yaml · 2026-08-30
## Which average effect are you even estimating?
When do ATE and ATT differ, and which one does a policymaker expanding Medicaid actually need?
Why can a perfectly internally valid estimate be the wrong number for the next state?
#short #advanced #english #dry #female #parts=3

---
status: done · id: 0a873a76-0b86-4be4-823e-61c972da0d24 · file: which-average-effect-are-you-even-estimating.yaml · 2026-08-30
## Nobody complies: intention-to-treat versus the effect of treatment
Only about a quarter of Oregon's lottery winners ended up on Medicaid — what does the simple winners-versus-losers comparison then measure?
Why is comparing enrollees to non-enrollees among lottery winners a trap, even inside a randomized experiment?
When is the diluted ITT the number you want, and when is it a nuisance to be scaled up?
#long #english #qa #male #why #parts=4

---
status: done · id: 9ae87296-5696-4c6e-920a-c30b31f6c6a4 · file: nobody-complies-intention-to-treat-versus-the-effect-of-treatment.yaml · 2026-08-30
## Instrumental variables and the LATE theorem
What are the four assumptions — relevance, independence, exclusion, monotonicity — and what does each one rule out in the Oregon setting?
Who is a complier, and why can we count compliers but never name them?
Why does dividing the reduced form by the first stage recover an effect only for that subgroup?
#long #advanced #english #female #quiz #click #parts=5

---
status: done · id: 15c80faf-bfc0-449e-827a-8c890f776f4b · file: instrumental-variables-and-the-late-theorem.yaml · 2026-08-30
## Bad instruments, weak instruments
Why is 'distance to the nearest cardiac catheterization hospital' a defensible instrument for treatment intensity, and what would break its exclusion restriction?
Where does the F > 10 rule of thumb come from, and why do recent econometricians argue it is far too lenient?
What does a weak instrument do to bias and to confidence intervals — and why is it worse than doing nothing?
#long #controversy #podcast #advanced #english #male #parts=4

---
status: done · id: baaf6741-1f9d-4184-a1c6-12f522d2b19c · file: bad-instruments-weak-instruments.yaml · 2026-08-30
## Selection on observables: matching, regression, and the leap of faith
What does conditional independence actually assert, and what would have to be true about the uninsured for it to hold?
What does common support mean, and what happens to the estimand when we quietly drop units without a match?
Where does matching beat regression, and where do both fail identically?
#long #proscons #english #female #calm #parts=4

---
status: done · id: 4df69cb0-95b4-40a0-a31a-ae01fa550d15 · file: selection-on-observables-matching-regression-and-the-leap-of-faith.yaml · 2026-08-30
## Arrows or potential outcomes? Bad controls and colliders
Why can adding a control variable — say, hospital admission — create bias rather than remove it?
How does a causal graph diagnose collider bias faster than the potential-outcomes notation, and what does the graph hide in return?
Is the Pearl-versus-Rubin disagreement about substance or about language?
#long #debate #advanced #english #male #parts=4

---
status: done · id: bb04fd37-1d8d-4d7b-8144-a672437da262 · file: arrows-or-potential-outcomes-bad-controls-and-colliders.yaml · 2026-08-30
## Difference-in-differences and the parallel trends assumption
What is the 2×2 DiD estimator subtracting, and what exactly does parallel trends claim about the untreated potential outcome?
Do pre-treatment parallel lines prove the assumption, or only fail to refute it?
When Medicaid expansion states are compared to non-expansion states, what plausible story would break parallel trends?
#long #facts #english #female #quiz #parts=5

---
status: done · id: e07453c7-e163-4fa4-8eb3-50c95d85aa64 · file: difference-in-differences-and-the-parallel-trends-assumption.yaml · 2026-08-30
## When treatment arrives at different times: staggered DiD in trouble
What comparisons does two-way fixed effects actually make when states adopt a policy in different years — and why is one of them already-treated units serving as controls?
How can the TWFE coefficient be negative when every single unit's effect is positive?
What do the Goodman-Bacon decomposition and the Callaway–Sant'Anna and Sun–Abraham estimators do differently, and what do you give up to use them?
Does the recent literature mean older staggered DiD papers are wrong, or only that their weights were unexamined?
### The problem: forbidden comparisons
### The diagnosis: decomposing the estimate
### The repair: clean controls and event-time plots
#verylong #advanced #controversy #english #male #click #parts=6

---
status: done · id: d606db00-52e8-492b-8911-42658ac2572d · file: when-treatment-arrives-at-different-times-staggered-did-in-trouble.yaml · 2026-08-30
## Regression discontinuity: what happens at your 65th birthday
Why does turning 65 in the United States create a jump in insurance coverage but not in anything else about a person?
What is the identifying assumption of RD, and why is it weaker than parallel trends but narrower in what it delivers?
What did the Medicare-at-65 discontinuity reveal about hospital use and about mortality among severely ill patients admitted through emergency departments?
#long #facts #english #female #parts=5

---
status: done · id: 7a4e2d76-9431-455f-b929-f5c81cee92cd · file: regression-discontinuity-what-happens-at-your-65th-birthday.yaml · 2026-08-30
## Stress-testing a discontinuity
Why does bandwidth choice change the estimate, and what does a sensible sensitivity plot look like?
What is manipulation of the running variable, how would a density test detect it, and why can birthdays not be manipulated but income thresholds can?
In a fuzzy RD, what is being instrumented by what — and which average does the jump ratio deliver?
#long #socratic #english #male #quiz #parts=4

---
status: done · id: 4de4d0cb-ecd3-479e-b4ee-75debc46e29d · file: stress-testing-a-discontinuity.yaml · 2026-08-30
## Building a counterfactual state: synthetic control and Proposition 99
When you have one treated unit and thirty-eight candidate controls, why is a weighted combination better than either the best match or the simple average?
How were the donor weights chosen for synthetic California, and what does the pre-1988 fit buy in credibility?
How large was the estimated decline in per-capita cigarette sales by 2000, and how do placebo runs on untreated states give us inference without standard errors?
#long #story #facts #english #female #parts=4

---
status: done · id: 32f86f70-51c7-4a0e-a892-ed5586756ce0 · file: building-a-counterfactual-state-synthetic-control-and-proposition-99.yaml · 2026-08-30
## Reading a null: power, precision, and the Oregon blood-sugar result
Oregon found no statistically significant effect on blood pressure, cholesterol or glycated hemoglobin — does that mean Medicaid does not improve physical health?
How do you use the confidence interval, rather than the p-value, to say what the study did and did not rule out?
Why did the same table get read as proof Medicaid works and proof it doesn't, and what would a well-powered follow-up have needed?
#long #controversy #english #human #male #parts=4

---
status: done · id: aa332131-c68a-4a01-b089-3f15e4f5a8bd · file: reading-a-null-power-precision-and-the-oregon-blood-sugar-result.yaml · 2026-08-30
## Genes as instruments: Mendelian randomization
Why is the allele you inherit at conception closer to a lottery draw than almost anything else an economist can find?
How does the alcohol-metabolism variant common in East Asian populations identify the effect of drinking on health?
What is horizontal pleiotropy, and why is it just the exclusion restriction wearing a lab coat?
#long #advanced #english #female #pun #parts=4

---
status: done · id: e5df175f-1c22-4fd6-9e4f-489b48fb2608 · file: genes-as-instruments-mendelian-randomization.yaml · 2026-08-30
## Choosing a design, and turning an estimate into a policy
Given a health policy question and the data you actually have, how do you decide between RCT, IV, DiD, RD and synthetic control — and what is the assumption you are agreeing to defend in each case?
Your estimate is a LATE for compliers in Oregon in 2008; what has to be argued before it can be used to price a Medicaid expansion elsewhere?
When cost-effectiveness turns a causal estimate into a cost per quality-adjusted life year, which parameters are causal and which are value judgements in disguise?
#verylong #english #why #quiz #male #click #parts=5
status: done · id: c2afd025-91a8-450c-adf4-7043f5e4152c · file: choosing-a-design-and-turning-an-estimate-into-a-policy.yaml · 2026-08-30
