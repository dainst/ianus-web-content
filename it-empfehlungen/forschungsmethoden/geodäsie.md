---
title: Geodäsie
sorting: it040101
authors:
  - heine.katja
  - kapp.ulrich
---

# Geodäsie

Alle Protokolle von Messungsrohdaten, mit Ergebnissen der Netzmessungen, der Ausgleichung und Festpunktkoordinaten inkl. Einmessungsskizzen müssen im ASCII-Format (TXT, CSV, DAT) gespeichert werden.

## Vermessungswesen

Es ist ja eine Binsenweisheit, dass archäologische und bauforscherische Tätigkeiten nicht ohne fundierte vermessungstechnische Basis- und begleitende Arbeiten auskommen. Die Zeiten, in denen man im 5X5 Meter Planquadrat seine Erkenntnisse sammelte, gehören zwar nicht der Vergangenheit an, aber die Bedingung ist, dieses Planquadrat in einen globalen Zusammenhang zu bringen. Die Vermessung bekommt in diesem Fall eine andere Bedeutung, die von der bloßen Herstellung von rechtwinkligen Quadranten abweicht. Andere Unterlagen wie Satelliten Images und Luftbilder sowie genaueres Kartenmaterial oder auch Unterlagen von z. B. geomagnetischen Prospektionen geben der Vermessung eine neue Wertigkeit.

Aber: der Einsatz elektronischer und satellitengestützter Geräte führt leider wie auch in der digitalen Fotografie zu einer fast unkontrollierbaren Anhäufung von Daten. Diese Ergebnisse müssen kurz-und langfristig verwaltbar sein. Aber dafür gibt es keine Ideallösung, weil die Entwicklungen im Gerätebau und den damit zusammenhängenden Programmen sich überschlagen, und was heute noch als Standard gilt, ist morgen schon überholt.

Meine Empfehlung: die Ergebnisse möglichst schnell auswerten, solange sie noch lesbar sind, denn nach wie vor ist eine Langzeitarchivierung von digitalen Daten nicht gesichert.

### Bezugssystem für Messdaten

Nach wie vor ist für viele archäologische Aktivitäten die Vermessungsgrundlage ein lokales Vermessungsnetz, das nicht in überörtliche oder gar in globale Systeme eingebunden ist. Für kleinere Messgebiete ist das legitim, solange sie nicht in einen Zusammenhang gebracht werden müssen.

Da das DAI aber in der Zwischenzeit viele Projekte mit großer räumlicher Ausdehnung bearbeitet, ist es sinnvoll, Messdaten in globalen Systemen zu erfassen, was durch die mittlerweile zur Verfügung stehenden Methoden und Geräte der Satelliten gestützten Vermessung deutlich vereinfacht wird. Durch die Einbeziehung von GPS-Messungen (Genauigkeit 5-10 m)) und Differential GPS-Messungen (Zentimetergenauigkeit) kann der räumliche Zusammenhang von verschiedenen Arbeitsplätzen hergestellt werden.

Als Voraussetzungen für globale Positionierungsbestimmungen mit cm-Genauigkeit muss entweder ein Punkt im globalen Koordinatensystem (im Umkreis von 10 km) bekannt sein oder die Möglichkeit der Einbindung eines Satellitenpositionierungs-services (z. B. EGNOS) bestehen. Eine hinreichende Genauigkeit kann auch erzielt werden, wenn auf einem Punkt im Messgebiet entsprechend lange Beobachtungszeiten registriert werden. Grundsätzlich sollten für die Anlage von Vermessungsnetzen im globalen Koordinatensystem mittels GPS Zweifrequenzempfänger benutzt werden. Alternativ können Einfrequenzempfänger mit langer Beobachtungszeit (mindestens 20 min) genutzt werden. Eine Netzauswertung sollte im Post Processing erfolgen. Für die Ermittlung von Höhen sind ein Referenzpunkt sowie ein Geoid-Modell notwendig.

### Geografisches System

