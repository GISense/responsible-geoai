# Lab 10 data

## Part A -- AI as a cartographer

| file | what it is | source |
|---|---|---|
| `neighborhood_style.json` | The Mapbox style the lab starts from: 20 layers (background, fills, lines, labels) over the UT campus. Repaired for Austin: labels fall back to `name` when `name_en` is missing, and neighbourhood names (`settlement_subdivision`) are shown. The two icon layers from the original example are removed. Fonts and sprite point at Mapbox's public sets so the file uploads to any account. | CartoAgent example style (GISense Lab), adapted |
| `base_map.jpg` | The starting style rendered over the UT campus, 1200 x 800. Map data © Mapbox © OpenStreetMap. | rendered with Mapbox GL JS |
| `inspiration.jpg` | The example picture: a misty mountain forest. Resized to 1600 px. | from the original Lab 10 |
| `cartoagent_examples.jpg` | Results figure from the CartoAgent paper (photographs, paintings, AI-generated maps and web maps turned into map styles). | CartoAgent, IJGIS 2025 |

## Part B -- Can we trust what AI knows about places?

| file | what it is | source |
|---|---|---|
| `tx_counties.geojson` | The 254 Texas counties: `GEOID`, `county` (name without "County"), `population` (July 2024 estimate), `n_neighbors` (Texas neighbors, edge or corner), `borders_other_state` (True if the county also touches another state). Boundaries simplified to 300 m for mapping. | Boundaries: U.S. Census Bureau TIGER (same source as Lab 8). Population: Census Bureau Population Estimates, `co-est2024-alldata.csv`. |
| `tx_county_neighbors.csv` | One row per pair of neighboring Texas counties, listed in both directions (1,448 rows = 724 pairs). `touch` is `edge` when they share a stretch of border and `corner` when they meet only at a point (shared border under 0.5 km). Neighbors in other states are left out. | U.S. Census Bureau county adjacency file, 2024 (`county_adjacency2024.txt`). The `edge`/`corner` split was measured from the county boundaries. |

The two Part B files are public U.S. government data.
