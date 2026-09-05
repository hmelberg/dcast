# Taylor Series and the Economics of Approximation
slug: taylor-series-and-the-economics-of
enroll: https://drawcast.anvil.app
level: Advanced undergraduate / first-year graduate: comfortable with calculus, some optimization and basic macro, but not a measure-theory audience
language: English
notation: Expansion of f around the point a: f(x) ≈ f(a) + f'(a)(x−a) + ½f''(a)(x−a)² + … ; general term f⁽ⁿ⁾(a)/n! (x−a)ⁿ. Remainder written R_n(x), Lagrange form R_n = f⁽ⁿ⁺¹⁾(ξ)/(n+1)! (x−a)ⁿ⁺¹ with ξ between a and x. Steady-state / reference point always called a or x̄; deviations ε = x − x̄; log deviations x̂ = ln(x/x̄) ≈ (x−x̄)/x̄. Utility u(c), risk aversion coefficient γ, Arrow–Pratt measure A(c) = −u''(c)/u'(c).
example: One running example throughout: a household with CRRA utility u(c) = c^(1−γ)/(1−γ) facing an uncertain consumption level c around its mean c̄. The same curve is expanded first for pure approximation error (Lecture 1), then to second order to extract risk aversion and the certainty equivalent (Lecture 2), then in logs around a steady state to build a linearized macro model (Lecture 3).

Three lectures on why economists spend so much of their lives replacing true functions with polynomials. We build the Taylor expansion carefully, then watch its second-order term become risk aversion and its first-order term become nearly all of modern macro.

---
## Why should a polynomial built at one point tell you anything about its neighbours?
If I only know f, f', f'' … at the single point a, what right do I have to say anything about f somewhere else?
What exactly is the remainder R_n measuring, and why does the Lagrange form make the error a statement about the derivative you did not use?
Why does a Taylor series sometimes converge beautifully and sometimes not converge to the function at all — what does 1/(1+x²) know that we don't?
In practice, what makes economists stop at n = 1 or n = 2 rather than pushing n higher?
#long #advanced #english #question #why #history #calm #male #rich #parts=4

---
status: done · id: a3987712-2c9a-48f4-b8f6-db59dfb765cb · file: why-should-a-polynomial-built-at-one.yaml · 2026-09-05
## What is the second derivative doing in the utility function?
Expand u(c) around mean consumption c̄: why does the first-order term vanish in expectation and leave curvature alone with the variance?
How does that one term become the Arrow–Pratt measure A(c) = −u''/u', and why is the level of u irrelevant to it?
What does the certainty equivalent look like once we accept a quadratic approximation — and what have we quietly assumed about skewness and fat tails by stopping at second order?
The equity premium puzzle: given the observed US premium of roughly six percentage points a year, what γ does the second-order argument demand, and should we blame the preference or the approximation?
### Curvature meets variance
### The certainty equivalent
### Where the approximation strains
#verylong #advanced #english #socratic #facts #proscons #female #click #parts=6

---
status: done · id: 4a1b2727-a756-4d87-a40e-f10afadacc87 · file: what-is-the-second-derivative-doing-in.yaml · 2026-09-05
## Is log-linearizing around the steady state a technique or a bet?
Why do macroeconomists write x̂ = ln(x/x̄), and in what sense is that just a first-order Taylor expansion wearing a hat?
Walk the Euler equation of our CRRA household from its nonlinear form to its linearized form — which terms survive and which are declared second-order small?
If first-order approximations can rank welfare across policies incorrectly, and the zero lower bound is a kink rather than a smooth curve, when does the local polynomial stop being an honest model?
First-order, second-order, or global solution methods — what is actually being traded away at each step?
#long #advanced #english #controversy #debate #quiz #dry #male #parts=5
status: done · id: 015992ac-677a-48d3-83a7-56365cca5a43 · file: is-log-linearizing-around-the-steady.yaml · 2026-09-05
