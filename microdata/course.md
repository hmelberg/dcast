# Dataanalyse i microdata.no: et skriptkurs
slug: microdata
level: Forskere, master- og ph.d.-studenter i samfunnsfag, økonomi og epidemiologi som har brukt Stata, R eller SPSS, men aldri har jobbet med norske registerdata
language: Norsk (bokmål), med variabelnavnene fra databanken vist slik de faktisk ser ut
notation: Hvert skript begynner med `require no.ssb.fdb:<versjon> as db`; databankens alias er alltid `db`. Datasett har korte navn med små bokstaver (`persons`, `income`, `muni`), variabelaliasene er korte engelske navn (`sex`, `educ`, `wage`, `kommune`), datoer skrives ÅÅÅÅ-MM-DD, kommentarer begynner med `//`. Ekte registervariabler som brukes gjennom kurset: BEFOLKNING_KJOENN (kjønn), BEFOLKNING_FOEDSELS_AAR_MND (fødselsår og -måned, numerisk ÅÅÅÅMM), BEFOLKNING_KOMMNR_FORMELL (bostedskommune), NUDB_BU (høyeste fullførte utdanning, NUS-kode), INNTEKT_WLONN (lønnsinntekt, akkumulert per år). Sjekk variabelnavn og databankversjon mot variabeloversikten før du kjører.
example: Lønnsforskjellen mellom kvinner og menn: vi følger ett fødselskull (de som er født i 1985) og spør hvor mye menn og kvinner tjener, hvordan forskjellen varierer med utdanning og kommune, og hvordan den åpner seg gjennom livsløpet. Hver forelesning legger til en linje i det samme skriptet.

En praktisk innføring i ti forelesninger i skriptspråket bak microdata.no, tjenesten der du analyserer norske registerdata uten å få dem utlevert. Vi bygger ett skript fra fem linjer til en full analyse av lønnsforskjellen mellom kvinner og menn, og lærer import, aggregering, kobling, omkoding og konfidensialitetstiltak underveis.

---
## Fem linjer til ditt første plott
Hva er det korteste skriptet som gir et ekte resultat: et gjennomsnitt, en tabell og et histogram over lønnsinntekt etter kjønn?
Hvorfor må hvert skript begynne med `require no.ssb.fdb:... as db` og `create-dataset`?
Hvor dukker resultatet opp når du aldri får se data om ett eneste individ?
#basic #why #long #parts=4 #click #female #calm

---
status: done · id: 4c201ca7-8231-483e-959c-6d858d26ca38 · file: five-lines-to-your-first-plot.cast · 2026-09-18
## Hva som faktisk ligger i databanken
Hvilke registre og hvilke år dekker databanken i microdata.no, og hvem er enheten?
Hvordan beskrives en variabel i variabeloversikten – navn, enhetstype, verdilabler, tidsdekning?
Hvordan 1985-kullet ser ut i dataene: hvor mange personer, og hvilke variabler finnes for dem
#data #long #parts=4 #facts #male

---
status: done · id: fc81fa2e-fb8a-433d-bc6f-9cd7b6a3289f · file: what-is-actually-inside-the-datastore.cast · 2026-09-18
## Å bygge datasett I: create-dataset og de fire typene import
Hvorfor trenger `import db/BEFOLKNING_KJOENN as sex` ingen dato, mens `import db/INNTEKT_WLONN 2015-12-31 as wage` trenger én – og hvorfor velger den datoen et helt år?
Hva er forskjellen på en fast variabel, en tverrsnittsvariabel målt på en dato, en akkumulert variabel summert over et år og en forløpsvariabel?
Hva skjer med radene i datasettet første gang du importerer – og hvorfor er det den første importen som bestemmer populasjonen?
#long #parts=5 #advanced #quiz #socratic #female

---
status: done · id: c8544de8-fd9c-4e40-9700-2c71fe7db05c · file: building-datasets-i-create-dataset-and.cast · 2026-09-18
## Å bygge datasett II: collapse og merge, eller hvordan du bytter analyseenhet
Hvordan gjør du et datasett med personer om til et datasett med kommuner med `collapse (mean) wage, by(kommune)`?
Hvordan legger `merge` kommunens snittlønn tilbake på hver person – og hva gjør microdata når koblingsnøkkelen ikke passer?
Når skal du aggregere før du kobler og ikke etter, og hvordan ser du at du har gjort det feil?
#verylong #parts=5 #why #qa #male

