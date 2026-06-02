# Data Quality Notes

Generated from the default full run:

- Source years: 1981-2025
- Baseline period: 1981-2010
- Latest local observation date: 2025-08-24
- Station observation records read: 8,342,123
- Unique stations read: 1,259
- Monthly index rows: 22,471
- Seasonal index rows: 7,435

## Latest National Values

- 2025-08 monthly CACI: `2.8525103529`, with 4 components.
- 2025 Summer seasonal CACI: `2.7785266490`, with 4 components.

## Province Identification Coverage

The run read 1,259 station IDs. Province identification assigned 1,040 stations to province-level units, including mainland provinces plus Hong Kong, Macau, and Taiwan. The remaining 219 stations were not forced into a province because many are unknown-location, zero-coordinate, ship, island, reef, or otherwise ambiguous records.

Assignment sources:

- Local station-table exact station match: 696 stations
- Province boundary match: 260 stations
- Country-code fallback: 63 stations
- Hong Kong coordinate fallback: 13 stations
- Nearest station-table coordinate fallback: 8 stations
- Unmapped: 219 stations

## Cautions

Temperature and wind components are the strongest parts of this prototype. Precipitation and dry-condition components should be interpreted carefully and ideally checked against a China-specific precipitation dataset. Broad-region definitions are approximate and should be replaced by official climate-region or exposure-region boundaries for production use.
