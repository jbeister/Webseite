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
- **Logo/Titel**: "Anime Aktuell" in Rot – großes A mit "nime" oben und "ktuell" unten
- Inspiriert an einer echten Zeitung, aber digital und anime-artig

## Inhalt
- **Ausgabe 1**: vorhanden (Titelbild + Ideen)
- **Ausgabe 2**: noch in Bearbeitung
- Bilder werden nach und nach eingefügt – Struktur ist bereits vorbereitet
- Empfehlungen: Aggretsuko, Kamikaze Kaito Jeanne (weitere in Bearbeitung)

## Technik
- Bootstrap (CSS + JS) ist bereits eingebunden (lokal in `/css/` und `/js/`)
- Kein separater Server nötig – einfache HTML-Dateien
- Anfängerprojekt: Erklärungen zu allem auf einfachem Niveau
- Responsiv: funktioniert auf Handy UND Computer (Bootstrap Responsive Design)

## Seitenstruktur (fertig)
- `index.html` – Startseite mit Logo, Anime-Augen, Top-Listen, Quiz-Score
- `ausgaben.html` – Übersicht aller Ausgaben
- `ausgabe1.html` – Seiten der Ausgabe 1 (mit Klick-zum-Vergrößern)
- `ausgabe2.html` – Seiten der Ausgabe 2 (noch in Bearbeitung)
- `empfehlungen.html` – Joshuans eigene Anime-Empfehlungen
- `extras.html` – Quiz-Seite (25 Fragen, zufällig gemischt)
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
- 25 Fragen zu: One Piece, Demon Slayer, Naruto, Spy×Family, Jujutsu Kaisen,
  Tagebücher der Apothekerin, Aggretsuko, Kamikaze Kaito Jeanne,
  Dragon Ball Z, Attack on Titan, My Hero Academia, Death Note
- Fragen werden bei jedem Start zufällig gemischt
- Score wird im localStorage gespeichert und auf der Startseite angezeigt

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
