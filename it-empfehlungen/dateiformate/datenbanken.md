---
title: Datenbanken
sorting: it030106
webtoc: true
authors:
  - trognitz.martina
  - gerth.philipp
  - schäfer.felix
downloads:
  - checkliste-erstellung-datenbank
---
*Der Stand der FDM-Empfehlungen entspricht 2018. Die FDM-Empfehlungen werden sukzessiv erneuert, falls Sie Interesse haben mitzuwirken nutzen Sie bitte [diesen Workflow](https://github.com/dainst/ianus-web-content/wiki/Erstellung-von-Lehrangeboten).*

# Datenbanken

## Übersicht
Datenbanksysteme (DBS) dienen der Strukturierung, Pflege und Verwaltung von Daten. Ein DBS besteht aus einer Datenbank mit dem eigentlichen Datenbestand und der Datenbanksoftware, mittels derer auf die Daten zugegriffen wird. Datenbanksysteme werden zur Strukturierung, Pflege und Verwaltung von Daten verwendet. Sie bestehen aus zwei Komponenten: einerseits aus der Datenbank, welche den logisch zusammengehörigen Datenbestand umfasst, andererseits aus dem Datenbankmanagementsystem (DBMS), der Datenbanksoftware, welche u.a. die Zugriffsrechte regelt und Vorkehrungen zur Datensicherheit gewährleistet.

<!--..ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.....
Häufig wird auch die englisch ausgesprochene Abkürzung IT verwendet. Empfehlungen betrachtet werden. Sätze unvollständig --> 

Es gibt verschiedene Datenbankmodelle, von denen relationale Datenbanksysteme am häufigsten verwendet werden und im Rahmen der Informationstechnologie ein Oberbegriff für die Informations- und Datenverarbeitung sowie für die dafür benötigte Hard- und Software sind. Dabei werden die Daten in Tabellen (Relationen) strukturiert, wobei Verweise von einer Tabelle auf eine andere möglich sind. Näheres zu Tabellen ist in dem Kapitel [Tabellen](https://ianus-fdz.de/it-empfehlungen/dateiformate/tabellen) zu finden.



### Langzeitformate
Für relationale Datenbanken wird eine Archivierung in Form eines Exports der Datenbankinhalte, der Strukturinformationen und weiterer Funktionalitäten in textbasierte Formate empfohlen, welche unabhängig vom verwendeten Datenbankmanagementsystem sind. Neben den Daten in den Tabellen müssen die Datenbankstrukturdefinitionen wie Attributdatentypen, Relationen zwischen den Tabellen und Formeln zwingend mit archiviert werden. Unabhängig vom gewählten Archivformat ist es nötig, die grafische Benutzeroberfläche zu dokumentieren, zum Beispiel in Form von Bildschirmfotos oder eines eventuell vorhandenen Benutzerhandbuches. Eine darüberhinaus gehende Erhaltung der Funktionalität ist zumeist nur mit Hilfe der technisch sehr aufwendigen [Emulation](https://www.google.com/search?q=emulation+bedeutung&rlz=1C1GCEA_enDE1030DE1030&oq=emulation+bedeut&aqs=chrome.0.0i512j69i57j0i22i30j0i15i22i30l2j0i22i30j0i15i22i30j0i22i30j0i390i650l2.7265j1j7&sourceid=chrome&ie=UTF-8) möglich, bei der das ursprüngliche Datenbanksystem durch ein anderes System mit ähnlicher Funktionsweise ersetzt wird. Unabhängig von den vorgestellten Archivformaten ist der Umgang mit sogenannten Binary Large Objects (BLOBs). Dabei handelt es sich um intern gespeicherte Mediendateien, meistens Fotos, Zeichnungen, z. B. von Funden, oder [PDF](https://ianus-fdz.de/it-empfehlungen/dateiformate/pdf-dokumente)-Dokumente. Diese Medien müssen in jedem Fall exportiert, auf die dann externen Dateien muss referenziert und je nach Dateityp in für die Archivierung geeigneten Formaten gespeichert werden (siehe entsprechendes Dateiformatkapitel). Grundsätzlich wird von der Verwendung von BLOBs abgeraten und eine externe Speicherung von Medieninhalten empfohlen.

Ein geeignetes Archivformat ist **SQL** ([Structured Query Language](https://www.techtarget.com/searchdatamanagement/definition/SQL), welches seit 1986 bei der ANSI (American National Standards Institute)) standardisiert ist und seit 1987 ebenfalls als ISO (International Organization for Standardization) bzw. IEC (International Electrotechnical Commission) 9075 zertifiziert ist. Seitdem wurde der SQL-Standard in sieben Revisionen weiter ausgebaut, wobei SQL:2011 die neueste Version ist. Jedoch wird dieser Standard in den verschiedenen Datenbanksystemen wie MySQL, PostgreSQL oder OracleDB unterschiedlich umgesetzt und erweitert. Daher gibt es je nach Datenbanksystem mehrere spezifische Befehle, welche über die Spezifikation des Standards hinausgehen. In Folge dessen sind die verschiedenen DBMS nicht vollständig kompatibel, weswegen eine exportierte Datenbank im SQL-Format nur dann problemlos und ohne zusätzlichen Aufwand importiert werden kann, wenn das ursprüngliche DBMS verwendet wird. Daher kann SQL für die Archivierung nur dann empfohlen werden, wenn ein einheitlicher ANSI-/ISO-Standard, z. B. SQL:2008, verwendet wird, welcher von DBMS-spezifischen Befehlen bereinigt ist. Der verwendete Standard muss dokumentiert werden. Der Vorteil in der Speicherung in SQL liegt in der gleichzeitigen Erhaltung der kompletten Daten, der Tabellen und ihrer Relationen zueinander, der Attributspezifikationen sowie der kompletten Metadaten. Nach einem Export, erhält man eine singuläre textbasierte Datei, welche sich mit relativ geringem Aufwand wiederherstellen lässt. Die Speicherung einer Datenbank in einem SQL-Skript erfolgt unter Angabe der SQL-Befehle, welche zum Import der Datenbankinhalte benötigt und ggf. für jeden Datensatz wiederholt werden müssen. Die damit einhergehende Redundanz erhöht die Datenmenge. Datenbanken aus geisteswissenschaftlichen Forschungsprojekten erreichen jedoch nur selten eine Größe, bei welcher dieser Nachteil zum Tragen kommt.

**XML** eignet sich als Archivformat für Datenbanken aus Gründen der Systemunabhängigkeit, Standardisierung, Lesbarkeit und Erweiterbarkeit. Für die Speicherung der Datenbankinhalte kann XML uneingeschränkt empfohlen werden. Die Beschreibung der Datenbankstruktur sollte mithilfe einer entsprechenden XML-Schema-Definition (XSD) wie der Database Markup Language erfolgen. Alternativ kann die Datenbankstruktur im SQL-Format und als Entitäten-Relationen-Diagramm (ERD) gespeichert werden.

Das 2008 initial vom schweizerischen Bundesarchiv entwickelte und im Rahmen des e-ARK-Projekts weiterentwickelte Format **SIARD** (Software Independent Archiving of Relational Databases) in der Version 2.0 beruht im Wesentlichen auf den beiden ISO-Standards XML gemäß ISO/IEC 19503:2005 und SQL:2008. Es vereinigt damit die Vorteile einer Datenhaltung in XML mit einer Dokumentation der Datenbankstruktur in SQL. Es ist als eCH-Standard offen und wird unter einer freien Lizenz zur Verfügung gestellt.

Ein alternativer bewährter Ansatz zur Archivierung der Tabellen einer Datenbank ist der Export in das **CSV**-Format, welches besonders langlebig und weit verbreitet ist. Diese Methode ist technisch mit relativ geringem Aufwand verbunden, besitzt aber einen starken Fokus auf die Datenbankinhalte und geht daher mit einem vollständigen Verlust der Funktionalitäten und Datenbankstruktur einher. Infolgedessen ist es zwingend erforderlich, bei der Speicherung im CSV-Format zusätzlich die Datenbankstruktur in Form von strukturierten Diagrammen, wie dem Entitäten-Relationen-Diagramm (ERD) festzuhalten. Selbst dann ist die Datenbankstruktur nur teilweise und sehr aufwendig rekonstruierbar, weswegen das CSV-Format nur bei einer hybriden Lösung mit der Archivierung der Datenbankstruktur in einem geeigneten Format (z. B. SIARD, SQL, XML/DML) bei gleichzeitiger Speicherung der Daten im CSV-Format, empfohlen werden kann. Als Zeichenkodierung sollte UTF-8 verwendet werden, wobei RFC-4180-konform als Trennzeichen ein Komma (,) und als Textbegrenzungszeichen das Anführungszeichen (") verwendet werden sollte. Mehr dazu ist in dem Kapitel [Tabellen](https://ianus-fdz.de/it-empfehlungen/dateiformate/tabellen) zu finden.

Bei der JavaScript Object Notation (**JSON**) handelt es sich um ein einfaches textbasiertes Datenformat, welches für einen schnellen Datentransfer im Internet entwickelt wurde und als RFC 7159 und ECMA-404 standardisiert ist. Es besitzt bei der Speicherung von Daten vergleichbare Vorteile wie XML, ist dabei aber wesentlich kompakter. Zur Zeit gibt es allerdings keinen Standard zur Beschreibung von Datenbankstrukturen in JSON, weswegen auch hier auf eine hybride Archivierungslösung mit der Speicherung der Datenbankinhalte in JSON und gleichzeitiger Speicherung der Datenbankstruktur in einem anderen Format (z. B. SIARD, SQL, XML/DML) zurückgegriffen werden muss.

Die proprietären Dateiformate von Desktop-DBMS, wie Microsoft Access, dBASE oder FileMaker eignen sich **nicht** für die Archivierung, da die Formatspezifikationen nicht offen vorliegen und verschiedene Versionen oft nicht untereinander kompatibel sind. Ebenso verhält es sich mit den binären Exportformaten serverbasierter, relationaler DBMS, wie Oracles DMP-Format oder das komprimierte BAK-Format von PostgreSQL. Auch diese folgen keinem allgemeingültigen Standard, liegen nur als Binärdatei vor und sind teilweise proprietär. Eine spätere Nachnutzung ist eng an das jeweilige für alle Nutzer kostenpflichtige Produkt sowie spezielle Tools gebunden.

**ODB** ist ein Container-Dateiformat des Programms, welche in LibreOffice und OpenOffice enthalten ist. ODB ist ein Teil vom OpenDocument Format (ODF) und wurde von einem technischen Komitee unter der Leitung der Organization for the Advancement of Structured Information Standards (OASIS) entwickelt und unter ISO/IEC 26300 standardisiert. Der ZIP-Container enthält verschiedene Dateien, die zum Betrieb der Datenbank erforderlich sind, wie persönliche Konfigurationsdateien, eine binäre Datei des Datenbankmanagementsystems HSQLDB mit den  Datenbankinhalten sowie der Datenbankstruktur und die XML-basierten Formulare und Reports. Aufgrund der binären Datenstruktur kann ODB nicht für die Langzeitarchivierung empfohlen werden.

Keines der genannten und empfohlenen Formate unterstützt und enthält alle notwendigen Informationen und signifikanten Eigenschaften, die für die Archivierung und Nachnutzung einer Datenbank relevant sind. Und einige Informationen, etwa ein Handbuch zur Benutzung, müssen ohnehin gesondert gespeichert werden. Daher ist eine hybride Archivierungsstrategie erforderlich, welche verschiedene Dateien mit unterschiedlichen Dateiformaten umfasst. In der folgenden Tabelle werden die Kategorien von Informationen, welche von den für die Archivierung geeigneten Datenbankformate prinzipiell gespeichert werden können, durch Abkürzungen kenntlich gemacht: I = Datenbankinhalt, S = Datenbankstruktur, F = Funktionalitäten, B = Benutzung. Eine zusätzliche Übersicht ist in dem Abschnitt Vertiefung zu finden.

*Anmerkung J. Watson 2023-06-05: M.E. vereinfacht. Sowohl in CSV als auch in xml kann die komplette DB abgebildet werden; hängt natürlich von der Datenbank ab. Ich würde sowohl CSV als auch XML und JSON mit einem grünen Häkchen versehen*

| &nbsp; | Format          | Begründung                                                                                                                                                                                                                                                                                                                                                                                   |
| ------ | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ✔      | SIARD, SIARD2   | SIARD ist offen, frei verfügbar und setzt auf die Standards SQL und XML. Der wesentliche Vorteil von SIARD liegt darin, dass sowohl die Datenbankstruktur als auch die Datenbankinhalte gemeinsam beschrieben und archiviert werden. Für die Archivierung sollte Version 2.0 verwendet werden. Speichert: I, S, F.                                                                           |
| ✔      | SQL             | Geeignet für die Langzeitarchivierung bei Verwendung eines offiziellen ISO/IEC 9075 Standards, z.B. SQL:2008. Daten, Datenbankstruktur und ein Großteil der Funktionalität bleiben erhalten. Der verwendete Standard muss dokumentiert sein. Speichert: I, S, F.                                                                                                                             |
| 〰️     | XML             | XML bietet sich insbesondere zur Speicherung der Daten einer Datenbank an. Die Datenbankstruktur sollte mit Hilfe eines XSD-Schemas, wie DBML, beschrieben werden. Alternativ ist dies auch mithilfe einer SQL-Datei oder SIARD möglich. Speichert I und teilweise S.                                                                                                                        |
| 〰️     | CSV, TSV        | Das CSV Format ist ein langlebiges, textbasiertes und weit verbreitetes Format. Bei dem Export von Datenbankinhalten in das CSV-Format gehen allerdings Informationen zur Datenbankstruktur und zu Funktionalitäten verloren, weshalb es nur bei einer gleichzeitigen Speicherung der Datenbankstruktur in einem anderen Format (z. B. SIARD, SQL, XML/DBML) zu empfehlen ist. Speichert: I. |
| 〰️     | JSON            | JSON bietet sich als Format zur strukturierten Speicherung von Datenbankinhalten an. Da es keine Standards zur Beschreibung der Datenbankstruktur im JSON Format gibt, muss diese gesondert in einem geeigneten Format (z. B. SIARD, SQL, XML/DBML) gespeichert werden. JSON bietet sich insbesondere für die Archivierung von Daten aus NoSQL Datenbanken an. Speichert: I.                 |
| ❌      | MDB, ACCDB      | Binäre, proprietäre Formate von Microsoft Access, die nicht zur Archivierung geeignet sind.                                                                                                                                                                                                                                                                                                  |
| ❌      | FP5, FP7, FMP12 | Binäre, proprietäre Formate von FileMaker, die nicht zur Archivierung geeignet sind.                                                                                                                                                                                                                                                                                                         |
| ❌      | ODB             | Containerformat von OpenOffice, welches verschiedene XML-basierte Dateien, wie z.B. Formulare und Abfragen, und die binären Dateien mit den Inhalten und der Struktur der Datenbank enthält. ODB ist nicht zur Archivierung geeignet. Speichert: teilweise B.                                                                                                                                |
| ❌      | DBF             | Binäres, proprietäres Format von dBASE, das nicht zur Archivierung geeignet ist.                                                                                                                                                                                                                                                                                                             |
| ❌      | BAK, DB, DMP    | Die verschiedenen, binären Exportformate von relationalen Datenbanksystemen sind für die Archivierung nicht geeignet.                                                                                                                                                                                                                                                                        |

### Dokumentation

Die Empfehlungen zur Dokumentation von Datenbanken orientieren sich an verschiedenen Standards, darunter SIARD Metadata Schema, Archival Data Description Mark-up Language (ADDML) und Database Markup Language (DBML). Allen Schemata gemein ist eine differenzierte Beschreibung der verschiedenen Ebenen eines Datenbanksystems. Dazu gehören [Metadaten](/it-empfehlungen/projektphasen/dokumentation/dokumentation-der-metadaten) zur allgemeinen Beschreibung der Datenbank als auch spezifische Metadaten zur Beschreibung der hierarchisch aufgebauten Ebenen einer Datenbank: den in SQL Datenbanken vorkommenden Schemen, die mehrere Tabellen beinhalten, welche wiederum mit Hilfe von mehreren Attributen definiert werden können.

Weitergehende Dokumente, die zum Verständnis einer Datenbank, ihrer spezifischen Nutzung oder zur Eigenart der Inhalte notwendig sind, wie beispielsweise Benutzerhandbuch, Bildschirmfotos, ERD-Diagramme, Beschreibungen semantischer Konventionen (wie Wertelisten), Anforderungsanalysen oder Rechte- und Rollendokumentation sollten auf alle Fälle mit archiviert werden.

Ergänzend zu den Metadaten, wie sie in dem Abschnitt [Metadaten in der Anwendung](/it-empfehlungen/projektphasen/dokumentation/metadaten-in-der-anwendung/). gelistet sind, sollten folgende minimale Metadaten zur nachhaltigen Beschreibung von Datenbanken aufgenommen werden.  


| **Metadatum**              | **Beschreibung**                                                                                                                                                                     |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Datenbankname              | Ansprache/Name der Datenbank                                                                                                                                                         |
| Beschreibung der Datenbank | Zusammenfassung über Zweck, Bedeutung und Inhalt der Datenbank                                                                                                                       |
| Sprache                    | Liste der Sprachen, in welchen die Daten eingegeben wurden sowie Sprachkennungen nach ISO 639 angeben.                                                                               |
| Identifikator              | Falls die Datenbank online öffentlich zugänglich ist, sollte ein persistenter Identifikator (z.B. DOI, URI) oder eine eindeutige Adresse (z.B. URL) angegeben werden.                |
| Rechteinhabende            | Falls die Datenbank online öffentlich zugänglich ist, sollte ein persistenter Identifikator (z.B. DOI, URI) oder eine eindeutige Adresse (z.B. URL) angegeben werden.                |
| DBMS                       | Name des Datenbankmanagementsystems mit Versionsnummer mit der die Datenbank betrieben wurde.                                                                                        |
| Schemata Liste             | Liste der Schemata innerhalb der Datenbank sofern vorhanden.                                                                                                                         |
| Nutzende                   | Liste der Nutzerinnen und Nutzer und ihrer Rolle innerhalb der Datenbank.                                                                                                            |
| Rolle                      | Liste der verschiedenen Rollen und Gruppen mit ihren definierten Zugriffsrechten.                                                                                                    |
| Standard                   | Name und Version verwendeter Standards, etwa zur Definition des Datentyps eines Attributs, zur Dokumentation von Abfragen oder zu dem Datenbankformat, z.B. SQL:2008 oder SIARD 2.0. |
| Abgeleitete Dateien        | Aus den Datenbankinhalten erzeugte Grafiken, Abbildungen, Diagramme müssen zusätzlich separat archiviert und gelistet werden.                                                        |
| Weitere Dateien            | Liste weiterer Dokumente, die für das Verständnis und die Dokumentation einer Datenbank notwendig sind, wie beispielsweise ein ERD oder ein Benutzerhandbuch.                        |



| **Schema Metadatum**  | **Beschreibung**                                                                     |
| --------------------- | ------------------------------------------------------------------------------------ |
| Schema Name           | Name des Schemas.                                                                    |
| Schema Beschreibung   | Bedeutung und Inhalt des Schemas.                                                    |
| Tabellenliste         | Liste der Tabellen im Schema.                                                        |
| Funktion              | Name und Art der Funktion (Gespeicherte Funktionen, Sichten).                        |
| Funktion Beschreibung | Beschreibung der Funktion hinsichtlich Sinn und Zweck.                               |
| Funktion Befehl       | Befehle der Funktion nach einem einheitlich festgelegten Standard (Syntax Standard). |



| **Tabelle Metadatum** | **Beschreibung**                      |
| --------------------- | ------------------------------------- |
| Tabelle Name          | Name der Tabelle.                     |
| Tabelle Beschreibung  | Bedeutung und Inhalt der Tabelle.     |
| Anzahl Datensätze     | Anzahl der Datensätze in der Tabelle. |
| Attributliste         | Liste der Attribute in der Tabelle.   |



| **Attribut Metadatum**   | **Beschreibung**                                                                                                                                                   |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Attribut Name            | Name des Attributs.                                                                                                                                                |
| Attribut Beschreibung    | Bedeutung und Inhalt des Attributs. Wird das Attribut mit Hilfe von Einheiten, z. B. metrische Maßeinheiten, ausgedrückt, ist die Angabe der Einheit erforderlich. |
| Attribut Typ             | Datentyp des Attributs nach einem einheitlich festgelegtem Standard (Syntax Standard) z. B. "Integer" nach SQL:2008.                                               |
| Kontrolliertes Vokabular | Sofern für das Attribut eine Werteliste vorliegt oder ein Thesaurus verwendet wurde, ist dieses zu dokumentieren.                                                  |
| Attribut Schlüssel       | Sofern es sich um ein Schlüsselattribut handelt, Benennung der Schlüsselart z. B. Primär- oder Fremdschlüssel.                                                     |
| Fremdschlüssel Referenz  | Im Falle eines Fremdschlüssels Angabe des referenzierten Attributs mit Angabe der Tabelle und des Schemas.                                                         |

<!---
```

Weitere Inhalte

FileMaker-Datenbanken · Attributtypen · Bestandteile einer Datenbank · Beziehungen · Datenbanksystem (DBS) · Datenbankmanagementsystem (DBMS) · Datenbankmodelle · Dateneingabe · Datenqualität · Desktop-DBMS · Dokumentation · Dokumentation von Access-Datenbanken · Entity-Relationship-Modell (ERM) · Entwurf einer Datenbank · ERD · Exportmöglichkeiten · Mehrsprachigkeit · Relationale Datenbanken · Schnittstellen · Serverbasierte DBMS · Speicherung und Sicherung · Structured Query Language (SQL)    Zerschießt Layout von Seite

```
-->

Ein Datenbanksystem (DBS) ist ein System zur elektronischen Verwaltung großer Datenmengen, um diese effizient, widerspruchsfrei und dauerhaft zu speichern und in den benötigten Teilmengen in unterschiedlichen Darstellungsformen für Benutzer und Anwendungsprogramme bereitzustellen. Gegenüber einer Speicherung in strukturierten Einzeldateien, wie Tabellen, werden unter anderem folgende Probleme effizienter gelöst:


* **Redundanzen**: Bei einer Speicherung in Einzeldateien werden viele Daten mehrfach gespeichert. Änderungen werden dadurch sehr aufwendig, da sie an verschiedenen Stellen durchgeführt werden müssen.
* **Inkonsistenzen**: Sowohl bei der gleichzeitigen Änderung von Daten durch mehrere Benutzer als auch bei Änderungen von redundanten Daten kann es leicht zu Widersprüchen und Inkonsistenzen in den Daten kommen, was mit der Verwendung von DBS vermieden wird.
* **Integritätsbedingungen**: Sofern einzelne oder globale Informationen direkt von anderen Informationen abhängen, lassen sich entsprechende Bedingungen in der Datenbank abbilden, die bei der Eingabe neuer Informationen eine Kontrollfunktion übernehmen und dadurch bestimmte Fehler in den Daten verhindern können.
* **Datenschutzprobleme**: Einzeldateien besitzen kein dezidiertes User-Management, weswegen ein Zugriff auf den gesamten Datenbestand vorliegt, wohingegen DBS differenzierte Zugriffsregelungen ermöglichen.
* **Darstellungsvarianten**: Mit einem DBS lassen sich verschiedene Ausschnitte, sog. Sichten (engl. views), aus der Gesamtmenge aller gespeicherten Informationen erstellen und so einmal eingetragene Informationen für unterschiedliche Zwecke und Nutzer variabel anzeigen (z.B. in einem Eingabeformular, als tabellarische Übersicht oder vorformatiert für eine Publikation).

![datenbanken_vergleich](https://github.com/dainst/ianus-web-content/assets/29372760/823bd2a3-fb8b-49c5-8d90-74bb3b5b682f)
*Vergleich von Datenhaltung in Einzeldateien (links) gegenüber Datenhaltung mit Hilfe eines Datenbanksystems (rechts).*

Ein DBS besteht aus der Verwaltungssoftware, genannt Datenbankmanagementsystem (DBMS), und der Menge der zu verwaltenden Informationen, der eigentlichen Datenbank (DB). Die Datenbank enthält zusätzlich zu den eigentlichen Inhalten noch die Beschreibung der Datenstruktur, die in einem Datenkatalog und in einem Datenbankschema mittels Metadaten festgehalten wird.\n
Bei einem DBMS handelt es sich um ein Programm (kommerzielle Produkte sind u. a. FileMakerPro, Access und Oracle, OpenSource sind u. a. MySQL und PostgreSQL), das als Steuerungsprogramm intern die strukturierte Speicherung der Daten organisiert und alle lesenden und schreibenden Zugriffe auf die Datenbank ausführt. Der Benutzer greift also nicht direkt auf die Datenbank zu, sondern auf das DBMS als Kontrollinstanz. Die Aufgaben eines DBMS umfassen u. a. folgende Bereiche:

* Eingabe, Änderung und Löschen von Daten
* Erstellen von Datenbanken inklusive Umsetzung des Datenmodells
* Suchen in den Datenbankinhalten mittels Abfragen
* generelle Verwaltung von Benutzern, Zugriffen und Zugriffsrechten

Der Begriff Datenbank (DB) bezieht sich auf die eigentlichen Sachdaten, die entweder von Benutzern manuell eingegeben oder automatisch generiert werden. Die Datenbankinhalte können in unterschiedlichen Formaten vorliegen und als Texte, Zahlen, Links oder Medien (Fotos, Zeichnungen, Filme etc.) in die Datenbank einfließen. Dieser Datenbestand wird von einem DBMS verwaltet, auf Speichermedien abgelegt und je nach Vorgabe kontrolliert (damit z. B. ein Funddatum immer auch einem Fund zugeordnet ist).

## Datenbankmodelle

Zur formalen Beschreibung aller in der Datenbank enthaltenen Daten, ihrer Speicherung und ihrer Beziehungen untereinander verwendet man auf der konzeptionellen Ebene ein Datenmodell. Es ist die konzeptuelle Grundlage für ein Datenbanksystem und legt fest, auf welche Art und Weise der jeweils interessierende Ausschnitt aus der realen Welt in einer Datenbank abgebildet wird.

Es gibt verschiedene Datenmodelle, von denen das relationale das am weitesten verbreitete ist.

**Relationales Datenmodell**: Bei Relationalen Datenbanken (untenstehende Abbildung) werden die Daten sowie deren Beziehungen untereinander in Form von Tabellen (Relationen) beschrieben. Die einzelnen Einträge in unterschiedlichen Tabellen können mittels Verweise miteinander in Beziehung gesetzt werden.

![datenbanken_relationaleDBs-web](https://github.com/dainst/ianus-web-content/assets/29372760/ecbbc10f-44be-4a82-b5a1-6a8319e29198)
*Beispiel einer relationalen Datenbank anhand von Münzdaten*

**Hierarchisches Datenmodell**: Bei hierarchischen Datenbanken (untenstehende Abbildung) werden die Informationen in Datensätze gruppiert und in einer baumartigen Datenstruktur gespeichert, die einer Mutter-Kind-Beziehung entspricht: Jede Mutter kann mehrere Kinder haben, ein Kind aber nur eine Mutter besitzen.

![datenbanken_hierarchischeDBs-web](https://github.com/dainst/ianus-web-content/assets/29372760/6936d791-25b9-4528-a7d6-85dfea68af56)
*Beispiel einer hierarchischen Datenbank anhand von Münzdaten*

**Netzwerk Datenmodell**: Netzwerkdatenbanken (untenstehende Abbildung) stellen eine Verallgemeinerung und Weiterentwicklung des hierarchischen Datenmodells dar, wobei die Daten in logischen Graphen strukturiert werden. Da die einzelnen Knoten im Graph beliebig miteinander über Beziehungen verknüpft werden könne, entfallen die Beschränkungen, die mit Mutter-Kind-Beziehungen einhergehen.

![datenbanken_netzwerkDBs-web](https://github.com/dainst/ianus-web-content/assets/29372760/1fe20bc7-1d5e-40e5-9916-438ddb13a771)
*Beispiel einer Netzwerkdatenbank anhand von Münzdaten*

**Objektorientiertes Datenmodell**: Analog zu den objektorientierten Programmiersprachen versuchen objektorientierte Datenbanken (untenstehende Abbildung) Objekte aus der realen Welt mit ihren Eigenschaften und ihrem Verhalten nachzubilden. Die Definition der Objekte erfolgt über Klassen, welche Attribut- und Verhaltensdefinitionen enthalten und als Bauplan für daraus erzeugte Objekte fungieren.

![datenbanken_objektorientierteDBs-web](https://github.com/dainst/ianus-web-content/assets/29372760/72f76cd1-da5c-4042-a3c4-dec2a60cb5b1)
*Beispiel einer objektorientierten Datenbank anhand von Münzdaten*

**NoSQL Datenmodell**: Der Begriff NoSQL steht für "Nicht nur SQL" (Not only SQL) und bezeichnet Datenbanken, welche kein relationales Datenschema, sondern andere Paradigmen verfolgen. Sie können in zwei Typen unterschieden werden:
* Bei dokumentenorientierten Datenbanken wird die zusammengehörige Informationsmenge in einem einzelnen Dokument gespeichert. Die Daten werden in Feldname-Wert-Paaren (z. B. Datierung: Römisch) z.B. im JSON Format gespeichert, wobei nicht jedes Paar vorhanden sein muss, was eine gewisse Flexibilität erlaubt.
* Graphen-Datenbanken können als moderne Nachfolger von Netzwerkdatenbanken verstanden werden, die vor allem bei sehr stark vernetzten Daten verwendet werden. Auch hier werden mit Hilfe von Graphen die Daten als Knoten dargestellt und die Beziehungen zwischen Ihnen als Kanten, wobei sowohl die Knoten als auch die Kanten Eigenschaften besitzen.

```
{
   "id":1,
   "Fundstellen_Name":"Korinth",
   "Breite":37.91,
   "Länge":22.87,
   "Münzen":[
      {
         "id":23,
         "Münzen_Name":"Commodus aus Korinth",
         "Metall":"Bronze",
         "Fotos":[
            {
               "id":49,
               "Foto_Name":"Fundfoto -- Avers"
            },
            {
               "id":50,
               "Foto_Name":"Fundfoto -- Revers"
            }
         ]
      },
      {
         "id":24,
         "Münzen_Name":"Münze aus Korinth",
         "Metall":"Bronze",
         "Fotos":{
            "id":51,
            "Foto_Name":"Fundfoto"
         }
      }
   ]
}

```

### Relationale Datenbanken

Das relationale Datenmodell hat sich als Standard von Datenbankanwendungen etabliert, da sich damit die Realwelt mit recht einfachen und realitätsnahen Strukturen abbilden lässt. In der archäologischen Forschung wird dieses Datenmodell fast ausschließlich eingesetzt.

Vereinfacht kann man sich eine relationale Datenbank als eine Sammlung von Tabellen (Relationen) vorstellen, in denen jeder Datensatz in einer Zeile (Tupel) einer Tabelle gespeichert wird (untenstehende Abbildung). Jede Zeile besteht aus einer Anzahl von Attributen (Eigenschaften), den Spalten der Tabelle. Jedes Attribut hat einen eindeutigen zur Referenzierung dienenden Namen und einen bestimmten Attributtyp, welcher definiert welche Art von Daten - beispielsweise Zeichensätze (String) oder Fließkommazahlen (Float) - in dem Attribut gespeichert werden können. Jedes Attribut kann Werte entsprechend ihres Wertebereiches aufnehmen, der sich aus den Attributtyp ergibt. Zum Beispiel kann eine Münze mit Hilfe folgender Attribute (mitsamt Attributtypen) beschrieben werden: ID (Integer), Nominal (String), Datierung (String), Material (String), Durchmesser (Integer), Gewicht (Float), Funddatum (Date).

![datenbanken_relationBsp](https://github.com/dainst/ianus-web-content/assets/29372760/ad8bd392-31f4-4431-be48-b07ac89703e8)
*Aufbau der Relation "Münze" am Beispiel von Informationen zu Münzen.*

Pro Tabelle werden immer nur gleichartige, reale Objekte (Entitäten) erfasst, z. B. nur Befunde, nur Münzen, nur Fotos, nur Bauwerke etc. Die eindeutige Referenzierung eines Datensatzes erfolgt mit Hilfe eines oder mehrer Schlüsselattribute, dem sogenannten Primärschlüssel. Dieser Schlüssel ist einzigartig und darf sich niemals ändern, da damit die Zeile in der Tabelle referenziert wird. Der Aufbau aller Tabellen, die zu einer Datenbank gehören, also die Datenbankstruktur, muss in dem Datenkatalog dokumentiert werden. Dieser enthält somit alle Festlegungen und Detailinformationen, die die Struktur der Datenbankinhalte in einem konkreten DBMS beschreiben, z.B. den Typ verschiedener Attribute (Kurztext, Langtext, Zahlen, Datum, Medien, etc.) und die Abhängigkeiten der Attribute zueinander. Der wichtigste Teilaspekt des Datenkataloges ist das Datenbankschema, das in abstrahierter Form die Beziehung und Art der Speicherung von Einzelinformationen festlegt.

#### Beziehungen
Einzelne Tabellen können anhand von Schlüsseln miteinander in Beziehung gesetzt werden, um Beziehungen zwischen einzelnen Datensätzen aus den unterschiedlichen Tabellen explizit auszudrücken. Beispielsweise um einer Münze, welche in der Tabelle "Münze" gespeichert ist, einem Fundort, welcher in der Tabelle "Fundort" gespeichert ist, zuzuweisen (untenstehende Abbildung). Mit Hilfe von Primärschlüsseln (Hauptschlüssel, engl. Primary Key) wird der Datensatz einer Relation eindeutig definiert, wie im vorliegenden Beispiel mit Hilfe des Attributs "Muenze-ID". Der Primärschlüssel einer Relation darf dabei nur einmal vorkommen, muss also einzigartig sein, um eine Referenzierung zu gewährleisten.

Ein Fremdschlüssel (engl. Foreign Key) dient zur Referenzierung eines Primärschlüssels einer anderen Tabelle. In dem Münzenbeispiel wurde die Relation "Muenze" um eine Attribut "FS_FundortID" erweitert. Es ist ein Fremdschlüssel, welcher auf den Primärschlüssel "PS_FundortID" der Relation Fundort verweist.

![datenbanken_beziehungBsp](https://github.com/dainst/ianus-web-content/assets/29372760/6b721b1a-8c77-42e7-bf72-77974d777953)
*Beispielhafte Beziehung zwischen der Relation "Muenze" und der Relation "Fundort"*

Die Beziehungen zwischen zwei verschiedenen Relationen können dabei mit den folgenden gebräuchlichen Beziehungstypen beschrieben werden. Der Beziehungstyp wird dabei mit Hilfe einer Mengenangabe, der Kardinalität, angesprochen, der angibt wie viele Datensätze einer Relation mit wie vielen Datensätzen einer weiteren Relation in Beziehung stehen:
* In 1 : 1 - Beziehungen ist jedem Datensatz einer Tabelle A nur ein einziger passender Datensatz in Tabelle B zugeordnet. Diesen Beziehungstyp verwendet man unter anderem, um eine unübersichtliche Tabelle mit vielen Attributen in mehrere übersichtliche Tabellen aufzuteilen. Beispielsweise werden in einer Tabelle für Münzen allgemeine Eigenschaften abgebildet und die Einzelheiten für die Vorder- und Rückseite einer Münze werden in gesonderten verknüpften Tabellen beschrieben.
* In 1 : N - Beziehungen, können einem Datensatz der Tabelle A mehrere passende Datensätze aus Tabelle B zugeordnet sein, wobei jedoch einem Datensatz aus Tabelle B nie mehr als ein Datensatz aus Tabelle A zugeordnet werden kann. Beispielsweise können an einem Fundort mehrere Münzen gefunden worden sein, aber eine Münze kann nur einen Fundort haben, wie in der Abbildung oben dargestellt ist.
* Bei M : N - Beziehungen können jedem Datensatz aus einer Tabelle A mehrere passende Datensätze aus einer Tabelle B zugeordnet sein und umgekehrt. Auf einem Foto können beispielsweises mehrere Münzen zu sehen sein, während es für eine Münze auch mehrere Fotoansichten geben kann.

#### Attributtypen

Es gibt verschiedene Attributtypen, die spezifische Informationen und Wertebereiche speichern:
* Ganze Zahlen (integer, long) sind zu verwenden für Schlüssel, ordinalskalierte Variablen, wie etwa Schulnoten, oder sonstige numerische Angaben, bei denen die Genauigkeit ganzer Zahlen ausreichend ist.
* Fließkommazahlen (float) kommen zum Beispiel bei metrischen Maßen zum Einsatz. Bei allen Maßeinheiten ist zu beachten, dass in der Attributdefinition die verwendete Maßeinheit notiert und diese während der Benutzung auch einheitlich verwendet wird.
* Bool'sche Felder lassen nur zwei Werte zu: "ja" (1) oder "nein" (0) bzw. "wahr" oder "falsch".
* Textfelder (varchar) können mit einer maximalen Länge definiert werden oder aber ohne weitere Angaben standardmäßig bis maximal 255 Zeichen verwendet werden.
* Größere Textfelder (text) erlauben einen beliebig langen Freitexteintrag. Sie sollten so wenig wie möglich verwendet werden, da sie verhindern Informationen strukturiert einzutragen und somit ein gezieltes Auffinden erschweren. Sie können bei einer späteren Konvertierung einer DB in ein neues System Schwierigkeiten verursachen.
* Medienfelder/Binary Large Objects (BLOBs) ist ein binärer Datentyp, der zur datenbankinternen Speicherung von externen Medieninhalten (Fotos, Zeichnungen, Filme, Texte etc.) verwendet werden kann. Jedoch empfiehlt es sich diese Medieninhalte außerhalb der eigentlichen Datenbank zu speichern und nur die Referenz auf den Speicherort der externen Ressource in einem Attribut zu erfassen. Dadurch werden u. a. die Datenbankgröße überschaubar gehalten, eine konsistente Datenhaltung der Einzeldaten gewährleistet und Probleme beim Export der Datenbankinhalte reduziert. Ist im Ausnahmefall dennoch das Importieren von externen Medieninhalten notwendig, sollten diese für den jeweiligen Zweck optimiert sein (z. B. sind für die Bildvorschau geringe Bildauflösungen ausreichend). *Note 2023-06-05 J.Watson: M.E. sollten Medien- und auch Wiederholfelder in einer Datenbank vermieden werden und stattdessen eine nachhaltigere technische Lösung fpr das Abbilden der entsprechenden Inhalte gesucht werden. Ein Beispiel ist [Field Desktop](https://field.idai.world/download).*


#### Structured Query Language (SQL)
*SQL ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt.*

Mit Hilfe von speziellen Datenbanksprachen kann ein Benutzer oder ein externes Programm über das DMBS mit einer Datenbank kommunizieren. Die am weitesten verbreitete Datenbanksprache im Bereich der relationalen Datenbanken ist SQL (structured query language). Sie wird rechnerunabhängig und produktübergreifend seit 1986 im ISO Standard 9075 definiert. Seitdem erfuhr SQL sieben Erweiterungen, von denen die letzte Aktualisierung 2011 als ISO/IEC 9075:2011 erschienen ist.

SQL-Befehle lassen sich in vier verschiedene Befehlsgruppen unterteilen:

| **Befehldgruppe**                | **Beschreibung**                                                                              | **Beispiel**                                                                                                                                                               |
| -------------------------------- | --------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Data Definition Language (DDL)   | Befehle zur Definition des Datenbankschemas: Erstellen von Datenbanken, Tabellen und Indizes. | Anlegen der Tabelle 'muenzen' mit beispielhaften Attributen unter Angabe des Datentyps : CREATE TABLE muenzen (PS_MuenzID serial NOT NULL, Nominal varchar, Gewicht float) |
| Data Query Language (DQL)        | Befehle zum Abfragen von Daten                                                                | Abfrage nach allen Münzen mit Fundort Paris (Paris entspricht Schlüssel 1 in der Tabelle muenzen): SELECT * FROM muenzen WHERE FS_FundortID = '1'                          |
| Data Manipulation Language (DML) | Befehle zur Datenmanipulation, also dem Ändern, Bearbeiten und Löschen von Datensätzen        | Ändern des Materials in Gold für den dritten Datensatz: UPDATE muenzen SET Material = 'Gold'  WHERE  PS_MuenzID = '3'                                                      |
| Data Control Language (DCL)      | Befehle zum Anlegen von Benutzern und zur Definition von Zugriffsrechten                      | Nutzers mit Passwort anlegen: CREATE USER mmustermann PASSWORD 'passwort'                                                                                                  |


### Entity-Relationship-Modell (ERM)

Ein wichtiges grafisches Hilfsmittel beim Entwurf und zur Dokumentation einer Datenbank ist das Entity-Relationship-Modell (ERM). Neben der grafischen Visualisierung mittels eines Entity-Relationship-Diagram (ERD) ist auch die tabellarische Erfassung und Beschreibung aller Entitätstypen, Beziehungstypen und Attribute für eine vollständige Dokumentation einer Datenbank notwendig. Das ERD ist ein beschriftetes Diagramm mit festgelegten Symbolen, das dazu dient, den gewünschten Ausschnitt der realen Welt formal zu beschreiben. Grundlage der ER-Modelle ist die Abstraktion von Objekten und deren Beziehungen untereinander. Folgende grundlegende Begriffe in einem ERM und deren grafische Wiedergabe in einem ERD werden in diesem Zusammenhang unterschieden:


| **Element**           | **Beschreibung**                                                                                                                         | **Grafische Darstellung**                                                                                                             |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Entität (Datensatz)   | Objekt der Wirklichkeit, materiell oder abstrakt, z. B. ein Fund "Münze XY", ein Befund "Pfostenloch 123" oder eine Abteilung "DAI Rom". | keine grafische Darstellung                                                                                                           |
| Entitätstyp (Tabelle) | Abstraktion gleichartiger Entitäten, z. B. Personen, Funde, Befunde, Adressen.                                                           | ![datenbanken_erdEntitaet-web](https://github.com/dainst/ianus-web-content/assets/29372760/6c4e0908-7bbe-463a-a630-15be0706e45d)      |
| Beziehung             | semantische Beziehung zwischen verschiedenen Datensätzen aus unterschiedlichen Tabellen, z. B. "Münze" in "Pfostenloch"                  | ![datenbanken_erdBeziehung-web](https://github.com/dainst/ianus-web-content/assets/29372760/0c753be7-09e2-4303-bb50-ed3c26aac138)     |
| Beziehungstyp         | Abstraktion gleichartiger Beziehungen, z. B. "gefunden in".                                                                              | ![datenbanken_erdBeziehungstyp-web](https://github.com/dainst/ianus-web-content/assets/29372760/a9f73789-c6ee-4acc-87bf-bb5a6890743c) |
| Kardinalität          | mögliche Anzahl der an einer Beziehung beteiligten Entitäten (s. u. Beziehungsarten); Symbol: 1, N oder M über Strich                    | ![datenbanken_erdKardinalitaet-web](https://github.com/dainst/ianus-web-content/assets/29372760/a8b01012-51df-41fb-8ef1-3e5b8f218855) |
| Attribut              | Eigenschaften eines Entitätstyps oder eines Beziehungstyps, z. B. Geburtsdatum von Personen.                                             | ![datenbanken_erdAttribut-web](https://github.com/dainst/ianus-web-content/assets/29372760/3a7807b4-ca88-492b-a9a2-904fb94b2e6e)      |
| Schlüssel             | Attribut/e, welche/s zur eindeutigen Identifizierung einer Entität von einem Entitätstypen dient/en.                                     | ![datenbanken_erdSchluessel-web](https://github.com/dainst/ianus-web-content/assets/29372760/88ce85ff-3fb1-4d40-9bb7-f01aa18f9c2f)    |


### Bestandteile einer Datenbank
Um eine Datenbank auch zukünftig nutzen und die in ihr erfassten Inhalte verstehen zu können, ist eine umfassende und vollständige Dokumentation erforderlich, zu der verschiedene Komponenten gehören:

* Die schriftliche und/oder tabellarische Anforderungsanalyse
* Die eigentlichen Datenbankinhalte
* Die Beschreibung der Datenstruktur
* Die Definition der implementierten Funktionalitäten
* Semantisch-inhaltliche Aspekte wir vorgegebene Wertelisten, Thesauri oder individuelle Definitionen von  Begriffen und Datensätzen
* Dokumentation der grafischen Benutzeroberflächen und verschiedenen Sichten auf die Daten (z.B.Eingabeformulare, Suchmasken, Ausgabeformate), technischen Schnittstellen und  erstellten Regelwerke (z.B. * Benutzerhandbücher)

Da mit keinem der empfohlenen Dateiformate alle Komponeneten erfasst und archiviert werden können, ist eine hybride Archivierungsstrategie erforderlich. Beispielsweise können der Inhalt, die Struktur und die Funktionalitäten einer Datenbank im SIARD-Format archiviert werden. Die Anforderungen werden schriftlich beschrieben und um ein grafisches Enitity-Relationship-Diagramm ergänzt. Individuelle Vorgaben zur Benutzung (insbesondere der Dateneingabe) werden mittels eines Benutzerhandbuches im Format PDF/A dokumentiert und die einzelnen Layoutmasken werden mittels Screenshots als unkomprimierte TIFF-Dateien gespeichert.

Die folgenden Tabelle gibt einen Überblick über die verschiedenen Formate für Datenbanken und welche davon für die langfristige Speicherung der genannten Dokumentationskomponenten  von Datenbanken geeignet sind.

Formate für Datenbanken und welche Elemente sie langfristig Speichern können. I = Datenbankinhalt, S =Datenbankstruktur, F = Funktionalitäten, B = Benutzung. Leere Zellen bedeuten fehlende Speichereigenschaften.

| **Format, Dokument**                           | **I** | **S** | **F** | **B** |
| ---------------------------------------------- | ----- | ----- | ----- | ----- |
| SIARD                                          | ✓     | ✓     | ✓     |       |
| SQL                                            | ✓     | ✓     | ✓     |       |
| XML                                            | ✓     | (✓)   |       |       |
| CSV                                            | ✓     |       |       |       |
| JSON                                           | ✓     |       |       |       |
| ERD (z. B. TIFF)                               |       |       | ✓     |       |
| Benutzerhandbuch (z. B. PDF/A)                 |       |       |       | ✓     |
| beschriebene Bildschirmfotos (z. B. TIFF)      |       |       |       | (✓)   |
| MDB, ACCDB, FP5, FP7, FMP12, ODB, DMP, BAK, DB |       |       |       | (✓)   |
 	    	 
Für den praktischen Umgang mit Datenbanken werden Hinweise gegeben, die einerseits Aspekte, die schon bei dem Entwurf der Datenbank berücksichtigt werden sollten, andererseits aber auch Empfehlungen für die tägliche Arbeit mit einer Datenbank thematisieren, wie etwa Dateneingabe, Exportmöglichkeiten, Speicherung und Sicherung sowie mehrsprachige Dateneingabe.

Es werden verschiedene DBMS und Administratorentools vorgestellt, mit denen sowohl Desktop- als auch serverbasierte Datenbanken erstellt und betrieben werden können. Für die Archivierung von Datenbanken werden Programme zur automatischen Analyse und Dokumentation der Datenbankstruktur vorgestellt. Auch für die Speicherung in SIARD und den Umgang mit diesem Format gibt es ein eigenes Toolkit. Für FileMaker- und MSAccess-Datenbanken gibt es gesonderte Hinweise.

### Datenbankentwurf

Der Datenbankentwurf bzw. das Datenbankschema hat einen großen Einfluss auf die Qualität einer Datenbank. Die richtige Strukturierung von Informationen vor der eigentlichen Eingabe von Daten stellt die Voraussetzung für eine langfristige, flexible und sinnvolle Verwendung einer Datenbank dar - vor allem dann, wenn sich im Laufe der Zeit die Anforderungen und Wünsche ändern

Der Entwurf von Datenbanken erfolgt idealerweise in folgenden Schritten:

* Anforderungsanalyse: Allgemeine Beschreibung des zukünftigen Systems in Rücksprache mit den Endanwendern, Sammlung der wissenschaftlichen und technischen Anforderungen, Definition der Eigenschaften der zu verarbeitenden Informationen, Festlegung der Arbeitsweise und Rechte der Benutzer, Einbindung von "Altbeständen" (alte Dokumentation, etc.) und Analyse der Häufigkeit verschiedener Abfragen und Eingaben
* Konzeptueller Entwurf: Erstellung eines softwareunabhängigen Datenbankschemas, welches sich als globale Sicht auf die Daten aus den Einzelsichten der jeweiligen Nutzergruppen zusammensetzt. Hierfür empfiehlt sich eine grafische Darstellung, z. B. als Entity-Relationship-Diagramm (ERD).
* Logischer Entwurf: Umsetzung des konzeptuellen Entwurfs auf ein gewähltes DBMS, z. B. durch Übertragung des ERD in einen Datenkatalog.
* Datendefinition: Konkrete Realisierung des logischen Entwurfs in einem DBMS, z.B. indem die im Datenkatalog festgelegten Spezifikationen in einer Datenbank-Software angelegt und gespeichert werden.
* Benutzerrechte: Festlegung, welcher Benutzer welche Daten in welcher Form sehen, bearbeiten, löschen, exportieren, drucken etc. darf.
* Dokumentation: Strukturiertes Festhalten des Datenbankentwurfes, der Attributdefinitionen, zulässiger Werte, Indizes, Layouts etc. und der dahinter stehenden Überlegungen.

Bei der Entscheidung, welche Eigenschaften eines realen Objektes durch welche Attribute einer Entität beschrieben werden, sollten folgende Punkte beachtet werden: Grundsätzlich sind die Eigenschaften (Attribute) eines Entitätstypes möglichst klein bzw. atomar zu halten (z. B. statt einem Attribut "Maßangaben" sind verschiedene Attribute wie "Höhe", "Breite", "Tiefe" etc. sinnvoller). Dies erleichtert präzise Abfragen und Berechnungen sowie den späteren Austausch der Daten mit anderen Systemen. Eine automatische Zusammenführung von Daten aus mehreren atomaren Attributen in ein einziges, umfangreicheres Attribut ist immer möglich -- der umgekehrte Weg, also eine automatische Aufteilung eines größeren Attributes auf viele kleinere, dagegen meist nicht. Dabei sollte bedacht werden, dass die Bearbeitungszeit eines Datensatzes mit der Anzahl der auszufüllenden Attribute wächst. Je nach Fragestellung und Anforderung muss ein ausgewogenes Verhältnis von Datenvielfalt (Vollständigkeit) und Effizienz gefunden werden.

Es wird dringend empfohlen, dass ein Datenbankentwurf vor dessen praktischer Umsetzung von einem Fachmann zur Informationsmodellierung nach inhaltlichen und formalen Kriterien (z. B. hinsichtlich Inkonsistenzen, Integritätsbedingungen, Redundanzen, Möglichkeiten der Verbesserung etc.) überprüft wird. In diesem Austausch sollte dann auch diskutiert werden, inwieweit ein vorhandenes Schema in die sog. erste bis fünfte Normalformen überführt werden kann oder nicht. Bei diesem Prozess der Normalisierung handelt es sich um ein in der Informatik entwickeltes Konzept zur Vermeidung von Anomalien der Datenbankinhalte und zur Beurteilung der Qualität eines relationalen Datenbankschemas, das allerdings ein vertieftes Verständnis zur Funktionsweise von DBMS voraussetzt.


### DBMS für Desktop-Datenbanken
Allen Desktop-Datenbankmanagementsystemen ist gemeinsam, dass eine gleichzeitige Nutzung durch mehrere Benutzer nur unzureichend möglich ist, weswegen diese nur für kleinere bis mittlere Datenbanken im lokalen Betrieb empfohlen werden können. In der Regel besteht auch die Möglichkeit ein Desktop-DBMS in einer Hybridlösung als Frontend zur Dateneingabe zu verwenden, während die Datenhaltung in einem serverbasierten DBMS erfolgt.

Sofern die Anforderung besteht, eine Datenbank für mehrere Benutzer betreiben zu wollen, sollte auf jeden Fall die Verwendung eines DBMS für eine Server-Datenbank in Betracht gezogen werden. Kann eine Server-Client-Architektur für mehrere Benutzer nicht realisiert werden und wird stattdessen parallel mit mehreren Desktop-Datenbanken gearbeitet, müssen gesonderte Vorkehrungen bei der Entwicklung der Datenbank getroffen werden und deren strikte Einhaltung gewährleistet werden, damit die Datenbankinhalte trotzdem konsistent bleiben (z. B. Vergabe individueller Nummernblöcke für einzelne Bearbeiter; Einschränkungen durch ein detailliertes Rechte-Management; regelmäßige Datenzusammenführungen, um frühzeitig Inkonsistenzen und Widersprüche im Datenbestand festzustellen).

**FileMaker Pro** ist ein kommerzielles DBMS für die Betriebssysteme Mac OS und Windows, das sich neben Microsoft Access zum Standardprogramm für Datenbanken auf Einzelplatzrechnern entwickelt hat. Charakteristisch ist seine einfache Benutzbarkeit, die es ermöglicht schnell Lösungen zu realisieren. Der Export der Datensätze in Standardformate (z. B. CSV, XML, XLS) ist gewährleistet, der Export der Datenbankstruktur ist mit FileMaker Advanced in den Formaten HTML oder XML möglich. Es gibt jedoch auch einige Schwächen wie die mangelnde Unterstützung von SQL und von Geodaten, erhöhte Anschaffungskosten und das Fehlen einer echten Programmiersprache.

**Microsoft Access** ist Bestandteil des Office-Professional-Pakets von Microsoft, das nur für das Windows-Betriebssystem angeboten wird. Alle Datenbankelemente, inkl. aller Elemente der Oberflächen als auch die Datenbanktabellen selbst, werden in einer einzigen Datei des proprietären MDB- bzw. ACCDB-Dateiformates abgespeichert. MS Access bietet im Vergleich zu FileMaker Pro weniger unterstützte Macros an, so dass umfangreiche Funktionen mit der Programmiersprache Visual Basic selbst entwickelt werden müssen. Dadurch können auch komplexe Aufgaben erstellt und individuelle Anpassungen vorgenommen werden, was bei FileMaker Pro mit den internen Script-Möglichkeiten nur eingeschränkt möglich ist. Nachteilig sind u.a. die Größenbegrenzung auf 2 GB und eine Instabilität bei größeren Anwendungen.

**OpenOffice** Base ist ein DBMS, welches im Office Paket von OpenOffice bzw. LibreOffice enthalten ist. Das in der Programmiersprache Java entwickelt Programm steht als Open Source zur Verfügung und kann daher ohne zusätzliche Kosten auf vielen unterschiedlichen Betriebssysteme installiert werden. Das Backend von Base wird mit Hilfe der sehr stabilen und robusten Datenbank HSQLDB betrieben, wobei das DBMS jedoch auch viele verschiedene Datenbanktreiber und Schnittstellen unterstützt. Gegenüber den kommerziellen Lösungen ist die Gestaltung der Oberflächen umständlicher und weniger umfangreich.

**SQLite** ist das weltweit am häufigsten verwendete DBMS, da es im Bereich von Android Smartphones und Browsern zum Speichern von Daten verwendet wird. Die Daten werden in einer einzigen SQLite Datenbank gespeichert. Mit Hilfe der GIS Erweiterung SpatiaLite lassen sich auch Geodaten verarbeiten. Es existiert keine Client-Server Architektur, weswegen das DBMS nur von einem Einzelbenutzer betrieben werden sollte.

* FileMaker Pro: http://www.filemaker.com/
* Microsoft Access: https://products.office.com/de-DE/access
* OpenOffice Base: https://www.openoffice.org/product/base.html
* SQLite: https://sqlite.org/

### DBMS für Server-Datenbanken
Serverbasierte Datenbankmanagementsysteme bilden die Grundlage für Datenbanken, die kollaborativ und webbasiert, z.B. über einen Internet-Browser, genutzt werden sollen. Anders als DBMS für Desktop-Datenbanken werden keine weiteren Möglichkeiten zur Gestaltung von grafischen Oberflächen (z.B. Eingabeformulare oder Listendarstellungen) bereitgestellt. Diese müssen mit Hilfe von Programmiersprachen (z.B. JavaScript, PHP oder Java) erstellt werden, was fundierte Software- und Informatikkenntnisse zur Entwicklung von Datenbankanwendungen voraussetzt. Insofern sind sie als Systeme für "schnelle Lösungen" ungeeignet, da in der Regel ein längerer Planungs- und Entwicklungszeitraum benötigt wird.

Gegenüber Desktop-Datenbanken, die u.U. parallel und technisch unabhängig voneinander betrieben werden, besitzen sie jedoch erhebliche Vorteile hinsichtlich einer konsistenten Datenhaltung. Der Betrieb eines Server DBMS in einer sogenannten Server-Client-Architektur ermöglicht es mehreren Benutzern, gleichzeitig auf den jeweils aktuellsten Datenbestand zuzugreifen. Bei einer parallelen Eingabe von Daten verschiedener Nutzer im selben Datensatz verhindert das DBMS, dass es zu Versionierungskonflikten oder Verletzungen von Integritätsbedingungen kommt und der Datenbestand inkonsistent wird.

**MySQL und PostgreSQL** sind weit verbreitete kostenlose Open-Source-DBMS, die sich in ihrem Funktionsumfang stark ähneln. Der wesentliche Unterschied ist, dass PostgreSQL mit der Erweiterung PostGIS in der Lage ist, geografische Daten adäquat zu speichern und zu verarbeiten, was für die Auswertung der Datenbankinhalte in einem Geografischen Informationssystem (GIS) entscheidend ist. Daneben besitzt PostgreSQL gegenüber MySQL eine höhere Konformität zum SQL-Standard, unterstützt JSON-Objekte, hat bessere Methoden zur Wahrung der Datenintegrität und umfangreichere Möglichkeiten zur Erstellung von internen Funktionen (sog. Stored Prozedures). Jedoch weist MySQL durch seine weitere Verbreitung eine höhere Unterstützung von Web Frameworks auf. Für Datenbankanwendungen in der Archäologie kann insbesondere PostgreSQL empfohlen werden. Ein umfangreicher Vergleich beider Systeme kann als Auswahlhilfe dienen. Für den Entwurf eines DMBS in MYSQL kann das frei verfügbare Tool DBDesigner 4 verwendet werden.

**Microsoft SQL Server und Oracle** sind kommerzielle, serverbasierte DBMS mit einem vergleichbaren Funktionsumfang. Im direkten Vergleich ist Microsoft SQL Server einfacher zu administrieren und billiger in den Anschaffungskosten, während Oracle die umfangreichsten Erweiterungs- und Anpassungsmöglichkeiten bietet, welche jedoch kaum einen praktischen Mehrwert für Datenbanken in den digitalen Geisteswissenschaften besitzen.

* MySQL: https://www.mysql.com/
* PostgreSQL: https://www.postgresql.org/
* Vergleich von MySQL, PostgreSQL und SSLite: [https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-post...](https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems)
* Microsoft SQL Server: https://www.microsoft.com/en-us/sql-server/sql-server-2016
* Oracle: https://www.oracle.com/database/index.html
* DBDesigner 4: http://fabforce.eu/dbdesigner4/

### Administration von Server-Datenbanken

Für alle genannten DBMS für Server-Datenbanken existieren grafische Administrationstools, mit deren Hilfe Anfragen an die Datenbank generiert werden können. Sie lassen sich nach Desktop- und webbasierten Anwendungen unterschieden sowie nach der Anzahl der unterstützten DBMS, da einige Tools entweder nur für ein spezifisches oder aber generisch für verschiedene DBMS geeignet sind.

Zu den empfehlenswerten Desktopanwendungen gehören die Tools pgAdmin3 (für PostgreSQL), MySQL Workbench (für MySQL), SQLite Database Browser (für SQLite), Oracle SQL Developer (für Oracle), SQL Server Management Studio (für Microsoft SQL Server) und SQuirrel SQL (u.a. für PostgreSQL, MySQL, Oracle, MicrosoftSQL, Microsoft Access). Webbasierte Administrationstools sind beispielsweise phpmyadmin (für MySQL), phppgadmin (für PostgreSQL) oder Adminer (für MySQL, PostgreSQL, SQLite, MS SQL und Oracle).

* pgAdmin3 <!--: https://www.pgadmin.org/MySQL Seite existiert nicht mehr -->
* Workbench: http://www.mysql.de/products/workbench/
* SQLite Database Browser: http://sqlitebrowser.org/
* Oracle SQL Developer: http://www.oracle.com/technetwork/developer-tools/sql-developer/
* SQL Server Management Studio: https://msdn.microsoft.com/de-de/library/mt238290.aspx
* phpmyadmin: https://www.phpmyadmin.net/
* phppgadmin: http://phppgadmin.sourceforge.net/
* Adminer: https://www.adminer.org/

### Dateneingabe und Datenqualität

Zentral für den Nutzen einer Datenbank ist, dass die semantische Definitionen jeder Entität, und jedes Attributes bekannt sind, d.h. den einzelnen Bearbeitern muss bewusst sein, welche Eigenschaften eines Objektes der realen Welt in welchem Eingabefeld gespeichert werden. Dies kann entweder durch eine externe Dokumentation, deskriptive Eingabeformulare (z.B. mittels Hilfefunktionen), Beispieldatensätze, vorgegebene Termini (z.B. Werte-/Codelisten, Thesauri, Vokabulare) oder technische Funktionen (z.B. Indizes, Autovervollständigungen) unterstützt werden. Innerhalb eines Projektes individuell definierte oder extern importierte Wörter und Begriffe sollten bereits im Verlauf des Datenbankentwurfs festgelegt werden, um eine semantisch saubere Trennung verschiedener Attribute zu gewährleisten.

Von Anfang an und insbesondere bei Mehrbenutzersystemen muss auf eine einheitliche Verwendung von Begriffen und eine möglichst vereinheitlichte Eingabe der einzelnen Werte geachtet werden. So sollte z. B. die gleiche Ansprache von Ortsnamen entweder abgesprochen und dokumentiert werden, durch einen entsprechenden Datenbankentwurf kontrolliert werden oder - im besten Falle - durch referenzierte Vokabular und Normdaten gewährleistet werden. Andernfalls kann es durch unterschiedliche Schreibweisen und Rechtschreibfehler beim Wiederauffinden von an sich gleichen Inhalten zu Problemen kommen. Hilfreich zur Verbesserung der Datenqualität sind Index-Funktionen, die viele DBMS anbieten, da mit ihnen in der Regel schnell erfasst werden kann, welche Werte bereits in ein Attribut eingetragen wurden, und dadurch fehlerhafte Einträge leicht identifiziert werden können.

Bei metrischen Eingaben muss frühzeitig die spätere Auswertung (z.B. statistische oder räumliche Analysen) im Auge behalten werden, da diese die Speicherung als numerische Datentypen, die einheitliche Verwendung einer Maßeinheit, die als Metadatum in der Attributbeschreibung hinterlegt werden sollte, oder den Umgang mit unscharfen bzw. unvollständigen Werten beeinflusst.

Um möglichst vollständige Suchergebnisse zu erhalten und eine höhere Vergleichbarkeit der eingegebenen Daten zu gewährleisten, kann es sinnvoll sein, bei Eigenschaften von Entitäten, die als Freitext-Attribute modelliert werden (z.B. ausführliche Beschreibungen), zusätzlich ein inhaltlich äquivalentes Attribut mit kontrolliertem Vokabular vorzusehen (z.B. Schlagworte, die zu der freien Beschreibung passen). Bei längeren Freitext-Attributen ist es zudem ratsam, eine inhaltliche Strukturierung vorzugeben, oder es sollte überlegt werden, diese Informationen auf mehrere separate Attribute aufzuteilen.

Wenn ein Attribut nicht ausgefüllt ist, kann es in manchen DBMS einen sog. NULL-Wert annehmen. Dieser entspricht keinem Datentyp und ist nicht mit der numerischen Ziffer 0 gleichzusetzen. Es ist ein symbolischer Wert, der aussagt, dass kein Wert vorhanden ist. Da in solchen Fällen jedoch üblicherweise unklar ist, ob das Feld vergessen, übersehen, nicht verstanden wurde, keine Angabe vorliegt oder erst später bearbeitet werden soll (sog. Nullwert-Problematik), kann eine Eingabe erfolgen, die diese Unklarheit beseitigt. Dafür können etwa bestimmte Zeichen reserviert werden, die sich von jedem anderen Wert in einer Datenbank unterscheiden, z.B.:
* Information zur Zeit unbekannt bzw. nicht relevant: NULL
* Information wird später nachgetragen: #
* Aussage derzeit nicht eindeutig möglich oder zu beantworten: ?


## Schnittstellen und Exportmöglichkeiten

Dient eine Datenbank u. a. als Arbeitsmittel zur strukturierten Erfassung von Daten, die in anderen Programmen weiterverarbeitet werden sollen, ist auf geeignete Exportformate zu achten. Oftmals kann die Entscheidung für oder gegen ein [DBMS](http://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.") davon abhängen, wie gut oder schlecht die Datenbankinhalte aus dem ursprünglichen System wieder herausgeholt und nachgenutzt werden können; ein Aspekt der insbesondere für die Langzeitarchivierung von besonders hoher Relevanz ist. Prinzipiell lassen sich drei Arten von Exportmöglichkeiten unterscheiden, die von den allermeisten [DBMS](http://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.") unterstützt werden:

* Export einfacher textbasierter Dateiformate wie [CSV](http://it-empfehlungen/glossar#CSV "(Comma Separated Values) ist ein textbasiertes Dateiformat für tabellarische Daten. Hierbei werden einzelne Zellen durch das ein bestimmtes Trennzeichen, z.B. durch ein Komma, voneinander getrennt. Jede Zeile einer CSV-Datei entspricht der Zeile einer Tabelle. Da das Trennzeichen auch als Inhalt der Zellen erlaubt ist, werden in diesem Fall zusätzlich Textbegrenzungszeichen (z.B. Anführungszeichen) vor und nach den Zellen eingefügt, falls das Trennzeichen auch als Wert innerhalb der Zelle verwendet wird. Ein De-facto-Standard für CSV-Dateien ist in RFC 4180 beschrieben.") oder [TSV](http://it-empfehlungen/glossar#TSV "(Tab-Separated Values) ist ein textbasiertes Dateiformat für tabellarische Daten. Hierbei werden einzelne Zellen durch das Tabulator-Zeichen (U+0009) voneinander getrennt. Jede Zeile einer TSV-Datei entspricht der Zeile einer Tabelle. Das Tabulator-Zeichen ist nicht als Inhalt der Zellen erlaubt. TSV ist ein Standard der IANA und ist als MIME-Type text/tab-separated-values registriert.")

* Export komplexer strukturierter Dateiformate wie [XML](http://it-empfehlungen/glossar#XML "(Extensible Markup Language) ist eine Auszeichnungssprache, die eine Teilmenge von SGML bildet und die Definition von eigenen Auszeichnungselementen erlaubt, um beliebige Strukturen annotieren zu können. De facto wurde SGML von der einfacher anwendbaren XML verdrängt. XML wird vom W3C gepflegt und entwickelt. Es bildet die Grundlage von vielen weiteren Dateiformaten wie ODT, DOCX, SVG etc. Für XML-Dateien gibt es als Alternative zu einer Dokumenttypdefinition (DTD) die Möglichkeit der Verwendung eines XML Schemas.") und JSON


* ODBC (Open Database Connectivity) und JDBC ([Java](http://it-empfehlungen/glossar#Java "bezeichnet sowohl die Programmiersprache Java als auch verschiedene Laufzeitumgebungen, die zur Ausführung von Java-Programmen dienen. Zahlreiche Anwendungen und Systeme verwenden die Java Technologie. Die Sprache Java ist eine auf Simplizität ausgelegte, sehr beliebte, plattformunabhängige Programmiersprache und ist aktuell durch die 8. Edition der Java Language Specification spezifiziert.") Database Connectivity) sind universelle Schnittstellen, welche den Zugriff auf und den Datenaustausch mit einer Datenbank ermöglichen.


## Speicherung und Sicherung

Da Datenbanken in den Altertumswissenschaften in der Regel statische Daten enthalten, die nach der initialen Eingabe und ggf. einer ersten Änderung kaum weiter modifiziert werden, sollte das Löschen von Datensätzen durch Sicherheitsabfragen und restriktive Zugriffsrechte abgesichert werden. Alle Veränderungen an dem Datenbankinhalt werden in der Regel immer sofort und ohne Interaktion mit dem Benutzer durch ein [DBMS](http://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.") gespeichert. Dies hat den Vorteile, dass ein ’manuelles’ Speichern entfällt, aber auch den Nachteile, dass alle Dateneingaben - also auch versehentlich falsche- sofort gültig und ohne eine Sicherung vorheriger Zustände nicht revidierbar sind. Daher ist das Anlegen von Sicherungskopien oder Datenexporten, insbesondere vor größeren Veränderungen des Datenbestandes, sehr zu empfehlen. Alternativ kann mit Hilfe einer Versionierung, die jegliche Zustände der Datenbankinhalte abspeichert und vor allem bei [Server](http://it-empfehlungen/glossar#Server "ist ein Programm oder Computer (Host), der in einem Netzwerk, wie beispielsweise im Internet, verschiedene Dienste und Ressourcen zur Verfügung stellt. Andere Programme oder Computer die auf den Server zugreifen werden Clients genannt.")-[DBMS](http://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus") gut konfiguriert werden kann, auch auf ältere Stände zurückgegriffen werden.


## Mehrsprachigkeit

Vor allem in internationalen Projekten besteht häufig die Anforderung, die Inhalte einer Datenbank mehrsprachig zu erfassen und auszuwerten. Eine technisch saubere Lösung, die die Inhalte in den verschiedenen Sprachen konsistent hält, ist nur mit relativ hohem Aufwand zu realisieren und muss sorgfältig geplant werden. Der Grad der Komplexität der Umsetzung hängt dabei auch davon ab, ob die Datenbank nur eine geringe und feste Anzahl von Sprachen (etwa nur zwei oder drei) oder prinzipiell beliebig viele unterstützen muss. Auf jeden Fall wirkt sich diese Anforderung auf den konzeptuellen und logischen Entwurf des Datenbankschemas aus.

Am einfachsten und unproblematischsten ist die Beschriftung der Benutzeroberflächen und Formulare (z. B. Überschriften, Bezeichnungen neben den Eingabefeldern, Hilfetexte) in verschiedenen Sprachen, da diese Elemente sich nicht auf die Datenbankinhalte selbst auswirken. Bei Attributen mit kontrolliertem Vokabular ist eine weitgehend automatische Übertragung in eine andere Sprache prinzipiell möglich, sofern Konkordanzlisten vorliegen. In diesen Fällen bietet sich die Benutzung internationaler Referenzsysteme an, bei denen Begriffe und Fachtermini bereits in verschiedenen Sprachen verwaltet werden, sowie im Wesentlichen auf abstrakte Konzepte - unabhängig von ihren sprachlich unterschiedlichen Bezeichnungen - verwiesen wird und die konkreten Wörter erst nach Auswahl einer Sprache durch den Datenbanknutzer nachgeladen werden.

Am schwierigsten und zeitaufwendigsten ist die Behandlung von mehrsprachigen Freitextfeldern. Entweder muss in diesem Fall für eine Eigenschaft eines Objektes mehrere sprachspezifische Attribute definiert werden (beispielsweise Beschreibung-deu, Beschreibung-eng) oder aber die Eingabe muss mit Hilfe von Hinweistexten, sogenannten Tags, annotiert werde (z.B. *&lt;de&gt;Der Avers zeigt den bekränzten Kopf von Nero nach rechts.&lt;de&gt;* *&lt;en&gt;Avers shows the wreath head of Nero facing to the right.&lt;en&gt;*) In beiden Varianten kann allerdings nicht gewährleistet werden, dass die Eingabe in der einen Sprache inhaltlich mit der Eingabe in der anderen Sprache tatsächlich übereinstimmt, was nur durch zusätzliche manuelle Kontrollen überprüft werden kann.


## Automatische Dokumentation der Datenbankstruktur


<!-- [SchemaSpyGUI Benutzeroberfläche zur automatischen Dokumentation der Datenbankstruktur](http://ianus-fdz.de/sites/default/files/styles/schmal/public/datenbanken_SchemaSpy_GUI.png)

*SchemaSpyGUI Benutzeroberfläche zur automatischen Dokumentation der Datenbankstruktur* Abbildung nicht auffindbar -->


Die Erfassung von [Metadaten](http://it-empfehlungen/glossar#Metadaten "sind Informationen über eine Datei oder ein Dokument. Sie umfassen sowohl technische (Dateiname, Dateigröße etc.) als auch inhaltliche Angaben, wie z.B. Schlagworte. Bei einem Foto beinhalten Metadaten beispielsweise Informationen über den Fotografen, die verwendete Ausrüstung, den Aufnahmeort etc.") zu einer Datenbank kann je ihrer Komplexität sehr aufwendig sein, wobei sich verschiedene Tools zur automatischen Dokumentation der Datenbankstruktur anbieten, von denen besonders das Tool SchemaSpy zu empfehlen ist. Neben der Möglichkeit, Befehle direkt über eine Kommandozeile einzugeben, existiert mit SchemaSpyGUI auch eine grafische Benutzeroberfläche (siehe Abbildungen).
Das Tool analysiert die Datenbank-[Metadaten](http://it-empfehlungen/glossar#Metadaten "sind Informationen über eine Datei oder ein Dokument. Sie umfassen sowohl technische (Dateiname, Dateigröße etc.) als auch inhaltliche Angaben, wie z.B. Schlagworte. Bei einem Foto beinhalten Metadaten beispielsweise Informationen über den Fotografen, die verwendete Ausrüstung, den Aufnahmeort etc.") verschiedener [DBMS](http://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.") wie OracleDB, MySQL, PostgreSQL und MySQL, und erstellt unter anderem ein [ERD](http://it-empfehlungen/glossar#ERD "(Entity Relationship Diagram) siehe ERM.") aus der vorhandenen Datenstruktur, listet die Eigenschaften der Tabellen auf und visualisiert die Beziehungen zwischen ihnen. Es bietet damit eine wertvolle Unterstützung bei der Dokumentation der Datenstruktur, ersetzt jedoch nicht die inhaltliche und semantische Beschreibung von Tabellen, Attributen, Wertelisten und Sichten.


<!-- [Beispiel einer Dokumentation der Tabelle library.book mit Hilfe von SchemaSpy](https://ianus-fdz.de/sites/default/files/datenbanken_SchemaSpy_Documentation.png)

*Beispiel einer Dokumentation der Tabelle library.book mit Hilfe von SchemaSpy* Abbildung nicht auffindbar -->


Ein weiteres Tool speziell für [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt.")-Datenbanken ist der kostenlose ExPEditor, das eine Beschreibung der Datenbank im docx-Format generiert.


* Schema Spy: [https://schemaspy.sourceforge.net/](http://schemaspy.sourceforge.net/)
  
* SchemaSpyGUI: [https://www.heise.de/download/product/schemaspygui-49350](http://www.heise.de/download/product/schemaspygui-49350)

* ExPEditor: [https://www.yury-iwtschenko.de/de/expeditor.html](http://www.yury-iwtschenko.de/de/expeditor.html)


## Access-Datenbanken dokumentieren

Microsoft Access bietet einige eingebaute Möglichkeiten, die die Erstellung einer Datenbank Dokumentation unterstützen.  Ausführlicher werden die Möglichkeiten auf AccessDatabaseTutorial.com, bei Microsoft oder bei access-im-unternehmen.de erläutert.

* Im Fenster Beziehungen (*Microsoft Access 2010 &gt; Datenbanktools &gt; Beziehungen*) sind alle Tabellen der Access Datenbank inklusive ihrer Beziehungen untereinander dargestellt. Es ist auch möglich dieses Beziehungsdiagramm als Beziehungsbericht zu exportieren. (*Microsoft Access 2010 &gt; Datenbanktools &gt; Beziehungen &gt; Entwurf &gt; Beziehungsbericht*)
  
* Der Databanken Dokumentierer (*Microsoft Access 2010 &gt; Datenbanktools &gt; Datenbankdokumentierer*) ermöglicht es automatisiert eine Dokumentation zu ausgewählten Objekten (Tabellen, Abfragen, Formularen, Berichten und Makros) zu erstellen. Das [Textdokument](https://it-empfehlungen/glossar#Textdokument "ist eine Datei, die neben darstellbaren Zeichen auch Formatierungsangaben und externe Medien enthält. Für Textdokumente gibt es spezielle Speicherformate wie DOCX oder ODT.") kann nach Word exportiert werden.

Das [Database Preservation Toolkit](https://database-preservation.com/) unterstützt MS Access. Damit lässt sich die Datenbank mit Hilfe von [SIARD](https://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.") archivieren. Mit [SIARD](http://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.") kann auch die Datenbankstruktur beschrieben werden. Es wird jedoch empfohlen, zusätzlich das Beziehungsdiagramm zu exportieren.


<!--* AccessDatabaseTutorial.com: [http://accessdatabasetutorial.com/2013/07/29/how-to-document-a-database-...](http://accessdatabasetutorial.com/2013/07/29/how-to-document-a-database-using-microsoft-access-tools-and-your-disciplines/">http://accessdatabasetutorial.com/2013/07/29/how-to-document-a-database-...) Seite existiert nicht mehr-->
  
* Anleitung von Microsoft: [https://support.microsoft.com/en-us](https://support.microsoft.com/en-us)
  
* Access im Unternehmen: [http://www.access-im-unternehmen.de/738](http://www.access-im-unternehmen.de/738)
  

## Datenbanken mit SIARD archivieren

Mit dem Format [SIARD](https://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.") in der Version 2 lassen sich Datenbanken unabhängig von dem verwendeten [DBMS](https://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.") sehr gut für die Archivierung vorbereiten. Die Erzeugung einer [SIARD](https://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.")-Datei erfolgt mit dem Database Preservation Toolkit, das per Kommandozeile bedient wird. Die [Software](http://it-empfehlungen/glossar#Software "meint Programme, die auf einer Hardware laufen, beziehungsweise deren Funktionalität erst herstellen. Dies kann beispielsweise das Betriebssystem auf einem Computer oder einer Totalstation sein. Es kann auch ganz speziell ein bestimmtes Programm gemeint sein, wie etwa das Programm zur Verarbeitung von Messdaten.") verbindet sich unter Angabe [DBMS](https://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.")-spezifischer Parameter mit einer laufenden Datenbank, extrahiert die Struktur inklusive aller Attribute, Metadaten, Skripte, sowie der Inhalte und transformiert alle Informationen in das [SIARD](https://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.")-Format. Umgekehrt ermöglicht das Toolkit auch die Umwandlung einer [SIARD](https://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.")-Datei imn ein anderes DBMS-Format. Eine Beschreibung der Benutzung des Tools wird ebenfalls bereit gestellt.


* Database Preservation Toolkit: [http://www.database-preservation.com/](http://www.database-preservation.com/)



## FileMaker-Datenbanken archivieren

Das [DBMS](https://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus.") FileMaker Pro wird von den genannten Tools nicht unterstützt, da die [Software](http://it-empfehlungen/glossar#Software "meint Programme, die auf einer Hardware laufen, beziehungsweise deren Funktionalität erst herstellen. Dies kann beispielsweise das Betriebssystem auf einem Computer oder einer Totalstation sein. Es kann auch ganz speziell ein bestimmtes Programm gemeint sein, wie etwa das Programm zur Verarbeitung von Messdaten.") anerkannte Standards, wie die Datenbanksprache [SQL](/it-empfehlungen/glossar#SQL "Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt."), nur eingeschränkt unterstützt. Daher muss bei der Archivierung und Dokumentation von FileMaker-Datenbanken ein individueller Ansatz gewählt werden, der hier skizziert wird.

Mit FileMaker Pro Advanced, einer erweiterten Version von FileMaker Pro, kann das [Datenbankschema](https://it-empfehlungen/glossar#Datenbankschema "ist Bestandteil eines Datenkatalogs. Es beschreibt formal die Struktur der Daten und legt in abstrahierter Form die Beziehung und Art der Speicherung von Einzelinformationen fest.") mit der Funktion "Datenbank-Design-Report" unter *Werkzeuge &gt; Datenbank-Design-Report* in [HTML](https://it-empfehlungen/glossar#HTML "Eine Hypertext Markup Language ist eine textbasierte Auszeichnungssprache, die Inhalte wie Texte, Bilder und Hyperlinks in Dokumenten strukturiert.") oder [XML](http://it-empfehlungen/glossar#XML "(Extensible Markup Language) ist eine Auszeichnungssprache, die eine Teilmenge von SGML bildet und die Definition von eigenen Auszeichnungselementen erlaubt, um beliebige Strukturen annotieren zu können. De facto wurde SGML von der einfacher anwendbaren XML verdrängt. XML wird vom W3C gepflegt und entwickelt. Es bildet die Grundlage von vielen weiteren Dateiformaten wie ODT, DOCX, SVG etc. Für XML-Dateien gibt es als Alternative zu einer Dokumenttypdefinition (DTD) die Möglichkeit der Verwendung eines XML Schemas.") dokumentiert werden. Die Funktion wird in der FileMaker Hilfe beschrieben.

Die Datenbankinhalte selbst lassen sich aus FileMaker Pro mit Hilfe von *Datei &gt; Datensätze exportieren...* unter Windows, bzw. *Ablage &gt; Datensätze exportieren...* unter MacOS im Format [XML](https://it-empfehlungen/glossar#XML "(Extensible Markup Language) ist eine Auszeichnungssprache, die eine Teilmenge von SGML bildet und die Definition von eigenen Auszeichnungselementen erlaubt, um beliebige Strukturen annotieren zu können. De facto wurde SGML von der einfacher anwendbaren XML verdrängt. XML wird vom W3C gepflegt und entwickelt. Es bildet die Grundlage von vielen weiteren Dateiformaten wie ODT, DOCX, SVG etc. Für XML-Dateien gibt es als Alternative zu einer Dokumenttypdefinition (DTD) die Möglichkeit der Verwendung eines XML Schemas.") exportieren, wobei als [XML](https://it-empfehlungen/glossar#XML "(Extensible Markup Language) ist eine Auszeichnungssprache, die eine Teilmenge von SGML bildet und die Definition von eigenen Auszeichnungselementen erlaubt, um beliebige Strukturen annotieren zu können. De facto wurde SGML von der einfacher anwendbaren XML verdrängt. XML wird vom W3C gepflegt und entwickelt. Es bildet die Grundlage von vielen weiteren Dateiformaten wie ODT, DOCX, SVG etc. Für XML-Dateien gibt es als Alternative zu einer Dokumenttypdefinition (DTD) die Möglichkeit der Verwendung eines XML Schemas.")-Grammatik *FMPDSORESULT* verwendet werden sollte, um die Lesbarkeit zu erhalten.  

<!-- <pre class=" true; codetag"> &lt;?xml version="1.0" <a href="/it-empfehlungen/glossar#encoding" title="siehe Zeichenkodierung." class="lexicon-term">encoding</a>="<a href="/it-empfehlungen/glossar#UTF" title="(Unicode Transformation Format) ist eine Menge von Zeichenkodierungen für den Unicode-Zeichensatz. Zu den häufigsten gehören dabei UTF-8 und UTF-16, die im Web und in verschiedenen Betriebssystemen eine große Verbreitung gefunden haben. Der Unterschied besteht dabei in der Zahl der pro Zeichen verwendeten Bytes. Eine Besonderheit von UTF-8 besteht darin, dass die Bytedarstellungen der ersten 128 Zeichen denen der 128 Zeichen des ASCII-Zeichensatzes entspricht. Weitere Varianten von UTF sind UTF-1, UTF-7 und UTF-32." class="lexicon-term">UTF</a> -->

<!--- 16"?&gt;    &lt;FMPReport creationTime="14:38:43" creationDate="08.12.2016"                       type="Summary" version="11.0v3"&gt;            &lt;File link=".//Bleibarren_Bohrkern.xml"\n                        name="Bleibarren_Bohrkern" path="134.95.117.58"&gt;\n                    &lt;BaseTables count="3"/&gt;\n                    &lt;Tables count="37"/&gt;\n                    &lt;Relationships count="35"/&gt;\n                    &lt;Accounts count="4"/&gt;\n                    &lt;Privileges count="4"/&gt;\n                    &lt;ExtendedPrivileges count="6"/&gt;\n                    &lt;FileAccess count="0"/&gt;\n                    &lt;Layouts count="1"/&gt;\n                    &lt;Scripts count="10"/&gt;\n                    &lt;ValueLists count="87"/&gt;\n                    &lt;CustomFunctions count="1"/&gt;\n                    &lt;FileReferences count="13"/&gt;\n                    &lt;CustomMenuSets count="2"/&gt;\n                    &lt;CustomMenus count="30"/&gt;\n            &lt;/File&gt; </pre>

Ausschnitt des Filemaker-Datenbank-Design-Berichts im [XML](http://it-empfehlungen/glossar#XML "(Extensible Markup Language) ist eine Auszeichnungssprache, die eine Teilmenge von SGML bildet und die Definition von eigenen Auszeichnungselementen erlaubt, um beliebige Strukturen annotieren zu können. De facto wurde SGML von der einfacher anwendbaren XML verdrängt. XML wird vom W3C gepflegt und entwickelt. Es bildet die Grundlage von vielen weiteren Dateiformaten wie ODT, DOCX, SVG etc. Für XML-Dateien gibt es als Alternative zu einer Dokumenttypdefinition (DTD) die Möglichkeit der Verwendung eines XML Schemas.")-Format     Zerschießt Layout von Seite --> 

Datenbank-Design-Report von Filemaker: [http://www.filemaker.com/de/help/html/fmpa_tools.24.5.html](http://www.filemaker.com/de/help/html/fmpa_tools.24.5.html)




T. Bossert -- U. Böttcher -- P. Teich, [SQL](http://it-empfehlungen/glossar#SQL "Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt.") -- Grundlagen und Datenbankdesign (Bodenheim 2010).

H. Eiteljorg, Archaeological Computing <sup>2</sup>(Bryn Mawr 2008) [http://archcomp.csanet.org/](http://archcomp.csanet.org/)

P. Kandzia -- H. J. Klein, Theoretische Grundlagen relationaler Datenbanksysteme. Reihe Informatik 79 (1993).

R. Elmasri -- S. B. Navathe. Fundamentals of Database Systems <sup>4</sup>(2004).

A. Kemper -- A. Eickler, Datenbanksysteme. Eine Einführung <sup>7</sup>(2009).


Koordinationsstelle für die dauerhafte Archivierung elektronischer Unterlagen (Hrsg.), Katalog archivischer Dateiformate: Datenbanken
[http://kost-ceco.ch/wiki/whelp/KaD/pages/Datenbanken.html](http://kost-ceco.ch/wiki/whelp/KaD/pages/Datenbanken.html)

Library of Congress (Hrsg.), Sustainability of Digital Formats. Planning for Library of Congress Collections. Format Descriptions for Dataset Formats (12.2016)
[http://www.digitalpreservation.gov/formats/fdd/dataset_fdd.shtml](http://www.digitalpreservation.gov/formats/fdd/dataset_fdd.shtml)

F. Schäfer -- K. Hofmann, Datenbankmanagementsysteme, in: DAI (Hrsg.), Leitfaden zur Anwendung von Informationstechniken der archäologischen Forschung. TEIL II Praxisratgeber (2011)
[http://www.ianus-fdz.de/it-empfehlungen/sites/default/files/ianusFiles/I...](http://www.ianus-fdz.de/it-empfehlungen/sites/default/files/ianusFiles/IT-Leitfaden_Teil2_v100_DAI.pdf)

R. Steiner, Grundkurs relationale Datenbanken. Einführung in die Praxis für Ausbildung, Studium und [IT](http://it-empfehlungen/glossar#IT "(Informationstechnologie) ein Oberbegriff für die Informations- und Datenverarbeitung sowie für die dafür benötigte Hard- und Software. Häufig wird auch die englisch ausgesprochene Abkürzung IT verwendet.")-Beruf <sup>7</sup>(Wiesbaden 2009).

P. Kleinschmidt -- Chr. Rank, Relationale Datenbanksysteme. Eine praktische Einführung <sup>3</sup>(Berlin 2005).

G. Lock, Using Computers in Archaeology (London 2003) 85-98.

D. Smith, Database fundamentals for archaeologists, in: S. Ross et al. (Hrsg.), Computing for Archaeologists (Oxford 1991) 111-125.


## Formatspezifikationen

* [SIARD](http://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.") 2.0: [http://www.ech.ch/vechweb/page?p=dossier&amp;documentNumber=eCH-0165&amp;documen...](http://www.ech.ch/vechweb/page?p=dossier&amp;documentNumber=eCH-0165&amp;documentVersion=2.0)


* [SIARD](http://it-empfehlungen/glossar#SIARD "(Software Independent Archiving of Relational Databases) ist ein vom schweizerischen Bundesarchiv entwickeltes Format, das im Projekt e-ARK weiterentwickelt wurde. Es beruht auf den ISO-Standards zu XML und SQL und dient als Archivformat für relationale Datenbanken. Es werden sowohl Datenbankstruktur als auch Datenbankinhalte gemeinsam beschrieben und archiviert. Der Standard ist offen und frei verfügbar.") 1.0: [https://www.bar.admin.ch/dam/bar/de/dokumente/kundeninformation/siard_fo...](https://www.bar.admin.ch/dam/bar/de/dokumente/kundeninformation/siard_formatbeschreibung.pdf.download.pdf/siard_formatbeschreibung.pdf)

* [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt."):2008 [ISO](http://it-empfehlungen/glossar#ISO/ "(International Organization for Standardization) eine internationale Vereinigung von Normungsorganisationen. Sie erarbeitet internationale Normen in allen Bereichen mit Ausnahme der Elektrik und der Elektronik, für die die Internationale elektrotechnische Kommission (IEC) zuständig ist, und mit Ausnahme der Telekommunikation, für die die Internationale Fernmeldeunion (ITU) zuständig ist.") 9075 [http://www.iso.org/iso/catalogue_detail.htm?csnumber=45498](http://www.iso.org/iso/catalogue_detail.htm?csnumber=45498)

* [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt."):2011 [ISO](http://it-empfehlungen/glossar#ISO/ "(International Organization for Standardization) eine internationale Vereinigung von Normungsorganisationen. Sie erarbeitet internationale Normen in allen Bereichen mit Ausnahme der Elektrik und der Elektronik, für die die Internationale elektrotechnische Kommission (IEC) zuständig ist, und mit Ausnahme der Telekommunikation, für die die Internationale Fernmeldeunion (ITU) zuständig ist.") 9075 [http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=53681](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=53681)


* Database Markup Language: [https://dbml.dbdiagram.io/home](https://dbml.dbdiagram.io/home)

* [XML](http://it-empfehlungen/glossar#XML "(Extensible Markup Language) ist eine Auszeichnungssprache, die eine Teilmenge von SGML bildet und die Definition von eigenen Auszeichnungselementen erlaubt, um beliebige Strukturen annotieren zu können. De facto wurde SGML von der einfacher anwendbaren XML verdrängt. XML wird vom W3C gepflegt und entwickelt. Es bildet die Grundlage von vielen weiteren Dateiformaten wie ODT, DOCX, SVG etc. Für XML-Dateien gibt es als Alternative zu einer Dokumenttypdefinition (DTD) die Möglichkeit der Verwendung eines XML Schemas."): [W3C](http://it-empfehlungen/glossar#W3C "(World Wide Web Consortium) ist das wichtigste Gremium zur Standardisierung des World Wide Web, das 1994 gegründet wurde. Das W3C entwickelt technische Spezifikationen und Richtlinien und stellt diese Vorgänge auch transparent auf deren Webseiten dar. http://www.w3.org/") [http://www.w3.org/TR/xml/](http://www.w3.org/TR/xml/)

* [CSV](http://it-empfehlungen/glossar#CSV "(Comma Separated Values) ist ein textbasiertes Dateiformat für tabellarische Daten. Hierbei werden einzelne Zellen durch das ein bestimmtes Trennzeichen, z.B. durch ein Komma, voneinander getrennt. Jede Zeile einer CSV-Datei entspricht der Zeile einer Tabelle. Da das Trennzeichen auch als Inhalt der Zellen erlaubt ist, werden in diesem Fall zusätzlich Textbegrenzungszeichen (z.B. Anführungszeichen) vor und nach den Zellen eingefügt, falls das Trennzeichen auch als Wert innerhalb der Zelle verwendet wird. Ein De-facto-Standard für CSV-Dateien ist in RFC 4180 beschrieben."): [RFC](http://it-empfehlungen/glossar#RFC "(Request for Comments) sind Dokumente in denen Methoden, Eingeschaften, Forschungen oder Innovationen im Zusammenhang mit dem Internet und der damit verbundenen Systeme veröffentlicht werden. Sie können als Richtlinien dienen oder werden sogar von der Internet Engineering Task Force zu Standards erhoben.") 4180 [https://tools.ietf.org/html/rfc4180](https://tools.ietf.org/html/rfc4180)
  
* JSON: [https://ecma-international.org/publications-and-standards/standards/ecma-404/](https://ecma-international.org/publications-and-standards/standards/ecma-404/)

* [ODB](http://it-empfehlungen/glossar#ODB "ist ein Teil von ODF zur Speicherung von Datenbanken. Es ist offen verfügbar und basiert auf XML."): [https://www.oasis-open.org/standards#opendocumentv1.2](https://www.oasis-open.org/standards#opendocumentv1.2)

* [ODB](http://it-empfehlungen/glossar#ODB "ist ein Teil von ODF zur Speicherung von Datenbanken. Es ist offen verfügbar und basiert auf XML."): [https://wiki.openoffice.org/wiki/FAQ_(Base)](https://wiki.openoffice.org/wiki/FAQ_(Base))
  

## Tools und Programme


* MySQL: [https://www.mysql.com/](https://www.mysql.com/)

* PostgreSQL: [https://www.postgresql.org/](https://www.postgresql.org/)

* Vergleich von [DBMS](http://it-empfehlungen/glossar#DBMS "(Datenbankmanagementsystem) ist die Verwaltungssoftware eines DBS über die der Nutzer auf die Datenbank zugreift. Es steuert die strukturierte Speicherung der Daten und führt alle lesenden und schreibenden Zugriffe auf die Datenbank aus."): [https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-post...](https://www.digitalocean.com/community/tutorials/sqlite-vs-mysql-vs-postgresql-a-comparison-of-relational-database-management-systems)

* Microsoft [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt.") [Server](it-empfehlungen/glossar#Server "ist ein Programm oder Computer (Host), der in einem Netzwerk, wie beispielsweise im Internet, verschiedene Dienste und Ressourcen zur Verfügung stellt. Andere Programme oder Computer die auf den Server zugreifen werden Clients genannt."): [https://www.microsoft.com/en-us/sql-server/sql-server-2016](https://www.microsoft.com/en-us/sql-server/sql-server-2016)

* Oracle: [https://www.oracle.com/database/index.html](https://www.oracle.com/database/index.html)

* FileMaker Pro: [http://www.filemaker.com/"](http://www.filemaker.com/)

* Microsoft Access: [https://products.office.com/de-DE/access](https://products.office.com/de-DE/access)

* OpenOffice Base: [https://www.openoffice.org/product/base.html](https://www.openoffice.org/product/base.html)

* SQLite: [https://sqlite.org/](https://sqlite.org/)

* pgAdmin3: [https://www.pgadmin.org/](https://www.pgadmin.org/)

* MySQL Workbench: [http://www.mysql.de/products/workbench/](http://www.mysql.de/products/workbench/)
  
* SQLite Database [Browser](http://sqlitebrowser.org/ "Ein Browser ist ein Computerprogramm zum Abrufen wie auch Darstellen von Dateien (HTML-Dokumente, PDF-Dateien, multimediale Inhalte). Ein Webbrowser dient speziell für die Darstellung von Dateien und ganzen Webanwendungen aus dem Internet und ist die Schnittstelle zwischen dem Nutzer und WWW"): [http://sqlitebrowser.org/](http://sqlitebrowser.org/)

* Oracle [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt.") Developer: [http://www.oracle.com/technetwork/developer-tools/sql-developer/](http://www.oracle.com/technetwork/developer-tools/sql-developer/)

* [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt.") [Server](http:///it-empfehlungen/glossar#Server "ist ein Programm oder Computer (Host), der in einem Netzwerk, wie beispielsweise im Internet, verschiedene Dienste und Ressourcen zur Verfügung stellt. Andere Programme oder Computer die auf den Server zugreifen werden Clients genannt.") Management Studio: [https://msdn.microsoft.com/de-de/library/mt238290.aspx](https://msdn.microsoft.com/de-de/library/mt238290.aspx)

* SQuirrel [SQL](http://it-empfehlungen/glossar#SQL "(Structured Query Language) ist eine Datenbanksprache zur Definition, Abfrage und Manipulation von Daten in relationalen Datenbanken. SQL ist unter ISO 9075 standardisiert und wird von fast allen gängigen Datenbanksystemen unterstützt."): [http://squirrel-sql.sourceforge.net/](http://squirrel-sql.sourceforge.net/)

* phpmyadmin: [https://www.phpmyadmin.net/](https://www.phpmyadmin.net/)

* phppgadmin: [http://phppgadmin.sourceforge.net](http://phppgadmin.sourceforge.net/)

* Adminer: [https://www.adminer.org/](https://www.adminer.org/)

* Schema Spy: [http://schemaspy.sourceforge.net/](http://schemaspy.sourceforge.net/)

* SchemaSpyGUI: [https://www.heise.de/download/product/schemaspygui-49350](https://www.heise.de/download/product/schemaspygui-49350)

* Database Preservation Toolkit: [http://www.database-preservation.com/](http://www.database-preservation.com/)

* Nutzung des Tools: [http://www.database-preservation.com/](http://www.database-preservation.com/)

* Datenbank-Design-Report von Filemaker: [http://www.filemaker.com/de/help/html/fmpa_tools.24.5.html](http://www.filemaker.com/de/help/html/fmpa_tools.24.5.html)


Haben Sie Anregungen, Änderungswünsche oder Ergänzungen zu dem Kapitel? Dann können Sie diese als Diskussionsbeitrag formulieren. Um die Funktion zu nutzen, ist eine Anmeldung erforderlich.

Bitte geben Sie möglichst genau an, worauf Sie sich beziehen. Das IANUS-Team prüft die Diskussionsbeträge regelmäßig und arbeitet diese bei Relevanz in die [FDM](http://it-empfehlungen/glossar#IT-Empfehlungen "(Informationstechnologie) ein Oberbegriff für die Informations- und Datenverarbeitung sowie für die dafür benötigte Hard- und Software. Häufig wird auch die englisch ausgesprochene Abkürzung IT verwendet.")-Empfehlungen ein.