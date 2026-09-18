# Doing Data Analysis in microdata.no: A Scripting Course
slug: microdata
level: Researchers, master and PhD students in social science, economics and epidemiology who have used Stata, R or SPSS but never touched Norwegian register data
language: English narration, with Norwegian variable names from the datastore shown as they really appear
notation: Every script opens with `require no.ssb.fdb:<version> as db`; the datastore alias is always `db`. Datasets are lowercase nouns (`persons`, `income`, `muni`), variable aliases are short English lowercase names (`sex`, `educ`, `wage`, `kommune`), dates are written YYYY-MM-DD, comments start with `//`. Real datastore variables used throughout: BEFOLKNING_KJOENN (sex), BEFOLKNING_FOEDSELS_AAR_MND (birth year-month), BEFOLKNING_KOMMNR_FORMELL (municipality), NUDB_BU (highest completed education), INNTEKT_WLONN (wage income). Teacher should verify exact variable names and datastore version against the current metadata catalogue before recording.
example: The gender gap in wage income: we follow one birth cohort (people born in 1985) and ask how much men and women earn, how the gap varies with education and municipality, and how it opens up over the life cycle. Every lecture adds one more line to the same script.

A ten-lecture, hands-on introduction to the scripting language behind microdata.no, Norway's remote-execution service for register microdata. We build one script from five lines to a full gender-wage-gap analysis, learning imports, collapsing, merging, transformation and disclosure control along the way.

---
## Five lines to your first plot
What is the shortest script that produces a real result: a mean, a table and a histogram of wage income by sex?
Why does every script have to begin with `require no.ssb.fdb:... as db` and `create-dataset`?
Where does the result appear if you never get to see a single individual's data?
#basic #why #long #parts=4 #click #female #calm

---
status: done · id: 4c201ca7-8231-483e-959c-6d858d26ca38 · file: five-lines-to-your-first-plot.yaml · 2026-09-18
## What is actually inside the datastore
Which registers and which years does the microdata.no datastore cover, and who is the unit of observation?
How is a variable described in the metadata catalogue — name, unit type, value labels, time coverage?
What the cohort born in 1985 looks like in the data: how many people, and which variables exist for them
#data #long #parts=4 #facts #male

---
status: done · id: fc81fa2e-fb8a-433d-bc6f-9cd7b6a3289f · file: what-is-actually-inside-the-datastore.yaml · 2026-09-18
## Building datasets I: create-dataset and the four shapes of import
Why does `import db/BEFOLKNING_KJOENN as sex` need no date while `import db/INNTEKT_WLONN 2015-01-01 to 2015-12-31 as wage` needs two?
What is the difference between a fixed variable, a status variable measured on a date, an accumulated variable measured over a period and an event variable?
What happens to the rows of your dataset the first time you import — and why is the first import the one that defines the population?
#long #parts=5 #advanced #quiz #socratic #female

---
status: done · id: c8544de8-fd9c-4e40-9700-2c71fe7db05c · file: building-datasets-i-create-dataset-and.yaml · 2026-09-18
## Building datasets II: collapse and merge, or how to change the unit of analysis
How do you turn a dataset of persons into a dataset of municipalities with `collapse (mean) wage, by(kommune)`?
How does `merge` put the municipal mean wage back onto every person — and what does microdata do when the key does not match?
When should you collapse before merging rather than after, and how do you tell you got it wrong?
#verylong #parts=5 #why #qa #male

---
status: done · id: f9375260-93e9-40b2-9cb8-7404979b4011 · file: building-datasets-ii-collapse-and-merge.yaml · 2026-09-18
## Making new variables: generate, replace, recode and labels
How do you build an education-level variable from the raw NUDB_BU codes with `recode` and `define-labels`?
Why does `generate` fail on a variable that already exists, and when do you need `replace` instead?
How do conditional expressions (`if`) work on a dataset you can never inspect row by row?
#long #parts=4 #fun #female

---
status: done · id: b90d085d-34fd-4287-b290-351618d52642 · file: making-new-variables-generate-replace.yaml · 2026-09-18
## Defining the population: keep, drop, and the people who quietly disappear
What is the difference between `keep if` on a condition and dropping a variable — and why do beginners confuse them?
How do missing values and people who emigrated or died mid-year silently shrink your cohort?
Common belief: the register data are complete, so selection is not a problem. Why does the 1985 cohort shrink anyway between import and analysis?
#long #parts=4 #provoke #quiz #male #rich

---
status: done · id: f45bd95a-2769-49d7-b451-a1fbfd0f7a80 · file: defining-the-population-keep-drop-and.yaml · 2026-09-18
## Output that tells the truth: tabulate, summarize, histogram, boxplot, scatter
Which command answers which question — when is `tabulate` enough and when do you need `summarize` or a histogram?
What does a boxplot of wage income by sex show that a mean difference hides?
Strengths and weaknesses: what can microdata's plotting commands do, and where do you have to export aggregates and plot elsewhere?
#long #parts=4 #proscons #pun #female

---
status: done · id: 9dcea5f6-8000-4bad-8198-8c3af2a908b8 · file: output-that-tells-the-truth-tabulate.yaml · 2026-09-18
## Why your output came back censored
Why does microdata.no refuse to print a cell with very few observations, and what exactly does the service do to your results before you see them?
How should you rewrite a script that keeps hitting suppression — coarser categories, larger populations, fewer crossings?
The real debate: how much statistical disclosure control can you add before the research answer changes?
#long #parts=4 #controversy #history #male #calm

---
status: done · id: 5cf1293a-678d-4b91-a668-f9803479690d · file: why-your-output-came-back-censored.yaml · 2026-09-18
## Many years at once: panels, event data and the gap over the life cycle
How do you import wage income for 2010 through 2022 and end up with a usable panel rather than thirteen unnamed columns?
How do event variables (spells with a start and an end) differ from yearly snapshots, and when do you need them?
What does the gender wage gap in the 1985 cohort look like from age 25 to age 37, and what does the shape suggest?
#verylong #parts=5 #advanced #quiz #facts #female

---
status: done · id: c49f4790-ec98-418a-9357-4765f5348e75 · file: many-years-at-once-panels-event-data-and.yaml · 2026-09-18
## The whole script, end to end — and what to do when it breaks
Can we read the complete gender-wage-gap script from `require` to the final regression and say what each block does?
What do the most common error messages actually mean, and how do you isolate the failing line?
Why pin the datastore version, and what else does a colleague need to reproduce your result a year from now?
### The finished script, block by block
### When the script fails
### Reproducibility and handing it over
#verylong #parts=6 #dry #podcast #male #click
status: done · id: 04c5a16a-af20-4846-90e2-d9f3f3a8c87a · file: the-whole-script-end-to-end-and-what-to.yaml · 2026-09-18
