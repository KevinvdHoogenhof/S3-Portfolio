# S3-Portfolio
Portfolio en documentatie voor mijn semester 3 van Fontys HBO-ICT

# Inhoud

[Learning outcome 1. Web application (IP&GP)](#Learning-outcome-1.-Web-application)

[Learning outcome 2. Software quality (IP)](#Learning-outcome-2.-Software-quality)

[Learning outcome 3. Agile method (GP)](#Learning-outcome-3.-Agile-method)

[Learning outcome 4. CI/CD (IP)](#Learning-outcome-4.-CI/CD)

[Learning outcome 5. Cultural differences and ethics (GP)](#Learning-outcome-5.-Cultural-differences-and-ethics)

[Learning outcome 6. Requirements and Design (GP)](#Learning-outcome-6.-Requirements-and-Design)

[Learning outcome 7. Business processes (GP)](#Learning-outcome-7.-Business-processes)

[Learning outcome 8. Professional (IP&GP)](#Learning-outcome-8.-Professional)

# Learning outcome 1. Web application
**Learning outcome:** You design and build **user-friendly**, **full-stack** web applications.

**Clarification:**

**User friendly:** You apply basic User experience testing and development techniques.

**Full-stack:** You design and build a full stack application using commonly accepted front end (Javascript-based framework) and back end techniques (e.g. Object Relational Mapping) choosing and implementing relevant communication protocols and addressing asynchronous communication issues.

Om deze leeruitkomst aan te kunnen tonen heb ik een ontwerp gemaakt van de applicatie die ik wil gaan bouwen. Zie https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Documentation.md#C4-model voor het C4 model, wat ik voor deze mijn applicatie heb gemaakt.    
De verschillende componenten van mijn software kunnen los van elkaar worden ontwikkeld end getest. 
Verder kun je iedere component in een losse docker container runnen.

#### Front-end

Mijn keuzes over de front-end kunnen gevonden worden onder https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Documentation.md#Front-end-development   
Mijn keuze voor het framework React.js wordt meer uitgelegd onder https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Documentation.md#Keuze-front-end   
De code voor mijn front-end kun je vinden op https://github.com/KevinvdHoogenhof/novelsite-frontend   
Ik heb ook nog een tweede front-end gemaakt. Dit is een front-end speciaal voor admin gebruikers.
Je kunt deze vinden op https://github.com/KevinvdHoogenhof/novelsite-frontend-admin

#### Back-end

Mijn uitleg over mijn keuze van de back-end kun je vinden onder https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Documentation.md#Back-end-development   
Mijn keuze over mijn ORM en het databehoud kan onder https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Documentation.md#Data-behoud worden gevonden.   
De back-end code kan gevonden worden op <https://github.com/KevinvdHoogenhof/novelsite-backend> 

# Learning outcome 2. Software quality 
**Learning outcome:** You use software **tooling and methodology** that continuously monitors and improve the software quality during software development.

**Clarification:**

**Tooling and methodology:** Carry out, monitor and report on unit integration, regression and system tests, with attention for security and performance aspects, as well as applying static code analysis and code reviews.

#### Testen back-end
Om aan te tonen dat mijn software voldoet aan de kwaliteitseisen maak ik gebruik van unit testen en integratie testen.   
Ik gebruik de unit testen om te kijken of alle code werkt. Als er iets niet werkt, kan ik hierdoor ook snel vinden waar het probleem zit.
De integratie testen gebruik ik om mijn endpoints te testen. Ik test hiermee de endpoints en kijk of de endpoint werk zoals ik het wil.
Ik kan hierdoor ook zien welke data ik terug krijg van de endpoint en of ik de correcte data terug krijg.

Ik wil ook nog de testen automatisch laten draaien in mijn CI op github actions.
Hiermee zouden de testen automatisch worden gedraaid, iedere keer dat ik een nieuwe pull request aanmaak.
Doordat de testen dan draaien bij ieder pull request kan ik in dit request zien of alles correct werkt, of dat ik nog eventuele veranderingen moet maken.

Zie ook: https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Research%20GitHub.md#pull-requests
Hier kun je meer informatie vinden over pull requests en github actions in het onderzoek wat ik hiernaar heb gedaan.

# Learning outcome 3. Agile method
**Learning outcome:** You **choose** and implement the most suitable agile software development method for your software project.

**Clarification:**

**Choose:** You are aware of the most popular agile methods and their underlying agile principles. Your choice of a method is motivated and based on well-defined selection criteria and context analyses.

#### Agile werken
Binnen ons groepsproject werken wij op een agile manier.
Wij doen namelijk iedere dag een stand-up, waarin we bespreken wat we die dag gaan doen en hoe we ervoor staan met het project.
Ook kijken we hierbij regelmatig op ons github planbord (https://github.com/users/kerimcanguney/projects/1)
Hierop kunnen we eenvoudig zien wat we nog willen doen in deze sprint en waar we nog meer aan kunnen werken binnen ons project.
Eventuele problemen waar we tegen aanlopen kunnen we ook snel hieraan toevoegen. 
(Zie ook https://github.com/KevinvdHoogenhof/S3-Portfolio/blob/main/Research%20GitHub.md#github-issues)

#### Sprint review & sprint retrospective
Wij werken dit semester met sprints. 
Iedere sprint houden wij een sprint review en retrospective.
De sprint review doen we tegelijk met de oplevering, hierbij bespreken we met de opdrachtgever wat we hebben gemaakt in deze sprint.
Hierin krijgen wij ook feedback over het werk wat we hebben verricht, dit kunnen we dan die volgende sprint aanpassen.
Daarnaast bespreken we ook nog waar we de volgende sprint aan gaan willen werken.
Op deze manier kunnen we samen we de opdrachtgever plannen waar we aan gaan werken, zodat zij ook weten wat ze aan het eind van de sprint kunnen verwachten.

De sprint retrospective houden wij met onze groep na de review. Hierin bespreken wij hoe het deze sprint is gegaan.
We kijken wat goed ging en wat beter kan.
De punten proberen we dan te verbeteren in de volgende sprints.
Eventuele andere tips die wij hebben gekregen tijdens deze sprint of bijvoorbeeld tijdens de oplevering nemen ook mee in dit gespreken.
Hiermee kunnen wij dan ook rekening houden.

Hieronder staat een afbeelding waarin ons scrum proces staat afgebeeld:   
![scrum-framework-example](https://user-images.githubusercontent.com/101703190/170763905-e3e050eb-ab16-4ac4-87fa-203edb09b0a6.jpg)

# Learning outcome 4. CI/CD
**Learning outcome:** You **design and implement** a (semi)automated software release process that matches the needs of the project context.

**Clarification:**

**Design and implement:** You design a release process and implement a continuous integration and deployment solution (using e.g. Gitlab CI and Docker).

#### CI/CD back-end
Ik heb voor het back-end project een goed werkende CI workflow opgesteld met GitHub actions. [Link naar mijn CI.yml bestand](https://github.com/KevinvdHoogenhof/novelsite-backend/blob/main/.github/workflows/main.yml)  
In dit bestand kun je zien dat ik een docker image laat bouwen en deze vervolgens naar DockerHub laat pushen.
Dit pushen wordt uiteraard alleen gedaan als alles correct werkt.
Als de CI geslaagd is kun je dit zien, vervolgens kun je op DockerHub de image zien onder mijn novelsite repository.

Als je deze image wilt gebruiken kun je de stappen in de readme van mijn back-end volgen.
Zie: https://github.com/KevinvdHoogenhof/novelsite-backend#readme  

Na deze commando's uit te voeren heb je als het goed is tweede lopende Docker containers.
Dit zijn de database container en de api zelf.  
Hiermee heb ik bereikt dat je de back-end eenvoudig kunt pullen en runnen om vervolgens aan het front-end te kunnen gaan werken.
Het is hierdoor niet meer nodig om dit project te openen in visual studio wat een stuk gemakkelijker is, omdat je hem nu heel snel kunt opstarten en gebruiken.

#### CI/CD front-end
Voor mijn front-end projecten heb ik ook een CI workflow opgesteld met GitHub actions.
Deze workflows doen hetzelfde als de back-end en bouwen een docker image die naar DockerHub wordt gepusht.
Door deze workflow kunnen we in een pull-request ook nogmaals zien of alles correct is geschreven.
Mocht dit niet zo zijn, dan kunnen we nog wijzigingen in de code maken.

Als je een of beide van deze projecten wilt uitvoeren kun je de stappen volgen in de readme van de front-end projecten.  

Zie: https://github.com/KevinvdHoogenhof/novelsite-frontend#readme   

Zie: https://github.com/KevinvdHoogenhof/novelsite-frontend-admin#readme

Ook hier kun je de heel simpel de containers locaal laten draaien.

#### Conclusie
Met de CI workflows die ik heb opgesteld is het heel simpel om bepaalde delen van mijn project te draaien.
Ook is het heel eenvoudig om verder te werken aan de code zelf.
Als je aan de back-end wilt werken, maak je een database container aan en als je aan een van de front-ends wilt werken maak je een container van de database en de back-end.

Dit toont ook nogmaals mooi aan hoe alle services los van elkaar kunnen werken. De containers staan namelijk los van elkaar en je hoeft ze niet allemaal te gebruiken.
Sommige hebben uiteraard wel een andere nodig om goed te kunnen werken, maar het is bijvoorbeeld niet nodig om de normale front-end te laten draaien,
als je alleen de admin front-end wilt gebruiken.

# Learning outcome 5. Cultural differences and ethics
**Learning outcome:** You **recognize** and **take into account** cultural differences between project stakeholders and ethical aspects in software development.

**Clarification:**

**Recognize:**  Recognition is based on theoretically substantiated awareness of cultural differences and ethical aspects in software engineering.

**Take into account:**

Adapt your communication, working, and behaviour styles to reflect project stakeholders from different cultures;

Address one of the standard Programming Ethical Guidelines (e.g., ACM Code of Ethics and Professional Conduct) in your work.  

# Learning outcome 6. Requirements and Design
**Learning outcome**: You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using **multiple types of test techniques.**

**Clarification:**

**Multiple types of test techniques:** You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

# Learning outcome 7. Business processes
**Learning outcome:** You analyze and describe **simple** business processes that are **related** to your project.

**Clarification:**

**Simple:** Involving stakeholders, predominantly sequential processes with one or two alternative paths.

**Related:** Business processes during which the software that you are developing will be used (business processes that the software must support by fully or partially automating them). or
Business processes needed for the success of your software development project (e.g., product release, market release, financial assurance).

# Learning outcome 8. Professional
**Learning outcome:** You act in a **professional manner** during software development and learning.

**Clarification:**

**Professional manner:**

You actively ask and apply feedback from stakeholders and advise them on the most optimal technical and design (architectural) solutions.

You choose and substantiate solutions for a given problem.
