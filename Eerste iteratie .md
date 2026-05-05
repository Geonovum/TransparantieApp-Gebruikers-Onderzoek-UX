# Eerste iteratie 

## Ideate
### Inzichten uit literatuuronderzoek

Uit het bestudeerde literatuuronderzoek komen een aantal terugkerende thema’s naar voren:

- Burgers worden geconfronteerd met een versnipperd landschap van instrumenten voor privacy en transparantie, die elk slechts een deel van hun rechten ondersteunen. Dit leidt tot onoverzichtelijkheid en verwarring.
- Inzage- en correctierechten zijn vaak wel geregeld, maar informatie over waarom gegevens worden gebruikt en hoe deze bijdragen aan besluiten ontbreekt veelal.
- Er bestaat geen gestandaardiseerde aanpak voor het inzichtelijk maken van gegevensuitwisseling en besluitvorming over organisatiegrenzen heen.
- Veel toepassingen zijn ontworpen vanuit het perspectief van de organisatie, en minder vanuit de klantreis en informatiebehoefte van de burger.
- Digitale ongelijkheid speelt een belangrijke rol: niet alle burgers beschikken over gelijke digitale vaardigheden of toegang tot digitale middelen.

Opvallend is dat de behoefte aan transparantie bij burgers vaak situationeel is. Zolang processen probleemloos verlopen, bestaat er doorgaans weinig actieve interesse in het gebruik van gegevens. De behoefte aan inzicht ontstaat vooral wanneer besluiten negatieve gevolgen hebben, zoals financiële consequenties of afwijzingen. Dit lijkt samen te hangen met een relatief hoog basisvertrouwen in de overheid, mede versterkt door positieve ervaringen met voorzieningen als DigiD.

### Interview VO-Rijk app

De VO-Rijk App (Rijksapp) is een initiatief binnen de digitalisering van de Nederlandse overheid dat gericht is op het centraliseren en vereenvoudigen van digitale dienstverlening voor burgers. Binnen de financiële sector is dit bijzonder relevant, omdat veel overheidsprocessen direct invloed hebben op de financiële situatie van burgers, bijvoorbeeld belastingen, toeslagen en uitkeringen. De Rijksapp brengt communicatie, informatie en acties samen op één plek, waardoor gebruikers minder afhankelijk zijn van verschillende systemen en beter overzicht krijgen. Gezien het één van de meest vooraanstaande partijen is die transparantie gebruikt in haar app, hebben wij een casus gemaakt van haar designs, methodiek en visie.

Hieronder verkennen wij de opbouw en UX-patronen van de app.

#### Activatieflow van de VO-Rijk App

