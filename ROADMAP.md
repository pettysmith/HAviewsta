# Roadmap

Entscheidungen des Projektinhabers: nur Karten, einzeln einstellbarer Look wie bei Frosted Glass, aber farbig und modern; farbige Kacheln mit eigenen Kontrasten, unabhängig von Hintergrund, Hell/Dunkel und Theme; mehrere Schriften. Alles Weitere sind Vorschläge.

## 0.2.1 (vorbereitet)
Uhr: Doppelpunkt (fest, pulsierend, aus), Ausrichtung, 12-Stunden-Anzeige mit AM/PM, eingebettete runde Schrift. Sonne: Nachtansicht mit Mond und „Aufgang in …“, größerer Bogen. Farben: jede CSS-Farbe als Eingabe, Theme-Palette liest die echten Farben des Dashboards, lesbare Markierungen. Weltzeit ohne Überlappung. Ausgewogenere Gestaltung nach dem Vorbild von Apple StandBy: Uhrzeiten optisch mittig, einheitlicher vertikaler Schwerpunkt, Monatsblatt mit gleichmäßigem Raster, Wochenende gedämpft, Termin-Punkte ohne Überschneidung, einheitliche Linienstärken bei Ziffernblättern, Sonne und Tag-Nacht-Karte. Termine laden bei Änderung im Editor neu. Karten zeichnen nur noch bei relevanten Änderungen neu. Vorschau mit festem Zeitpunkt (`?t=HH:MM`), Theme-Fall und Größenfällen.

## 0.2.0
Klick-Editor für alle Karten (Formular von Home Assistant). Nach Screenshots des Projektinhabers erscheint der Editor mit Vorschau und Layout-Reiter, die Themes sind in der Ansicht wählbar. Offen: Zeitzonen-Auswahl mit Suche, Farbwähler statt Textfeldern, Test mit aktivem Frosted-Glass-Profil.

## 0.1.0
Uhr (11 Stile), Termine (Liste, Monat, Countdown), Weltzeit (Liste, Ziffernblätter), Sonne, Tag-Nacht-Karte. Palette, Oberfläche, Schrift und Radius je Karte; Dashboard-weit über Ansichts-Theme, Helfer oder CSS-Variablen.

## Später
- Abfahrten: vorhandene Integration und Karte anpassen (kein eigener Datenabruf).
- Weitere Karten nach Wunsch: Wetter, Medien, Pegel, Mond, Fotos, Nachrichten (Vorlage: eigenes früheres Dashboard). Nicht gewünscht: Gestirne.
- Weitere Kalender-Stile (Woche, Datum und Termine, Wochentag-Plakat), Einzelfarben-Ableitung, Klapp-Animation.
- Eingebettete Schriften schlanker machen.
