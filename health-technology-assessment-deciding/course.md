# Health Technology Assessment: Deciding What a Health System Should Buy
slug: health-technology-assessment-deciding
level: Master's / professional level. Assumes basic statistics and curiosity, no prior health economics. Lectures 13-19 are deliberately more technical and are tagged #advanced where they assume modelling vocabulary.
language: English narration and labels throughout. Norwegian policy terms are kept in Norwegian and glossed once: nytte (benefit), ressursbruk (resource use), alvorlighet (severity), absolutt prognosetap (absolute shortfall), blaresept, Beslutningsforum.
notation: Consistent across all lectures: two options, new technology (1) vs current care (0). C = cost, E = effect in QALYs; DeltaC = C1 - C0, DeltaE = E1 - E0. ICER = DeltaC / DeltaE. Threshold = lambda (kr per QALY). Net monetary benefit NMB = lambda*DeltaE - DeltaC. Health utility u in [0,1], u=1 full health, u=0 dead, negative values allowed for states worse than dead. QALY = sum over t of u_t * time_t, discounted at rate r (Norwegian guideline r = 4%). Markov: states S, cycle length one year, transition matrix P. Cost-effectiveness plane always drawn with DeltaE on the x-axis and DeltaC on the y-axis, threshold line through the origin with slope lambda.
example: Running example: nusinersen (Spinraza) for spinal muscular atrophy in Norway - a drug with a real, visible effect and an extraordinary price, rejected and then accepted with an age limit by Beslutningsforum. Contrast case used repeatedly: a cheap, boring, high-volume intervention (statins for primary prevention, or hip replacement) that buys far more health per krone but no headlines. Both are carried through the QALY, costing, modelling, threshold and uncertainty lectures so the same numbers keep reappearing.

A course on how health systems decide whether something new is worth its price: the principles behind priority setting, the definitions that make them operational, the methods that produce a number, and the uncertainty that should stop us from trusting that number too much. Built around one Norwegian case that made the front pages, and one that never did.

---
## It works. So why is anyone still saying no?
What exactly are we being asked when someone asks whether a new treatment is 'worth it'?
Why is 'it has a real effect' not enough to justify adoption, in a private clinic as much as in a public system?
Who is the 'we' that pays for nusinersen, and what does that 'we' give up?
#question #why #long #english #male #calm #rich #ask #parts=4

---
status: done · id: 15be9777-72dc-4220-8337-71a236f933ac · file: it-works-so-why-is-anyone-still-saying.yaml · 2026-08-30
## The patients you never meet: opportunity cost as the hidden loser
If the budget is fixed, who pays for a yes - and why do they never appear in the newspaper?
Why does an opportunity cost exist even for a rich private buyer with no budget cap?
#short #socratic #dry #english #female #parts=3

---
status: done · id: fc2a6b0e-b236-4a8c-a81e-b225797719db · file: the-patients-you-never-meet-opportunity.yaml · 2026-08-30
## Where did this whole enterprise come from?
What made Archie Cochrane's 1972 'Effectiveness and Efficiency' the founding text of a field about money?
Why did the US Congress build an Office of Technology Assessment in 1972 and then abolish it in 1995?
Why did Britain create NICE in 1999, and why was 'postcode lottery' the phrase that did it?
#long #history #story #human #english #male #parts=4

---
status: done · id: 91ac580f-752e-4ff9-9169-7b5fe9e99f5a · file: where-did-this-whole-enterprise-come.yaml · 2026-08-30
## Norway's priority-setting system, criterion by criterion
The three criteria of Meld. St. 34 (2015-2016): nytte, ressursbruk, alvorlighet
Absolutt prognosetap: how severity becomes a number, and how it raises what we are willing to pay
Who does what: Legemiddelverket's method assessment, Bestillerforum, Beslutningsforum, and the blaresept route for outpatient drugs
The commissions behind it: Lonning I (1987), Lonning II (1997), Norheim (NOU 2014:12), Magnussen (2015)
#data #facts #long #english #female #rich #parts=5

---
status: done · id: dd1f65a1-ff2c-403f-8c50-7d4871c839f5 · file: norway-s-priority-setting-system.yaml · 2026-08-30
## Whose costs count? The perspective question decides the answer
Why can the same drug be cost-effective from a societal perspective and a disaster from the hospital's budget?
What enters and leaves the calculation when we move from health-payer to societal perspective: productivity, informal care, transport, municipal services?
Which perspective should a Norwegian decision use - and who is silently harmed by each choice?
#long #debate #quiz #english #male #parts=4