De Rijksapp maakt gebruik van een op DigiD gebaseerde activatieflow om gebruikers op een betrouwbare en uniforme manier toegang te geven tot aangesloten overheidsdiensten. Deze activatieflow is vergelijkbaar met andere rijksbrede applicaties, zoals [MijnOverheid](https://mijn.overheid.nl/), en sluit aan bij [bestaande afspraken rondom identiteit, authenticatie en autorisatie](https://gitdocumentatie.logius.nl/publicatie/dk/idauth/1.5.0/).

De DigiD-activatieflow binnen de Rijksapp heeft als doel om:

- de identiteit van de gebruiker vast te stellen via DigiD;

- de app veilig te activeren op een specifiek apparaat;

- een technische vertrouwensrelatie op te bouwen tussen gebruiker, app en dienst;

- het mogelijk te maken dat gebruikers namens zichzelf vragen kunnen stellen aan overheidsorganisaties, waarbij duidelijk is wie de afzender is en waar het antwoord naartoe moet.

De activatieflow vormt daarmee een essentiële randvoorwaarde voor het veilig en gecontroleerd gebruik van de Rijksapp.

#### Lokale appbeveiliging

Na installatie van de Rijksapp stelt de gebruiker een persoonlijke pincode in. Deze pincode fungeert als lokale beveiligingsmaatregel en beschermt de app en de daarin opgeslagen gegevens tegen ongeautoriseerd gebruik.

De pincode staat los van de DigiD-inloggegevens en wordt uitsluitend gebruikt om toegang te krijgen tot de app op het betreffende apparaat.

#### Identificatie via DigiD

Na het instellen van de pincode start de gebruiker de activatie via DigiD. Hiervoor wordt de gebruiker doorgestuurd naar de standaard DigiD-inlogflow. Dit kan plaatsvinden op hetzelfde apparaat of via een ander apparaat of browser waarop de DigiD-app actief is.

De DigiD-authenticatie vindt volledig buiten de Rijksapp plaats. De app ontvangt geen inloggegevens, maar uitsluitend een bevestiging dat de authenticatie succesvol is afgerond.

#### Activatie van de dienst

Na een succesvolle DigiD-authenticatie wordt de Rijksapp geactiveerd. In deze stap wordt binnen de achterliggende infrastructuur een certificaat of token aangemaakt dat:

- gekoppeld is aan de geauthenticeerde gebruiker;

- gekoppeld is aan de Rijksapp als kanaal;

- gebruikt kan worden om communicatie met overheidsorganisaties te autoriseren.

Voor de gebruiker wordt deze stap zichtbaar gemaakt via een bevestigingsscherm waarin staat dat de app succesvol is geactiveerd en klaar is voor gebruik.

#### Functionele betekenis van de activatie

Na activatie kan de gebruiker binnen de Rijksapp:

- aangesloten overheidsorganisaties selecteren;

- vragen of verzoeken indienen;

- informatie opvragen of ontvangen.

Bij het versturen van een vraag wordt het certificaat dat tijdens de activatie is verkregen meegestuurd. Hierdoor kan de ontvangende organisatie vaststellen dat de vraag afkomstig is van een geauthenticeerde gebruiker en waar het antwoord naartoe gestuurd moet worden, zonder dat direct persoonsgegevens zoals het BSN worden gedeeld.

### UX-structuur: Overzicht en Dossiers

De VO-Rijk app kent een duidelijke opdeling in twee hoofdonderdelen: Overzicht en Dossiers.

**Overzicht** : Het Overzicht is gericht op wat de gebruiker op dit moment moet doen. Het is een actiegerichte weergave die de gebruiker helpt inzicht te krijgen in:

- lopende zaken

- benodigde acties

- prioriteiten (zoals betaalverzoeken)

Uit gebruikersonderzoek blijkt dat gebruikers het woord "overzicht" beter begrijpen dan "inzicht". Het kan worden gezien als een dashboard waarin de meest relevante informatie centraal staat.

**Dossiers**:  Dossiers bevatten alle informatie en data rondom een specifieke zaak. Dit omvat:

- gegevens

- communicatie;

- status van het dossier.

Het dossier fungeert als de inhoudelijke en volledigere weergave van informatie.

### Onderzoeksmethoden (UX)

Binnen de ontwikkeling van de Rijksapp is sterk iteratief gewerkt. Hierbij zijn aannames continu getest en gevalideerd.

Gebruikte methoden:

- A/B-testen om te bepalen welke componenten en informatie noodzakelijk zijn;

- card sorting om te onderzoeken welke termen gebruikers begrijpen;

- het testen van prototypes en deze vervolgens "uitkleden" door alleen de relevante onderdelen te behouden.

Een belangrijk uitgangspunt hierbij is dat elk onderdeel van de interface moet bijdragen aan begrip en relevantie voor de gebruiker.

### Klantreis en informatiepositie van de burger

De huidige situatie voor burgers is complex:
- informatie is verspreid over meerdere applicaties;

- gebruikers moeten zelf navigeren tussen systemen;

- fouten in data kunnen doorwerken in verschillende systemen zonder dat dit zichtbaar is.

Dit leidt tot een zwakke informatiepositie voor de burger.

De visie van de Rijksapp is daarom:

De burger hoeft niet te reizen; de informatie komt naar de burger.

Dit impliceert dat ook transparantie-informatie idealiter binnen de Rijksapp beschikbaar is, zodat gebruikers niet afhankelijk zijn van meerdere systemen.

Boeken zoals [\*De Digitale Kooi\*](https://digitalekooi.kafkabrigade.nl/) en [\*Volwassen Digitale Overheid\*](https://vdo.kafkabrigade.nl/) beschrijven hoe:

- slechte informatiearchitectuur burgers kan benadelen;

- fouten in data doorwerken in ketens van systemen;

- zowel burgers als organisaties onvoldoende zicht hebben op deze processen.

Er ontstaat een "black box" waarin:

- data wordt gedupliceerd

- verbanden onzichtbaar zijn

- fouten moeilijk te herleiden zijn


## Define 
### Doelgroepen en verschillen in informatiebehoefte

Op basis van literatuur en gesprekken zijn grofweg drie doelgroepen te onderscheiden:

- **De actieve inzagezoekende burger**, die expliciet wil weten welke gegevens zijn gebruikt en hoe deze hebben bijgedragen aan een besluit.
- **De pragmatische, vertrouwende burger**, die uitgaat van een goed functionerende overheid en pas behoefte krijgt aan inzicht wanneer iets misgaat.
- **De kwetsbare burger**, waaronder ouderen, mensen met een beperking en sommige groepen immigranten, die vaker drempels ervaren in digitale dienstverlening.

Deze groepen verschillen sterk in hun informatiebehoefte, taalgebruik en mate van regie die zij wensen. Waar de ene burger behoefte heeft aan detail en controle, zoekt de andere vooral bevestiging dat processen correct verlopen en duidelijke handelingsperspectieven wanneer dat niet het geval is.


### Aansluiting TransparantieApp en Rijksapp

De Rijksapp werkt met dossiers die bestaan uit meerdere gebeurtenissen. De TransparantieApp kan hierop aansluiten door:

- per gebeurtenis een tijdlijn te tonen;

- inzicht te geven in samenhang en gevolgen van gebeurtenissen;

- complexe processen begrijpelijk te maken.

Dit kan zowel als aparte applicatie worden ontwikkeld, als geïntegreerd binnen de Rijksapp zelf.

Waar de Rijksapp zich richt op overzicht en dossiers, kan de TransparantieApp een extra laag toevoegen: inzicht in gebeurtenissen en geschiedenis.

#### Inzichtlaag

Deze laag richt zich op vragen als:

- wat is er gebeurd met mijn gegevens?

- welke stappen zijn genomen?

- hoe werken verschillende systemen en organisaties op elkaar in?

Per dossier kan een tijdlijn van gebeurtenissen worden toegevoegd:

- een beknopt overzicht op hoofdlijnen;

- een gedetailleerdere weergave van onderliggende processen.

#### Architectuur- en designimplicaties

Voor het ondersteunen van transparantie is het nodig om:

- een API te ontwikkelen voor het ontsluiten van gebeurtenissen;

- een designsysteem op te zetten voor het visualiseren van data, gebeurtenissen en beslissingen.

Hiermee kunnen:

- afzonderlijke transparantie-oplossingen worden gebouwd;

- bestaande apps deze functionaliteit integreren.

Belangrijke vragen voor het ontwerp zijn:

- wanneer is bepaalde informatie relevant voor de gebruiker?

- hoe maak je ketens en oorzaak-gevolgrelaties inzichtelijk?

- hoe voorkom je dat informatie te complex of overweldigend wordt?

- welke informatie is wel of niet relevant voor burgers?

Dit vormt de kern van de designuitdaging.

###  Hypotheses voor ontwerp en standaardisatie

De beschreven gebruikerswensen leiden tot een aantal aandachtspunten voor de TransparantieApp en de standaard voor het lezen van logging:

- Transparantie moet waarschijnlijk gelaagd worden aangeboden, zodat gebruikers zelf kunnen bepalen hoeveel detail zij willen zien.
- Uitleg dient aan te sluiten bij het taalgebruik en de belevingswereld van burgers, en niet uitsluitend bij juridische of technische definities.
- De app moet rekening houden met stressvolle gebruikssituaties, waarin burgers grip zoeken en snel willen begrijpen wat er is gebeurd en wat zij kunnen doen.
- Een standaard aanpak is nodig om informatie over dataverwerkingen consistent en vergelijkbaar te presenteren, maar mag niet leiden tot een one-size-fits-all benadering die onvoldoende ruimte laat voor gebruikersverschillen.

Deze inzichten vormen input voor vervolgonderzoek en het ontwikkelen van prototypes, die gebruikt zullen worden om aannames te toetsen en gebruikerswensen verder te verfijnen.

## Realize


## Evaluate 


