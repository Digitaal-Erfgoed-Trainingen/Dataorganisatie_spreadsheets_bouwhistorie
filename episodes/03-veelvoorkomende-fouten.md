---
title: "Veelvoorkomende fouten"
teaching: 30 # teaching time in minutes
exercises: 20 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 

- Welke fouten komen vaak voor in gegevens in spreadsheets?
- Hoe herken je of een fout gaat over de opbouw van de tabel, over de leesbaarheid voor de computer of over de betekenis van de gegevens?
- Hoe kun je deze fouten voorkomen of herstellen?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Overzicht van de veelvoorkomende fouten in tabulaire data
- Fouten herkennen en indelen aan de hand van drie hoofdvragen
- Per fout een betere manier van vastleggen kiezen

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: instructor

Deze aflevering is vooral een naslagwerk bij de bespreking van de rommelige
dataset `historisch-glas-in-gebouwen_messy.xlsx`. Laat cursisten eerst zelf
fouten zoeken in de dataset en gebruik daarna deze pagina om hun bevindingen
in te delen. Je hoeft de tien problemen niet één voor één te behandelen.

De indeling in drie hoofdvragen komt terug in les twee. Daar worden de
problemen bij hoofdvraag 1 (opbouw van de tabel) verder uitgewerkt met
relationeel datamodelleren en normalisatie. In deze les gebruiken we bewust
geen vaktermen als *normaalvorm* of *functionele afhankelijkheid*.

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

## Introductie

Een spreadsheet is snel gemaakt, maar dat maakt het nog geen goede dataset.
In deze aflevering bespreken we tien fouten die vaak voorkomen in tabellen.
De voorbeelden komen uit de dataset
`historisch-glas-in-gebouwen_messy.xlsx`, met waarnemingen van historisch
glas in monumenten. De gegevens staan verdeeld over de werkbladen
`voor 1900`, `Na 1900` en `Datum onbekend`.

Bij elke fout kun je jezelf drie vragen stellen:

1. **Is de tabel goed opgebouwd?**
   Staat elk onderwerp in een eigen tabel? Heeft elke rij een eigen unieke
   code? Staat dezelfde informatie niet op meerdere plekken?
2. **Kan een computer de gegevens goed lezen?**
   Zijn getallen echt getallen en datums echt datums? Is duidelijk waar de
   tabel begint en eindigt? Is overal hetzelfde gedaan als een waarde
   ontbreekt?
3. **Is de betekenis duidelijk en vastgelegd?**
   Weet iemand anders over vijf jaar nog wat een kolom, een code of een
   afkorting betekent? Worden overal dezelfde woorden gebruikt?

Een fout kan bij meer dan één vraag horen. Een tabel kan ook op het ene punt
goed zijn en op het andere niet: hij kan bijvoorbeeld netjes opgebouwd zijn
maar toch datums bevatten die de computer niet begrijpt.

::::::::::::::::::::::::::::::::::::: callout

### Een paar begrippen

- **Rij**: één waarneming of één ding dat je beschrijft, bijvoorbeeld één
  ruit in één monument.
- **Kolom**: één eigenschap, bijvoorbeeld de soort glas of de dikte.
- **Cel**: het snijpunt van een rij en een kolom. Bevat één waarde.
- **Unieke code (ID)**: een code waarmee je precies één rij aanwijst, zoals
  een klantnummer of een monumentnummer. In databases heet dit een
  *sleutel*.
- **Referentielijst**: een vaste lijst met toegestane waarden, zoals een
  lijst van glassoorten.
- **Metadata**: gegevens over je gegevens, zoals wie ze heeft verzameld,
  wanneer en hoe.

::::::::::::::::::::::::::::::::::::::::::::::::

## Overzicht

In de tabel staat per fout bij welke hoofdvragen hij hoort.
**●** = hoort vooral hierbij, **○** = speelt ook mee, **–** = speelt meestal geen rol.

