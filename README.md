# Handelsregister


## Phasenplan

### 1. Kickoff und Konzept

- Gemeinsam klären: Welche Daten braucht das Gewerberegister?
- Use Cases festlegen: Unternehmen registrieren, Mitarbeiter zuordnen, Löhne melden, Steuerdaten bereitstellen.
- Schnittstellen mit den anderen Teams abstimmen.
- Ergebnis: Datenmodell-Skizze, User Stories, API-Liste.

### 2. Datenmodell und Backend

- Django-Projekt anlegen.
- Modelle erstellen, zum Beispiel:
    - `Gewerbe`: Name, Rechtsform, Branche, Adresse, Status
    - `Arbeitnehmer`: Verweis auf Bürger, Unternehmen, Rolle, Gehalt
    - `Transaktionen` : Einkommen, Datum, Zweck
    - `Berechtigungen` / Rolle: Admin, Unternehmen, Behörde 
- Django-Admin für erste Tests nutzen.

### 3. API entwickeln

- REST-Endpunkte für Unternehmen, Mitarbeiter und Einkommen.
- Beispiele:
    - `GET /gewerbe/`
    - `POST /gewerbe/`
    - `GET /gewerbe/{id}/arbeitnehmer/`
    - `POST /gewerbe/{id}/transaktionen/`
- Authentifizierung und Berechtigungen einbauen.
- API-Dokumentation erstellen.

### 4. GUI bauen

- Übersicht aller Unternehmen mit Suche und Filter.
- Unternehmensprofil mit Stammdaten und Mitarbeitern.
- Formular zur Unternehmensregistrierung.
- Ansicht für Mitarbeiterzuordnung.
- Optional: Dashboard für Umsatz, Löhne oder offene Steuern.

### 5. Integration mit anderen Teams

- Personenregister: Bürger als Mitarbeiter identifizieren.
- Bankenregister: Kontoverbindung, Lohnzahlungen, Steuern.
- Infrastrukturregister: Unternehmensstandort, Straßen-/Infrastrukturbezug.
- Gemeinsame Testfälle definieren: „Unternehmen wird gegründet → Mitarbeiter werden zugewiesen → Lohn wird gezahlt → Steuer entsteht.“

### 6. Testen und abgeben

- Funktionstests: Registrierung, Suche, API-Zugriffe, Berechtigungen.
- Integrationstest mit mindestens einem anderen Register.
- Demo vorbereiten: Ablauf von Unternehmensgründung bis Steuerzahlung.
- Dokumentation und Präsentation finalisieren.