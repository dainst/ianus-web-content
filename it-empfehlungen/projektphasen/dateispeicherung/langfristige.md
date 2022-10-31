---
title: Mittelfristige Sicherung
sorting: it020401
authors:
  - trognitz.martina
  - komp.rainer
  - förtsch.reinhard
---

# Mittelfristige Sicherung

Digitale Daten sind nur dann über einen längeren Zeitraum sicher, wenn sie mehr als einmal gespeichert werden. Es müssen also mindestens zwei Sicherungskopien auf physisch getrennten Speichermedien vorliegen, um etwa bei einem Hardwaredefekt auf eine alternative Sicherungskopie zugreifen zu können.

Die Sicherung von Daten auf unterschiedlichen Arbeitsgeräten wird erleichtert, wenn diese zunächst auf einem Datenträger gesammelt werden und dieser dann gesichert wird.

## Speichermedium

Welches Speichermedium gewählt wird, hängt vor allem von der Speichergröße der zu sichernden Dateien und der vorhandenen Infrastruktur ab. So eignen sich eine CD oder eine DVD nur für Daten bis maximal 900 MB bzw. 17 GB Speichervolumen. Für größere Datenmengen werden entsprechend größere Datenträger benötigt.

Steht ein lokaler oder institutioneller Server zur Verfügung, sollte dieser zur Datensicherung verwendet werden, da diese üblicherweise gewartet werden und meist selbst in eigene Sicherungsstrategien eingebunden sind. In Umgebungen mit Zugriff auf das Internet, kann eine Sicherung auch auf einen entfernten Server, beispielsweise in einem Rechenzentrum, erfolgen. In allen anderen Fällen können externe Festplatten verwendet werden. Von externen kommerziellen Diensten, wie beispielsweise Dropbox, ist für eine mittelfristige Sicherung abzuraten, weil es sich oft um ausländische Anbieter handelt, die nicht dem deutschen Recht unterliegen und den Nutzer im Unklaren darüber lassen, wie mit den Daten umgegangen wird.

Da die Speichermedien eine begrenzte Lebenszeit von etwa zehn Jahren haben, sollten die Sicherungen von Zeit zu Zeit auf neue Speichermedien migriert werden. Außerdem sollten sie zwischenzeitlich an verschiedenen Orten, mindestens in verschiedenen Räumen, gelagert werden, um etwa im Brandfall den Schaden zu begrenzen. Auch der Transport von Original- und Sicherungsdatenbeständen sollte getrennt durch unterschiedliche Personen erfolgen, um zu vermeiden, dass etwa durch Diebstahl alle Sicherungskopien auf einmal abhanden kommen.

Für das Kopieren der Daten auf ein Speichermedium gibt es verschiedene Methoden, wie die im Folgenden beschriebene Volldatensicherung, inkrementelle und differentielle Datensicherung.

## Volldatensicherung

Bei der Volldatensicherung werden die zu sichernden Dateien komplett und eins zu eins auf ein Speichermedium kopiert. Wird zum ersten Mal eine Sicherungskopie angelegt, so muss dies als Volldatensicherung geschehen. Dabei ist zu beachten, dass der Kopiervorgang viel Zeit in Anspruch nehmen kann, wobei dies auch über Nacht geschehen kann. Vor der Ausführung der Volldatensicherung muss geprüft werden, dass auf dem Speichermedium ausreichend freier Speicherplatz vorhanden ist.

Die Volldatensicherung ist die einzige Methode, die manuell, ohne weitere Hilfsprogramme, durchgeführt werden kann. Wird eine Volldatensicherung angelegt, sollten, beispielsweise in einer Textdatei, Informationen gespeichert werden, die Auskunft über den Zeitpunkt der Sicherung, den Ansprechpartner und den Umfang der Daten geben.

Liegt eine erste Volldatensicherung vor, können neue oder geänderte Daten mittels inkrementeller oder differentieller Datensicherung gesichert werden, was die Möglichkeit bietet, verschiedene Versionen der Daten zu sichern. Für beide Methoden werden jedoch eigene Programme benötigt.

## Inkrementelle Sicherung

Die inkrementelle Sicherung speichert nur jene Daten, die sich im Vergleich zu der vorliegenden Volldatensicherung oder vergangenen inkrementellen Sicherungsvorgängen geändert haben. Dies spart Zeit und Speicherplatz, erfordert jedoch im Fall einer Wiederherstellung der Daten, dass zunächst die Volldatensicherung übertragen wird und anschließend alle erfolgten inkrementellen Sicherungen nacheinander eingespielt werden.

## Differentielle Sicherung

