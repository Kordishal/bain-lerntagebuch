---
title: "Einführung"
date: 2023-02-15T08:10:30Z
toc: true
---
Dies ist mein Lerntagebuch für den Kurs Bibliotheks- und Archivinformatik (BAIN). Diese erste Seite bildet eine Übersicht
als Einstieg. In der Vorlesung lernen wir verschiedene Systeme kenne die in der Branche verwendet werden
und wie diese Verbunden werden.

Die Vorlesung soll den Teilnehmenden eine Übersicht bieten, damit sie diese Systeme kennenlernen und im richtigen Moment anwenden können.
Zu der Vorlesung wird dieses Lerntagebuch verfasst. Es wird ein Beitrag zu den Inhalten von jedem Block und zu den verschiedenen 
Übungen gemacht. Dabei sollen wir darüber reflektieren was und wie wir das gemacht haben und was wir gelernt haben. Es sollen
auch eigene Schwerpunkte gesetzt werden.

## Meine Vorkenntnisse
Ich kenne viele verschieden Systeme und Applikationen, die in diesem Bereich verwendet werden. Unten eine Liste mit Links was ich alles
mir mal angesehen habe. Mein Fokus ist in der Regel auf Elasticsearch und das transformieren und normalisieren von Metadaten und deren Serialisierung.

Dort verwende ich Services die auf Kafka aufbauen in einer Pipeline wo jeder Service eine Aufgabe hat und diese erledigt und dann die Daten weitersendet. Die Daten werden mit verschiedenen Bibliotheken geöffnet und transformiert.

### Applikationen

- VuFind. Ein Framework für Kataloge von Bibliotheken. Wurde verwendet für swissbib und nun für swisscollections. 
- Solr / Elasticsearch. Suchmaschinen die eine API anbieten mit der man die indexierten Daten schnell und effizient durchsuchen kann. Grundlage für alle Webseiten die Suche implementieren. Ich bin vor allem mit Elasticsearch vertraut.
- [Fedora](https://fedora.lyrasis.org/). Eine open source Server Applikation die das verwalten von Archivdaten ermöglicht. Die Platform unterstützt auch das speichern von Linked Date Nativ. Wird bei uns bei verschiedenen Projekten eingesetzt. 
- [Eprints](https://www.eprints.org/uk/). Wird von Edoc verwendet. Ich habe diese Software verwendet aber auch system administration betrieben. Wird Ende Jahr von DSpace abgelöst.
- [Fuseki](https://jena.apache.org/documentation/fuseki2/) (SPARQL). Einfacher und langsamer SPRQL Webserver der bei uns für ein kleines Projekt verwendet wurde. Dieses Projekt wird aber jetzt nicht mehr deployed.

### Infrastruktur

- [Kafka](https://kafka.apache.org/). Das Herz unser Datenverarbeitungsarchitektur von vor allem Memobase. 
- [Flink](https://flink.apache.org/), [Spark](https://spark.apache.org/). Batch und streaming Plattformen die wir im Moment nicht mehr verwenden, weil wir primär auf Kafka setzten.

### Datenverarbeitung

- XSLT
- Metafacture
- Openrefine
- Apache Jena (Java)

### API Standards

- [OAI-PMH](https://www.openarchives.org/pmh/). Diesen Standard verwenden wir in vielen verschiedenen Schnittstellen um Daten zu holen und zu liefern. Zum Beispiel alle Daten aus Alma kommen von der OAI Schnittstelle.
- [SRU](https://www.loc.gov/standards/sru/). Ein Standard für das Suchen von Metadaten. Wurde von uns bei swissbib Angeboten. Ist im Moment nicht mehr im Einsatz.
- [IIIF](https://iiif.io/). Wird verwendet um Bilder im Web zur Verfügung zu stellen. Insbesondere von Digialisaten auch bei Memobase. Infrastruktur befindet sich aber immer noch im Aufbau.

### Metadatenstandards / Datensets


- [Linked Data](https://en.wikipedia.org/wiki/Linked_data)
- [MARC / MARC21 XML](https://www.loc.gov/standards/marcxml/)
- [Records in Context](https://www.ica.org/en/records-in-contexts-conceptual-model)
- [Dublin Core](https://www.dublincore.org/)
- [Schema](https://schema.org/)
- [Wikidata](https://wikidata.org) / [Dbpedia](https://www.dbpedia.org/)
- [Viaf](https://viaf.org/) / [GND](https://www.dnb.de/DE/Professionell/Standardisierung/GND/gnd_node.html)

## Meine Erwartungen

Da ich bereits viele Vorkenntnisse habe, habe ich nicht sehr hohe Erwartungen, dass es viel neues gibt. Ich hoffe
aber dennoch, dass ich vielleicht das eine oder andere neue Stichwort mitnehmen kann. Ich freue micht, dass
der Kurs einen Fokus auf Open Source Tools und Software legt. In der Schweizer Bibliotheks- und Archivlandschaft 
werden die leider kaum betrachtet für die wichtigen und grossen Systeme. Dementsprechend ist es wichtig, dass diese
Tools den zukünftigen Bibliothekar:innen und Archivar:innen bekannt sind. So gibt es eine Chance, dass sich dieser Umstand
in der Zukunft ändern wird.

Gleichzeitig gibt es mir die Chance diese Dokumentation in einem sinnvollen Rahmen zusammenzustellen.