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

Git löst konkret die Probleme von oben:

- **Jede Änderung wird festgehalten** — wer hat wann was geändert (wie "Track Changes" in Word, aber für alle Dateien)
- **Nichts geht verloren** — jeder frühere Zustand ist wiederherstellbar; einzelne Commits können gezielt rückgängig gemacht werden, ohne die Geschichte zu löschen
- **Parallel arbeiten** — mehrere Personen können gleichzeitig an verschiedenen Stellen arbeiten
- **Testen ohne Risiko** — Änderungen in einem geschützten Bereich ausprobieren, bevor sie "live" gehen
- **Offline arbeiten** — Commits, Branches und lokale Historie funktionieren ohne Internet; Synchronisation mit GitHub erfolgt erst beim nächsten Push/Pull

## 3. Wie funktioniert das Arbeiten mit Git?

### Überblick: Lokales und Remote-Repository

Beim Arbeiten mit Git gibt es immer **zwei Orte**:

- **Remote-Repository** — die zentrale Version auf GitHub (im Internet)
- **Lokales Repository** — die persönliche Kopie auf deinem Rechner

Alle Änderungen machst du zuerst **lokal**. Erst wenn du fertig bist, schickst du sie zu GitHub.

### Die Schritte im Überblick

```
Klonen → Pull → Branch erstellen → Datei ändern → Stagen → Commit → Push → Pull Request → Merge
```

### Schritt für Schritt erklärt

#### 1. Klonen (einmalig)

> Das Projekt zum ersten Mal auf den eigenen Rechner holen.

- Du lädst das gesamte Repository von GitHub herunter — inklusive aller Dateien und der kompletten Änderungshistorie.
- Ab jetzt ist dein lokaler Ordner mit GitHub verknüpft.
- **Das macht man nur einmal pro Projekt.**

#### 2. Pull — den neusten Stand holen

> Bevor du anfängst zu arbeiten: schauen, ob jemand anderes etwas geändert hat.

- Mit `pull` holst du die neusten Änderungen von GitHub auf deinen Rechner.
- **Gute Gewohnheit:** Immer zuerst pullen, bevor man anfängt zu arbeiten.

#### 3. Branch erstellen — auf einer Kopie arbeiten

> Einen geschützten Bereich erstellen, um in Ruhe zu arbeiten.

- Ein **Branch** ist ein Parallelstrang — wie eine Kopie des Projekts, auf der du arbeiten kannst, ohne den Hauptstrang (`main`) zu verändern.
- Andere können gleichzeitig auf ihren eigenen Branches arbeiten, ohne sich gegenseitig in die Quere zu kommen.

#### 4. Datei ändern

> Ganz normal die Datei bearbeiten — wie immer.

- Du öffnest die Datei in VS Code, machst deine Änderungen und speicherst.

#### 5. Stagen — Änderungen vormerken

> Git sagen, welche Änderungen zum nächsten Snapshot gehören sollen.

- Nicht jede gespeicherte Änderung wird automatisch festgehalten. Du wählst bewusst aus, welche Änderungen in den nächsten Commit aufgenommen werden.
- Das nennt man **stagen** (vormerken).

#### 6. Commit — Snapshot erstellen

> Einen Snapshot des aktuellen Zustands speichern — mit einer kurzen Beschreibung.

- Ein **Commit** ist wie "Speichern unter" mit Kommentar, z.B. *"Hundenamen ergänzt"*.
- Jeder Commit ist ein Punkt in der Geschichte, zu dem man jederzeit zurückkehren kann.

#### 7. Push — Änderungen hochladen

> Den Commit von deinem Rechner zu GitHub schicken.

- Erst durch den **Push** werden deine Änderungen für alle sichtbar auf GitHub.
- Ohne Push bleiben deine Commits nur lokal auf deinem Rechner.

#### 8. Pull Request (PR) — Änderungen zur Prüfung vorschlagen

> Eine Anfrage stellen, dass deine Änderungen in den Hauptstrang übernommen werden.

- Du erstellst auf GitHub einen **Pull Request**: "Ich habe auf meinem Branch etwas geändert — bitte prüfen und übernehmen."
- Eine andere Person schaut sich die Änderungen an und kann Kommentare oder Verbesserungsvorschläge machen.

#### 9. Merge — Zusammenführen

> Die geprüften Änderungen in den Hauptstrang (`main`) übernehmen.

- Nach der Prüfung wird der Branch in `main` **gemergt** (zusammengeführt).
- Die Änderungen sind jetzt Teil des Hauptprojekts.
- Der Branch kann danach gelöscht werden — die Geschichte bleibt im Commit erhalten.

### Der typische Ablauf auf einen Blick

```
Pull → Branch → Ändern → Stagen → Commit → Push → Pull Request → Merge
```

## 4. Und was ist Github?

- GitHub ist der **gemeinsame Ort im Internet**, wo unser Repository liegt
- Wie ein Netzlaufwerk, aber mit Versionshistorie und Kommentarfunktion
- Dort kann man:
  - Die Änderungshistorie ansehen
  - Dateien im Browser anschauen
  - **Pull Requests** stellen und prüfen (→ Theorie: Pull Request)
  - **Issues** erstellen: Aufgaben und Fehler erfassen

---
