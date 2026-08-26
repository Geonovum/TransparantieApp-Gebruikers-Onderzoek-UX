
# Introductie

De overheid verwerkt dagelijks enorme hoeveelheden persoonsgegevens ten behoeve van besluitvorming. Hoewel er diverse technische standaarden bestaan voor het vastleggen van gegevensverwerking, zoals het Logboek Dataverwerkingen, blijft het voor burgers in de praktijk vaak onduidelijk welke data bij besluiten zijn gebruikt en waarom. Er bestaat een kloof tussen de technisch vastgelegde logging en de informatiebehoefte van de burger. Het toegankelijk en begrijpelijk maken van deze informatie, zonder de gebruiker te overvragen, vormt de kernuitdaging van dit UX-onderzoek.

Dit onderzoek richt zich op de ontwikkeling van de **TransparantieApp**: een interface die transparantie over datagebruik en besluitvorming biedt door complexe datastromen te vertalen naar voor de burger begrijpelijke 'gebeurtenissen'. In een simulatieomgeving onderzoeken wij hoe logbestanden, gebaseerd op open standaarden, kunnen worden ontsloten op een manier die aansluit bij de belevingswereld en de mentale modellen van diverse gebruikersgroepen. Het onderzoek maakt deel uit van een bredere initiatief om de standaard [<u>“data logboek verwerken”</u>](https://geonovum.github.io/logboek-dataverwerkingen-voor-objecten/) te ontwikkelen. Een belangrijke uitbreiding hierop is het onderdeel [<u>“Logboek Dataverwerkingen, extensie lezen”</u>](https://geonovum.github.io/TransparantieApp/). Aangezien deze standaard gelogde gegevens ook inzichtelijk maakt voor onder meer burgers, staat een optimale gebruikerservaring hierin centraal.

### Onderzoekskader

Dit document fungeert als de specifieke UX-rapportage van het project. Aangezien het project breder is dan alleen het ontwerp van de interface, maakt dit rapport onderdeel uit van een drieluik (inclusief Applicatie Architectuur en Gebruikersonderzoek). De focus in dit document ligt niet op de technische architectuur, maar op de menselijke ervaring: hoe presenteren we complexe datastromen aan de burger zonder hen te overvragen?

Gedurende het traject is een iteratieve, op de gebruiker gerichte ontwerpaanpak gevolgd. Door middel van kwalitatief onderzoek, co-creatie en usability-tests is inzicht verkregen in hoe transparantie effectief vormgegeven kan worden. De kern conclusie uit dit onderzoek is dat transparantie geen kwestie is van technische kwantiteit, maar van menselijke context. Het ontwerp resultaat, zoals in dit rapport beschreven, dient als blauwdruk voor het verder herstellen van het vertrouwen tussen de burger en de overheid.

## Probleemdefinitie

Binnen de overheid worden persoonsgegevens van burgers door verschillende organisaties geregistreerd, verwerkt en uitgewisseld. Deze gegevens spelen een rol binnen overheidsprocessen en kunnen bijdragen aan besluiten en uitkomsten die directe gevolgen hebben voor burgers. Voor burgers is echter niet altijd inzichtelijk hoe gegevens, regels en verschillende overheidsorganisaties binnen deze processen met elkaar samenhangen.

Onderzoek van Stichting Kafkabrigade laat zien dat problemen met overheidsdienstverlening niet uitsluitend binnen afzonderlijke organisaties of regelingen ontstaan. Juist de wisselwerking tussen verschillende regels, registraties en uitvoeringsorganisaties kan leiden tot situaties die voor burgers moeilijk te begrijpen of te voorspellen zijn. De afzonderlijke onderdelen van een proces kunnen vanuit organisatorisch perspectief correct functioneren, terwijl de gecombineerde uitkomst voor de burger problematisch is.

### **Onvoorspelbaarheid van inkomen door samenkomende regelingen**

In het onderzoek *Belasting onbekend* beschrijft Stichting Kafkabrigade situaties waarin burgers inkomsten ontvangen van meerdere uitbetalers. Verschillende partijen, zoals werkgevers, pensioenuitvoerders en het UWV, kunnen daarbij inhoudingen en heffingskortingen toepassen vanuit hun eigen positie binnen het proces. De uiteindelijke financiële situatie van de burger wordt echter bepaald door de samenhang tussen deze afzonderlijke inkomensstromen en fiscale regels.

Hierdoor ontstaat een informatieprobleem. Om de uiteindelijke gevolgen voor het inkomen te kunnen begrijpen en voorspellen, is inzicht nodig in de verschillende inkomensbestanddelen, toegepaste heffingskortingen en relevante regels. Deze informatie bevindt zich echter verspreid over verschillende organisaties en processen en is voor burgers niet eenvoudig als één samenhangend geheel te overzien.

Dit is problematisch omdat tegelijkertijd van burgers wordt verwacht dat zij tijdig wijzigingen doorgeven, financiële verplichtingen nakomen en indien nodig geld reserveren. Wanneer de benodigde informatie niet in samenhang beschikbaar is, kan het moeilijk zijn om vooraf te bepalen wat de financiële gevolgen van verschillende regelingen zijn. De Kafkabrigade beschrijft dat deze onvoorspelbaarheid kan leiden tot gevoelens van onzekerheid, machteloosheid, stress en angst. Ook voor experts kunnen dergelijke situaties moeilijk te controleren zijn.

Het probleem ligt daarmee niet uitsluitend in de complexiteit van fiscale regelgeving, maar ook in de beperkte mogelijkheid voor burgers om de gegevens en regels die hun persoonlijke situatie beïnvloeden in samenhang te begrijpen.

### **Gevolgen van een BRP-registratie voor toegang tot voorzieningen**

Een tweede voorbeeld betreft de Basisregistratie Personen (BRP). Voor burgers zonder vast woonadres, bijvoorbeeld als gevolg van woningnood, een scheiding of dakloosheid, kan inschrijving in de BRP problematisch zijn. Een adresregistratie heeft binnen de overheid echter een bredere functie dan uitsluitend het vastleggen van een woonadres.

De BRP vormt een belangrijke basis voor toegang tot verschillende rechten, diensten en voorzieningen. Problemen met een registratie kunnen daardoor gevolgen hebben voor onder andere verzekeringen, uitkeringen, stemrecht en officiële documenten. Een administratief probleem binnen één registratie kan zich daarmee doorzetten naar andere onderdelen van de overheid en aanzienlijke gevolgen hebben voor de persoonlijke situatie van een burger.

Voor burgers is niet altijd inzichtelijk hoe deze registraties en organisaties onderling met elkaar verbonden zijn. Hierdoor kan het moeilijk zijn om vast te stellen waar een probleem is ontstaan, welke gegevens daaraan ten grondslag liggen en welke organisatie verantwoordelijk is voor een bepaald onderdeel van het proces. In kwetsbare situaties kan dit ertoe leiden dat burgers worden uitgesloten van zorg, ondersteuning of andere voorzieningen.

### **Overkoepelend probleem**

Hoewel de twee voorbeelden betrekking hebben op verschillende domeinen, laten zij een vergelijkbaar onderliggend patroon zien. Overheidsdienstverlening is verdeeld over verschillende organisaties, registraties, regels en informatiesystemen, terwijl de gecombineerde gevolgen daarvan uiteindelijk bij de individuele burger samenkomen.

Voor afzonderlijke organisaties kan inzichtelijk zijn welke gegevens worden gebruikt en welke regels binnen het eigen proces worden toegepast. Voor burgers is dit totaalbeeld aanzienlijk moeilijker te verkrijgen. Informatie bevindt zich verspreid over verschillende organisaties en systemen, terwijl juist de samenhang tussen gegevens, regels en gebeurtenissen noodzakelijk kan zijn om te begrijpen hoe een bepaalde uitkomst tot stand is gekomen.

Daarbij bevatten bestaande vormen van overheidscommunicatie, zoals brieven en de Berichtenbox, niet altijd voldoende informatie om deze samenhang te reconstrueren. Burgers weten daardoor niet altijd welke gegevens zijn gebruikt, tussen welke organisaties gegevens zijn uitgewisseld en welke regels een rol hebben gespeeld bij een uitkomst.

Het centrale probleem is dat burgers onvoldoende begrijpelijk en samenhangend inzicht hebben in hoe hun persoonsgegevens binnen en tussen overheidsorganisaties worden gebruikt en hoe gegevens, regels en verschillende processen gezamenlijk bijdragen aan uitkomsten die hen raken. Hierdoor is het voor burgers moeilijk om te begrijpen hoe een uitkomst tot stand is gekomen, te controleren welke informatie daarbij een rol heeft gespeeld en te bepalen waar en wanneer zij moeten handelen.

Het gebrek aan transparantie en samenhang is daarmee niet uitsluitend een informatieprobleem, maar heeft ook invloed op het handelingsvermogen van burgers. Wanneer van burgers wordt verwacht dat zij verantwoordelijkheid nemen, wijzigingen doorgeven en op basis van overheidsinformatie handelen, is het noodzakelijk dat zij voldoende inzicht hebben in de gegevens en processen die hun persoonlijke situatie beïnvloeden.

## Doelstelling en onderzoeksvragen

Het doel van dit onderzoek is om in kaart te brengen hoe de TransparantieApp, oftewel Logboek Dataverwerkingen, extensie lezen, optimaal kan bijdragen aan het inzichtelijk maken van overheidsbesluiten en datagebruik voor de burger. Centraal staat hierbij de hoofdvraag:

**Hoe kan transparantie over datagebruik en besluitvorming door de overheid op een gebruiksvriendelijke manier worden vormgegeven, zonder burgers te overvragen met informatie, en aansluitend bij hun uiteenlopende behoeften?**

Om deze vraag te beantwoorden, zijn de volgende subvragen opgesteld:

**1. Behoeften & context van burgers**

> 1.1 Welke informatiebehoeften hebben burgers rondom datagebruik en besluitvorming?
>
> 1.2 In welke situaties ontstaat bij burgers daadwerkelijk de behoefte aan transparantie over hun gegevens (bijv. afwijzing, financiële gevolgen, bezwaar)?

**2. Begrip & taal**

> 2.1 Hoe ervaren burgers begrippen als “besluit”, “gegevensgebruik” en “datastromen”, en waar ontstaat verwarring tussen juridische en alledaagse betekenis?
>
> 2.2 Welke vormen van uitleg helpen burgers om besluiten beter te begrijpen zonder juridische of technische voorkennis?

**3. Information overload & UX**

> 3.1 Welke UX-patronen worden gebruikt om complexe informatie en data begrijpelijk te presenteren zonder een overvloed aan informatie te veroorzaken?
