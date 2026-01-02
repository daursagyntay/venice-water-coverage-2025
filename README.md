# Venice Water Coverage (2025)

While planning a trip to Venice, I wondered:
**How much of Venice is actually water?**

This project is a quick GIS snapshot using Sentinel-2 satellite imagery and QGIS.

## Data
- Sentinel-2 Level-2A (2025), tile T32TQR
- Bands used: B03 (Green), B11 (SWIR)
- Administrative boundary: Comune di Venezia (OpenStreetMap)
- CRS: EPSG:32632 (UTM Zone 32N)

## Method
1. Calculate MNDWI = (Green - SWIR) / (Green + SWIR)
2. Extract water pixels using threshold MNDWI > 0
3. Clip water mask to Venice administrative boundary
4. Calculate water surface area using pixel count

## Result
- Water surface area: **248.27 km²**
- Water coverage: ~45% of Venice administrative area
- Pixel size: 20 m (400 m² per pixel)

## Output
See the map in:
`maps/venice_water_mask_2025.png`

## Notes
This is a single-date snapshot. Tidal and seasonal effects may influence water extent.