Grundsätzlich sollte als geografisches Bezugssystem das System WGS 84 (World Geodetic System 84) gewählt werden. Dieses ist auch Bezugssystem für das Satellitennavigationssystem GPS und zukünftig auch für das europäische System Galileo. WGS 84 ist ein räumliches, globales, geozentrisches System mit den rechtwinkligen Koordinaten x,y,z oder wahlweise auch geografischen Koordinaten geografische Länge (longitude) L und geografische Breite (latitude) B (°,',''). Die Koordinaten lassen sich nach Bedarf in andere Koordinatensysteme transformieren.

### Geodätisches System

Für praktische Zwecke der Aufnahme mit der Totalstation und Darstellung von Objekten in Zeichnungen und Plänen, insbesondere für großmaßstäbige Darstellungen (großmaßstäbig bedeutet hier: großer Abbildungsmaßstab, demzufolge i.d.R. kleineres Gebiet) ist dieses räumliche System in ein Abbildungssystem (geodätisches Koordinatensystem, projected coordinate system) zu transformieren. Hierfür eignen sich insbesondere transversale Zylinderabbildungen wie die UTM-Abbildung (Universal Transversal Mercator projection). Mit der UTM-Abbildung können auch lokale Systeme realisiert werden, indem als Mittelmeridian (central meridian) ein durch das Aufnahmegebiet verlaufender Meridian (Längengrad) und als Maßstab der Wert 1,0000 festgelegt wird. Die Angabe der UTM-Koordinaten erfolgt als East (E)- und North (N) - Wert.

### Nationale Systeme

In vielen Ländern existieren ein oder mehrere amtliche Systeme, denen unterschiedliche Bezugsellipsoide (z.B. Hayford, Bessel, Krassowski o.a) mit unterschiedlichem Datum (Lagerung) und verschiedene Abbildungsmethoden (stereografisch, Lambert, Gauß-Krüger, UTM o.a.) zugrundeliegen. Sofern Ellipsoidparameter, Lagerung und Abbildungsverfahren bekannt sind, kann auch in diesen Systemen gearbeitet werden, da diese dann jederzeit in andere Systeme transformierbar sind. Sofern die Parameter nicht bekannt sind, ist zu empfehlen, ein eigenes System unter Verwendung des WGS 84 und der UTM-Abbildung (s.o.) zu wählen und bestehende Karten im unbekannten System über Passpunkte in das neue System zu integrieren.

Momentan verfügen die meisten europäischen Staaten und auch die meisten Bundesländer noch über eigene amtliche Systeme. Für die nächsten Jahre ist aber der Übergang zum einheitlichen System ETRS89 (European Terrestrial Reference System 89) geplant. ETRS89 basiert auf dem Ellipsoid GRS80 (für praktische Zwecke mit WGS 84 identisch) sowie der europäischen Lagerung ETRF (European Terrestrial Reference Frame) von 1989. Als Abbildungsverfahren wird die UTM-Abbildung mit 6° Streifenbreite und dem Maßstabsfaktor 0.9996 gewählt. Messungen in Deutschland sowie in den betroffenen europäischen Staaten sollten dann grundsätzlich ebenfalls in diesem System erfolgen, da die amtlichen Koordinaten für Festpunkte sowie Geobasisdaten dann ebenfalls in diesem System vorliegen.

### EPSG

International werden Bezugssysteme nach dem System der EPSG (European Petroleum Survey Group) angegeben. Die EPSG stellt die Parameter für die meisten Bezugssysteme bereit. Diese sind als Download auf den Webseiten der EPSG (www.epsg.io ) zu beziehen.

### Örtliche Systeme für die Bauforschung

In der Bauforschung ist auch ein objektbezogenes Koordinatensystem, welches beispielsweise parallel zur längsten Bauwerksachse ausgerichtet ist und einen beliebigen Koordinatenursprung besitzt, anwendbar. Dies ist für große und komplexe Bauwerke unter Umständen praktikabler als die Verwendung eines globalen Systems. Um die Messungen bzw. Pläne später in solch ein übergeordnetes System einhängen zu können, sollten mindestens drei Passpunkte bestimmt werden, deren Koordinaten sowohl im bauwerksbezogenen, als auch im globalen System (bestimmbar beispielsweise mittels GPS) bekannt sind.

## Einsatz von Hard- und Software in der Praxis

Da es eigentlich nur noch zwei wesentliche Hersteller von Vermessungsgeräten gibt - Leica und Trimble, die alle anderen Hersteller integriert haben - liegt der Entschluss, welches Gerät man wählt, eigentlich nur in der Beziehung, die zum Verkäufer besteht, denn preislich findet man die Unterschiede nicht mehr so groß. Auch die Handhabung ist nicht so unterschiedlich, da sie einem Schema folgt: Gerät aufbauen, Orientieren, Messen, Auslesen. Bei Neuanschaffungen sollte darauf geachtet werden, dass eine Systemreihe fortgeführt wird, wenn nicht zwingende Gründe dagegen sprechen, denn mit jedem Gerätesystemwechsel geht auch ein Softwarewechsel einher.

Eine Beschreibung der Handhabung der Geräte geht meistens aus der Gebrauchsanleitung hervor und würde den Rahmen dieses Leitfadens sprengen.

### Messungsdaten

Ich möchte hier nicht das Handaufmaß einbeziehen, sondern nur die elektronischen Messweisen mit Totalstation und GPS. Laserscan-Daten fallen beim DAI noch nicht an, da es noch kein eigenes Gerät gibt. Zum Handaufmaß gehören auch Daten, die mit Laser-Distomat gemessen, also nicht registriert, gespeichert werden.

Grundsätzlich muss man die eigentliche Vermessung von der Weiterverarbeitung im Computer trennen, da es für viele Vermessungsgeräte nach wie vor keine direkte Schnittstelle zum Computer gibt, sieht man von einigen Programmen ab, wie z.B. TachyCad als Aufsatz für AutoCad. Doch damit tauchen dann auch andere Probleme auf, die hardwaremäßig bedingt sind.

Sämtliche Vermessungsdaten der gängigen Totalstationen lassen sich mit den vom Hersteller des Geräts beigefügten Programmen in ASCII, TXT- oder DXF-Dateien in den Computer übertragen. Für die Weiterverarbeitung in CAD-Programmen bedarf es nun eines Transferprogramms, damit - besonders bei AutoCad - diese Daten erkannt und als Objekte behandelt werden können.

Es gibt einige Profi-Programme. Ich benutze seit Jahren BB-VermCad und bin, auch weil ich es gut kenne, damit zufrieden. Nur hat es, wie jedes Aufsatzprogramm den Nachteil, dass vorhandene Versionen nie kompatibel mit neueren Versionen von AutoCad sind, man also theoretisch mit jeder neueren Ausgabe von AutoCad auch eine neue Version von BB kaufen müsste; oder man behält die laufende Version - auch von AutoCad - zur Bearbeitung der Vermessungsdaten auf dem Rechner und lädt dann die erhaltenen Ergebnisse in die neue Version. Die Frage ist, ob man diese neuen Versionen braucht? Meine Antwort: leider ja, da viele Kollegen sich diesem Trend nicht ausschließen, und dann plötzlich Ergebnisse im Austausch nicht mehr kompatibel sind, weil sie mit verschiedenen Versionen abgespeichert wurden (down-kompatibel ist fast immer möglich, up-kompatibel fast nie!).

AutoCad, MicroStation, ArchiCad sind nur drei Programme, die mir im Laufe meines Arbeitslebens als Vermesser begegnet sind. Von diesen ist AutoCad am verbreitetsten, und zusätzliche Programme (BB, TachyCad) werden auch nur für ACAD gemacht. Auch "handgeschriebene" Programme beziehen sich fast nur auf ACAD, da AutoCad eine eigene Programmiersprache (AutoCad lisp (.lsp)), die relativ leicht zu erlernen sein soll, beinhaltet. Es ist nicht nur eine Sache des guten Geschmacks sondern auch eine Antwort auf die Frage: welches Programm benutzt mein Kollege, und der Kompromiss ist AutoCad.

Das einzige Austauschformat zwischen unterschiedlichen Programmen - .dxf - ist hier mit Vorsicht zu genießen, da es auch versionsabhängig ist. Häufig wird die gesamte .dxf-Datei nicht von einem anderen Programm vollständig gelesen, besonders bei 3D-Dateien kann es hier zu Irritationen führen.

Es gilt also, einen Standard aufzubauen, der sowohl Geräte als auch Computerprogramme einschließt.

### Netzmessungen

Eine dauerhafte Sicherung der Messungsrohdaten scheint nur für die Vermessung der Grundlagennetze sinnvoll. Dies gilt sowohl für terrestrische als auch für GPS-Messungen. Für jedes Projekt sollten die Festpunktkoordinaten und die Festpunktbeschreibungen inkl. der Einmessungsskizzen gespeichert werden.

### Objektpunkte

Ob es sinnvoll ist, die Koordinaten aller aufgemessenen Punkte dauerhaft zu sichern ist fraglich, denn entweder werden bei der Aufmessung alle relevanten Informationen zu einem Punkt mit eingegeben (was sehr aufwendig ist) und abgespeichert, oder es muss, um die Messung nachvollziehen zu können eine eindeutige Skizze (Feldriss) vorhanden sein, die dann ebenfalls dauerhaft (digitalisiert) gespeichert werden müsste.

Wenn eine dauerhafte Sicherung erfolgen soll, sollte dies im ASCII-Daten-Format (.txt, .dat, .csv o.ä.) erfolgen, da die meisten CAD-Programme diese in irgendeiner Form erkennen. Häufig müssen die Daten mit Zusatzprogrammen (s.o.) CAD-gerecht aufbereitet werden. Es gibt in diesem Fall auch keine Empfehlung, da die Programme nur bedingt kompatibel sind. Wie schon erwähnt, ist auch das .dxf-Format nur mit Vorsicht zu benutzen, EXCEL-Dateien müssen auch wieder in .txt-Dateien gespeichert werden, usw.

Man erreicht einen Standard nur dann, wenn alle Beteiligten die gleichen Programme der gleichen Version benutzen.

Um Zeichendateien, bei AutoCad .dwg auszutauschen, empfehle ich die Dateien in einer Version (2000, 2002) abzuspeichern, die ohne Schwierigkeiten und Verluste auch mit einer neueren Version zu öffnen ist. Die meisten 3D-Daten lassen sich so verlustfrei austauschen.

## Quellen

- Bauer, M.: Vermessung und Ortung mit Satelliten. Wichmann Verlag Heidelberg
- Schimke, A.: Kartenprojektionen und Koordinatentransformationen
- Zeiske, K.: Vermessen leicht gemacht. Leica Publikation
- Herrmann K.: Bautechnische Vermessung. Dümmlers Verlag Bonn
- Seckel/Hell/Schnuchel: Vermessungskunde und Bauaufnahme für Architekten. Herbert Wichmann Verlag Karlsruhe
- GPS Basics, Einführung in die GPS Vermessung, Leica Publikation
- Gebrauchsanweisungen für Geräte beinhalten häufig gute Ratschläge
- http://www.olanis.de/knowhow/mapprj/index.shtml
- www.epsg.org
