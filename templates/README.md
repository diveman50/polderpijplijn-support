# Grim Reader Templates

Een template past de look-and-feel van Grim Reader aan: kleuren, fonts en achtergrondafbeeldingen. Templates worden verspreid als `.grimtemplate`-bestand (een gewone zip met een andere extensie).

## Installeren

1. Stuur het `.grimtemplate`-bestand naar je iPhone/iPad (AirDrop, Mail, Bestanden).
2. Tik op het bestand → **Open met Grim Reader**.

Of via de app: **Instellingen → Weergave → Template importeren**.

---

## Bestandsstructuur

```
mijntemplate.grimtemplate   ← zip-bestand
├── template.json            ← verplicht
├── background.jpg           ← optioneel
├── header.png               ← optioneel
└── snowflakes.png           ← optioneel
```

De afbeeldingen mogen elke naam hebben; je verwijst ernaar vanuit `template.json`.

---

## template.json

Zie [`voorbeeld.json`](voorbeeld.json) voor een kant-en-klaar startpunt.

| Veld | Type | Verplicht | Omschrijving |
|---|---|---|---|
| `id` | string | ja | Unieke identifier, alleen kleine letters en koppeltekens |
| `name` | string | ja | Naam zoals getoond in de app |
| `description` | string | ja | Korte omschrijving |
| `author` | string | ja | Naam van de maker |
| `color_primary` | hex | ja | Hoofdkleur (sectietitels, highlights) |
| `color_secondary` | hex | ja | Secundaire kleur |
| `color_background` | hex | ja | Achtergrondkleur van het startscherm |
| `color_text` | hex | ja | Standaard tekstkleur |
| `color_accent` | hex | ja | Accentkleur (knoppen, links, toggles) |
| `color_muted` | hex | ja | Gedempte kleur voor subtekst |
| `font_heading` | string | ja | Font voor koppen (zie lijst hieronder) |
| `font_body` | string | ja | Font voor lopende tekst |
| `font_mono` | string | ja | Monospace font |
| `image_background` | string\|null | nee | Bestandsnaam achtergrondafbeelding |
| `image_header` | string\|null | nee | Bestandsnaam headerafbeelding (gereserveerd) |
| `image_footer` | string\|null | nee | Bestandsnaam footerversiering (gereserveerd) |
| `image_book_card_bg` | string\|null | nee | Achtergrond boekenkaart (gereserveerd) |
| `corner_radius` | number | ja | Hoekafronding kaarten (aanbevolen: 8–20) |
| `shadow_radius` | number | ja | Schaduwsterkte (aanbevolen: 0–10) |

Kleuren als hex-string: `"#RRGGBB"` (met hekje, 6 cijfers).

---

## Afbeeldingen

| Veld | Gebruik | Aanbevolen formaat |
|---|---|---|
| `image_background` | Vult het volledige startscherm | JPG, ≥ 1290 × 2800 px, < 3 MB |
| `image_header` | Decoratie bovenaan (toekomstig) | PNG, transparantie mogelijk |
| `image_footer` | Decoratie onderaan (toekomstig) | PNG, transparantie mogelijk |

Houd het hoofdmotief **gecentreerd** — randen worden bijgesneden op kleinere schermen.

---

## Beschikbare fonts

Gebruik de **PostScript-naam** in `template.json`. Als een font niet gevonden wordt, valt iOS terug op het systeemfont.

