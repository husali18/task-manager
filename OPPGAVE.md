# PGR203 Innlevering 3: Data Access Object

I denne oppgaven skal dere lage en Data Access Object som 

1. Liste ut alle prosjektmedlemmene i databasen
2. Legge til nye prosjektmedlemmer til et prosjekt i en database

Denne funksjonalitene vil bli kjernen av eksamensinnleveringen. Dere kan valgfritt bruke oppgaven som en sjanse til å utvikle mer funksjonalitet for å bli klar til eksamen.

Oppgaven skal utvikles med parprogrammering og test-drevet utvikling og dere må ha et omfattende sett med tester som skal kjøre automatisk med Travis CI. Oppgaven skal utvikles med GitHub Classroom og dere må benytte linken dere har fått i Canvas til repository. Repository må linke til Travis CI.

Dere skal finne en annen gruppe som dere skal gi hverandrevurdering til. Del prosjektene med hverandre på GitHub og skriv minst to "bra at ..." issues og to "programmet bør..." issues. *Opprett en link i README.md til issues dere gir til den andre gruppen slik at vi kan finne disse*

Programmet vil testes ut som følger når det vurderes:

1. Vi vil kjøre `mvn package` og se at tester kjøres og jar-filen bygges
2. Vi vil kopiere inn en fil som heter `task-manager.properties` inn i prosjekt directory. Denne vil inneholde:
   * dataSource.url=...
   * dataSource.username=...
   * dataSource.password=...
3. Vi vil starte `java -jar target/task-manager-1.0-SNAPSHOT.jar`. Vi forventer
   * Programmet bruker verdiene i `task-manager.properties` til å connecte seg til databasen
   * Programmet bruker Flyway til å opprette databasetabeller
   * Programmet skriver ut innholdet av prosjekt-deltager-tabellen
   * Programmet ber brukeren skrive inn navn og email-adresse på en ny bruker
   
Dersom dere vil ta oppgaven videre for å være forberedt til eksamen kan dere *valgfritt* legge til mer funksjonalitet:

* La bruker opprette prosjektoppgaver i tillegg til prosjektmedlemmer
* La bruker endre egenskaper på en eksisterende prosjektmedlem i databasen
* Bruk PlantUML for å beskrive datamodellen i README.md
* Bruk HTTP server fra innlevering 2 til å returnere alle prosjektmedlemmen når man går til http://localhost:8080/projectMembers
* Lag en HTML-fil med et skjema som `<form method='post' action='/addProjectMembers'>` og implementer kode i HTTP serveren som legger inn en ny prosjektdeltager i databasen


## Sjekkliste for å få godkjent

* [ ] Koden er sjekket inn på github.com/Westerdals-repository
* [ ] `README.md` inneholder en korrekt link til Travis CI
* [ ] `mvn package` bygger en executable jar-fil
* [ ] `java -jar target/...jar` (etter `mvn package`) starter opp en webserver
* [ ] `README.md` beskriver prosjektet, hvordan man bygger det og hvordan man kjører det 
* [ ] Programmet leser `dataSource.url`, `dataSource.username` og `dataSource.password` fra `task-manager.properties` for å connecte til databasen
* [ ] Programmet bruker Flywaydb for å sette opp databaseskjema
* [ ] Programmet kan liste prosjektdeltagere fra databasen
* [ ] Programmet lar bruker opprette nye prosjektdeltagere i databasen
* [ ] Koden inneholder et godt sett med tester og testene kjører i Travis CI
* [ ] GitHub repository er private, men delt med gruppen dere gjør hverandrevurdering på
* [ ] Dere har mottatt minst 2 positive og 2 korrektive GitHub issues i github repository fra en annen gruppe
* [ ] Dere har gitt minst 2 positive og 2 korrektive GitHub issues til en annen gruppe og inkluderer link til disse fra README.md
* [ ] Veilederne er lagt til som Collaborators på GitHub repository (`alacho2`, `aridder`, `asmadsen`)
* [ ] Dere har committed kode med begge prosjektdeltagernes GitHub konto
* [ ] Dere har registrert link til GitHub repository i Canvas

## Sjekkliste for god leveranse

* [ ] `.gitignore` hindrer `target/`, `.idea` og `*.iml` fra å sjekkes inn ved uhell
* [ ] Navn på pakker, klasser og metoder skal følge vanlig Java-konvensjon når det gjelder små og store bokstaver
* [ ] Indentering skal følge vanlig Java-konvensjon
* [ ] `README.md` inneholder link til en diagram som viser datamodellen
* [ ] Programmet kan opprette og liste prosjektoppgaver fra databasen
* [ ] Programmet kan vise prosjektdeltagere fra databasen over http
* [ ] Programmet kan opprette nye prosjektdeltagere i databasen over http