---
status: done · id: f2674cd0-da86-47ab-8c74-9b78df265858 · file: whose-costs-count-the-perspective.yaml · 2026-08-30
## What is a QALY really claiming about you?
How do we get from 'ten years in a wheelchair' to a single number?
What does multiplying quality by time assume - and would you actually accept that trade for yourself?
Why did we need a common currency at all, instead of comparing life-years and symptoms separately?
#long #question #calm #english #female #parts=4

---
status: done · id: a894638a-6c4a-44e6-af83-76c864d26575 · file: what-is-a-qaly-really-claiming-about-you.yaml · 2026-08-30
## How can you possibly measure how bad an illness feels? A map of the methods
What is the difference between direct valuation (VAS, time trade-off, standard gamble) and indirect instruments (EQ-5D, SF-6D, 15D)?
Why does a descriptive system need a separate value set, and why does the same EQ-5D state get different values in Norway, the UK and the US?
When is a discrete choice experiment the right tool, and what does it buy you that a rating scale cannot?
#long #rich #english #male #parts=5

---
status: done · id: 322b3a3b-54a3-404a-a3ed-9c40e6dc85fb · file: how-can-you-possibly-measure-how-bad-an.yaml · 2026-08-30
## Time trade-off and standard gamble: whose values, and what lies below zero?
How does each method actually work, step by step, on the same health state?
Why do the two methods give systematically different numbers, and which distortion belongs to which?
Should we ask patients who live in the state, or the general public who pay for it - and why do they disagree so consistently?
What does it mean for a state to be valued worse than dead, and what does that do to a QALY calculation?
#long #controversy #quiz #english #female #parts=5

---
status: done · id: 0334b32b-4bb6-44b0-8913-a531fc1e76c2 · file: time-trade-off-and-standard-gamble-whose.yaml · 2026-08-30
## Severity: absolute shortfall, proportional shortfall, or something else?
Why should severity buy a higher price per QALY at all, if a QALY is a QALY?
How do absolute prognosetap and proportional shortfall treat a 20-year-old and an 80-year-old differently?
Is severity a fairness correction or a second bite at the same benefit - and where does the Norwegian system land?
#long #debate #ask #english #male #parts=4

---
status: done · id: 9f0a8382-e226-4d91-add6-dd67d416def4 · file: severity-absolute-shortfall-proportional.yaml · 2026-08-30
## What counts as a cost, and why does the future cost less?
Where do unit costs come from: micro-costing a procedure versus top-down DRG averages?
Should lost production count, and does the human capital or the friction cost approach reflect what society actually loses?
Norway discounts both costs and health effects at 4% a year - why discount health at all, and what happens to a childhood intervention if you don't?
Which costs are routinely forgotten: informal care, unrelated future medical costs, the cost of the assessment itself?
#long #dry #english #female #parts=5

---
status: done · id: 64c96802-ea7d-4e6f-9f06-41d2483efcd0 · file: what-counts-as-a-cost-and-why-does-the.yaml · 2026-08-30
## CEA, CUA, CBA - and why cost-of-illness answers a different question entirely
What does each method compare, and what does each require you to be able to measure?
Why is cost-minimisation almost always a mistake in disguise?
Why is a cost-of-illness study not an evaluation of anything, and why is it still quoted as if it were?
When is cost per natural unit (per case detected, per infection avoided) better than cost per QALY?
#long #proscons #english #male #parts=5

---
status: done · id: 8f38dfea-b0c8-4260-8782-673b275ad57a · file: cea-cua-cba-and-why-cost-of-illness.yaml · 2026-08-30
## What is a life worth in money, and who decided that?
How do revealed preference studies read a value of a statistical life off wage premiums for risky jobs?
What goes wrong with stated preference and contingent valuation - scope insensitivity, protest answers, hypothetical bias?
Why do transport and safety regulators use values per statistical life far above what health-sector thresholds imply, inside the same government?
Does cost-benefit analysis capture things cost-utility cannot - dignity, information, process utility?
#long #controversy #facts #quiz #english #female #parts=5

---
status: done · id: d9a5153f-49d9-4c6a-b356-b7aa61f68091 · file: what-is-a-life-worth-in-money-and-who.yaml · 2026-08-30
## Why model at all - and which model shape fits which problem?
The trial ran three years and the patient lives forty - what do we do with the missing thirty-seven?
When is a decision tree enough, and when does the recurring, time-dependent nature of disease force a Markov model?
When do you need discrete event simulation or an individual-level model, and what does that cost you in transparency?
#long #podcast #fun #english #male #parts=4

