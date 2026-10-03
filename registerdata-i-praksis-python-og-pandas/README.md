# Register data in practice: Python and pandas on NPR, the Norwegian drug register and HELFO

Eight drawcasts on how you actually get Norwegian health register data into pandas, link it, and turn it into something that can answer a question. We follow one cohort with type 2 diabetes from raw file to finished figure — and talk along the way about what the registers don't measure.

1. [Three registers, three very different rows — where does the data come from?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/tre-registre-tre-helt-ulike-rader-hvor.cast)
   - What does one row really represent in npr, in lmr and in kuhr?
   - Why were all three registers built for administration and reimbursement, not for research — and what does that do to your data?
   - Why is 2007–2008 a watershed for the Norwegian Patient Registry, and what happened to the Prescription Database in 2022?
2. [How do you read a 12 GB register file without crashing your machine?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/hvordan-leser-du-en-12-gb-registerfil.cast)
   - Why does pd.read\_csv blow up memory, and what do dtype, category and usecols do to the bill?
   - When does it pay to switch from CSV to parquet, and what does the conversion cost?
   - How do you read the file in chunks without losing patients who straddle two chunks?
3. [What actually links a hospital contact to a prescription?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/hva-er-det-egentlig-som-binder-en.cast)
   - Why are pid and a date all you have — and what does that mean for the questions you can ask?
   - Why are there suddenly three times as many rows after a merge, and what does validate= save you from?
   - Left join or inner join: how do they give two different cohorts from the same patients?
4. [Is one E11 code enough to call someone diabetic?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/holder-en-e11-kode-for-a-kalle-noen.cast)
   - How do you filter on ICD-10 and ATC without losing subgroups — str.startswith, isin or regex?
   - What happens to the cohort when you require two contacts instead of one, or add ATC A10 from lmr?
   - What do you gain and lose with a strict cohort definition?
5. [From events to patients: how do you collapse millions of rows into one row per person?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/fra-hendelser-til-pasienter-hvordan.cast)
   - How do you go from one row per contact to one row per patient without losing what you need later?
   - When do you use groupby().agg(), when transform(), and when pivot\_table?
   - Why are the first and last date per pid almost always the two most important columns in kohort?
6. [Time is everything: washout, new users and drug coverage in pandas](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/tid-er-alt-washout-ny-bruker-og.cast)
   - What is a washout period, and why does it decide whether a patient counts as a new user?
   - How do you turn dispensing dates and DDD into continuous periods of drug coverage?
   - Why are incidence and prevalence two completely different queries against the same dataset?
   - What does merge\_asof do that an ordinary merge cannot?
7. [The numbers themselves: diabetes drug use and contacts in Norway](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/tallene-selv-bruk-av-diabeteslegemidler.cast)
   - The number of users of A10 drugs per year, from the drug register's open statistics bank
   - Age and sex distribution among the users — what do you see in the pyramid?
   - Contact types in NPR: inpatient stays, day treatment and outpatient visits side by side
   - From groupby to figure: one table, three plots, with matplotlib straight on the pandas object
8. [What the registers don't measure — and why your analysis must withstand scrutiny](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/hva-registrene-ikke-maler-og-hvorfor.cast)
   - Why do more registered diagnoses and fee codes not necessarily mean more disease?
   - What is small-cell suppression, and why must cells with few patients be suppressed before you publish the figure?
   - Who decides who may link these registers — and what really happened to the Health Analytics Platform (Helseanalyseplattformen)?
   - Why is your notebook part of the method, not an appendix to it?

---

Made with [drawcast](https://drawcast.app/).
