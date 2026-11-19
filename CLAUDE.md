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


## Arbeitsregeln (festgelegt vom Projektinhaber)
- Sehr kurz antworten: Ergebnis zuerst, Stichpunkte, etwa ein Viertel der früher üblichen Länge.
- Eine Frage ist kein Auftrag. Gebaut wird erst nach ausdrücklicher Freigabe. Größere Vorhaben in Pakete teilen und einzeln vorlegen, iterativ arbeiten.
- Etablierte Standardlösungen und vorhandene Systeme von Home Assistant nutzen, möglichst wenig selbst bauen, wartungsarm, keine Insellösungen. Selbst gestaltet werden nur feste Elemente.
- Nichts erfinden: an der Quelle prüfen, Ungeprüftes als ungeprüft kennzeichnen.
- Raster: Innenabstand P = 16 px (Kacheln unter 140 px: 12 px), Außenradius R = 24 px, Innenradius r = R − P. Inhalte ankern am Abstand P, Grafiken füllen die Fläche mittig. Randlos nur Fotos, geteilte Uhr, Laufband.
- Texte nie abschneiden: einpassen oder weich ausblenden, Platz für Unterlängen.

## Quellen würdigen
Jede genutzte Ressource (Schrift, Daten, Code, Vorbild) wird vor der Veröffentlichung in CREDITS.md und, falls eingebettet, in LICENSES.txt eingetragen: Urheber, Lizenz, wie sie genannt wird, Stand. Nichts als geprüft markieren, was nicht an der Quelle nachgelesen wurde.

## Öffentliche Dateien
Alles in diesem Repo ist öffentlich. Nicht hineinschreiben: Klarnamen, Wohnort, Arbeitgeber, Adressen, IPs, Gerätetypen, Netz- und Zugangsdetails, Token, Passwörter, Kontaktdaten, private Pläne, Screenshots mit Konten oder Gerätenamen. Als Autor steht nur der GitHub-Name `pettysmith`. Vor jedem Commit alle geänderten Dateien danach durchsuchen und das Ergebnis zeigen.
