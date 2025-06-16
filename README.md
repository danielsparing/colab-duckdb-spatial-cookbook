# Colab geospatial cookbook with DuckDB

![Timo Volz via Unsplash](https://images.unsplash.com/photo-1597760078652-6359f83febaf)

- [Introduction](./Introduction.md)

Or if you prefer to [cut to the chase](https://www.youtube.com/watch?v=gZbwbxMKb_c&t=51s):

- [Setting up your environment](./Environment.md) (e.g. GDAL)
- **Data Ingestion**
    - don't ingest data. you have a temporary, small environment anyway. Read [cloud-native geo formats](https://github.com/cloudnativegeo/cloud-optimized-geospatial-formats-guide) on demand.
- **Data Visualization**
   - [Visualize a GeoJSON](notebooks/viz_geojson.ipynb)
   - [Visualize a GeoPandas GeoDataFrame](notebooks/viz_gpd.ipynb)
- **Miscellanious**:
    - Working with Overture Maps: this is easy, see the [Overture Maps Docs](https://docs.overturemaps.org/getting-data/duckdb/)
    - [Map Matching with GraphHopper](notebooks/graphhopper.ipynb)

- Netherlands-specific:
   - [Process the Dutch buildings dataset (BAG)](notebooks/bag.ipynb)
