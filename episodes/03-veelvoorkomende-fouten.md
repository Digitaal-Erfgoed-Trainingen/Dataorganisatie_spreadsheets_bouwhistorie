---
title: "Veelvoorkomende fouten"
teaching: 20 # teaching time in minutes
exercises: 0 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- Welke fouten komen vaak voor in spreadsheet data?
- Hoe kun je deze fouten voorkomen of herstellen?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Veelvoorkomende fouten in de opbouw en opmaak van een dataset herkennen
- Veelvoorkomende fouten in de waardes in een cel herkennen
- Per fout een betere manier van vastleggen kiezen

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: instructor

Dit hoofdstuk is vooral een naslagwerk bij de bespreking van de rommelige
dataset `historisch-glas-in-gebouwen_messy.xlsx`. Laat cursisten eerst zelf
fouten zoeken in de dataset en gebruik daarna deze pagina om hun bevindingen
te bespreken. Je hoeft de fouten niet één voor één te behandelen.

In module 2 gaan we verder met relationele datamodellen en databases. Bepaalde best practices die hier aan bod komen, zoals het gebruik van unieke identificatiecodes (UIDs) worden in die module essentieel.

In deze module gebruiken we bewust nog geen vaktermen als *normaalvorm* of *functionele afhankelijkheid*.

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

## Introductie

Een spreadsheet is snel gemaakt, maar dat maakt het nog geen goede dataset.
In dit hoofdstuk bespreken we fouten die vaak voorkomen in spreadsheet data.
De voorbeelden komen uit de dataset
`historisch-glas-in-gebouwen_messy.xlsx`, met waarnemingen van historisch
glas in monumenten. De data staat verdeeld over de tabbladen `voor 1900`,
`Na 1900` en `Datum onbekend`.

We delen de fouten in twee groepen in:

1. **Opbouw en opmaak van de dataset**: hoe de tabel in elkaar zit. Waar
   staan de tabellen, rijen en kolommen, en waar staat de uitleg?
2. **Waardes in de cel**: wat er in een cel staat. Staat er één waarde in, en
   is die overal op dezelfde manier geschreven?

Let op: het probleem zit soms in de cel, terwijl de oplossing in de opbouw
ligt. Een eenheid haal je bijvoorbeeld uit de cel en zet je in de kolomnaam.

::::::::::::::::::::::::::::::::::::: callout

### Een paar begrippen

- **Rij**: één waarneming of één ding dat je beschrijft, bijvoorbeeld één
  ruit in één monument.
- **Kolom**: één eigenschap, bijvoorbeeld de soort glas of de dikte.
- **Cel**: het snijpunt van een rij en een kolom. Bevat één waarde.
- **Unieke Identificatiecode (UID)**: een code waarmee je precies één rij aanwijst, zoals
  een klantnummer of een monumentnummer. In databases heet dit een **key**.
- **Referentielijst**: een vaste lijst met toegestane waarden, zoals een
  lijst van glassoorten.
- **Metadata**: data over je data, zoals wie ze heeft verzameld, wanneer en
  hoe.

::::::::::::::::::::::::::::::::::::::::::::::::
## Opbouw en opmaak van de dataset

### 1. Meerdere tabellen op één werkblad

**Voorbeeld.** Op het werkblad `Na 1900` staan twee tabellen naast elkaar:
*Blank glas* (kolommen B–G) en *Zwart glas* (kolommen I–N), met dezelfde
kolomnamen. Op rij 3 staan `Tuindorp 't Lansink` en `Begraafplaats Soesterweg`
naast elkaar, terwijl die niets met elkaar te maken hebben.

**Waarom is dit een probleem?**

- Waar de ene tabel ophoudt en de andere begint, ziet alleen een mens. Een computer leest elke rij als één waarneming. In dit geval is dat problematisch.
- Of het glas blank of zwart is, staat alleen in de kop boven de tabel. Als je
  de tabellen onder elkaar plakt, ben je die informatie kwijt.

**Wat kun je beter doen?** Kijk eerst of de tabellen over **hetzelfde soort
ding** gaan.

- *Hetzelfde soort ding* (blank en zwart glas zijn allebei glaswaarnemingen):
  zet alles onder elkaar in één tabel en voeg een kolom `glaskleur` toe met
  `blank` of `zwart`.
- *Verschillende dingen* (glaswaarnemingen en een uitleg van glassoorten):
  zet ze elk op een eigen werkblad.

