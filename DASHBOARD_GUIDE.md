# SPOKARS-24 Global Surveillance Dashboard — Companion Guide

## Access

The dashboard is available at:
**[https://midas-network.github.io/spokars24-dashboard/](https://midas-network.github.io/spokars24-dashboard/index.html)**

---

## What Is the Dashboard?

The SPOKARS-24 Global Surveillance Dashboard is an interactive data platform that aggregates reported surveillance data on the SPOK-24 epidemic from multiple open sources worldwide. It provides a visual overview of the global spread of SPOKARS-24, including death counts, detected case counts, and confirmed travel-related importation events.

The dashboard covers the period from **November 16, 2024 through January 11, 2025** and includes data for **232 countries** at the global level and **US state-level** breakdowns.

---

## Dashboard Tabs and Features

### Weekly Deaths

A global choropleth map showing weekly reported SPOK-24 deaths by country (or by US state when toggled to the United States view). The color scale is fixed across all weeks to allow visual comparison of epidemic intensity over time. Selecting a country or state updates the epidemic curve and summary panel to show that location's time series.

The right-hand panel shows a summary for the selected entity (or global totals), including weekly and cumulative death counts, trend direction compared to the previous week, and an age distribution breakdown.

### Cumulative Deaths

The same map and panel views, but displaying cumulative reported deaths from the start of the reporting period through the selected week.

### New Weekly Cases

Weekly detected SPOK-24 cases. At the global level, case data is available for a subset of countries. For the United States, case counts are available at the state level. A cumulative toggle allows switching between weekly and cumulative views for the case curve.

### Importations

A dedicated view showing the 53 laboratory-confirmed travel-related importation events reported in WHO Situation Reports 1–4 and by national health authorities. An interactive map displays Brisbane (Australia) as the epidemic origin with connections to each destination city where a travel-related case was confirmed. A sortable table lists each event with its date, city, destination country, source country, and reporting source.

### Timeline

An interactive chronological timeline of the major events in the SPOKARS-24 epidemic, from the initial nursing home cluster on September 26, 2024 through January 18, 2025. Events are color-coded by category: Australia (green), WHO (blue), United States (red), Global (amber), and Science (purple). This timeline mirrors the content of the `Early_Timeline_guide_teams.pdf` provided in the repository.

### About

A disclaimer panel confirming that the dashboard and all associated data are entirely fictional, created for the SMH CrypticChallenge (C-CHA).

---

## Additional Features

- **World / United States toggle**: Switch between a global country-level view and a US state-level view for deaths and cases.
- **Week navigation**: A slider and week-pill selector allow browsing data week by week. An autoplay button animates through the weeks sequentially.
- **Country/state search**: A search box above the map allows quick lookup and selection of any country or US state.
- **Tooltips**: Hovering over any country or state on the map shows a tooltip with weekly deaths, cumulative deaths, weekly cases, and cumulative cases for that entity at the selected week.
- **CSV download**: A download button on the epidemic curve panel exports the currently displayed time series as a CSV file. The download adapts to context: global totals, a selected country, all US states, or a selected US state. Downloads include both death and case data where available.
- **Info buttons (ⓘ)**: Small info icons next to section headers provide contextual notes about data limitations (see below).

---

## Important Notes on Dashboard Data

> **The dashboard may contain time series that differ from the baseline data files provided to teams in the `Raw_data_Teams/` folder.** Teams should keep in mind that the dashboard is designed to simulate a real-world open-data aggregation platform and is therefore subject to different reporting noise, misreporting, delays, and incompleteness compared to the curated files distributed directly to teams.

Specifically, teams should be aware of the following characteristics of the dashboard data:

- **Death data represents reported (delayed) deaths**, not real-time true counts. There is an inherent lag between actual deaths and their appearance in the reported data.
- **Some countries have significant underreporting** due to limited testing and notification capacity. Rankings and totals reflect reported data only and may substantially underestimate the true burden, particularly in countries with constrained diagnostic infrastructure.
- **Age stratification is incomplete.** A significant share of reported deaths have unknown age classification, and the age distribution shown on the dashboard should be interpreted with caution.
- **Some countries may have missing data for recent weeks** due to reporting delays. Absence of data for a given week does not imply zero cases or deaths.
- **US detected case data reflects diagnostic capacity constraints** described in the scenario timeline, including testing supply shortages, the removal of travel-history requirements in mid-December, and the overlap with seasonal influenza-like illness that complicates case identification.

These characteristics are intentional and reflect the realistic challenges teams would face when working with aggregated open-source surveillance data during an emerging epidemic.

---

## Relationship to Repository Data Files

The data files in `Raw_data_Teams/` (Australia, California, Virginia, France, United Kingdom, and CDC TGS airport surveillance) are provided as curated datasets distributed directly to teams. The dashboard aggregates data from a broader set of simulated open sources and applies its own reporting pipelines. As a result:

- Time series values in the dashboard and in the CSV files may not match exactly for the same location and time period.
- The dashboard covers a wider set of countries and US states than the curated files.
- The curated files may contain data at finer temporal resolution (e.g., daily for Australian cases) or with different age-group stratifications than what is shown on the dashboard.

Teams should treat both the dashboard and the curated files as complementary but independent data sources, each with its own reporting characteristics — just as they would when working with real-world surveillance data from different platforms.
