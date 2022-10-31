---
title: Browser-Titel des Inhalts
sorting: Sortierung im Inhaltsverzeichnis, "it010203" entspräche 1.2.3
webtoc: Optional, ob für das gesamte Markdown-Dokument ein weiteres TOC angezeigt werden soll. Sinnvoll bei großen Dokumenten [true/false]
draft: false
authors:
  - max.mustermann (wird aus content/autoren geladen)
downloads:
  - example (wird aus content/downloads geladen)
---

# Erste Überschrift

Eine detalierte Anleitung findet sich unter

- https://www.markdownguide.org/basic-syntax
- https://content.nuxtjs.org/writing/#markdown
- https://www.markdownguide.org/extended-syntax/

## Zweite Überschrift

![Alt-Text](./_media/example.png "Bild-Titel (mouseover)")

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut quis vehicula justo. Phasellus at lorem id nibh elementum ultrices vitae eu tellus. Sed lobortis purus turpis, quis rutrum nisl blandit eget. Nunc quis tortor sapien. Phasellus sed tellus imperdiet, porttitor felis ac, auctor leo. Pellentesque consequat erat erat. Sed eu lacus volutpat nisl faucibus tristique. Quisque pretium diam a semper bibendum. Integer in libero sed nibh fermentum rhoncus. Vivamus massa lectus, consectetur dignissim diam hendrerit, varius dignissim felis. Quisque sit amet elementum sapien. Sed eleifend odio et eros porttitor, at pellentesque turpis fringilla. In mollis feugiat dolor ut commodo. Nulla laoreet orci neque, quis aliquet ipsum tristique eu.

<!--more-->

Vivamus in purus enim. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Cras vehicula, erat vel iaculis blandit, ex est molestie lacus, nec molestie arcu nulla ut neque. Aliquam malesuada risus diam, ut elementum justo luctus at. Nullam aliquet finibus elit ut mattis. Etiam hendrerit lectus risus, sed porta dui porta at. Pellentesque quis nisi accumsan, pretium ligula id, vestibulum ex. Cras scelerisque est id tempor porttitor. Donec convallis feugiat massa, sed volutpat erat aliquet et. Vivamus porta fringilla finibus. Duis at rhoncus sapien.

> Zitat

Fußnoten funktionieren [^1] wie folgt, auch mehrzeilig[^big]:

[^1]: Fußnote.

[^big]: Absatz 1

    Absatz 2

Codeblöcke

```js{1,3-5}[server.js]
const http = require('http')
const bodyParser = require('body-parser')
```

Dateiformat-Tabelle

| Status️ | Ausgangsformat | Begründung |
|---------|----------------|------------|
| ✔️      | DNG            | text       |
| ❌️      | TIFF           | text       |
