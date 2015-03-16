Git Tutorial
====================

Wir schreiben ein Buch.

## 1 (init, clone, add, commit, push, remote)

### Erstellen eines Github Accounts (Server)
- https://github.com/join

### Installieren von Git (Lokal)
- http://git-scm.com/book/en/v2/Getting-Started-Installing-Git

### Erstellen eines Git Repositories (Lokal)

    mkdir buch
    cd buch
    git init

### Auschecken eins vorhandenen Git Repositories (Lokal/Global)

    git clone https://github.com/linux-node-eberswalde/git.git

### Erstellen einer Datei (Lokal)

    touch kapitel-1.txt

### Hinzufügen einer Datei zum Index (Lokal)

    git add kapitel-1.txt
oder
    git add *

### Bestätigung der Änderungen im Git Repository (Lokal)

    git commit -m "Kapitel 1 erstellt"

### Hinzufügen der Adresse für das Remote Repository (Lokal)

    git remote add origin https://github.com/MeinUsername/buch.git (wenn noch keine remote existiert)

oder

    git remote set-url origin https://github.com/MeinUsername/buch.git (wenn remote schon existiert)

### Hochladen der Änderungen (Lokal)

    git push origin master


## 2 (branching)

### Erstellen eines Branch

    git checkout -b kapitel_2

### zum Master zurückkehren

    git checkout master

### Branch löschen

    git branch -d kapitel_2

### Branch veröffentlichen

    git push origin kapitel_2

## 3 (update & merge)

### Lokales Repository aktualisieren (pull = fetch + merge)

    git pull

### Branches zusammenführen

    git checkout master
    git merge kapitel_2
    git add kapitel-2.txt

### Differenzen zwischen Branches

    git diff master kapitel_2

## 4 (tagging)

### tag

    git tag 1.0.0 <commit> (benutzt den ausgewählten commit als tag)

oder 

    git tag -b 1.0.0 (benutzt den aktuell ausgechekten branch als tag)

## 5 Änderungen rückgängig machen

    git checkout -- <dateiname>


## 6 Git Helfer

### Aktuelle Veränderungen im Repository

    git status

### Liste der Commits

    git log

### Liste der Tags

    git tag

### Liste der Branches

    git branch

## 7 Git Konfiguration

Begriffe
====================
- Repository
- Index
- Master
- Branch
- Working Dir
- Head
- Commit
- Remote --> das entfernte (Server) Repository
- Tag
