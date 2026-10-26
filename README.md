# Solcast (solcast)

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

Solcast is a solar and renewable energy data company, acquired by DNV in 2023, that provides high-resolution, satellite-derived solar irradiance, PV power, weather forecasting, and historical climate data via a developer API. Its data covers live, forecast, historical, and typical meteorological year (TMY) datasets for rooftop PV, advanced PV, grid aggregations, and soiling models globally.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Solar
- Energy
- Forecasting
- Irradiance
- Weather
- Renewable Energy
- PV Power

## Timestamps

- **Created:** 2025-05-02
- **Modified:** 2026-05-19

## APIs

### Solcast API

The Solcast API provides live, forecast, historical, and typical meteorological year (TMY) solar irradiance, PV power, and weather data derived from a global fleet of weather satellites. It supports rooftop PV power, advanced PV power (for registered sites), grid aggregation data, and soiling loss models (Kimber and HSU). Authentication uses an API key. Data is available in JSON and CSV formats with 5- to 60-minute granularity anywhere on the planet.

- **Human URL:** [https://docs.solcast.com.au/](https://docs.solcast.com.au/)
- **Base URL:** `https://api.solcast.com.au`

#### Tags

- Solar
- Forecasting
- Irradiance
- PV Power
- Weather
- Renewable Energy
- Grid Aggregation
- Historical Data
- TMY
- Soiling

#### Properties

- [Documentation](https://docs.solcast.com.au/)
- [Getting Started](https://docs.solcast.com.au/docs/getting-started)
- [Authentication](https://docs.solcast.com.au/docs/api-authentication)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/openapi/solcast-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [S D Ks](https://solcast.com/sdk)
- [Python S D K](https://github.com/Solcast/solcast-api-python-sdk)
- [C Sharp S D K](https://github.com/Solcast/solcast-api-csharp-sdk)
- [Julia S D K](https://github.com/Solcast/Solcast.jl)
- [Rules](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/rules/solcast-rules.yml)
- [Capabilities](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/capabilities/solar-forecasting.yaml)
- [Capabilities](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/capabilities/solar-resource-assessment.yaml)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-schema/solcast-radiation-and-weather-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-schema/solcast-pv-power-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-schema/solcast-pv-power-site-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-structure/solcast-radiation-and-weather-structure.json)
- [JSON Structure](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-structure/solcast-pv-power-structure.json)
- [JSON Structure](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-structure/solcast-pv-power-site-structure.json)
- [J S O N L D Context](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/json-ld/solcast-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/vocabulary/solcast-vocabulary.yml)
- [Postman Collection](collections/solcast.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/solcast.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/solcast)
- [Portal](https://solcast.com/)
- [Documentation](https://docs.solcast.com.au/)
- [S D Ks](https://solcast.com/sdk)
- [Sign Up](https://toolkit.solcast.com.au/register)
- [Pricing](https://solcast.com/pricing/irradiance-weather)
- [Changelog](https://solcast.com/changelog)
- [Website](https://solcast.com)
- [Git Hub](https://github.com/Solcast)
- [A P I  Toolkit](https://toolkit.solcast.com.au/)
- [Terms of Service](https://solcast.com/terms-of-service)
- [Privacy Policy](https://solcast.com/privacy-policy)
- [Contact](https://solcast.com/contact)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
