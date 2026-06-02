# China Actuaries Climate Index Prototype

This repository contains a research prototype of a China-focused actuarial climate index built from station-based meteorological observations. The files provide monthly and seasonal index and component results for China, broad regions, and province-level units.

## Coverage

- Years: 1981-2025
- Baseline period: 1981-2010
- Latest source observation date: 2025-08-24
- Station observation records processed: 8,342,123
- Unique station IDs processed: 1,259

Latest national values:

- 2025-08 monthly CACI: `2.8525103529`
- 2025 Summer seasonal CACI: `2.7785266490`

## Components

- `T90`: warm temperature extremes
- `T10`: cold temperature extremes, sign-reversed in the composite index
- `P`: heavy precipitation
- `D`: consecutive dry conditions
- `W`: high wind power
- `S`: sea-level component, unavailable in this station-data prototype

## Files

- `outputs/monthly_index.csv`: monthly CACI values by broad area.
- `outputs/monthly_index_by_province.csv`: monthly CACI values by province-level unit.
- `outputs/seasonal_index.csv`: seasonal CACI values by broad area.
- `outputs/seasonal_index_by_province.csv`: seasonal CACI values by province-level unit.
- `outputs/*components*`: raw and standardized component values.
- `outputs/station_month_components.csv`: station-level monthly component table.
- `outputs/station_inventory.csv`: station inventory used in the calculation.
- `outputs/unmapped_station_inventory.csv`: stations not assigned to province-level units.
- `outputs/source_zip_inventory.csv`: local source archive inventory.
- `metadata/station_province_map.csv`: station-to-province mapping.
- `docs/methodology.md`: compact methodology notes.
- `docs/data_quality_report.md`: coverage and caution notes.
- `DATA_DICTIONARY.md`: field definitions.

## Notes

This is a research prototype, not an official actuarial climate index. Temperature and wind components are generally more robust in this workflow. Precipitation and dry-condition components should be checked against a China-specific precipitation dataset before formal actuarial pricing, reserving, or regulatory use.

<sub>Contact: Author: WANG GAO. Email: aiscience@foxmail.com. School of Finance, Hebei University of Economics and Business, Shijiazhuang 050062, China.</sub>
