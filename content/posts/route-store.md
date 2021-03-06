---
title: "Route Store"
date: 2022-02-08T06:47:07+01:00
draft: true
tags: ["Analysis"]
---
# Abspeichern von Routen

## Wie werden Daten von Openstreetmap und GoogleMaps abgespeichert?

### Openstreetmap:

#### In Openstreetmap werden die Daten in GPX abgespeichert. GPX ist XML für GPS Daten.

##### Hier ein Beispiel, wie die Daten aussehen können:
    ```
    Waypoint( <wpt> )
        Einzelne Ortspunkte/Wegpunkte
    Route( <rte> )
        Eine sortierte Abfolge von Ortspunkten/Wegpunkten( <rtept> ). Beschreibt
        einen geplanten Kurs, bzw. eine Folge von Wendepunkten, um zu einem Ziel
        zu gelangen.
    Track( <trk> )
        Eine sortierte Liste aufeinander folgender Punkte (<trkpt>), die einen
        Linienzug ergeben. Beispielsweise ein durch ein GPS-Gerät aufgezeichneter
        Pfad. Die Punkte werden nochmals in einzelne Abschnitte zusammengefasst
        (Tracksegment, kurz <trkseg>).
    ```

    ```
    <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
    <gpx version="1.1" creator="Ersteller der Datei">
        <metadata> <!-- Metadaten --> </metadata>
        <wpt lat="xx.xxx" lon="yy.yyy"><!-- Attribute des Wegpunkts --></wpt>
        <!-- weitere Wegpunkte -->
        <rte>
            <!-- Attribute der Route -->
            <rtept lat="xx.xxx" lon="yy.yyy"> <!-- Attribute des Routenpunkts --> </rtept>
            <!-- weitere Routenpunkte -->
        </rte>
        <!-- weitere Routen -->
        <trk>
            <!-- Attribute des Tracks -->
            <trkseg>
            <trkpt lat="xx.xxx" lon="yy.yyy"> <!-- Attribute des Trackpunkts --> </trkpt>
            <!-- weitere Trackpunkte -->
            </trkseg>
            <!-- weitere Track-Segmente -->
        </trk>
        <!-- weitere Tracks -->
    </gpx>
    ```

##### Hier https://wiki.openstreetmap.org/wiki/OpenStreetMap-Tutorial_f%C3%BCr_Anf%C3%A4nger gibt es ein sehr gutes Tutorial für OSM. Es sind alle Grundfunktionen vermerkt um schnellstmöglich auf ein Ergebnis zu kommen.

### GoogleMaps:

#### GoogleMaps routen werden auch als GPX-Datei gedownloaded.

