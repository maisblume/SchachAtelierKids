# Schach-Abenteuer 🦊

Eigenständige Kids-Schach-App mit KI-Gegner und Lern-Coach, herausgelöst aus dem Kinder-Modus der großen Schach-App.

## Installation / Update (GitHub Pages)
1. Beim ersten Mal: alle Dateien in diesem Ordner direkt (ohne Unterordner) in ein GitHub-Repository hochladen, dann unter Repo-Einstellungen → "Pages" die Veröffentlichung vom main-Branch (Root) aktivieren.
2. Für spätere Updates reicht es, **nur `index.html` zu ersetzen** — manifest.json, sw.js und die Icons bleiben unverändert bestehen. Der Service Worker lädt die neue Version automatisch beim nächsten Öffnen nach (network-first).
3. Die App lässt sich auf dem Handy "zum Home-Bildschirm hinzufügen" (PWA-Installation).

## Features
- **Vier Fuchs-Niveaus + adaptiver Modus** ("🧭 Adaptiv", Standard): passt sich live an gute/schlechte Zugserien an und kalibriert sich zwischen Partien nach Sieg/Niederlage neu. Startet bei 🐣 Sehr leicht, sichtbare Einblendung bei Niveauwechsel, jederzeit unter ⚙️ zurücksetzbar.
- **Vier Persönlichkeiten** für den Fuchs-Gegner (Ausgewogen, Mutiger Löwe, Schildkröte, Kluger Adler).
- **Eine einzige Coach-Zeile** statt vieler Boxen — zeigt priorisiert Bedrohungen, Zugbewertung, Reaktionen (Schach/Schlagen/Sonderregeln), Ziel-Tipp oder Zauber-Tipp, aber nie mehrere gleichzeitig.
- **Bedrohungs-Radar**: markiert nur wirklich ungedeckte eigene Figuren (nicht jede theoretisch angegriffene), mit kurzer Texterklärung.
- **Bei großen Fehlern kurz nachfragen**: unterbricht nur bei wirklich großen Materialverlusten (z.B. Damenverlust), nicht bei jeder Kleinigkeit.
- **Partie-Rückblick**: nach jeder Partie die stärksten/schwächsten Züge anklickbar mit Erklärung.
- **🧠 Fehler-Training**: Positionen mit klaren Fehlern werden automatisch gespeichert und später als "Finde den besseren Zug"-Rätsel wiedervorgelegt — mit sichtbarer Markierung des damals gespielten Zugs, korrekter Brettausrichtung und Spaced-Repetition-Rhythmus (1/3/7/16 Tage bei Erfolg, ca. 3 Std. bei Misserfolg). Badge im Header zeigt fällige Rätsel.
- **Zug zurück**: nimmt nur das letzte Zugpaar zurück, nicht die ganze Partie.
- Läuft komplett offline (keine externe KI-Anbindung, kein CDN nötig).

## Speicherung
Alle Daten (Spielstand, Statistik, adaptives Niveau, Fehler-Sammlung) liegen im `localStorage` des Geräts. Unter ⚙️ → Sicherung können sie als Datei exportiert/importiert werden.
