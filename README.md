# Auto-Dealer Marketing & Sales Dashboard

Interactive Power BI dashboard that joins marketing web data with CRM sales
and answers one business question: which channels, cities and models bring
not just traffic and leads, but actual sales.

## Data & Model

- **Marketing data** — sessions, pageviews, goal conversions by city,
  device, browser and traffic source
- **CRM sales** — deals linked to clients, with prices in original currency
- **Reference table (справочник)** — car models, price and margin in RUB,
  average car price
- **CBR exchange rates** — daily rates to normalize currency before join
- Star-schema relationships: reference ↔ marketing ↔ CRM, with
  bidirectional cross-filtering so both sources filter each other

## Dashboard pages

**Conversion analysis**
- Conversions by city, device, browser and source
- Daily conversion dynamics; "(not set)" city values cleaned
- 5-step sales funnel with unified corporate color scale
- Map with funnel tooltips; Sunburst by brand & model, treemap by region & device
- Top-3 cities dealer visits, unique users, avg goal value (DAX measures)

**Sales analysis**
- Decomposition of sales by 5 parameters in corporate palette
- Treemap of sales by brand & model; calendar with daily sales
- Table by region / city / brand with alternating-row styling,
  conversion histogram bars, presence-of-sale flag and traffic-light
  conditional formatting
- Page navigation via arrows

## Key findings

- Best-performing source: **[X]** — [X]% of sales from [X]% of spend/leads
- Weakest link in the funnel: step **[X]**, drop-off **[X]%**
- Leading brand: **[X]**; top city: **[X]**

## Stack

Power BI (Power Query, DAX), Google Sheets as data source, CBR rates API/manual table

## Visual case study

The design version of this project: [From Click to Car Sale on Behance](https://www.behance.net/annshchuga)