**Wanneer is het geen probleem?** Meerdere tabellen gebruiken is heel normaal:
een lijst van monumenten en een lijst van glaswaarnemingen horen juist apart.
Het gaat mis als tabellen door elkaar op één werkblad staan, of als één
dataset in losse stukken is geknipt.

### 2. Meerdere tabbladen voor dezelfde data

**Voorbeeld.** De glaswaarnemingen staan verdeeld over drie tabbladen:
`voor 1900`, `Na 1900` en `Datum onbekend`. De kolommen zijn niet overal
gelijk: `Mon. nr.` heet op een ander tabblad `Monumentnr`, alleen `voor 1900`
heeft een kolom `Dikte` en `Datum onbekend` heeft geen kolom `Datering`.

**Waarom is dit een probleem?**

- De naam van het tabblad bevat informatie (de periode) die niet in de tabel
  zelf staat. Bij opslaan als CSV ben je die kwijt.
- Wie alles samen wil bekijken, moet de tabbladen eerst samenvoegen. Door de
  verschillende kolommen gaat dat snel mis.
  `voor 1900` of op `Na 1900`?

**Wat kun je beter doen?** Zet alle waarnemingen in één tabel met dezelfde
kolommen. De periode volgt dan vanzelf uit de kolommen met de datering. Gebruik tabbladen alleen voor echt verschillende dingen, zoals
`waarnemingen` en `glassoorten`.

**Wanneer is het geen probleem?** Tabbladen voor verschillende soorten data
of voor uitleg zijn prima. Het probleem is één dataset die over meerdere
tabbladen is verdeeld.

### 3. Opmaak gebruiken om informatie vast te leggen

**Voorbeeld.** In cel J14 van het werkblad `voor 1900` staat
`gele cellen heb ik twijfel over`. Welke waarden onzeker zijn, is alleen te
zien aan de gele achtergrondkleur.

**Waarom is dit een probleem?**

- Software kan kleuren niet of nauwelijks lezen. Bij opslaan als CSV is de
  kleur weg, en daarmee de informatie.
- Je kunt niet filteren of tellen op "alle twijfelgevallen".
- Kleuren zijn niet voor iedereen goed te zien, bijvoorbeeld bij
  kleurenblindheid of een zwart-witprint.

**Wat kun je beter doen?** Maak een extra kolom, zoals `zeker` met `ja` of
`nee`. Wil je de twijfelgevallen toch zien? Gebruik dan voorwaardelijke
opmaak die de kleur uit die kolom haalt.

### 4. Opmaak om de tabel mooi te maken

**Voorbeeld.** Boven de kolomnamen op het werkblad `Na 1900` staan de titels
`Blank glas` en `Zwart glas` in samengevoegde cellen. De kolomnamen beginnen
daardoor pas op rij 2.

**Waarom is dit een probleem?**

- Software verwacht de kolomnamen op de eerste rij. Een titel erboven
  verstoort het inlezen.
- Samengevoegde cellen maken sorteren en filteren onmogelijk of onbetrouwbaar.
  Bij opslaan als CSV staat de waarde maar in één van de cellen.

**Wat kun je beter doen?** Begin het werkblad met precies één rij
kolomnamen. Gebruik geen samengevoegde cellen en geen lege rijen of kolommen
om de tabel op te delen. Wil je de tabel mooi presenteren, maak dan een kopie
en maak die op.

### 5. Metadata en uitleg in de tabel

**Voorbeeld.** Op het werkblad `voor 1900` staat onder de data het blok
`BELANGRIJKE INFORMATIE`, met uitleg over `Mon. Nr.`, `Cilinderglas` en
`ossenoog`. Nergens staat wie de data heeft verzameld, wanneer en hoe.

**Waarom is dit een probleem?**

- De uitleg staat in hetzelfde gebied als de data. Een computer leest de
  uitleg als extra rijen, met `Cilinderglas` in de kolom monumentnummer.
- Zonder metadata kan niemand de data later goed begrijpen, controleren of
  hergebruiken. Ook jijzelf niet, over een paar jaar.

**Wat kun je beter doen?**

- Zet informatie over de dataset (bron, makers, methode, periode, licentie)
  in een **README**: een apart bestand met een naam die duidelijk bij het
  databestand hoort.
- Zet de uitleg van kolommen in een **data dictionary**: een apart tabblad of
  bestand met per kolom de naam, de betekenis, de eenheid en de toegestane
  waarden.
- Gebruik voor de betekenis van waarden een bestaande **referentielijst** of
  thesaurus (zie fout 12).

