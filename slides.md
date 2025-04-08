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

# **Was erwartet euch?**

<div class="py-12">

- 🏗️ **Vision und Projektkontext**
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
- 24 MitarbeiterInnen und 2 Geschäftsführer
- Aufbau von Geodateninfrastrukturen und WebGIS
  - Modular mit etablierten OS-Komponenten
  - Fachsysteme (z.B. Gewässerschutz, Telekommunikation)
  - Berechtigungsmanagement
- Aktiv auf FOSSGIS und FOSS4G
- Aktive Mitarbeit in vielen OS GIS Projekten
- Masterportal, MapProxy, GeoServer, QGIS, Postgres, Superset, SHOGun

::right::

![terrestris](/terrestris_spanbroek.png)

<div class="text-center py-2">

  📫 info@terrestris.de

  🔗 linkedin: [terrestris-gmbh-co-kg](terrestris-gmbh-co-kg)

  🎨 [github/terrestris.de](https://github.com/terrestris)

</div>

---
layout: warendorf
---
# **Vision**

## Ziel
- Fachämter und Gemeinden mit einem Tool befähigen, selbstständig Daten georeferenziert erfassen und bearbeiten zu können

## Anforderungen
- Masterportal-Tool 
- Einbindung anbieterunabhängiger Formulare zur Datenerfassung
- Abbildung von komplexen Datenmodellen
- Upload von Dateien (Fotos, PDFs etc.)
- Open Source

---
layout: warendorf
---
# **Projektkontext**

- Umsetzung der Idee als agiles Projekt
- In regelmäßigen Sprints wurden Konzepte entwickelt, implementiert und getestet
- Dauer das Projekts ca. 6 Monate

---
layout: warendorf
---
# **Aktueller Stand**

- Erste Anwendungen in der Testumgebung
- Austausch mit Fachämtern und kreisangehörigen Kommunen zur Umsetzung verschiedener Anwendungsfälle:
  - Hygienekontrollen des Gesundheitsamts (Brunnen)
  - Hausnummernerfassung in den Kommunen
  - Planung Winterdienststrecken
  - Vermarktung von Gewerbeflächen
  - Erfassung von Stadtmöblierung
  - Kartierung von Riesenbärenklaubeständen

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
        <li><i>Inspektionen</i></li>
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
    <div class="box">
      <b>Eigentümer</b><br/>
      <ul>
        <li>Name</li>
      </ul>
    </div>
    <div class="box">
      <b>Status</b><br/>
      <ul>
        <li>Name</li>
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
---

# **Architektur**

<img src="/form-backend-architecture.drawio.svg" width="50%" />

---
layout: two-cols-header
---
::title::

# **Weiterentwicklungen**

::left::
# Epics

- Addon: Integration in Masterportal Core
- Admin-UI für Formular-Konfigurationen
- JSON Schema für die Konfiguration (Autocompletion)
- Verknüpfte Formulare
- Granulares Rechtemanagement

::right::
# Features
- Ausbau der Karteninteraktionen
  - Filtern nach Kartenausschnitt
  - Geocoder
  - Kartenintegration im standalone Viewer
- Ausbau der Digitalisierungsmöglichkeiten
- UI Polishing

---
layout: two-cols-header
---

::title::

# 🚀 **Loslegen**

- [Demo Setup (Docker Compose)](https://github.com/formcapture/form-backend/tree/main/demo)

::left::
**Warendorf**
- Erfahrungen Use Cases
  - Winterdienststrecken
  - Gewerbeflächen
  - ...
- Austausch Datenmodellierung
- Austausch über Konfigurationen
- Zusammenarbeit für Weiterentwicklung

::right::
**terrestris**

- Integration in vorhandene Systeme
- Schulungen & Workshops
- Support
- Weiterentwicklung
- Wartung
- Upgrade auf Masterportal v3

---
layout: statement
---
## Vielen Dank
## für das Interesse 🤝

<div class="py-4"><b>Fragen gerne jetzt stellen oder an:</b><br>
blitza@terrestris.de, suleiman@terrestris.de<br/>
Maria.Wunsch@kreis-warendorf.de, Marlena.Hecker@kreis-warendorf.de
</div>
<div class="logos-end">
  <img class="footer-logo py-2" src="/terrestris-logo-normal.svg" />
  <img class="footer-logo py-2" src="/warendorf_logo.png" />
  <img class="footer-logo py-2" src="/eu_nextgen_logo.png" />
</div>

### 🗣️ **08.05. 10 Uhr** - Webseminar mundialis
#### "Offene Geodaten der Bundesländer: Verfügbarkeit und Anwendung in der Einzelbaumerkennung"