---
status: done · id: 5016ca72-f9b3-40c1-842c-8da0ee9b2b51 · file: why-model-at-all-and-which-model-shape.yaml · 2026-08-30
## Building a Markov model: states, cycles, transitions and the long tail
How do you choose states so that they are exhaustive, mutually exclusive and clinically honest?
Where do transition probabilities come from, and how do you convert a rate into a per-cycle probability without lying?
Why does the extrapolation of the survival curve beyond the trial often drive the whole result?
What are half-cycle correction, tunnel states and time dependence actually fixing?
How do you check a model you cannot validate against the future: internal, external and cross-model validation?
### The states and the cycle
### Filling the transition matrix
### Extrapolating past the evidence
### Does the model deserve trust?
#verylong #advanced #english #female #parts=6

---
status: done · id: e3aaf1f3-4dc6-4081-94c5-277f5dc31303 · file: building-a-markov-model-states-cycles.yaml · 2026-08-30
## The ICER, the plane, and why net benefit is easier to think with
How do you read the four quadrants of the cost-effectiveness plane, and why are two of them uncomfortable?
Why is the ICER a treacherous number - negative ICERs, dominance, extended dominance?
How does net monetary benefit remove those pathologies, and what does it require you to commit to?
With more than two options, why must you build an efficiency frontier instead of comparing everything to placebo?
#long #quiz #english #male #parts=5

---
status: done · id: 01f1c1c1-12b2-4001-9b66-46c012f50682 · file: the-icer-the-plane-and-why-net-benefit.yaml · 2026-08-30
## Where does the threshold come from - willingness to pay, or what we displace?
What is the difference between a demand-side threshold (what society will pay) and a supply-side one (what the marginal krone currently buys)?
NICE uses 20-30,000 pounds per QALY while Claxton and colleagues estimated the NHS marginal productivity at about 13,000 - what should happen when the two disagree?
Why did the WHO's old '1-3 times GDP per capita' rule get abandoned by its own authors?
If the threshold is too high, who actually dies - and can we ever see them?
#long #controversy #facts #english #female #parts=5

---
status: done · id: d221c727-2b28-44e2-9b5f-8fc4815e58c3 · file: where-does-the-threshold-come-from.yaml · 2026-08-30
## Which uncertainties can more money actually fix?
What separates parameter uncertainty, structural uncertainty, heterogeneity and methodological uncertainty?
Why is heterogeneity not uncertainty at all, and what happens when you average over it?
Which of these can a new trial reduce, and which will still be there after every trial is run?
#long #question #english #male #parts=4

---
status: done · id: 1e96df7e-34ba-46da-893f-a2b17d4b2273 · file: which-uncertainties-can-more-money.yaml · 2026-08-30
## Showing what you don't know: from tornado diagrams to acceptability curves
Why best-case/worst-case analysis is the worst common practice, and what it implies about probability
One-way sensitivity analysis and the tornado diagram, read bar by bar on the nusinersen model
Probabilistic sensitivity analysis: distributions on parameters, 1000 draws, a scatter on the cost-effectiveness plane
The cost-effectiveness acceptability curve, and what 'probability 0.7 cost-effective' does and does not mean
#long #data #quiz #english #female #parts=5

---
status: done · id: 88240aa2-d76b-4d99-8fc1-d5d1c6154850 · file: showing-what-you-don-t-know-from-tornado.yaml · 2026-08-30
## If we are unsure, should we decide now or pay to learn?
What does expected value of perfect information put a price on, and why is it bounded by the cost of being wrong?
How does EVPPI tell you which single parameter is worth a new study?
Why do 'approve only in research' and managed entry agreements follow directly from this logic?
#short #advanced #dry #english #male #parts=3

---
status: done · id: 1c8124f5-19d9-45e1-9a1b-ad85f05499fd · file: if-we-are-unsure-should-we-decide-now-or.yaml · 2026-08-30
## Is the QALY fair - and should the number decide?
The case against: does the QALY discriminate against disabled, elderly or chronically ill people by construction?
The case for: what were we doing before, and was it more fair or just less visible?
Where do the rule of rescue, ultra-rare diseases and identified versus statistical lives break the arithmetic?
Can multi-criteria decision analysis or deliberative process repair it, or do they just relocate the judgement?
If the analysis is a decision aid rather than a decision machine, what is the analyst actually accountable for?
### The case against the QALY
### The case for the QALY
### What the number cannot settle
### Aid, not machine
#verylong #debate #controversy #human #english #female #parts=6
status: done · id: bd8d5e0c-d884-48ef-8917-60ebe52e3e44 · file: is-the-qaly-fair-and-should-the-number.yaml · 2026-08-30
