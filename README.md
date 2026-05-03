# Solcast (solcast)

Solcast is a solar and renewable energy data company (acquired by DNV in 2023) that provides high-resolution, satellite-derived solar irradiance, PV power, weather forecasting, and historical climate data via a developer API. Covering live, forecast, historical, and Typical Meteorological Year (TMY) datasets, the Solcast API serves rooftop PV, advanced PV, grid aggregations, and soiling models globally — processing over 26 million API calls daily.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/solcast/refs/heads/main/apis.yml)

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
- **Modified:** 2026-05-02

## APIs

### Solcast API

Solar irradiance, PV power, weather, soiling, and grid aggregation data via REST API. Authentication uses a Bearer API key. Data available in JSON and CSV at 5- to 60-minute granularity, globally.

**Human URL:** [https://docs.solcast.com.au/](https://docs.solcast.com.au/)
**Base URL:** `https://api.solcast.com.au`

#### Tags

- Solar, Forecasting, Irradiance, PV Power, Weather, Renewable Energy, Grid Aggregation, Historical Data, TMY, Soiling

#### Properties

| Type | URL |
|---|---|
| Documentation | [https://docs.solcast.com.au/](https://docs.solcast.com.au/) |
| Getting Started | [https://docs.solcast.com.au/docs/getting-started](https://docs.solcast.com.au/docs/getting-started) |
| Authentication | [https://docs.solcast.com.au/docs/api-authentication](https://docs.solcast.com.au/docs/api-authentication) |
| OpenAPI | [openapi/solcast-openapi.yml](openapi/solcast-openapi.yml) |
| SDKs | [https://solcast.com/sdk](https://solcast.com/sdk) |
| Python SDK | [https://github.com/Solcast/solcast-api-python-sdk](https://github.com/Solcast/solcast-api-python-sdk) |
| C# SDK | [https://github.com/Solcast/solcast-api-csharp-sdk](https://github.com/Solcast/solcast-api-csharp-sdk) |
| Julia SDK | [https://github.com/Solcast/Solcast.jl](https://github.com/Solcast/Solcast.jl) |

## API Endpoints

The Solcast API is organized into six resource groups:

| Group | Description | Endpoints |
|---|---|---|
| **Live Data** | Real-time estimated actuals (last 7 days, updated every 5 min) | radiation_and_weather, rooftop_pv_power, advanced_pv_power, soiling/kimber, soiling/hsu, aggregations |
| **Forecast Data** | Forecasts up to 14 days ahead | radiation_and_weather, rooftop_pv_power, advanced_pv_power, soiling/kimber, soiling/hsu, aggregations |
| **Historic Data** | Historical data from 2007 (up to 31 days per request) | radiation_and_weather, rooftop_pv_power, advanced_pv_power, soiling/kimber, soiling/hsu |
| **TMY Data** | Typical Meteorological Year (2007–2023 average) | radiation_and_weather, rooftop_pv_power |
| **Aggregations** | Grid portfolio live and forecast aggregation | live, forecast |
| **PV Power Sites** | CRUD site management for advanced PV model | list, get, create, patch, update, delete |

## Artifacts

### OpenAPI Specification

- [openapi/solcast-openapi.yml](openapi/solcast-openapi.yml) — Full OpenAPI 3.1 spec covering all 22 endpoints across Live, Forecast, Historic, TMY, Aggregation, and PV Site Management groups.

### Spectral Rules

- [rules/solcast-rules.yml](rules/solcast-rules.yml) — Spectral ruleset enforcing Solcast API conventions: Title Case summaries, camelCase operationIds, Bearer auth, 401/429 response coverage, and schema completeness.

### Capabilities

Naftiko capability files organized by customer workflow:

| File | Workflow | Tools |
|---|---|---|
| [capabilities/solar-forecasting.yaml](capabilities/solar-forecasting.yaml) | Solar Forecasting and Real-Time Monitoring | 12 tools: live + forecast radiation, PV power, soiling, aggregations |
| [capabilities/solar-resource-assessment.yaml](capabilities/solar-resource-assessment.yaml) | Solar Resource Assessment and Yield Analysis | 13 tools: historic + TMY data, soiling history, site management |

**Shared per-API definitions:**

- [capabilities/shared/solcast.yaml](capabilities/shared/solcast.yaml) — Full Solcast API consumed definition (22 operations, REST and MCP expose on ports 8100/9100)

### JSON Schemas

| File | Description |
|---|---|
| [json-schema/solcast-radiation-and-weather-schema.json](json-schema/solcast-radiation-and-weather-schema.json) | Schema for irradiance and weather data points (GHI, DNI, DHI, air temp, wind, etc.) |
| [json-schema/solcast-pv-power-schema.json](json-schema/solcast-pv-power-schema.json) | Schema for PV power output data points (pv_estimate, pv_power_rooftop, percentiles) |
| [json-schema/solcast-pv-power-site-schema.json](json-schema/solcast-pv-power-site-schema.json) | Schema for registered PV power site objects (location, specs, tracking) |

### JSON Structures

| File | Description |
|---|---|
| [json-structure/solcast-radiation-and-weather-structure.json](json-structure/solcast-radiation-and-weather-structure.json) | Hierarchical documentation of the radiation and weather response envelope |
| [json-structure/solcast-pv-power-structure.json](json-structure/solcast-pv-power-structure.json) | Structure of PV power response (estimated_actuals vs forecasts, percentile bands) |
| [json-structure/solcast-pv-power-site-structure.json](json-structure/solcast-pv-power-site-structure.json) | Structure of PV power site resources and the site list envelope |

### JSON-LD Context

- [json-ld/solcast-context.jsonld](json-ld/solcast-context.jsonld) — Linked data context mapping Solcast properties to schema.org, QUDT units (W/m², kW, °C, m/s), WGS84 geo coordinates, and Solcast-specific IRIs.

### Examples

| File | Endpoint |
|---|---|
| [examples/solcast-get-live-radiation-and-weather-example.json](examples/solcast-get-live-radiation-and-weather-example.json) | GET /data/live/radiation_and_weather |
| [examples/solcast-get-forecast-radiation-and-weather-example.json](examples/solcast-get-forecast-radiation-and-weather-example.json) | GET /data/forecast/radiation_and_weather |
| [examples/solcast-get-forecast-rooftop-pv-power-example.json](examples/solcast-get-forecast-rooftop-pv-power-example.json) | GET /data/forecast/rooftop_pv_power |
| [examples/solcast-get-historic-radiation-and-weather-example.json](examples/solcast-get-historic-radiation-and-weather-example.json) | GET /data/historic/radiation_and_weather |
| [examples/solcast-list-pv-power-sites-example.json](examples/solcast-list-pv-power-sites-example.json) | GET /resources/pv_power_sites |
| [examples/solcast-create-pv-power-site-example.json](examples/solcast-create-pv-power-site-example.json) | POST /resources/pv_power_site |

### Vocabulary

- [vocabulary/solcast-vocabulary.yml](vocabulary/solcast-vocabulary.yml) — Domain vocabulary covering 30+ terms across irradiance (GHI, DNI, DHI), PV power (pv_estimate, P50/P90), meteorology, solar geometry, soiling models (Kimber, HSU), TMY, and grid aggregation.

## Common Properties

| Type | URL |
|---|---|
| Portal | [https://solcast.com/](https://solcast.com/) |
| Documentation | [https://docs.solcast.com.au/](https://docs.solcast.com.au/) |
| SDKs | [https://solcast.com/sdk](https://solcast.com/sdk) |
| Sign Up | [https://toolkit.solcast.com.au/register](https://toolkit.solcast.com.au/register) |
| Pricing | [https://solcast.com/pricing/irradiance-weather](https://solcast.com/pricing/irradiance-weather) |
| Change Log | [https://solcast.com/changelog](https://solcast.com/changelog) |
| Website | [https://solcast.com](https://solcast.com) |
| GitHub | [https://github.com/Solcast](https://github.com/Solcast) |
| API Toolkit | [https://toolkit.solcast.com.au/](https://toolkit.solcast.com.au/) |
| Terms of Service | [https://solcast.com/terms-of-service](https://solcast.com/terms-of-service) |

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
