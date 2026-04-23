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
- Scores gespeichert in `localStorage` (`bestScore`, `lastScore`)
- Quiz-Themenauswahl gespeichert in `localStorage` (`quizThemen`)

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
- **64 Fragen** insgesamt (Stand April 2026)
- Themen: One Piece (7), Naruto (6), Demon Slayer (5), Spy×Family (5), Jujutsu Kaisen (5),
  Dragon Ball (5), My Hero Academia (4), Attack on Titan (3), Death Note (3),
  Sailor Moon (3), Pokémon (3), Bleach (3), Fairy Tail (3), Fullmetal Alchemist (3),
  Tagebücher der Apothekerin (2), Aggretsuko (2), Kamikaze Kaito Jeanne (2)
- **Themenauswahl** vor dem Quiz – Benutzer wählt Themen, mindestens 10 Fragen nötig
- Auswahl wird in `localStorage` gespeichert und ist jederzeit änderbar
- Pro Runde: 10 zufällige Fragen aus den gewählten Themen (`FRAGEN_PRO_RUNDE = 10`)
- Score wird in `localStorage` gespeichert und auf der Startseite angezeigt (`/10`)
- "Themen ändern"-Button auf dem Ergebnis-Bildschirm

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