Bei der differentiellen Sicherung werden immer jene Daten gespeichert, die sich im Verlgeich zu der vorliegenden letzten Volldatensicherung geändert haben. Im Unterschied zu der inkrementellen Sicherung entfällt also der Vergleich mit Daten aus zwischenliegenden Sicherungsvorgängen seit Erstellung der Volldatensicherung. Diese Methode erfordert zwar etwas mehr Zeit und Speicherplatz als die inkrementelle Sicherung, erleichtert aber die Wiederherstellung der Daten, da nur die Volldatensicherung und die letzte differentielle Sicherung auf das System übertragen werden muss. Die vorherigen differentiellen Sicherungen werden nicht benötigt.

## Automatisierung

Die Datensicherung kann mit Hilfe von Programmen oder Skripten automatisiert erfolgen. Wichtig ist dabei zu kontrollieren, dass die Datensicherung auch tätsächlich in der gewünschten Form ausgeführt wird. Geeignete Programme gibt es viele, wie beispielsweise [Bacula](http://bacula.org/), [DirSync Pro](http://www.dirsyncpro.org/), [TrayBackup](http://www.traybackup.de), [PersonalBackup](http://personal-backup.rathlev-home.de) oder [rsync](http://rsync.samba.org/). Eine ausführliche Liste ist außerdem auf der englischen Wikipedia unter [List of backup software](https://en.wikipedia.org/wiki/List_of_backup_software) zu finden. Oft können die Programme auch zur Wiederherstellung von gesicherten Daten verwendet werden.

- DirSync Pro: [http://www.dirsyncpro.org/](http://www.dirsyncpro.org/)
- TrayBackup: [http://www.traybackup.de](http://www.traybackup.de)
- PersonalBackup: [http://personal-backup.rathlev-home.de](http://personal-backup.rathlev-home.de)
- rsync: [http://rsync.samba.org/](http://rsync.samba.org/)
- Liste von Backup-Programmen auf Wikipedia: [https://en.wikipedia.org/wiki/List\_of\_backup\_software](https://en.wikipedia.org/wiki/List_of_backup_software)

## Sicherungszeitpunkt

Der Zeitpunkt der Sicherung spielt eine nicht zu unterschätzende Rolle. Beispielsweise kann eine Sicherung von Datenbanken im laufenden Betrieb zu Inkonsistenzen führen, weshalb in solchen Fällen ein Administrator diese Aufgabe übernehmen sollte.

Regelmäßige Sicherungsvorgänge, die zu bestimmten Zeitpunkten täglich, wöchentlich oder monatlich automatisiert gestartet und durchlaufen werden, gewährleisten, dass eine Sicherung auch tatsächlich erfolgt, zumal sie nicht vom individuellen Verhalten eines Nutzers abhängen.

Für Daten, die verschiedene Arbeitsschritte durchlaufen und dadurch große Änderungen erfahren, können die verschiedenen Zustände als Sicherungspunkte gespeichert werden. Beispielsweise können zunächst unbearbeitete digitale Bilder gespeichert werden, sowie ein daraus erzeugtes photogrammetrisches Modell oder andere nicht oder nur schwer reproduzierbare signifikante Verarbeitungsschritte. Solche Sicherungspunkte müssen allerdings manuell gemacht werden, indem beispielsweise ein Ordner mit den Rohdaten angelegt wird. Hinweise für solche Sicherungspunkte werden für bestimmte angewendete Methoden in dem Kapitel [Forschungsmethoden] (/it-empfehlungen/forschungsmethoden/index) gegeben.

## Sicherungsversionen

Es empfiehlt sich, eine vorhandene Volldatensicherung nicht direkt mit einer neuen Volldatensicherung zu überschreiben. Tritt nämlich während des Sicherungsvorganges ein Fehler auf, könnte auch die bereits vorhandene Sicherungsversion beschädigt werden.

Bei der Anwendung von inkrementellen oder differentiellen Sicherungsmethoden sollte trotzdem in geregelten Zeitabständen eine neue Volldatensicherung angelegt werden, welche mindestens bis zur nächsten Volldatensicherung aufgehoben wird. Dies ist im Sinne des Generationenprinzips oder Großvater-Vater-Sohn-Prinzips, einer Strategie zur Datensicherung, bei der mehrere Sicherungen für verschiedenen Zeitpunkte und Zwecke angelegt werden. Hierfür können beispielsweise wöchentlich und monatlich Volldatensicherungen angelegt werden (Vater und Großvater), die primär den Datenverlust durch Hardware- oder Software-Fehler reduzieren sollen. Tägliche inkrementelle oder differentielle Sicherungen (Sohn) erlauben es beispielsweise auf Arbeitsversionen des Vortages zuzugreifen und können mit dem Beginn einer neuen Woche nach und nach überschrieben werden.

## Disaster Recovery

Eine gute Sicherungsstrategie umfasst zusätzlich die Erprobung der Wiederherstellung der Daten, um im Ernstfall sicher zu sein, dass die verwendete Strategie auch wirklich funktioniert und die Daten schnell wieder einsatzfähig sind. Somit können vorhandene Sicherungsversionen ebenfalls auf ihre Funktionsfähigkeit überprüft werden.
