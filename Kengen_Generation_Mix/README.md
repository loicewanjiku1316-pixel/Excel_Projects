# KenGen Generation Mix Analysis (2020–2025)

An Excel-based analysis of KenGen's electricity generation mix from 2020 to 2025, examining how hydro, geothermal, thermal, and wind output shifted in response to Kenya's 2021–2023 drought and subsequent rainfall recovery.

## Overview

Kenya's power generation relies on a mix of hydro, geothermal, thermal, and wind sources. This project traces how that mix has shifted over a six-year period, with a particular focus on how the system responded to a historic drought — five consecutive failed rainy seasons that hit the Tana River basin starting in 2021.

**Key finding:** When hydro output dropped sharply in 2022 (–23.8%), geothermal and thermal generation stepped in to absorb the shock, preventing a total generation collapse. As rainfall recovered in 2023–2025, hydro rebounded (+36.83%) and geothermal's share eased back down accordingly.

## Data Sources

Generation figures (GWh, by source) were manually extracted from KenGen's publicly available Integrated Annual Reports:

- KenGen Integrated Annual Report & Financial Statement, 2021
- KenGen Integrated Annual Report & Financial Statement, 2022
- KenGen Integrated Annual Report & Financial Statement, 2023
- KenGen Integrated Annual Report & Financial Statement, 2024
- KenGen Financial Results, 2025

Each report discloses the current year's generation mix alongside the prior year's, for comparison. All annual reports are publicly available at [kengen.co.ke](https://www.kengen.co.ke).

## Methodology

1. **Extraction** — Generation-by-source figures (GWh) were pulled manually from each PDF report, since the data isn't published in a downloadable spreadsheet format.
2. **Cleaning** — Raw extracted data was cleaned in Excel (fixing merged text, converting text-formatted numbers, standardizing source names) and structured into a consistent `Source | GWh | Year` format per year.
3. **Combining** — The six yearly tables were stacked into a single dataset using Power Query's Append Queries function.
4. **Analysis** — A PivotTable was built to calculate each source's % share of total generation per year. A second PivotTable (with Year and Source layout reversed) supported a year-over-year trend view.
5. **Visualization** — Two charts were produced:
   - A 100% stacked column chart showing generation mix (% share) by year
   - A line chart showing generation trends (GWh) by source over time

## Repository Contents

| File | Description |
|---|---|
| `KenGen_Generation_Mix_Analysis.xlsx` | Full workbook — raw yearly data, Power Query steps, PivotTables, and both charts |
| `charts/` | Exported chart images (generation mix %, generation trends GWh) |

## Tools Used

- Excel (Power Query, PivotTables, PivotCharts)

## Related

A summary write-up of this analysis, with additional context comparing Kenya's diversified grid to Zambia's hydro-dependent grid during the same drought period, was published on LinkedIn: *[add link]*

## Author

Loice Wanjiku
*[add LinkedIn / contact info]*
