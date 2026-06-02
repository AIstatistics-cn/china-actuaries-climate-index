# Data Dictionary

## Index Files

- `CACI`: composite index, averaged from available standardized components after reversing the sign of `T10`.
- `component_count`: number of available components used in `CACI`.
- `T90`: standardized warm-temperature extreme component.
- `T10`: standardized cold-temperature extreme component. The sign is reversed when forming `CACI`.
- `P`: standardized heavy-precipitation component.
- `D`: standardized dry-condition component.
- `W`: standardized high-wind-power component.
- `S`: sea-level component. This field is not available in the current station-data prototype.

## Time Columns

- `year`: calendar year.
- `month`: calendar month.
- `season_year`: year assigned to the season.
- `season`: `Winter`, `Spring`, `Summer`, or `Autumn`.

Winter is December-February, with December assigned to the following winter year.

## Area Columns

- `area`: national or broad-region unit.
- `province`: province-level unit.

## Component Tables

Files with `raw` in the name contain component values before standardization. Files with `standardized` in the name contain baseline-standardized values used in the composite index.
