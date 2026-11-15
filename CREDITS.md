# Quellen und Lizenzen

Stand: 0.4.0. Jeder neue Baustein wird hier eingetragen, bevor er veröffentlicht wird. Vollständige Lizenztexte: `LICENSES.txt`.

| Quelle | Wofür | Lizenz | Stand |
| --- | --- | --- | --- |
| Archivo Black, The Archivo Black Project Authors (Omnibus-Type) | Schrift „archivo“, als WOFF2 eingebettet (Dateien aus @fontsource/archivo-black 5.3.0) | SIL Open Font License 1.1 | Lizenzdatei im Paket gelesen |
| Nunito, The Nunito Project Authors (github.com/googlefonts/nunito) | Schrift „rounded“, Gewichte 700 und 800 als WOFF2 eingebettet, auf Latein und Ziffern gekürzt (@fontsource/nunito 5.3.0) | SIL Open Font License 1.1 | Lizenzdatei im Paket gelesen (Kopfzeile und Lizenztext) |
| Space Mono, The Space Mono Project Authors | Schrift „mono“, als WOFF2 eingebettet (@fontsource/space-mono 5.3.0) | SIL Open Font License 1.1 | Lizenzdatei im Paket gelesen |
| global-land-mask 1.0.0, Todd Karin (github.com/toddkarin/global-land-mask), Daten GLOBE der NOAA | Landmaske der Tag-Nacht-Karte (90 × 40 Raster) | MIT License | Lizenzdatei geladen |
| Sonnenstand und Tag-Nacht-Linie | Karten „Tag-Nacht“ | eigene Umsetzung gängiger astronomischer Näherungsformeln | geprüft |
| Zeitansage „in Worten“, Bahnhofsuhr (eigene schlichte Variante, nicht die SBB-Uhr), Klapptafel | Uhr-Stile | eigene Umsetzung | geprüft |
| Mondphase (Karte „Mond“) | Phase, Beleuchtung, nächster Voll- und Neumond | eigene Umsetzung einer gängigen Näherung über die mittlere synodische Periode (29,530588853 Tage); Abweichung bis zu einigen Stunden | geprüft gegen zwei bekannte Termine |
| Wettersymbole, Wetterverläufe, 16 Einzelfarben und ihre Ableitung | Karten „Wetter“ und Palette | eigene Zeichnungen und Werte des Autors (aus dem früheren Dashboard) | Status wie Vorlage: offen |
| Home Assistant Frontend (github.com/home-assistant/frontend, Stand 15. November 2026, Commit f2d0da0): `weather/subscribe_forecast`, `todo/item/list`, Dienst `todo.update_item`, `history/history_during_period`, Ereignis `hass-more-info`, Element `ha-state-icon`, Eigenschaft `layout` der Karten, Aufbau der Kartenauswahl, Dauer für Halten | Daten und Verhalten der Karten | Apache License 2.0; nur aufgerufen, kein Code übernommen | an der Quelle gelesen |
| Dienste von Home Assistant für die Regler (`light.turn_on`, `cover.set_cover_position`, `fan.set_percentage`, `media_player.volume_set`, `climate.set_temperature`, `number.set_value`, `homeassistant.toggle`) | Schalter-Karte | Teil von Home Assistant (Apache 2.0); nur aufgerufen | aus dem Gedächtnis, an der Quelle noch zu prüfen |
| Sensor einer Abfahrts-Integration von Home Assistant (Attribute `line`, `direction`, `delay`, `next`) | Karte „Abfahrten“, nur Anzeige | Teil von Home Assistant (Apache 2.0); kein Code übernommen | Attributnamen aus dem Gedächtnis, an der Quelle noch zu prüfen |
| Paletten in `palettes.json` | Farben | eigene Zusammenstellung des Autors | geprüft |
| Apple StandBy | Gestalterisches Vorbild | Marke der Apple Inc.; weder Code noch Bilder übernommen | geprüft |
| Eigenes früheres Dashboard des Autors (Web-App im Querformat) | Vorlage für Stile, Farbrollen und Paletten der Karten | eigene Werke des Autors; das Repo der Vorlage hat keine eigene Lizenzdatei | Status offen, vor weiteren Übernahmen klären |
| Home Assistant Dokumentation zu benutzerdefinierten Karten | Aufbau von Karten (`setConfig`, `hass`, `getGridOptions`) | Dokumentation des Projekts | zu prüfen, bevor Inhalte übernommen werden |
