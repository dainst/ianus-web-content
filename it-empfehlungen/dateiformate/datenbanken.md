---
title: Datenbanken
sorting: it030106
webtoc: true
authors:
  - trognitz.martina
downloads:
  - checkliste-erstellung-datenbank
---

# Datenbanken

## Übersicht

Bitte beachten Sie, dass die Inhalte dieses Abschnittes den Inhalten des IT-Leitfadens des DAIs von 2011 entsprechen. Eine aktuellere Empfehlung können Sie den Guides to Good Practice des ADS entnehmen: http://guides.archaeologydataservice.ac.uk/g2gp/Gis_Toc

Für die Langzeitarchivierung von GIS-Daten ist derzeit noch kein allgemeingültiger Standard etabliert, weswegen auf die Vorgaben zu den in das GIS importierten Daten (z.B. Luftbilder, Geländemodell etc.) verwiesen wird. Es sollen jedoch möglichst keine programminternen Formate, die nicht von anderen GIS Systemen importiert werden können, genutzt werden. Bevorzugt werden sollen:

- Vektordaten als Esri Shapefile (shp + shx + dbf)
- Rasterdaten als Geo-Tiff

Die Haltung von Geodaten sollte vorzugsweise in Geodatenbanken erfolgen. Falls dies nicht möglich ist, müssen die Metadaten ausgefüllt werden. Folgende Informationen sind in der Geodatenbank / den Metadaten bereitzustellen:

- Datenquelle (z.B. SRTM, Tachymeter)
- Verarbeitung: Programm, Algorithmus, Parameter (z.B. QGIS , r.shaded.relief, altitude, azimuth etc.)
- Projektion (WGS 1984, EPSG: 4326)
- Datenqualität (Auflösung 90m, Ungenauigkeit)
- Information, was mit den Layern ausgedrückt wird, da es nicht immer aus dem Dateinamen hervorgeht (z.B. Höhenmodell)


## Vertiefung

### GIS in der Archäologie

Geographische Informationssysteme (GIS) dienen der Aufnahme, Verwaltung, Darstellung und Auswertung raumbezogener (Sach- und Geometrie-) Daten. In der Regel beschreibt der Terminus GIS die Gesamtheit eines GIS-Projektes, d.h. ein Gesamtsystem, das alle für die digitale, raumbezogene Arbeit erforderlichen Werkzeuge (Hardware, Software) und Daten (archäologische Basisdaten, geographisch - naturräumliche Daten) umfasst. Seltener beschränkt sich der Terminus GIS lediglich auf die Software mit der Aufnahme, Verwaltung, Darstellung und Auswertung raumbezogener Daten.

Den Datenbestand eines GIS könnte im Kern bereits eine digitale Liste mit Keramikfunden einer Ausgrabung bilden, unverzichtbar sind dabei Informationen zur Lage der Funde. Daraus lassen sich mit Hilfe von GIS-Software Karten erstellen, die verschiedene Informationen zu den Keramikfunden wiedergeben (Verbreitung der Verzierungsmotive, Typen, Menge der Scherben usw.). Viele Nutzer beschränken sich beim Gebrauch eines GIS auf die computergestützte Kartographie. Der entscheidende Vorteil eines GIS besteht aber in den darüber hinausgehenden vielfältigen Möglichkeiten der Datenanalyse. Derartige Analysen setzen in der Regel Berechnungen zum Raumbezug voraus, wie die Abstände zwischen den Funden, die Größe der ausgegrabenen Flächen oder der entsprechenden Ausgrabungsbefunde. Solche Daten lassen sich mit geringem Aufwand mit Hilfe eines GIS automatisch erheben und in Bezug zueinander setzen. Damit eröffnen sich neue Wege, die Verteilungen des Fundmaterials mit statistischen Methoden zu vergleichen, häufig werden hier Funddichteberechnungen durchgeführt, wie die Verteilung von Scherbenanzahl oder -gewicht.

### Maßstabsebenen

