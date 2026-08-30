# Causal Inference in Economics: Evidence from Health and Health Care

Health care is where causal inference gets hard and where it matters most: sick people buy more insurance, hospitals that treat the toughest cases post the worst survival rates, and the states that expand coverage are not like the states that don't. This course builds the standard toolkit — potential outcomes, randomization, instrumental variables, difference-in-differences, regression discontinuity, synthetic control — around one running thread, Oregon's 2008 Medicaid lottery.

1. [What makes a question causal?](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/what-makes-a-question-causal.yaml)
   - What exactly is being compared when we say 'health insurance improved her health' — and why can that comparison never be observed for one person?
   - Why is the fundamental problem of causal inference a missing-data problem rather than a statistics problem?
   - What does the Oregon lottery let us see that a survey of insured and uninsured Oregonians never can?
2. [Why insured people can look sicker: selection bias, decomposed](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/why-insured-people-can-look-sicker-selection-bias-decomposed.yaml)
   - If we simply subtract mean outcomes, E\[Y|D=1\] − E\[Y|D=0\], what two terms is that difference actually made of?
   - Which way does selection bias run when the sick are the ones who sign up for coverage — and can it flip the sign of the true effect?
   - Why does 'we controlled for age, income and prior conditions' not make the second term disappear?
3. [The Oregon lottery: what randomization actually buys you](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/the-oregon-lottery-what-randomization-actually-buys-you.yaml)
   - What does random assignment make true about Y(1) and Y(0) that nothing else does?
   - How do we check that a lottery worked, and what would a failed balance table look like?
   - What did Oregon find in the first two years on health care use, financial strain, and depression — and what did it not find?
4. [The RAND Health Insurance Experiment: randomizing the price of care](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/the-rand-health-insurance-experiment-randomizing-the-price-of-care.yaml)
   - What did RAND randomize between 1974 and 1982, and why randomize coinsurance rates rather than coverage itself?
   - What happened to spending when care was free, and what happened to measured health?
   - Why is 'more care did not improve average health' the most misread sentence in health economics?
5. [Which average effect are you even estimating?](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/which-average-effect-are-you-even-estimating.yaml)
   - When do ATE and ATT differ, and which one does a policymaker expanding Medicaid actually need?
   - Why can a perfectly internally valid estimate be the wrong number for the next state?
6. [Nobody complies: intention-to-treat versus the effect of treatment](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/nobody-complies-intention-to-treat-versus-the-effect-of-treatment.yaml)
   - Only about a quarter of Oregon's lottery winners ended up on Medicaid — what does the simple winners-versus-losers comparison then measure?
   - Why is comparing enrollees to non-enrollees among lottery winners a trap, even inside a randomized experiment?
   - When is the diluted ITT the number you want, and when is it a nuisance to be scaled up?
7. [Instrumental variables and the LATE theorem](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/instrumental-variables-and-the-late-theorem.yaml)
   - What are the four assumptions — relevance, independence, exclusion, monotonicity — and what does each one rule out in the Oregon setting?
   - Who is a complier, and why can we count compliers but never name them?
   - Why does dividing the reduced form by the first stage recover an effect only for that subgroup?
8. [Bad instruments, weak instruments](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/bad-instruments-weak-instruments.yaml)
   - Why is 'distance to the nearest cardiac catheterization hospital' a defensible instrument for treatment intensity, and what would break its exclusion restriction?
   - Where does the F \> 10 rule of thumb come from, and why do recent econometricians argue it is far too lenient?
   - What does a weak instrument do to bias and to confidence intervals — and why is it worse than doing nothing?
9. [Selection on observables: matching, regression, and the leap of faith](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/selection-on-observables-matching-regression-and-the-leap-of-faith.yaml)
   - What does conditional independence actually assert, and what would have to be true about the uninsured for it to hold?
   - What does common support mean, and what happens to the estimand when we quietly drop units without a match?
   - Where does matching beat regression, and where do both fail identically?
10. [Arrows or potential outcomes? Bad controls and colliders](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/arrows-or-potential-outcomes-bad-controls-and-colliders.yaml)
   - Why can adding a control variable — say, hospital admission — create bias rather than remove it?
   - How does a causal graph diagnose collider bias faster than the potential-outcomes notation, and what does the graph hide in return?
   - Is the Pearl-versus-Rubin disagreement about substance or about language?
