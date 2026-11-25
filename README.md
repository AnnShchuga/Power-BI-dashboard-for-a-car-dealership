# Auto-Dealer Marketing & Sales Dashboard

Interactive Power BI dashboard that joins marketing web data with CRM sales
for a car dealership (Jan 1 – Feb 17, 2020). One business question:
which channels, cities and models bring not just traffic, but actual sales.

![Dashboard](images/main.png)

## Data & Model

- **Marketing data** — sessions, pageviews and goal conversions by city,
  device, browser and traffic source
- **CRM sales** — deals linked to clients
- **Reference table** — car models with price, margin (RUB) and average price
- **CBR exchange rates** — daily rates to normalize currency before the join
- Star-schema relationships: reference ↔ marketing ↔ CRM, with
  bidirectional cross-filtering so both sources filter each other

## Dashboard pages

**Conversion analysis**
- Conversions by city, device, browser, model and source;
  "(not set)" city values cleaned
- Daily conversion dynamics
- 5-step sales funnel in a unified corporate color scale
- Map with funnel tooltips; Sunburst by brand & model
- Top-3 cities dealer visits, unique users, avg goal value (DAX measures)

**Sales analysis**
- Sales decomposition by 5 parameters in the corporate palette
- Treemap of sales by brand & model; calendar with daily sales
- Table by region / city / brand with alternating-row styling,
  conversion histogram bars and traffic-light conditional formatting
- Page navigation via arrows

## Key findings

- **33,033 conversions** over 7 weeks; leading brand: **Mercedes (52.2%)** vs BMW (47.8%)
- **Google** is the top source — 18.1k conversions (~55% of all),
  followed by Yandex (~10k)
- Top model: **Mercedes e220** — 4.6k conversions, more than the next three combined
- **Mobile drives 59.7%** of conversions (desktop 37.2%, tablet 3.1%)
- **Chrome dominates** the browser mix (52.4%)

## Stack

Power BI (Power Query, DAX), Google Sheets as data source, CBR daily FX rates

## Visual case study

The design version of this project:
[From Click to Car Sale on Behance](https://www.behance.net/annshchuga)
