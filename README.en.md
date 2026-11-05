<div align="center">

<table>
<tr>
<td><img src="readme-media/logo_arrows.png" alt="MoreArrows" width="140" /></td>
<td align="left">
<h1 style="margin:0">MoreArrows</h1>
<p style="margin:0.25em 0 0"><strong>Arrows in notes · Live Preview · Obsidian</strong><br/>Plugin · Markdown syntax · leader-line</p>
</td>
</tr>
</table>

<a href="https://atelier.atechnologie.fr/" title="l'Atelier – book fabrication and research tools association"><img src="readme-media/logoasso.jpg" alt="l'Atelier" width="200" /></a>  
<sub>Developed by <a href="https://atelier.atechnologie.fr/">l'Atelier</a> — book fabrication and research tools (EHESS)</sub>

<p>
🇫🇷 <a href="README.md">Français</a> ·
🇬🇧 <a href="README.en.md"><b>English</b></a> ·
🇩🇪 <a href="README.de.md">Deutsch</a> ·
🇪🇸 <a href="README.es.md">Español</a>
</p>

<p>
<a href="https://atelier.atechnologie.fr/"><img src="https://img.shields.io/badge/🌐_l'Atelier-atelier.atechnologie.fr-2d5016?style=for-the-badge" alt="l'Atelier website" /></a>
<a href="https://github.com/Atelier-Recherche/more-arrows"><img src="https://img.shields.io/badge/📦_Repository-GitHub-181717?style=for-the-badge&logo=github" alt="GitHub repository" /></a>
<a href="https://obsidian.md/plugins?search=BRAT#"><img src="https://img.shields.io/badge/⬇️_Obsidian_Plugin-BRAT-7c3aed?style=for-the-badge&logo=obsidian&logoColor=white" alt="Install plugin via BRAT" /></a>
</p>

</div>

---

## 📸 Preview

| Live Preview | MoreArrows |
| :---: | :---: |
| <img src="readme-media/screen1.jpg" alt="MoreArrows in Live Preview" width="400" /> | <img src="readme-media/screen2.jpg" alt="Arrows in a note" width="400" /> |

---

## 📖 About

