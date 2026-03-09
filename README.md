# Theorieteil

## 1. Status Quo: Unsere Editionsdaten liegen auf Netzlaufwerk

- **Gemeinsam Bearbeiten**, aber nur nacheinander
- **Wenn eine Datei bearbeitet wird**, wird die alte Version quasi gelöscht

### Probleme:

- Keine Nachvollziehbarkeit, wer wann was geändert hat
- Keine Möglichkeit, parallel zu arbeiten
- Keine Möglichkeit, Schritte rückgängig zu machen
- Keine Möglichkeit, Änderungen zu testen, ohne Schattenablagen zu machen
- Versionenchaos

## 2. Warum git?

TODO

## 3. Wie funktioniert das Arbeiten mit Git?

Die wichtigsten Prinzipien und Begriffe

TODO

## 4. Und was ist Github?

TODO

---

# Praxisteil

## 1. Setup

- Haben alle Visual Studio Code und git
- Visual Studio Code öffnen
- Unten links klicken und mit Github-Konto verknüpfen

### Git config

```bash
git config --global http.proxy http://127.0.0.1:9000
git config --global user.name "Tim Rüdiger"
git config --global user.email "tim.ruediger@ji.zh.ch"
```

- "Repositories"-Ordner erstellen auf C:-Laufwerk

## 2. Repository Klonen

- **Bedeutet**: Herunterladen, aber inklusive Git-History und Verknüpfung zum Ort, wo man heruntergeladen hat
- Klonen in "Repositories"-Ordner

## 3. Synchrones Ändern von gleicher html-Datei: der erste Commit

- Name des Hundes geben
- Speichern
- Change appenden
- Commit message "Wolfi erblickt die Welt"
- Push

## 4. Problem: Das sieht man immer alles gleich im Internet

- Vorher sollte jemand drüber schauen
- Vorher sollte man testen können

## 5. Besser zusammenarbeiten mit verschiedenen Branches

- Damit der Produktive Branch geschützt ist, falls man etwas kaputt macht

## 6. Einen Commit rückgängig machen

TODO

## 7. Issues

TODO

## 8. Jetzt ernst: Alle zusammen arbeiten mit Editionsdaten und Issues

- ß zu ss
- GND-Nummern einfügen
- Metadaten massenhaft ändern (z.B. Links zum Query)
- Etwas in der App ändern
    
    