**Wanneer is het geen probleem?** Uitleg is waardevol. Het gaat alleen om de
plek: buiten de data, op een eigen tabblad of in een eigen bestand.

### 6. Geen Unieke Identificatiecodes per rij

**Voorbeeld.** De verschillende waarnemingen (rijen in de dataset) hebben geen Unieke Identificatiecode (UID). Er is wel de kolom `monumentnummer`. Maar één
monument kan meerdere ruiten hebben, en panden zonder nummer heten `Woonhuis`,
`Winkel` of `Restaurant (nu)`.

**Waarom is dit een probleem?**

- Je kunt nu niet refereren naar één bepaald glaspaneel (één rij in de spreadsheet). Wel naar een monumentnummer, maar voor sommige monumenten zijn meerdere glaspanelen.
- Om dit op te lossen is in de dataset soms een volgnummer aan het
  monumentnummer geplakt (`459758-1`, `459758-2`). Daardoor kun je de kolom
  niet meer koppelen aan het Rijksmonumentenregister.

**Wat kun je beter doen?**

- Geef elke rij een eigen code die **uniek** is, **nooit leeg** is en
  **niet verandert**. Dat kan een simpel volgnummer zijn, bijvoorbeeld
  `GLAS-0001`, `GLAS-0002`, …
- Zet het monumentnummer in een eigen kolom, altijd op dezelfde manier
  geschreven en alleen als getal. Het verwijst naar het monument.
- Gebruik geen namen of omschrijvingen als UID.

## Waardes in de cel

### 7. Opmerkingen in een cel

**Voorbeeld.** De cel wordt gebruikt als post-it: twijfel of een notitie
staat in de waarde zelf, zoals `cilinderglas (?)` en
`19e eeuw (niet 100% zeker)`.

**Waarom is dit een probleem?**

- `cilinderglas (?)` wordt niet meegeteld bij `cilinderglas`: voor de computer
  is het een ander woord.
- Je kunt niet filteren of tellen op "alle twijfelgevallen".

**Wat kun je beter doen?** Leg twijfel vast in een eigen kolom, zoals `zeker`
met `ja` of `nee`. Houd één kolom `opmerking` voor toelichting die je niet
hoeft te tellen of te filteren.

**Wanneer is het geen probleem?** Een opmerkingenkolom is juist handig. Het
wordt pas een probleem als belangrijke gegevens alleen in een opmerking staan.

### 8. Meer dan één gegeven in een cel


**Voorbeeld.** De kolom `Dikte` bevat `0.6-0.8cm`, `6-8mm` en `onbekend`.

**Waarom is dit een probleem?**

- Voor de computer is `6-8mm` tekst, geen getal. Je kunt niet sorteren,
  filteren op "dikker dan 5 mm" of een gemiddelde berekenen.
- Door verschillende eenheden (`cm` en `mm`, of `kg`, `gr.` en `g`) kun je
  waarden niet zomaar vergelijken.

**Wat kun je beter doen?**

- Zet alleen het getal in de cel en de eenheid in de kolomnaam, bijvoorbeeld
  `dikte_mm`. Reken alle waarden om naar die ene eenheid.
- Verdeel een bereik over twee kolommen: `dikte_min_mm` = `6` en
  `dikte_max_mm` = `8`.
- Komen verschillende eenheden echt voor? Gebruik dan een kolom `waarde` met
  alleen getallen en een kolom `eenheid` met een vaste keuzelijst.
- Stel een controle in, zodat alleen getallen kunnen worden ingevoerd (zie [hoofdstuk 4: Kwaliteitscontrole, referentielijsten & publieke thesauri](04-kwaliteitscontrole.md)).

**Wanneer is het geen probleem?** Als je de waarde alleen wilt laten zien en
er nooit mee rekent, is `250 g` minder erg. Maar meestal wil je later toch
vergelijken of tellen, en dan is het makkelijker als het getal al los staat.

### 9. Onbekende en ontbrekende waarden

**Voorbeeld.** In de kolom met monumentnummers staan door elkaar: een lege
cel, `onbekend`, `?` en `-999`.

**Waarom is dit een probleem?**

- Door woorden als `onbekend` of `?` ziet de computer een kolom met getallen
  ineens als tekst. Rekenen en sorteren gaan dan mis.
- Getallen als `-999` lijken echte waarden. Een computer rekent er gewoon
  mee, en verwijst bij `-999` naar een monument dat niet bestaat.
- **Nul is niet hetzelfde als leeg.** "0 ruiten beschadigd" is een
  waarneming; "niet geteld" is iets anders. Vul een gemeten nul dus altijd
  in.

