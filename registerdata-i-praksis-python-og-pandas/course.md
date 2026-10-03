# Register data in practice: Python and pandas on NPR, the Norwegian drug register and HELFO
slug: registerdata-i-praksis-python-og-pandas
enroll: https://drawcast.anvil.app
level: Health researchers, analysts and master's students with some Python (loops and functions), but no experience with large register data. No background in epidemiological method beyond the basic concepts.
language: English. Norwegian register names (NPR, Legemiddelregisteret/LMR, HELFO/KUHR) are kept and explained in English; code, column names, function names and error messages are shown exactly as they are.
notation: pandas is always imported as pd, numpy as np. The three data sources are DataFrames with fixed names: npr (one row per contact/stay in the Norwegian Patient Registry), lmr (one row per pharmacy dispensing in Legemiddelregisteret, the Norwegian drug register, formerly the Prescription Database) and kuhr (one row per reimbursement claim to HELFO, the Norwegian Health Economics Administration, from its KUHR database). The linkage key is always pid (a pseudonymous ID number). Date columns: dato_inn (admission), dato_ut (discharge), dato_utlev (dispensing), dato_krav (claim). Code columns: icd10, atc, takst (fee code). Quantities: ddd (defined daily doses), antall_pakn (number of packs). The patient-level table built through the course is called kohort (the cohort).
example: One running example: a cohort of adults with type 2 diabetes, defined from ICD-10 E11 in npr and ATC A10 (especially A10BA02, metformin) in lmr, with GP contacts from kuhr. Every code snippet, figure and debugging example uses this cohort.

Eight drawcasts on how you actually get Norwegian health register data into pandas, link it, and turn it into something that can answer a question. We follow one cohort with type 2 diabetes from raw file to finished figure — and talk along the way about what the registers don't measure.

---
## Three registers, three very different rows — where does the data come from?
What does one row really represent in npr, in lmr and in kuhr?
Why were all three registers built for administration and reimbursement, not for research — and what does that do to your data?
Why is 2007–2008 a watershed for the Norwegian Patient Registry, and what happened to the Prescription Database in 2022?
#english #long #why #history #calm #male #parts=4

---
status: done · id: 8a196cd5-0877-46f4-a431-5d1803923f8c · file: tre-registre-tre-helt-ulike-rader-hvor.cast · 2026-09-04
## How do you read a 12 GB register file without crashing your machine?
Why does pd.read_csv blow up memory, and what do dtype, category and usecols do to the bill?
When does it pay to switch from CSV to parquet, and what does the conversion cost?
How do you read the file in chunks without losing patients who straddle two chunks?
#english #long #advanced #quiz #dry #female #parts=4

---
status: done · id: a4f6d22f-9aca-47be-ac10-18872cf0da7a · file: hvordan-leser-du-en-12-gb-registerfil.cast · 2026-09-04
## What actually links a hospital contact to a prescription?
Why are pid and a date all you have — and what does that mean for the questions you can ask?
Why are there suddenly three times as many rows after a merge, and what does validate= save you from?
Left join or inner join: how do they give two different cohorts from the same patients?
#english #long #socratic #rich #male #parts=5

---
status: done · id: ca333b32-ddc5-49ce-a9bc-a0bce3f245d5 · file: hva-er-det-egentlig-som-binder-en.cast · 2026-09-04
## Is one E11 code enough to call someone diabetic?
How do you filter on ICD-10 and ATC without losing subgroups — str.startswith, isin or regex?
What happens to the cohort when you require two contacts instead of one, or add ATC A10 from lmr?
What do you gain and lose with a strict cohort definition?
#english #long #question #proscons #female #parts=4

---
status: done · id: 7da4bcc1-eb26-4f84-9987-459f3f1a26f2 · file: holder-en-e11-kode-for-a-kalle-noen.cast · 2026-09-04
## From events to patients: how do you collapse millions of rows into one row per person?
How do you go from one row per contact to one row per patient without losing what you need later?
When do you use groupby().agg(), when transform(), and when pivot_table?
Why are the first and last date per pid almost always the two most important columns in kohort?
#english #long #qa #quiz #fun #human #male #parts=4

---
status: done · id: 0023e1a7-6d87-4315-9c1f-f1de3712ae32 · file: fra-hendelser-til-pasienter-hvordan.cast · 2026-09-04
## Time is everything: washout, new users and drug coverage in pandas
What is a washout period, and why does it decide whether a patient counts as a new user?
How do you turn dispensing dates and DDD into continuous periods of drug coverage?
Why are incidence and prevalence two completely different queries against the same dataset?
What does merge_asof do that an ordinary merge cannot?
#english #verylong #advanced #calm #click #female #parts=5

---
status: done · id: d463d0a3-6d9b-44cf-982a-946c110d7215 · file: tid-er-alt-washout-ny-bruker-og.cast · 2026-09-04
## The numbers themselves: diabetes drug use and contacts in Norway
The number of users of A10 drugs per year, from the drug register's open statistics bank
Age and sex distribution among the users — what do you see in the pyramid?
Contact types in NPR: inpatient stays, day treatment and outpatient visits side by side
From groupby to figure: one table, three plots, with matplotlib straight on the pandas object
#english #long #data #facts #rich #male #parts=4

---
status: done · id: fd6ce183-8961-47b6-b8bd-7db6f53e556d · file: tallene-selv-bruk-av-diabeteslegemidler.cast · 2026-09-04
## What the registers don't measure — and why your analysis must withstand scrutiny
Why do more registered diagnoses and fee codes not necessarily mean more disease?
What is small-cell suppression, and why must cells with few patients be suppressed before you publish the figure?
Who decides who may link these registers — and what really happened to the Health Analytics Platform (Helseanalyseplattformen)?
Why is your notebook part of the method, not an appendix to it?
### What the registers actually measure
### Privacy, small-cell suppression and reproducibility
#english #verylong #provoke #controversy #female #parts=5
status: done · id: de5ea468-bd3c-45df-b169-af3e3bb6a371 · file: hva-registrene-ikke-maler-og-hvorfor.cast · 2026-09-04