| # | Fout | 1. Opbouw | 2. Leesbaar voor computer | 3. Betekenis | In het kort |
|---|------|:---------:|:-----------:|:-----------:|-------------|
| 1 | Meerdere tabellen op één werkblad | ● | ○ | – | Eén tabel per werkblad; gegevens van hetzelfde soort onder elkaar. |
| 2 | Meerdere tabbladen voor dezelfde gegevens | ○ | ● | ○ | Zet alles in één tabel en voeg een kolom toe. |
| 3 | Opmerkingen in de tabel | ○ | ● | ○ | Belangrijke gegevens in een eigen kolom, toelichting in een opmerkingenkolom. |
| 4 | Een legenda tussen de gegevens | ○ | ● | ○ | Zet uitleg op een apart tabblad of in een apart bestand. |
| 5 | Metadata in de tabel | ○ | ○ | ● | Zet informatie over de dataset in een apart leesmij-bestand. |
| 6 | Onbekende en ontbrekende waarden | – | ● | ○ | Kies één manier, bij voorkeur een lege cel, en leg de reden apart vast. |
| 7 | Unieke codes (ID's) | ● | ○ | ○ | Elke rij een eigen, unieke code die nooit leeg is. |
| 8 | Getal en eenheid in één cel | ○ | ● | ○ | Alleen het getal in de cel, de eenheid in de kolomnaam. |
| 9 | Datums die niet overal hetzelfde zijn | ○ | ● | ○ | Eén notatie, bij voorkeur `jjjj-mm-dd`. |
| 10 | Vrije woorden voor categorieën | ○ | ○ | ● | Gebruik een vaste lijst met termen of een thesaurus. |

## 1. Meerdere tabellen op één werkblad

**Hoort vooral bij:** opbouw. **Ook:** leesbaar voor computer.

**Voorbeeld.** Op het werkblad `Na 1900` staan twee tabellen naast elkaar:
*Blank glas* (kolommen B–G) en *Zwart glas* (kolommen I–N), met dezelfde
kolomnamen. Op rij 3 staan `Tuindorp 't Lansink` en `Begraafplaats Soesterweg`
naast elkaar, terwijl die niets met elkaar te maken hebben. Op het werkblad
`voor 1900` staat ook nog een blok `BELANGRIJKE INFORMATIE` onder de gegevens.

**Waarom is dit een probleem?**

- Een computer leest elke rij als één waarneming. Door twee tabellen naast
  elkaar lijkt het alsof `Datum aangepast` in kolom A ook bij het zwarte glas
  hoort.
- Waar de ene tabel ophoudt en de andere begint, ziet alleen een mens.
  Software ziet één grote tabel met lege kolommen.
- Kolomnamen komen dubbel voor (`Pand`, `Monumentnr`).
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

## 2. Meerdere tabbladen voor dezelfde gegevens

**Hoort vooral bij:** leesbaar voor computer. **Ook:** opbouw en betekenis.

**Voorbeeld.** De glaswaarnemingen staan verdeeld over drie tabbladen:
`voor 1900`, `Na 1900` en `Datum onbekend`. De kolommen zijn niet overal
gelijk: `Mon. nr.` heet op een ander tabblad `Monumentnr`, alleen `voor 1900`
heeft een kolom `Dikte` en `Datum onbekend` heeft geen kolom `Datering`.

**Waarom is dit een probleem?**

- De naam van het tabblad bevat informatie (de periode) die niet in de tabel
  zelf staat. Bij opslaan als CSV ben je die kwijt.
- Wie alles samen wil bekijken, moet de tabbladen eerst samenvoegen. Door de
  verschillende kolommen gaat dat snel mis.
- Het is niet altijd duidelijk waar iets hoort: komt glas uit precies 1900 op
  `voor 1900` of op `Na 1900`?
- Als iemand een datering verbetert, moet de rij ook naar een ander tabblad.
  Dat wordt vaak vergeten.

**Wat kun je beter doen?** Zet alle waarnemingen in één tabel met dezelfde
kolommen. De periode volgt dan vanzelf uit de kolom met de datering
(zie fout 9). Gebruik tabbladen alleen voor echt verschillende dingen, zoals
`waarnemingen` en `glassoorten`, en beschrijf in een tabblad `leesmij` wat
elk tabblad bevat.

**Wanneer is het geen probleem?** Tabbladen voor verschillende soorten
gegevens of voor uitleg zijn prima. Het probleem is één dataset die over
meerdere tabbladen is verdeeld.

## 3. Opmerkingen in de tabel

**Hoort vooral bij:** leesbaar voor computer. **Ook:** opbouw en betekenis.

**Voorbeeld.**

- In de kolom `Details_01` staat
  `mat gemaakt glas, ontwerp Carl Lion Cachet, uitvoering Fa. Koelewijn`.
  Daar zitten drie gegevens in: een bewerking, een ontwerper en een
  uitvoerder.
- `platen pakweg 2x4 meter; minieme belletjes te zien` bevat afmetingen én
  een waarneming.
- Twijfel staat in de waarde zelf: `cilinderglas (?)`,
  `19e eeuw (niet 100% zeker)`.
- In cel J14 staat `gele cellen heb ik twijfel over`. De twijfel zelf is
  alleen zichtbaar als gele achtergrondkleur.
- Notities die je aan een cel hangt (*opmerkingen* in Excel) verdwijnen als
  je het bestand als CSV opslaat.

**Waarom is dit een probleem?**

- Software kan opmerkingen bij cellen en kleuren niet of nauwelijks lezen.
- Gegevens waarop je wilt zoeken of tellen, zoals "alle ruiten van Lion
  Cachet" of "alle twijfelgevallen", zitten verstopt in vrije tekst.
- `cilinderglas (?)` wordt niet meegeteld bij `cilinderglas`: voor de computer
  is het een ander woord.

**Wat kun je beter doen?**

- Geef belangrijke gegevens een eigen kolom, zoals `ontwerper`, `uitvoerder`,
  `breedte_m` en `hoogte_m`.
- Leg twijfel vast in een eigen kolom, zoals `zeker` met `ja` of `nee`, in
  plaats van met een vraagteken of een kleur.
- Houd één kolom `opmerking` voor toelichting die je niet hoeft te tellen of
  te filteren.

**Wanneer is het geen probleem?** Een opmerkingenkolom is juist handig. Het
wordt pas een probleem als belangrijke gegevens alleen in een opmerking, een
celnotitie of een kleur staan.

## 4. Een legenda tussen de gegevens

**Hoort vooral bij:** leesbaar voor computer. **Ook:** opbouw en betekenis.

**Voorbeeld.** Op het werkblad `voor 1900` staat onder de gegevens het blok
`BELANGRIJKE INFORMATIE`, met uitleg over `Mon. Nr.`, `Cilinderglas` en
`ossenoog`. In cel J14 staat uitgelegd wat de gele kleur betekent.

**Waarom is dit een probleem?**

- De uitleg staat in hetzelfde gebied als de gegevens. Een computer leest de
  uitleg als extra rijen, met `Cilinderglas` in de kolom monumentnummer.
- De legenda haalt twee soorten uitleg door elkaar: wat een **kolom** betekent
  (`Mon. Nr.`) en wat een **waarde** betekent (`Cilinderglas`).
- De legenda is onvolledig: de meeste glassoorten worden niet uitgelegd.

**Wat kun je beter doen?**

- Zet de uitleg van kolommen in een **gegevenswoordenboek**: een apart
  tabblad of bestand met per kolom de naam, de betekenis, de eenheid en
  de toegestane waarden.
- Zet de uitleg van waarden in een **referentielijst** met per term een
  omschrijving (zie fout 10).
- Gebruik geen kleur om iets vast te leggen, maar een kolom.

**Wanneer is het geen probleem?** Een legenda is waardevol. Het gaat alleen
om de plek: buiten de gegevens, op een eigen tabblad of in een eigen bestand.

## 5. Metadata in de tabel

**Hoort vooral bij:** betekenis. **Ook:** opbouw en leesbaar voor computer.

**Voorbeeld.**

- Boven de kolomnamen staat een titel (`Blank glas`) in samengevoegde cellen.
  De kolomnamen beginnen daardoor pas op rij 2.
- Nergens staat wie de gegevens heeft verzameld, wanneer en hoe. Ook is niet
  duidelijk wat `Datum aangepast` betekent: aangepast in de spreadsheet, of
  aan het gebouw?
- `[register]` in een opmerking verwijst naar een bron, maar zegt niet welke.
- De naam van het pand staat bij elke waarneming opnieuw, ook als een monument
  vaker voorkomt (`Jachthuis Sint Hubertus`, 530191).

**Waarom is dit een probleem?**

- Software verwacht de kolomnamen op de eerste rij. Een titel erboven
  verstoort het inlezen.
- Zonder metadata kan niemand de gegevens later goed begrijpen, controleren of
  hergebruiken. Ook jijzelf niet, over een paar jaar.
- Als dezelfde informatie (zoals de pandnaam) op veel rijen herhaald wordt,
  sluipen er verschillen in: hetzelfde monument kan op twee rijen een andere
  naam krijgen. Welke is dan juist?

**Wat kun je beter doen?**

- Zet informatie over de dataset (bron, makers, methode, periode, licentie,
  eenheden, uitleg van begrippen) in een apart **leesmij-bestand**
  (*README*) met een naam die duidelijk bij het gegevensbestand hoort.
- Begin het werkblad met precies één rij kolomnamen.
- Informatie over een monument (zoals de naam) hoort bij het monument, niet
  bij elke waarneming. Je kunt een aparte tabel `monumenten` maken en in de
  waarnemingen alleen het monumentnummer noemen.

::::::::::::::::::::::::::::::::::::: callout

### Vooruitblik

Het idee dat elk gegeven op precies één plek hoort te staan, werken we in les
twee verder uit. Daar leer je hoe je een dataset stap voor stap opsplitst in
tabellen die naar elkaar verwijzen.

::::::::::::::::::::::::::::::::::::::::::::::::

## 6. Onbekende en ontbrekende waarden

**Hoort vooral bij:** leesbaar voor computer. **Ook:** betekenis.

**Voorbeeld.** In de kolom met monumentnummers staan door elkaar: een lege
cel, `onbekend`, `?` en `-999`. In de kolom `Dikte` staat `onbekend`. In
`Details_01` staat een cel met alleen een spatie.

**Waarom is dit een probleem?**

- Door woorden als `onbekend` of `?` ziet de computer een kolom met getallen
  ineens als tekst. Rekenen en sorteren gaan dan mis.
- Getallen als `-999`, `99999` of `-9999` lijken echte waarden. Een computer
  rekent er gewoon mee, en verwijst bij `-999` naar een monument dat niet
  bestaat.
- Een cel met een spatie lijkt leeg, maar is het niet.
- **Nul is niet hetzelfde als leeg.** "0 ruiten beschadigd" is een
  waarneming; "niet geteld" is iets anders. Vul een gemeten nul dus altijd
  in.
- "Ontbreekt" kan veel betekenen: niet gemeten, onbekend, niet van toepassing
  (het pand is geen rijksmonument), nog niet opgezocht, of bewust niet
  gedeeld.

**Wat kun je beter doen?**

- Kies één manier om aan te geven dat een waarde ontbreekt, en schrijf op
  welke. Een **lege cel** werkt in de meeste programma's het best. Vermijd
  `0`, `-999`, `N/A`, `onbekend`, `?` en `-`.
- Wil je vastleggen *waarom* iets ontbreekt? Voeg dan een aparte kolom toe,
  zoals `status_monumentnummer`, met een vaste keuze uit `onbekend`,
  `niet van toepassing` of `nog niet opgezocht`.
- Haal spaties uit cellen die leeg horen te zijn.

## 7. Unieke codes (ID's)

**Hoort vooral bij:** opbouw. **Ook:** leesbaar voor computer en betekenis.

**Voorbeeld.**

- De kolom heet op het ene tabblad `Mon. nr.` en op het andere `Monumentnr`.
- Er staan getallen in (`32139`), tekst (`459758-1`, `459758-2`) en
  ontbrekende waarden (`onbekend`, `?`, `-999`, leeg).
- `Jachthuis Sint Hubertus` (530191) komt twee keer voor, met twee soorten
  glas.
- Panden zonder nummer heten `Woonhuis`, `Winkel` of `Restaurant (nu)`. Er
  zijn duizenden woonhuizen, dus zo'n naam wijst niet één pand aan.

**Waarom is dit een probleem?**

- Het monumentnummer wijst een **monument** aan, niet een **waarneming**. Eén
  monument kan meerdere ruiten hebben. Er is dus geen kolom waarmee je precies
  één rij kunt aanwijzen, en dubbele invoer valt niet op.
- `459758-1` bestaat uit twee gegevens: het monumentnummer en een volgnummer.
  Daardoor kun je de kolom niet meer koppelen aan het
  Rijksmonumentenregister.
- Als hetzelfde nummer op verschillende manieren is geschreven (`32139`,
  `032139`), herkent de computer het niet als hetzelfde nummer.

**Wat kun je beter doen?**

- Geef elke rij een eigen code die **uniek** is, **nooit leeg** is en
  **niet verandert**. Dat kan een simpel volgnummer zijn, bijvoorbeeld
  `GLAS-0001`, `GLAS-0002`, …
- Zet het monumentnummer in een eigen kolom, altijd op dezelfde manier
  geschreven en alleen als getal. Het verwijst naar het monument.
- Splits samengestelde codes: `459758-1` wordt `monumentnummer` = `459758` en
  `volgnummer` = `1`.
- Gebruik geen namen of omschrijvingen als unieke code.

::::::::::::::::::::::::::::::::::::: challenge 

## Opdracht 1: wat staat er dubbel?

Een collega maakt de volgende tabel.

| monumentnummer | volgnummer | pandnaam | gemeente | provincie | glassoort |
|---|---|---|---|---|---|
| 459758 | 1 | Koninklijke Verzamelingen | Den Haag | Zuid-Holland | cilinderglas |
| 459758 | 2 | Koninklijke Verzamelingen | Den Haag | Zuid-Holland | spiegelglas |
| 530191 | 1 | Jachthuis Sint Hubertus | Apeldoorn | Gelderland | spiegelglas |
| 530191 | 2 | Jachthuis Sint Hubertus | Apeldoorn | Gelderland | prismategel |

1. Welke informatie wordt herhaald?
2. Wat gaat er mis als het Jachthuis een nieuwe naam krijgt en iemand die maar
   op één rij aanpast?
3. Hoe zou je deze gegevens over meerdere tabellen verdelen?

:::::::::::::::::::::::: solution 

1. `pandnaam`, `gemeente` en `provincie` worden voor elk monument herhaald.
   Ze horen bij het monument, niet bij de ruit. `provincie` hoort eigenlijk
   zelfs bij de gemeente.
2. Dan heeft hetzelfde monument twee verschillende namen en weet niemand meer
   welke klopt.
3. Bijvoorbeeld:
   - een tabel `glaswaarnemingen` met `monumentnummer`, `volgnummer` en
     `glassoort`;
   - een tabel `monumenten` met `monumentnummer`, `pandnaam` en `gemeente`;
   - een tabel `gemeenten` met `gemeente` en `provincie`.

   Elk gegeven staat nu op één plek. In les twee leer je hoe je dit stap voor
   stap en systematisch doet.

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

## 8. Getal en eenheid in één cel

**Hoort vooral bij:** leesbaar voor computer. **Ook:** opbouw en betekenis.

**Voorbeeld.** De kolom `Dikte` bevat `0.6-0.8cm`, `6-8mm` en `onbekend`.
Elders zie je vaak waarden als `1 kg`, `100 gr.` en `250 g` in één kolom.

**Waarom is dit een probleem?**

- Voor de computer is `6-8mm` tekst, geen getal. Je kunt niet sorteren,
  filteren op "dikker dan 5 mm" of een gemiddelde berekenen.
- Door verschillende eenheden (`cm` en `mm`, of `kg`, `gr.` en `g`) kun je
  waarden niet zomaar vergelijken.
- `0.6-0.8cm` zijn eigenlijk twee getallen: een minimum en een maximum.
- Een punt of een komma als decimaalteken wordt niet door elk programma
  hetzelfde gelezen.

**Wat kun je beter doen?**

- Zet alleen het getal in de cel en de eenheid in de kolomnaam, bijvoorbeeld
  `dikte_mm`. Reken alle waarden om naar die ene eenheid.
- Verdeel een bereik over twee kolommen: `dikte_min_mm` = `6` en
  `dikte_max_mm` = `8`.
- Komen verschillende eenheden echt voor? Gebruik dan een kolom `waarde` met
  alleen getallen en een kolom `eenheid` met een vaste keuzelijst.
- Stel een controle in, zodat alleen getallen kunnen worden ingevoerd (zie
  [Kwaliteitscontrole](04-kwaliteitscontrole.md)).

**Wanneer is het geen probleem?** Als je de waarde alleen wilt laten zien en
er nooit mee rekent, is `250 g` minder erg. Maar meestal wil je later toch
vergelijken of tellen, en dan is het makkelijker als het getal al los staat.

## 9. Datums die niet overal hetzelfde zijn

**Hoort vooral bij:** leesbaar voor computer. **Ook:** opbouw en betekenis.

**Voorbeeld.** De kolom `Datum aangepast` bevat echte datums naast tekst:
`3 maart 2017`, `2023-10-22`, `mar 2019`, `?? 2018`, `2025-4-14` en
`2025-13-8`. De kolom `Datering` bevat `1895`, `1700-1900`, `vóór 1890`,
`begin 17e eeuw/18e eeuw`, `19e eeuw (niet 100% zeker)` en `1940; 1956`.
Sommige jaartallen heeft Excel veranderd in de datum `1-1-1934`.

**Waarom is dit een probleem?**

- Tekst die op een datum lijkt is voor de computer geen datum. Sorteren op
  datum gaat dan mis.
- `04-05-2019` is 4 mei of 5 april, afhankelijk van het land.
- Spreadsheets veranderen invoer soms ongevraagd in een datum, zoals het
  jaartal `1934`.
- De **datum van invoer** (wanneer is de rij aangepast?) is iets anders dan
  de **datering** (uit welke tijd is het glas?). Een datering is vaak een
  periode en vaak onzeker. Die past niet in een gewone datumcel.

**Wat kun je beter doen?**

- Schrijf exacte datums als `jjjj-mm-dd`, bijvoorbeeld `2025-08-13`. Dit is
  de internationale norm (ISO 8601).
- Leg een datering vast als begin- en eindjaar in twee kolommen:
  `datering_vanaf` = `1801` en `datering_tot` = `1900`. Voeg eventueel een
  kolom toe voor de zekerheid (`zeker`, `waarschijnlijk`, `onzeker`).
- Twee jaartallen in één cel (`1940; 1956`) zijn twee gegevens. Zet ze op twee
  aparte rijen, bijvoorbeeld in een tabel met bouwfasen.
- Schrijf op welke afspraak je gebruikt, bijvoorbeeld dat "19e eeuw"
  betekent: 1801–1900.

Meer hierover staat in de aflevering [Datums in spreadsheets](03-datums.md).

## 10. Vrije woorden voor categorieën

**Hoort vooral bij:** betekenis. **Ook:** opbouw en leesbaar voor computer.

**Voorbeeld.** In de kolom `Soort glas?` staan onder andere:
`cilinderglas`, `cilindergas`, `cilinderglas (?)`, `spiegelglas`,
`speigelglass`, `prismategel`, `pirsmategel`, `prismaglas`, `marmerglas`,
`gegraveerd`, `ijsbloemenachtig` en `ossenoog`.

**Waarom is dit een probleem?**

- **Tikfouten en schrijfvarianten** (`cilindergas`, `speigelglass`,
  `pirsmategel`) telt de computer als aparte soorten.
- **Verschillende soorten informatie** staan in één kolom: een glassoort
  (`cilinderglas`), een bewerking (`gegraveerd`), een uiterlijk
  (`ijsbloemenachtig`) en zelfs de vorm van een raam (`ossenoog`).
- **Woorden die op elkaar lijken betekenen niet altijd hetzelfde.** Is
  `prismaglas` hetzelfde als `prismategel`?

Een voorbeeld van buiten de dataset: `bos`, `Bos`, `BOS`, `forest` en
`loofbos`. `bos`, `Bos` en `BOS` zijn hetzelfde woord, anders geschreven.
`forest` is de Engelse vertaling. Maar `loofbos` is een **specifieker**
begrip: elk loofbos is een bos, maar niet elk bos is een loofbos. Als je die
allemaal gelijk maakt, gooi je informatie weg.

**Wat kun je beter doen?** Er zijn drie niveaus, van eenvoudig naar
uitgebreid:

- **Keuzelijst**: een vaste lijst toegestane woorden, bijvoorbeeld als
  uitklaplijst in Excel. Dat voorkomt tikfouten.
- **Referentielijst**: een apart tabblad met per term een code, de
  voorkeursterm en een omschrijving. In de gegevens gebruik je alleen de
  code of de term.
- **Thesaurus**: een uitgebreide lijst met voorkeurstermen, synoniemen,
  definities en de verbanden tussen termen (breder en smaller). Voor erfgoed
  zijn bijvoorbeeld de
  [Cultuurhistorische Thesaurus](https://thesaurus.cultureelerfgoed.nl/)
  van de Rijksdienst voor het Cultureel Erfgoed en de
  [Getty AAT](https://www.getty.edu/research/tools/vocabularies/aat/)
  beschikbaar. Gebruik je dezelfde termen als anderen, dan kun je gegevens
  makkelijker vergelijken en delen.

Verdeel daarnaast verschillende soorten informatie over aparte kolommen, zoals
`glassoort`, `bewerking` en `raamvorm`. Meer hierover staat in de aflevering
[Referentielijsten gebruiken](06-referentielijsten.md).

::::::::::::::::::::::::::::::::::::: challenge 

## Opdracht 2: hetzelfde of iets anders?

Bekijk deze waarden uit de kolom `Soort glas?`. Welke zijn eigenlijk hetzelfde
woord, en welke betekenen echt iets anders?

`cilinderglas`, `cilindergas`, `cilinderglas (?)`, `spiegelglas`,
`speigelglass`, `prismategel`, `prismaglas`, `ossenoog`

:::::::::::::::::::::::: solution 

- `cilindergas` is een tikfout voor `cilinderglas`.
- `cilinderglas (?)` is hetzelfde woord, maar met twijfel. Schrijf
  `cilinderglas` en zet de twijfel in een aparte kolom.
- `speigelglass` is een tikfout voor `spiegelglas`.
- `prismategel` en `prismaglas` lijken op elkaar, maar zijn niet zeker
  hetzelfde: een prismategel is een specifiek product. Zoek dit op in een
  thesaurus voordat je ze samenvoegt.
- `ossenoog` is geen soort glas maar de vorm van een raam. Dit hoort in een
  andere kolom.

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: challenge 

## Opdracht 3: fouten indelen

Open het werkblad `Na 1900` van `historisch-glas-in-gebouwen_messy.xlsx`.
Zoek ten minste vijf fouten. Geef bij elke fout aan bij welke hoofdvraag hij
vooral hoort: opbouw, leesbaar voor computer of betekenis.

:::::::::::::::::::::::: solution 

Enkele mogelijke antwoorden:

| Fout | Hoort vooral bij |
|---|---|
| Blank en zwart glas als twee tabellen naast elkaar | Opbouw |
| `Monumentnr` bevat `?` en lege cellen | Leesbaar voor computer |
| `Datum aangepast` met `2025-13-8` en `3 maart 2017` | Leesbaar voor computer |
| `Datering` met `1940; 1956` (twee jaartallen in één cel) | Leesbaar voor computer (en opbouw) |
| Jaartal `1934` veranderd in `1-1-1934` | Leesbaar voor computer |
| Ontwerper en uitvoerder in vrije tekst in `Details_01` | Leesbaar voor computer |
| `gele cellen heb ik twijfel over` in K9 | Betekenis |
| `Restaurant (nu)` als naam van een pand | Opbouw en betekenis |

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: callout

### Overige opmaakfouten

Samengevoegde cellen, kleur als informatie, lege rijen als scheiding,
onhandige kolomnamen (met spaties, leestekens of eenheden tussen haakjes,
zoals `Soort glas?`) en harde enters in cellen komen aan bod in de aflevering
[Data opmaak in spreadsheets](02-opmaak.md).

::::::::::::::::::::::::::::::::::::::::::::::::

## Conclusie

Met de drie hoofdvragen kun je elke dataset kritisch bekijken:

- **Is de tabel goed opgebouwd?** Elk soort ding in een eigen tabel, elke rij
  een unieke code, en elk gegeven op één plek.
- **Kan een computer de gegevens goed lezen?** Eén tabel per werkblad, één
  rij kolomnamen, getallen zonder eenheid, datums in één notatie en één manier
  om ontbrekende waarden aan te geven.
- **Is de betekenis duidelijk en vastgelegd?** Uitleg van kolommen en codes,
  informatie over de herkomst van de gegevens, en vaste termen in plaats van
  vrije woorden.

De drie vragen vullen elkaar aan. Een tabel kan op het ene punt goed zijn en
op het andere niet. In les twee gaan we dieper in op de eerste vraag: hoe
ontwerp je een set tabellen waarin elk gegeven precies één keer voorkomt?

::::::::::::::::::::::::::::::::::::: keypoints 

- Bekijk een dataset met drie vragen: is de tabel goed opgebouwd, kan een computer hem lezen en is de betekenis duidelijk?
- Zet één dataset in één doorlopende tabel; gebruik aparte tabellen alleen voor verschillende soorten dingen.
- Geef elke rij een unieke code die nooit leeg is en niet verandert.
- Zet één gegeven per cel, getallen zonder eenheid en datums als `jjjj-mm-dd`.
- Kies één manier voor ontbrekende waarden en leg de reden apart vast.
- Zet uitleg, legenda's en metadata buiten de gegevens, in een leesmij-bestand of op een apart tabblad.
- Gebruik een keuzelijst, referentielijst of thesaurus voor categorieën.

::::::::::::::::::::::::::::::::::::::::::::::::

*Deze aflevering is gedeeltelijk gebaseerd op
[Formatting problems](https://datacarpentry.github.io/spreadsheet-ecology-lesson/02-common-mistakes.html)
uit de Data Carpentry-les* Data Organization in Spreadsheets for Ecologists
*(CC BY 4.0).*
