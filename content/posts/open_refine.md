---
title: "03 Open Refine"
date: 2023-02-28T16:19:37Z
draft: false
toc: true
---
In dieser Einheit haben wir uns OpenRefine angesehen. Ich habe OpenRefine auf meinem privaten 
Laptop installiert für diese Einheit. 


Ich habe bereits verschiedene Erfahrungen mit OpenRefine gemacht und auch verwendet für verschiedene Projekte.
Diese Projekte haben sich alle mit Bibliographischen Metadaten beschäftigt. Das Ziel war es jeweils diese Daten mit den GND
Daten anreichern zu können. Dazu habe ich jeweils den Endpunkt vom hbz auf [lobid](https://lobid.org/) verwendet.
In einem Projekt habe ich auch Daten aus der Wikidata reconciliert. Dies hat zwar viel mehr Treffer geliefert, war aber
dann schwieriger das zu korrekt zu verbinden. Es gab mehr falsche Zusammenführungen.

Die Beispieldaten konnten einfach geladen werden mit dem Link zu raw.github. Für die Übung gibt es ein paar Schritte die gemacht werden 
können.

## Vorführung von Basisfunktionen

- Spalte Language > Facet > Text Facet: 

> Diese Spalte enthält fünf Werte. EN, FR, ES, English und kein Wert (blank). Der Wert English kann einfach mit OpenRefine ändern zu EN.

- Spalte Authors > Edit cells > Split multi-valued cells… > Separator: |
- Spalte Authors > Edit cells > Cluster and edit…
- Spalte Authors > Edit cells > Join multi-valued cells… > Separator: |

>    Mit diesem vorgehen, können die Autoren getrennt werden und dann wieder zusammengeführt. Allerdings habe ich von der Erklärung selber nicht verstanden was genau Cluster und edit macht. Beim zweiten mal habe ich dann verstanden, dass man mit dieser Funktion Personen die ähnlich heissen zusammenführen kann. Diese Funktion gibt Vorschläge für Autoren, die ähnlich geschrieben sind aber nicht genau gleich, oder z.B. den Vor- und Nachnamen umgekehrt eingetragen haben. So kann man für jeden Treffer entscheiden ob das wirklich die gleiche Person ist oder nicht. Dies kann das Programm eigentlich nie mit grosser Sicherheit entscheiden, aber ein Mensch kann aus verschiedene Heuristiken ob dieser Zusammenschluss Sinn macht oder nicht.

> Mit der Funktion Split Column konnte ich die Autoren aufteilen. Die höchste Anzahl an Autoren für ein Paper ist 16. Es gibt zwei Personen in der letzten Spalte. Damit sind es nur zwei Papers die 16 Autoren haben.

## Kleine Fingerübungen

    Spalte Licence > Facet > Text facet
        Was ist die am häufigsten vergebene Lizenz
        Wieviele Artikel haben keine Lizenz?

| Wert | Anzahl |
|---|---|
| CC BY | 954 | 
| CC BY-NC | 11 |      
| CC BY-NC-ND | 30 |
| Leer | 6 |


Spalte Publisher > Facet > Text facet Warum erscheint MDPI AG zweimal? Wie lässt sich das korrigieren?

> Der Unterschied ist ein zusätzlicher Leerschlag. Dieser kann einfach mit der Edit-Funktion entfernt werden damit alle Werte gleich sind.

## Vorführung Reconciliation

    Ziel: Über die ISSN Informationen zur Zeitschrift ergänzen
    Spalte Citation > Edit column > Add column based on this column…
        Name: Journal
        Expression: value.split(",")[0]
    Spalte Journal > Reconcile > Start reconciling
        Wikidata reconci.link (en) auswählen
        links “Reconcile against no particular type” auswählen
        rechts “ISSNs” aktivieren und in Textfeld ISSN eingeben und P236 anklicken
    Spalte Journal > Edit column > Add columns from reconciled values…
        official website (P856)
        configure: Limit auf 1 setzen

> Dieser Service ist sehr mächtig um Daten aus externen Datenbanken einzubinden. Es kann jeweils eine Weile dauern bis es klappt und es ist wichtig, dass die Daten bereits einen guten Identifier haben. Ich habe auch schon ohne diesen Idenifier nach matches gesucht. Dies führt dann aber dazu, dass man dann die meisten Treffer manuell überprüfen muss. Dies ist sicher kein Problem wenn es ein paar Dutzend sind, aber bei viele Tausend oder sogar Millionen ist das natürlich nicht mehr möglich. Ein Problem hier das ich festgestellt habe ist, dass es Teilweise mehrere ISSN mit einem | als Trennzeichen dazwischen hat. Das hat natürlich dazu geführt, dass diese Zeilen keinen Treffer haben. Die Treffer sind auch nicht sehr vollständig. Ich hätte erwartet, dass Wikidata eine ziemlich vollständige Sammlung von ISSN hat. Dies ist aber anscheinend nicht der Fall. Ah und im Nachhinein habe ich gemerkt, dass ich das ganze auf der falschen Spalte gemacht habe...



