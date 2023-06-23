# Projektbeschreibung
## Ziel des Projektes
Entwicklung eines webbasierten Zeiterfassungssystems für Kleinunternehmen

## Anforderungen
Die Anforderungen wurden in Kooperation mit einem lokalen Buchladen(4 Mitarbeiter) erarbeitet.
### Registrierung
Unternehmen könnnen sich mit Emailadresse/Passwort registrieren. Nach der Registierierung erhalten die Kunden eine Bestätigungsemail mit einem Link zur Bestätigung der E-Mail-Adresse. Nach der Bestätigung der E-Mail-Adresse kann der Benutzer sich anmelden und landet auf dem Dashboard. Der Registrierungsprozess ist danach abgeschlossen.
### Hinzufügen der Mitarbeiter
Das Hinzufügen von Mitarbeiter erfolgt über ein Formular in der Benutzeroberfläche und ist nur für Benutzer mit entsprechenden Rechten möglich. Nach dem ein Mitarbeiter hinzugefügt wird bekommt er einen Einladungslink per E-Mail. Über diesen Link kann er sein Passwort festlegen und wir automatisch eingeloggt. Das Unternehmen bzw. berechtigte Benutzer werden über den Abschluss des Prozesse informiert.Der Prozess ist damit abgeschlossen.
### Stundenverwaltung Unternehmen
Das Unternehmen kann wöchentliche/monatliche Soll-Stunden für einen Mitarbeiter definieren. Bei Überschreitung der festgelegten Stunden soll das Unternehmen benachrichtigt werden. 
### Zeiterfassung Mitarbeiter
Mitarbeiter haben die Möglichkeit nach dem Einloggen in die Anwendung einzustempeln/auszustempeln. Nach 10h Arbeitszeit wird jeder Mitarbeiter automatisch ausgestempelt. Nach dem Austempeln soll der aktuelle Stand der Minus/Über-stunden angezeigt werden. Ein Mitarbeiter hat keine Möglichkeit seine Zeiten nachträgtlich zu bearbeiten. Dies kann nur durch durch berechtigte Personen erfolgen. Die Anfrage zur Änderung von Zeiten wird nicht in dieser Anwendung abgebildet.
### Auswertung Stunden
Jeder Mitarbeiter hat die Möglichkeit seine geleisteten Stunden einzusehen. Hierbei soll auf monatlicher Basis das Anzeigen der erbrachten Stunden möglich sein. Auch eine einfache grafische Darstellung soll mittels Balkendiagramm soll das Verständnis erleichtern. Diese Auswertungsmöglichkeit soll es auch für das Unternehmen geben.
### Benutzerkonto
Jeder Benutzer hat die Möglichkeiten sein Passwort zu ändern. Änderungen anderer Attribute kann nur durch das Unternehmen erfolgen und nicht durch den Mitarbeiter direkt. Auch das Löschen des Benutzerkontos ist nur über das Unternehmen möglich. 

## Technische Details
### Frontend
Hier wird auf das Javascript Frontend Framework SvelteKit(1.20.5) und Tailwind CSS gesetzt.
### Backend 
Es soll eine REST-API in Go 1.20 implementiert werden.
### Datenspeicherung & Backup
Die Daten sollen in einer PostgreSQL-Datenbank (Version 15) gespeichert werden. Diese Datenbank läuft auf einem einfachen V-Server um Kosten zu sparen. Es sollen tägliche Backups durchgeführt werden und an einem anderen Ort gespeichert werden.

## Ablauf des Projektes
### 1. Erstellung Design Prototyp
Mit Hilfe von Figma wird ein Design Prototyp erstellt, welcher es ermöglicht ein Gefühl für die Anwendung zu erlangen. Generell soll es sich hierbei um eine SPA handeln. Der Design Prototyp dient als Fundament für alle weiteren Schritte und ermöglicht das Ableiten von Frontend Komponenten sowie Backend Business Logik.
### 2. Erstellung der REST-API 
Nachdem der Design Prototyp fertig gestellt ist wird die REST-API Konzeptioniert und implementiert. Dies umfasst auch das Aufsetzten der Datenbank sowie die Migration der Tabellen. Auch das schreiben von Tests spielt hier eine große Rolle, es soll eine Test-Coverage von min. 80% erreicht werden.
### 3. Erstellung des Frontends
Hierbei wird sich am Design Prototyp orientiert und die REST-API verwendent, um auf den Daten arbeiten zu können.

