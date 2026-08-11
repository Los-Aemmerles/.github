# Kinderspielstadt Los Ämmerles e.V.

This page is also [available in English](https://github.com/Los-Aemmerles/.github/blob/main/profile/README.md).

Gemeinnütziger Verein in Ammerbuch — wir digitalisieren die [Kinderspielstadt](https://de.wikipedia.org/wiki/Kinderstadt) „Los Ämmerles“.

In unserem Sommercamp erleben Kinder Alltag und Gesellschaft in realistischen Rollen — als Bäcker, Bankangestellte, Schreiner und vieles mehr. **Kinder und Betreuer** nutzen diese Software gemeinsam mit unseren Client-Apps während der Veranstaltung.

Jeder Teilnehmer erhält eine persönliche Mitarbeiternummer und meldet sich damit an. Morgens erfassen Betreuer am Tor die Ankunft der Kinder. Ein Terminal im Jobcenter zeigt, welche Firmen noch Plätze frei haben und welchen Stundenlohn sie in der Camp-Währung zahlen.

Ein Kind nimmt einen Job an und arbeitet mindestens eine Stunde. Später kann es zu einer anderen Firma wechseln. Der Server behält den Überblick, wer gerade wo arbeitet. Jeden vergangenen Job legt er in der Beschäftigungshistorie ab.

Firmen und Teilnehmer können auch in Teilzeit arbeiten — mit getrennten Vormittags- und Nachmittagsschichten an jedem Wochentag.

Alle Apps kommunizieren über eine dokumentierte REST-API mit einem zentralen Backend, dem [la-server](https://github.com/Los-Aemmerles/la-server). Die Software ist nicht an Ämmerles gebunden: Name, Währung, Farben und Logo des Camps kommen aus einer camp-spezifischen Konfiguration, die der Server an jeden Client ausliefert — so kann jede andere Kinderspielstadt dieselbe Software mit eigenem Erscheinungsbild einsetzen.

Für das Sommercamp 2026 umfasst die Software folgende Funktionen:

- **Check-in und Check-out** — Betreuer erfassen Ankunft und Abgang ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Jobcenter** — Betreuer weisen einem Kind einen Job zu und drucken den Arbeitsschein ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Jobbörse** — Kiosk-Bildschirm mit noch offenen Stellen ([la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk))
- **Postamt** — Abfrage, bei welcher Firma ein Kind gerade arbeitet ([la-client](https://github.com/Los-Aemmerles/la-client))
- und viele weitere Funktionen

Der hier veröffentlichte Code ist Open Source unter der [MIT license](https://opensource.org/licenses/MIT).

## Projekte

| Repository                                                                    | Beschreibung                                                                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [la-server](https://github.com/Los-Aemmerles/la-server)                       | Zentrales Backend für alle Client-Apps: Python-Flask-REST-API mit MariaDB-Datenbank, JWT-Anmeldung für Mitarbeiter, Betreuer und Admins sowie Endpunkte für Firmen, Jobs, Anwesenheit und das Erscheinungsbild der Spielstadt |
| [la-client](https://github.com/Los-Aemmerles/la-client)                       | Windows-Desktop-App (C# / WPF, .NET 8) für den bequemen Zugriff der Betreuer auf die Camp-Datenbank, mit Unterstützung für Belegdrucker und Scanner           |
| [la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk)     | Vollbild-Anzeige (Python / PySide6) für den Jobbörsen-Bildschirm — zeigt die freien Stellen der Firmen in Echtzeit vom la-server, mit Ampelstatus, Stundenlohn und automatischer Aktualisierung |

## Datenschutz

Die Software speichert im Camp-Betrieb Namen und Anwesenheit von Kindern. **Kein Repository dieser Organisation enthält echte Teilnehmerdaten** — nur Beispiel- oder Testdaten. Personenbezogene Daten aus laufenden Camps werden getrennt von den Repositories geführt und gemäß DSGVO sowie den Datenschutzrichtlinien unseres Vereins verarbeitet.

## Mitwirken

Neu dabei? Stöbern Sie in unseren [good first issues](https://github.com/orgs/Los-Aemmerles/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) in allen Repositories.

- Fehler und Feature-Wünsche: **Issues** im jeweiligen Repository
- Code-Änderungen: **Pull Requests** willkommen — siehe `CONTRIBUTING.md` im jeweiligen Repo
- Sicherheitslücken: **bitte nicht** über öffentliche Issues melden — siehe `SECURITY.md` im jeweiligen Repo

## Links

- Website: [los-aemmerles.de](https://los-aemmerles.de)
- Kontakt: [developers@los-aemmerles.org](mailto:developers@los-aemmerles.org)
- Unterstützung: [los-aemmerles.de/verein/](https://los-aemmerles.de/verein/)
- Lizenz: MIT — Copyright © Kinderspielstadt Los Ämmerles e.V.
