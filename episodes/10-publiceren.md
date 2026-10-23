---
title: Data publiceren
teaching: 15
exercises: 15
---

::::::::::::::::::::::::::::::::::::::: objectives

- Een goed online platform kiezen om mijn data te publiceren.
- Data zo publiceren dat ze Vindbaar, Toegankelijk, Interoperabel en Herbruikbaar is. 

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Hoe zorg ik dat anderen mijn data effectief kunnen gebruiken?
- Waar moet ik mijn data publiceren?

::::::::::::::::::::::::::::::::::::::::::::::::::

::: discussion
## Data publiceren
Wie heeft er een dataset gepubliceerd? 
Waar staat de data? Hoe zorg je dat anderen de data vinden en effectief kunnen gebruiken? 

Wat zijn redenen om data niet te delen/publiceren?
:::

## Doelgroep & usecase
Stel jezelf voordat je data publiceert de volgende vragen:
1. Wie is de doelgroep? Wie verwacht je dat de data gaat gebruiken?
2. Wat is de usecase? Waar verwacht je dat anderen de data voor gaan gebruiken?

Afhankelijk van deze vragen zal de manier waarop je je data publiceert er heel anders uitzien.
Een paar voorbeelden:

FIXME links naar real-life voorbeelden geven

## Vindbare, Toegankelijke, Interoperabele en Herbruikbare data (FAIR principes)
Bij het publiceren van data kunnen de [FAIR data principes](https://www.go-fair.org/fair-principles/) een handige 
richtlijn zijn. Nogmaals, afhankelijk van je doelgroep en usecase zul je hier verschillende keuzes in maken.

### Vindbaar (**F**indable)
Zorg dat anderen de data makkelijk kunnen vinden of doorzoeken.

- Gebruik een goed online platform zodat de data makkelijk vindbaar is. FIXME aanpassen!
  - Dataverse (https://dataverse.nl/dataverse/RCE)
  - Datastation SSH (https://ssh.datastations.nl/) van DANS
  - Zenodo (https://zenodo.org/)
  - Een eigen gebouwd platform. Meer werk, maar ook meer flexibiliteit.
- Beschrijf je data met metadata. Data over data, wat metadata genoemd wordt, zijn gestructureerde gegevens die de kenmerken van
je dataset beschrijven. Het zorgt ervoor dat andere gebruikers (en zoekmachines) een beeld krijgen van je data zonder dat ze de data zelf hoeven te bekijken.
Idealiter gebruik je voor de metadata een standaardformat zoals [DCAT-ap-nl30](https://docs.geostandaarden.nl/dcat/dcat-ap-nl30/), 
afhankelijk van de usecase kan dit ook overkill zijn.  
- Maak duidelijk welke versie van je data de publicatie betreft. Gebruik het liefst een *globally unique and persistent identifier*. 
Dit is een unieke URL die altijd naar jouw data verwijst. Met deze URL kun je expliciet verwijzen naar een bepaalde versie van de data.
Als je publiceert op één van de bovenstaande platformen, wordt meestal automatisch zo'n identifier aangemaakt. 

### Toegankelijk (**A**ccessible)
Maak de data publiek toegankelijk of beschrijf hoe je toegang tot de data kunt verkrijgen.

### Interoperabel (**I**nteroperable)
Zorg dat de dataset interoperabel (koppelbaar, uitwisselbaar) is met andere datasets.

- Gebruik gestandardiseerde vocabulair en identificering. Bijvoorbeeld:
  - Gebruik het monumentnummer vanuit het monumentregister, 
  zodat de data gekoppeld kan worden aan andere datasets die dezelfde standaard nummering gebruiken.
  - Gebruik publieke thesauri (FIXME: referentie naar episode 4) zodat bepaalde glastechnieken 
  met dezelfde term worden aangeduid als in andere datasets.

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

Check ook of je in jouw dataset gebruik maakt van bronnen die een bepaalde licentie hebben!

Dit lesmateriaal heeft de licentie CC BY, omdat we vinden dat iedereen dit lesmateriaal moet kunnen hergebruiken, 
maar we daar wel graag de credits voor willen ontvangen.   

:::

::: challenge
## Hoe publiceer ik mijn data?
Gebruik voor deze opdracht jouw eigen dataset of de real-life dataset die je in het eerste deel van de cursus hebt gebruikt.
Ga ervan uit dat je de data gaat publiceren. Als je data al gepubliceerd is, schrijf dan eventuele verbeteringen op.

1. Wie is de doelgroep? Wat zijn verwachte usecases?
2. Waar zet je de data?
3. Hoe zorg je ervoor dat de data-publicatie aan de FAIR principes voldoet?

:::: solution
Bespreek je antwoorden met degene naast je.
:::: 
:::
:::::::::::::::::::::::::::::::::::::::: keypoints

- Publiceer de data zo dat ze Vindbaar, Toegankelijk, Interoperabel en Herbruikbaar is (FAIR).
- Houd altijd rekening met voor wie je de data publiceert en waarom (doelgroep & usecase).
::::::::::::::::::::::::::::::::::::::::::::::::::