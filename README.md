# Road Network Density Ranking by Region

**Country:** Ghana
**CRS:** EPSG:25000 - Leigon / Ghana Metre Grid
**Project file:** `Road_Network_Density_Ranking.qgz`

---

## Overview

This project ranks all 16 administrative regions of Ghana by road network density, measured as total road kilometres per square kilometre of regional area. The analysis normalises road length by area to produce a comparable density metric across regions of widely differing size, enabling planners and investors to identify where road infrastructure is most and least concentrated.

---

## Objectives

- Calculate total road length per administrative region.
- Normalise road length by regional area to produce a density metric (km/sq km).
- Rank all 16 regions from highest to lowest road density.
- Store ranked output as a spatial layer for map display.

## Methodology

1. Road network intersected against administrative region polygons: `roads_intersected.gpkg`.
2. Total road length per region computed in kilometres.
3. Road density calculated as: `road_km / area_sqkm`.
4. Regions ranked 1-16 descending by density.
5. Final ranked output stored in `road_density_by_region.gpkg`.

## Road Density Ranking Results

| Rank | Region | Road Length (km) | Area (sq km) | Density (km/sq km) |
|------|--------|-----------------|--------------|---------------------|
| 1 | Greater Accra | 21,237 | 3,699 | 5.74 |
| 2 | Central | 11,169 | 9,664 | 1.16 |
| 3 | Ashanti | 22,840 | 24,379 | 0.94 |
| 4 | Upper East | 7,285 | 8,622 | 0.84 |
| 5 | Volta | 8,096 | 9,825 | 0.82 |
| 6 | Eastern | 14,205 | 18,966 | 0.75 |
| 7 | Ahafo | 3,819 | 5,195 | 0.74 |
| 8 | Bono | 8,224 | 11,647 | 0.71 |
| 9 | Western | 9,558 | 14,258 | 0.67 |
| 10 | Northern | 14,736 | 24,849 | 0.59 |
| 11 | Oti | 5,076 | 11,066 | 0.46 |
| 12 | Western North | 4,581 | 10,075 | 0.45 |
| 13 | Upper West | 7,792 | 19,033 | 0.41 |
| 14 | Northern East | 3,209 | 9,075 | 0.35 |
| 15 | Bono East | 7,579 | 23,256 | 0.33 |
| 16 | Savannah | 9,849 | 35,863 | 0.27 |

## Output Layers

| File | Description |
|------|-------------|
| `roads_intersected.gpkg` | Road segments intersected against administrative region polygons |
| `road_density_by_region.gpkg` | Administrative regions with road length, area, density, and rank attributes |

## Key Findings

- Greater Accra has a road density of 5.74 km/sq km, nearly five times higher than the second-ranked region (Central at 1.16), reflecting its urban road grid.
- Savannah, Bono East, and Northern East have the lowest densities (under 0.35 km/sq km), consistent with their low financial service density and high isolated settlement proportions.
- The national road density distribution is highly skewed; most regions cluster in the 0.3-0.9 range while Greater Accra is a strong outlier.

## Deliverables

| File | Type |
|------|------|
| `Road_Network_Density_Ranking.qgz` | QGIS project |

## Notes

- No `reference_layout.png` or PDF export is present in this folder.
- All layers use EPSG:25000 (Leigon / Ghana Metre Grid).
- Road density reflects the total network length regardless of road class; a class-weighted density would better reflect functional connectivity.
