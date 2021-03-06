---
title: "Geo Tagging"
date: 2022-02-08T06:46:31+01:00
draft: true
tags: ["Analysis"]
---
## Analyse von "Peak Hunter"
### Funktionalität der App
Das Logbuch: Im Logbuch befinden sich Berge die man als nächsten bestreiten möchte / bereits erklommen hat.

Kategorie "Entdecken": öffnet eine Google Street Map Karte und zeigt den naheliegendsten Berg bei dem es möglich ist diesen zu erklimmen.

Kategorie "Karte": Hier befindet sich der eigene Standort über OpenStreetMap

Kategorie "Eintragen": Hiermit wird per GPS überprüft ob sie sich in der nähe des, im Logbuch eingetragenen Wunschgipfel, befinden. Angezeigt wird ihre Höhe (gemessen vom Meeresspiegel), die Abweichungen und ihre Koordinaten (Längen- und Breitengrade).

Kategorie "Challanges": Eine Challange handelt mit gefüllten Listen von Bergen die zu bewältigen / eintragen sind. Diese Challange hat eine Deadline und es gibt eine Chance einen Finisherpreis zu gewinnen.

Da man in den Bergen oftmals kein Empfang hat, gibt es auch die Möglichkeit sich eine Offline-Karte, von dem Berg den man vorhat zu erklimmen, herunterzuladen.

#### Geotagging von Fotos
Beim Geotagging werden digitalen Fotos zusätzliche Informationen zum Aufnahmeort hinzugefügt. Um Ortsinformationen in die Metadaten eines Fotos einzufügen bieten sich verschiedene Methoden an. Sie unterteilen sich in direkte, manuell und indirekte Arten des Geotaggings.

#### direktes / kamerainternes Geotagging
Hierbei werden Geoinformationen direkt bei der Aufnahme von der Kamera in die Exif-Daten geschrieben. Diese Methode wird am meisten von Smartphone Applikationen verwendet. Der große Vorteil dieser Variante ist sicher, dass die Exif-daten nicht nachträglich überarbeitet oder verändert werden müssen, also keine Nacharbeit am Computer nötig ist.

#### Manuelles Geotagging
Dabei wir aus einer Landkarte heraus einem Foto ein Ort zugewiesen. Diese Variante ist mit Hilfe einer kartenmaterialverwendenden Software möglich.

#### indirektes / trackbasiertes Geotagging
Die Positionswerte werden den Aufnahmen aus einem aufgezeichneten GPS-Track (Reiseroute) automatisch zugewiesen. Neben der GPS-Datei benötigen Sie dafür eine entsprechende Software. So lange die Zeitdifferenz zwischen Kamera und GPS-Empfänger hinreichend übereinstimmend sind, handelt sich sich hier um eine sehr präzise Art der Verortung, da in der Regel reine GPS-Empfänger etwas präziser sind als Geotagger.

#### Selbst testen und anwenden
Es werden automatisch schon Metadaten und zahlreiche weitere Informationen zum Bild abgelegt. Im Exif-Bereich (Exchangeable Image File Format) befinden sich verschiedene technische Aufnahmedaten.

Beispiel einer Webseite die Fotos auf einer Karte anzeigt: https://whereis.silverpeaks.de/. Diese Seite verwendet eine Google Maps API, um geographische Informationen visuell darzustellen.

Ein Programm könnte die Längen- und Breitengrade auslesen und mit dem Bild in eine Datenbank persistiert werden. Hier könnte die Libary "libexif" oder "ExifTool" hilfreich sein.

Es sollte vor der Persistierung überprüft werden ob das Foto überhaupt GPS-Geotags enthält. (.jpg Dateien)

