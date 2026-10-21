# SAP RAP Fiori App: Produkt- & Kategorieverwaltung

Ein vollständiges End-to-End Projekt im **SAP RESTful Application Programming Model (RAP)** zur Verwaltung von Produktkategorien und Produkten (Entwickelt als Hochschulprojekt an der THM). Das Projekt umfasst die Datenbankmodellierung, ABAP-Programme, mehrschichtige Core Data Services (CDS), UI-Annotationen für SAP Fiori Elements sowie Service Bindings (OData V4).

---

## 🛠️ Technologien & Architektur

* **Backend & Programmiersprache:** SAP ABAP / ABAP Cloud
* **Entwicklungsumgebung:** ABAP Development Tools (ADT) in Eclipse & SAP GUI
* **Datenbank & Data Dictionary:** SAP HANA DDIC (Domains, Data Elements, Transparente Tabellen)
* **Data Modeling:** Core Data Services (CDS Views: Interface, Reuse & Consumption Layer)
* **UI & Frontend:** SAP Fiori Elements (List Report & Object Page)
* **Service Layer:** OData V4 (Service Definition & Service Binding)
* **Architektur-Pattern:** ABAP RESTful Application Programming Model (RAP) mit Draft-Handling

---

## 📂 Projektstruktur & Aufgaben

Das Projekt ist in folgende logische Phasen unterteilt :

1. **Datenschicht & Seeding (Aufgabe 1 & 2):**
   * Erstellung von individuellen Domains und Data Elements (`INT4`, `CHAR`, etc.).
   * Anlage der Datenbanktabellen für Produktgruppen (`Z_..._G`) und Produkte (`Z_..._P`) mit Fremdschlüsselbeziehung.
   * Entwicklung eines ABAP-Programms zum automatischen Befüllen und Sortieren der Tabellendaten.

2. **Core Data Services - CDS Layer (Aufgabe 3):**
   * **Interface Views:** Verknüpfung der Tabellen mittels `Left Outer Join` und Aggregation (`count(distinct ...)`) für die Anzahl der Produkte je Kategorie.
   * **Reuse Views (Business Object Layer):** Definition der Hierarchie mit `composition` und `association to parent`.
   * **Consumption Views (Projection Layer):** Bereitstellung als `transactional_query` inklusive Umleitung der Assoziationen.

3. **OData Service & SAP Fiori App (Aufgabe 3.5 & 3.6):**
   * Erstellung einer Service Definition und eines Service Bindings (`OData V4 - UI`).
   * Bereitstellung einer responsiven SAP Fiori List Report und Object Page Anwendung.

4. **UI-Annotationen & Metadata Extensions (Aufgabe 4):**
   * Konfiguration von Filterfeldern, Tabellenspalten, Quickinfos und Facetten über separate Metadata Extensions (`@Metadata.layer: #CUSTOMER`).

5. **Draft Handling & Behavior Definitions (Aufgabe 5):**
   * Implementierung des Draft Handlings für das interaktive Anlegen, Bearbeiten und Löschen von Datensätzen direkt in der Fiori App.

---

## 📄 Dokumentation
Die vollständige, bebilderte Schritt-für-Schritt-Dokumentation aller Arbeitsschritte (inklusive Eclipse- und SAP-GUI-Screenshots) findest du hier:
👉 **(https://github.com/amri81/sap-rap-fiori-product-management/blob/main/docs/Dokumentation%20der%20KSW-Pflicht%C3%BCbung.pdf)**
