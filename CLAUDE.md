# Anime Aktuell – Webseite

## Über das Projekt
Ein Schulprojekt: die offizielle Webseite der Anime-Zeitung **"Anime Aktuell"**.
Der Entwickler ist 12 Jahre alt und hat noch keine Vorkenntnisse in HTML/CSS.
Sprache mit dem Nutzer: **immer Deutsch**, einfach und verständlich erklären.

## Ziel der Webseite
- Digitale Ausgaben der Anime Aktuell Zeitung präsentieren
- Extras-Bereich (Quiz + Empfehlungen)
- Einsteigerfreundlich – Schritt für Schritt aufbauen

## Design & Stil
- **Stil**: Cool, Anime-Look
- **Farben**: Gold, Silber, bunt (Akzente) – Rot für Überschriften
- **Hintergrund**: `#1a1a2e` (dunkles Blau)
- **Logo/Titel**: "Anime Aktuell" in Rot – großes A mit "nime" oben und "ktuell" unten
- Inspiriert an einer echten Zeitung, aber digital und anime-artig
- **News-Kachel** auf der Startseite ist silber/grau (nicht gold) und hat keinen Hover-Effekt

## Inhalt
- **Ausgabe 1**: vorhanden (Titelbild + Ideen)
- **Ausgabe 2**: noch in Bearbeitung
- Bilder werden nach und nach eingefügt – Struktur ist bereits vorbereitet
- Empfehlungen: siehe unten

## Technik
- Bootstrap (CSS + JS) ist bereits eingebunden (lokal in `/css/` und `/js/`)
- Kein separater Server nötig – einfache HTML-Dateien
- Anfängerprojekt: Erklärungen zu allem auf einfachem Niveau
- Responsiv: funktioniert auf Handy UND Computer (Bootstrap Responsive Design)
- localStorage-Keys:
  - `bestScore`, `lastScore` – Quiz-Scores
  - `bestScoreSchwierigkeit`, `lastScoreSchwierigkeit` – Schwierigkeit beim jeweiligen Score
  - `quizThemen` – gespeicherte Themenauswahl (JSON-Array)
  - `quizSchwierigkeit` – gespeicherte Schwierigkeit (`normal` / `zeitdruck` / `extrem`)

## Seitenstruktur (fertig)
- `index.html` – Startseite mit Logo, Anime-Augen, Top-Listen, Quiz-Score, Danke-Nachricht
- `ausgaben.html` – Übersicht aller Ausgaben
- `ausgabe1.html` – Seiten der Ausgabe 1 (mit Klick-zum-Vergrößern via Bootstrap Modal)
- `ausgabe2.html` – Seiten der Ausgabe 2 (noch in Bearbeitung)
- `empfehlungen.html` – Joshuans eigene Anime-Empfehlungen (ein- und ausklappbar)
- `extras.html` – Quiz-Seite mit Themenauswahl
- `impressum.html` – Impressum mit allen Pflichtangaben

## Bilder einfügen
Ordnerstruktur für Bilder:
```
images/
  ausgabe1/
    cover.jpg      ← Titelbild
    seite2.jpg
    seite3.jpg ...
  ausgabe2/
    cover.jpg
    seite2.jpg ...
```
In der HTML-Datei das `<!-- <img ...> -->` Kommentar entfernen und den Platzhalter-Div löschen.

## Extras: Quiz
- **101 Fragen** insgesamt (Stand April 2026)
- **Normale Themen** (sortiert nach Fragenanzahl):
  One Piece (7), Naruto (7), Demon Slayer (7), Spy×Family (7), Jujutsu Kaisen (7),
  Dragon Ball (7), My Hero Academia (7), Attack on Titan (5), Death Note (5),
  Sailor Moon (5), Pokémon (5), Bleach (5), Fairy Tail (5), Fullmetal Alchemist (5),
  Black Clover (5), Tagebücher der Apothekerin (4), Aggretsuko (4), Kamikaze Kaito Jeanne (4)
- **Für kleine Anime Fans** (eigener Abschnitt in der Themenauswahl, blau markiert):
  Heidi (15), Biene Maja (6), Digimon (6), Wickie (5), Nils Holgersson (5), Pinocchio (5)
- **Themenauswahl** vor dem Quiz – Benutzer wählt Themen, mindestens 10 Fragen nötig
- Auswahl wird in `localStorage` gespeichert und ist jederzeit änderbar
- Pro Runde: 10 zufällige Fragen aus den gewählten Themen (`FRAGEN_PRO_RUNDE = 10`)
- **Schwierigkeitsstufen** (wählbar vor dem Quiz UND auf dem Ergebnis-Bildschirm):
  - ⏸ **Normal** – kein Timer
  - ⏱ **Zeitdruck** – 20 Sekunden pro Frage
  - ⚡ **Extremer Zeitdruck** – 10 Sekunden pro Frage (rot markiert)
- Score + Schwierigkeit werden in `localStorage` gespeichert
- Auf der Startseite: Score mit Schwierigkeit-Symbol (⏸/⏱/⚡) angezeigt
- Buttons auf dem Ergebnis-Bildschirm: "Nochmal spielen", "Themen ändern ⚙"

## Empfehlungen
Alle Empfehlungen sind ein- und ausklappbar (Bootstrap Collapse, Pfeil ▼/▲).
Standardmäßig eingeklappt – Übersicht über alle Karten auf einen Blick.

| # | Titel | Kategorie | Badge |
|---|-------|-----------|-------|
| 1 | Aggretsuko | Für Hello Kitty Fans | Joshua empfiehlt |
| 2 | Kamikaze Kaito Jeanne | Für Geschichte Fans | Joshua empfiehlt |
| 3 | Spy × Family | Für Action Fans | Joshua empfiehlt |
| 4 | Tagebücher der Apothekerin | Für Medizin Fans | Joshua empfiehlt |
| 5 | One Piece | Für Piraten Fans | Joshua empfiehlt |
| 6 | Pokémon | Für Fantasiewesen Fans | Joshua empfiehlt |
| 7 | Die 4 gegen die Monster | Für Abenteuer Fans | **Joshua hat geschrieben** (blau) |

- Empfehlung 7 ist Joshuans eigener Manga (mit Freunden geschrieben, nur an der Wilhelm-Leuschner-Schule)
- Badge-Farben: Rot = "Joshua empfiehlt", Blau = "Joshua hat geschrieben"
- IDs der Collapse-Divs: `#empf1` bis `#empf7`

## Git & GitHub
- **Git** ist eingerichtet – lokale Speicherstände (Commits)
- **GitHub Repository:** https://github.com/jbeister/Webseite
- **Live-Webseite:** https://jbeister.github.io/Webseite/
- **Verbindung:** SSH (Schlüssel unter `~/.ssh/id_ed25519`)
- **GH CLI** ist installiert und eingerichtet (`gh auth status` zum Prüfen)

### Workflow nach jeder Änderung:
```bash
git add .
git commit -m "Kurze Beschreibung was geändert wurde"
git push
```
Nach dem Push dauert es ca. 1–2 Minuten bis die Änderung auf der Live-Seite sichtbar ist.

## Regeln für Claude
- Immer auf Deutsch antworten
- Einfache, kindgerechte Erklärungen (12 Jahre, Anfänger)
- Schritt für Schritt vorgehen – nichts überstürzen
- Den Nutzer nach jedem Schritt fragen, bevor weitergemacht wird
- Bilder immer als Platzhalter vorbereiten, damit sie leicht ersetzt werden können
