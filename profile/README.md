# Kinderspielstadt Los Ämmerles e.V.

Diese Seite ist auch [auf Deutsch verfügbar](https://github.com/Los-Aemmerles/.github/blob/main/profile/README.de.md).

We are a non-profit organisation based in Ammerbuch, Germany, dedicated to digitising the [Kinderspielstadt](https://de.wikipedia.org/wiki/Kinderstadt) “Los Ämmerles”.

At our summer camp, children learn about everyday life and society by taking on realistic roles — for example, working as bakers, bank clerks or carpenters. **Children and staff** use this software together throughout the event.

Each participant is assigned a unique employee number, which they use to sign in. Every morning, staff record the children's arrival at the gate. They can also record when children leave the camp. A display in the job centre shows which companies still have vacancies and the hourly wage they pay in the camp's own currency.

A child can take a job and must work there for at least one hour. Afterwards, they can move to another company, the employment office is also a possible company. The server keeps track of where everyone is currently working and which positions remain vacant. Each completed job is recorded in an employment history, enabling later analysis.

All apps communicate with a central backend, the [la-server](https://github.com/Los-Aemmerles/la-server), through a documented REST API. The software is not tied to Los Ämmerles: the camp's name, currency, colours and logo come from a camp-specific configuration that the server distributes to every client. This allows any other Kinderspielstadt to use the same software with its own branding.

At the 2026 summer camp, the software provided the following features:

- **Check-in and check-out** — Staff record arrivals and departures ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Job centre** — A job is assigned to a child and a work slip is printed ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Job board** — A kiosk display shows the positions that are still available ([la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk))
- **Post office** — Staff look up where a child is currently working so that mail can be delivered ([la-client](https://github.com/Los-Aemmerles/la-client))
- Many more features

All code published here is open source under the [MIT License](https://opensource.org/licenses/MIT).

## Projects

| Repository                                                                | Description |
|---------------------------------------------------------------------------|-------------|
| [la-server](https://github.com/Los-Aemmerles/la-server)                   | Central backend for all client apps: a REST API built with Python and Flask, backed by MariaDB, with JWT authentication for employees, staff and administrators, plus endpoints for companies, jobs, attendance and the play city's branding |
| [la-client](https://github.com/Los-Aemmerles/la-client)                   | Windows desktop app (C# / WPF, .NET 8) that gives staff convenient access to the camp database and supports receipt printers and scanners |
| [la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk) | Full-screen job board display (Python / PySide6) showing companies' vacancies in real time using data from the la-server, with colour-coded availability, hourly wages and automatic updates |

## Data protection

During camp operations, the software stores children's names and attendance records. **No repository in this organisation contains real participant data** — only sample or test data. Personal data from active camps is stored separately from the repositories and processed in accordance with the GDPR and our association's privacy policies.

## Contributing

New to the project? Browse the [Good First Issues across our repositories](https://github.com/orgs/Los-Aemmerles/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) or contact us.

- Bug reports and feature requests: use **Issues** in the relevant repository
- Code changes: **Pull requests** are welcome — see `CONTRIBUTING.md` in the relevant repository
- Security vulnerabilities: **please do not** report them through public issues — see `SECURITY.md` in the relevant repository

## Links

- Website: [los-aemmerles.de](https://los-aemmerles.de)
- Contact: [developers@los-aemmerles.org](mailto:developers@los-aemmerles.org)
- Support us: [los-aemmerles.de/verein/](https://los-aemmerles.de/verein/)
- Licence: MIT — Copyright © Kinderspielstadt Los Ämmerles e.V.
