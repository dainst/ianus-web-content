# ianus-web-content

Dieses Repository enthält die Inhalte für https://ianus-fdz.de.

## Lehrangebote einreichen

Interessierte Dozent:innen können neue [Lehrangebote](https://ianus-fdz.de/lehrangebote) über Pull Requests hier auf Github einreichen, siehe [Wiki](https://github.com/dainst/ianus-web-content/wiki/Erstellung-von-Lehrangeboten).

## Neue Unterseiten hinzufügen

Sollen neben den bestehenden Seiten neue Unterseiten hinzugefügt werden, ist dies über Templates möglich.

### Template Struktur
```
---
title: Browser-Titel des Inhalts
sorting: Sortierung im Inhaltsverzeichnis, "it010203" entspräche 1.2.3
webtoc: Optional, ob für das gesamte Markdown-Dokument ein weiteres TOC angezeigt werden soll. Sinnvoll bei großen Dokumenten [true/false] 
authors:
  - max.mustermann (wird aus content/autoren geladen)
downloads:
  - example.pdf (wird aus content/dateien geladen)
---
````


### Beispiele

in /it-empfehlungen liegt eine Datei _template.md. Diese kann als Vorlage dienen.


