# Kinderspielstadt Los Ämmerles e.V.

> This page is also available in [English](https://github.com/Los-Aemmerles/.github/blob/main/profile/README.md).

Wir sind ein gemeinnütziger Verein in Ammerbuch und digitalisieren die [Kinderspielstadt](https://de.wikipedia.org/wiki/Kinderstadt) „Los Ämmerles“.

In unserem Sommercamp lernen Kinder den Alltag und das gesellschaftliche Zusammenleben kennen, indem sie realitätsnahe Rollen übernehmen — beispielsweise in einer Bäckerei, einer Bank oder einer Schreinerei. **Kinder und Betreuer** nutzen diese Software während des Camps gemeinsam.

Jeder Teilnehmer erhält eine persönliche Mitarbeiternummer, mit der er sich anmeldet. Morgens erfassen Betreuer am Eingang die Ankunft der Kinder. Auch das Verlassen des Camps kann protokolliert werden. Ein Bildschirm im Jobcenter zeigt, welche Firmen noch freie Stellen haben und welchen Stundenlohn sie in der Camp-Währung zahlen.

Ein Kind kann einen Job annehmen und muss ihn mindestens eine Stunde lang ausüben. Danach kann es zu einer anderen Firma wechseln, das Arbeitsamt is auch eine mögliche Firma. Der Server behält den Überblick darüber, wer gerade wo arbeitet und welche Stellen noch frei sind. Jeder abgeschlossene Arbeitseinsatz wird in einer Beschäftigungshistorie erfasst, um spätere Auswertungen zu ermöglichen.

Alle Apps kommunizieren über eine dokumentierte REST-API mit einem zentralen Backend, dem [la-server](https://github.com/Los-Aemmerles/la-server). Die Software ist nicht an Los Ämmerles gebunden: Name, Währung, Farben und Logo stammen aus einer campbezogenen Konfiguration, die der Server an alle Clients ausliefert. So kann jede andere Kinderspielstadt dieselbe Software mit ihrem eigenen Erscheinungsbild einsetzen.

Beim Sommercamp 2026 bot die Software unter anderem folgende Funktionen:

- **Check-in und Check-out** — Betreuer erfassen, wann Kinder das Camp betreten und verlassen ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Jobcenter** — Kinder wählen selbst einen Job aus oder bekommen ihn von Betreuern zugewiesen; anschließend wird der Arbeitsschein ausgedruckt ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Jobbörse** — Ein Kiosk-Bildschirm zeigt die noch verfügbaren Stellen ([la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk))
- **Postamt** — Betreuer können nachsehen, in welcher Firma ein Kind gerade arbeitet, um die Post verteilen zu können ([la-client](https://github.com/Los-Aemmerles/la-client))
- viele weitere Funktionen

Der hier veröffentlichte Code steht unter der [MIT-Lizenz](https://opensource.org/licenses/MIT) und ist damit Open Source.

## Projekte

| Repository                                                                    | Beschreibung                                                                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [la-setup](https://github.com/Los-Aemmerles/la-setup)                         | Dokumentation zur Durchführung unseres Sommercamps — **in Arbeit** |
| [la-server](https://github.com/Los-Aemmerles/la-server)                       | Zentrales Backend für alle Client-Apps: eine mit Python und Flask entwickelte REST-API mit MariaDB-Datenbank, JWT-Authentifizierung für Mitarbeiter, Betreuer und Administratoren sowie Endpunkten für Firmen, Jobs, Anwesenheit und das Erscheinungsbild der Spielstadt |
| [la-client](https://github.com/Los-Aemmerles/la-client)                       | Windows-Desktop-App (C# / WPF, .NET 8), die Betreuern einen komfortablen Zugriff auf die Camp-Datenbank ermöglicht und Belegdrucker sowie Scanner unterstützt |
| [la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk)     | Vollbildanwendung (Python / PySide6) für die Jobbörse — zeigt anhand der Daten des la-server in Echtzeit die freien Stellen der Firmen mit Ampelstatus, Stundenlohn und automatischer Aktualisierung |

## Datenschutz

Während des Camps speichert die Software die Namen und Anwesenheitsdaten der Kinder. **Kein Repository dieser Organisation enthält echte Teilnehmerdaten** — ausschließlich Beispiel- oder Testdaten. Personenbezogene Daten aus dem laufenden Campbetrieb werden getrennt von den Repositories gespeichert und gemäß der DSGVO sowie den Datenschutzrichtlinien unseres Vereins verarbeitet.

## Mitwirken

Neu dabei? Werfen Sie einen Blick auf die [Good First Issues in unseren Repositories](https://github.com/orgs/Los-Aemmerles/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) oder kontaktieren Sie uns.

- Fehler und Funktionswünsche: Erstellen Sie ein **Issue** im jeweiligen Repository
- Codeänderungen: **Pull Requests** sind willkommen — beachten Sie `CONTRIBUTING.md` im jeweiligen Repository
- Sicherheitslücken: **Bitte nicht** über öffentliche Issues melden — beachten Sie `SECURITY.md` im jeweiligen Repository

## Links

- Website: [los-aemmerles.de](https://los-aemmerles.de)
- Kontakt: [developers@los-aemmerles.org](mailto:developers@los-aemmerles.org)
- Unterstützen Sie uns: [los-aemmerles.de/verein/](https://los-aemmerles.de/verein/)
- Lizenz: MIT — Copyright © Kinderspielstadt Los Ämmerles e.V.
