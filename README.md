# Pos3xhif
C# Beispiele für den 3. Jahrgang in POS.

## Anlegen eines Ordners und Vorbereiten des Repositories:
1. Lege dir auf [GitHub] einen Zugang an.
2. Lege einen Ordner auf der Festplatte an, wo dem du dein lokales Repository speichern möchtest 
    (z. B. *C:\Schule\POS*)
3. Setze in der Konsole deinen Namen und deine Mailadresse in den globalen Einstellungen deiner
   git Installation:
```
git config --global user.name "FIRST_NAME LAST_NAME"
git config --global user.email "MY_NAME@example.com"
```
4. Lege auf GitHub unter *Repositories* ein neues Repository (z. B. *POS*) an. Wichtig: Initialisiere
    es NICHT mit einer Readme Datei, denn diese würde einen Konflikt beim Synchronisieren mit dem 
    Mustercode Repository verurachen. 
5.  Nach dem Anlegen erscheint ein Textfeld mit der URL des Repositories (z. B. *https://github.com/username/POS*).
    Ersetze nun (URL) in den nachfolgenden Befehlen durch diese Adresse und führe sie
    in der Konsole in deinem lokalen git Verzeichnis aus. Hinweis: Kopiere alle Befehle. Mit 
    Rechtsklick kannst du sie in der Konsole aus der Zwischenablage einfügen.
```
git init
git commit -m "first commit"
git remote add origin (URL)
git pull https://github.com/schletz/Pos3xhif.git master --allow-unrelated-histories
git push -u origin master
```

## Aktualisieren des Repositories
Erstelle eine Datei *syncGit.cmd* im Texteditor und füge folgende die folgenden Befehle ein. Die Datei
muss so heißen und im Hauptverzeichnis des Repositories liegen, denn die vordefinierte *.gitignore*
Datei schließt diese Datei von der Synchronisation aus.
```
git add -A
git commit -a -m "Commit"
git pull https://github.com/schletz/Pos3xhif.git master --allow-unrelated-histories
git pull origin master
git push origin master
```

Speichere die Datei im root deines git Ordners und synchroisiere durch Doppelklick auf die Datei im
Explorer dein lokales Repository mit dem Github Server.

## Arbeiten mit dem Repository
Durch den Befehl 
`git pull https://github.com/schletz/Pos3xhif.git master --allow-unrelated-histories`
wird immer der neue Inhalt des Mustercode Repositories integriert. **Arbeite daher immer in einem
eigenen Verzeichnis (z. B. Work)**. Werden Dateien vom Mustercode Repository gelöscht, so wird das
Löschen auch als bewusste Änderung angenommen und die Datei wird nicht mehr geladen.

[GitHub]: https://github.com
