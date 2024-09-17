---
title: Dateibenennung
sorting: it020303
authors:
  - trognitz.martina
---

# Dateibenennung

Üblicherweise besteht der Dateiname einer Datei aus dem eigentlichen Namen und der durch einen Punkt getrennten Dateinamenserweiterung, die das Format der Datei angibt. Die Erweiterung wird in der Regel von dem Programm, mit dem die Datei gespeichert wurde, automatisch an den Dateinamen gehängt.

Ein Beispiel: _FDM-Empfehlungen.pdf_ gibt an, dass es sich um eine Datei mit dem Namen _"FDM-Empfehlungen"_ handelt, die in dem PDF-Format vorliegt.

Da die Erweiterung automatisch erzeugt wird, muss die Datei mit einem geeigneten Programm konvertiert werden, wenn man das Dateiformat ändern möchte. In dem Kapitel [Dateiformate](/it-empfehlungen/dateiformate/index) sind ausführliche Informationen darüber zu finden.

Im Folgenden geht es nur noch um den reinen Dateinamen, ohne die Dateinamenserweiterung.

## Erlaubte Zeichen

Moderne Betriebssysteme können mit Sonderzeichen umgehen, zu denen Umlaute und Leerzeichen gehören. Das war aber nicht immer so und kann auch heute noch zu Problemen führen. Webserver lesen zum Beispiel das Leerzeichen als die Zeichenfolge "%20" ein und da Umlaute nicht immer gleich kodiert werden, kann auch das zu Schwierigkeiten führen.

Für die Langzeitarchivierung sollten also nur die alphanumerischen Zeichen des englischen Alphabets, also a-z, A-Z und 0-9 verwendet werden. Zusätzlich kann der Bindestrich (**\-**) und bei Bedarf auch der Unterstrich (**\_**) verwendet werden.

## Zu vermeidende Zeichen

Es gibt eine ganze Reihe von Zeichen, die für besondere Aufgaben von Betriebssystemen verwendet werden. Der Punkt dient zur Trennung des Dateinamens von der Dateinamenserweiterung und der Schrägstrich dient in Windows um Ordnerebenen zu kennzeichnen.

Zu den Zeichen, die absolut nicht verwendet werden dürfen, gehören: **\\ / : \* ? " < > |**

Die Verwendung von allen weiteren Sonderzeichen ist zwar möglich, kann jedoch zu einem unerwarteten Verhalten des Systems führen. Daher wird von der Verwendung von Leerzeichen und Sonderzeichen, Bindestrich (**\-**) und Unterstrich (**\_**) ausgenommen, abgeraten.

## Groß- und Kleinschreibung

Die Groß- und Kleinschreibung in einem Dateinamen wird von unterschiedlichen Systemen verschieden gedeutet. In Windows beispielsweise kann, wenn es eine Datei mit dem Namen _"TestDatei"_ schon gibt, keine Datei mit dem Namen _"testdatei"_ angelegt werden. Andere Systeme könnten dies jedoch erlauben, was aber nicht bedeutet, dass man dies auch tun sollte.

Hat man sich in der Praxis einmal für eine Schreibweise entschieden, muss diese auch konsequent eingehalten werden und insbesondere bei der Arbeit auf verschiedenen Systemen darauf geachtet werden.

## Länge

Der Dateiname sollte so kurz wie möglich und so lang wie nötig sein. Eine aktuelle Obergrenze, die auf manchen Systemen nicht überschritten werden darf, sind 260 Zeichen, wobei dabei der gesamte Dateipfad gezählt wird. Kryptische oder untypische Kürzel sollten vermieden werden, da sie in der Regel in Vergessenheit geraten.