Die Aufnahme, Verwaltung, Darstellung und Analyse raumbezogener Daten mit einem GIS ist auf verschiedenen Maßstabsebenen archäologischer Arbeit sinnvoll. In diesem kurzen Ratgeber wird vor allem der Einsatz innerhalb einer Ausgrabung thematisiert. GIS-Anwendungen sind jedoch auch für die Auswertung größerer Landschaftsausschnitte attraktiv. Der Fundplatz, den man ausgräbt, ist eingebettet in eine Umgebung, die archäologisch teils durch frühere Arbeiten bekannt ist, teils durch eigene Oberflächenbegehungen weiter untersucht wird. Dies ist das Niveau von „Siedlungskammer“ oder „Schlüsselgebiet“. Die naturräumlich - geographischen Daten stehen auf diesem Niveau meist im Maßstab 1:25.000 oder 1:50.000 zur Verfügung. Die Größe solcher Mikro-Regionen beträgt typischerweise zwischen wenigen 10km2 und wenigen 100km2. Auf dieser Maßstabsebene ist es möglich, alle Nachbarplätze inklusive Fundstoff selbst zu überschauen und man kann Vollständigkeit anstreben.

Auf der nächst höheren Maßstabsebene, der der Regionalstudien, bewegt man sich in einer Größenordnung von wenigen 1.000km2. Wenn man die archäologischen Daten einer solchen Region selbst erfassen will, muss mit einem Arbeitsaufwand in der Größenordnung eines Dissertationsprojektes gerechnet werden. Bei Maßstäben ab 1:500.000 und einigen 10.000km2 oder gar größer muss man sich auf die Richtigkeit von Angaben aus der Literatur verlassen und es ist unmöglich, die Vollständigkeit des archäologischen Datensatzes zu gewährleisten.

Trotzdem ist auch die Betrachtung dieser Maßstabsebenen notwendig, denn Fragen zu kulturellen Diffusionsprozessen, zu Migrationen, zu Tausch und Handel, zur Mensch-Umwelt-Beziehung und auch zur Lage des selbst ausgegrabenen Fundplatzes in Bezug zu kulturellen Zentren sowie peripheren Regionen usw. sind nicht in Maßstabsebenen zu beantworten, die nur die Darstellung von wenigen 100km2 erlauben. GIS-Anwendungen erlauben theoretisch einen gleitenden Übergang von einer Skalenebene zur anderen. Die archäologischen Konsequenzen der eben beschriebenen, scheinbar trivialen Zusammenhänge steht in der Archäologie erst ganz am Anfang. Lösungen sind nur vom Einsatz derjenigen Rechenverfahren zu erwarten, die GIS-Programme mit anbieten und für die sich Archäologen bisher nur am Rande interessiert haben. Da man sich nicht darauf verlassen kann, dass auf einer Karte, die ein Gebiet von mehreren 10.000km2 Größe darstellt, alle archäologischen Fundpunkte vorhanden sind, muss man an dieser Stelle eben von der Punkt- zur Schraffurdarstellung übergehen. Allerdings sollte der schraffierte Bereich, in dem die meisten Fundpunkte liegen, nach nachvollziehbaren Kriterien bestimmt sein. Es liegen bereits Vorschläge vor, welche Methoden man zu diesem Zweck verwenden sollte.

Aber natürlich gewinnt auch der Einsatz von GIS auf Ausgrabungen eine zunehmende Bedeutung. Umso mehr, da mit höherer Komplexität der erhobenen Daten (Funde, Architekturbefunde, naturwissenschaftliche Daten) die Schwierigkeit wächst, diese Informationseinheiten in ihrer Gesamtheit zu erfassen und die vielfältigen Beziehungen zwischen ihnen auswerten zu können.
Datenmodell eines GIS

Man unterscheidet allgemein zwischen Sach- und Geometriedaten. Um beim Beispiel der Liste der Keramikfunde zu bleiben, handelt es sich bei diesen Informationen um Sachdaten. Aus Geometriedaten besteht der ins GIS eingebundene digitalisierte Grabungsplan. Er könnte beliebig viele geometrische Objekte enthalten, wie die Flächen von Häusern oder Pfostenlöcher.

