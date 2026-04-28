Terraform Getting Started

3
Umgebungsvariablen setzen

    Die Umgebuzngsvariablen sind Teil der Session im Terminal/Powershell
    Im AWS Kontext nutzen wir die Env-Variablen, um unseren AWS_ACCESS_KEY_ID und AWS_SECRET_ACCESS_KEY zu setzen

Linux

export AWS_ACCESS_KEY_ID=

export AWS_SECRET_ACCESS_KEY=

export AWS_DEFAULT_REGION=us-east-1
Windows

$env:AWS_ACCESS_KEY_ID="" $env:AWS_SECRET_ACCESS_KEY="" $env:AWS_DEFAULT_REGION="us-east-1"
Git

    Versionskontrollsystem

Git Dictionary

    Repository: Projektmappe (z.B. 01_terraform_getting_started)
    .gitignore Dateu im root Verzeichnis des repositories beschreibt alle Dateien/Verzeichnisse die ignoriert werden sollen

Commands

init: Initalisiert das Repository lokal in dem aktuellen Verzeichnis

    commit: Zusammenfassung der veränderten Dateien unter einem Titel
    status: Welche Dateien haben sich verändert
    add: Fügt Änderungen einem commit hinzu
    clone: Lädt sich ein repository herunter
    push: Lädt alle commits hoch

Aufgabe 10.3.26:

    Ihr erstellt einen leeren Ordner bei euch auf dem Computer (nicht in OneDrive)
    Öffne den leeren Ordner in VSCode
    Terminal öffnen und git init
    Comitten, reverten , adden etc. Tipp: Am besten mit Readme.md und der Nutzung von Markdown

Aufgabe 12.03.26:

    Repository über github.com erstellen
    Leeren ordner unter C:// (nicht OneDrive)
    Inititalisierung des repositories
    Die Commands von eurem Github.com Repository verfolgen (Die da stehen wenn das Repo leer ist) --> Am besten per SSH (nicht HTTPS)
    Readme.md erstellen
    Ein paar commits machen
    über die WSL oder PS in einen neuen leeren ordner navigieren
    Das repository in diesen Ordner clonen
    Dann eine Änderung in VSCode machen (einen punkt in die Readme.md hinzufügen)
    Aus der PS oder WSL git pull ausführen (achtet darauf, dass ihr in dem repository seid und nicht noch in dem übergeordneten Ordner)

Aufgabe 12.03.26 - 2:

    Erstelle über die VS-Code UI (git checkout -b <branch-name>)
    Eine Änderung auf dem neuen Branch machen (neue Datei)
    Diese Änderung commiten und Branch publishen/pushen
    Github.com repository verfolgen und die Änderungen auf den unterschiedlichen Branches betrachten

Andys Git Link

    https://learngitbranching.js.org/?locale=de_DE

Aufgabe 17.03.26 Merge Konflikte beheben (einfach):

    git checkout main
    Datei auf main branch anlegen (Merge_Conflicts.md)
    Datei mit # Merge Conflicts füllen
    Speichern, comitten und auf main pushen
    git checkout -b dev-1-test
    Ändern der Überschrift zu # Merge Konflikte beheben
    Commiten, Branch veröffentlichen und PR erstellen
    wieder git checkout main und natürlich git pull
    von hier aus git checkout -b dev-2-test
    Ändern der Überschrift zu # Arbeiten mit Merge Konflikten
    Commiten, Branch veröffentlichen und PR erstellen
    PR-1 mergen
    in Github.com den PR-2 überprüfen --> Merge Konflikte anzeigen
    VS-Code öffnen
    git checkout main && git pull
    git checkout dev-2-test
    git merge main
    Müsst ihr merge Konflikte beheben, commiten, pushen
    Auf github.com PR überprüfen, dass mergen möglich ist und letzendlich mergen
