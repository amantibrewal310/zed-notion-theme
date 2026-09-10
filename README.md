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

Until it lands in the extension registry: clone this repo, open `cmd-shift-x`, click
**Install Dev Extension** and pick the folder.

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
| Notion Light | 4.62:1 | 0 of 102 |
| Notion Dark | 4.64:1 | 0 of 102 |

Both themes define every style key Zed reads (189, as of September 2026) and all 102
syntax keys, so nothing falls back to Zed's defaults.

Two things are deliberately not Notion:

- **Selection** is Notion's own `#2383E2` at about 28%, the same tint Notion uses when
  you select text in a page, rather than a colour from the text palette.
- **Terminal cyan** is a teal. Notion has no cyan, and brown in its place makes `ls`
  output and shell prompts read as dirt. It is the only hue outside the palette.

## Credits

Colour values sourced from Notion's published palette, catalogued by
[Matthias Frank](https://matthiasfrank.de/en/notion-colors/).

Not affiliated with or endorsed by Notion Labs, Inc.

## Licence

MIT — see [LICENSE](LICENSE).