**Wat kun je beter doen?**

- Kies één manier om aan te geven dat een waarde ontbreekt, en schrijf in de
  README welke. Een **lege cel** werkt in de meeste programma's het best.
  Vermijd `0`, `-999`, `N/A`, `onbekend`, `?` en `-`.
- Wil je vastleggen *waarom* iets ontbreekt? Voeg dan een aparte kolom toe,
  zoals `status_monumentnummer`, met een vaste keuze uit `onbekend`,
  `niet van toepassing` of `nog niet opgezocht`.

### 10. Datums die niet overal hetzelfde zijn opgemaakt

**Voorbeeld.** De kolom `Datum aangepast` bevat echte datums naast tekst:
`3 maart 2017`, `2023-10-22`, `mar 2019`, `2025-4-14` en `2025-13-8`.

**Waarom is dit een probleem?**

- Tekst die op een datum lijkt is voor de computer geen datum. Sorteren op
  datum gaat dan mis.
- `04-05-2019` is 4 mei of 5 april, afhankelijk van het land.
- Spreadsheets veranderen invoer soms ongevraagd in een datum. In de dataset
  is het jaartal `1934` veranderd in `1-1-1934`.

**Wat kun je beter doen?** Schrijf datums als `jjjj-mm-dd`, bijvoorbeeld
`2025-08-13`. Dit is de internationale norm (ISO 8601).

### 11. Meerdere dateringsgegevens in één kolom

**Voorbeeld.** De kolom `Datering` bevat `1895`, `1700-1900`, `vóór 1890`,
`begin 17e eeuw/18e eeuw` en `19e eeuw (niet 100% zeker)`.

**Waarom is dit een probleem?**

- In één kolom staan jaartallen, periodes, eeuwen en twijfel door elkaar. Je
  kunt dan niet sorteren of filteren op "alles van vóór 1900".

**Wat kun je beter doen?**

- Leg een datering vast als begin- en eindjaar in twee kolommen:
  `datering_vanaf` = `1801` en `datering_tot` = `1900`. Voeg eventueel een
  kolom toe voor de zekerheid (`zeker`, `waarschijnlijk`, `onzeker`).
- Schrijf in de README welke afspraak je gebruikt, bijvoorbeeld dat
  "19e eeuw" betekent: 1801–1900.

### 12. Vrije woorden voor categorieën

**Voorbeeld.** In de kolom `Soort glas?` staan onder andere `cilinderglas`,
`cilindergas`, `spiegelglas`, `speigelglass`, `gegraveerd` en `ossenoog`.

**Waarom is dit een probleem?**

- **Tikfouten en schrijfvarianten** (`cilindergas`, `speigelglass`) telt de
  computer als aparte soorten.
- **Verschillende soorten informatie** staan in één kolom: een glassoort
  (`cilinderglas`), een bewerking (`gegraveerd`) en zelfs de vorm van een
  raam (`ossenoog`).

**Wat kun je beter doen?** Gebruik een vaste lijst met termen, bij voorkeur
een bestaande thesaurus zoals de
[Cultuurhistorische Thesaurus](https://thesaurus.cultureelerfgoed.nl/) of de
[Getty AAT](https://www.getty.edu/research/tools/vocabularies/aat/), en zet
verschillende soorten informatie in aparte kolommen. Meer hierover staat in
[hoofdstuk 4: Kwaliteitscontrole, referentielijsten & publieke thesauri](04-kwaliteitscontrole.md).

::::::::::::::::::::::::::::::::::::: keypoints 

- Zet één dataset in één doorlopende tabel; gebruik aparte tabellen alleen voor verschillende soorten dingen.
- Leg informatie vast in kolommen, niet in kleur of opmaak.
- Zet uitleg en metadata buiten de data, in een README of data dictionary.
- Geef elke rij een Unieke Identificatiecode die nooit leeg is en niet verandert.
- Zet één gegeven per cel: getallen zonder eenheid, lijstjes op aparte rijen en datums als `jjjj-mm-dd`.
- Kies één manier voor ontbrekende waarden.
- Gebruik een referentielijst of thesaurus voor categorieën.

::::::::::::::::::::::::::::::::::::::::::::::::

*Dit hoofdstuk is gedeeltelijk gebaseerd op
[Formatting problems](https://datacarpentry.github.io/spreadsheet-ecology-lesson/02-common-mistakes.html)
uit de Data Carpentry-les* Data Organization in Spreadsheets for Ecologists
*(CC BY 4.0).*
