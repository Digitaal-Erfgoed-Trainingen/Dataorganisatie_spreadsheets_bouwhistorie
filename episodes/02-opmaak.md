---

title: Data opmaken in spreadsheets
teaching: 15
exercises: 20
-------------

::::::::::::::::::::::::::::::::::::::: objectives
* Herkennen en voorkomen van veelvoorkomende opmaakfouten in spreadsheets

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

* Hoe organiseer ik mijn spreadsheet zo zodat de data effectief kan worden gebruikt?

::::::::::::::::::::::::::::::::::::::::::::::::::

De meest voorkomende fout in het gebruik van spreadsheetprogramma's is dat het een soort persoonlijk notitieboek wordt.
Dat wil zeggen dat je gebruik maakt van commentaar, ruimtelijke indeling, highlights etc. om informatie over te brengen.
Als mensen kunnen we deze zaken (meestal) interpreteren, maar computers bekijken informatie niet op dezelfde manier.

Dankzij de kracht van computers kunnen we data veel effectiever en sneller beheren en analyseren. 
Om die mogelijkheden te benutten, moeten we onze data echter zo structureren dat de computer ze kan begrijpen. 
Computers interpreteren informatie namelijk heel letterlijk.


Daarom is het belangrijk om vanaf het begin goed opgemaakte tabellen te maken, 
het liefst nog voordat je data invoert.

Je kunt spreadsheets op verschillende manieren inrichten, maar sommige keuzes kunnen je mogelijkheden beperken om met de data in andere programma's te werken. 
Ze kunnen er ook voor zorgen dat jijzelf over zes maanden, of een van je samenwerkingspartners, moeite krijgt om met de data te werken.

::::::::::::::::::::::::::::::::::::::::: callout

## Opmerking

De beste indeling en opmaak voor dataverzameling kunnen verschillen van die voor data-analyse. 
Hetzelfde geldt voor de gebruikte software en interfaces. 
Het is belangrijk om hiermee rekening te houden en de omzetting van de ene indeling naar de andere waar mogelijk te automatiseren.

::::::::::::::::::::::::::::::::::::::::::::::::::

### Je analyses bijhouden

Wanneer je met spreadsheets werkt, bijvoorbeeld tijdens het opschonen of analyseren van data, 
is het heel gemakkelijk om uiteindelijk een spreadsheet te krijgen die er heel anders uitziet dan het oorspronkelijke bestand.

Om je analyses te kunnen reproduceren of te kunnen achterhalen wat je hebt gedaan, moet je het volgende doen:

* Wijzig nooit de oorspronkelijke data. Maak een nieuw bestand met je opgeschoonde of geanalyseerde data.
* Houd bij welke stappen je hebt uitgevoerd tijdens het opschonen of analyseren van de data. We raden aan dit te doen in een gewoon tekstbestand dat je in dezelfde map als het databestand bewaart.

Pas deze principes toe tijdens de oefeningen van deze cursus.

### Data structureren in spreadsheets

De belangrijkste regel is 'houd het netjes', dit komt neer op:

1. Plaats alle variabelen in kolommen.
2. Plaats elke waarneming op een eigen rij.
3. Combineer niet meerdere stukjes informatie in één cel. Soms lijkt informatie één geheel te vormen, maar bedenk of je die data later ook afzonderlijk wilt kunnen gebruiken of sorteren.
4. Laat de ruwe data ongewijzigd: verander ze niet!
5. Exporteer de opgeschoonde data naar een tekstbestand, zoals CSV (*comma-separated values*). Zo kan iedereen de data gebruiken. Bovendien is dit formaat vereist door de meeste databases.

::::::::::::::::::::::::::::::::::::::: challenge

## Oefening

We gaan een rommelige dataset bekijken en beschrijven hoe we deze zouden opschonen.

1. Download de dataset door [hier te klikken](https://github.com/Digitaal-Erfgoed-Trainingen/Digitale_geletterdheid_WS1/raw/refs/heads/main/data/historisch-glas-in-gebouwen_messy.xlsx).
2. Open de data in een spreadsheetprogramma (Excel of iets vergelijkbaars). Je ziet dat er 3 tabbladen zijn.
3. Jij bent nu verantwoordelijk voor dit project en wilt de data gaan analyseren.
Bespreek samen met degene naast je wat er mis is met deze spreadsheet. 
Bespreek ook welke stappen nodig zijn om de tabbladen `voor 1900` en `na 1900` en `Datum onbekend` op te schonen en alle data samen te voegen in één spreadsheet.

**Belangrijk:** vergeet ons eerste advies niet: maak een nieuw bestand of tabblad voor de opgeschoonde data. Wijzig nooit de oorspronkelijke (ruwe) data.

Na deze oefening bespreken we gezamenlijk wat er mis was met de data en hoe je dit zou kunnen oplossen.

::::::::::::::: solution

## Oplossing

* Neem ongeveer 10 minuten de tijd voor deze oefening.
* Alle fouten die worden beschreven in hoofdstuk [Meestvoorkomende fouten](03-meestvoorkomende-fouten.md) komen voor in de rommelige dataset, behalve 'Niet invullen van nullen'. 

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

Er zijn uitstekende bronnen beschikbaar die je helpen bij het werken met data in spreadsheets. Hieronder vind je enkele voorbeelden.

Met betrekking tot programmeren in R:

> Hadley Wickham, *Tidy Data*, deel 59, nummer 10, september 2014, *Journal of Statistical Software*. [http://www.jstatsoft.org/v59/i10](https://www.jstatsoft.org/v59/i10).

Met betrekking tot het op de juiste manier organiseren van data in spreadsheets:

> Karl W. Broman & Kara H. Woo (2018), *Data Organization in Spreadsheets*, The American Statistician, 72:1, 2-10. [DOI: 10.1080/00031305.2017.1375989](https://www.tandfonline.com/doi/full/10.1080/00031305.2017.1375989).

:::::::::::::::::::::::::::::::::::::::: keypoints

* Wijzig nooit je ruwe data. Maak altijd een kopie voordat je wijzigingen aanbrengt.
* Organiseer je data zo dat jij-zelf-in-de-toekomst, anderen, en een computer de data kan begrijpen.
* Voorkom veelvoorkomende fouten in data opmaak.

::::::::::::::::::::::::::::::::::::::::::::::::::