Den Kern des GIS bilden die Sachdaten, die in unterschiedlich komplexen Datenbanken organisiert werden. Diese Sachdaten sind in Abhängigkeit von der archäologischen Fragestellung zu strukturieren. Unverzichtbar sind Informationen zur Lage der Funde. Das sind zumeist x,y-Koordinaten und Tiefenangaben, häufig aber auch Angaben des entsprechenden Quadranten mit der horizontalen Auflösung von 1x1m bei Nennung des jeweiligen Planums.

Geometriedaten stehen in zwei verschiedenen Klassen zur Verfügung. Man unterscheidet zwischen Vektor- und Rasterdaten. Vektordaten ermöglichen eine exakte Abbildung räumlicher Objekte, z. B. der Grenze einer Hausgrube oder einen Flusslauf. Jedes Objekt besteht dabei aus einer variablen Menge von Koordinatenpaaren, die gewissermaßen Knotenpunkte in diesem System darstellen. Die Knotenpunkte können zu beliebigen Strukturen kombiniert werden. Auf diese Weise lassen sich Punkte, Linienzüge oder Flächen abbilden. Die Kombination der Knotenpunkte zu Flächen oder zu Linien ergibt sich aus Zusatzinformationen. Ein Pfostenloch kann in einem Grabungsplan als Objekt dargestellt werden, das aus fünf oder mehr Knotenpunkten besteht. Die Zusatzinformationen beschreiben die Zusammengehörigkeit der Knotenpunkte und die Eigenschaft des Objektes als Fläche. Die Geometriedaten werden im GIS dann mit Sachdaten verknüpft. Für das Objekt Pfostenloch könnten dies Daten zur Höhe bzw. Tiefe der Unterkante des Pfostenloches sein oder Informationen zu dem hier vorgefundenen Keramikmaterial.

Rasterdaten bestehen aus nur einem geometrischen Grundelement - der Rasterzelle. Die in der Regel quadratischen Rasterzellen werden in Zeilen und Spalten angeordnet. Die Zellgröße bestimmt die Auflösung der so entstehenden Karte. Jeder Zelle wird dann ein Attributwert zugewiesen. Das häufigste Anwendungsbeispiel für eine Rasterdatei ist ein Digitales Geländemodell (DGM), in der jede Zelle die Information des Höhenwertes enthält. Am bekanntesten dürfte das weltweit kostenlos zur Verfügung stehende SRTM-Höhenmodell (Shuttle Radar Topography Mission ) aus dem Jahr 2000 mit einer Rastergröße von ca. 90x90m sein. In einer Rasterdatei lässt sich auch die Verteilung der Scherbenanzahl oder des Scherbengewichts in einer Grabungsfläche mit Rasterzellen von 1x1m Quadraten veranschaulichen.

In einem GIS-Projekt lassen sich je nach Fragestellung Raster- und Vektordaten integrieren. Für die Umwandlung von Rasterdaten in Vektordaten oder umgekehrt stehen dabei in den meisten GIS Standardwerkzeuge zur Verfügung. Dabei gilt es zu bedenken, dass Rasterdateien in der Regel größer sind als Vektordateien vergleichbarer Auflösung, sie bieten aber beim Verschneiden mit Hilfe von Basisrechenverfahren einige Vorteile.


## Praxis

### Einsatz von Hard- und Software in der Praxis

Die Software eines GIS setzt sich aus zwei Hauptbestandteilen zusammen. Erster Bestandteil ist ein Datenbankprogramm für die Verwaltung der Sachdaten. Häufig wird für diese Arbeit auf spezielle Datenbanksoftware zurückgegriffen (MS Access, FileMaker, MySQL). Den zweiten Teil bilden spezielle GISProgramme wie ArcView, Manifold, MapInfo, QunatumGIS, SAGA, gvSIG oder GRASS. Derartige Programme ermöglichen es, die Daten in ihrem räumlichen Bezug zu analysieren und deren Strukturen zu visualisieren. Die graphische Funktionalität der GIS-Programme, eröffnet für die Erstellung thematischer Karten vielfältige Möglichkeiten. Der große Vorteil von GIS-Programmen sind deren Werkzeuge zur Analyse raumbezogener Daten. Durch die Möglichkeiten der Visualisierung, der Herstellung von Karten, lassen sich viele Fragen auf eine empirische Weise verfolgen. Es ist es jedoch unverzichtbar, dass der Visualisierung eine Analyse folgt, mit der geprüft wird, inwieweit die herausgearbeiteten Unterschiede oder Gemeinsamkeiten bedeutsam sind. Die analytischen Werkzeuge ermöglichen einfache Abfragen, die Berechnung von Vektor- und Rasterflächen bis zu komplexen statistischen Operationen. Spezielle GIS-Programme enthalten daneben auch Bausteine, mit denen Datenbanken erstellt und verwaltet werden können. Meist wird man aber auf spezielle Datenbanksoftware zurückgreifen.

