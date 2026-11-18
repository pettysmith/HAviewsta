# Viewsta

Colorful, modern cards for Home Assistant, inspired by Apple StandBy. Every card is one element with several styles. The look is set per card, per view or per dashboard, and does not depend on your theme, background or light/dark mode: tiles bring their own colors and contrast.

Cards (version 0.7.0):

| Card | Type | Styles |
| --- | --- | --- |
| Clock | `custom:viewsta-clock-card` | `digital`, `split`, `stack`, `outline`, `float`, `words`, `flip`, `flipclassic`, `analog`, `numbers`, `rings`, `station`, `stationclassic` |
| Calendar | `custom:viewsta-calendar-card` | `agenda`, `month`, `countdown`, `date`, `poster`, `week`, `dateagenda`, `timeline` |
| World time | `custom:viewsta-worldclock-card` | `list`, `dials` |
| Sun | `custom:viewsta-sun-card` | arc with sunrise and sunset |
| Day and night map | `custom:viewsta-daynight-card` | dot map with the day/night line |
| Switch / entity | `custom:viewsta-entity-card` | `tile`, `button` (large icon, plain on/off), `wide`, `value`; sliders and color buttons on the tile, tap, double tap and hold |
| Room | `custom:viewsta-room-card` | temperature, humidity, lights, open windows and doors, one switch per device, one switch for all, brightness slider; pick what to show and which devices to switch |
| Scenes | `custom:viewsta-scenes-card` | `buttons`, `pills`; a bar of scenes, scripts or switches |
| Progress | `custom:viewsta-progress-card` | `bar`, `ring`, `dots`; day, week, month or year |
| Wikipedia | `custom:viewsta-wiki-card` | `onthisday`, `article` |
| Weather | `custom:viewsta-weather-card` | `now`, `text`, `days`, `temp`, `rain`, `combo`, `uv`, `wind`, `details` |
| To-do | `custom:viewsta-todo-card` | `list` (tap to check off, hold or double tap opens the list), `count` |
| Sensor | `custom:viewsta-sensor-card` | `chart`, `level` (water level with highest and lowest value), `bars`, `value`, `ring` |
| Moon | `custom:viewsta-moon-card` | `disc`, `only`; calculated, needs no integration |
| Departures | `custom:viewsta-departures-card` | `list`, `next`; shows the sensor of an existing departures integration |
| Photos | `custom:viewsta-photos-card` | folders or pictures picked in Home Assistant's media browser, Immich, or own addresses; crossfade |
| Headlines | `custom:viewsta-news-card` | `headline`, `list`, `ticker`, `rows` (ticker in several lines); tap opens the article |
| Timer | `custom:viewsta-timer-card` | `digital`, `ring`; tap starts and pauses |

Every card has a visual editor with dropdowns, switches and entity pickers. YAML works too.

## Install

Settings → Marketplace → **Add from link** → `pettysmith/HAviewsta` → install. Reload the browser afterwards.

## Add a card

Edit dashboard → **Add card** → search for "Viewsta" → pick a card. The editor lets you choose the style, palette, tile color, font and the other options by clicking.

## Look

Options that every card understands:

