<div align="center">

<table>
<tr>
<td><img src="https://atelier.atechnologie.fr/wp-content/uploads/2026/09/mesure-1.webp" alt="MoreArrows" width="140" /></td>
<td align="left">
<h1 style="margin:0">MoreArrows</h1>
<p style="margin:0.25em 0 0"><strong>Pfeile in Notizen · Live Preview · Obsidian</strong><br/>Plugin · Markdown-Syntax · leader-line</p>
</td>
</tr>
</table>

<a href="https://atelier.atechnologie.fr/" title="l'Atelier – Verein für Buchherstellung und Forschungswerkzeuge"><img src="https://atelier.atechnologie.fr/wp-content/uploads/2026/11/logoasso.webp" alt="l'Atelier" width="200" /></a>  
<sub>Entwickelt von <a href="https://atelier.atechnologie.fr/">l'Atelier</a> — Buchherstellung und Forschungswerkzeuge (EHESS)</sub>

<p>
🇫🇷 <a href="README.md">Français</a> ·
🇬🇧 <a href="README.en.md">English</a> ·
🇩🇪 <a href="README.de.md"><b>Deutsch</b></a> ·
🇪🇸 <a href="README.es.md">Español</a>
</p>

<p>
<a href="https://atelier.atechnologie.fr/"><img src="https://img.shields.io/badge/🌐_l'Atelier-atelier.atechnologie.fr-2d5016?style=for-the-badge" alt="Website l'Atelier" /></a>
<a href="https://github.com/Atelier-Recherche/more-arrows"><img src="https://img.shields.io/badge/📦_Repository-GitHub-181717?style=for-the-badge&logo=github" alt="GitHub-Repository" /></a>
<a href="https://obsidian.md/plugins?search=BRAT#"><img src="https://img.shields.io/badge/⬇️_Obsidian_Plugin-BRAT-7c3aed?style=for-the-badge&logo=obsidian&logoColor=white" alt="Plugin über BRAT installieren" /></a>
</p>

</div>

---

## 📸 Vorschau

| Live Preview | Pfeile |
| :---: | :---: |
| <img src="readme-media/screen1.jpg" alt="MoreArrows in Live Preview" width="400" /> | <img src="readme-media/screen2.jpg" alt="Pfeile in einer Notiz" width="400" /> |

---

## 📖 Über das Projekt

