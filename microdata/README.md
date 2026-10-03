# Doing Data Analysis in microdata.no: A Scripting Course

A ten-lecture, hands-on introduction to the scripting language behind microdata.no, Norway's remote-execution service for register microdata. We build one script from five lines to a full gender-wage-gap analysis, learning imports, collapsing, merging, transformation and disclosure control along the way.

1. [Five lines to your first plot](https://drawcast.app/#gh=hmelberg/dcast/microdata/five-lines-to-your-first-plot.cast)
   - What is the shortest script that produces a real result: a mean, a table and a histogram of wage income by sex?
   - Why does every script have to begin with \`require no.ssb.fdb:... as db\` and \`create-dataset\`?
   - Where does the result appear if you never get to see a single individual's data?
2. [What is actually inside the datastore](https://drawcast.app/#gh=hmelberg/dcast/microdata/what-is-actually-inside-the-datastore.cast)
   - Which registers and which years does the microdata.no datastore cover, and who is the unit of observation?
   - How is a variable described in the metadata catalogue — name, unit type, value labels, time coverage?
   - What the cohort born in 1985 looks like in the data: how many people, and which variables exist for them
3. [Building datasets I: create-dataset and the four shapes of import](https://drawcast.app/#gh=hmelberg/dcast/microdata/building-datasets-i-create-dataset-and.cast)
   - Why does \`import db/BEFOLKNING\_KJOENN as sex\` need no date while \`import db/INNTEKT\_WLONN 2015-01-01 to 2015-12-31 as wage\` needs two?
   - What is the difference between a fixed variable, a status variable measured on a date, an accumulated variable measured over a period and an event variable?
   - What happens to the rows of your dataset the first time you import — and why is the first import the one that defines the population?
4. [Building datasets II: collapse and merge, or how to change the unit of analysis](https://drawcast.app/#gh=hmelberg/dcast/microdata/building-datasets-ii-collapse-and-merge.cast)
   - How do you turn a dataset of persons into a dataset of municipalities with \`collapse (mean) wage, by(kommune)\`?
   - How does \`merge\` put the municipal mean wage back onto every person — and what does microdata do when the key does not match?
   - When should you collapse before merging rather than after, and how do you tell you got it wrong?
5. [Making new variables: generate, replace, recode and labels](https://drawcast.app/#gh=hmelberg/dcast/microdata/making-new-variables-generate-replace.cast)
   - How do you build an education-level variable from the raw NUDB\_BU codes with \`recode\` and \`define-labels\`?
   - Why does \`generate\` fail on a variable that already exists, and when do you need \`replace\` instead?
   - How do conditional expressions (\`if\`) work on a dataset you can never inspect row by row?
6. [Defining the population: keep, drop, and the people who quietly disappear](https://drawcast.app/#gh=hmelberg/dcast/microdata/defining-the-population-keep-drop-and.cast)
   - What is the difference between \`keep if\` on a condition and dropping a variable — and why do beginners confuse them?
   - How do missing values and people who emigrated or died mid-year silently shrink your cohort?
   - Common belief: the register data are complete, so selection is not a problem. Why does the 1985 cohort shrink anyway between import and analysis?
7. [Output that tells the truth: tabulate, summarize, histogram, boxplot, scatter](https://drawcast.app/#gh=hmelberg/dcast/microdata/output-that-tells-the-truth-tabulate.cast)
   - Which command answers which question — when is \`tabulate\` enough and when do you need \`summarize\` or a histogram?
   - What does a boxplot of wage income by sex show that a mean difference hides?
   - Strengths and weaknesses: what can microdata's plotting commands do, and where do you have to export aggregates and plot elsewhere?
8. [Why your output came back censored](https://drawcast.app/#gh=hmelberg/dcast/microdata/why-your-output-came-back-censored.cast)
   - Why does microdata.no refuse to print a cell with very few observations, and what exactly does the service do to your results before you see them?
   - How should you rewrite a script that keeps hitting suppression — coarser categories, larger populations, fewer crossings?
   - The real debate: how much statistical disclosure control can you add before the research answer changes?
9. [Many years at once: panels, event data and the gap over the life cycle](https://drawcast.app/#gh=hmelberg/dcast/microdata/many-years-at-once-panels-event-data-and.cast)
   - How do you import wage income for 2010 through 2022 and end up with a usable panel rather than thirteen unnamed columns?
   - How do event variables (spells with a start and an end) differ from yearly snapshots, and when do you need them?
   - What does the gender wage gap in the 1985 cohort look like from age 25 to age 37, and what does the shape suggest?
10. [The whole script, end to end — and what to do when it breaks](https://drawcast.app/#gh=hmelberg/dcast/microdata/the-whole-script-end-to-end-and-what-to.cast)
   - Can we read the complete gender-wage-gap script from \`require\` to the final regression and say what each block does?
   - What do the most common error messages actually mean, and how do you isolate the failing line?
   - Why pin the datastore version, and what else does a colleague need to reproduce your result a year from now?

---

Made with [drawcast](https://drawcast.app/).
