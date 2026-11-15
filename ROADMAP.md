# Roadmap

Entscheidungen des Projektinhabers: nur Karten, einzeln einstellbarer Look wie bei Frosted Glass, aber farbig und modern; farbige Kacheln mit eigenen Kontrasten, unabhängig von Hintergrund, Hell/Dunkel und Theme; mehrere Schriften. Alles Weitere sind Vorschläge.

## 0.4.0
Schalter-Karte: Regler direkt auf der Kachel (Helligkeit, Farbe, Farbtemperatur, Position, Stufe, Lautstärke, Solltemperatur, Wert), wählbar im Editor; Antippen, Doppeltipp und Halten einstellbar; ausgeschaltet werden die beiden Akzentfarben getauscht statt die Kachel abzudunkeln (neue Kachelfarbe „Akzent umgekehrt“ für alle Karten). Vorschau: Karten ohne gewählte Entität zeigen Beispieldaten mit dem Hinweis „Beispiel“, und nur in der Abschnitte-Ansicht füllt die Karte die Zelle (in der Kartenauswahl behält sie ihr Format). Schnittstellen am Quelltext des Home-Assistant-Frontends nachgelesen. In Chromium geprüft, in Home Assistant und auf dem iPhone noch zu bestätigen.

## 0.3.2
Karten füllen in der Abschnitte-Ansicht ihre Rasterzelle (vorher blieb die Karte bei ihrem Entwurfsformat und der Inhalt wurde in Safari winzig und abgeschnitten). Innenfläche wird fest positioniert statt über eine Prozenthöhe berechnet. Schriftgrößen sind auch in hohen Zellen begrenzt. Vorschau mit quadratischen, hohen und nur in der Breite festgelegten Zellen. In Chromium geprüft, auf dem iPhone noch zu bestätigen.

## 0.3.1
Darstellung auf dem iPhone (Safari): Zeichnungen haben jetzt feste Größen statt einer Höhe aus dem Seitenverhältnis, damit unten nichts mehr abgeschnitten wird (Sonne, Ziffernblätter, Tag-Nacht-Karte, Ringe, Mond, Kurven). Ziffernblätter der Weltzeit füllen die Kachel und stehen mittig, auch bei ungerader Anzahl. Nur in Chromium geprüft, auf dem iPhone noch zu bestätigen.

## 0.3.0 (vorbereitet)
Neun neue Karten: Schalter/Entität, Wetter (6 Stile), Aufgaben, Sensor (Kurve, Säulen, Wert, Ring), Mond (berechnet), Abfahrten (zeigt den Sensor einer vorhandenen Integration), Fotos, Schlagzeilen, Timer. Termine: fünf weitere Stile (Datum groß, Wochentag-Plakat, Woche, Datum und Termine, Tagesverlauf mit Jetzt-Linie). Für alle Karten: 16 Einzelfarben mit abgeleiteten Begleitfarben, Option „Nachts Nachtrot“, Antippen öffnet die Details der Entität. Zweite Vorschau `dev/preview-cards.html`.

Offen: Test in einem laufenden Home Assistant. Ungeprüft sind dort die Vorhersage-Abfrage der Wetter-Karte, das Laden und Abhaken der Aufgaben, der Verlauf der Sensor-Karte, die Attribute des Abfahrts-Sensors und der Schlagzeilen-Entitäten sowie die Symbole der Schalter-Karte. Nicht gebaut: Medien-Karte (abgewählt), Rezept des Tages (Aufbau der Rezeptesammlung unbekannt).

## 0.2.1 (vorbereitet)
Uhr: Doppelpunkt (fest, pulsierend, aus), Ausrichtung, 12-Stunden-Anzeige mit AM/PM, eingebettete runde Schrift. Sonne: Nachtansicht mit Mond und „Aufgang in …“, größerer Bogen. Farben: jede CSS-Farbe als Eingabe, Theme-Palette liest die echten Farben des Dashboards, lesbare Markierungen. Weltzeit ohne Überlappung. Ausgewogenere Gestaltung nach dem Vorbild von Apple StandBy: Uhrzeiten optisch mittig, einheitlicher vertikaler Schwerpunkt, Monatsblatt mit gleichmäßigem Raster, Wochenende gedämpft, Termin-Punkte ohne Überschneidung, einheitliche Linienstärken bei Ziffernblättern, Sonne und Tag-Nacht-Karte. Termine laden bei Änderung im Editor neu. Karten zeichnen nur noch bei relevanten Änderungen neu. Vorschau mit festem Zeitpunkt (`?t=HH:MM`), Theme-Fall und Größenfällen.

## 0.2.0
Klick-Editor für alle Karten (Formular von Home Assistant). Nach Screenshots des Projektinhabers erscheint der Editor mit Vorschau und Layout-Reiter, die Themes sind in der Ansicht wählbar. Offen: Zeitzonen-Auswahl mit Suche, Farbwähler statt Textfeldern, Test mit aktivem Frosted-Glass-Profil.

## 0.1.0
Uhr (11 Stile), Termine (Liste, Monat, Countdown), Weltzeit (Liste, Ziffernblätter), Sonne, Tag-Nacht-Karte. Palette, Oberfläche, Schrift und Radius je Karte; Dashboard-weit über Ansichts-Theme, Helfer oder CSS-Variablen.

## Später
- Rezept des Tages, sobald der Aufbau der Rezeptesammlung bekannt ist. Nicht gewünscht: Gestirne, Medien-Karte.
- Farbwähler im Editor, Zeitzonen-Suche, Klapp-Animation.
- Eingebettete Schriften schlanker machen.
