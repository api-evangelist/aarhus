# Aarhus University (aarhus)

Aarhus University (Aarhus Universitet) is a public research university in Aarhus, Denmark, founded in 1928 and ranked #144 in the QS World University Rankings 2025. This repository catalogs the university's public developer and API footprint as an [APIs.json](https://apisjson.org) profile. Aarhus does not run a unified public developer portal; its most concrete machine-readable surface is the Pure research portal, with most code activity living in departmental GitHub organizations.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/aarhus/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=aarhus-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, Open Data, Denmark, Europe

## APIs

- **Pure Research Portal Web Service (REST)** — Elsevier Pure research information API for research outputs, persons, and projects. Gated (HTTP 401 unauthenticated). Docs: https://pure.au.dk/portal/
- **Pure OAI-PMH Metadata Service** — OAI-PMH harvesting of research-output metadata. Path resolves; Identify verb errored during review. Base: https://pure.au.dk/ws/oai — Docs: https://pure.au.dk/portal/
- **Course Catalogue and Timetable (mitstudie / STADS)** — Public course catalogue plus the mitstudie.au.dk student self-service environment with iCal timetable export. Docs: https://kursuskatalog.au.dk/en and https://studerende.au.dk/en/it-support/mitstudieaudk/

## Plans

See [plans/aarhus-plans-pricing.yml](plans/aarhus-plans-pricing.yml).

## Rate Limits

See [rate-limits/aarhus-rate-limits.yml](rate-limits/aarhus-rate-limits.yml).

## FinOps

See [finops/aarhus-finops.yml](finops/aarhus-finops.yml).

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.au.dk/en/
- GitHub: https://github.com/cs-au-dk
- LinkedIn: https://www.linkedin.com/school/aarhus-university/
- Plans: plans/aarhus-plans-pricing.yml
- Rate Limits: rate-limits/aarhus-rate-limits.yml
- FinOps: finops/aarhus-finops.yml
- Review: review.yml

## Notes

All entries were verified live on 2026-06-03. No endpoints were fabricated. The Pure REST API is gated (HTTP 401 without credentials). The Pure OAI-PMH base path resolves but the Identify verb returned HTTP 500 and should be re-verified. The course catalogue and timetables are web/iCal based rather than documented open APIs. The cs-au-dk GitHub organization is a Computer Science departmental org; Aarhus has multiple departmental/research orgs (e.g., CDS-AU-DK, AU-DIS, logsem) but no single central organization. The LinkedIn school page returns HTTP 999 due to LinkedIn bot blocking, not absence.

## Maintainers

- Kin Lane — kin@apievangelist.com