| Option | Meaning | Default |
| --- | --- | --- |
| `palette` | One of the 12 palettes or `Nachtrot`, one of 16 single colors (the other colors are derived), or `theme` to follow your Home Assistant theme | `Gelb · Silber` |
| `night_red` | Switch to `Nachtrot` while the sun is below the horizon (uses `sun.sun`) | `false` |
| `surface` | Tile color: `accent`, `invert` (accent colors swapped), `tint`, `dark`, `black`, `card` (your theme's card), `none`, or any CSS color | depends on card and style |
| `font` | `rounded` (embedded Nunito), `archivo`, `serif`, `mono`, `theme` | `rounded` |
| `radius` | Corner radius, e.g. `16px` | `24px` |
| `border` | `auto`, `none`, `fine` (hairline inside the tile), `theme` (uses `--ha-card-border-width` and `--ha-card-border-color` of your theme, e.g. Frosted Glass) | `auto` |
| `accent`, `on_accent`, `tint`, `text` | Override single colors; any CSS color works (`#fff`, `rgb()`, names) | from palette |

Switch / entity card options:

| Option | Meaning | Default |
| --- | --- | --- |
| `controls` | Controls shown on the tile: `switch` (on/off switch), `brightness`, `color`, `color_temp` (lights), `position` (covers), `speed` (fans), `volume` (media players), `temperature` (climate), `value` (numbers), `none` | the main control of the entity |
| `entities` | More entities switched together with `entity`, e.g. several lamps | none |
| `colors` | Colors offered by the `color` control, any CSS colors | nine preset colors |
| `tap_action`, `double_tap_action`, `hold_action` | `auto` (toggle, or details if the entity cannot be toggled), `toggle`, `more-info`, `none` | `auto`, `none`, `more-info` |
| `off_surface` | Tile while the entity is off: `invert`, `dark`, `black`, `tint`, `card`, `none` | `invert` |
| `collapse_controls` | Hide the controls while the entity is off | `false` |

Drag a slider or tap it to set a value; the tile is on the accent color while the entity is on and swaps its two colors while it is off.

A card without an entity shows sample data marked "Beispiel", so the card picker and a freshly added card look like the finished card.

Photos card: choose `source: media` and pick folders or single pictures in the field below; the picker is Home Assistant's own media browser. To add pictures from your phone or computer, open "Manage" ("Verwalten") in that browser inside "My media" and upload them there, then pick them. Uploading needs an administrator account. `source: immich` shows all pictures the Immich integration offers (favorites and albums, at most 60 by default).

Headlines card options:

| Option | Meaning | Default |
| --- | --- | --- |
| `open_links` | Tapping a headline opens the article in the browser (only `http` and `https` links) | `true` |
| `ticker_mode` | For `rows`: `single` (one headline per line), `mixed` (all headlines, every line starts elsewhere) or `latest` (only the newest, offset in every line) | `mixed` |
| `text_size` | `s`, `m`, `l`, `xl` | `m` |
| `ticker_rows` | For `rows`: number of lines | `4` |
| `ticker_speed` | For `ticker` and `rows`: speed, 1 is normal | `1` |

Dates of feed entries without a year (some feed integrations write `Mon, Nov 16 10:30 PM`) are read as this year. Entries without a readable date show no age.

To-do card: `hold_action` and `double_tap_action` can be `list` (open the list in Home Assistant), `more-info` or `none`; defaults `list` and `none`.

Layout: every tile keeps 16 px between content and edge (12 px on tiles under 140 px), corner radius 24 px, inner elements use radius minus padding. The calendar option `scroll_long` lets long titles scroll. The photos card has arrows to step through the pictures (`show_arrows`).

Long texts are not cut off: they fade out at the end, and there is room for descenders such as g and p.

Clock card options:

| Option | Meaning | Default |
| --- | --- | --- |
| `colon` | `steady`, `pulse` (fades once per second) or `off`; styles digital, outline, float, flip | `steady` |
| `align` | `left`, `center`, `right`; styles digital and words | `center` (digital), `left` (words) |
| `hour12` | 12-hour display with AM/PM | `false` |
| `show_seconds` | Second hand, analog styles only | `true` |

Single colors: Gelb, Orange, Rot, Pink, Magenta, Lila, Indigo, Blau, Cyan, Mint, Grün, Limette, Pfirsich, Sand, Silber, Weiß.

Palettes: Gelb · Silber, Rosa · Blau, Limette · Tanne, Orange · Creme, Mint · Marine, Rot · Rosé, Lila · Gelb, Pfirsich · Bordeaux, Blau · Eis, Grün · Pink, Silber · Schwarz, Marine · Creme, Nachtrot.

### One look for a whole dashboard

Pick one of these:

1. **View theme (recommended):** install the companion repository `pettysmith/HAthemebook`. It only sets variables for these cards and changes nothing else in Home Assistant. Edit dashboard → pencil next to the view name → **Theme** dropdown → pick a Viewsta theme. Do not choose it in your profile, that would replace your own theme. Leave `Palette` on *Automatisch* in the cards, otherwise the card wins.

2. **A helper:** create an `input_select` with the palette names and add `palette_entity: input_select.viewsta_palette` to each card. Changing the helper changes all those cards at once, for example by an automation at sunset.
3. **CSS variables:** `--viewsta-palette`, `--viewsta-accent`, `--viewsta-font`, `--viewsta-surface` set by any theme or card-mod. Options on the card win over variables.

## YAML examples (optional)

```yaml
type: custom:viewsta-clock-card
style: digital
palette: Rosa · Blau
font: archivo
```

```yaml
type: custom:viewsta-calendar-card
entities:
  - calendar.my_calendar
style: agenda
days: 14
max_items: 6
```

```yaml
type: custom:viewsta-worldclock-card
zones:
  - { tz: Europe/London, name: London }
  - { tz: America/New_York, name: New York }
  - { tz: Asia/Tokyo, name: Tokio }
style: list   # or dials
```

```yaml
type: custom:viewsta-sun-card
entity: sun.sun
```

```yaml
type: custom:viewsta-daynight-card
show_home: true
markers:
  - { name: Tokio, lat: 35.7, lon: 139.7 }
time_zone_2: Asia/Tokyo
name_2: Tokio
```

The calendar card needs a calendar entity in Home Assistant, for example from the Remote Calendar integration. The styles `date` and `poster` work without one.

### Where the data comes from

All cards only read what Home Assistant already has, with one exception: the Wikipedia card fetches the feed of the day from `wikipedia.org` once per day and browser, shows "Quelle: Wikipedia · Text unter CC BY-SA 4.0" and opens the article when tapped. It does not fetch anything while it is only shown in the card picker.

| Card | Needs |
| --- | --- |
| Switch / entity | any entity |
| Weather | a `weather` entity; forecasts come from Home Assistant's forecast subscription |
| To-do | a `todo` entity |
| Sensor | a numeric entity; the curve uses the recorder history |
| Departures | the sensor of a departures integration with the attributes `line`, `direction`, `delay` and `next` |
| Photos | image addresses such as `/local/photo.jpg`, `image`, `camera` or `person` entities, or a media source: the Immich integration (`source: immich`), your own media folder `viewsta` (`source: local`) or any other (`source: custom` with `media_source`) |
| Room | an area; lights, windows, doors and sensors are taken from it, or pick them yourself |
| Scenes | scenes, scripts, buttons or switches |
| Headlines | entities that carry a `title` attribute or an `entries` list, for example from a feed integration |
| Timer | a `timer` helper |

The calls for weather forecasts, to-do lists, sensor history, the details dialog and the grid layout were checked against the Home Assistant frontend source. The attribute names of departure and headline entities were not; if one of these cards shows nothing, please open an issue with the entity's attributes.

## Local preview

Open `dev/preview.html` (clocks, calendar, sun, map) or `dev/preview-cards.html` (all other cards) in a browser. Both show the cards with sample data on several backgrounds; `?t=22:15` sets a fixed time. Icons are placeholders there, the real ones come from Home Assistant.

## License and credits

MIT, see `LICENSE`. Embedded fonts and map data: `LICENSES.txt`. Sources and inspirations: `CREDITS.md`.
