---
title: "Introductie"
teaching: 10 # teaching time in minutes
exercises: 2 # exercise time in minutes
---

:::::::::::::::::::::::::::::::::::::: questions 
- Wat zijn de basisprincipes waaraan tabulaire data moet voldoen? 
::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Het kunnen beschrijven van *best practices* voor het organiseren van tabulaire gegevens zodat deze bruikbaar worden voor analyse en koppelbaar met andere datasets. 
::::::::::::::::::::::::::::::::::::::::::::::::

## Leerdoelen

In deze les leer je hoe je over dataorganisatie kunt nadenken en welke werkwijzen je kunt toepassen om data efficiënter te verwerken. Met deze aanpak kun je bestaande data beter structureren en nieuwe dataverzameling beter plannen, zodat je achteraf minder tijd kwijt bent aan het opschonen en organiseren van data.

In deze les leer je *niet* hoe je data analyseert met spreadsheets.

Na afloop van deze module kan de deelnemer:

* Veelvoorkomende opmaakfouten herkennen en voorkomen; 
* Datums op een consistente en correcte wijze vastleggen en beheren; 
* Eenvoudige kwaliteitscontroles uitvoeren en basisbewerkingen op tabulaire gegevens toepassen; 
* Gegevens op een correcte wijze exporteren voor gebruik in andere applicaties en analyseomgevingen.
* Identificeren wanneer het gebruiken of opstellen van referentielijsten/ thesauri van toegevoegde waarde is bij een dataset;
* Hoe het beste omgegaan kan worden met het documenteren van afbeeldingen. 

### Waarom behandelen we geen data-analyse in spreadsheets?

* Data-analyse in spreadsheets vereist vaak veel handmatig werk. Wanneer je een parameter wilt aanpassen of een analyse wilt uitvoeren met een nieuwe dataset, moet je doorgaans veel stappen handmatig opnieuw uitvoeren. 

* Het is lastig om analyses in spreadsheets te controleren en te reproduceren. Wanneer je later je werk opnieuw wilt bekijken of iemand om een toelichting op je analyse vraagt, is het vaak moeilijk om precies te achterhalen welke stappen zijn uitgevoerd. Dit geldt zowel voor statistische analyses als voor het maken van grafieken en visualisaties.

Natuurlijk kunnen hier ook scripts voor worden gemaakt, maar dat vergt een aanzienlijke basis programmeren, hetgeen voor de beoogde doelgroep van deze cursus te ver gaat.

## Spreadsheet software

Om met tabulaire data te werken zijn er verschillende spreadsheet software beschikbaar. Omdat de meeste deelnemers Excel gebruiken, wordt deze software gebruikt bij de voorbeelden in deze cursus. Hoewel de exacte functies en opdrachten per programma kunnen verschillen vormt dit geen probleem aangezien de onderliggende principes  hetzelfde blijven.

Alternatieven voor excel zijn gegeven op op de [setup pagina](index.html#software)


:::::::::::::::::::::::::::::::::::::::::  callout

## Oefening

- Wie heeft er wel eens gewerkt met spreadsheet software? 

- Wie heeft er wel eens iets in een spreadsheet gedaan waar hij of zij achteraf spijt van had?  

::::::::::::::::::::::::::::::::::::::::::::::::::


Spreadsheets encompass a lot of the things we need
to be able to do as researchers. We can use them for:

- Data entry
- Organizing data
- Subsetting and sorting data
- Statistics
- Plotting

We do a lot of different operations in spreadsheets. What kind of operations do you do in spreadsheets? Which ones do you think spreadsheets are good for?

## Problems with Spreadsheets

Spreadsheets are good for data entry, but in reality we tend to
use spreadsheet programs for much more than data entry. We use them
to create data tables for publications, to generate summary
statistics, and make figures.

Generating tables for publications in a spreadsheet is not
optimal - often, when formatting a data table for publication, we're
reporting key summary statistics in a way that is not really meant to
be read as data, and often involves special formatting
(merging cells, creating borders, making it pretty). Cutting and pasting from a spreadsheet
to a document software (like Word) can have unpredictable results.
We advise you to create tables within these document software
using the document's own table editing software.

The latter two applications, generating statistics and figures, should
be used with caution: because of the graphical, drag and drop nature of
spreadsheet programs, it can be very difficult, if not impossible, to
replicate your steps (much less retrace anyone else's), particularly if your
stats or figures require you to do more complex calculations. Furthermore,
in doing calculations in a spreadsheet, it's easy to accidentally apply a
slightly different formula to multiple adjacent cells. When using a
command-line based statistics program like R or SAS, it's practically
impossible to apply a calculation to one observation in your
dataset but not another unless you're doing it on purpose.

### Using Spreadsheets for Data Entry and Cleaning

However, there are circumstances where you might want to use a spreadsheet
program to produce "quick and dirty" calculations or figures, and data
cleaning will help you use some of these features. Data cleaning also
puts your data in a better format prior to importation into a
statistical analysis program. We will show you how to use some features of
spreadsheet programs to check your data quality along the way and produce
preliminary summary statistics.

In this lesson, we will assume that you are most likely using Excel as
your primary spreadsheet program - there are others (gnumeric, Calc
from OpenOffice), and their functionality is similar, but Excel seems
to be the program most used by biologists and ecologists.

In this lesson we're going to talk about:

1. [Formatting data tables in spreadsheets](01-format-data.md)
2. [Formatting problems](02-common-mistakes.md)
3. [Dates as data](03-dates-as-data.md)
4. [Quality control](04-quality-control.md)
5. [Exporting data](05-exporting-data.md)

:::::::::::::::::::::::::::::::::::::::: keypoints

- Good data organization is the foundation of any research project.

::::::::::::::::::::::::::::::::::::::::::::::::::
