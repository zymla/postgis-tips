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


#Osm2po
osm2pgrouting hard to install
Trying osm2po
```
java -Xmx1408m -jar osm2po/osm2po-core-5.2.43-signed.jar prexif=ospo tileSize=x,c ile-de-france-latest.osm  postp.0.class=de.cm.osm2po.plugins.postp.PgRoutingWriter
```
