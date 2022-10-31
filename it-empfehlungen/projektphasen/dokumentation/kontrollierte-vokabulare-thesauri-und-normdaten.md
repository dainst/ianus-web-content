---
title: Kontrollierte Vokabulare, Thesauri und Normdaten
sorting: it020203
authors:
  - bibby.david
  - gerth.philipp
  - heinrich.maurice
  - jahn.sabine
  - ludwig.bernhard
  - posluschny.axel
  - siegloff.eicke
  - sieverling.anne
  - trognitz.martina
downloads:
  - readme-vorlage
  - fundliste-vorlage-pdf
  - fundliste-vorlage-excel
  - befundliste-vorlage-pdf
  - befundliste-vorlage-excel
  - probenverzeichnis-vorlage-pdf
  - probenverzeichnis-vorlage-excel
  - restaurierungsverzeichnis-vorlage-pdf
  - restaurierungsverzeichnis-vorlage-excel
  - geraeteliste-vorlage-pdf
  - geraeteliste-vorlage-excel
  - zeichnungsverzeichnis-vorlage-pdf
  - zeichnungsverzeichnis-vorlage-excel
  - fotoliste-vorlage-pdf
  - fotoliste-vorlage-excel
---

# Kontrollierte Vokabulare, Thesauri und Normdaten

Damit Metadaten möglichst sinnvoll genutzt und maschinell verarbeitet werden können, sollten neben klar definierten Metadatenschemata auch möglichst einheitliche Begriffe und homogene Beschreibungen verwendet werden. Nur wenn gleiche Dinge auch mit den gleichen Begriffen benannt werden, ist es möglich vollständige und präzise Suchergebnisse zu erhalten oder vergleichbare Daten richtig miteinander zu verknüpfen. Die Vorgabe und Definition von festen Begriffen und Regeln hilft zudem, Mehrdeutigkeiten und Redundanzen zu vermeiden, etwa wenn eine Zeichenkette verschiedene Bedeutungen besitzen kann (z. B. Abakus als Rechenhilfsmittel oder als architektonischer Abschluss eines Kapitells), ein identischer Sachverhalt durch unterschiedliche Worte erfasst werden kann (z. B. Survey und Oberflächenbegehung) oder die Form der Angabe variieren kann (z. B. ein Datum in der Form 12.03.2012 oder 2012-03-12).  
  
Das geeignete Mittel zur Vereinheitlichung der sprachlichen Vielfalt sind sogenannte kontrollierte oder normierte Vokabulare, die entweder einfache Wortlisten oder strukturierte Thesauri sein können, in denen Wörter zusammen mit ihrem semantischen Kontext verwaltet werden. Diese "terminologische Kontrolle" kann in unterschiedlicher Weise systematisiert und implementiert sein.

Beispielsweise können innerhalb eines Projektes alle zu verwendenden Begriffe unter allen Beteiligten abgestimmt, klar fachlich definiert, voneinander abgegrenzt und in strukturierter Form dokumentiert werden. Diese Absprachen können dann in einem zentralen Textdokument als Projektleitfaden abgelegt oder in einer Datenbank als Felder umgesetzt werden, die nur eine begrenze Auswahl von Begriffen zur Beschreibung eines spezifischen Sachverhaltes zulassen (z. B. für das Attribut Filmart nur die Werte "Diapositiv (Farbe)", "Negativfilm (Farbe)", "Negativfilm (SW)" und "Digital").

Besser eignen sich jedoch etablierte, standardisierte, globale Vokabulare, Thesauri oder Normdateien. Sie weisen oft eine thematische, fachspezifische oder institutionelle Ausprägung auf und werden von maßgeblichen Einrichtungen kontinuierlich gepflegt. Dazu gehören beispielsweise Normdateien zur Katalogisierung aus dem Bibliotheksbereich, Personennormdateien oder Thesauri zur eindeutigen Identifizierung von geografischen Orten oder Zeitbegriffen.

