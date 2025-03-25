## Einladung zum dritten Masterportal Webseminar

Ein Datenerfassungs-AddOn für das Masterportal

![terrestris Webseminar Logo](public/terrestris_webseminar_logo.svg)

`Ein Datenerfassungs-AddOn für das Masterportal`

Die Kreisverwaltung Warendorf betreibt eine GDI mit diversen Masterportal Instanzen. Eine wiederkehrende Aufgabe ist es, einfache Geodaten zu erheben oder Alphanumerik an bestehenden Geometrien zu ändern. Das können z.B.  Winterdienststrecken sein, der Zustand von Gewerbeflächen im Eigentum des Kreises oder die Verortung von Brunnen sowie die Dokumentation von Kontrollen. Also sowohl interne Workflows, als auch Information für Bürger und Wirtschaft.  

Gut strukturierte und gut organisierte Workflows zur Datenerfassung sind essentiell für den Betrieb von Geodateninfrastrukturen. In enger Zusammenarbeit mit dem Kreis Warendorf wurde auf Basis der GDI des Kreises ein abgesichertes AddOn für das Masterportal sowie Datenbank-Frontend und -Backend entwickelt. Die eigentlichen Anwendungen oder 'Apps' werden über eine einfache Konfiguration erstellt, mit der sich relativ einfach individuelle Workflows zur Datenerfassung erzeugen lassen (Stichwort: Low-Code Plattform). 

Mit dem form-backend [1] lassen sich mittels JSON-Konfigurationen individuelle Formulare erstellen, die sowohl einfache als auch komplexe Tabellenstrukturen abbilden können. Der Datenzugriff erfolgt hierbei via PostgREST, auf eine PostgreSQL Datenbank. Für das Rendering der Formulare wurde eine Web-App mit einer Übersicht (table view) und einer Detailansicht (item view) entwickelt: In der Übersicht lassen sich alle Einträge der Tabelle bzw. der verknüpften Tabellen anzeigen, filtern und sortieren. Über entsprechende Aktionsbuttons kann in die Detailansicht gewechselt und der entsprechende Eintrag editiert werden.

Die Integration in das Masterportal bietet viele Vorteile: Es können Geometrien aus vorhandenen Vektorlayern in das Formular übernommen werden - ebenso können Geometrien gezeichnet werden oder der aktuelle Standort als Input für Formularfelder übernommen werden. Hierfür wurde ein AddOn entwickelt, das Formulare als IFrame einbindet und über die PostMessage-API mit dem Portal kommuniziert [2]. 

Die Formulare können aber auch standalone genutzt werden und funktionieren dann ohne den ganzen Overhead des Masterportals, was für viele Routineaufgaben völlig ausreicht und die Komponenten sauber trennt und eine unabhängige Weiterentwicklung gewährleistet. 

Zur Zugriffskontrolle auf die Formulare sowie auf die Daten bietet die Lösung eine Anbindung an zentrale Identity & Access Management Systeme (Keycloak). Per Konfiguration lässt sich steuern, welche Rollen welche Art von Zugriff (lesend oder schreibend) auf die Übersicht oder Detailansicht erlangen sollen. Somit sind die Formulare und Daten vor ungewollten Zugriff geschützt.

terrestris und der Kreis Warendorf möchten im Rahmen des Webseminars einen praxisnahen Einstieg in die Datenerfassungs-Lösung präsentieren und die vielfältigen Anwendungsmöglichkeiten beleuchten. Wir laden Sie und euch herzlich zum dritten kostenfreien **Masterportal Webseminar** am **08. April 2025 um 10:00 Uhr** ein.

[1] https://github.com/formcapture/form-backend
[2] https://github.com/formcapture/masterportal-addons

## Wichige Infos:

**Kosten:** Keine  
**Anmeldung:** Email an info@terrestris.de bis zum **03.04.2025** mit Betreff [Anmeldung Masterportal Webseminar]  
**Zugangslink:** Wird nach erfolgter Annmeldung mitgeteilt.
