# Documentation
# Inhoud

[User stories](#User-stories)

[C4 model](#C4-model)

[C1 Context](#C1-Context)

[C2 Containers](#C2-Containers)

[Conceptueel model](#Conceptueel-model)

[Front-end development](#Front-end-development)

[Keuze front-end](#Keuze-front-end)

[Back-end development](#Back-end-development)

[Data behoud](#Data-behoud)

[UX design](#UX)

# User stories
#### 1. Als gebruiker wil ik een overzicht kunnen zien van alle boeken om te kunnen zien welke boeken ik uit kan kiezen. 
Acceptatiecriteria:  
- Ik kan de titel/auteur en omslagafbeelding van een boek zien.  
- Er is een melding als er geen boeken worden gevonden.

#### 2. Als gebruiker wil ik de informatie van een boek kunnen bekijken om meer over het boek te weten te komen. 
Acceptatiecriteria:
- Ik alle informatie van dit boek zien.
- Ik kan zien wat andere gebruikers van dit boek vinden.
- Ik kan zien of dit boek tot mijn favorieten toebehoort.
- Er is een melding als het boek niet kan worden gevonden.

#### 3. Als gebruiker wil ik een boek als favoriet kunnen toevoegen zodat ik het boek kan bewaren en makkelijk terugkijken. 
Acceptatiecriteria:
- De gebruiker kan een boek toevoegen als favoriet.
- Er wordt getoond wanneer een boek een favoriet boek is.

#### 4. Als administrator wil ik boeken kunnen toevoegen om nieuwe boeken op de site te zetten die gebruikers kunnen bekijken. 
Acceptatiecriteria:
- De informatie van een nieuw boek kan worden ingevuld.
- De informatie wordt gecontroleerd of deze in de juiste vorm staat.
- Er is een melding wanneer er iets mist/wanneer dit in de foute vorm staat.

#### 5. Als administrator wil ik boeken kunnen aanpassen om incorrecte/gewijzigde informatie van een boek bij te werken. 
Acceptatiecriteria:
- Er kunnen wijzigingen gemaakt worden aan de informatie van een boek.
- Er is een melding wanneer er iets mist/wanneer dit in de foute vorm staat.

#### 6. Als administrator wil ik boeken kunnen verwijderen om ongeldige boeken van de site te halen.
Acceptatiecriteria:
- Boeken kunnen worden verwijderd.
- Er is een melding die toont dat het boek is verwijderd.

#### 7. Als gebruiker wil ik een boek kunnen beoordelen zodat ik mijn mening over het boek kwijt kan. 
Acceptatiecriteria:
- Je kunt een comment achter laten op een boek.
- De comments worden bij het juiste boek opgeslagen.
- Er wordt gecontroleerd of alle velden zijn ingevuld en geldig zijn.
- Er is een melding wanneer er iets mist/wanneer dit in de foute vorm staat.

#### 8. Als gebruiker wil ik mijn favorieten (favoriete boeken) kunnen bekijken, zodat ik een makkelijk inzicht heb over de boeken die ik heb gelezen/wil gaan lezen. 
Acceptatiecriteria:
- Je kunt je favoriete boeken bekijken.
- Er is een melding als er geen favorieten zijn.


# C4 model
Om duidelijk te maken welke onderdelen ik allemaal wil gaan maken voor mijn project heb ik gebruik gemaakt van de C4-methode. De methode wordt gebruikt om de software architectuur overzichtelijk in kaart te brengen. De C4 methode bestaat uit 4 diagrammen, waarbij ieder diagram dieper ingaat op de software. Ik heb de eerste 2 diagrammen hiervan gemaakt.
## C1 Context
Zie onderstaand diagram voor de context van dit systeem.

![image](https://user-images.githubusercontent.com/101703190/164194501-3a4f7cd2-2d9c-44e4-9d8e-482102e9bdff.png)

## C2 Containers
Als we verder gaan inzoomen op het software systeem kun je zien dat het uit verschillende componenten (containers) bestaat. Deze kun je in het onderstaande diagram zien.

![image](https://user-images.githubusercontent.com/101703190/164194560-ef2cd31a-e03f-4554-8ab4-366ca3ada5e7.png)

# Conceptueel model

![image](https://user-images.githubusercontent.com/101703190/164194584-129f9398-fc38-4ed0-9463-e38107cd849f.png)

Met dit conceptueel model kunnen we duidelijk maken welke entiteiten ik in mijn applicatie wil hebben. We kunnen hierin bijvoorbeeld zien dat een Novel (boek) een van de hoofdonderdelen van de applicatie is. Verder kun je zien wat de relaties tussen deze entiteiten zijn.


# Front-end development
Voor de front-end van mijn applicatie ga ik een JavaScript framework gebruiken. 



Ik heb gekeken naar 3 potentiële JavaScript frameworks: 

- React 
- Angular 
- Vue.js 
![image](https://user-images.githubusercontent.com/101703190/164194620-6e69513b-0640-4222-8f88-06b160ad67ea.png)

Deze 3 frameworks worden genoemd op de canvas course als de meest populaire frameworks om te gebruiken en volgens Google is dit ook het geval. 

Om een beslissing te kunnen maken over welk JavaScript framework ik wil gaan gebruiken heb ik naar de voor- en nadelen van ieder framework gekeken. 

### React 
Voordelen: 
- Goed leesbare code en makkelijk te debuggen. 
- Gebruikt een virtuele DOM, hierdoor kan gewijzigde data snel worden geladen op de pagina. 
- Gebruikt JSX, dit is vergelijkbaar met HTML en dus duidelijk te lezen. 
- Componenten zijn herbruikbaar. 

Nadelen: 
- Documentatie zou beter kunnen volgens developers (<https://talentopia.global/front-end/the-pros-and-cons-of-the-most-used-javascript-frameworks>) 
### Angular 
Voordelen: 
- Uitgebreide documentatie 
- Gebruikt Typescript, dit lijkt veel op andere OOP-talen zoals C#. 

Nadelen: 
- Beperkte vrijheid in het organiseren van code. 
- Moeilijker te leren.(<https://www.imaginarycloud.com/blog/angular-vs-react/>) 
### Vue.js 
Voordelen: 
- Gebruikt een virtuele DOM, hierdoor kan gewijzigde data snel worden geladen op de pagina. 
- Het is makkelijk om animatie toe te voegen. 
- HTML-template. 

Nadelen: 
- Is comfortabel als je bekent bent met JavaScript. 
- Het is erg nieuw, waardoor er weinig support is. 
## Keuze front-end
Ik heb er uiteindelijk voor gekozen om React te gaan gebruiken. Deze is het meest populair bij andere developers. Hierdoor ben ik van mening dat dit een goede keuze kan zijn voor mij als beginner, omdat dit laat zien dat het een vertrouwd framework is dat veel gebruikt wordt.
Er staat wel als nadeel dat de documentatie beter zou kunnen, maar ik denk niet dat ik hier veel last van zal gaan krijgen aangezien ik waarschijnlijk niet veel dingen er mee gaan doen die niet goed gedocumenteerd staan.


# Back-end development
De back-end van software is de code die wordt uitgevoerd door de computer zonder dan een gebruiker erbij kan of deze direct kan aansturen. De back-end zit, zoals de naam ook al aangeeft achter de front-end. De back-end is ervoor gemaakt om met de database te communiceren. Wanneer er in de front-end data wordt opgevraagd haalt de back-end deze op uit de database en omgezet in juiste vorm en geeft de back-end deze gegevens terug aan de front-end.

Bij het maken van de back-end moet ik ook een keuze maken uit welk framework ik hiervoor wil gaan gebruiken. Op canvas staat dat we de keuze moeten maken uit het gebruiken van Java, of .NET frameworks. Dit zijn dan ook degene waaruit ik een keuze heb gemaakt.

Ik heb ervoor gekozen om .NET te gebruiken voor mijn back-end, omdat ik het vorige semester al met C# gewerkt heb en ik dit een fijne taal vond. Verder wilde ik hier ook nog meer over leren en heb hier dus ook voor gekozen om mijzelf er meer in te kunnen verdiepen.

Ten slotte heb ik er ook voor .NET gekozen omdat het mij mooi leek om de back-end in Visual Studio  te maken en de front-end in Visual Studio Code. Hiermee heb ik namelijk ook zelf al gelijk een mooie splitsing tussen verschillende onderdelen binnen mijn software.


# Data behoud
Met data behoud bedoelen we het opslaan van gegevens die zijn aangemaakt door de gebruiker of het systeem, zodat we deze gegevens later kunnen ophalen, bijwerken of verwijderen. 
Het doel van data behoud is dat wanneer je de applicatie afsluit data blijft bestaan. Deze data moet dus ergens ‘permanent’ worden opgeslagen.

Het opslaan van data kan op verschillende manieren, zoals:

- In-memory. Data die in-memory wordt opgeslagen verdwijnt echter als deze wordt afgesloten en dit willen we niet. Wel kunnen we in memory gebruiken om unit tests uit te voeren, zodat we de kwaliteit van de software kunnen aantonen.
- Disk-based. Data wordt opgeslagen op een SSD/HDD van een server

Deze disk-based methode houdt in dat er een database wordt gebruikt. Hierin wordt de data zo opgeslagen dat we deze later nog kunnen bekijken, bewerken en kunnen verwijderen.

Volgens <https://insights.stackoverflow.com/survey/2021#section-most-popular-technologies-databases> zijn de volgende databases het meest populair:

- MySQL
- PostgreSQL
- SQLite
- MongoDB
- Microsoft SQL server

Om eenvoudig met de database te kunnen werken zijn er ORM’s gemaakt (Object-Relational-Mapping). Een ORM zorgt ervoor dat je geen SQL hoeft te gebruiken in je code, maar direct een object in dezelfde taal als waarmee je werkt gebruikt.

Enkele voordelen van een ORM zijn: testbaarheid en herbruikbaarheid.

Het is dus belangrijk om een ORM te zoeken die past bij mijn back-end. 

Ik heb ervoor gekozen om Entity Framework Core te gebruiken. Dit is namelijk een veelgebruikte ORM voor ASP.NET Core projecten. Ik had hier ook duidelijke documentatie over gevonden (<https://www.entityframeworktutorial.net/efcore/entity-framework-core.aspx>) waarin staat hoe ik dit kan gebruiken. Het fijne van Entity Framework is dat het eenvoudig is om migraties te maken en dus met de database te verbinden. Ook heb je voor Entity Framework een handige In-memory package. Deze kan worden gebruikt om de applicatie te testen. Het in-memory testen is nog eens extra fijn door data-seeding, wat ik gebruik om snel data toe te kunnen voegen aan de database.

# UX
Om ervoor te zorgen dat mijn applicatie user friendly is, ga ik ervoor zorgen dat het simpel is om gebruik te maken van mijn website.

### User friendly
![image](https://user-images.githubusercontent.com/101703190/170964468-841bb9c0-a785-4c29-836a-09a514ca9981.png)
Hierboven kun je zien hoe de homepage van mijn front-end eruit ziet.
Ik heb hier wat test voorbeeld die worden getoond.
Je kunt zien dat alle boeken op een rij staan en dat het duidelijk is welke boeken er zijn.
Als je meer informatie wilt hebben over een boek kun je op de cover-afbeelding klikken.
Hierdoor is het gemakkelijker voor de gebruiker om door te klikken, omdat je niet op een klein veld hoeft te klikken.
Een ander punt wat ik hierin heb meegenomen is hoeveel boeken er tegelijk zichtbaar zijn.
Ik heb ervoor gekozen om 6 boeken op een rij te plaatsen.
Hierdoor zijn de titels en hun cover goed zichtbaar en niet te klein, maar tegelijk ook niet zo groot dat ze het hele scherm innemen.

### Website doorlopen
Ik vind het ook belangrijk dat het makkelijk is om door website heen te lopen.
Dit houdt in dat je niet tientallen keren moet klikken om op de juiste pagina te komen.
Dit is voor mij gelukkig niet echt een probleem, omdat ik niet zo'n grote website heb, maar ik wil hier alsnog rekening mee houden.
Om ervoor te zorgen dat dit simpel gaat kun je direct op de titel van het boek en de cover klikken om naar de informatie van het boek te gaan.
Verder kun je altijd terug naar wat overzichtspaginas door de links in de navigatiebalk te gebruiken.
Door de links in de navigatiebalk is het voor de gebruiker eenvoudig en snel om op de juiste pagina te komen.

### Laadsnelheid
Een ander punt waar ik rekening mee wil houden bij het maken van mijn front-end, is de laadsnelheid van pagina's en performance van de website.
Om een idee te krijgen over hoe het hiermee is, heb ik gebruik gemaakt van Google Lighthouse [Link chrome extensie](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=nl)
![image](https://user-images.githubusercontent.com/101703190/170966941-4c5a4d16-562b-41cb-a490-09161b91d3c0.png)

Hierboven kun je een deel van het report zien.
In dit report kun je zien hoelang mijn webpagina erover doet om te laden, verder kun je dit soort tools gebruiken om de code verder te optimaliseren.
Hierdoor wordt de website sneller, wat voor een gebruiker een stuk fijner is.

