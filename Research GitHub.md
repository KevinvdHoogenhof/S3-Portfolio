# Research GitHub 

## Inleiding 
Git is een populair gereedschap voor programmeurs. 
Het helpt om de verschillende versies van je broncode beter te beheren. 
Maar wat doen versiebeheersystemen precies, voor wie zijn ze bedoeld en hoe kun je ze gebruiken? Kortom: hoe werkt GitHub? 
[Bron](https://techacademy.id.nl/blog/hoe-werkt-github/) 
GitHub wordt door heel veel mensen gebruikt om hun project goed te onderhouden, maar hoe welke dingen kun je hier nou zelf mee doen? 

## Onderzoeksvraag 
Hoe kan ik GitHub gebruiken om mijn project te managen? 

## Hoe kun je GitHub issues gebruiken om user stories bij te houden?
GitHub Issues is een handige manier om je user stories bij te houden en te weten wat je nog allemaal moet/ wilt gaan doen binnen jouw project. 
Doordat GitHub issues geïntegreerd is met GitHub zijn er ook een hoop handige functies waar je gebruik van kunt maken. 
Je kunt bijvoorbeeld issues koppelen aan pull requests of een branch. 
Hierdoor is het heel handig om je werkt in de gaten te houden en te vinden wat wat doet. 
Ook kun je hierdoor snel zien wat al is gemaakt en hoef je niet eerst naar een ander planbord toe om daar het issue als afgerond af te vinken. 
Je kunt dit namelijk direct doen door dit bepaalde issue te sluiten bij de pull request, als deze dan wordt goedgekeurt en gemerged wordt hij vanzelf gesloten.  

Een ander groot voordeel van GitHub issues is dat het ook mogelijk is hierin de issues (bugs/enhancements etc.) erin kunt zetten, waardoor je snel problemen kunt vinden. 

Ten slotte kun je ook nog een project bord aanmaken, waarop je heel snel alle relevante issues (user stories) aan toe kunt voegen, 
om een nog beter overzicht te krijgen van hoe het project ervoor staat.    
[Bron: GitHub](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues) 

## Hoe kun je nieuwe code toevoegen in jouw project? 
Een andere nuttige functie binnen GitHub zijn de branches.
Je kunt nieuwe code die je schrijft naar een branch toe pushen.
Een branch kan worden gebruikt om nieuwe functies te ontwikkelen, bugs te fixen of dingen uit te proberen. 
Dit doe je dan binnen een losse omgeving, waardoor je makkelijk terug kunt naar hoe het eerst was als iets niet werkt of bijvoorbeeld niet zo is als je had gedacht.   

Binnen een project is er altijd een hoofd-branch, dit wordt vaak de main/master branch genoemd. 
Deze branch wordt getoond wanneer iemand jouw repository bezoekt.  

Wanneer iemand een nieuwe functie maakt op een andere branch wordt dit via een merge naar de main branch toegebracht. 
Alle wijzigingen worden dan toegepast op de main branch. 
Onder GitHub issues zijn wij er ook al achter gekomen dat je een issue aan branch kunt koppelen. 
Binnen een project kun je branches dus ook handig gebruiken om een functie te maken in een bepaalde branch. 
Hiermee is het dan ook gelijk overzichtelijk waar een branch voor is.    
[Bron: GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches) 

## Hoe voegen we code van verschillende branches samen?
Om branches samen te kunnen voegen moet je ze met elkaar mergen. 
Hierbij worden de gemaakte wijzigingen toegepast op een andere (vaak dus de main) branch.  

Om ervoor te zorgen dat je niet zomaar branches met elkaar kunt mergen kun je een protected branch aanmaken. 
Hiermee kun je ervoor zorgen dat je bijvoorbeeld niet zomaar met de main branch kunt mergen. 
In plaats van een directe merge, zou je dan een pull request aan moeten maken. 
Hierin wordt dan eerst gekeken of alles correct is, en als dit zo is, kan de pull request worden goedgekeurt, 
waardoor de wijzingen in de main branch kunnen worden gemerged.  
[Bron: GitHub](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github) 

## Hoe kunnen we het samenvoegen van code controleren? 
Zoals ik ook al beschreef bij het mergen kun je binnen GitHub pull requests aanmaken, maar wat houdt dit nou in?  

Een pull request wordt gebruikt om anderen te laten zien welke wijzigingen je hebt gemaakt aan een branch. 
In een open pull request kun je samen met degene die met jouw werken de wijzigingen bespreken en eventuele wijzingen maken. 
Hiermee kun je eventuele problemen/fouten oplossen voordat de pull request wordt gemerged in de main branch.   
[Bron: GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)  
Een andere functie die handig is om te gebruiken bij een pull request is GitHub Actions. 
Hiermee kun je namelijk automatisch testen laten lopen, waardoor je kunt checken of de code die je wilt toevoegen/wijzigen aan de main branch, nog steeds correct werkt. 

## Hoe voeg je CI/CD toe met behulp van GitHub
GitHub actions wordt er dus voor gebruikt om ervoor te zorgen dat je automatisch dingen kunt bouwen testen en deployen. 
Je kunt hiermee dus bijvoorbeeld ervoor zorgen dat worden getest en gemergde pull requests wordt gedeployt naar een server.  

Om gebruik te maken van GitHub actions moet je eerst een workflow maken. 
Een workflow is een automatisch proces waarin je jobs kunt aanmaken die je kunt laat lopen wanneer er een bepaald event plaatsvindt in jouw repository. 
Zo kun je er dus bijvoorbeeld een maken die testen runt op een pull request zodat je kunt kijken of alles klopt.  
[Bron: GitHub](https://docs.github.com/en/actions ) 

# Conclusie & validatie
Github kan ervoor zorgen dat jouw project op een handige en overzichtelijke manier wordt gemanaged, zonder iets onnodig complex te maken.

Ik toon wat ik heb onderzocht aan binnen mijn eigen projecten en github issues/het planbord wordt gebruikt binnen ons groepsproject.
Hiermee valideer ik ook gelijk datgene wat ik heb onderzocht en pas het toe in mijn project.
In mijn eigen project heb ik CI/CD kunnen toevoegen door github actions te gebruiken.
Onder de 'actions' tab kun je deze actions zien en hoe ze werken.
Verder kun je ook zien hoe ik nieuwe code toevoeg in de commit geschiedenis van het project.
Je kunt hier ook zien dat ik verschillende branches gebruikte voor de desbetreffende toevoegingen aan mijn project.

Voor het groepsproject geld hetzelfde als bij mijn eigen project.
Hier hebben wij ook losse branches gebruikt om aan nieuwe functies te werken.
Verder gebruiken wij ook het planbord voor ons groepsproject.
Op dit planbord hebben wij alle user stories staan, die we aan het begin hebben opgesteld.
Tijdens een sprint planning pakken wij enkele van deze op en splitsen deze in kleinere issues die wij verdelen over de groep.

## Hoe zou ik wat ik van dit onderzoek heb geleerd de volgende keer toepassen?
Door dit onderzoek en GitHub gedurende het semester te leren heb ik redelijk goed geleerd hoe je hiermee kunt werken.
De volgende keer zou ik sowieso ook bij mijn eigen project user stories in github issues zetten en een planbord maken.
Hiermee kan ik dan ook makkelijker voor mezelf bijhouden wat ik nog zou willen doen en hoelang iets duurt.

De branches, mergen hiervan en pull requests zijn allemaal functies waarmee ik dit semester heb leren werken.
Voor mijn volgende project zou ik hier al mee bekent zijn dus hoef ik deze niet nog een keer te onderzoeken.

Binnen een nieuw project zou ik ook sneller workflows kunnen aanmaken, omdat ik nu weet hoe ik dit kan doen.
Dit ben ik ook zeker van plan, omdat deze heel handig zijn om je code te controleren.

Ook zou ik de volgende keer het pushen naar Dockerhub zo snel mogelijk opzetten.
Dit was namelijk een van de dingen die ik graag werkend wilde krijgen in dit semester, omdat dit mij erg handig leek om nieuwe code te schrijven.
Nu dit mij is gelukt, kan ik ook met zekerheid zeggen dat dit daadwerkelijk het geval is.
Het is nu namelijk heel eenvoudig voor mij om de containers op te starten die ik nodig heb in Docker desktop en dan aan de andere onderdelen te werken.

Al met al zou ik alles wat ik gedurende dit semester heb geleerd over GitHub de volgende keer sneller en beter toe willen passen.
GitHub is namelijk een erg fijn platform om je project mee te ontwikkelen.

## GitHub repositories van mijn projecten en het groepsproject en het planbord van ons groepsproject:

[Novelsite-backend](https://github.com/KevinvdHoogenhof/novelsite-backend)

[Novelsite-frontend](https://github.com/KevinvdHoogenhof/novelsite-frontend)

[Novelsite-frontend-admin](https://github.com/KevinvdHoogenhof/novelsite-frontend-admin)

[WOC-backend](https://github.com/kerimcanguney/WOC-Back-End)

[WOC-frontend](https://github.com/kerimcanguney/WOC-Front-End)

[WOC-planbord](https://github.com/users/kerimcanguney/projects/1)

## Andere bronnen   
https://www.jobsity.com/blog/a-quick-guide-to-using-github-for-project-management  