### Serif
| PostScript-naam | Weergavenaam |
|---|---|
| `Georgia` | Georgia |
| `Georgia-Bold` | Georgia Bold |
| `Georgia-Italic` | Georgia Italic |
| `Georgia-BoldItalic` | Georgia Bold Italic |
| `TimesNewRomanPSMT` | Times New Roman |
| `TimesNewRomanPS-BoldMT` | Times New Roman Bold |
| `TimesNewRomanPS-ItalicMT` | Times New Roman Italic |
| `Palatino-Roman` | Palatino |
| `Palatino-Bold` | Palatino Bold |
| `Palatino-Italic` | Palatino Italic |
| `Baskerville` | Baskerville |
| `Baskerville-Bold` | Baskerville Bold |
| `Baskerville-Italic` | Baskerville Italic |
| `Didot` | Didot |
| `Didot-Bold` | Didot Bold |
| `Didot-Italic` | Didot Italic |
| `GillSans` | Gill Sans |
| `GillSans-Bold` | Gill Sans Bold |
| `GillSans-Italic` | Gill Sans Italic |
| `AmericanTypewriter` | American Typewriter |
| `AmericanTypewriter-Bold` | American Typewriter Bold |
| `Cochin` | Cochin |
| `Cochin-Bold` | Cochin Bold |
| `Cochin-Italic` | Cochin Italic |

### Sans-serif
| PostScript-naam | Weergavenaam |
|---|---|
| `Avenir` | Avenir Book |
| `Avenir-Medium` | Avenir Medium |
| `Avenir-Heavy` | Avenir Heavy |
| `Avenir-Black` | Avenir Black |
| `Avenir-Oblique` | Avenir Oblique |
| `AvenirNext-Regular` | Avenir Next |
| `AvenirNext-Medium` | Avenir Next Medium |
| `AvenirNext-DemiBold` | Avenir Next Demi Bold |
| `AvenirNext-Bold` | Avenir Next Bold |
| `HelveticaNeue` | Helvetica Neue |
| `HelveticaNeue-Bold` | Helvetica Neue Bold |
| `HelveticaNeue-Light` | Helvetica Neue Light |
| `HelveticaNeue-Thin` | Helvetica Neue Thin |
| `HelveticaNeue-Italic` | Helvetica Neue Italic |
| `Futura-Medium` | Futura Medium |
| `Futura-Bold` | Futura Bold |
| `Futura-MediumItalic` | Futura Medium Italic |
| `Optima-Regular` | Optima |
| `Optima-Bold` | Optima Bold |
| `Optima-Italic` | Optima Italic |
| `TrebuchetMS` | Trebuchet MS |
| `TrebuchetMS-Bold` | Trebuchet MS Bold |
| `TrebuchetMS-Italic` | Trebuchet MS Italic |
| `Verdana` | Verdana |
| `Verdana-Bold` | Verdana Bold |
| `Verdana-Italic` | Verdana Italic |
| `ArialMT` | Arial |
| `Arial-BoldMT` | Arial Bold |
| `Arial-ItalicMT` | Arial Italic |
| `Arial-BoldItalicMT` | Arial Bold Italic |

### Monospace
| PostScript-naam | Weergavenaam |
|---|---|
| `Menlo-Regular` | Menlo |
| `Menlo-Bold` | Menlo Bold |
| `Menlo-Italic` | Menlo Italic |
| `CourierNewPSMT` | Courier New |
| `CourierNewPS-BoldMT` | Courier New Bold |
| `CourierNewPS-ItalicMT` | Courier New Italic |
| `Courier` | Courier |
| `Courier-Bold` | Courier Bold |

### Kalligrafie / decoratief
| PostScript-naam | Weergavenaam |
|---|---|
| `SnellRoundhand` | Snell Roundhand |
| `SnellRoundhand-Bold` | Snell Roundhand Bold |
| `Zapfino` | Zapfino |
| `PartyLetPlain` | Party LET |
| `ChalkboardSE-Regular` | Chalkboard SE |
| `ChalkboardSE-Bold` | Chalkboard SE Bold |
| `MarkerFelt-Thin` | Marker Felt Thin |
| `MarkerFelt-Wide` | Marker Felt Wide |
| `Papyrus` | Papyrus |
| `Noteworthy-Light` | Noteworthy Light |
| `Noteworthy-Bold` | Noteworthy Bold |

### Kortschrift
| PostScript-naam | Weergavenaam |
|---|---|
| `BradleyHandITCTT-Bold` | Bradley Hand |

> **Tip:** voor de meeste lees-templates zijn `Georgia` (serif) of `Avenir` (sans-serif) als `font_body` een goede keuze. Decoratieve fonts werken beter als `font_heading`.