---
status: done · id: f9375260-93e9-40b2-9cb8-7404979b4011 · file: building-datasets-ii-collapse-and-merge.cast · 2026-09-18
## Nye variabler: generate, replace, recode og labler
Hvordan lager du en variabel for utdanningsnivå fra de rå NUDB_BU-kodene med `recode` og `define-labels`?
Hvorfor feiler `generate` på en variabel som allerede finnes, og når trenger du `replace` i stedet?
Hvordan virker betingelser (`if`) på et datasett du aldri kan se på rad for rad?
#long #parts=4 #fun #female

---
status: done · id: b90d085d-34fd-4287-b290-351618d52642 · file: making-new-variables-generate-replace.cast · 2026-09-18
## Å definere populasjonen: keep, drop og folkene som stille forsvinner
Hva er forskjellen på `keep if` med en betingelse og å droppe en variabel – og hvorfor blander nybegynnere dem?
Hvordan krymper manglende verdier og folk som utvandret eller døde i løpet av året kullet ditt uten at du merker det?
Vanlig oppfatning: registerdataene er komplette, så utvalg er ikke noe problem. Hvorfor krymper 1985-kullet likevel mellom import og analyse?
#long #parts=4 #provoke #quiz #male #rich

---
status: done · id: f45bd95a-2769-49d7-b451-a1fbfd0f7a80 · file: defining-the-population-keep-drop-and.cast · 2026-09-18
## Output som forteller sannheten: tabulate, summarize, histogram, boxplot, hexbin
Hvilken kommando svarer på hvilket spørsmål – når holder `tabulate`, og når trenger du `summarize` eller et histogram?
Hva viser et boksplott av lønnsinntekt etter kjønn som en forskjell i gjennomsnitt skjuler?
Styrker og svakheter: hva kan plottekommandoene i microdata gjøre, og når må du eksportere aggregater og plotte et annet sted?
#long #parts=4 #proscons #pun #female

---
status: done · id: 9dcea5f6-8000-4bad-8198-8c3af2a908b8 · file: output-that-tells-the-truth-tabulate.cast · 2026-09-18
## Hvorfor resultatet ditt kom tilbake sensurert
Hvorfor nekter microdata.no å vise tabeller med for mange små celler, og hva gjør tjenesten egentlig med resultatene dine før du ser dem?
Hvordan skriver du om et skript som stadig blir stoppet – grovere kategorier, større populasjoner, færre krysninger?
Den egentlige debatten: hvor mye konfidensialitetsvern kan du legge på før forskningssvaret endrer seg?
#long #parts=4 #controversy #history #male #calm

---
status: done · id: 5cf1293a-678d-4b91-a668-f9803479690d · file: why-your-output-came-back-censored.cast · 2026-09-18
## Mange år på en gang: paneldata, forløpsdata og lønnsgapet gjennom livsløpet
Hvordan importerer du lønnsinntekt for 2010 til 2022 og ender opp med et brukbart panel i stedet for tretten navnløse kolonner?
Hvordan skiller forløpsvariabler (perioder med en start og en slutt) seg fra årlige øyeblikksbilder, og når trenger du dem?
Hvordan ser lønnsforskjellen mellom kvinner og menn i 1985-kullet ut fra 25 til 37 år, og hva antyder formen?
#verylong #parts=5 #advanced #quiz #facts #female

---
status: done · id: c49f4790-ec98-418a-9357-4765f5348e75 · file: many-years-at-once-panels-event-data-and.cast · 2026-09-18
## Hele skriptet fra start til slutt – og hva du gjør når det stopper
Kan vi lese hele skriptet om lønnsgapet fra `require` til den siste regresjonen og si hva hver blokk gjør?
Hva betyr de vanligste feilmeldingene egentlig, og hvordan finner du linjen som feiler?
Hvorfor låse databankversjonen, og hva mer trenger en kollega for å gjenskape resultatet ditt om et år?
### Det ferdige skriptet, blokk for blokk
### Når skriptet feiler
### Etterprøvbarhet og overlevering
#verylong #parts=6 #dry #podcast #male #click
status: done · id: 04c5a16a-af20-4846-90e2-d9f3f3a8c87a · file: the-whole-script-end-to-end-and-what-to.cast · 2026-09-18
