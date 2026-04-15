# RackLog Parcel Data

App-ready county parcel datasets for RackLog HuntMaps.

## Structure
```
wi/
  lacrosse_parcels_mobile.json
  bayfield_parcels_mobile.json
  ...
```

## Format
- GeoJSON FeatureCollection
- CRS: EPSG:4326 (WGS84)
- Mobile-optimized geometry (simplified + precision-reduced)
- Consistent schema per feature:
  - `parcel_id` — county parcel identifier
  - `owner_name` — primary owner
  - `acreage` — GIS-calculated acres
  - `source_county` / `source_state` — origin
  - `ingest_date` — processing date

## Source
Wisconsin Statewide Parcels V11 (2025) via UW-Madison SCO.

## Pipeline
Processed by RackLog County Agent V1 — deterministic pipeline with automated QA.
