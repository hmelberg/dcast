# Registerdata i praksis: Python og pandas på NPR, Legemiddelregisteret og HELFO

Åtte drawcasts om hvordan du faktisk får norske helseregisterdata inn i pandas, koblet sammen, og gjort om til noe du kan svare på et spørsmål med. Vi følger én kohort med type 2-diabetes fra rå fil til ferdig figur — og snakker underveis om hva registrene ikke måler.

1. [Tre registre, tre helt ulike rader — hvor kommer dataene fra?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/tre-registre-tre-helt-ulike-rader-hvor.yaml)
   - Hva representerer egentlig én rad i npr, i lmr og i kuhr?
   - Hvorfor ble alle tre registrene bygget for administrasjon og refusjon, ikke for forskning — og hva gjør det med dataene dine?
   - Hvorfor er 2007 et vannskille for Norsk pasientregister, og hva skjedde med Reseptregisteret i 2024?
2. [Hvordan leser du en 12 GB registerfil uten at maskinen dør?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/hvordan-leser-du-en-12-gb-registerfil.yaml)
   - Hvorfor sprenger pd.read\_csv minnet, og hva gjør dtype, category og usecols med regnskapet?
   - Når lønner det seg å bytte fra CSV til parquet, og hva koster konverteringen?
   - Hvordan leser du filen i chunks uten å miste pasienter som ligger på tvers av to biter?
3. [Hva er det egentlig som binder en sykehuskontakt til en resept?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/hva-er-det-egentlig-som-binder-en.yaml)
   - Hvorfor er pid og en dato det eneste du har — og hva betyr det for hva du kan spørre om?
   - Hvorfor blir det plutselig tre ganger så mange rader etter en merge, og hva redder validate= deg fra?
   - Left join eller inner join: hvordan gir de to ulike kohorter av de samme pasientene?
4. [Holder én E11-kode for å kalle noen diabetiker?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/holder-en-e11-kode-for-a-kalle-noen.yaml)
   - Hvordan filtrerer du på ICD-10 og ATC uten å miste undergrupper — str.startswith, isin eller regex?
   - Hva skjer med kohorten når du krever to kontakter i stedet for én, eller legger til ATC A10 fra lmr?
   - Hva vinner og hva taper du på en streng kohortdefinisjon?
5. [Fra hendelser til pasienter: hvordan kollapser du millioner av rader til én rad per person?](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/fra-hendelser-til-pasienter-hvordan.yaml)
   - Hvordan går du fra én rad per kontakt til én rad per pasient uten å miste det du trenger senere?
   - Når bruker du groupby().agg(), når transform(), og når pivot\_table?
   - Hvorfor er første og siste dato per pid nesten alltid de to viktigste kolonnene i kohort?
6. [Tid er alt: washout, ny bruker og legemiddeldekning i pandas](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/tid-er-alt-washout-ny-bruker-og.yaml)
   - Hva er en washout-periode, og hvorfor avgjør den om pasienten telles som ny bruker?
   - Hvordan gjør du utleveringsdatoer og DDD om til sammenhengende perioder med legemiddeldekning?
   - Hvorfor er insidens og prevalens to helt forskjellige spørringer mot det samme datasettet?
   - Hva gjør merge\_asof som en vanlig merge ikke klarer?
7. [Tallene selv: bruk av diabeteslegemidler og kontakter i Norge](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/tallene-selv-bruk-av-diabeteslegemidler.yaml)
   - Antall brukere av A10-legemidler per år, hentet fra Legemiddelregisterets åpne statistikkbank
   - Alders- og kjønnsfordeling blant brukerne — hva ser du i pyramiden?
   - Kontakttyper i NPR: døgnopphold, dagbehandling og poliklinikk side om side
   - Fra groupby til figur: én tabell, tre plott, med matplotlib rett på pandas-objektet
8. [Hva registrene ikke måler — og hvorfor analysen din må tåle innsyn](https://drawcast.app/#gh=hmelberg/dcast/registerdata-i-praksis-python-og-pandas/hva-registrene-ikke-maler-og-hvorfor.yaml)
   - Hvorfor betyr flere registrerte diagnoser og takster ikke nødvendigvis mer sykdom?
   - Hva er prikking, og hvorfor må celler med få pasienter undertrykkes før du publiserer figuren?
   - Hvem bestemmer hvem som får koble disse registrene — og hva skjedde egentlig med Helseanalyseplattformen?
   - Hvorfor er notebooken din en del av metoden, ikke et vedlegg til den?

---

Made with [drawcast](https://drawcast.app/).
