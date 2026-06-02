# Methodology Notes

The prototype follows the broad logic of the North American Actuaries Climate Index: climate-extreme components are computed, standardized against a baseline period, and averaged into a composite index.

## Data Scope

The calculation uses local China ISD-Lite station-year archives from 1981 through 2025 and an ISD station-history table. The default baseline period is 1981-2010 because the local station inventory is much more stable in this period than in earlier decades.

## Component Outline

`T90` measures warm-temperature extremes using station-level high-tail thresholds.

`T10` measures cold-temperature extremes using station-level low-tail thresholds. This component is sign-reversed in the composite index, so fewer cold extremes raise the composite value.

`P` measures heavy precipitation using short-window precipitation totals.

`D` measures persistent dry conditions from precipitation occurrence.

`W` measures high wind power using wind speed transformed as `0.5 * rho * wind_speed^3`.

`S` is not computed because the available station files do not provide ocean sea-level height.

## Spatial Aggregation

Stations are assigned to grid cells and then aggregated with cosine-latitude weights. The release includes national, broad-region, and province-level outputs.

Province-level outputs use a station identification process based on station-table matching, country-code fallbacks for Hong Kong, Macau, and Taiwan, province-boundary matching, and a conservative nearest-station fallback.

## Standardization

For each area, component, and calendar period:

```text
standardized = (raw_value - baseline_mean) / baseline_sd
```

The composite index is the average of available standardized components, with `T10` sign-reversed. The default index requires at least three available components.

## Seasons

- Winter: December-February
- Spring: March-May
- Summer: June-August
- Autumn: September-November
