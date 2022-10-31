---
title: Versionskontrolle
sorting: it020304
authors:
  - trognitz.martina
---

# Versionskontrolle

Wenn unterschiedliche Personen an einer Datei arbeiten, ist es wichtig, die verschiedenen Änderungen und Entwicklungsstadien zu verfolgen und zu kennzeichnen. Nur so kann vermieden werden, dass an der falschen Dateiversion gearbeitet wird oder diese gar gelöscht wird. Dateiversionen, die nicht mehr benötigt werden, sollten bei Bedarf gelöscht werden.

Es gibt mehrere Strategien, um die Versionskontrolle durchzuführen, die im Folgenden erläutert werden.

## Angabe im Dateinamen

Eine einfache und übersichtliche Methode ist, die Versionsangabe in den Dateinamen zu integrieren. Das kann beispielsweise mit einer Datumsangabe oder Ziffern erfolgen. Durch ein vorangestelltes **v** werden die Ziffern als eine Versionsnummer gekennzeichnet, wie zum Beispiel **v001**. Führende Nullen stellen sicher, dass die Versionsnummern einheitlich und leichter lesbar sind und richtig sortiert werden.

Eine Kennzeichnung von Versionen durch Worte wie _"neu"_, _"neuer"_ und _"alt"_ ist unbedingt zu vermeiden. Eine Ausnahme können endgültige Dateiversionen bilden, die der Übersicht halber etwa durch _FINAL_ am Ende gekennzeichnet werden können. Es darf aber nur eine Datei mit dieser Kennzeichnung in einem Ordner und einem bestimmten Format vorliegen. Eine endgültige Version, die zum Beispiel sowohl als _docx_ als auch als _pdf_ vorliegt, ist also erlaubt.

## Angabe in der Datei

Angaben zum Erstellungsdatum und den verschiedenen Versionen und deren Änderungen können im Header der Datei oder in standardisierten Kopfzeilen in der Datei selbst angegeben werden. Bei Textdokumenten bietet sich die Möglichkeit einen Innentitel mit einer Versionshistorie zu verwenden. Ein Beispiel für solch einen Innentitel findet sich am Anfang der PDF-Version dieser Empfehlungen.

## Änderungsprotokoll

Statt einzelne Dateiversionen abzuspeichern, kann auch ein Änderungsprotokoll geführt werden. Dabei werden die einzelnen Änderungen in einer einfachen Textdatei protokolliert, die zusammen mit der eigentlichen Datei abgelegt wird. Im Englischen wird dafür der Begriff _ChangeLog_ verwendet.

## Software

Die bisher beschriebenen Methoden sind hauptsächlich manuell anzuwendende Vorgänge. Es gibt jedoch auch Software zur Versionsverwaltung. Deren Einsatz lohnt sich vor allem in großen Projekten, die zentral auf einem Server abgelegt werden. Versionsverwaltungssoftware kann aus den Dateiänderungen automatisch _ChangeLogs_ erstellen. Die am weitesten verbreiteten Systeme zur Versionsverwaltung sind [Subversion (SVN)](http://subversion.apache.org/) und [Git](https://git-scm.com/). Primär wurden sie für die Bedürfnisse von Softwareentwicklern konzipiert, jedoch eignen sie sich auch für allgemeinere Aufgaben. Für die einzelnen Computerarbeitsplätze werden Clients wie [TortoiseSVN](https://tortoisesvn.net/) für SVN oder [GitHub](https://git-scm.com/downloads/guis) für Git benötigt.

Eine einfache Versionsverwaltung für Dateien bieten [ownCloud](https://owncloud.org/), [Dropbox](https://www.dropbox.com/) und [Google Drive](https://drive.google.com/drive/) wobei die Menge der unterschiedlichen gespeicherten Versionen abhängig von dem persönlichen Speicherplatz ist.

- Git: [https://git-scm.com/](https://git-scm.com/)
- Clients für Git: [http://git-scm.com/downloads/guis](http://git-scm.com/downloads/guis)
- Subversion (SVN): [http://subversion.apache.org/](http://subversion.apache.org/)
- TortoiseSVN: [https://tortoisesvn.net/](https://tortoisesvn.net/)
- ownCloud: [https://owncloud.org/](https://owncloud.org/)
- Dropbox: [https://www.dropbox.com/](https://www.dropbox.com/)
- Google Drive: [https://drive.google.com/drive/](https://drive.google.com/drive/)
- Vergleich von Versionsverwaltungssystemen auf Wikipedia: [http://en.wikipedia.org/wiki/Comparison\_of\_revision\_control\_software](http://en.wikipedia.org/wiki/Comparison_of_revision_control_software)

