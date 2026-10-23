---
title: Data exporteren
teaching: 10
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Begrijpen waarom je spreadsheet data beter opslaat in universele bestandsformaten.
- Data vanuit een spreadsheet exporteren naar een CSV-bestand.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Hoe kunnen we data uit spreadsheets exporteren op een manier die bruikbaar is voor vervolgtoepassingen?

::::::::::::::::::::::::::::::::::::::::::::::::::

Het is geen goed idee om de data waarmee je je analyses gaat uitvoeren op te slaan in
het standaardbestandsformaat van Excel (`*.xls` of `*.xlsx` - afhankelijk van de
Excel-versie). Waarom niet?

Omdat:

- Een Excel-bestand bevat meer dan alleen data. 
Formules, opmaak, kleuren, meerdere tabbladen en macro’s zitten allemaal in hetzelfde bestand. 
Daardoor is het in de praktijk vooral goed te lezen met Excel zelf.
- Andere programma’s lezen het niet altijd hetzelfde. 
- LibreOffice, Apple Numbers, Google Sheets, een GIS- of een analyseprogramma kunnen een Excel-bestand openen, 
- maar opmaak, formules of datums kunnen daarbij anders uitpakken of verloren gaan.
- Ook verschillende versies van Excel verwerken data niet altijd gelijk. 
- Datums zijn een bekend voorbeeld: die kunnen bij het uitwisselen tussen versies of tussen Windows en Mac onverwachts veranderen.
- Voor de lange termijn is eenvoud veiliger. 
Hoe ingewikkelder een bestandsformaat, hoe groter de kans dat het over tientallen jaren lastig te openen is. 
- Het oude .xls-formaat wordt nu al door steeds minder programma’s goed ondersteund.

Bewaar je analysedata daarom (ook) in een universeel, open en statisch formaat zoals CSV. 
CSV is plat tekstbestand waarin de kolommen door komma's worden gescheiden, vandaar 'comma separated values' of CSV. 
Gewone tekst met alleen rijen en kolommen, die door vrijwel elk programma gelezen kan worden, nu en in de toekomst.

Data in een CSV-bestand kan bovendien eenvoudig worden geïmporteerd in andere formaten en
omgevingen, zoals SQLite, Python en R.

We zijn niet gebonden aan een bepaalde versie van een duur programma wanneer we met CSV-bestanden werken, 
dus het is een goed formaat voor maximale overdraagbaarheid en duurzaamheid. 
De meeste spreadsheetprogramma's kunnen eenvoudig opslaan in gescheiden tekstformaten zoals CSV, al kunnen ze tijdens het exporteren wel een waarschuwing geven.

Laten we het bestand dat je in Excel hebt geopend opslaan in CSV-formaat:

1. Kies in het bovenste menu 'Bestand' en 'Opslaan als'.
2. Kies in het veld 'Formaat' uit de lijst 'Comma Separated Values' (`*.csv`).
3. Controleer nogmaals de bestandsnaam en de locatie waar je het wilt opslaan en klik op 'Opslaan'.

#### Kanttekeningen bij komma's

In sommige datasets kunnen de datawaarden zelf komma's (,) bevatten. Bijvoorbeeld landen die
komma's als decimaal scheidingsteken gebruiken. In dat geval zal de software die je gebruikt (inclusief Excel)
de data waarschijnlijk onjuist in kolommen weergeven. Dit komt doordat de komma's die deel uitmaken van de datawaarden
als scheidingstekens worden geïnterpreteerd.

Als je werkt met data die komma's bevatten, moet je waarschijnlijk een ander scheidingsteken gebruiken wanneer je in een spreadsheet werkt. In dat geval kun je ook kiezen om een tab, een puntkomma (;) of een pipe (|) te gebruiken.
geval kun je overwegen tabs als scheidingsteken te gebruiken en met TSV-bestanden te werken. TSV-bestanden kunnen op dezelfde manier uit spreadsheetprogramma's worden geëxporteerd
als CSV-bestanden.

:::::::::::::::::::::::::::::::::::::::: keypoints

- Data die in gangbare spreadsheetformaten zijn opgeslagen, worden door software voor data-analyse vaak niet correct ingelezen, waardoor er fouten in je data kunnen ontstaan.
- Door data uit spreadsheets te exporteren naar formaten zoals CSV of TSV zijn ze consistent bruikbaar in de meeste programma's.

::::::::::::::::::::::::::::::::::::::::::::::::::