Plugin for [Obsidian](https://obsidian.md/) that lets you draw arrows in your notes, as if you were manually connecting different parts of the text.

**Works only in Live Preview mode.**

---

## ⬇️ Obsidian plugin (BRAT)

1. 🔌 Install **BRAT**: [Obsidian — BRAT](https://obsidian.md/plugins?search=BRAT#)
2. ➕ Add this repository with *« Add Beta plugin »*:  
   `https://github.com/Atelier-Recherche/more-arrows`

> **Plugin ID**: `more-arrows`

> 💡 Our plugins may be pending Obsidian catalogue approval; BRAT lets you try them now. See also 🌐 [l’Atelier](https://atelier.atechnologie.fr/).

---

## ✏️ Usage

### Drawing arrows

Type `{arrow-id|color}` to mark the **start** of an arrow, e.g. `{my-arrow|#1e90ff}`.

Then type `{arrow-id}` elsewhere to mark the **end** of the arrow: here `{my-arrow}`.

An arrow is drawn from start to end along the margin.

```
Lorem ipsum dolor sit amet, consectetur {my-arrow|#1e90ff} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus augue. {my-arrow} Aliquam non lectus varius.
```

<img width="450" src="./screenshots/drawing-arrows.png" alt="Drawing arrows" />

---

### Diagonal arrows

For a **diagonal** arrow, add `|diagonal` at the start, e.g. `{my-arrow2|#ff5555|diagonal}`.

```
Lorem ipsum dolor sit amet, consectetur {my-arrow2|#ff5555|diagonal} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus {my-arrow2} augue. Aliquam non lectus varius.
```

<img width="450" src="./screenshots/diagonal.png" alt="Diagonal arrows" />

---

### Straight arrows

For a **straight** line between start and end (without following the margin), add `|straight` at the start, e.g. `{my-arrow3|#1e90ff|straight}`.

```
Lorem ipsum dolor sit amet, consectetur {my-arrow3|#1e90ff|straight} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus {my-arrow3} augue. Aliquam non lectus varius.
```

---

### Multiple arrows

Use **different identifiers** for several arrows, e.g. `{other-arrow|orange}`:

```
Lorem ipsum dolor sit amet, {other-arrow|orange} consectetur adipiscing elit. {my-arrow3}

Morbi et lacus suscipit, dignissim purus at, dapibus augue. Aliquam non lectus varius, tempus tortor ac, commodo purus. {other-arrow}
```

<img width="450" src="./screenshots/more-arrows.png" alt="Multiple arrows" />

---

### Multi-arrows

The same start can have **several ends**: an arrow is drawn to each matching `{id}`.

```
Lorem ipsum dolor sit amet, {multi|limegreen} consectetur adipiscing elit.

Morbi et lacus suscipit, dignissim purus at, dapibus augue. Aliquam non lectus varius, tempus tortor ac, commodo purus. {multi}

Pellentesque posuere ex non facilisis bibendum. Integer iaculis dolor dignissim, ultrices ligula eu, malesuada metus. {multi}
```

<img width="450" src="./screenshots/multi-arrows.png" alt="Multi-arrows" />

---

### Margin arrows: horizontal position

For **margin** arrows, set the horizontal position with `|x-pos` where `x-pos` is an integer between **0** and **30**, e.g. `{my-arrow|blue|10}`.

```
Lorem ipsum dolor sit amet, {first|dodgerblue|20} consectetur adipiscing elit. {second|limegreen|10}

Morbi et lacus suscipit, dignissim purus at, dapibus augue. {third|tomato} Aliquam non lectus varius, tempus tortor ac, commodo purus.

Pellentesque posuere {third} ex non facilisis bibendum. {second}
Integer iaculis dolor dignissim, ultrices ligula eu, malesuada metus. {first}
```

<img width="450" src="./screenshots/adjusting-margin-arrows.png" alt="Margin arrow horizontal position" />

---

### Boxes and linked text

You can wrap a piece of text in a **border** and start the arrow from the **bottom center** of the box toward the **top center** of the target (as with other arrow types).

- **Start with box**: add the `box` subtype to the arrow type, e.g. `straight,box`, `diagonal,box`, or just `box` for a margin arrow.
- **Close**: `{/id}` ends the box; all text **between** the end of the opening tag and this marker is inside the box.
- **End with box**: for the **arrival** to also be a box, use `{id|box}` as the arrow end (without repeating all start details), then `{/id}` to close.

**Two colors** (comma-separated): the **first** colors the arrow, the **second** the box border. Example: `{id|#1e90ff40, #fff|straight,box}`.

If the end `{id|box}` does not specify a border color, it **reuses the start border color** (the second color if you gave two), otherwise the arrow color.

Minimal example (two boxes linked with the same id):

```
test phrase {arrow3|#1e90ff40, #fff|straight,box} text to wrap {/arrow3} test

test phrase {arrow3|box} text to wrap {/arrow3} test
```

`{/id}` tags are hidden in display (except when the cursor is on them for editing). The ● endpoints are hidden when the id is in box mode.

---

### Arrowheads

- Add a head at the **start**: `|arrow` on the start tag.
- Remove the head at the **end**: `{id|no-arrow}` on the end tag.

```
Lorem ipsum dolor sit amet, {double|#3d6eff|arrow} consectetur adipiscing elit.

Morbi et lacus suscipit, {double} dignissim purus at, dapibus augue. {line|#9d6efa} Aliquam non lectus varius, tempus tortor ac, commodo purus.

Pellentesque posuere ex non facilisis bibendum. {line|no-arrow}
```

<img width="450" src="./screenshots/arrowheads.png" alt="Arrowheads" />

---

### Navigating between arrows

When the cursor is **outside** `{…}` syntax, identifiers are shown as a small ● circle for a cleaner look.

Clicking a ● scrolls the editor to the **next matching identifier**, useful in long notes.

---

## 📘 Full syntax

**Arrow start** — `{id|color|opacity|type|x-position|arrowhead}` where:

| Field | Description |
|--------|-------------|
| `id` | Unique string linking start and end(s). |
| `color` | CSS color (`red`, `#ff0000`, etc.). For boxes: two comma-separated colors: **arrow**, then **border** (e.g. `#1e90ff, #ffffff`). |
| `opacity` (optional) | Number between 0 and 1 (e.g. `0.6`). Default: 1. |
| `type` (optional) | `diagonal`, `margin`, or `straight`. Can combine with `box`: `straight,box`, `diagonal,box`, or `box` alone for a margin arrow with box. Default: `margin`. |
| `x-position` (optional) | Integer 0–30 for horizontal position of **margin** arrows. Default: 0. |
| `arrowhead` (optional) | `no-arrow` or `arrow` at the **start** to add a head at the origin. Default: `no-arrow`. |

**Arrow end**:

- `{id}` — classic end.
- `{id|no-arrow}` — no head at arrival.
- `{id|box}` — end that opens a **box**; text until `{/id}` is framed.

**Box close**: `{/id}` — closes the box opened by a start or end in `box` mode.

An arrow is drawn from the start(s) to **all** ends with the same id.

---

## ⚠️ Limitations

- **Live Preview** only (not the same way in source-only mode).

---

## 🤝 Contributing

Contributions and PRs are welcome.

---

## 📜 Provenance

This repository is maintained by [l'Atelier](https://atelier.atechnologie.fr/) and builds on the original [Arrows](https://github.com/artisticat1/arrows) plugin by **artisticat1** (MIT licence). The original author is credited as a contributor of the upstream project.

> **Obsidian catalogue**: if you submit this plugin to the community catalogue, Obsidian’s fork policy may require written consent from the original author, or proof they are unreachable and inactive for 6 months.

---

## 📦 Obsidian catalogue

| Item | Detail |
| --- | --- |
| **Plugin ID** | `more-arrows` |
| **Repository** | [github.com/Atelier-Recherche/more-arrows](https://github.com/Atelier-Recherche/more-arrows) |
| **Licence** | MIT — [LICENSE](LICENSE) |
| **Network** | no |
| **Release** | `.\Release-Plugin.ps1` |

---

## 🙏 Acknowledgements

The project uses the [leader-line](https://anseki.github.io/leader-line/) library for arrow rendering.

---

## 🔗 Resources

| | |
| --- | --- |
| 🌐 **l'Atelier** | [atelier.atechnologie.fr](https://atelier.atechnologie.fr/) |
| 📦 **Repository** | [github.com/Atelier-Recherche/more-arrows](https://github.com/Atelier-Recherche/more-arrows) |
| 🔌 **Obsidian** | [obsidian.md](https://obsidian.md/) |

---

<div align="center">

<sub><a href="README.md">🇫🇷 Français</a> · 🇬🇧 English · <a href="README.de.md">🇩🇪 Deutsch</a> · <a href="README.es.md">🇪🇸 Español</a> · MoreArrows — <a href="https://atelier.atechnologie.fr/">l'Atelier</a></sub>

</div>
