# Viewsta

Colorful, modern cards for Home Assistant, inspired by Apple StandBy. Every card is one element with several styles. The look is set per card, per view or per dashboard, and does not depend on your theme, background or light/dark mode: tiles bring their own colors and contrast.

Cards (version 0.2.0):

| Card | Type | Styles |
| --- | --- | --- |
| Clock | `custom:viewsta-clock-card` | `digital`, `split`, `stack`, `outline`, `float`, `words`, `flip`, `analog`, `numbers`, `rings`, `station` |
| Calendar | `custom:viewsta-calendar-card` | `agenda`, `month`, `countdown` |
| World time | `custom:viewsta-worldclock-card` | `list`, `dials` |
| Sun | `custom:viewsta-sun-card` | arc with sunrise and sunset |
| Day and night map | `custom:viewsta-daynight-card` | dot map with the day/night line |

Every card has a visual editor with dropdowns, switches and entity pickers. YAML works too.

## Install

Settings → Marketplace → **Add from link** → `pettysmith/HAviewsta` → install. Reload the browser afterwards.

## Add a card

Edit dashboard → **Add card** → search for "Viewsta" → pick a card. The editor lets you choose the style, palette, tile color, font and the other options by clicking.

## Look

Options that every card understands:

| Option | Meaning | Default |
| --- | --- | --- |
| `palette` | One of the 12 palettes or `Nachtrot`, or `theme` to follow your Home Assistant theme | `Gelb · Silber` |
| `surface` | Tile color: `accent`, `tint`, `dark`, `black`, `card` (your theme's card), `none`, or any CSS color | depends on card and style |
| `font` | `rounded`, `archivo`, `serif`, `mono`, `theme` | `rounded` |
| `radius` | Corner radius, e.g. `16px` | `28px` |
| `accent`, `on_accent`, `tint`, `text` | Override single colors | from palette |

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

The calendar card needs a calendar entity in Home Assistant, for example from the Remote Calendar integration.

## Local preview

Open `dev/preview.html` in a browser. It shows all cards with sample data on four backgrounds.

## License and credits

MIT, see `LICENSE`. Embedded fonts and map data: `LICENSES.txt`. Sources and inspirations: `CREDITS.md`.
