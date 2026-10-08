# Utah Home Hazard Map

An interactive screening map of geologic hazards in Utah for people comparing places to live. Click anywhere in the state to rate that spot for faults, liquefaction, landslides and recorded earthquakes.

**Live map:** https://anthonyblackham.github.io/utah-home-hazard-map/

## What it shows

- **Quaternary faults** and surface-fault-rupture special study zones
- **Liquefaction** from detailed hazard studies and the 1990s Wasatch Front regional maps
- **Landslides** from the detailed inventory and the statewide legacy compilation
- **Earthquakes** of M2.5+ since 1990
- A **screening index** (0–12) that adds the four ratings for every 1 km square

## Limits

This is a first screen, not a site assessment. It does not replace a site-specific geotechnical study.

- Blank does not mean safe. Liquefaction and detailed landslide mapping cover only parts of the state.
- The rating thresholds are screening cut-offs chosen for this map, not Utah Geological Survey standards. They are listed in the map under "How the ratings work".
- Ground shaking, flooding, debris flows, rockfall, radon and problem soils are not included.
- Shapes are simplified by roughly 10 to 30 m. `data.json` is a snapshot downloaded on 2026-10-08.

## Data sources

- [Utah Geological Survey](https://geology.utah.gov/apps/hazards/): Quaternary Fault and Fold Database; Utah Geologic Hazards database; Wasatch Front liquefaction potential maps (Contract Reports 94-1 to 94-5, Special Study 96)
- [USGS earthquake catalog](https://earthquake.usgs.gov/earthquakes/search/)
- [Utah Geospatial Resource Center](https://gis.utah.gov/): county and municipal boundaries, lakes, highways

## How it works

A single `index.html` with no libraries. It draws everything on a canvas from `data.json`, a compact delta-encoded copy of the source layers.
