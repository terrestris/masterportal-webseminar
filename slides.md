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
##### terrestris und dataport am 17. Dezember 2024

---
layout: two-cols-header
---

::title::
# 🗣️ Über terrestris

::left::

- Open Source GIS aus Bonn seit **22 Jahren**
- 25 MitarbeiterInnen und 2 Geschäftsführer
- Aufbau von Geodateninfrastrukturen und WebGIS
  - modular mit etablierten OS-Komponenten
  - Fachsysteme (z.B. Gewässerschutz, Telekommunikation)
  - Berechtigungsmanagement
- Aktiv auf FOSSGIS und FOSS4G
- Aktive Mitarbeit in vielen OS GIS Projekten
- Geo-Consulting
- Wartung und Support u.a. für
  - Masterportal, MapProxy, GeoStyler, SHOGun, OL, GeoServer, MapServer, QGIS, Postgres, Mapfish

::right::

![terrestris](/terrestris_spanbroek.png)

<p class="text-center py-2">

  📫 info@terrestris.de

  🔗 linkedin: [terrestris-gmbh-co-kg](terrestris-gmbh-co-kg)

  🎨 [github/terrestris.de](https://github.com/terrestris)

</p>
---
layout: main
---

# 📄 Was erwartet Sie?

<div class="py-12">

- 👥 **Vorstellung der IP (Implementierungs­­partnerschaft)**
- 👨‍💻 **Technischer Background**
- 🌍 **Globale Konfiguration vs. ⚙️ Portalkonfiguration**
- 📰 **V3 Neuerungen**
- ⏫ **V3 Migration**
- 🔐 **Integration Identitäts- und Zugriffsverwaltung**
- ❓ **Fragerunde**
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
  <img src="/code_architecture_v3.png"  class="self-center" />
</div>
---
layout: main
---

# Applikationskontext

<!-- ### Begriff definieren, aufzeigen der einzelnen Dateien -->

  <img src="/code_architecture.png" class="w-9/10" />

---
layout: main
---
# 📰 Neuerungen v3

- Menü Modul – neue Oberfläche
  - Neuanordnung von Elementen und Layern: `MainMenu` und `SecondaryMenu`
  - GUIs der einzelnen Module unverändert
  - Neue GUI adressiert auch GIS unerfahrene User
- Stärkung der **masterportalAPI**, um Nutzung in anderen Anwendungsgebieten zu ermöglichen
  - z.B. Auslagerung aller Daten-Schnittstellen in die **masterportalAPI**
- Customizable 🎨 
    - Mehrere Möglichkeiten zur Individualisierung
- Neues UI
    - Entstanden im Rahmen einer größeren Studie/Umfrage
- Vue3 und Vuex
- Bootstrap 5
    - UI Elemente (Buttons, Modals, Forms, Navs und tabs, ... )

---
layout: main
---
# 📰 Neuerungen v3

- Performance
    - Refaktorierung Config and Layer Loading
- Responsivity
    - Design/Layout für Tablets und Smartphones optimiert
- Map Controls: Können individueller konfiguriert werden
- Addon-Typen:  Tools, GFI Themes, Controls, JavaScript, **SearchInterface**
- Layer-Tree:
  - Layer-Katalog (Suche, Baselayer, Layer)
- Layer-Pills 💊
- Weitere Tools: `News`, `baseLayerSwitcher`, `customMenuElement`, `StatisticDashboard`, `openConfig`, `About`
- 3D: Core Refactoring, Print 3D, Modeler 3D (https://pretalx.com/fossgis2024/talk/93LW77/)[https://pretalx.com/fossgis2024/talk/93LW77/]

---
layout: statement
---
# Live-Demo 🎮


---
layout: two-cols-header
---

::title::
# 🪁 Addons

::left::
## Beispiele:
- populationRequest
- commuterFlows
- <span class="font-extrabold text-blue-500">Einwohnerabfrage</span>
- <span class="font-extrabold text-red-500">Erweiterte Suche (Detailsuche)</span>
- Custom GFI Themes
- <span class="font-extrabold text-yellow-500">Generische Import und Export-Tools</span>
  - Einstieg von verschiedenen Komponenten (Suche, Tree, Menü)
  - SHAPE, GPKG, GeoJSON
  - Styling beim Import von Vektordaten
- Custom SearchInterfaces

::right::

- https://bitbucket.org/geowerkstatt-hamburg/addons
- https://github.com/Dataport/MasterportalAddonshttps://github.com/Dataport/MasterportalAddons
- https://github.com/terrestris/masterportal-addons

---
layout: main
---

# Hilfreiche Links

<div class="py-12">

- [Migrate Config Guide](https://bitbucket.org/geowerkstatt-hamburg/masterportal/src/v3.3.3/docs/User/Misc/migrateConfigv2Tov3.md)

- [FOSSGIS Masterportal Workshop Unterlagen](https://terrestris.github.io/masterportal-ws)

- [Masterportal Dokumentation](https://www.masterportal.org/mkdocs/doc/v3.2.0/doc.html)

- [FOSSGIS Videos zum Masterportal (media.ccc.de)](https://media.ccc.de/search/?q=masterportal)

- [Liste von Masterportalen in der Praxis](https://www.masterportal.org/referenzen/referenzen)

</div>

---
layout: statement
---
# Vielen Dank
## für das Interesse 🤝


<p class="py-28">Fragen gerne jetzt oder an:<br>
blitza@terrestris.de, wagner@terrestris.de, maren.michaelis@dataport.de</p>