Diese globalen Systeme bieten nicht nur eine feste Bezeichnung und eine Definition eines Begriffes oder des diesem zugrunde liegenden Konzeptes, sondern auch alternative und gegebenenfalls mehrsprachige Benennungen und eine eindeutige Kennung zur Identifizierung des Begriffes. So kann beispielsweise der Ort "Alexandria" ([361058](http://www.geonames.org/361058/alexandria.html)) in Ägypten von dem Ort "Alexandria" ([4744091](http://www.geonames.org/4744091/alexandria.html)) in den USA mittels der in den Klammern angegebenen Kennungen aus GeoNames unterschieden werden.

Bereits existierende Thesauri und Vokabulare sollten bei der Vergabe von Metadaten berücksichtigt und angewendet werden, um den späteren elektronischen Austausch, also die Interoperabilität, der eigenen Daten mit anderen Systemen erheblich zu vereinfachen. Wenn Ressourcen in mehreren Sprachen vorliegen und entsprechend multilingual beschrieben werden sollen, müssen die genutzten Wörterbücher, Thesauri und Schlagwortsysteme äquivalente Begriffe in mehreren Sprachen abbilden.

Für die systematische Erfassung archäologischer und allgemeiner Begriffe existieren folgende Vokabulare:

- Art & Architecture Thesaurus (AAT) wurde Ende der 1970er von dem Getty Research Institute entwickelt, um die Katalogisierungsprozesse in Kunstbibliotheken und im Museumsbereich zu unterstützen und zu vereinheitlichen. Dieser Thesaurus wird von einer breiten Fachgemeinschaft kuratiert.
- Heritage Data - Linked Data Vocabularies for Cultural Heritage führt die in England genutzten Vokabulare im Bereich kulturelles Erbe zusammen.
- Wortnetz Kultur (WNK) wurde vom Landschaftsverband Rheinland ins Leben gerufen, um die Inhalte in deren verschiedenen Informationssystemen zu vereinheitlichen. Mittlerweile sind die Themen Kulturlandschaft, Archäologie, Kulturanthropologie, Denkmalpflege sowie Kunstgeschichte mit rund 15.000 Begriffen vertreten.
- Das DAI bietet mit iDAI.vocab (auch archwort) ein flaches multilinguales Vokabular mit Links auf den AAT. Außerdem gibt es mit dem iDAI.thesaurus ein System, das die Schlagworte aus den unterschiedlichen Thesauri der Bibliotheken zusammenführt und strukturiert.
- Die Encyclopedia of Life stellt eine weltweite Datenbank für Pflanzen und Lebewesen dar, die zusätzlich Fotos, Verbreitungskarten und Literaturhinweise enthält.
- In Wikidata werden alle strukturierten Daten aus den Systemen von WikiMedia erfasst und mit eindeutigen Identifikatoren zur Verfügung gestellt.

Für die eindeutige Identifizierung von geografischen Orten eignen sich, neben den amtlichen Gemeindekennzahlen und dem geodätischen Parameterdatensatz EPSG, folgende Ortshesauri, sogenannte Gazetteers:

- GeoNames ist ein Gazetteer, in dem vor allem moderne Orte, deren alternative Bezeichnungen und geografischen Koordinaten systematisch erfasst werden. Die Inhalte stammen von engagierten Nutzern weltweit.
- Getty Thesaurus of Geographic Names (TGN) wurde 1987 von dem Getty Research Institute ins Leben gerufen, um ebenfalls deren Katalogisierungsprozesse in Kunstbibliotheken und im Museumsbereich zu unterstützen und zu vereinheitlichen.
- Das DAI betreibt mit dem iDAI.gazetteer einen Gazetteer für die eindeutige Adressierung von antiken Orten, in dem außerdem auch die Eintragungen in GeoNames berücksichtigt werden.
- Pleiades ist ebenfalls ein Gazetteer für antike Orte mit einem Schwerpunkt auf der griechischen und römischen Antike, dessen Inhalt durch jeden Nutzer erweitert oder korrigiert werden kann.

Auch für Zeitbegriffe gibt es kontrollierte Vokabulare:

- PeriodO ist ein Gazetteer für Zeitepochen. Neben der zeitlichen Information wird auch die geografische Verbreitung der jeweiligen Epoche erfasst.
- iDAI.chronontology ist ein vom DAI durchgeführtes Projekt, das wie PeriodO zeitliche und geografische Informationen miteinander in Beziehung setzt.

Zur Erfassung von Informationen zu Personen oder Institutionen sollten Normdateien verwendet werden, wie beispielsweise:

- Das Virtual International Authority File (VIAF) kombiniert Normdateien mehrerer Nationalbibliotheken und speichert Informationen zu Personen und Institutionen, sowie deren Publikationen.
- Die Open Researcher and Contributor ID (ORCID) ist eine alphanumerische Zeichenkette, die der eindeutigen Identifizierung wissenschaftlicher Autoren dient. ORCID wird von einem gemeinnützigen Gremium betrieben und Autoren müssen sich selbst registrieren, um eine ID zu bekommen.
- Die Gemeinsame Normdatei (GND) der Deutschen Nationalbibliothek dient primär der Katalogisierung in Bibliotheken. Neben Informationen zu Personen und Körperschaften werden auch weitere Informationen zu Konferenzen, Geografika, Sachschlagwörtern und Werktiteln verwaltet.

Wenn in Metadaten auf Publikationen verwiesen werden soll, eignen sich folgende Systeme:

- Die Internationale Standardbuchnummer (engl. _International Standard Book Number_, ISBN) wird zur eindeutigen Identifizierung von Publikationen verwendet. Sie ist vor allem im Buchhandel verbreitet. Für Reihen und Zeitschriften wird eine ähnliche Nummer, die ISSN (Internationale Standardnummer für fortlaufende Sammelwerke, engl. _International Standard Serial Number_) verwendet.
- Für in Deutschland veröffentlichte Medienwerke gibt es eine Ablieferungspflicht bei der Deutschen Nationalbibliothek, weshalb die dort vergebenen  eindeutigen Kennungen ebenfalls zur Identifizierung verwendet werden können.
- Für archäologische und altertumswissenschaftliche Publikationen eignen sich auch die Identifikatoren aus iDAI.bibliography (Zenon), in dem die umfangreichen Bestände aller DAI Bibliotheken nachgewiesen werden.
