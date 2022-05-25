# Research Security 

## Inleiding 
In minder dan een seconde tijd kan een hacker een wachtwoord van zeven tekens kraken. 
Met ‘1234567’, ‘password’ en ‘1111111’ maak je dus geen schijn van kans, maar hoe dan wel? 
[Bron](https://www.jobat.be/nl/art/73-van-de-wachtwoorden-binnen-1-seconde-gekraakt)  
Dat simpele wachtwoorden snel gekraakt kunnen worden is algemeen bekend, maar hoe kunnen we dit tegengaan?
Natuurlijke is een simpele oplossing voor een veiliger wachtwoord om letters, hoofdletters, nummers en tekens te gebruiken, 
maar hoe kunnen we als ontwikkelaar veilig met wachtwoorden omgaan? 

### Onderzoeksvraag 
Hoe kan ik veilig wachtwoorden encrypten en opslaan in mijn database? 

## Problemen met geen encryptie 
In mijn onderzoeksvraag zeg ik dat ik wil gaan kijken hoe ik veilig wachtwoorden kan opslaan in mijn database, 
maar eerst wil ik even toelichten waarom het nou niet veilig is om wachtwoorden op te slaan als plain-tekst (zonder encryptie). 
De reden waarom we geen plain-tekst wachtwoorden in onze database willen hebben is, 
omdat alle wachtwoorden zichtbaar zijn voor een hacker als je database gecompromitteerd wordt. 
Hierdoor loopt iedereen die zijn wachtwoord & eventuele andere gegevens in jouw database heeft staan groot gevaar. 
Hackers kunnen dan namelijk personen die dezelfde wachtwoorden op verschillende sites gebruiken makkelijk hacken. 

## Encryptie 
Om te voorkomen dat een hacker direct alle wachtwoorden kan zien in een database, worden wachtwoorden geencrypt. 
Er zijn hiervoor vele algoritmes, deze zijn echter lang niet allemaal even veilig. 
De algoritmes die niet veilig zijn in dit geval zijn omkeerbare algoritmes. 
Een hacker kan namelijk eenvoudig de logica van deze algoritmes vinden door verschillende wachtwoorden te testen tegen de geencrypte vorm van het wachtwoord. 
Als dit eenmaal lukt kan hij snel ook de andere decrypten en heeft hij weer toegang tot alle wachtwoorden. 

## Hashen 
Een veel voorkomende term bij wachtwoorden opslaan is hashen, maar wat houdt dit nu in? 
Bij een hash van een wachtwoord kunnen we niet het wachtwoord uit de hash afleiden. 
Dit klinkt misschien als een nadeel, maar het is niet nodig om het wachtwoord hieruit af te leiden. 
Je kunt namelijk ook het wachtwoord hashen en controleren of deze overeenkomen.    
![image](https://user-images.githubusercontent.com/101703190/170257617-6ef9190f-badc-45e0-96cb-368b05cfd856.png)    
Hierboven staat een voorbeeld van wachtwoorden en hun hash via MD5 en SHA1 [Bron: hashtoolkit](https://hashtoolkit.com/common-passwords/) 
In deze tabel kun je een voorbeeld zijn van enkele wachtwoorden en hun gehashde vorm. 
Iets wat we wel moeten opmerken hierbij is dat dezelfde wachtwoorden dezelfde hash hebben.  
Omdat deze hashes hetzelfde zijn kunnen we met een simpele google search het wachtwoord vinden.    
![image](https://user-images.githubusercontent.com/101703190/170258475-c8539567-f60a-48f3-8edb-647a4e8e1423.png)   
Ook als je het wachtwoord niet direct kunt vinden zijn er andere manieren voor om hierachter te komen.
Zo kun je bijvoorbeeld gebruik maken van de volgende methodes om een wachtwoord te kraken:

### Brute force 
Een brute force attack is een veelgebruikte methode om iemand zijn wachtwoord te kunnen kraken. 
Een hacker maakt hierbij gebruik van software die verschillende wachtwoorden probeert en loopt zo systematisch combinaties af. 
Bij een brute force attack zijn zwakke wachtwoorden ook nog makkelijker te kraken. [Bron](https://realhosting.nl/helpdesk/wat-is-een-brute-force-attack/) 

### Dictionary attack 
Een dictionary attack is een brute force aanval waarbij de software op bepaalde termen of veelgebruikte wachtwoorden focust. 
Als je meer weet over de gebruiker wiens wachtwoord je wilt stelen, 
zou je ook dingen als zijn geboortejaar/datum / naam / favoriete dier gebruiken en hiervan combinaties maken die de software dan als wachtwoord gaat proberen. 

### Rainbow table 
Een rainbow table is een tabel waarin allerlei wachtwoorden met hun bijbehorende hash staan. 
Het kost dan wel wat tijd om een tabel te maken, maar als we deze eenmaal hebben is heel snel om een wachtwoord te kraken. 
Je hoeft namelijk niet los alle hashes te berekenen. [Bron: Wikipedia](https://nl.wikipedia.org/wiki/Rainbow_table) 

## Salt 
Een salt wordt gebruikt om willekeurige data toe te voegen aan een hashfunctie. 
Wanneer er gebruik wordt gemaakt van een salt, wordt het ook mogelijk om verschillende hashes van hetzelfde wachtwoord te krijgen. 
Doordat de salt willekeurig is, is er een grotere kans dat de hash niet eerder is gebruikt. 
De voordelen van het toevoegen van een salt zijn als volgt: 
Het is bijna onmogelijk om de hash direct op het internet te vinden, zolang de salt lang en willekeurig genoeg is. 
Een rainbow table kan niet worden gebruikt met een gesalte hash 
Als een gebruiker hetzelfde wachtwoord heeft, kan er geen gebruik gemaakt worden van software om tegelijk het wachtwoord van de andere gebruiker te vinden. 
Als er een salt wordt gebruikt is de hash immers verschillend van elkaar. 

## Pepper 
Een pepper is een andere manier om gegevens toe te voegen aan een hash. 
Een pepper wordt gebruikt voor alle gebruikers en wordt vaak opgeslagen in de configuration van een applicatie. 
Als een hacker toegang krijgt tot de database zal hij dus ook nog de pepper moeten raden. 

## Iteraties 
Een andere manier om een wachtwoord beter te encrypten is het aantal iteraties vergroten 
[Bron](https://scottsauber.com/2018/01/29/increasing-password-hashing-iterations-with-asp-net-core-identity/#:~:text=Iterations%20is%20the%20%E2%80%9Cwork%20factor,password%20and%20hash%20it%20once.) 
Wanneer je het aantal iteraties vergroot, hash je de hash en dan de dubbele hash, totdat je het aantal iteraties hebt behaalt. 
Als je aantal iteraties vergroot kost dit ook meer tijd voor je CPU om deze operatie te voltooien. 
Mocht iemand je database in handen krijgen zal het hun dus ook meer tijd kosten om de wachtwoorden te kraken. 

# Combineren van de methodes 
Wanneer we een methode maken voor het opslaan van wachtwoorden kunnen we de methodes combineren. 
Hierdoor krijgen we een methode die de wachtwoorden veiliger opslaat dan een simpele hash. 
Hieronder kun je functie zien die ik heb gemaakt voor het encrypten van wachtwoorden in mijn back-end:    
![image](https://user-images.githubusercontent.com/101703190/170258616-f11cb36b-369d-4205-83e3-bc4f2713e8c3.png)    
In deze functie kun je zien dat ik geen gebruik maak van een pepper. 
Ik vond dit namelijk nog niet nodig voor mijn doeleinden. 
Ik heb hier echter wel een salt die willekeurig wordt gegenereerd. 
Vervolgens gebruik ik het Pbkdf2 algoritme 
[Bron: Microsoft](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.cryptography.keyderivation.keyderivation.pbkdf2?view=aspnetcore-5.0 ) 
om het wachtwoorden te hashen. 
De hash en salt worden dan vervolgens teruggegeven, zodat we deze in de database kunnen opslaan. 

Wanneer iemand wil inloggen en we het wachtwoord moeten checken kunnen we de volgende functie gebruiken om te kijken of het ingevoerde wachtwoord overkomt met het opgeslagen wachtwoord.    
![image](https://user-images.githubusercontent.com/101703190/170258785-53b67b5b-9956-42bb-a901-c0fb54422d73.png)    
Hierboven kun je zien hoe we het ingevoerde wachtwoord opnieuw hashen me dezelfde salt en dan kijken of de hashes hetzelfde zijn. 

# Conclusie 
Door dit onderzoek heb ik geleerd dat je tenminste een hash en salt wilt gebruikt om je wachtwoord te encrypten. 
Hierdoor is namelijk een stuk moeilijker voor hackers om het wachtwoord te kraken. 
Iets anders wat ik heb geleerd is dat het nog steeds handig is om sterke wachtwoorden te gebruiken, ondanks goede wachtwoord encryptie, omdat zwakke wachtwoorden nog steeds vrij snel kunnen worden gevonden. 

## Andere bronnen   
https://www.vaadata.com/blog/how-to-securely-store-passwords-in-database/  
https://security.stackexchange.com/questions/211/how-to-securely-hash-passwords  
https://teampassword.com/blog/what-is-password-encryption-and-how-much-is-enough#:~:text=Password%20encryption%20is%20essential%20to,easily%20view%20any%20stored%20passwords.  
https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html  
https://nl.wikipedia.org/wiki/Rainbow_table  
https://fusionauth.io/blog/2019/03/12/plaintext-passwords#:~:text=Here's%20why%3A-,Storing%20plaintext%20passwords,drained%20or%20their%20identities%20stolen.  
https://owasp.org/Top10/A02_2021-Cryptographic_Failures/  
https://nl.wikipedia.org/wiki/Hashfunctie  
