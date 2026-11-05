<div align="center">

<table>
<tr>
<td><img src="readme-media/logo_arrows.png" alt="MoreArrows" width="140" /></td>
<td align="left">
<h1 style="margin:0">MoreArrows</h1>
<p style="margin:0.25em 0 0"><strong>Flechas en notas · Live Preview · Obsidian</strong><br/>Plugin · sintaxis Markdown · leader-line</p>
</td>
</tr>
</table>

<a href="https://atelier.atechnologie.fr/" title="l'Atelier – asociación de fabricación de libros y herramientas de investigación"><img src="readme-media/logoasso.jpg" alt="l'Atelier" width="200" /></a>  
<sub>Desarrollado por <a href="https://atelier.atechnologie.fr/">l'Atelier</a> — fabricación de libros y herramientas de investigación (EHESS)</sub>

<p>
🇫🇷 <a href="README.md">Français</a> ·
🇬🇧 <a href="README.en.md">English</a> ·
🇩🇪 <a href="README.de.md">Deutsch</a> ·
🇪🇸 <a href="README.es.md"><b>Español</b></a>
</p>

<p>
<a href="https://atelier.atechnologie.fr/"><img src="https://img.shields.io/badge/🌐_l'Atelier-atelier.atechnologie.fr-2d5016?style=for-the-badge" alt="Sitio l'Atelier" /></a>
<a href="https://github.com/Atelier-Recherche/more-arrows"><img src="https://img.shields.io/badge/📦_Repositorio-GitHub-181717?style=for-the-badge&logo=github" alt="Repositorio GitHub" /></a>
<a href="https://obsidian.md/plugins?search=BRAT#"><img src="https://img.shields.io/badge/⬇️_Plugin_Obsidian-BRAT-7c3aed?style=for-the-badge&logo=obsidian&logoColor=white" alt="Instalar plugin vía BRAT" /></a>
</p>

</div>

---

## 📸 Vista previa

| Live Preview | Flechas |
| :---: | :---: |
| <img src="readme-media/screen1.jpg" alt="MoreArrows en Live Preview" width="400" /> | <img src="readme-media/screen2.jpg" alt="Flechas en una nota" width="400" /> |

---

## 📖 Acerca del proyecto

