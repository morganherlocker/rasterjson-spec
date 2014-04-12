rasterjson-spec
===============

*experimental json raster specification*

Rasterjson is an open data specification similar to geojson, but focused on raster data. Its goal is to provide a simple way to pass around raster data used in geospatial analysis in much the same way that geojson has for vector analysis. Rasters tend to have a smaller footprint than vectors, and many algrothims already exist for manipulating them efficiently.

```json
{
  "bbox": [0,0,1,1],
  "resolution": 100,
  "interval": 0.01,
  "z": "Elevation"
  "data": [
    [0.00,0.00,5],
    [0.01,0.00,6],
    [0.02,0.00,7],
    [0.03,0.00,5],
    [0.04,0.00,7],
    [0.05,0.00,4],
    [0.06,0.00,3],
    [0.07,0.00,9],
    ...
  ]
}
```

- bbox, resolution, and intervals are set explicitely
- any other attributes can also be added
- data is an array of arrays comprised of [x, y, z]
