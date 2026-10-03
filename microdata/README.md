# Dataanalyse i microdata.no: et skriptkurs

En praktisk innføring i ti forelesninger i skriptspråket bak microdata.no, tjenesten der du analyserer norske registerdata uten å få dem utlevert. Vi bygger ett skript fra fem linjer til en full analyse av lønnsforskjellen mellom kvinner og menn, og lærer import, aggregering, kobling, omkoding og konfidensialitetstiltak underveis.

1. [Fem linjer til ditt første plott](https://drawcast.app/#gh=hmelberg/dcast/microdata/five-lines-to-your-first-plot.cast)
   - Hva er det korteste skriptet som gir et ekte resultat: et gjennomsnitt, en tabell og et histogram over lønnsinntekt etter kjønn?
   - Hvorfor må hvert skript begynne med \`require no.ssb.fdb:... as db\` og \`create-dataset\`?
   - Hvor dukker resultatet opp når du aldri får se data om ett eneste individ?
2. [Hva som faktisk ligger i databanken](https://drawcast.app/#gh=hmelberg/dcast/microdata/what-is-actually-inside-the-datastore.cast)
   - Hvilke registre og hvilke år dekker databanken i microdata.no, og hvem er enheten?
   - Hvordan beskrives en variabel i variabeloversikten – navn, enhetstype, verdilabler, tidsdekning?
   - Hvordan 1985-kullet ser ut i dataene: hvor mange personer, og hvilke variabler finnes for dem
3. [Å bygge datasett I: create-dataset og de fire typene import](https://drawcast.app/#gh=hmelberg/dcast/microdata/building-datasets-i-create-dataset-and.cast)
   - Hvorfor trenger \`import db/BEFOLKNING\_KJOENN as sex\` ingen dato, mens \`import db/INNTEKT\_WLONN 2015-12-31 as wage\` trenger én – og hvorfor velger den datoen et helt år?
   - Hva er forskjellen på en fast variabel, en tverrsnittsvariabel målt på en dato, en akkumulert variabel summert over et år og en forløpsvariabel?
   - Hva skjer med radene i datasettet første gang du importerer – og hvorfor er det den første importen som bestemmer populasjonen?
4. [Å bygge datasett II: collapse og merge, eller hvordan du bytter analyseenhet](https://drawcast.app/#gh=hmelberg/dcast/microdata/building-datasets-ii-collapse-and-merge.cast)
   - Hvordan gjør du et datasett med personer om til et datasett med kommuner med \`collapse (mean) wage, by(kommune)\`?
   - Hvordan legger \`merge\` kommunens snittlønn tilbake på hver person – og hva gjør microdata når koblingsnøkkelen ikke passer?
   - Når skal du aggregere før du kobler og ikke etter, og hvordan ser du at du har gjort det feil?
5. [Nye variabler: generate, replace, recode og labler](https://drawcast.app/#gh=hmelberg/dcast/microdata/making-new-variables-generate-replace.cast)
   - Hvordan lager du en variabel for utdanningsnivå fra de rå NUDB\_BU-kodene med \`recode\` og \`define-labels\`?
   - Hvorfor feiler \`generate\` på en variabel som allerede finnes, og når trenger du \`replace\` i stedet?
   - Hvordan virker betingelser (\`if\`) på et datasett du aldri kan se på rad for rad?
6. [Å definere populasjonen: keep, drop og folkene som stille forsvinner](https://drawcast.app/#gh=hmelberg/dcast/microdata/defining-the-population-keep-drop-and.cast)
   - Hva er forskjellen på \`keep if\` med en betingelse og å droppe en variabel – og hvorfor blander nybegynnere dem?
   - Hvordan krymper manglende verdier og folk som utvandret eller døde i løpet av året kullet ditt uten at du merker det?
   - Vanlig oppfatning: registerdataene er komplette, så utvalg er ikke noe problem. Hvorfor krymper 1985-kullet likevel mellom import og analyse?
7. [Output som forteller sannheten: tabulate, summarize, histogram, boxplot, hexbin](https://drawcast.app/#gh=hmelberg/dcast/microdata/output-that-tells-the-truth-tabulate.cast)
   - Hvilken kommando svarer på hvilket spørsmål – når holder \`tabulate\`, og når trenger du \`summarize\` eller et histogram?
   - Hva viser et boksplott av lønnsinntekt etter kjønn som en forskjell i gjennomsnitt skjuler?
   - Styrker og svakheter: hva kan plottekommandoene i microdata gjøre, og når må du eksportere aggregater og plotte et annet sted?
8. [Hvorfor resultatet ditt kom tilbake sensurert](https://drawcast.app/#gh=hmelberg/dcast/microdata/why-your-output-came-back-censored.cast)
   - Hvorfor nekter microdata.no å vise tabeller med for mange små celler, og hva gjør tjenesten egentlig med resultatene dine før du ser dem?
   - Hvordan skriver du om et skript som stadig blir stoppet – grovere kategorier, større populasjoner, færre krysninger?
   - Den egentlige debatten: hvor mye konfidensialitetsvern kan du legge på før forskningssvaret endrer seg?
9. [Mange år på en gang: paneldata, forløpsdata og lønnsgapet gjennom livsløpet](https://drawcast.app/#gh=hmelberg/dcast/microdata/many-years-at-once-panels-event-data-and.cast)
   - Hvordan importerer du lønnsinntekt for 2010 til 2022 og ender opp med et brukbart panel i stedet for tretten navnløse kolonner?
   - Hvordan skiller forløpsvariabler (perioder med en start og en slutt) seg fra årlige øyeblikksbilder, og når trenger du dem?
   - Hvordan ser lønnsforskjellen mellom kvinner og menn i 1985-kullet ut fra 25 til 37 år, og hva antyder formen?
10. [Hele skriptet fra start til slutt – og hva du gjør når det stopper](https://drawcast.app/#gh=hmelberg/dcast/microdata/the-whole-script-end-to-end-and-what-to.cast)
   - Kan vi lese hele skriptet om lønnsgapet fra \`require\` til den siste regresjonen og si hva hver blokk gjør?
   - Hva betyr de vanligste feilmeldingene egentlig, og hvordan finner du linjen som feiler?
   - Hvorfor låse databankversjonen, og hva mer trenger en kollega for å gjenskape resultatet ditt om et år?

---

Made with [drawcast](https://drawcast.app/).
