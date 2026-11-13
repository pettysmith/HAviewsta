# Arbeitsanweisung für Claude Code

Projekt: Viewsta, benutzerdefinierte Karten für Home Assistant (öffentliches Repo, Installation über den Marketplace per „Add from link“). Die Karten sind farbig, modern und unabhängig von Theme, Hintergrund und Hell/Dunkel, angelehnt an Apple StandBy.

Persönliche Arbeitsregeln des Projektinhabers und alle privaten Angaben stehen in einer Ergänzung, die nicht im Repo liegt:
@~/.claude/standby-privat.md
Fehlt die Datei, arbeite mit den Regeln unten weiter und frage nach, statt zu raten.

## Stand
`dist/viewsta.js` (0.2.0) enthält fünf Karten (Uhr, Termine, Weltzeit, Sonne, Tag-Nacht-Karte) mit Klick-Editor über `static getConfigForm()`. Getestet mit Beispieldaten in `dev/preview.html`; der Editor und die Karten sind noch nicht in einem laufenden Home Assistant gesehen. Nicht neu schreiben, sondern prüfen und verbessern.

## Erst lesen
README.md, ROADMAP.md, CREDITS.md, dev/preview.html

## Regeln
- Kurz antworten. Erst die gestellte Frage beantworten.
- Änderungen nur nach ausdrücklichem Auftrag. Vorher zeigen, welche Dateien sich ändern und wie. Commit und Push nur nach ausdrücklicher Freigabe, das Repo ist öffentlich.
- Nichts erfinden. Annahmen als offene Frage kennzeichnen.
- Vorhandenes anpassen statt neu bauen. Für ÖPNV-Abfahrten gibt es fertige Integrationen und Karten; keine eigene Abfragelogik.
- Karten bleiben eine einzelne Datei ohne Build-Schritt und ohne Abhängigkeiten. Ein Element pro Kartenart, Stile über die Option `style`.
- Jede Karte muss auf hellem, dunklem und buntem Hintergrund und mit jeder Schrift lesbar sein. Prüfen mit `dev/preview.html` und Playwright-Screenshots.

## Quellen würdigen
Jede genutzte Ressource (Schrift, Daten, Code, Vorbild) wird vor der Veröffentlichung in CREDITS.md und, falls eingebettet, in LICENSES.txt eingetragen: Urheber, Lizenz, wie sie genannt wird, Stand. Nichts als geprüft markieren, was nicht an der Quelle nachgelesen wurde.

## Öffentliche Dateien
Alles in diesem Repo ist öffentlich. Nicht hineinschreiben: Klarnamen, Wohnort, Arbeitgeber, Adressen, IPs, Gerätetypen, Netz- und Zugangsdetails, Token, Passwörter, Kontaktdaten, private Pläne, Screenshots mit Konten oder Gerätenamen. Als Autor steht nur der GitHub-Name `pettysmith`. Vor jedem Commit alle geänderten Dateien danach durchsuchen und das Ergebnis zeigen.
