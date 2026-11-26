# Roadmap

Entscheidungen des Projektinhabers: nur Karten, einzeln einstellbarer Look wie bei Frosted Glass, aber farbig und modern; farbige Kacheln mit eigenen Kontrasten, unabhängig von Hintergrund, Hell/Dunkel und Theme; mehrere Schriften. Alles Weitere sind Vorschläge.

## 0.11.0
Ohne Viewsta-Theme folgen die Karten jetzt dem Dashboard-Theme (zum Beispiel Frosted Glass): Fläche, Unschärfe, Rand, Ecken, Schatten und Schrift kommen vom Theme, die Akzentfarbe von dessen Primärfarbe. Vorher galt dann Gelb · Silber, und je nach Stil waren Karten teils farbig, teils dunkel. Eine an der Karte gewählte Palette bleibt farbig.

## 0.10.1
Wikipedia: Der zuletzt geladene Eintrag erscheint sofort beim Öffnen. Vorher blieb die Karte bis zu 15 Sekunden auf „Wikipedia wird geladen …“, weil das Neuzeichnen nach dem Lesen des Zwischenspeichers gleich wieder überschrieben wurde.

## 0.10.0
Themes können Farben je Kartenart setzen (`--viewsta-<kartenart>-<name>`, etwa `--viewsta-weather-accent`), dazu eine eigene Reglerfarbe (`--viewsta-control`). Bei Eckenradius 0 sind Regler, Schalter und Knöpfe eckig. Schrift auf einer eigenen Zweitfarbe wählt jetzt die besser lesbare von Hell und Dunkel. Grundlage für die Sets Metro Mono, Duet Blue und Duet Orange in Themebook 0.5.0.

## 0.9.1
Eine an der Karte gewählte Palette hat jetzt Vorrang vor Akzent-, Schrift- und Zweitfarbe aus einem Theme (wichtig für die Looks in Themebook 0.4.0, etwa mehrere Farben nebeneinander im Look Metro).

## 0.9.0
Fünf neue Paletten nach dem Muster heller Akzent und tiefe Partnerfarbe: Himmel · Nachtblau, Zitrone · Graphit, Salbei · Tanne, Koralle · Petrol, Flieder · Tinte. Kein Rand mehr als Standard (nur noch mit „Fein“ oder „Wie Theme“), dadurch füllt die geteilte Uhr die Kachel ohne Kante. Geteilte Uhr rechts standardmäßig in der Zweitfarbe. Wetter standardmäßig in der dunklen Kachel mit Symbol in der Akzentfarbe, der Himmelsverlauf ist als Kachelfarbe „Himmel“ wählbar. Schalter-Karte: Feld für weitere Entitäten hieß fälschlich „Kalender“. Uhr: Beschriftungen nennen, in welchen Stilen Datum, Doppelpunkt und Ausrichtung wirken. Nachtrot lässt sich für eine ganze Ansicht über die Theme-Variable `viewsta-night-red: "on"` einschalten. In Chromium mit Beispieldaten geprüft, in Home Assistant noch zu bestätigen.

## 0.8.0
Feste Größenklassen für Sonne, Mond und Wetter (klein, breit, groß) mit wachsender Informationsdichte. Sonne: Kreisbogen, nachts unter dem Horizont. Mond: groß mit den nächsten vier Hauptphasen. Wetter: neue Stundenreihe, aktuelles Wetter groß mit fünf Tagen, UV-Index in den fünf Stufen der WHO, Wind in Beaufort mit Böen statt Kompass, Symbole aus den Material Design Icons. Wikipedia: Text passt sich genauer ein, Jahreszahl wird bei langem Text kleiner, Ausblenden nur wenn nötig. Schlagzeilen: Titel ganz, nur die letzte angeschnittene Meldung blendet aus.

## 0.7.1
Abfahrten ohne doppelte erste Fahrt. Durchlaufen langer Zeilen auch in Safari. Ausblenden robuster (neu messen nach Schriftladen und Größenänderung, feste Flächen blenden immer weich aus). Wettersymbol größer.

## 0.7.0
Festes Raster: Innenabstand 16 px (kleine Kacheln 12 px), Radius 24 px, Innenradius R − P. Option „Rand“ (fein oder wie Theme). Editor zeigt die wirksamen Namen in Klammern. Abfahrten: Verspätung nicht mehr doppelt gerechnet, Ausfälle durchgestrichen, Antippen ohne Detailfenster. Aufgaben: Kopf öffnet die bearbeitbare Liste. Wikipedia: nur die nötige Abfrage, alter Stand bis zum neuen, Text wird eingepasst, kurze Quelle. Schlagzeilen: eine Meldung pro Zeile, Textgröße. Termine: lange Zeilen durchlaufen. Fotos: Pfeile.

## 0.6.0
Lange Texte werden sanft ausgeblendet statt abgeschnitten, mit Platz für Unterlängen. Schlagzeilen: Datum von Feeds ohne Jahresangabe richtig gelesen, Antippen öffnet die Meldung, neues Laufband in mehreren Zeilen (verschiedene Meldungen oder nur die jüngste versetzt). Uhr: Kontur ohne sichtbare Überschneidungen in den Ziffern, Klapptafeln ohne pulsierende Punkte. Schalter-Karte: Schalter ein/aus als Regler, mehrere Entitäten gemeinsam schalten. Raum: beliebige Geräte wählbar, Einzelschalter je Gerät und Schalter für alle. Aufgaben: Halten oder Doppeltipp öffnet die Liste. Fotos: Auswahl über die Mediathek von Home Assistant, Hochladen dort über „Verwalten“; der Hochlade-Knopf auf der Karte entfällt.

## 0.5.0
Neue Karten: Raum (Temperatur, Feuchte, Lichter, Fenster und Türen, Helligkeitsregler, wählbar), Szenen-Leiste, Fortschritt (Tag, Woche, Monat, Jahr), Wikipedia (Was geschah heute, Artikel des Tages). Schalter-Karte: Stil „Schalter“ mit großem Symbol ohne Regler, Option „Regler ausblenden, wenn ausgeschaltet“. Fotos: Bilder aus Immich oder einer anderen Medienquelle, Hochladen vom Gerät. Wetter: Satz neu formuliert, dazu UV-Index, Wind mit Richtung und Einzelwerte. Sensor: Stil „Pegel“. Uhr: einheitliche Größen und Ränder, in quadratischen Kacheln Stunden über Minuten, Klapptafel und Bahnhofsuhr in klassischen Farben, Bahnhofsuhr nachts rot.

Offen: Test in Home Assistant und auf dem iPhone. Wikipedia war aus der Entwicklungsumgebung nicht erreichbar und ist nur mit nachgestellten Daten geprüft; die Nutzungsbedingungen von Wikimedia sind noch an der Quelle zu lesen. Zurückgestellt auf Wunsch: Rezept-Karte.

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
- Rezept des Tages (auf Wunsch, Rezepte bleiben außerhalb des Repos). Nicht gewünscht: Gestirne, Medien-Karte.
- Farbwähler im Editor, Zeitzonen-Suche, Klapp-Animation.
- Eingebettete Schriften schlanker machen.
