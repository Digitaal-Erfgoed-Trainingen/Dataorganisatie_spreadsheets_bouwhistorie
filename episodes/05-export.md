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

- Omdat het een niet-open bestandsformaat is. Het is mogelijk dat de technologie om
  het bestand te openen in de toekomst niet meer bestaat (of zo zeldzaam wordt)
  dat het lastig, zo niet onmogelijk wordt om het bestand te openen.

- Andere spreadsheetsoftware (LibreOffice/MacOS Sheets etc.) kan bestanden die in een niet-open
  Excel-formaat zijn opgeslagen mogelijk niet openen.

- Verschillende versies van Excel kunnen data
  verschillend verwerken, wat tot inconsistenties leidt.
- Niet alle softwarepakketten kunnen de bestandsformaten van Excel gebruiken

- Bovenstaande punten gelden ook voor andere formaten, zoals de open dataformaten van LibreOffice / Open Office. Deze formaten zijn niet statisch en worden niet door alle softwarepakketten op dezelfde manier geïnterpreteerd.

Het opslaan van data in een universeel, open en statisch formaat helpt deze probleem te voorkomen. 
Standaards zijn tabgescheiden (tab separated values
of TSV) of kommagescheiden (comma separated values of CSV) bestanden. 
CSV-bestanden zijn platte tekstbestanden waarin de kolommen door komma's worden gescheiden,
vandaar 'comma separated values' of CSV. 
Het voordeel van een CSV-bestand ten opzichte van een Excel-/SPSS-/enz.-bestand is dat we een CSV-bestand kunnen openen en lezen
met vrijwel elke software, inclusief eenvoudige teksteditors zoals TextEdit of NotePad.
Data in een CSV-bestand kan bovendien eenvoudig worden geïmporteerd in andere formaten en
omgevingen, zoals SQLite en R. 
We zijn niet gebonden aan een bepaalde versie van een bepaald duur programma wanneer we met CSV-bestanden werken, 
dus het is een goed formaat voor maximale overdraagbaarheid en duurzaamheid. 
De meeste spreadsheetprogramma's kunnen eenvoudig opslaan in gescheiden tekstformaten zoals CSV,
al kunnen ze tijdens het exporteren wel een waarschuwing geven.

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