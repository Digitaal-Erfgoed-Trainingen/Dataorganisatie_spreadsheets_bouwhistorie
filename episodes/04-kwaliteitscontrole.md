---
title: "Kwaliteitscontrole, referentielijsten & publieke thesauri"
teaching: 20
exercises: 15
---

:::::::::::::::::::::::::::::::::::::: questions 
- Hoe kan ik makkelijk de kwaliteit van data controleren in spreadsheets?
- Hoe kan ik tijdens het invoeren van data de kwaliteit van de data waarborgen?
- Hoe gebruik ik referentielijsten en publieke thesauri?
::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives
- Data validatie gebruiken om datakwaliteit te waarborgen
- Eenvoudige kwaliteitscontroles uitvoeren 
- Een referentielijst of publieke thesaurus gebruiken om expliciet te maken wat er met een waarde wordt bedoeld
::::::::::::::::::::::::::::::::::::::::::::::::

## Dataset
Voor dit hoofdstuk gebruiken we `historisch-glas-in-gebouwen_kwaliteitscontrole.xlsx`.
[Volg hier de downloadinstructies](learners/setup.md#glas-in-gebouwen-kwaliteitscontrole-dataset).

## Datakwaliteit controleren

::: challenge
## Filteren als snelle datacontrole

1. Selecteer de `Soort glas` kolom.
2. Klik op `Gegevens` -> `Filter`.
3. Klik op het filterpijltje bovenaan de `Soort glas` kolom die nu is verschenen.
4. Kun je de 2 typefouten vinden?
5. (Bonus) Kijk nu naar de kolom `Plaatsing` en pas dezelfde filtering toe. Bekijk de waarden. Schrijf mogelijke verbeteringen op voor de waardes in deze kolom. Hoe makkelijk zijn deze waardes te groeperen?  

:::: solution
De typefouten bij de `Soort glas` kolom zijn:
- `Cilindergas` ipv `Cilinderglas`
- `Prismagels` ipv `Prismategel`

Voor de kolom `Plaatsing` zal je zien dat het gemakkelijk categoriseren van deze kenmerken niet heel eenvoudig is. Er zit een behoorlijke diversiteit in de waardes van deze kolom waardoor het de vraag is hoe zinvol het is deze in vastgelegde categorieën te organiseren. 

Het voordeel van het wél doen is dat de data makkelijker te doorzoeken wordt. Het nadeel is echter dat het beperkend kan werken wanneer er vastgelegde categorieën zijn. De eigenschap `Plaatsing` lijkt zeer contextafhankelijk waardoor het raadzaam zou zijn vrijheid te geven hoe deze in te vullen.

::::
:::

::: callout
Voor numerieke waardes kun je een snelle controle uitvoeren door de waardes van klein naar groot te sorteren.
Zo zie je snel of er gekke waardes tussen zitten (denk aan glas met een dikte van 1000 mm).
:::

## Data validatie
Een typefout is snel gemaakt. Met data-validatie kun je dat voorkomen.
Laten we naar een voorbeeld kijken.

::: instructor
Voor sommige cursisten is dit gesneden koek. Voor anderen zal het heel lang duren om hier doorheen te klikken.
Je kunt er daarom ook voor kiezen om dit te demonstreren zonder dat cursisten mee doen. 
Het gaat er immers niet per se om dat cursisten uit hun hoofd data-validatie in spreadsheets kunnen toepassen na deze cursus,
maar dat ze het principe snappen.

:::

1. Selecteer de `Soort glas` kolom.
2. Klik op `Gegevens` -> `Gegevensvalidatie`.
3. Selecteer in het dropdownmenu bij `Validatiecriteria` onder `Toestaan`: `Lijst`.
4. Klik bij `Bron:` op het icoontje rechts om handmatig waardes te selecteren.
5. Selecteer in het tabblad `Referentielijst` de waardes onder `Soort glas` die je wilt toestaan.
6. Klik op `OK`.
7. Probeer nu in een lege cel in de `Soort glas` kolom `Prismagels` te typen.
8. Wat gebeurt er?

## Referentielijsten en thesauri
In het tabblad `referentielijst` zien we mogelijke waardes voor de `Soort glas` kolom.
Ook zien we de bijbehorende beschrijving. 
Dit maakt het expliciet wat we bedoelen met bijvoorbeeld `Prismategels` en voorkomt verwarring.

Nog beter is om gebruik te maken van een publieke thesaurus. 
Een publieke thesaurus is een geordende lijst van termen en hun betekenis. 
Vaak zijn het termen en opdelingen waar men het in het veld over eens is dat we die zo gebruiken.

::: challenge
## Soorten glas in de Cultuurhistorische Thesaurus

1. Bekijk [de soorten glas in de Cultuurhistorische Thesaurus van de Rijksdienst voor Cultureel Erfgoed](https://thesaurus.cultureelerfgoed.nl/concept/cht:dcc2121b-8394-44f7-9664-86b109d079a4/nl).
Het is daarbij handig om het menu aan de linkerzijde van die pagina te gebruiken.
2. Probeer de waardes in de `Soort glas` kolom te vinden in de thesaurus. 
Je kunt handmatig zoeken in de `Glas` subcategorieën, of de zoekbalk gebruiken. Wat valt je op?

:::: solution
- `Prismategel` valt hier onder `artefacten` -> `bouwelement` -> `tegel`. 
Als we de thesaurus zouden volgen zou het dus logischer zijn om in deze kolom `Prismategel` als `Prismaglas` op te nemen.
We kunnen wellicht in een andere kolom specificeren dat het hier om een tegel gaat.
- `marmerglas` heet hier `gemarmerd glas`.
- `glasronden` staat onder [Butzenscheiben](https://thesaurus.cultureelerfgoed.nl/concept/cht:a603b7b4-afe2-4cbe-8fed-b89bdc6d570e/nl).
- `ijsbloemachtig` verwijst naar [berijpt glas](https://thesaurus.cultureelerfgoed.nl/concept/cht:1ae0fcc2-6598-4e92-823d-a97436163cbe/nl).
- `ossenoog` staat niet in de thesaurus, dit verwijst naar de vorm van het raam.
- `cilinderglas` staat binnen de thesaurus gegeven als een subcategorie van `vlakglas`. In de hiërarchische structuur van de termen in de [erfgoedthesaurus](https://thesaurus.cultureelerfgoed.nl/concept/cht:dcc2121b-8394-44f7-9664-86b109d079a4/nl) staat cilinderglas daarmee een niveau lager dan `marmerglas`, hetgeen problematisch kan zijn. Het is raadzaam om bij het gebruiken van referentielijsten termen te gebruiken die op hetzelfde niveaus van specificiteit liggen.

::::
:::

Concluderend, referentielijsten en publieke thesauri kunnen helpen bij het waarborgen van de datakwaliteit.
Door expliciet te zijn over wat we bedoelen met een bepaalde waarde, voorkomen we verwarring.

Publieke Thesauri zoals de RCE erfgoed thesaurus hebben bovendien nog een paar voordelen:

- De URL die verwijst naar een bepaalde term blijft stabiel, ook al verandert de naam. 
Voorbeeld: het gebruik van een term als `De gouden eeuw` is beladen en zou vervangen kunnen worden door een meer feitelijke term als de `17e eeuw`. Wanneer we besluiten dat collectief te doen voldoet een verandering in de thesaurus om alle gegevens up te daten. De URL's blijven onveranderd.
- Andere talen hebben vergelijkbare thesauri en omdat alles gestandaardiseerd is, kun je de termen in verschillende talen aan elkaar linken.
Zo kan je gemakkelijk datasets over glas uit verschillende landen met elkaar vergelijken wat tot nieuwe inzichten kan leiden. 

::: callout
Een thesaurus heeft unieke webadressen, ook wel [URIs](https://nl.wikipedia.org/wiki/Uniform_resource_identifier) genoemd, voor iedere term. 

Voor bijvoorbeeld `vlakglas` is dat [https://data.cultureelerfgoed.nl/term/id/cht/963156e3-7f49-4073-ab86-cea592518c26](https://data.cultureelerfgoed.nl/term/id/cht/963156e3-7f49-4073-ab86-cea592518c26) (deze vind je onderaan bij de erfgoedthesaurus **Internetadres van de resource** bij [`vlakglas`](https://thesaurus.cultureelerfgoed.nl/concept/cht:963156e3-7f49-4073-ab86-cea592518c26/nl) ). 

Voor `ijsglas`is dat [https://data.cultureelerfgoed.nl/term/id/cht/0caa0539-e7db-4bfa-9150-bc3a64d6dc3a](https://data.cultureelerfgoed.nl/term/id/cht/0caa0539-e7db-4bfa-9150-bc3a64d6dc3a). Wanneer je met referentielijsten in spreadsheet software werkt is het raadzaam deze unieke URI te gebruiken en hieraan toe te voegen.

:::



::::::::::::::::::::::::::::::::::::: keypoints 
- Gebruik data validatie om datakwaliteit te waarborgen tijdens data verzameling.
- Gebruik data filtering voor een snelle datacontrole.
- Maak het zo expliciet mogelijk wat er met bepaalde waardes in een dataset wordt bedoeld.
Referentielijsten en publieke thesauri kunnen daarbij helpen en zorgen dat data beter doorzoekbaar worden.
::::::::::::::::::::::::::::::::::::::::::::::::
