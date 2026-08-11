# Kinderspielstadt Los Ämmerles e.V.

Diese Seite ist auch [auf Deutsch verfügbar](https://github.com/Los-Aemmerles/.github/blob/main/profile/README.de.md).

Non-profit association in Ammerbuch — we are digitalising the [Kinderspielstadt](https://de.wikipedia.org/wiki/Kinderstadt) “Los Ämmerles”.

In our summer camp, children experience everyday life and society through realistic roles — baker, bank clerk, carpenter, and many more. Together with our client apps, **children and staff** use this software during the camp.

Every participant has a personal employee number and signs in with it. Staff check the children in at the gate in the morning, and a terminal at the job center shows which companies still have places free and what they pay per hour in the camp's own currency. A child takes a job, works at minimum 1 hour, and can move on to another company later; the server keeps track of who currently works where and archives every past job as an employment history. Companies and participants can also work part time, with separate morning and afternoon shifts per weekday.

All apps talk to a single backend, the [la-server](https://github.com/Los-Aemmerles/la-server), over a documented REST API. Nothing is hard-wired to Ämmerles: the camp's name, currency, colours, and logo come from a per-camp configuration that the server hands out to every client, so another Kinderspielstadt can run the same software with its own branding.

For the 2026 summer camp, the software covers the following functions:

- **Check-in and check-out** — staff record when a child arrives and leaves ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Job center** — staff assign a job to a child and print the work slip ([la-client](https://github.com/Los-Aemmerles/la-client))
- **Job board** — kiosk screen showing which jobs are still open ([la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk))
- **Post office** — look up which company a child is currently working at ([la-client](https://github.com/Los-Aemmerles/la-client))
- and many other functions

All code here is open source under the [MIT license](https://opensource.org/licenses/MIT).

## Projects

| Repository                                                                    | Description                                                                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [la-server](https://github.com/Los-Aemmerles/la-server)                       | Central backend for all client apps: Python Flask REST API with a MariaDB database, JWT sign-in for employees, staff, and admins, and endpoints for companies, jobs, attendance, and village branding |
| [la-client](https://github.com/Los-Aemmerles/la-client)                       | Windows desktop app (C# / WPF, .NET 8) giving staff easy access to the camp database, with receipt printer and scanner support           |
| [la-jobcenter-kiosk](https://github.com/Los-Aemmerles/la-jobcenter-kiosk)     | Full-screen display app (Python / PySide6) for the job board screen — shows the companies' open job slots live from the la-server, with traffic-light availability, hourly pay, and automatic refresh |

## Data protection

The software stores children's names and attendance during camp operation. **No repository in this organisation contains real participant data** — only sample or test data. Personal data from live camps is handled separately in accordance with the GDPR (DSGVO) and our association's privacy practices.

## Contributing

New to the project? Browse [good first issues across our repositories](https://github.com/orgs/Los-Aemmerles/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22).

- Bug reports and feature ideas: use **Issues** in the relevant repository
- Code changes: **Pull requests** welcome; see `CONTRIBUTING.md` in each repo
- Security issues: **do not** use public issues — see `SECURITY.md` in each repo

## Links

- Website: [los-aemmerles.de](https://los-aemmerles.de)
- Contact: [developers@los-aemmerles.org](mailto:developers@los-aemmerles.org)
- Funding: [los-aemmerles.de/verein/](https://los-aemmerles.de/verein/)
- License: MIT — Copyright © Kinderspielstadt Los Ämmerles e.V.
