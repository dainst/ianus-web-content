# Archivierung bei IANUS


Bitte beachten Sie **unbedingt** die nachfolgenden Informationen zu den akzeptierten Datenformaten (*ausklappbar*). Nicht jedes Dateiformat ist für die Langzeitarchivierung geeignet, weshalb dies ein zentrales Thema der IT-Empfehlungen ist. Nur in Ausnahmefällen können abweichende Dateiformate langzeitarchiviert werden und hier muss dies entsprechend in der preservation policy vermerkt werden sowie im Datenübergabevertrag. Bitte sprechen Sie mit uns in diesem Fall. Dies sind die gängigen Dateiformate und die Liste erhebt keinen Anspruch auf Vollständigkeit. 

### Präferierte und akzeptierte Dateiformate

<details><summary>PDF-Dokumente</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [PDF-Dokumente](https://ianus-fdz.de/it-empfehlungen/dateiformate/pdf-dokumente).
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
PDF/A-1 | .pdf   | präferiert  | -a oder -u
PDF/A-2 | .pdf   | präferiert  | -a oder -u
PDF/A-3 | .pdf   | akzeptiert  | -a oder -u; nach eingehender Prüfung
  
</details>

<details><summary>Text-Dokumente</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [Textdokumente](https://ianus-fdz.de/it-empfehlungen/dateiformate/textdokumente).
  Wichtig ist hier, dass eingebundene Inhalte ebenfalls erhalten werden können. Insbesondere bei eingebundenen Bildern, Formeln oder künstlerischen Grafiken ist dies zu beachten. 
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
Open Document Format| .odt   | präferiert  | 
Microsoft Office XML |	.docx |	präferiert |
Reiner Text, plain text	 |	.txt |	präferiert |
Strukturierter Text, Markup	 |	.xml, .sgml, .html etc. + .dtd, .xsd etc.	|	präferiert |
Rich Text Format	 |	.rtf	|	akzeptiert |
PDF/A | .pdf   | akzeptiert  | -a oder -u
  
</details>

<details><summary>Bilder und Rastergrafiken</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [Bilder – Rastergrafiken](https://ianus-fdz.de/it-empfehlungen/dateiformate/rastergrafiken).
  Wichtig ist hier, dass es sich um möglichst nicht komprimierte Formate handelt. Insbesondere proprietäre Kameraformate der Hersteller können nicht archiviert werden.
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
Baseline TIFF v. 6, unkomprimiert | .tiff, .tif   | präferiert  | 
Adobe Digital Negative |	.dng |	präferiert |
Portable Network Graphics |	.png |	akzeptiert | nur wenn ein TIFF nicht möglich oder sinnvoll ist (z. B. 3D-Modelle)
Joint Photographic Expert Group |	.jpeg, .jpg	|	akzeptiert | nur wenn ein TIFF nicht möglich oder sinnvoll ist 
JPEG2000 |	.jp2, .jpx	|	akzeptiert | nur wenn ein TIFF nicht möglich oder sinnvoll ist 
  
</details>

<details><summary>Tabellen und Datenbanken </summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [Tabellen](hhttps://ianus-fdz.de/it-empfehlungen/dateiformate/tabellen) und [Datenbanken](https://ianus-fdz.de/it-empfehlungen/dateiformate/datenbanken).
  Wichtig ist hier, die Datenentstehung und insbesondere alle Codes in den Metadaten zu vermerken. Alle Beziehungen zu den Daten sowie alle notwendigen Details für die Lesbarkeit der Daten sollten gut dokumentiert werden.
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
Delimited text  | .csv, .tsv, .tab, .txt  | präferiert  | 
SQL Datenbanken | .csv, .xml | präferiert  | 
No-SQL Datenbanken | .json, .xml  | präferiert  | 
Microsoft Office Open XML | .csv, .tsv, .tab, .txt  | akzeptiert  | 
LibreOffice and Apache OpenOffice  Calc  | .ods| akzeptiert  | 


Excel Tabellen (.xlsx oder auch .xls) genauso wie die Open- oder Libreoffice-Dateien können nicht allein langzeitarchiviert werden, da Informationen wie Markierungen oder Hervorhebungen oder auch in den Tabellen durchgeführte Berechnungen potentiell nicht mehr lesbar sind in 100+ Jahren. Es ist jedoch unter Umständen sinnvoll .xlsx oder auch .ods zusätzlich zu archivieren.
  
</details>

<details><summary>GIS-Daten</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [GIS](https://ianus-fdz.de/it-empfehlungen/dateiformate/gis).
  Wichtig ist hier, die Datenentstehung und insbesondere EPSG bzw. CRS in den Metadaten zu vermerken.
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
ESRI Shapefile | .shp + .shx + .dbf  | akzeptiert  | 
GeoJSON |	.geojson|	präferiert |
Geography Markup Language  |	.gml|	präferiert | 
Koordinaten / Rohdaten  |	.xyz, .csv/.tsv, .txt, .xml etc. |	präferiert | Alle Formate, die auch als Tabellen oder Datenbanken erhalten werden können.
Raster (GeoTIFF etc.) |	.tiff/.tif + .xml/.txt|	präferiert | Alle Formate, die auch als Bilder oder Koordinaten erhalten werden können. Textdokumente mit dokumentierten Bild-Koordinaten oder GPC sind ebenfalls möglich.
  
</details>

<details><summary>3D-Daten</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [3D und Virtual Reality](https://ianus-fdz.de/it-empfehlungen/dateiformate/3d).
  Wichtig ist hier Entscheidungen zu treffen, für welche Modelle auch die Originalbilder erhalten werden sollen. Proprietäre Formate der Hersteller können nicht archiviert werden.
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
Extensible 3D | .x3d + .tiff/.tif   | präferiert  | 
COLLAborative Design Activity (COLLADA) |	.dae + .tiff/.tif|	präferiert |
Wavefront OBJ |	.obj + .tiff/.tif|	präferiert | 
Polygon File Format |	.ply + .tiff/.tif	|	präferiert | 
ASCII Text File |	.txt |	präferiert | 
Raw XYZ|	.xyz, .txt etc. |	präferiert | 
  
</details>

<details><summary>Vector-Grafiken</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [Vektorgrafiken](https://ianus-fdz.de/it-empfehlungen/dateiformate/vektorgrafiken).
  Wichtig ist hier Entscheidungen zu treffen, für welche Modelle auch die Originalbilder erhalten werden sollen. Proprietäre Formate der Hersteller können nicht archiviert werden. Es ist sinnvoll, neben den reinen Daten, auch eine Ansichtsgestaltung zu erhalten, damit der orginale Kontext nicht verloren geht. Für CAD-Daten und Konstruktionszeichnungen werden mehrere Versionen der Datei erhalten. Für Details kann auch der Report ["Preserving CAD" aus der Data Types Series der Digital
Preservation Coalition](http://doi.org/10.7207/twgn21-15) konsultiert werden.
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
SVG | .svg + .tiff/.tif / + PDF/A + .dxf   | präferiert  | bei reinen Vektorzeichnungen ist ein .svg ausreichend, nur bei komplexeren Zeichnungen sind zusätzliche Details notwendig. Dies wird im Preservation Plan dokumentiert.
  
</details>
  
<details><summary>Audio und Video</summary>
  
  Details finden Sie in den IT-Empfehlungen im Kapitel [Audio](https://ianus-fdz.de/it-empfehlungen/dateiformate/audio) und [Video](https://ianus-fdz.de/it-empfehlungen/dateiformate/video).
  Wichtig ist hier, dass es sich bei den Dateiformaten für digitale Audiodateien um Containerformate handelt. Deshalb muss bei der Auswahl für die Langzeitarchivierung nicht nur ein passendes Format, sondern auch ein geeigneter Codec gefunden werden.
  
Format | Extension | Status | Kommentar
-------- | -------- | -------- | --------
Free Lossless Audio Codec | .flac | präferiert  | 
Waveform Audio File Format  | .wav | präferiert  | 
Broadcast Wave Format | .bwf | präferiert  | 
Matroska| .mkv | präferiert  | Für die Archivierung können die Codecs FFV1 für Video und FLAC für Audio empfohlen werden. Weitere geeignete Codecs für Matroska sind H.264/MPEG-4 AVC und MPEG-2.
MPEG1/2/4 | .mpeg/.mpg/MPEG4 .mp4 | präferiert  |
  
</details>
  
Sollten Sie Dateien in anderen Formaten vorliegen haben, kontaktieren Sie uns unter ianus-fdz@dainst.de. Für weitere Dateitypen finden Sie außerdem auf den Seiten des [ADS Anhaltspunkte](https://archaeologydataservice.ac.uk/help-guidance/instructions-for-depositors/files-and-metadata/) Hinweise.

## Archivierungsprozess
*Der Workflow wird aktuell angepasst. Stand: 2023-06-01. Die Anpassung wird vorraussichtlich mindestens bis Ende 2024 dauern. Bei Fragen kontaktieren Sie bitte ianus-fdz@dainst.de*

Im Folgenden können Sie sich zu den Übernahme- und Archivierungsprozessen bei IANUS informieren. Da die Daten und Informationen im Forschungsdatenzentrum professionell archiviert werden müssen, werden die Prozesse entsprechend dem [Open Archival Information System (OAIS)](http://nestor.sub.uni-goettingen.de/handbuch/artikel/nestor_handbuch_artikel_183.pdf) Referenzmodell umgesetzt. Dieser OAIS-Standard definiert **drei Informationspakete**, die nacheinander nach bestimmten Vorgaben prozessiert werden. Die Bezeichnungen der Informationspakete wurden aus diesem Standard übernommen:

- Einlieferungspaket = Submission Information Package - SIP
- Archivierungspaket = Archival Information Package - AIP
- Darstellungspaket = Dissemination Information Package - DIP 

### Datenübertragung der Forschungsdaten an IANUS

Nach der Registrierung im IANUS-Archivsystem kann der Datengeber seine initialen Metadaten der Datensammlung eingeben, die vom IANUS-Kurator geprüft werden. Passt die Datensammlung in die [Sammlungsstrategie](http://datenportal.ianus-fdz.de/resources/documents/Sammlungsstrategie.pdf) erfolgt nach Rückmeldung des IANUS-Kurators an den Datengeber die Freigabe des Datenuploads.

## Möglichkeiten der Datenübertragung

Der Transfer einer neuen Datensammlung an IANUS kann auf unterschiedliche Weise erfolgen:

- **Kleinere Datenmengen** können direkt mit Hilfe eines Upload-Formulars auf einen Server von IANUS kopiert werden. Dies bietet neben der zeitnahen Übertragung der Daten auch den Vorteil, dass eine automatisierte Überprüfung der akzeptierten Dateiformate erfolgen und dadurch schneller eine Rückmeldung gegeben werden kann. Zur Reduzierung der Übertragungszeit und von Übertragungsfehlern müssen die Dateien vor dem Upload in ein Containerformat verpackt und komprimiert werden 
- **Größere Datenmengen**, für die eine Online-Übertragung nicht mehr infrage kommen, müssen postalisch über externe Speichermedien (externe Festplatten, USBs, SD-Karten etc.) an IANUS geschickt werden, welche nach Überspielung auf die IANUS-Systeme an den Absender zurückgesandt werden.

Die Datenpakete, die an IANUS übertragen werden, heißen im Folgenden Transferpakete.

![transfer-workflow_UserView_2016-09-28_final](https://user-images.githubusercontent.com/29372760/226942569-3b277f6f-db9e-4c50-aab1-896defbce0f8.jpeg)
Flowchart des Transferprozesses bei IANUS © IANUS.

### Übernahmeprozesse bei IANUS

Während die Überprüfung der eingehenden Transferpakete (TP), also der hochgeladenen oder mit der Post verschickten Forschungsdaten, auf Schadsoftware und Viren sofort vorgenommen wird, erfolgen weitere Schritte der technischen und inhaltlichen Qualitätskontrolle erst, wenn alle Daten übertragen, die Metadaten vorliegen und der gesamte Vorgang des Datentransfers durch den Datengeber abgeschlossen wurde.

Sobald eine neue Datensammlung bei IANUS eingegangen ist und einem zuständigen Datenkurator zugewiesen wurde, werden folgende Schritte zur ersten Validierung der Datensammlung durchgeführt:

1. Verifizierung der angegebenen Kontaktdaten
2. Test der Lesbarkeit des Datenträgers und automatisiertes Öffnen aller Dateien, um korrupte und technisch defekte Dateien zu erkennen
3. Feststellung, ob eine oder mehrere Dateien einen Passwortschutz besitzen oder andere Zugriffsbeschränkungen aufweisen
4. Identifikation der technischen Dateiformate mit Hilfe des Werkzeuges Digital Record Object Identification (DROID)
5. Prüfung möglicher rechtlicher Probleme
6. Prüfung der Dateiformate im Hinblick auf die IANUS-spezifischen Vorgaben
7. Prüfung, ob eine ausreichende Dokumentation für die gesamte Datensammlung vorliegt (z. B. Liste der eingelieferten Dateien, Beschreibungen zu einzelnen Dateitypen) und ob die Daten sinnvoll strukturiert und benannt sind
8. Prüfung, ob die beschreibenden Metadaten inhaltlich verständlich sind und ob die Angaben mit den tatsächlichen Daten übereinstimmen (z. B. hinsichtlich Anzahl, Datenformaten, Aussagen zu Rechteinhabern) 

Zum Abschluss der initialen Validierung eines Transferpaketes informiert der IANUS-Datenkurator den Datengeber über das Ergebnis der Analyse, erstellt eine Prognose über den Aufwand und kommuniziert notwendige Verbesserungen.

### Erstellung eines Einlieferungspakets (SIP)

Abschließend sind Fragen zu Kuratierung und Bereitstellung der Daten zu klären, die zusammen mit einem Datengeber erörtert und entschieden werden müssen. Sie betreffen im Einzelnen folgende Aspekte:

- Festlegungen der Veröffentlichungsweise der Datensammlung über das Online-Datenportal, insbesondere Formulierung eines Kurztextes und Auswahl von geeigneten Abbildungen
- Beratung und Fixierung von Nutzungsrechten, Lizenzbestimmungen und Zugriffsbeschränkungen für die Nachnutzung
- Entwurf des Datenübergabevertrages

Mit diesen letzten Informationen kann der IANUS-Kurator alle verbleibenden Arbeiten zur Finalisierung eines gültigen Einlieferungspaktes ausführen, also

- alle Vereinbarungen und Entscheidungen dokumentieren
- relevante analoge Dokumente einscannen und der Datensammlung hinzufügen (z. B. Korrespondenz, Datenübergabevertrag, Lizenzverträge)
- alle Metadaten importieren
- ggf. originale Datenträger zurücksenden
- Sicherung des validen Einlieferungspakets auf lokalem Backup-Server
- alle Arbeitsschritte in einer PREMIS-Dokument protokollieren
- die Gegenprüfung des gesamten Prozesses durch einen zweiten Datenkurator

Das so erstellte Einlieferungspaket sollte nun alle zu archivierenden Originaldaten und Metadaten plus die für die Archivierung notwendigen Zusatzinformationen enthalten.

## Datenübergabevertrag

Für den Eingang einer neuen Datensammlung in den Archivbestand von IANUS ist die Unterzeichnung eines [Datenübergabevertrages](http://datenportal.ianus-fdz.de/resources/documents/Datenuebergabevertrag_annotiert.pdf) erforderlich. Die vertragliche Vereinbarung mit IANUS ist nicht-exklusiv, so dass der Rechteinhaber einerseits weiterhin über seine Daten unabhängig von IANUS verfügen kann und andererseits seine Daten auch an Dritte weitergeben kann.

# Aufbereitung der Daten durch IANUS

Während der Datenübertragungsphase (Ingest-Phase) werden aus dem validierten Einlieferungspaket alle digitalen Objekte und Metadaten extrahiert und in eine für die Langzeitarchivierung geeignete Form überführt. Am Ende liegt ein Archivpaket (Archival Information Package - AIP) vor, das zur Bitstream Preservation an ein vertragliches Rechenzentrum übertragen wird. Die erforderlichen Arbeitsschritte werden primär von den IANUS-Datenkuratoren ausgeführt, die durch das IANUS-Archiv-System unterstützt werden, das neben der Protokollierung aller Veränderungen an den Daten vor allem auch die automatisierbaren Aufgaben ausführt und den gesamten Prozess steuert. Die Prozesse werden nun erneut mit dem endgültigen, für die Archivierung und Bereitstellung vorgesehenen, Datenbestand durchgeführt und entsprechend vollständig dokumentiert. Für den Eingabeprozess wird davon ausgegangen, dass die Mitwirkung und Zuarbeit eines Datengebers nur noch bei neuen Problemsituationen oder in Zweifelsfällen erforderlich ist.

![PreIngest-workflow_UserView_2017-03-03_final](https://user-images.githubusercontent.com/29372760/226942833-a7b648ca-4a19-4ff5-a206-cfd4bc5f030f.jpeg)
Flowchart des Einlieferungsprozesses bei IANUS © IANUS

Vom Einlieferungsprozess (SIP) zum Archivpaket (AIP)

Zunächst werden eine aktuelle Dateiliste erstellt und die Verzeichnisstruktur vollständig als strukturelle Metadaten in der METS-Datei abgebildet. Dabei wird erneut für jede Datei mit Hilfe einer Hashfunktion (z. B. md5 oder SHA-3) eine Checksumme erzeugt, um im weiteren Verarbeitungsprozess ungewollte Fehler rasch ermitteln zu können. Außerdem wird jedem digitalen Objekt ein IANUS-interner Universal Unique Identifier (UUID) zugewiesen, damit Informationen ohne eine zentrale Koordination eindeutig aufgefunden und referenziert werden können. Für die interne, aber auch die externe, Ansprache der Datensammlung als Ganzes wird ein DOI als persistenter Identifikator reserviert und die hierfür erforderlichen Metadaten aus den bereits vorliegenden Informationen von dem IANUS-Datenkurator extrahiert. Sofern nicht bereits in der Übergabephase geschehen, werden nun Leer- und Sonderzeichen in Ordner- und Dateinamen nach festgelegten Regeln durch unproblematische Zeichen ersetzt, wobei der alte, unveränderte Datei- bzw. Ordnername in der PREMIS-Datei protokolliert wird.

Im nächsten Schritt werden alle formatspezifischen technischen Metadaten aus den digitalen Objekten ausgelesen, um auf dieser Basis über die weiteren Arbeitsschritte entscheiden zu können. Hierbei kommen verschiedene Tools und Webservices zum Einsatz, die im Bereich der digitalen Langzeitarchivierung weit verbreitet sind:

FITS (File Information Tool Set), das verschiedene Komponenten wie DROID, Apache TIKA, JHOVE, Exitfool, Metadata extration Tool beinhaltet.

Als Ergebnis der Formatidentifikation werden unter anderem sog. PRONOM Identifier geliefert, die nicht nur Auskunft über das erkannte Dateiformat selbst geben, sondern auch Informationen über die Version eines Dateiformates enthalten. Als zweiter Schritt ist eine Dateivalidierung notwendig, bei der geprüft wird, ob eine Datei tatsächlich der technischen Spezifikation für das identifizierte Format entspricht.

Anhand dieser technischen Angaben und der zuvor mit dem Datengeber vereinbarten zu erhaltenden Eigenschaften, legt ein Datenkurator nun die weitere Erhaltungsstrategie für eine Datensammlung fest und entwickelt einen Migrationsplan. Er wählt also die am besten für die Archivierung geeigneten Zielformate aus und entscheidet über die Frage, welche digitalen Objekte automatisiert nach den einheitlichen Standardregeln zur Formatmigration von IANUS prozessiert werden können und welche Dateien eine davon abweichende – insbesondere eine manuelle – Kuratierung benötigen, z. B. weil es sich um Spezialformate handelt, die von Tools nicht erkannt werden oder weil besondere signifikante Eigenschaften zu berücksichtigen sind. Egal welche Strategie angewandt wird, muss das Ergebnis teils automatisiert, teils manuell überprüft werden. Im Falle eines fehlerhaften Ergebnisses kann auf ein originales digitales Objekt, das in einem SIP unverändert enthalten ist, zurückgegriffen werden und es mit angepassten Parametern erneut verarbeitet werden.

Neben diesen formatbezogenen Aufgaben, die stärker die technischen Aspekte einer Datensammlung betreffen, ist während des Ingests die detaillierte Überprüfung aller inhaltlichen Informationen notwendig, damit eine fachlich sinnvolle Nachnutzung gewährleistet ist. Diese Qualitätssicherung muss überwiegend manuell durch einen Datenkurator geleistet werden, der die vorliegenden Metadaten und zugehörige Dokumente sowohl bezogen auf einzelne Dateien als auch auf die gesamte Datensammlung redigiert, ergänzt und standardisiert. Neben den fachspezifischen Erschließungsinformationen werden auch die übrigen Metadaten wie administrative und rechtliche sowie Angaben zur Provenienz eingehend geprüft und ggf. vervollständigt. Weiterhin werden Beziehungen und Referenzen zu anderen Ressourcen – sowohl innerhalb des IANUS-Archivbestandes als auch zu externen Quellen - geprüft oder neu angelegt und in den entsprechenden Abschnitten der METS-Datei festgehalten.

Je nach der Strukturierung der digitalen Objekte innerhalb einer Datensammlung kann es zudem notwendig sein, die Verzeichnisstruktur abzuändern und/oder Dateien umzubenennen. Es muss von Fall zu Fall entschieden werden, ob eine solche Anpassung eher zur Erhöhung der Archivierbarkeit oder eher zur Verbesserung der Nachnutzbarkeit dient, diese Arbeiten also bereits während des Ingest-Prozesses vorgenommen werden sollten oder erst später als Vorbereitung für die Bereitstellung sinnvoll sind.

![Ingest-workflow_UserView_2017-06-02_final](https://user-images.githubusercontent.com/29372760/226942736-ed922502-a667-4860-9cdb-9318acf04313.jpeg)
Flowchart des Archivierungsprozesses bei IANUS © IANUS

# Finalisierung des Archivpakets (AIP)

Die anschließenden Arbeitsschritte zur Finalisierung eines Achivpakets dienen vor allem der Qualitätssicherung des gesamten Kuratierungsprozesses und des Ergebnisses. Daher ist das neu entstandene Archivpaket auf seine Konsistenz und seine Authentizität hin zu überprüfen:

- Ist das Informationspaket in sich schlüssig und sind die zugehörigen Metadaten frei von Widersprüchen?
- Wurden alle Veränderungen nachvollziehbar dokumentiert, so dass sie zu einem späteren Zeitpunkt wiederholt bzw. rückgängig gemacht werden können?
- Sind die Urheber und der Zeitpunkt von Ergänzungen und Neuerungen lückenlos protokolliert?

Zur Beantwortung dieser Fragen dient das System IANUS.ingest, in dem kontinuierlich die Arbeitsschritte dokumentiert werden und das ggf. mit noch fehlenden Informationen zu vervollständigen ist. Zur Qualitätssicherung dient auch, dass ein 2. Datenkurator unabhängig von dem eigentlichen Bearbeiter einer Datensammlung das Einlieferungspaket als Ausgangsdatenbestand, das Ergebnis der Kuratierung als Archivpaket und die Dokumentation der Arbeitsschritte überprüft und die Korrektheit des gesamten Vorgangs bestätigt.

Die letzten Aufgaben ähneln der Finalisierung eines Einlieferungspakets, beinhalten also:

- die Komprimierung des AIPs in ein BagIt-Format zur schnelleren Datenübertragung
- die Übertragung des AIPs auf lokale Backup-Server
- die Übertragung an vertraglich festgelegte Rechenzentren zur bitstream preservation
- die Überprüfung der beiden Kopiervorgänge
- Import der finalen Metadaten in das System IANUS.data-management.

# Erstellung des Darstellungspakets (DIP)

Das Darstellungspaket wird automatisiert im Archivsystem von IANUS erstellt und wird für die Darstellung im Datenportal prozessiert. Hier werden alle Formate verwendet, die sich für eine schnelle Darstellung im Web eignen und nicht langzeitarchivierungsfähig sein müssen. Die bereits im SIP erfassten Projekt- und Dateimetadaten werden gemeinsam mit den Forschungsdaten im Datenportal angezeigt und können heruntergeladen werden.

IANUS Datenportal digitaler Forschungsdaten aus Archäologie & Altertumswissenschaften: http://datenportal.ianus-fdz.de/
