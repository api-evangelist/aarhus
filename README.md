# Aarhus University (aarhus)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Aarhus University (Aarhus Universitet) is a public research university in Aarhus, Denmark, founded in
1928. This repository catalogs the university's public developer and API footprint as an
[APIs.json](https://apisjson.org) profile.

Aarhus runs no central developer portal and no public API program. Its one genuinely
institution-operated, publicly readable machine-readable surface is the **OAI-PMH metadata harvesting
service at `pure.au.dk/ws/oai`**, which is live and fully functional. Everything else in its
programmable footprint is a vendor's product running under the institution's name.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/aarhus/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=aarhus-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party
- University — Public Research University

## Tags

University, Higher Education, Education, Research, Research Repository, Open Access, OAI-PMH,
Identity Federation, Research Computing, Course Catalog, Denmark, Nordic, Europe

## Surfaces, and who operates each one

A university is a federation of buyers, not a producer. Every surface below carries an **operator**:
`institution` means Aarhus runs the thing the contract describes, `tenant` means Aarhus runs the
deployment but a vendor wrote the contract.

| Surface | Operator | What it is |
|---|---|---|
| [OAI-PMH Metadata Service](https://pure.au.dk/ws/oai?verb=Identify) | **institution** | OAI-PMH 2.0, verified live. Identifies as the Aarhus University repository, administered from `pure@au.dk`, earliest datestamp 2005-06-02. Five metadata prefixes (`oai_dc`, `mods`, `fi-person`, `ddf-mxd`, `xmetadiss`), OpenAIRE CERIF 1.2 profile declared, sets by person/publication/year, and Aarhus authors' ORCID iDs inline in the records. |
| [Course Catalogue](https://kursuskatalog.au.dk/en) | **institution** | Web application only. No API, no JSON, and no real sitemap — `/sitemap.xml` returns the app shell with HTTP 200, which is a soft-404. |
| [Elsevier Pure REST API](https://pure.au.dk/ws/api) | tenant | Aarhus's data, Elsevier's contract. Gated: HTTP 401 unauthenticated. The specification is **not kept in this repository** — see below. |
| [Timetable](https://timetable.au.dk/) | tenant | MyTimetable by Semestry, on an au.dk host. The iCal feeds are a vendor product feature. |
| [ERDA Research Data Archive](https://erda.au.dk/) | tenant | Aarhus's deployment of the University of Copenhagen SCIENCE ERDA / MiG platform. No public API. |

## Why there are no OpenAPI definitions here

This profile previously carried **37 OpenAPI definitions and 128 derived artifacts**. Every one of
them was the **Elsevier Pure product contract** — `info.title: "Pure API"`, `info.contact.email:
pure-support@elsevier.com`, `version: 5.35.3-4` — split one file per tag by our own refine step, and
the same document is shipped by at least ten other institutions in this catalog.

The deployment at `pure.au.dk` is real and it is Aarhus's. The **contract is Elsevier's**, and keeping
it here credited Aarhus University with Elsevier's engineering. All 128 files were removed on
2026-08-30 and the relationship is recorded instead as a `tenant` entry in `apis.yml`. The
specification remains publicly readable at https://pure.au.dk/ws/api/openapi.json for anyone who
wants to inspect the product; it belongs in Elsevier's own profile, not in Aarhus University's.

**A correct profile that lowers a score is the pipeline working.**

## Domain standards

Measured against the Kin Score `education` regime — see
[conformance/aarhus-conformance.yml](conformance/aarhus-conformance.yml). Probed, not claimed:

- **OAI-PMH 2.0** — conformant, verified across `Identify`, `ListMetadataFormats`, `ListSets` and `ListRecords`.
- **ORCID** — conformant. Aarhus researchers' ORCID iDs are emitted inline in the harvested Dublin Core.
- **SAML 2.0** — conformant. `au.dk` is carried as a `shibmd:Scope` in the WAYF national federation aggregate; WAYF is operated by DeiC and connected to eduGAIN.
- **Shibboleth** — unverified. The federation metadata uses the Shibboleth namespace, but Aarhus's own IdP metadata is not publicly resolvable (`idp.au.dk` and `login.au.dk` do not resolve).
- **Not claimed:** `lti`, `scim`, `oneroster`, `ed-fi`, `caliper`, `qti`, `datacite`, `crossref`. DOIs in the harvested metadata are publisher-registered and cited, not minted by Aarhus.

## Plans, Rate Limits, FinOps

- [plans/aarhus-plans-pricing.yml](plans/aarhus-plans-pricing.yml)
- [rate-limits/aarhus-rate-limits.yml](rate-limits/aarhus-rate-limits.yml)
- [finops/aarhus-finops.yml](finops/aarhus-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Common Properties

- Website: https://www.au.dk/en/
- Research Repository: https://pure.au.dk/portal/
- Course Catalog: https://kursuskatalog.au.dk/en
- Identity Federation: https://wayf.au.dk/
- Research Computing (GenomeDK): https://genome.au.dk/ — [docs](https://genome.au.dk/docs/)
- Library Catalog: https://library.au.dk/en
- AI Policy (students): https://studerende.au.dk/en/gai
- AI Tooling (staff): https://medarbejdere.au.dk/en/administration/it/guides/using-gai-responsibly
- Privacy Policy: https://international.au.dk/about/profile/privacy-policy/
- security.txt: https://au.dk/.well-known/security.txt
- GitHub: https://github.com/cs-au-dk
- LinkedIn: https://www.linkedin.com/school/aarhus-university/
- Review: review.yml

## Notes

All entries were re-verified live on **2026-08-30**. No endpoints were fabricated.

- **Correction to the 2026-06-03 review:** it recorded the OAI-PMH `Identify` verb as returning
  HTTP 500. It now returns a valid HTTP 200 OAI-PMH response, and the whole service is functional.
- No central developer or open-data portal exists: `api.au.dk`, `data.au.dk`, `developer.au.dk`,
  `open.au.dk`, `opendata.au.dk` and `services.au.dk` all return NXDOMAIN.
- `au.dk/llms.txt` returns 404.
- GenomeDK, the university's HPC facility, is documented across 78 pages but exposes no API.
- The `cs-au-dk` GitHub organization is a Computer Science departmental org. Aarhus has several
  departmental and research orgs but no single central one.
- The LinkedIn school page returns HTTP 999 due to LinkedIn bot blocking, not absence.

## Maintainers

- Kin Lane — kin@apievangelist.com
