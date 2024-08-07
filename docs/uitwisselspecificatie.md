# Uitwisselmodel

## Inleiding

De uitwisselspecificatie specificeert welke gegevens en in welke vorm de gegevens aan het CBS aangeleverd dienen te worden. Hiertoe is een specificatie in [JSON-schema](https://json-schema.org) gespecificeerd. De inhoud van deze JSON-schema is afgeleid van het [informatiemodel schuldhulpverlening](./rapport_1.md).

De uitwisselspecificatie kent de volgende opbouw: 

1. Op het hoofdniveau is het Uitwisselmodel gedefinieerd met een aantal attributen opgenomen die informatie geven over de levering: start- en einddatum van de levering en de aanleverdattum en tijd;
2. Op het tweede niveau is het mogelijk gemaakt meerdere leveringen in te voegen. Dit maakt het mogelijk voor cloud-leveranciers voor meerdere schuldhulpverlenende organisaties in 1 bestand aan te leveren, **mits daar natuurlijk toestemming voor is afgegeven**. 
3. Op het derde niveau wordt per levering de aanleverende [schuldhulporganisatie](./rapport_1.md/#organisaties) met de bijbehorende schuldhultrajecten aangeleverd. Er wordt vanuit gegaan dat er petr levering steeds door precies één schuldhulporganisatie gegevens wordenn aangeleverd. 
4. Op detailniveau wordt een aantal schuldhultrajecten aangeleverd. Dit met de verschillende fases die de trajecten hebben doorlopen volgens het [procesmodel](./rapport_1.md/#processen), en de [client(en)](./rapport_1.md/#clienten) die het betreft, met hun leefsituatie. Per client worden de schulden opgegeven. Per traject wordt ook de gemeente opgegeven die verantwoordelijk is voor het schuldhulptraject.

Aan het eind van de specficatie staan de gebruikte datatypes en waardenlijsten (enumeraties) die worden gebruikt opgenomen. 

## Uitwisselspecificatie

Onderstaand de definitie van de uitwisselspecificatie. Van deze definitie is ook een [downloadversie](https://raw.githubusercontent.com/brienen/ddas/main/v0.9/json_schema_Uitwisselmodel.json) beschikbaar.

```
{!../v0.9/json_schema_Uitwisselmodel.json!}

```

## Voorbeelden

### Enkelvoudig voorbeeld

Onderstaand een voorbeeld JSON-bestand conform de uitwisselspecificatie, waarbij slechts 1 traject wordt aangeleverd. Dit voorbeeld kun je ook [downloaden](https://raw.githubusercontent.com/brienen/ddas/main/v0.9/enkelvoudigVoorbeeld.json).

```
{!../v0.9/enkelvoudigVoorbeeld.json!}

```

### Meervoudig voorbeeld

Onderstaand een voorbeeld JSON-bestand conform de uitwisselspecificatie, waarbij meerdere trajecten worden aangeleverd. Dit voorbeeld kun je ook [downloaden](https://raw.githubusercontent.com/brienen/ddas/main/v0.9/meervoudigVoorbeeld.json).

```
{!../v0.9/meervoudigVoorbeeld.json!}

```

### Samenloop voorbeeld

Het komt voor dat gemeenten een deel van de dienstverlening aan een schuldhulpverlenende partij heeft uitbesteed. In een dergelijk geval worden er door meerdere schuldhulpverleners aanleveringen gedaan over dezelfde clienten in dezelfde periode. Onderstaand twee voorbeeld JSON-bestanden conform de uitwisselspecificatie, waarbij meerdere trajecten worden aangeleverd. Deze voorbeeld kun je ook [downloaden deel 1](https://raw.githubusercontent.com/brienen/ddas/main/v0.9/samenloopVoorbeeldDeel1.json) en [downloaden deel 2](https://raw.githubusercontent.com/brienen/ddas/main/v0.9/samenloopVoorbeeldDeel2.json).

#### Samenloop bestand 1
```
{!../v0.9/samenloopVoorbeeldDeel1.json!}

```

#### Samenloop bestand 2

```
{!../v0.9/samenloopVoorbeeldDeel2.json!}

```