Plugin para [Obsidian](https://obsidian.md/) que permite dibujar flechas en las notas, como si se unieran a mano distintas partes del texto.

**Funciona únicamente en modo Live Preview.**

---

## ⬇️ Plugin Obsidian (BRAT)

1. 🔌 Instalar **BRAT**: [Obsidian — BRAT](https://obsidian.md/plugins?search=BRAT#)
2. ➕ Añadir este repositorio con *« Add Beta plugin »*:  
   `https://github.com/Atelier-Recherche/more-arrows`

> **ID del plugin**: `more-arrows`

> 💡 Nuestros plugins pueden estar pendientes de validación en el catálogo Obsidian; BRAT permite probarlos ya. Véase también 🌐 [l’Atelier](https://atelier.atechnologie.fr/).

---

## ✏️ Uso

### Dibujar flechas

Escriba `{id-flecha|color}` para marcar el **inicio** de una flecha, p. ej. `{mi-flecha|#1e90ff}`.

Luego escriba `{id-flecha}` en otro lugar para marcar el **fin**: aquí `{mi-flecha}`.

Se traza una flecha del inicio al fin, a lo largo del margen.

```
Lorem ipsum dolor sit amet, consectetur {mi-flecha|#1e90ff} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus augue. {mi-flecha} Aliquam non lectus varius.
```

<img width="450" src="./screenshots/drawing-arrows.png" alt="Dibujar flechas" />

---

### Flechas diagonales

Para una flecha **diagonal**, añada `|diagonal` al inicio, p. ej. `{mi-flecha2|#ff5555|diagonal}`.

```
Lorem ipsum dolor sit amet, consectetur {mi-flecha2|#ff5555|diagonal} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus {mi-flecha2} augue. Aliquam non lectus varius.
```

<img width="450" src="./screenshots/diagonal.png" alt="Flechas diagonales" />

---

### Flechas rectas (straight)

Para una línea **recta** entre inicio y fin (sin seguir el margen), añada `|straight` al inicio, p. ej. `{mi-flecha3|#1e90ff|straight}`.

```
Lorem ipsum dolor sit amet, consectetur {mi-flecha3|#1e90ff|straight} adipiscing elit. Tempus tortor ac, commodo purus.

Morbi et lacus suscipit, dignissim purus at, dapibus {mi-flecha3} augue. Aliquam non lectus varius.
```

---

### Varias flechas

Use **identificadores distintos** para varias flechas, p. ej. `{otra-flecha|orange}`:

```
Lorem ipsum dolor sit amet, {otra-flecha|orange} consectetur adipiscing elit. {mi-flecha3}

Morbi et lacus suscipit, dignissim purus at, dapibus augue. Aliquam non lectus varius, tempus tortor ac, commodo purus. {otra-flecha}
```

<img width="450" src="./screenshots/more-arrows.png" alt="Varias flechas" />

---

### Multi-flechas

Un mismo inicio puede tener **varios fines**: se dibuja una flecha hacia cada `{id}` correspondiente.

```
Lorem ipsum dolor sit amet, {multi|limegreen} consectetur adipiscing elit.

Morbi et lacus suscipit, dignissim purus at, dapibus augue. Aliquam non lectus varius, tempus tortor ac, commodo purus. {multi}

Pellentesque posuere ex non facilisis bibendum. Integer iaculis dolor dignissim, ultrices ligula eu, malesuada metus. {multi}
```

<img width="450" src="./screenshots/multi-arrows.png" alt="Multi-flechas" />

---

### Flechas de margen: posición horizontal

Para las flechas **margin**, ajuste la posición horizontal con `|x-pos` donde `x-pos` es un entero entre **0** y **30**, p. ej. `{mi-flecha|blue|10}`.

```
Lorem ipsum dolor sit amet, {primera|dodgerblue|20} consectetur adipiscing elit. {segunda|limegreen|10}

Morbi et lacus suscipit, dignissim purus at, dapibus augue. {tercera|tomato} Aliquam non lectus varius, tempus tortor ac, commodo purus.

Pellentesque posuere {tercera} ex non facilisis bibendum. {segunda}
Integer iaculis dolor dignissim, ultrices ligula eu, malesuada metus. {primera}
```

<img width="450" src="./screenshots/adjusting-margin-arrows.png" alt="Posición horizontal de flechas de margen" />

---

### Recuadros (box) y texto enlazado

Puede rodear un fragmento de texto con un **borde** y hacer partir la flecha del **centro inferior** del recuadro hacia el **centro superior** del destino (como en los demás tipos).

- **Inicio con box**: añada el subtipo `box` al tipo de flecha, p. ej. `straight,box`, `diagonal,box`, o solo `box` para una flecha de margen.
- **Cierre**: `{/id}` termina el recuadro; todo el texto **entre** el final de la etiqueta de apertura y este marcador está en la box.
- **Fin con box**: para que la **llegada** también sea un recuadro, use `{id|box}` como fin de flecha (sin repetir todo el detalle del inicio), luego `{/id}` para cerrar.

**Dos colores** (separados por coma): el **primero** colorea la flecha, el **segundo** el borde de las box. Ejemplo: `{id|#1e90ff40, #fff|straight,box}`.

Si el fin `{id|box}` no precisa color de borde, **retoma el color de borde del inicio** (el segundo color si dio dos), si no el color de la flecha.

Ejemplo mínimo (dos box unidas con el mismo id):

```
frase de prueba {arrow3|#1e90ff40, #fff|straight,box} texto a enmarcar {/arrow3} de prueba

frase de prueba {arrow3|box} texto a enmarcar {/arrow3} de prueba
```

Las etiquetas `{/id}` se ocultan en la visualización (salvo cuando el cursor está encima para editar). Los puntos ● de los extremos se ocultan cuando el id está en modo box.

---

### Puntas de flecha

- Añada una punta al **inicio**: `|arrow` en la etiqueta de inicio.
- Quite la punta al **fin**: `{id|no-arrow}` en la etiqueta de fin.

```
Lorem ipsum dolor sit amet, {double|#3d6eff|arrow} consectetur adipiscing elit.

Morbi et lacus suscipit, {double} dignissim purus at, dapibus augue. {linea|#9d6efa} Aliquam non lectus varius, tempus tortor ac, commodo purus.

Pellentesque posuere ex non facilisis bibendum. {linea|no-arrow}
```

<img width="450" src="./screenshots/arrowheads.png" alt="Puntas de flecha" />

---

### Navegación entre flechas

Cuando el cursor está **fuera** de la sintaxis `{…}`, los identificadores se muestran como un pequeño círculo ● para un aspecto más limpio.

Un clic en ● desplaza el editor al **siguiente identificador** correspondiente, útil en notas largas.

---

## 📘 Sintaxis completa

**Inicio de flecha** — `{id|color|opacidad|tipo|posición-x|punta}` donde:

| Campo | Descripción |
|--------|-------------|
| `id` | Cadena única para enlazar inicio y fin(es). |
| `color` | Color CSS (`red`, `#ff0000`, etc.). Para box: dos colores separados por coma: **flecha**, luego **borde** (ej. `#1e90ff, #ffffff`). |
| `opacidad` (opcional) | Número entre 0 y 1 (ej. `0.6`). Por defecto: 1. |
| `tipo` (opcional) | `diagonal`, `margin` o `straight`. Combinable con `box`: `straight,box`, `diagonal,box`, o solo `box` para flecha de margen con box. Por defecto: `margin`. |
| `posición-x` (opcional) | Entero 0–30 para la posición horizontal de flechas **margin**. Por defecto: 0. |
| `punta` (opcional) | `no-arrow` o `arrow` en el **inicio** para añadir punta en el origen. Por defecto: `no-arrow`. |

**Fin de flecha**:

- `{id}` — fin clásico.
- `{id|no-arrow}` — sin punta a la llegada.
- `{id|box}` — fin que abre una **box**; el texto hasta `{/id}` queda enmarcado.

**Cierre de box**: `{/id}` — cierra el recuadro abierto por un inicio o un fin en modo `box`.

Se traza una flecha desde el/los inicio(s) hacia **todos** los fines con el mismo id.

---

## ⚠️ Limitaciones

- Solo **Live Preview** (no del mismo modo en vista de código fuente sola).

---

## 🤝 Contribución

Las contribuciones y los PR son bienvenidos.

---

## 📜 Procedencia

Este repositorio lo mantiene [l'Atelier](https://atelier.atechnologie.fr/) y se basa en el plugin original [Arrows](https://github.com/artisticat1/arrows) de **artisticat1** (licencia MIT). El autor original figura como colaborador del proyecto de origen.

> **Catálogo Obsidian**: si envía este plugin al catálogo comunitario, la política de forks de Obsidian puede exigir el acuerdo escrito del autor original o la prueba de que es inalcanzable e inactivo desde hace 6 meses.

---

## 📦 Catálogo Obsidian

| Elemento | Detalle |
| --- | --- |
| **ID plugin** | `more-arrows` |
| **Repositorio** | [github.com/Atelier-Recherche/more-arrows](https://github.com/Atelier-Recherche/more-arrows) |
| **Licencia** | MIT — [LICENSE](LICENSE) |
| **Red** | no |
| **Release** | `.\Release-Plugin.ps1` |

---

## 🙏 Agradecimientos

El proyecto utiliza la biblioteca [leader-line](https://anseki.github.io/leader-line/) para el renderizado de las flechas.

---

## 🔗 Recursos

| | |
| --- | --- |
| 🌐 **l'Atelier** | [atelier.atechnologie.fr](https://atelier.atechnologie.fr/) |
| 📦 **Repositorio** | [github.com/Atelier-Recherche/more-arrows](https://github.com/Atelier-Recherche/more-arrows) |
| 🔌 **Obsidian** | [obsidian.md](https://obsidian.md/) |

---

<div align="center">

<sub><a href="README.md">🇫🇷 Français</a> · <a href="README.en.md">🇬🇧 English</a> · <a href="README.de.md">🇩🇪 Deutsch</a> · 🇪🇸 Español · MoreArrows — <a href="https://atelier.atechnologie.fr/">l'Atelier</a></sub>

</div>
