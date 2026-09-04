# Registerdata i praksis: Python og pandas på NPR, Legemiddelregisteret og HELFO
slug: registerdata-i-praksis-python-og-pandas
enroll: https://drawcast.anvil.app
level: Helsefaglige forskere, analytikere og masterstudenter med litt Python-erfaring (kan løkker og funksjoner), men uten erfaring med store registerdata. Ingen forkunnskaper i epidemiologisk metode utover grunnbegreper.
language: Norsk (bokmål). Kodeord, funksjonsnavn og feilmeldinger vises på engelsk slik de faktisk er.
notation: pandas importeres alltid som pd, numpy som np. De tre datakildene er DataFrames med faste navn: npr (én rad per kontakt/opphold), lmr (én rad per utlevering fra Legemiddelregisteret, tidligere Reseptregisteret) og kuhr (én rad per refusjonskrav fra HELFO/KUHR). Koblingsnøkkelen heter alltid pid (pseudonymt løpenummer). Datokolonner: dato_inn, dato_ut, dato_utlev, dato_krav. Kodekolonner: icd10, atc, takst. Mengder: ddd, antall_pakn. Pasientnivåtabellen som bygges gjennom kurset heter kohort.
example: Ett gjennomgående eksempel: en kohort voksne med type 2-diabetes, definert fra ICD-10 E11 i npr og ATC A10 (særlig A10BA02 metformin) i lmr, med fastlegekontakter fra kuhr. Alle kodesnutter, figurer og feilsøkingseksempler bruker denne kohorten.

Åtte drawcasts om hvordan du faktisk får norske helseregisterdata inn i pandas, koblet sammen, og gjort om til noe du kan svare på et spørsmål med. Vi følger én kohort med type 2-diabetes fra rå fil til ferdig figur — og snakker underveis om hva registrene ikke måler.

---
## Tre registre, tre helt ulike rader — hvor kommer dataene fra?
Hva representerer egentlig én rad i npr, i lmr og i kuhr?
Hvorfor ble alle tre registrene bygget for administrasjon og refusjon, ikke for forskning — og hva gjør det med dataene dine?
Hvorfor er 2007 et vannskille for Norsk pasientregister, og hva skjedde med Reseptregisteret i 2024?
#norwegian #long #why #history #calm #male #parts=4

---
status: done · id: 8a196cd5-0877-46f4-a431-5d1803923f8c · file: tre-registre-tre-helt-ulike-rader-hvor.yaml · 2026-09-04
## Hvordan leser du en 12 GB registerfil uten at maskinen dør?
Hvorfor sprenger pd.read_csv minnet, og hva gjør dtype, category og usecols med regnskapet?
Når lønner det seg å bytte fra CSV til parquet, og hva koster konverteringen?
Hvordan leser du filen i chunks uten å miste pasienter som ligger på tvers av to biter?
#norwegian #long #advanced #quiz #dry #female #parts=4

---
status: done · id: a4f6d22f-9aca-47be-ac10-18872cf0da7a · file: hvordan-leser-du-en-12-gb-registerfil.yaml · 2026-09-04
## Hva er det egentlig som binder en sykehuskontakt til en resept?
Hvorfor er pid og en dato det eneste du har — og hva betyr det for hva du kan spørre om?
Hvorfor blir det plutselig tre ganger så mange rader etter en merge, og hva redder validate= deg fra?
Left join eller inner join: hvordan gir de to ulike kohorter av de samme pasientene?
#norwegian #long #socratic #rich #male #parts=5

---
status: done · id: ca333b32-ddc5-49ce-a9bc-a0bce3f245d5 · file: hva-er-det-egentlig-som-binder-en.yaml · 2026-09-04
## Holder én E11-kode for å kalle noen diabetiker?
Hvordan filtrerer du på ICD-10 og ATC uten å miste undergrupper — str.startswith, isin eller regex?
Hva skjer med kohorten når du krever to kontakter i stedet for én, eller legger til ATC A10 fra lmr?
Hva vinner og hva taper du på en streng kohortdefinisjon?
#norwegian #long #question #proscons #female #parts=4

---
status: done · id: 7da4bcc1-eb26-4f84-9987-459f3f1a26f2 · file: holder-en-e11-kode-for-a-kalle-noen.yaml · 2026-09-04
## Fra hendelser til pasienter: hvordan kollapser du millioner av rader til én rad per person?
Hvordan går du fra én rad per kontakt til én rad per pasient uten å miste det du trenger senere?
Når bruker du groupby().agg(), når transform(), og når pivot_table?
Hvorfor er første og siste dato per pid nesten alltid de to viktigste kolonnene i kohort?
#norwegian #long #qa #quiz #fun #human #male #parts=4

---
status: done · id: 0023e1a7-6d87-4315-9c1f-f1de3712ae32 · file: fra-hendelser-til-pasienter-hvordan.yaml · 2026-09-04
## Tid er alt: washout, ny bruker og legemiddeldekning i pandas
Hva er en washout-periode, og hvorfor avgjør den om pasienten telles som ny bruker?
Hvordan gjør du utleveringsdatoer og DDD om til sammenhengende perioder med legemiddeldekning?
Hvorfor er insidens og prevalens to helt forskjellige spørringer mot det samme datasettet?
Hva gjør merge_asof som en vanlig merge ikke klarer?
#norwegian #verylong #advanced #calm #click #female #parts=5

---
status: done · id: d463d0a3-6d9b-44cf-982a-946c110d7215 · file: tid-er-alt-washout-ny-bruker-og.yaml · 2026-09-04
## Tallene selv: bruk av diabeteslegemidler og kontakter i Norge
Antall brukere av A10-legemidler per år, hentet fra Legemiddelregisterets åpne statistikkbank
Alders- og kjønnsfordeling blant brukerne — hva ser du i pyramiden?
Kontakttyper i NPR: døgnopphold, dagbehandling og poliklinikk side om side
Fra groupby til figur: én tabell, tre plott, med matplotlib rett på pandas-objektet
#norwegian #long #data #facts #rich #male #parts=4

---
status: done · id: fd6ce183-8961-47b6-b8bd-7db6f53e556d · file: tallene-selv-bruk-av-diabeteslegemidler.yaml · 2026-09-04
## Hva registrene ikke måler — og hvorfor analysen din må tåle innsyn
Hvorfor betyr flere registrerte diagnoser og takster ikke nødvendigvis mer sykdom?
Hva er prikking, og hvorfor må celler med få pasienter undertrykkes før du publiserer figuren?
Hvem bestemmer hvem som får koble disse registrene — og hva skjedde egentlig med Helseanalyseplattformen?
Hvorfor er notebooken din en del av metoden, ikke et vedlegg til den?
### Hva registrene faktisk måler
### Personvern, prikking og reproduserbarhet
#norwegian #verylong #provoke #controversy #female #parts=5
status: done · id: de5ea468-bd3c-45df-b169-af3e3bb6a371 · file: hva-registrene-ikke-maler-og-hvorfor.yaml · 2026-09-04
