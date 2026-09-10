# Notion for Zed

Notion's own colour palette, as a light and dark theme for [Zed](https://zed.dev).

Not a port of anyone's VS Code theme — the colours are taken from Notion's published
palette (its ten text colours, ten icon colours, and its interface surfaces) and mapped
onto Zed's syntax slots.

| | Light | Dark |
| --- | --- | --- |
| Editor | `#FFFFFF` | `#191919` |
| Sidebar, tabs, status bar | `#F7F6F3` | `#202020` |
| Text | `#24221D` | `#D4D4D4` |

## Install

Zed → `cmd-shift-x` → search **Notion**.

Then pick it with `cmd-k cmd-t`, or follow your system light/dark setting:

```json
"theme": {
  "mode": "system",
  "light": "Notion Light",
  "dark": "Notion Dark"
}
```

## Readable by default

Notion's palette is built for documents, where an accent colour appears once in a
paragraph. Code is denser, and several of those colours sit right at or below the
WCAG AA floor (4.5:1) when used as syntax colours.

So every colour here is lifted in lightness — hue and saturation untouched — until it
clears the floor: **5.4:1 for syntax, 4.6:1 for comments and hints**. It still reads as
Notion; it just doesn't wash out at small sizes.

| | worst syntax contrast | colours below AA |
| --- | --- | --- |
| Notion Light | 4.60:1 | 0 of 102 |
| Notion Dark | 4.64:1 | 0 of 102 |

Both themes define all 176 of Zed's style keys and all 102 syntax keys, so nothing
falls back to Zed's defaults.

## Credits

Colour values sourced from Notion's published palette, catalogued by
[Matthias Frank](https://matthiasfrank.de/en/notion-colors/).

Not affiliated with or endorsed by Notion Labs, Inc.

## Licence

MIT — see [LICENSE](LICENSE).
