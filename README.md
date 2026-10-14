# Bastide Theme

A dark Home Assistant theme with a game-HUD feel: deep navy background, orange and blue accents, square cards and condensed type.

It is designed to go with [Bastide Cards](https://github.com/Bolero27/bastide-cards). With this theme active, Bastide Cards switch to their HUD look (slanted buttons and chips, bevelled corners, uppercase titles) and load the theme's fonts. Other cards simply take the theme's colours.

## Installation

### HACS (recommended)

1. In HACS, open the menu (⋮) → **Custom repositories**.
2. Add `https://github.com/Bolero27/bastide-theme` with the type **Theme**.
3. Search for **Bastide Theme** in HACS and download it.
4. Restart Home Assistant, or call the `frontend.reload_themes` action.
5. In your profile, pick **Bastide** as the theme.

Your `configuration.yaml` needs the themes folder enabled:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

### Manual

Copy `themes/bastide.yaml` to the `themes` folder of your configuration, then reload themes.

## Fonts

The theme uses [Barlow and Barlow Condensed](https://fonts.google.com/specimen/Barlow) (SIL Open Font License). Bastide Cards load them from Google Fonts when the theme is active. Without Bastide Cards, Home Assistant falls back to Roboto.

Loading fonts from Google sends a request to Google's servers. To avoid it, add this line to the theme:

```yaml
bastide-fonts: none
```

## Colours

| Variable | Default | Used for |
| --- | --- | --- |
| `bastide-orange` | `#f99e1a` | Primary accent, heating, boilers |
| `bastide-blue` | `#3fa9f5` | Secondary accent, heat pumps, cooling |
| `bastide-pink` | `#ff5fa2` | Security, insights |
| `bastide-violet` | `#a68bff` | Calendar, night |
| `bastide-teal` | `#2ee6c5` | Living room, media |
| `bastide-yellow` | `#ffd84d` | Office, warnings |
| `bastide-green` | `#4ade80` | System, all good |
| `bastide-steel` | `#8fb3e8` | Away |

## License

[MIT](LICENSE)
