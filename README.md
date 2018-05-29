# postgis-tips

# OSX

## PostgreSQL
[https://postgresapp.com]
```
CREATE EXTENSION POSTGIS;
```

## Osm2pgsql
[https://wiki.openstreetmap.org/wiki/Osm2pgsql]

```
osm2pgsql -c -d osm -U postgres -H localhost -P 5438 -S default.style ../Downloads/ile-de-france-latest.osm.pbf
```

# PostGIS
## Queries
### Get tables
```
SELECT * FROM pg_catalog.pg_tables WHERE schemaname = 'public';
```
```
SELECT aeroway, count(*) FROM planet_osm_point GROUP BY aeroway;
```
```
SELECT * FROM planet_osm_point WHERE aeroway = 'airplane';
```


