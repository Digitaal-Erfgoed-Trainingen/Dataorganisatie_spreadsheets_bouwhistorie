# Dataorganisatie in spreadsheets voor bouwhistorie

De module Dataorganisatie in spreadsheets voor bouwhistorie is ontwikkeld voor erfgoedvrijwilligers en professionals die systematisch gegevens verzamelen over bouwhistorische objecten. Goede dataorganisatie vormt de basis van elk project. Een spreadsheet (Excel-bestand) is een goede manier om data op te slaan. Meestal beginnen we data te organiseren op een manier die voor ons als mensen prettig is om mee te werken. Computers vereisen echter dat data op een specifieke manier wordt georganiseerd. Om tools te kunnen gebruiken die analyses en zoeken efficiënter maken, zoals programmeertalen (zoals R of Python), of een database, moeten we onze data structureren op een manier die computers kunnen verwerken.

## Voor wie is deze les?

De cursus is bedoeld als basiscursus voor iedereen die met tabulaire data werkt. De casuïstiek is weliswaar glas voor bouwhistorie, maar de lessen zijn ook bruikbaar voor andere (sub) domeinen.

In deze les leer je hoe je over dataorganisatie kunt nadenken en welke werkwijzen je kunt toepassen om data efficiënter te verwerken. Met deze aanpak kun je bestaande data beter structureren en nieuwe dataverzameling beter plannen, zodat je achteraf minder tijd kwijt bent aan het opschonen en organiseren van data. In deze les leer je niet hoe je data analyseert met spreadsheets.

Na afloop van deze module kan de deelnemer:

* Veelvoorkomende opmaakfouten herkennen en voorkomen;
* Datums op een consistente en correcte wijze vastleggen en beheren;
* Eenvoudige kwaliteitscontroles uitvoeren en basisbewerkingen op tabulaire gegevens toepassen;
* Gegevens op een correcte wijze exporteren voor gebruik in andere applicaties en analyseomgevingen.
* Identificeren wanneer het gebruiken of opstellen van referentielijsten/ thesauri van toegevoegde waarde is bij een dataset;
* Hoe het beste omgegaan kan worden met het documenteren van afbeeldingen.


## Deze les geven?
Dit lesmateriaal is openbaar en kan vrij en gratis gebruikt worden. Ben je van plan de les te gebruiken? 
We helpen je graag bij de voorbereiding en krijgen ook graag feedback op de les. 
Laat ons weten als je de les gaat geven door te mailen naar [m.dekleijn@cultureelerfgoed.nl](mailto:m.dekleijn@cultureelerfgoed.nl). 

## Bijdragen
Als je wilt bijdragen aan deze les, neem dan contact op met Maurice de Kleijn ([m.dekleijn@cultureelerfgoed.nl](mailto:m.dekleijn@cultureelerfgoed.nl)).

## Lokaal draaien
Om deze les lokaal te bouwen, volg je de [installatie-instructies voor de Workbench](https://carpentries.github.io/sandpaper-docs/#overview). 
Kort gezegd: 
- Zorg er voor dat R, Git en Pandoc zijn geïnstalleerd. 
- Open vervolgens R en run de volgende commands in de console om de benodigde 
infrastructuurpakketten te installeren of bij te werken:
```R
install.packages(c("sandpaper", "varnish", "pegboard"),
  repos = c("https://carpentries.r-universe.dev/", getOption("repos")))
```

Om te renderen, run:
```R
sandpaper::serve()
```
Bekijk ook de [Carpentries Workbench](https://carpentries.github.io/workbench/#usage) instructies.

## Beheerders
Maurice de Kleijn ([m.dekleijn@cultureelerfgoed.nl](mailto:m.dekleijn@cultureelerfgoed.nl))
Sven van der Burg
Olivier Wieringa