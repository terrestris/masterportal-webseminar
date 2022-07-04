---
theme: default
highlighter: shiki
lineNumbers: true
colorSchema: light
drawings:
  persist: false
class: text-center text-black
title: 'Masterportal Webinar'
layout: start
---
# 

![Masterportal Webinar Logo](/terrestris_webinar_logo.svg)

### In wenigen Schritten zum eigenen Geoportal
##### terrestris und dataport am 30. Juni 2022

---
layout: two-cols-header
---

::title::
# 🗣️ Über terrestris

::left::

- Open Source GIS aus Bonn seit **20 Jahren** 🥳
- 25 MitarbeiterInnen und 2 Geschäftsführer
- Aufbau von Geodateninfrastrukturen und WebGIS
  - modular mit etablierten OS-Komponenten
  - Bspw. Berechtigungsmanagement
- Präsent auf FOSSGIS und FOSS4G
- Aktive Mitarbeit in vielen OS GIS Projekten
- Geo-Consulting
- Wartung und Support u.a. für
  - Masterportal, MapProxy, SHOGun, OL, GeoServer, MapServer, QGIS, Postgres, Mapfish

::right::

![terrestris](/terrestris_greece.png)

<p class="text-center py-2">

  info@terrestris.de

  twitter: terrestrisde

  [github/terrestris.de](https://github.com/terrestris)

</p>
---
layout: main
---

# Was erwartet Sie?

<div class="py-12">

- 👥 **Vorstellung der IP (Implementierungs­­partnerschaft)**
- 👨‍💻 **Technischer Background**
- 🌍 **Globale Konfiguration**
- ⚙️ **Portalkonfiguration**
- 🛠 **Werkzeuge**
- 🗺️ **Anbindung von Services (Print, Suche)**
- 🪁 **Addons**
- 🚀 **Ausblick**
</div>

---
layout:  statement
---
# 👥Vorstellung der IP

---
layout: main

---
# 👨‍💻 Technischer Background

<div class="flex items-center py-4 mt-12">
  <img src="/Vue.js_Logo_2.svg" width="5rem" class="basis-10 framework" />
  <span class="basis-3/12 px-5">
    Vue.js
  </span>
  <span class="basis-full px-5">
    Modernes Javascript Framework
  </span>
</div>

<div class="flex items-center py-4">
  <img src="/Bootstrap_logo.svg" width="5rem" class="basis-10 framework" />
  <span class="basis-3/12 px-5">
    Bootstrap
  </span>
  <span class="basis-full px-5">
    Frontend Framework
  </span>
</div>

<div class="flex items-center py-4">
  <img src="/openlayers_logo.png" width="5rem" class="basis-10 framework" />
  <span class="basis-3/12 px-5">
    Openlayers
  </span>
  <span class="basis-full px-5">
    Webmapping API
  </span>
</div>

<div class="flex items-center py-4">
  <img src="/cesium.png" width="5rem" class="basis-10 framework" />
  <span class="basis-3/12 px-5">
    Cesium
  </span>
  <span class="basis-full px-5">
    Library for 3D Globes (WebGL basiert)
  </span>
</div>

---
layout: main

---
# 👷‍♂️ Technischer Background - Architektur


<div class="flex items-center mt-32">
  <img src="/core-api-addon_paths.svg"  class="self-center" />
</div>
---
layout: main
---

# Applikationskontext

<!-- ### Begriff definieren, aufzeigen der einzelnen Dateien -->

  <img src="/code_architecture.png" class="w-9/10" />

---
layout: two-cols-header
---

::title::
# 🌍 Globale Konfiguration

::left::

## services.json

- Zentrale Konfiguration für Layer
- WMS, WFS, WMTS, SensorThings-API, GeoJSON u.a.
- wird in der jeweiligen Portalkonfiguration `config.js` referenziert
- Kann auch über einen API-Endpunkt generiert werden (z.B. Dienstemanager)

::right::

```json
{
    "id" : "8",
    "name" : "Aerial View DOP 10",
    "url" : "https://geodienste.hamburg.de/HH_WMS_DOP10",
    "typ" : "WMS",
    "layers" : "1",
    "format" : "image/jpeg",
    "version" : "1.3.0",
    "singleTile" : false,
    "transparent" : true,
    "tilesize" : "512",
    "gutter" : "0",
    "minScale" : "0",
    "maxScale" : "1000000",
    "gfiAttributes" : "ignore",
    "layerAttritibuon" : "nicht vorhanden",
    "legend" : false
}
```

---
layout: two-cols-header
---

::title::
# 🌍 Globale Konfiguration

::left::
## rest-services.json

- Services, die nicht direkt für die Darstellung von Daten benötigt werden:
  - Print services (MapFish)
  - Metadata sources (CSW)
  - BKG geocoding service
  - Gazetteer URL
  - WPS

::right::

## style.json

- Styledefinitionen für Vektorlayer (Styling erfolgt im Client)

```json
  {
    "styleId": "blue-point",
    "rules": [
      {
        "style":
          {
          "circleRadius" : 6,
          "circleStrokeColor": [51, 102, 255, 1],
          "circleStrokeWidth": 2,
          "circleFillColor": [51, 102, 255, 1]
          }
      }
    ]
  }
```
---
layout: two-cols-header
---

::title::
# ⚙️ Portalkonfiguration

::left::

## config.js

- Pfade zu Backends und weiteren Konfigurationsdateien
- Projektionsdefinitionen *(z.B. UTM32N, UTM33N)*
- Liste an Addons
- Quickhelp
- Footer
- Mousehover
- Sprachen
- Blacklist für GFI-Attribute (z.B. *geom, id*)

::right::

```js
const Config = {
    namedProjections: [
        ["EPSG:25832", "+title=ETRS89/UTM 32N +proj=utm +zone=32 +ellps=GRS80 +towgs84=0,0,0,0,0,0,0 +units=m +no_defs"]
    ],
    footer: {
        showVersion: true
    },
    quickHelp: {
        imgPath: "./resources/img/"
    },
    layerConf: "./resources/services-internet.json",
    restConf: "./resources/rest-services-internet.json",
    styleConf: "./resources/style_v3.json",
    scaleLine: true,
    mouseHover: {
      numFeaturesToShow: 2,
      infoText: "(weitere Objekte. Bitte zoomen.)"
    }
}
```

---
layout: two-cols-header
---

::title::
# ⚙️ Portalkonfiguration

::left::

## config.json

- Konfiguration der Portal-Oberfläche
- Titel und Logo
- Kartenelemente
- Menüelemente
- Werkzeuge und Addons
- Suche 
- Themenbaum (Layertree)

::right::

```json
	"Portalconfig": {
    "treeType": "light",
		"searchBar": {
			"komoot": {
        "minChars": 3,
        "serviceId": "11",
        "limit": 20,
        "lang": "de",
        "lat": 53.6,
        "lon": 10.0,
        "bbox": "9.6,53.3,10.4,53.8"
    },
      "visibleVector": {
		  "layerTypes": ["WFS"]
	  },
      "tree": {},
			"startZoomLevel": 9,
			"placeholder": "Suche nach: - Adresse - Aktiven WFS"
		}
	}
```
---
layout: statement
---
# Live-Demo 🎮

---
layout: iframe-right
url: https://viz.berlin.de/wp-content/plugins/masterportal-wordpress/public/portals/berlin_2_19/index.html?layerIds=WebatlasBrandenburg,EcoCounter&transparency=30,0&lng=de

---

## SensorThings API

- Datenfluss von IoT Sensoren
- **Beispiele:** Verkehrszählungen, Mobilität, Luftmessnetzdaten

```json
   {
      "id" : "999999",
      "name" : "Live - Charging locations",
      "typ" : "SensorThings",
      "version" : "1.0",
      "url" : "https://51.5.242.162/itsLGVhackathon",
      "intersect": true,
      "urlParameter" : {
         "root" : "Things",
         "filter" : "startswith(Things/name,'Charging')",
         "expand" : "Locations,Datastreams/Observations($orderby=phenomenonTime%20desc;$top=1)"
      }
      "mqttOptions" : {
        "host" : "https://localhost",
        "port": "1883"
      }
```

---
layout: iframe-right
url: https://test.geoportal-hamburg.de/vectorTiles

---

## VectorTiles

```json
{
  "id": "UNIQUE_ID",
  "name": "Ein Vektortilelayername",
  "epsg": "EPSG:3857",
  "url": "https://example.com/3857/tile/{z}/{y}/{x}.pbf",
  "typ": "VectorTile",
  "vtStyles": [
    {
      "id": "STYLE_2",
      "name": "Nachtansicht",
      "url": "https://example.com/3857/resources/styles/night.json"
    }
  ]
}
```

### Ausblick
- Optimierung VectorTile Support in OL
- OGC API Tiles *(maps and vector tiles)*

---
layout: two-cols-header
---

::title::
# Featureliste (Auszug)

::left::

- Strecke / Fläche messen
- Zeichnen / Schreiben
- Layerslider
- <span class="text-blue-500 font-extrabold">Schrägluftbilder</span>
- Vergleichslisten
- Koordinatenabfrage
- <span class="text-green-500 font-extrabold">Elastic Search</span>
- Informationsabfrage Metadaten
- Informationen abfragen (Attribute) + Theming
- Koordinatensuche
- <span class="text-red-500 font-extrabold">Komoot Photon</span>
- Auswahl speichern (Permalink)

::right::
- <span class="text-yellow-500 font-extrabold">Graph</span>
- Auswahl Vektordienstübergreifend
- <span class="decoration-green-500 text-blue-500 font-extrabold">Mehrsprachigkeit</span>
- Buffer Analyse
- Time Slider
- <span class="text-green-500 font-extrabold">Flurstückssuche</span>
- Layer Swipe
- Aktive Themen durchsuchen
- <span class="text-red-500 font-extrabold">Routing</span>

---
layout: two-cols-header
---

::title::
# 🪁 Addons

::left::

- <span class="font-extrabold text-green-500">Vue.js</span> Komponenten (früher Backbone)
- Kommunikation mit den Core-Komponenten über <span class="font-extrabold text-green-500">Vuex</span> (*zentrales state management*)
- Beliebige, individuelle Tools oder GFI-Themes
- Erweiterung von
  - Kartenfunktionen
  - Suchen
  - Layout

::right::
## Beispiele:
- BORIS
- <span class="font-extrabold text-blue-500">Einwohnerabfrage</span>
- backgroundSwitcher
- <span class="font-extrabold text-red-500">Erweiterte Suche (Detailsuche)</span>
- scaleLineCustom
- mpJsApi (Javascript API, zum Steuern des Masterportals von außen)
- <span class="font-extrabold text-yellow-500">Generische Import und Export-Tools</span>
  - Einstieg von verschiedenen Komponenten (Suche, Tree, Menü)
  - SHAPE, GPKG, GeoJSON
  - Styling beim Import von Vektordaten

---
layout: main
---
# 🚀 Ausblick

<div class="py-12">

- Verknüpfung Masterportal Anwendung mit Fachanwendungen
- Verbesserung der Einbindung in CMS
- Erweiterung der Flurstückssuche
- Daten-Analyse und Präsentation
- Verbesserung der Barrierearmut
- Großformatiges Plotten
- ...

</div>

---
layout: main
---

# Hilfreiche Links

<div class="py-12">

- [FOSSGIS Masterportal Workshop Unterlagen](https://terrestris.github.io/masterportal-ws)

- [Masterportal Dokumentation](https://www.masterportal.org/files/masterportal/html-doku/doc/latest/doc.html)

- [FOSSGIS Videos zum Masterportal (media.ccc.de)](https://media.ccc.de/search/?q=masterportal)

- [Liste von Masterportalen in der Praxis](https://www.masterportal.org/referenzen.html)

</div>

---
layout: statement
---
# Vielen Dank
## für das Interesse 🤝


<p class="py-28">Fragen gerne jetzt oder an:<br>
blitza@terrestris.de, jens.nienaber@dataport.de</p>