11. [Difference-in-differences and the parallel trends assumption](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/difference-in-differences-and-the-parallel-trends-assumption.yaml)
   - What is the 2×2 DiD estimator subtracting, and what exactly does parallel trends claim about the untreated potential outcome?
   - Do pre-treatment parallel lines prove the assumption, or only fail to refute it?
   - When Medicaid expansion states are compared to non-expansion states, what plausible story would break parallel trends?
12. [When treatment arrives at different times: staggered DiD in trouble](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/when-treatment-arrives-at-different-times-staggered-did-in-trouble.yaml)
   - What comparisons does two-way fixed effects actually make when states adopt a policy in different years — and why is one of them already-treated units serving as controls?
   - How can the TWFE coefficient be negative when every single unit's effect is positive?
   - What do the Goodman-Bacon decomposition and the Callaway–Sant'Anna and Sun–Abraham estimators do differently, and what do you give up to use them?
   - Does the recent literature mean older staggered DiD papers are wrong, or only that their weights were unexamined?
13. [Regression discontinuity: what happens at your 65th birthday](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/regression-discontinuity-what-happens-at-your-65th-birthday.yaml)
   - Why does turning 65 in the United States create a jump in insurance coverage but not in anything else about a person?
   - What is the identifying assumption of RD, and why is it weaker than parallel trends but narrower in what it delivers?
   - What did the Medicare-at-65 discontinuity reveal about hospital use and about mortality among severely ill patients admitted through emergency departments?
14. [Stress-testing a discontinuity](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/stress-testing-a-discontinuity.yaml)
   - Why does bandwidth choice change the estimate, and what does a sensible sensitivity plot look like?
   - What is manipulation of the running variable, how would a density test detect it, and why can birthdays not be manipulated but income thresholds can?
   - In a fuzzy RD, what is being instrumented by what — and which average does the jump ratio deliver?
15. [Building a counterfactual state: synthetic control and Proposition 99](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/building-a-counterfactual-state-synthetic-control-and-proposition-99.yaml)
   - When you have one treated unit and thirty-eight candidate controls, why is a weighted combination better than either the best match or the simple average?
   - How were the donor weights chosen for synthetic California, and what does the pre-1988 fit buy in credibility?
   - How large was the estimated decline in per-capita cigarette sales by 2000, and how do placebo runs on untreated states give us inference without standard errors?
16. [Reading a null: power, precision, and the Oregon blood-sugar result](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/reading-a-null-power-precision-and-the-oregon-blood-sugar-result.yaml)
   - Oregon found no statistically significant effect on blood pressure, cholesterol or glycated hemoglobin — does that mean Medicaid does not improve physical health?
   - How do you use the confidence interval, rather than the p-value, to say what the study did and did not rule out?
   - Why did the same table get read as proof Medicaid works and proof it doesn't, and what would a well-powered follow-up have needed?
17. [Genes as instruments: Mendelian randomization](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/genes-as-instruments-mendelian-randomization.yaml)
   - Why is the allele you inherit at conception closer to a lottery draw than almost anything else an economist can find?
   - How does the alcohol-metabolism variant common in East Asian populations identify the effect of drinking on health?
   - What is horizontal pleiotropy, and why is it just the exclusion restriction wearing a lab coat?
18. [Choosing a design, and turning an estimate into a policy](https://drawcast.app/#gh=hmelberg/dcast/causal-inference-in-economics-evidence-from-health-and-health-care/choosing-a-design-and-turning-an-estimate-into-a-policy.yaml)
   - Given a health policy question and the data you actually have, how do you decide between RCT, IV, DiD, RD and synthetic control — and what is the assumption you are agreeing to defend in each case?
   - Your estimate is a LATE for compliers in Oregon in 2008; what has to be argued before it can be used to price a Medicaid expansion elsewhere?
   - When cost-effectiveness turns a causal estimate into a cost per quality-adjusted life year, which parameters are causal and which are value judgements in disguise?

---

Made with [drawcast](https://drawcast.app/).