In der Praxis werden häufig Grabungszeichnungen in AutoCAD erzeugt und dann als DXF-Datei in das GIS importiert und mit den vorhandenen Sachdaten zusammengefügt. Ein weiteres klassisches Anwendungsbeispiel für ein vektorbasiertes GIS ist ein digitales Landschaftsmodell, in dem Straßen, Waldflächen, überbaute Flächen u.a. enthalten sind. Der Vorteil liegt darin, dass jedem dieser Objekte Zusatzinformationen zugewiesen werden können (Breite einer Straße, Belag, Steigung usw.).

Besondere Aufmerksamkeit ist bei der Planung von GIS-Vorhaben dem Einsatz der entsprechenden Software zu widmen. In den zurückliegenden Jahren sind leistungsfähige OpenSource-Programme entwickelt worden, die nahezu alle Anwendungsgebiete abdecken. Dabei ist zu bedenken, dass die hohen Kosten kommerzieller GIS-Software ihrem Einsatz bislang Grenzen gesetzt haben. An Universitäten stehen die Programme häufig nur in den PC-Pools der Rechenzentren oder aber auf einigen Rechner zur Verfügung. Für weit vernetzte, internationale Forschungsvorhaben ist dieser Umstand von erheblichen Nachteil. Eine besondere Empfehlung unter den neu aufkommenden leistungsfähigen OpenSource-Programme verdient die spanische GIS-Software gvSIG, die plattformübergreifend auf Windows-, Linux- und Mac-Bertriebssystemen eingesetzt werden kann.

Die eingesparten Kosten lassen sich zukünftig effektiver durch die gezielte Anpassung der Software an die spezifischen Projektanforderungen einsetzen oder aber für Schulungen.

### Ausgrabungen und GIS

Die ersten Anwendungen zur Digitalisierung von Grabungsdaten basierten auf der Konstruktionssoftware AutoCAD. Diese Versuche reichen bis in die frühen 90er Jahre zurück.

Die Vorzüge dieser Werkzeuge kamen bei der Herstellung und Vorlage digitaler Planzeichnungen zum Tragen. Nachteilig ist die umständliche Einbindung von Datenbanken und das weitgehende Fehlen von Werkzeugen für die Analyse von Raumstrukturen.

Die Vorzüge eines GIS bei der Durchführung und Auswertung einer Ausgrabung liegen auf der Hand. Nahezu alle auf einer Ausgrabung gewonnenen Informationen haben einen Raumbezug. Viele der Sachdaten sind in Datenbanken zu verwalten, wie Funddaten, Vermessungsdaten, Schichtbeschreibungen usw. Die Form, Ausdehnung und Lage der Befunde und Architekturreste lassen sich durch geometrische Daten eines GIS abbilden. Die reine graphische Dokumentation ist auch mit einer Software wie AutoCAD möglich, nur bieten derartige Programme standardmäßig keine Werkzeuge, mit denen sich bspw. Flächengrößen und Mittelpunkte von Flächenobjekten berechnen lassen. Das GIS eröffnet darüber hinaus die Möglichkeit Verteilungen zu vergleichen, Flächen zu verschneiden etc. Bliebe man bei der digitalen Umsetzung der konventionellen Grabungspläne, wäre ein Programm wie AutoCAD ausreichend. Folgerichtig wird AutoCAD bei Ausgrabungen da eingesetzt, wo das besondere Augenmerk auf der Dokumentation liegt. Bewährt haben sich speziell für AutoCAD entwickelte Werkzeuge, wie das Programm TachyCAD von der Firma Kubit oder das Programm ArchäoCAD der Firma ArcTron. Mit diesen Lösungen lassen sich mittels einer Totalstation auf Ausgrabungen Befunde einmessen. Computer und Totalstation sind auf der Grabung miteinander verbunden. Die Daten werden direkt ins AutoCAD eingelesen. Später lassen sich die Daten problemlos in ein GIS exportieren. Das gängige Austauschformat ist DXF/DWG.

