# Cryptic Scenario Modeling Hub - Resources

The repository contains resources associated with the 
[Pandemic cryptic phase modeling hub](https://github.com/midas-network/cryptic-scenario-modeling-hub).

For more information on the Pandemic cryptic phase modeling hub, please consult the
associated [Pandemic cryptic phase modeling hub GitHub Repository](https://github.com/midas-network/cryptic-scenario-modeling-hub).

## Overview

This repository contains all the data, documents, and contextual materials for the **Scenario Modeling Hub Cryptic Challenge (C-CHA)**. The challenge is built around a **fictional emerging respiratory pathogen** — the **Spooky-like Virus 2024 (SPOK-24)** — causing an epidemic that originates in Brisbane, Australia.

Teams are provided with epidemiological data, news reports, government advisories, WHO situation reports, and scientific publications that progressively reveal the natural history and spread of the disease. The goal is for teams to use these materials to inform their scenario modeling efforts.

> **Important:** All documents, news articles, scientific papers, and advisories in this repository are **fictional** and were created solely for the purposes of this challenge.

---


## Repository Structure

```
├── README.md
├── Early_Timeline_guide_teams.pdf
├── Raw_data_Teams/
│   ├── Australia/
│   │   ├── AUSTRALIA_total_weekly_hospitalizations.csv
│   │   ├── Top_4_locations_AUS_weekly_hospitalizations.csv
│   │   ├── Australia_deaths_by_actual_date_from_November2024.csv
│   │   └── aus-country-cases.csv
│   ├── California/
│   │   ├── California_cases_weekly_by_agegroup.csv
│   │   ├── California_deaths_weekly_by_agegroup.csv
│   │   └── California_hospitalizations_weekly_by_agegroup.csv
│   ├── Virginia/
│   │   └── Virginia_hospitalizations_weekly_by_agegroup.csv
│   ├── France/
│   │   ├── France_cases_weekly_by_agegroup.csv
│   │   ├── France_deaths_weekly_by_agegroup.csv
│   │   └── France_hospitalizations_weekly_by_agegroup.csv
│   ├── United Kingdom/
│   │   ├── United-Kingdom_cases_weekly_by_agegroup.csv
│   │   ├── United-Kingdom_deaths_weekly_by_agegroup.csv
│   │   └── United-Kingdom_hospitalizations_weekly_by_agegroup.csv
│   └── CDC_TGS_detection.csv
├── News_Advisories_SITREP_PDFs/
│   └── [16 PDF files — news articles, government advisories, WHO alerts and SITREPs]
└── technical_Papers_briefs_PDFs/
    └── [5 PDF files — scientific papers and WHO technical briefs]
```

---

## Timeline and Guide

| File | Description |
|------|-------------|
| `Early_Timeline_guide_teams.pdf` | **Start here.** Master timeline of the SPOK-24 epidemic from the first cluster (September 26, 2024) through January 2025. Lists every major event — case clusters, deaths, pathogen identification, international spread, WHO declarations, data releases — and cross-references the specific documents and data files that correspond to each event. |

---

## Data (`Raw_data_Teams/`)

This folder contains the epidemiological datasets available for modeling. Data are organized by geography. Unless otherwise noted, US state-level and international files use a common structure with weekly counts broken down by age group (`0-4`, `5-17`, `18-49`, `50-64`, `65plus`, `unknown`).

### Australia

Australia is the epidemic origin and has the longest data series. Data are provided at the national level and for the four most affected sub-national locations.

| File | Columns | Period | Description |
|------|---------|--------|-------------|
| `AUSTRALIA_total_weekly_hospitalizations.csv` | `week_end_date`, `Hospitalized` | Sep 28, 2024 – Jan 18, 2025 | National weekly hospitalization counts. The earliest series in the repository, capturing the full arc from the initial nursing-home cluster through the peak and plateau. |
| `Top_4_locations_AUS_weekly_hospitalizations.csv` | `basin_label`, `week`, `week_end_date`, `Hospitalized` | Sep 28, 2024 – Jan 18, 2025 | Weekly hospitalizations for the four most affected Australian locations: **Brisbane**, **Townsville**, **Rockhampton**, and **Cairns**. Useful for understanding sub-national spread dynamics within Queensland. |
| `Australia_deaths_by_actual_date_from_November2024.csv` | `week_end_date`, `Deaths` | Nov 2, 2024 – Dec 28, 2024 | National weekly deaths by date of death (not notification date). |
| `aus-country-cases.csv` | `country`, `date`, `case_counts_detected_delayed` | Nov 1, 2024 – Jan 18, 2025 | Daily detected case counts at the national level. Note: this file uses a different format than the other country files, with daily resolution |

### California

| File | Columns | Period | Description |
|------|---------|--------|-------------|
| `California_hospitalizations_weekly_by_agegroup.csv` | `report_date`, `age_group`, `hospitalizations` | Oct 26, 2024 – Jan 18, 2025 | Weekly SPOK-24 hospitalizations by age group. The longest US state series, starting from late October. |
| `California_cases_weekly_by_agegroup.csv` | `report_date`, `age_group`, `cases` | Dec 28, 2024 – Jan 18, 2025 | Weekly confirmed cases by age group. Reporting begins later due to initial testing constraints. |
| `California_deaths_weekly_by_agegroup.csv` | `report_date`, `age_group`, `deaths` | Dec 14, 2024 – Jan 18, 2025 | Weekly deaths by age group. |

### Virginia

| File | Columns | Period | Description |
|------|---------|--------|-------------|
| `Virginia_hospitalizations_weekly_by_agegroup.csv` | `report_date`, `age_group`, `hospitalizations` | Dec 28, 2024 – Jan 18, 2025 | Weekly SPOK-24 hospitalizations by age group. Virginia currently has only hospitalization data available, reflecting the earlier stage of the epidemic in this state. |

### France

| File | Columns | Period | Description |
|------|---------|--------|-------------|
| `France_hospitalizations_weekly_by_agegroup.csv` | `report_date`, `age_group`, `hospitalizations` | Dec 21, 2024 – Jan 18, 2025 | Weekly hospitalizations by age group. France begins regular reporting after the first confirmed cases in Paris in late December. |
| `France_cases_weekly_by_agegroup.csv` | `report_date`, `age_group`, `cases` | Dec 28, 2024 – Jan 18, 2025 | Weekly confirmed cases by age group. |
| `France_deaths_weekly_by_agegroup.csv` | `report_date`, `age_group`, `deaths` | Jan 4, 2025 – Jan 18, 2025 | Weekly deaths by age group. |

### United Kingdom

| File | Columns | Period | Description |
|------|---------|--------|-------------|
| `United-Kingdom_hospitalizations_weekly_by_agegroup.csv` | `report_date`, `age_group`, `hospitalizations` | Oct 19, 2024 – Jan 18, 2025 | Weekly hospitalizations by age group. The UK has an early and long hospitalization series, starting from mid-October. |
| `United-Kingdom_cases_weekly_by_agegroup.csv` | `report_date`, `age_group`, `cases` | Dec 28, 2024 – Jan 18, 2025 | Weekly confirmed cases by age group. |
| `United-Kingdom_deaths_weekly_by_agegroup.csv` | `report_date`, `age_group`, `deaths` | Nov 23, 2024 – Jan 18, 2025 | Weekly deaths by age group. |

### CDC Traveler-based Genomic Surveillance (US Airports)

| File | Columns | Period | Description |
|------|---------|--------|-------------|
| `CDC_TGS_detection.csv` | `target_city_normalized`, `date`, `positive sample` | Sep 23, 2024 – Dec 31, 2024 | Wastewater and swab detections of SPOK-24 at major US airports through the CDC Traveler-based Genomic Surveillance (TGS) program. Covers seven cities: **Baltimore**, **Boston**, **Los Angeles**, **Miami**, **New York**, **San Francisco**, and **Seattle**. The `positive sample` column is binary (0/1). First positive detections appear in late November in Los Angeles, with sporadic positives in other cities through December. This dataset provides early signals of pathogen introduction into the US prior to confirmed clinical cases. |

---

## News, Advisories, and Situation Reports (`News_Advisories_SITREP_PDFs/`)

These documents provide the narrative and situational context of the epidemic as it unfolds. Listed in chronological order.

### News Articles

| File | Date | Summary |
|------|------|---------|
| `The_MAIL_Mystery Illness Emerges in Brisbane_October4.pdf` | Oct 4, 2024 | First media report on the mystery illness cluster at a Brisbane nursing home. |
| `ABC News_October_5.pdf` | Oct 5, 2024 | Coverage of the children's hospital cluster and its potential link to the nursing home outbreak; raises early pandemic fears in Brisbane. |
| `First USA_case_CNN.pdf` | Oct 29, 2024 | CNN report on the first confirmed US case — an Australian traveler isolated in a New York City hospital. |

### Government Advisories

| File | Date | Issuing Authority | Summary |
|------|------|--------------------|---------|
| `Australian_Advisory_October_10.pdf` | Oct 10, 2024 | Australian Dept. of Health and Aged Care | First national public health advisory on the unexplained respiratory illness in Queensland. |
| `Queensland Chief Health_October 14.pdf` | Oct 14, 2024 | Queensland Chief Health Officer | Press statement announcing 25 new suspected cases across Brisbane hospitals (including pediatric cases) and a case in Townsville linked to travel from Brisbane. |
| `Queensland_Advisory_October_14.pdf` | Oct 14, 2024 | Queensland Health | Public advisory on the evolving respiratory illness situation in Queensland. |
| `Australian_Advisory_October_14.pdf` | Oct 14, 2024 | Australian Dept. of Health and Aged Care | Updated national advisory reflecting geographic spread beyond Brisbane. |
| `Australian_Advisory_Nov_12.pdf` | Nov 12, 2024 | Australian Dept. of Health and Aged Care | Updated guidance and mitigation measures following the PHEIC declaration; virus officially named SPOK-24. |

### WHO Alerts and Situation Reports

| File | Date | Summary |
|------|------|---------|
| `WHO_alert_October_7.pdf` | Oct 7, 2024 | First WHO public health alert following notification by Australia's IHR Focal Point. Issued after the first two deaths (patients aged 82 and 84). |
| `WHO_Alert_October17.pdf` | Oct 17, 2024 | Revised WHO alert following genetic identification of the causative virus ("Virus X") by the Doherty lab on October 16. |
| `who_situation_report_1.pdf` | Oct 25, 2024 | SITREP 1 — Epidemiological overview of the Australian outbreak. |
| `who_situation_report_2.pdf` | Oct 29, 2024 | SITREP 2 (Week 43) — Updated case counts; virus now referred to as SPOK-24. |
| `who_situation_report_3.pdf` | Nov 4, 2024 | SITREP 3 (Week 44) — International spread detected; cases with travel history from Australia reported in multiple countries. |
| `who_situation_report_4.pdf` | Nov 12, 2024 | SITREP 4 (Week 45) — Accompanies the declaration of a Public Health Emergency of International Concern (PHEIC). |
| `who_press_release_PHEIC.pdf` | Nov 12, 2024 | Official WHO press release declaring PHEIC for the SPOK-24 outbreak. |

---

## Scientific and Technical Papers (`technical_Papers_briefs_PDFs/`)

These fictional publications characterize the pathogen, clinical features, transmission dynamics, and severity of SPOK-24. They are the primary source for epidemiological and clinical parameters needed for modeling. Listed in chronological order.

| File | Date | Summary |
|------|------|---------|
| `WHO_Brief_Spooky.pdf` | Oct 20, 2024 | WHO technical brief on the identification of the causative agent of the emerging respiratory epidemic, designated SPOK-24. |
| `The Lancet_October_25.pdf` | Oct 25, 2024 | Prospective observational study of the first 70 patients hospitalized with SPOK-24 in Brisbane. Key source for **clinical characterization**: symptom profiles, disease progression, and patient outcomes. |
| `NEJM_October_29.pdf` | Oct 29, 2024 | Analysis of the early transmission dynamics of SPOK-24 in Brisbane. Key source for **epidemiological parameters** such as serial interval, incubation period, and reproduction number. |
| `SPOK-24_NEJM_correspondence November_29.pdf` | Oct 29, 2024 | NEJM correspondence summarizing early findings and the outbreak timeline to date. |
| `SPOK-24_Severity_Analysis.pdf` | Jan 7, 2025 | Preprint estimating infection severity from early household and hospital data in Australia. Key source for **severity parameters**: infection fatality ratios, hospitalization rates, and age-stratified risk estimates. |

---

## Key Epidemic Milestones

| Date | Event |
|------|-------|
| Sep 26, 2024 | First cluster at a Brisbane nursing home |
| Oct 5, 2024 | Pediatric cluster identified; media coverage begins |
| Oct 7, 2024 | First deaths reported; WHO issues first alert |
| Oct 16, 2024 | Virus genetically identified by the Doherty lab |
| Oct 20, 2024 | Pathogen officially characterized (SPOK-24) |
| Oct 25, 2024 | First scientific paper (*Lancet*) and WHO SITREP 1 |
| Oct 29, 2024 | First US case (NYC traveler); transmission dynamics paper (*NEJM*) |
| Nov 12, 2024 | WHO declares PHEIC; virus officially named **SPOK-24** / disease named **SPOKARS-24** |
| Nov 23–30, 2024 | Autochthonous transmission confirmed in Vietnam, South Korea, Japan |
| Late Nov 2024 | First US wastewater detections (Los Angeles) |
| Dec 7, 2024 | First US hospitalizations (San Francisco, Seattle) |
| Dec 25, 2024 | Cases detected in France and the United Kingdom |
| Jan 7, 2025 | Severity analysis preprint published |
| Jan 15–18, 2025 | Weekly state-level and country-level surveillance data become available |

---

## How to Use This Repository

1. **Start with `Early_Timeline_guide_teams.pdf`** to understand the chronological sequence of events and which documents correspond to each phase of the epidemic.
2. **Read the news and advisories** in chronological order to build situational awareness of how the epidemic unfolded and how authorities responded.
3. **Read the scientific papers** to extract the key epidemiological and clinical parameters needed for modeling (transmission rate, serial interval, severity, hospitalization rates, age-stratified risk, etc.).


## License

All source code specific to the overall project is available under an 
open-source MIT license. Some items might be available under different terms 
and licenses. Please consult these licenses before using it to ensure that you 
follow the terms under which they were released.

## Contributing

Please feel free to open an issue if you identify any issue or would like to 
suggest an idea/improvement.

## Funding

Scenario modeling groups are supported through grants to the contributing 
investigators.

The Scenario Modeling Hub site is supported by the MIDAS Coordination Center, 
NIGMS Grant U24GM132013 (2019-2024) and R24GM153920 (2024-2029) to the 
University of Pittsburgh.
