# Octo

A flat, monospace Home Assistant theme with a simple palette - near-black surfaces, warm off-white text, one slate-blue accent and one greige neutral.

| Token | Hex |
| --- | --- |
| Background | `#0f0f11` |
| Surface | `#1b1b1e` |
| Line | `#2e2e33` |
| Text | `#e9e7e1` |
| Muted text | `#8b8a85` |
| Accent | `#56688c` |
| Neutral | `#b2b1a9` |

Includes dark and light modes, plus two tile helper themes (`octo-accent`, `octo-neutral`).

## Install

**HACS:** add this repo as a custom repository (category: Theme), install **Octo**, then restart.

**Manual:** copy `themes/octo.yaml` into `config/themes/` and make sure `configuration.yaml` has:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

Restart (or call `frontend.reload_themes`), then pick **Octo** in your profile.

## Font

Themes can't load web fonts, so add one as a dashboard resource (Settings > Dashboards > ⋮ > Resources, type **Stylesheet**):

```
https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600&display=swap
```

`Space Mono` or `IBM Plex Mono` also work - the font stack falls back through them to your system monospace.

## Optional extras

- **[card-mod](https://github.com/thomasloven/lovelace-card-mod)** - enables uppercase card titles, tabular numbers and an uppercase header, matching the reference style more closely.
- **Tile helpers** - set `theme: octo-accent` (slate blue) or `theme: octo-neutral` (greige) on cards that support the `theme` option (gauge, entities, button, markdown, glance etc).

See `examples/dashboard.yaml` for a starter view.
