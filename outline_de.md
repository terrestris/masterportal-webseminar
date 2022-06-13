# Outline Masterportal Webinar

## Konzept

- Voraufgezeichneter Talk ca. 1 h
- Live Fragerunde am Ende (mit Moderator) ca. 15-20 min?
    - Im Chat oder per Audio-Meldung

## Ablauf

1. Vorstellung der IP durch Dataport

|Zeit<div style="width:50px">|Inhalt<div style="width:290px"/>|Sprecher|
|---|---|---|
|15 min|Vorstellung der IP|Dataport|
|10 min|"Theorieteil" Konfiguration<br>  - Global vs. Portalspezifisch<br> -Layer<br> -Services|Hannes|
|25 min|Live Konfiguration|Hannes|
|20 min|Ausblick<br>- geplante Entwicklungen|   |


## Konkrete Inhalte

1. **Vorstellung der IP**

- Wie ist die IP organisiert? (Meetings vorstellen)
- Welche Aufgaben hat die IP?
- Wer ist Mitglied

2. **Vorstellung Theorieteil**

- Framework / Basiskomponenten
    - Vue.js
    - Openlayers
    - Bootstrap 5
- Konfiguration (Applikationskontext)
    - `services.json`
    - `rest-services.json`
    - `style.json`
    - `config.js`
    - `config.json`

Jeweils allgemeine Erläuterung und konkrete Beispiele. Siehe hierzu: [Masterportal WS auf der FOSSGIS 2022](https://terrestris.github.io/masterportal-ws/latest/config/)

3. **Live Konfiguration**

- Auschecken der letzten stabilen Version
- Dev-Environment starten
- Start: `basic` Portal
- Sukzessive Konfiguration des Portals:
    - Layer (WMS, WFS, WMTS)
    - Rest-Services: Print und Suche
    - Werkzeuge.
    - Logo und Basic Farben
    - ...

4. **Ausblick**

- Module in Entwicklung
- Abschluss Migration
- Einbettung in CMS
- ...
