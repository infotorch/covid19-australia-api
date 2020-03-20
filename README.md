![infotorch logo](https://i.imgur.com/xtS74my.png | width=100)

# Infotorch COVID-19 Australia Data API

This is an API of COVID-19 data for Australia proivded by Infotorch as part of our [COVID-19 portal](https://infotorch.org)

The data is sourced from the various website of state government health and other departments and parsed into a format. We crawl the websites every 10-15 minutes so updates should be frequent and regular.

We will also be providing a backfill of international data using the [ECDC dataset](https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide)

## Details

The base endpoint is at

https://api.infotorch.org/api/covid19/

The API is web browsable and you can perform test actions if you visit any webpoint in a browser.

Endpoints support content negotiation.

No authentication is required.

## Endpoints

Totals:

https://api.infotorch.org/api/covid19/totals/

Returns a JSON object

Time Series:

https://api.infotorch.org/api/covid19/statlist/?geos=&stat=confirmed

Both `geos` and `stat` query parameters are required

Where geos is one or more list of supported geographies comma separated `,`

Supported geos are:

- `NSW` `VIC` `QLD` `WA` `SA` `TAS` `ACT` `NT` - States
- `AU` - All of Australia
- Country codes - coming soon

Supported stat parameters

- `confirmed` - confirmed cases
- `deaths` - confirmed deaths
- `tested` - tested cases
- `recovered` - recovered cases