Ein weiteres AutoCAD-Werkzeug der Firma Kubit ist Photoplan, mit dem sich Grabungsbefunde photogrammetrisch dokumentieren lassen. Diese Arbeitschritte ließen sich auch mit einer GIS-Lösung ohne AutoCAD realisieren. Nach unseren Erfahrungen sind diese Programmbestandteile jedoch nicht so anwenderfreundlich. In der Regel wird man bei der Wahl der Software nicht allein das nach den theoretischen Leistungsparametern beste Programm wählen, sondern diejenigen Programme bevorzugen, für die ein guter Ausbildungsstand vorhanden ist und kompetente Ansprechpartner für die Diskussion von Problemen zur Verfügung stehen. Zudem hat sich herausgestellt, dass keines der angebotenen GIS-Programme alle benötigten Rechenverfahren gleich oder in gleicher Anwenderfreundlichkeit zur Verfügung stellt. Häufig ist es daher - je nach Fragestellung - sinnvoll oder unumgänglich, dass verschiedene GIS-Programme zum Einsatz kommen. Den Vorzug sollten zukünftig mehr und mehr OpenSource-Lösungen erhalten.


## Quellen

Bill, R. , Grundlagen der Geo-Informationssysteme (Heidelberg 1999). Blankholm, H. P., Intrasite Spatial Analysis in Theory and Practice (Aarhus 1991).

Burrough, P. A. / R. A. McDonnel, Principles of Geographical Information Systems (Oxford 1999).

J. Conolly/M. Lake, Geographical Information Systems in Archaeology. Cambridge Manuals in Archaeology (Cambridge 2006).

Gaffney, V. / Z. Stancic GIS approaches to regional analysis: A case study of the island of Hvar (Ljubljana 1991).

Hietala, H. J. , Intrasite spatial analysis: a brief overview (Cambridge1984).

Hodder, I. / C. Orton (1976). Spatial Analysis in Archaeology. Cambridge, Cambridge University Press.

Kunow, J. / J. Müller Archäoprognose Brandenburg 1. Symposium Landschaftsarchäologie und geographische Informationssysteme. Prognosekarten, Besiedlungsdynamik und prähistorische Raumordnung (Wünsdorf 2003).

G. Lock/B. Leigh Molyneaux (Hrsg.), Confronting scale in archaeology (Berlin 2006).

Neteler, M., GRASS-Handbuch, Der praktische Leitfaden zum Geographischen Informationssystem GRASS. Hannover, Abteilung Physische Geographie und Landschaftsökologie am Geographischen Institut der Universität Hannover (Hannover 2000).

C. Orton, Sampling in Archaeology (Cambridge 2000).

Schier, W. (1992). Zum Einsatz multivariater Verfahren bei der Analyse des Lage- und Umweltbezugs prähistorischer Siedlungen. Archaeologische Information 15/1&2: 117-122.

Wheatley, D. and M. Gillings. Spatial Technology and Archaeology. The archaeological applications of GIS. (London / New York 2002 ).

Zimmermann, A., J. Richter, et al., Landschaftsarchäologie II - Überlegungen zu Prinzipien einer Landschaftsarchäologie. Bericht der Römisch-Germanischen Kommission 2004, 85: 37-95.

Preserving Geospatial Data:
http://www.dpconline.org/component/docman/doc_download/363-preserving-geospatial-data-by-guy-mcgarva-steve-morris-and-gred-greg-janee
http://www.dpconline.org/component/docman/doc_download/363-preserving-geospatial-data-by-guy-mcgarva-steve-morris-and-gred-greg-janee
http://www.gdi-de.org/

Weiteres:
http://web.stanford.edu/dept/SUL/library/prod//depts/gis/Archaeology.htm
http://oadigital.net/software/gvsigoade
http://www.fuerstensitze.de/1140_Publikationen.html
