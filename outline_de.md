# Konzept Masterportal Webseminar 2024

- Live Talk ca. 1 h
- Live Fragerunde am Ende (mit Moderator) ca. 15-20 min?
    - Im Chat oder per Audio-Meldung

## Ablauf

1. Vorstellung der IP durch Dataport

|Zeit<div style="width:50px">|Inhalt<div style="width:290px"/>|Sprecher|
|---|---|---|
|5 min|Begrüßung und Vorstellung terrestris|Hannes|
|15 min|Vorstellung der IP|Dataport?|
|10 min|Überblick: Neuigkeiten v3 und Konfigurationsmöglichkeiten|Hannes|
|20 min|Live Konfiguration|Hannes|
|10 min|Offene Fragerunde|Alle|

## Einladung / Zielgruppe

- dataport integrieren
- übliche Kanäle (website, social media)
- Bestandskunden darauf aufmerksam machen

## Konkrete Inhalte

1. **Vorstellung der IP**

- Wie ist die IP organisiert?
    - Kommittees und Meetings vorstellen
- Welche Aufgaben hat die IP?
- Wer ist bereits Mitglied, welche Vorteile habe ich als Mitglied?

2. **Neuigkeiten und Konfigurationsmöglichleiten**

- Kurz: Framework und Software Stack
- Migration zu v3
    - Was ist zu beachten bei der Migration?
    - Kurzvorstellung neuer Module
- Möglichkeiten zur Integration
    - Einbettung bestehender Daten und Dienste
    - Integration von Suchbackends
- Userverwaltung    

3. **Live Konfiguration**

- Auschecken der LTS und Installation von Abhängigkeiten
- Dev-Environment starten
    - Im Hintergrund Docker-GDI starten (pygeoapi, postgres, geoserver)
- Migration `npm run migrateConfig`
    - Kurze Erläuterung des Logs
- Anpassung an v3
- Exemplarische Konfiguration der Suche
- Anbindung an Nutzerverwaltung (Keycloak)
