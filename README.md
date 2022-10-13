# Kurs i Git og Terminal

Et repo for kurs i Git og Terminal bruk. I dette kurset skal vi gå gjennom hvordan vi navigerer oss gjennom terminalen på mac/windows. I tillegg til dette skal vi klone et github repo og lage en pull request til repoet. I dette tilfelle skal dere alle få tilgang til repoet, men dersom dere ikke har dette, må dere forke repoet før dere har tilgang til å lage en pull request på et public repository.

## Enkle navigeringskommandoer for Mac og Windows

Kommandolinjetolken for macOS er "Terminal", Windows har cmd, eller på norsk "Ledetekst". Denne finner dere under programmer eller ved å søke på pcen deres.

Endre directory

```sh
cd <directory>
```

Navigere seg til parent directory (gå opp en mappe fra der du befinner deg):

```sh
cd ..
```

Om du vil vite hvor i systemet du befinner deg kan du benytte kommandoen:

Mac:

```sh
pwd
```

Windows:

```sh
cd
```

For å få en liste over innholdet i det directoryet du er i

Mac:

```sh
ls
```

Widows:

```sh
dir
```

For flere kommandoer til mac kan dere sjekke ut [terminal-mac-cheatsheet](https://github.com/0nn0/terminal-mac-cheatsheet)

Windows har mange av de samme kommandoene, men det er bare å søke på google. Det er lett å finne frem om dere skulle trenge noen andre.

## 1. Sjekk at dere har git installert

De fleste versjoner av MacOS har git allerede installert, og du kan aktivere det ved å benytte følgende kommando i terminalen:

```sh
git --version
```

Regner med at dette vil funke for alle med mac, om ikke finner vi ut av det.

Windows derimot har ikke git installert som standard, derfor må vi laste det ned. Dette kan gjøres [her](https://gitforwindows.org/)

## 2. Konfigurering av git

I terminal/cmd bruker dere følgende kommandoer for å konfigurere git:

```sh
git config --global user.name "Your Name"
```

```sh
git config --global user.email dinepost@gmail.com
```

om dere vil sjekke konfigureringen deres kan dere benytte kommandoen:

```sh
git config --list
```

## 3. Naviger dere frem til folderen deres for faget

Naviger dere frem til mappen for Webteknologi. Dette kan gjøres ved bruk av kommadoene øverst.

f.eks. på denne måten:

```sh
cd Documents/webtek
```

## 4. Last ned repoet for første gang

Når dere er i Webteknologi directoryet på pcen deres kan dere, for å laste ned repoet, benytte git kommandoen i termimnal/cmd:

```sh
git clone <link>
```

Linken dere benytter finner dere under den grønne knappen "Code" øverst på siden.

Naviger dere heretter inn i mappen installert ved

f.eks. på denne måten:

```sh
cd LearnGitTerminal
```

For å åpne prosjektet i VSCode kan dere skrive i kommando linjen

f.eks. på denne måten:

```sh
code .
```

## 5. Lag et nytt html dokument i prosjektet

This you have already done plenty of times so no need to explain more here.

## 6. Last opp endringene til GitHub

For å være sikker på at man ikke ødelegger for hverandre kan det være lurt å jobbe i en egen branch. For å lage en ny branch kan du bruke kommadoen:

```sh
git branch new_branch
```

new_branch refererer til det du vil kalle branchen din. normal praksis vil være å kalle branchen din noe relatert til endringene du jobber med.

For å bytte til branchen skriver du:

```sh
git checkout my_branch
```

my_branch referer til branchen du har opprettet.

Man kan også opprette ny branch og bytte til denne i en og samme kommando ved bruk av:

```sh
git checkout -b new-branch
```

Du kan også liste alle branchene for oversikt ved følgende kommando:

```sh
git branch
```

For å holde styr på endringer, slik at man har oversikt og kan gå tilbake, er det lurt å legge til endringene hele tiden. Feks hvis jeg har lagt til et avsnitt på siden min og stylet det, kan det være lurt å legge det til. Da skriver man:

```sh
git status
```

for å se hvilke filer som er endret. For å legge til filer skriver man:

```sh
git add <file-name>
```

Man kan også bruke følgende kommando for å legge til alle endringer i commiten:

```sh
git add .
```

hvor man bytter ut filename med navnet på fila. Feks 'git add P0_Requirements.html'. Derretter må du commite fila, ved å skrive:

```sh
git commit -m <commit-message>
```

Her er det vanlig å skrive 'fix: hva du har fiksa' eller 'feat: hva du har lagt inn' hvor fix er når du fikser på noe mens feature er en ny ting som er lagt til. Etter du har commit'et, må du huske å skrive:

```sh
git push
```

Det er for å faktisk sende endringene dine til github.

Når du skriver git push kan det være du må skrive inn brukernavn og passord på github. Jeg pleier å bruke brukernavnet mitt, og som passord bruker jeg en github token. Den kan du lage ved å gå til profilbildet ditt oppe til høyre --> settings --> Developer settings --> Personal access tokens --> generate new token. Dette får du kun se en gang, så husk å lagre det en plass slik at du har det.

Dersom dere vil se på flere kommandoer på git er [dette](https://community.quali.com/articles/2434/application-git-cheat-sheet) et cheet sheet jeg liker.

## 7. Lag en Pull Request (PR) på GitHub

Gå til Github i nettleseren og inn på repoet du klonet. Du vil da se at din branch har kommet opp og du kan lage en PR, her kan du spørre andre om å gjøre en review av det du har endret på, og når du har fått godkjenning fra andre, kan du merge den inn i hovedbranchen.

Dersom du ikke er helt ferdig med det du holder på med, kan du opprette en draft-PR.

## Endre ting i prosjektet etter du har lastet det ned første gang

Husk å gå inn i riktig mappe og ALLTID SKRIVE:

```sh
git pull
```

i terminalen før du gjør noe. Dette er for å hente endringene som er gjort tidligere av andre personer. For å være sikker på at man ikke ødelegger for hverandre kan det være lurt å jobbe i en egen branch. Da skriver du:
