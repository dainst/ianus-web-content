---
title: Satellitenmessungen
sorting: it040105
webtoc: true
authors:
- reinhold.sabine
---

# Satellitenmessungen

## Einsatz von Hard- und Software in der Praxis

Auf allgemeiner Ebene sind momentan die unter GoogleEarth einsehbaren Satellitenbilder eine gute Alternative zu kommerziellen Satellitenbildern. Die bei GoogleEarth verwandten Bilder stammen aus verschiedenen Quellen und haben eine unterschiedliche Auflösung. Diese schwankt von 30-15m pro Pixel im Fall der auf Landsat-Aufnahmen basierenden Grundbilder bis zu einer Auflösung von etwa 1m pro Pixel bei Detailausschnitten. Diese Bilder stammen vom Satelliten Quickbird und werden laufend in GoogleEarth integriert. Es lohnt sich daher immer wieder die interessierende Region anzuschauen.

Eine Übersicht über die Quickbird-Aufnahmen sowie den Zeitpunkt der Aufnahme lässt sich unter Layers/DigitalGlobe Coverage im GoogleEarth Menü abrufen.

GoogleEarth hat den Nachteil, dass die Bilder nur in einer verhältnismäßig schlechten Auflösung abgespeichert werden können und sie nicht georeferenziert sind. Eine Lösung ist ein Upgrade auf GoogleEarthPlus. Dieses kostet 20\$ pro Jahr und erlaubt es, eine bessere Auflösung abzuspeichern und GPS-Daten sowie geographische Positionen können aus .CSV-Dateien importiert werden.

Für die Nutzung von georeferenzierten Satellitenbildern besteht die Möglichkeit, Bilder der Landsat Satelliten 4,5 und 7 im Internet frei zu laden. Die Daten des Satelliten Landsat ETM+ stammen aus dem Jahr 2000. Diejenigen von Landsat TM aus den 1990'er Jahren und die Bilder von Landsat MMS aus dem Zeitraum von 1972-1978.

BILD Aus: Eurimage Products and Services Guide

Um Bilder zu laden steuert man auf der Homepage landsat.org unter dem link 'Search for imagery' die freien LandsatOrtho Daten an. Mit dem dort vorgegebenen Path-Row Finder kann man die entsprechenden Angaben zur interessierenden Region über ein interaktives Kartenmodul ermitteln. Wichtig ist es dazu den Popublocker (Internetexplorer: Extra/Popupblocker; Firefox: Extras-Einstellungen-Inhalt/Pop-up-Fenster blockieren) zu deaktivieren. Wichtig ist auch im Suchmodus die Kästchen WRS I und WRS II anzukreuzen und refresh map zu aktivieren. Nur so lassen sich dann mit dem Informations-Tool die entsprechenden Flugbahndaten ermitteln. Eine alternative Suchmöglichkeit bietet sich unter: https://www.usgs.gov/landsat-missions/landsat-shapefiles-and-kml-files. Dort sind ESRI-shp files herunter zu laden, die ebenfalls Path/Row Informationen enthalten.

Hat man die Angaben lassen sich bei https://landsat.gsfc.nasa.gov/ die entsprechenden Daten ansteuern und kopieren. Die gezippten Daten müssen dann entzippt werden und man erhält verschiedene Datensätze im Format Geo-Tiff. Diese sind georeferenziert im System WGS 1984.

Die Auflösung der Landsat Bilder ist unterschiedlich und liegt bei 30m bzw. 15m per Pixel.

BILD Aus: Eurimage Products and Services Guide

Für detailliertere Satellitenbilder mit hoher Auflösung stehen momentan nur kommerzielle Anbieter zur Verfügung. Dort können georeferenzierte Bilder mit einer Auflösung bis unter 1m pro Pixel erworben werden. Die folgende Tabelle gibt einen Überblick über die vorhandenen Systeme und die Quellen, über die Bildausschnitte und Preisinformationen zu erhalten sind.

### Fotografische Sensoren

#### CORONA

Satellitenaufnahmen aus den 1960er und frühen 1970er Jahren der amerikanischen Spionagesatelliten CORONA, LANYARD und ARGON. CORONA Bilder der Missionen KH4 und 6 haben eine Auflösung von 2-3m. Es empfiehlt sich die Angaben in den Missionsdokumentationen zu lesen. Und Bilder in 7 Micron scannen zu lassen. Nicht georeferenziert!

<!-- Allgemeine Angaben finden sich unter: http://edc.usgs.gov/products/satellite/declass1.html#description Seite existiert nicht mehr
Bildauswahl unter: http://edcsns17.cr.usgs.gov/EarthExplorer/ dort finden sich die CORONA Bilder unter der Angabe "declassified images". Preis (2007): 30$ pro Filmstreifen (die DVD ist jedoch recht teuer) http://edcsns17.cr.usgs.gov/helpdocs/prices.html#CORONA Seiten existieren nicht mehr --> 

#### KFA-1000

Der russische Spionagesatellit KFA-1000 hat eine Auflösung von 1.5-3m. Die Bilder Stammen aus den 1990er Jahren. Nicht georeferenziert!

Übersichtskarten und Bildauswahl sind erhältlich über http://www.sovinformsputnik.com/

### Digitale Sensoren

#### LANDSAT

Amerikanische Multispektral-Satelliten, die seit 1972 aktiv sind. Die LANDSATs 1-3 hatten einen Multispektral Sensor (MSS) mit einer Auflösung von 80m. Die LANDSATs 4 and 5 haben MSS und Themaic Mapper (TM) Sensoren mit einer Auflösung von 30 oder 15m.

Übersicht bei https://landsat.gsfc.nasa.gov/. <!-- Kommerzielle Anbieter sind u.a. http://www.eurimage.com/index.html oder http://www.digitalglobe.com/ Preise (2007) ab 250 EURO http://www.eurimage.com/products/docs/eurimage_price_list.pdf nicht mehr aktuell-->

#### SPOT

SPOT. Französische Satelliten mit Multispektral (XS) Sensoren und einer Auflösung von 20m bis 10m.

<!-- Bilder und Preisangaben bei http://www.spotimage.fr/html/_.php Seite existiert nicht mehr--> 

#### IKONOS 2

Satellit mit hochauflösenden Kameras, die Graustufen- und Farbbilder aufnehmen. Jedes Bild bildet eine Fläche von mindestens 11 x 11 km mit einer Auflösung von bis zu 0,82m ab. Es können auch Flächen von 60 x 60 km in einem Überflug aufgenommen werden können.

Bilder und Preisangaben bei http://www.euspaceimaging.com/ Preis ca. 30$ pro qkm

#### QuickBird

QuickBird 2 ist ein kommerzieller Satellit zur Erdbeobachtung. Er wird von DigitalGlobe betrieben. Er hat eine Auflösung von 0,6m. Die Detailbilder in GoogleEarth sind Quickbirdaufnahmen seit 2001.

Bilder und Preisangaben bei http://www.digitalglobe.com/ oder http://www.eurimage.com/index.html Preis 16-41 $ pro qkm (mindestens 272 qkm)

## Quellen

<!-- - http://www.dainst.org/medien/de/Nasca-BMBF_Programm.pdf Seite existiert nicht mehr -->
- David L. Kennedy, Declassified satellite photographs and archaeology in the Middle East: case studies from Turkey. Antiquity 72, Nr. 277 1998, 553-561.
- Graham Philip/Daniel Donoghue/Anthony Beck/N. Galiatsatos, CORONA satellite photography: an archaeological application from the Middle East. Antiquity 76, Nr. 291 2002, 109-118.
- Jason Ur, CORONA satellite photography and ancient road networks: A Northern Mesopotamina case study. Antiquity 77, Nr. 295 2003, 102-105.
- Wouter Gheyle/Raf Trommelmans/Jean Bourgeois/Rudi Goosens/Ignace Bourgeois/Alain De Wulf/Tom Wilkens, Evaluation CORONA: A case study in the Altai Republic (South Siberia). Antiquity 78, Nr. 300 2004, 391-403.
- M. Altaweel, The use of ASTER satellite imagery in archaeological contexts. Archaeological Prospection 12, 2005, 151-166.
- K.N. Wilkinson/Anthony Beck/Graham Philip, Satellite imagery as a resource in the prospection for archaeological sites in central Syria. Geoarchaeology 21, 2003, 735-750.
- Anthony Beck/Graham Philip/Maamun Abdulkarim/Daniel Donoghue, Evaluation of CORONA and IKONOS high resolution satellite imagery for archaeological prospection in western Syria. Antiquity 81, Nr. 311 2007, 176-190.
