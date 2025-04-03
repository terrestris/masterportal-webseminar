---
theme: default
highlighter: shiki
lineNumbers: true
colorSchema: light
drawings:
  persist: false
class: text-center text-black
title: 'Masterportal Datenerfassung Web-Seminar'
layout: start
---
# 

![Masterportal Web-Seminar Logo](/terrestris_webseminar_logo.svg)

### Datenerfassung im Masterportal
##### terrestris und die Kreisverwaltung Warendorf im April 2025

---
layout: main
---

# 📄 **Was erwartet euch?**

<div class="py-12 text-m">

- 🏗️ **Projektkontext**
- 🚰 **Use Case Trinkwasserbrunnen**
- 🌳 **Use Case Kompensationsflächen**
- 👨‍💻 **Architektur**
- 🔭 **Weiterentwicklung**
- ❓ **Fragerunde**

</div>

---
layout: two-cols-header
---

::title::
# 🗣️ **Über terrestris**

::left::

- Open Source GIS aus Bonn seit > 20 Jahren
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

<div class="text-center py-2">

  📫 info@terrestris.de

  🔗 linkedin: [terrestris-gmbh-co-kg](terrestris-gmbh-co-kg)

  🎨 [github/terrestris.de](https://github.com/terrestris)

</div>

---
layout: main
---
# **Vision und Projektkontext**

- Tool für das Masterportal, mit dem Daten georeferenziert erfasst und bearbeitet werden können
- Abbildung von komplexen Datenmodellen sollte möglich sein
- Erfassung von Geo- und Sachdaten durch Einbindung anbieter-unabhängiger Formulare

---
layout: main
---

# **Szenario Trinkwasserbrunnen** 🚰

<div class="py-4">

## **Kontext**
Zunehmend wichtiges Thema im städt. Kontext (Stadtklima, Hitzeschutz).  
Querschnittsthema: Stadtplanungs- und Bauamt, Umwelt- und Gesundheit, Wasserwerke.

## **Datenmodell** (verkürzt)

<div class="container">
    <div class="box">
      <b>Trinkwasserbrunnen</b><br/>
      <ul>
        <li>Status</li>
        <li>Inbetriebnahme</li>
        <li>Standort</li>
        <li><i>Inspektion</i></li>
        <li><i>Typ</i></li>
      </ul>
    </div>
    <div class="box">
      <b>Inspektion</b><br/>
      <ul>
        <li>Datum</li>
        <li><i>Inspekteur</i></li>
      </ul>
    </div>
    <div class="box">
      <b>Wartungspersonal</b><br/>
      <ul>
        <li>Name</li>
        <li><i>Amt</i></li>
      </ul>
    </div>
    <div class="box">
      <b>Brunnentyp</b>
      <ul>
        <li>Bauart</li>
      </ul>
    </div>
</div>

</div>

<!-- **A)** Ein Mitarbeiter des Ordnungsamts möchte im Rahmen des monatlichen Monitorings den Zustand der bestehenden Brunnen prüfen und entsprechend dokumentieren.  

**B)** Eine Mitarbeiterin der kommunalen Verwaltung möchte einen neuen Trinkwasserbrunnen in der Altstadt erfassen.   -->

---
layout: statement
---

# Live-Demo 🎮

---
layout: main
---

# **Szenario Kompensationsflächen** 🌳

<div class="py-4">

## **Kontext**

Das kommunale Kataster für Ausgleichs- und Kompensationsflächen unterstützt ein nachhaltiges Flächenmanagement und dient der klaren Dokumentation für Verwaltung und Öffentlichkeit.

## **Datenmodell** (verkürzt)

<div class="container">
    <div class="box">
      <b>Kompensationsflächen</b><br/>
      <ul>
        <li>Name</li>
        <li>Geometrie</li>
        <li><i>Status</i></li>
        <li>Maßnahme</li>
        <li>Flächengröße</li>
        <li><i>Eigentümer</i></li>
        <li>Foto</li>
      </ul>
    </div>
</div>

<!-- ## **Use Cases**

**A)** Eine Mitarbeiterin der kommunalen Verwaltung möchte eine neue geplante Kompensationsfläche (Obstbaumreihe) an der Stieldorfer Straße (Holtdorf) erfassen.

**B)** Ein Mitarbeiter der unteren Naturschutzbehörde möchte die Daten für eine Fläche aktualisieren und hierbei ein Foto der abgeschlossenen Maßnahme hochladen. -->

</div>

---
layout: statement
---

# Live-Demo 🎮

---
layout: main
class: h-screen
---

# **Architektur**

<img src="/form-backend-architecture.drawio.png" width="50%" />

---
layout: main
---
# **Weiterentwicklung**

- Addon: Integration in Masterportal Core
- JSON Schema für die Konfiguration (Autocompletion)
- Typescript Typings für PostgREST Definitionen
- Caching der Form Konfigurationen
- Ausbau der Karteninteraktionen
- Ausbau der Digitalisierungsmöglichkeiten
- Optimierung des Formular Layouts

---
layout: two-cols-header
---

::title::

# **Loslegen**

- [Demo Setup (Docker Compose)](https://github.com/formcapture/form-backend/tree/main/demo)

::left::
**Warendorf**
- Erfahrungen Use Cases
  - Winterdienststrecken
  - Gewerbeflächen
  - ...
- Austausch Datenmodellierung
- Austausch über Konfigurationen
- Zusammenarbeit in IP

::right::
**terrestris**

- Integration in vorhandenes System
- Schulungen & Workshops
- Support
- Weiterentwicklung
- Wartung

---
layout: statement
---
# Vielen Dank
## für das Interesse 🤝

<div class="py-28">Fragen gerne jetzt oder an:<br>
blitza@terrestris.de, suleiman@terrestris.de<br/>
Maria.Wunsch@kreis-warendorf.de, Marlena.Hecker@kreis-warendorf.de
</div>
