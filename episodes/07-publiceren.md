---
title: Data publiceren
teaching: 15
exercises: 15
---

::::::::::::::::::::::::::::::::::::::: objectives

- Een goed online platform kiezen om mijn data te publiceren.
- Data zo publiceren dat ze Vindbaar, Toegankelijk, Interoperabel en Herbruikbaar zijn. 

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Hoe zorg ik dat anderen mijn data effectief kunnen gebruiken?
- Waar moet ik mijn data publiceren?

::::::::::::::::::::::::::::::::::::::::::::::::::

::: discussion
## Data publiceren
Wie heeft er wel eens een dataset gepubliceerd? 
Waar staat de data? Hoe zorg je dat anderen de data vinden en effectief kunnen gebruiken? 

Wat zijn redenen om data niet te delen/publiceren?
:::

## Doelgroep & usecase
Stel jezelf de volgende vragen voordat je data publiceert:
1. Wie is de doelgroep? Wie verwacht je dat de data gaat gebruiken?
2. Waarvoor verwacht je dat de data gebruikt gaat worden? 

Afhankelijk van deze vragen zal de manier waarop je je data publiceert er anders uitzien. 

## Vindbare, Toegankelijke, Interoperabele en Herbruikbare data (FAIR principes)
Bij het publiceren van data kunnen de [FAIR data principes](https://www.go-fair.org/fair-principles/) een handige 
richtlijn zijn. Nogmaals, afhankelijk van je doelgroep en casuïstiek zul je hier verschillende keuzes in maken.

### Vindbaar (**F**indable)
Zorg dat anderen de data makkelijk kunnen vinden of doorzoeken. Het gaat daarbij om informatie die gebruikers nodig hebben voordat ze je data gebruiken. Dit wordt ook wel de metadata genoemd.

- Beschrijf je data met metadata. De matadata van je data zijn gestructureerde gegevens die de kenmerken van
een dataset beschrijven. Het zorgt ervoor dat andere gebruikers (en zoekmachines) een beeld krijgen van je data zonder dat ze de data zelf hoeven te bekijken.
Idealiter gebruik je voor de metadata een standaardformat zoals [DCAT-ap-nl30](https://docs.geostandaarden.nl/dcat/dcat-ap-nl30/), maar dit is ook weer afhankelijk van waar je de data publiceert en welke doelgroep je wilt dat je data kan gebruiken.  
- Maak duidelijk welke versie van je data de publicatie betreft. 
- Gebruik het liefst een *globally unique and persistent identifier*. 
Dit is een unieke URL/URI die altijd naar jouw data verwijst. Met deze URL/URI kun je ook expliciet verwijzen naar een bepaalde versie van de data. Afhankelijk van waar de data wordt gepubliceerd wordt automatisch zo'n identifier aangemaakt. 

Het juiste platform vinden voor data die je wilt publiceren is niet eenvoudig. Voor vrijwilligers in het Erfgoedveld is het raadzaam contact te zoeken met [erfgoed coaches]( https://netwerkdigitaalerfgoed.nl/datawerkplaatsen/) vanuit het Netwerk Digitaal Erfgoed. Zij kunnen adviseren waar de verzamelde data het best gepubliceerd kan worden. Het zou bijvoorbeeld kunnen dat data bij de [Rijksdienst voor het Cultureel Erfgoed](https://www.cultureelerfgoed.nl/) gepubliceerd kan worden, of bij een van de nationale of provinciale archieven. Voor archeologische datasets bestaat het [Portable Antiquities of the Netherlands](https://portable-antiquities.nl/pan/#/public) platform. 

Bij het aanleveren van datasets helpt het enorm wanneer de data van een goede kwaliteit zijn, oftewel wanneer de lessen uit deze module succesvol zijn toegepast!

Voor data voortkomend uit (wetenschappelijk) onderzoek worden de volgende platformen gebruikt. Deze platformen kunnen in theorie ook relevant zijn voor data verzameld door vrijwilligers. 

  - Dataverse (https://dataverse.nl/dataverse/RCE)
  - Datastation SSH (https://ssh.datastations.nl/) van [DANS](https://dans.knaw.nl/nl/)
  - Zenodo (https://zenodo.org/)

### Toegankelijk (**A**ccessible)
Maak de data publiek toegankelijk of beschrijf hoe je toegang tot de data kunt verkrijgen. Dit hangt wederom af van het gevonden/ gekozen platform waar de data wordt gepubliceerd, maar ook van de licentie (zie hieronder meer informatie over licenties).

### Interoperabel (**I**nteroperable)
Zorg dat de dataset interoperabel (koppelbaar, uitwisselbaar) is met andere datasets.

- Gebruik gestandardiseerde vocabulair en identificering. Bijvoorbeeld:
  - Gebruik het monumentnummer vanuit het monumentregister, 
  zodat de data gekoppeld kan worden aan andere datasets die dezelfde standaard nummering gebruiken.
  - Gebruik publieke thesauri, zodat bepaalde glastechnieken 
  met dezelfde term worden aangeduid als in andere datasets (zie [hoofdstuk 4: Kwaliteitscontrole, referentielijsten & publieke thesauri](04-kwaliteitscontrole.md)).

### Herbruikbaar (**R**eusable)
Zorg dat anderen de data kunnen gebruiken.

- Gebruik de *best practices* voor dataorganisatie die je tot nu toe hebt geleerd. 
Een georganiseerde dataset is een herbruikbare dataset.
- Voeg een (open) licentie toe. Zie de 'uitgelicht' over licenties hieronder.


::: callout
## Licentie
Zonder licentie heeft niemand het recht om je data te gebruiken!
De meest voorkomende licenties en een korte samenvatting van hun eigenschappen zijn:

| Licentie | Wat mag |
|---|---|
| **CC0** | Geen rechten voorbehouden (publiek domein). Hergebruik zonder voorwaarden. |
| **CC BY** | Alles mag, mits je de bron vermeldt. |
| **CC BY-NC** | Bronvermelding verplicht, geen commercieel gebruik. |
*Een uitgebreid overzicht van verschillende licenties op data en software is [hier](https://creativecommons.nl/uitleg/) te vinden.* 

Wanneer een dataset wordt gepubliceerd in een doorzoekbare metadata catalogus/datasetregister zoals [data.overheid](https://data.overheid.nl/data) voor overheidsdata of het [datasetregister](https://datasetregister.netwerkdigitaalerfgoed.nl/datasets) van het [Netwerk Digitaal Erfgoed](https://netwerkdigitaalerfgoed.nl/) is het toekennen van een licentie verplicht. 

*N.B. Bij het invullen van de metadata hebben deze registers dus gebruik gemaakt van referentielijsten met de verschillende keuzes voor licenties (net zoals we dat in hoofdstuk 4 hebben gedaan bij de referentielijsten!)* 

Check ook of je in jouw dataset gebruik maakt van bronnen die een bepaalde licentie hebben!

Dit lesmateriaal heeft de licentie CC BY, omdat we vinden dat iedereen dit lesmateriaal moet kunnen hergebruiken, 
maar we daar wel graag de credits voor willen ontvangen.

:::

::: challenge
## Hoe publiceer ik mijn data?
Gebruik voor deze opdracht jouw eigen dataset of de real-life dataset die je in het eerste deel van de cursus hebt gebruikt.
Ga ervan uit dat je de data gaat publiceren. Als je data al gepubliceerd is, schrijf dan eventuele verbeteringen op.

1. Wie is de doelgroep? 
2. Waarvoor verwacht je dat de data gebruikt kan worden?
3. Waar zet je de data?
4. Hoe zorg je ervoor dat de data-publicatie aan de FAIR principes voldoet?

:::: solution
Bespreek je antwoorden met degene naast je.
:::: 
:::
:::::::::::::::::::::::::::::::::::::::: keypoints

- Publiceer de data zo dat ze Vindbaar, Toegankelijk, Interoperabel en Herbruikbaar is (FAIR).
- Houd altijd rekening met voor wie je de data publiceert en waarom (doelgroep & gebruik).
::::::::::::::::::::::::::::::::::::::::::::::::::