Plugin für [Obsidian](https://obsidian.md/), mit dem Sie Pfeile in Ihren Notizen zeichnen können, als würden Sie verschiedene Textstellen von Hand verbinden.

**Funktioniert nur im Live-Preview-Modus.**

---

## ⬇️ Obsidian-Plugin (BRAT)

1. 🔌 **BRAT** installieren: [Obsidian — BRAT](https://obsidian.md/plugins?search=BRAT#)
2. ➕ Dieses Repository mit *« Add Beta plugin »* hinzufügen:  
   `https://github.com/Atelier-Recherche/more-arrows`

> **Plugin-ID**: `more-arrows`

> 💡 Unsere Plugins können auf Katalogfreigabe warten; BRAT ermöglicht Tests schon jetzt. Siehe auch 🌐 [l’Atelier](https://atelier.atechnologie.fr/).

---

## ✏️ Verwendung

### Pfeile zeichnen

Tippen Sie `{pfeil-id|farbe}`, um den **Anfang** eines Pfeils zu markieren, z. B. `{mein-pfeil|#1e90ff}`.

Tippen Sie dann woanders `{pfeil-id}`, um das **Ende** zu markieren: hier `{mein-pfeil}`.

Ein Pfeil wird vom Anfang zum Ende entlang des Rands gezeichnet.

```
Lorem ipsum dolor sit amet, consectetur {mein-pfeil|#1e90ff} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus augue. {mein-pfeil} Aliquam non lectus varius.
```

<img width="450" src="./screenshots/drawing-arrows.png" alt="Pfeile zeichnen" />

---

### Diagonale Pfeile

Für einen **diagonalen** Pfeil fügen Sie am Anfang `|diagonal` hinzu, z. B. `{mein-pfeil2|#ff5555|diagonal}`.

```
Lorem ipsum dolor sit amet, consectetur {mein-pfeil2|#ff5555|diagonal} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus {mein-pfeil2} augue. Aliquam non lectus varius.
```

<img width="450" src="./screenshots/diagonal.png" alt="Diagonale Pfeile" />

---

### Gerade Pfeile (straight)

Für eine **gerade** Linie zwischen Anfang und Ende (ohne dem Rand zu folgen) fügen Sie am Anfang `|straight` hinzu, z. B. `{mein-pfeil3|#1e90ff|straight}`.

```
Lorem ipsum dolor sit amet, consectetur {mein-pfeil3|#1e90ff|straight} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus {mein-pfeil3} augue. Aliquam non lectus varius.
```

---

### Mehrere Pfeile

Verwenden Sie **unterschiedliche Kennungen** für mehrere Pfeile, z. B. `{anderer-pfeil|orange}`:

```
Lorem ipsum dolor sit amet, {anderer-pfeil|orange} consectetur adipiscing elit. {mein-pfeil3}

Morbi et lacus suscipit, dignissim purus at, dapibus augue. Aliquam non lectus varius, tempus tortor ac, commodo purus. {anderer-pfeil}
```

<img width="450" src="./screenshots/more-arrows.png" alt="Mehrere Pfeile" />

---

### Multi-Pfeile

Derselbe Anfang kann **mehrere Enden** haben: zu jedem passenden `{id}` wird ein Pfeil gezeichnet.

```
Lorem ipsum dolor sit amet, {multi|limegreen} consectetur adipiscing elit.

Morbi et lacus suscipit, dignissim purus at, dapibus augue. Aliquam non lectus varius, tempus tortor ac, commodo purus. {multi}

Pellentesque posuere ex non facilisis bibendum. Integer iaculis dolor dignissim, ultrices ligula eu, malesuada metus. {multi}
```

<img width="450" src="./screenshots/multi-arrows.png" alt="Multi-Pfeile" />

---

### Randpfeile: horizontale Position

Für **margin**-Pfeile stellen Sie die horizontale Position mit `|x-pos` ein, wobei `x-pos` eine Ganzzahl zwischen **0** und **30** ist, z. B. `{mein-pfeil|blue|10}`.

```
Lorem ipsum dolor sit amet, {erste|dodgerblue|20} consectetur adipiscing elit. {zweite|limegreen|10}

Morbi et lacus suscipit, dignissim purus at, dapibus augue. {dritte|tomato} Aliquam non lectus varius, tempus tortor ac, commodo purus.

Pellentesque posuere {dritte} ex non facilisis bibendum. {zweite}
Integer iaculis dolor dignissim, ultrices ligula eu, malesuada metus. {erste}
```

<img width="450" src="./screenshots/adjusting-margin-arrows.png" alt="Horizontale Position von Randpfeilen" />

---

### Rahmen (box) und verknüpfter Text

Sie können ein Textstück mit einem **Rahmen** umgeben und den Pfeil von der **unteren Mitte** des Kastens zur **oberen Mitte** des Ziels führen (wie bei anderen Pfeiltypen).

- **Anfang mit box**: Untertyp `box` zum Pfeiltyp hinzufügen, z. B. `straight,box`, `diagonal,box`, oder nur `box` für einen Randpfeil.
- **Schließen**: `{/id}` beendet den Rahmen; der gesamte Text **zwischen** dem Ende des Öffnungs-Tags und diesem Marker liegt in der Box.
- **Ende mit box**: damit die **Ankunft** ebenfalls ein Rahmen ist, `{id|box}` als Pfeilende verwenden (ohne alle Anfangsdetails zu wiederholen), dann `{/id}` zum Schließen.

**Zwei Farben** (kommagetrennt): die **erste** färbt den Pfeil, die **zweite** den Box-Rand. Beispiel: `{id|#1e90ff40, #fff|straight,box}`.

Gibt das Ende `{id|box}` keine Randfarbe an, **übernimmt es die Randfarbe des Anfangs** (die zweite Farbe, wenn zwei angegeben wurden), sonst die Pfeilfarbe.

Minimales Beispiel (zwei Boxen mit derselben ID verbunden):

```
Testphrase {arrow3|#1e90ff40, #fff|straight,box} Text zum Einrahmen {/arrow3} Test

Testphrase {arrow3|box} Text zum Einrahmen {/arrow3} Test
```

`{/id}`-Tags werden in der Anzeige ausgeblendet (außer wenn der Cursor darauf liegt). Die ● an den Enden werden ausgeblendet, wenn die ID im Box-Modus ist.

---

### Pfeilspitzen

- Spitze am **Anfang** hinzufügen: `|arrow` am Start-Tag.
- Spitze am **Ende** entfernen: `{id|no-arrow}` am End-Tag.

```
Lorem ipsum dolor sit amet, {double|#3d6eff|arrow} consectetur adipiscing elit.

Morbi et lacus suscipit, {double} dignissim purus at, dapibus augue. {linie|#9d6efa} Aliquam non lectus varius, tempus tortor ac, commodo purus.

Pellentesque posuere ex non facilisis bibendum. {linie|no-arrow}
```

<img width="450" src="./screenshots/arrowheads.png" alt="Pfeilspitzen" />

---

### Navigation zwischen Pfeilen

Wenn der Cursor **außerhalb** der Syntax `{…}` steht, werden Kennungen als kleiner Kreis ● angezeigt.

Ein Klick auf ● scrollt den Editor zur **nächsten passenden Kennung** — nützlich in langen Notizen.

---

## 📘 Vollständige Syntax

**Pfeilanfang** — `{id|farbe|opazität|typ|x-position|spitze}` wobei:

| Feld | Beschreibung |
|--------|-------------|
| `id` | Eindeutige Zeichenkette zum Verbinden von Anfang und Ende(n). |
| `farbe` | CSS-Farbe (`red`, `#ff0000` usw.). Für Boxen: zwei kommagetrennte Farben: **Pfeil**, dann **Rand** (z. B. `#1e90ff, #ffffff`). |
| `opazität` (optional) | Zahl zwischen 0 und 1 (z. B. `0.6`). Standard: 1. |
| `typ` (optional) | `diagonal`, `margin` oder `straight`. Kombinierbar mit `box`: `straight,box`, `diagonal,box` oder nur `box` für einen Randpfeil mit Box. Standard: `margin`. |
| `x-position` (optional) | Ganzzahl 0–30 für die horizontale Position von **margin**-Pfeilen. Standard: 0. |
| `spitze` (optional) | `no-arrow` oder `arrow` am **Anfang**, um eine Spitze am Ursprung hinzuzufügen. Standard: `no-arrow`. |

**Pfeilende**:

- `{id}` — klassisches Ende.
- `{id|no-arrow}` — ohne Spitze an der Ankunft.
- `{id|box}` — Ende, das eine **Box** öffnet; Text bis `{/id}` ist eingerahmt.

**Box schließen**: `{/id}` — schließt den von einem Anfang oder Ende im `box`-Modus geöffneten Rahmen.

Ein Pfeil wird vom/von den Anfang(en) zu **allen** Enden mit derselben ID gezeichnet.

---

## ⚠️ Einschränkungen

- Nur **Live Preview** (nicht auf dieselbe Weise im reinen Quellmodus).

---

## 🤝 Mitwirken

Beiträge und PRs sind willkommen.

---

## 📜 Herkunft

Dieses Repository wird von [l'Atelier](https://atelier.atechnologie.fr/) gepflegt und basiert auf dem Original-Plugin [Arrows](https://github.com/artisticat1/arrows) von **artisticat1** (MIT-Lizenz). Der Originalautor wird als Mitwirkender des Upstream-Projekts genannt.

> **Obsidian-Katalog**: Bei Einreichung in den Community-Katalog kann die Fork-Richtlinie von Obsidian die schriftliche Zustimmung des Originalautors verlangen oder den Nachweis, dass er seit 6 Monaten unerreichbar und inaktiv ist.

---

## 📦 Obsidian-Katalog

| Element | Detail |
| --- | --- |
| **Plugin-ID** | `more-arrows` |
| **Repository** | [github.com/Atelier-Recherche/more-arrows](https://github.com/Atelier-Recherche/more-arrows) |
| **Lizenz** | MIT — [LICENSE](LICENSE) |
| **Netzwerk** | nein |
| **Release** | `.\Release-Plugin.ps1` |

---

## 🙏 Danksagungen

Das Projekt nutzt die Bibliothek [leader-line](https://anseki.github.io/leader-line/) für die Pfeildarstellung.

---

## 🔗 Ressourcen

| | |
| --- | --- |
| 🌐 **l'Atelier** | [atelier.atechnologie.fr](https://atelier.atechnologie.fr/) |
| 📦 **Repository** | [github.com/Atelier-Recherche/more-arrows](https://github.com/Atelier-Recherche/more-arrows) |
| 🔌 **Obsidian** | [obsidian.md](https://obsidian.md/) |

---

<div align="center">

<sub><a href="README.md">🇫🇷 Français</a> · <a href="README.en.md">🇬🇧 English</a> · 🇩🇪 Deutsch · <a href="README.es.md">🇪🇸 Español</a> · MoreArrows — <a href="https://atelier.atechnologie.fr/">l'Atelier</a></sub>

</div>
