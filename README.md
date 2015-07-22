Geodata
=======

* [swissBOUNDARIES3D](#swissboundaries3d)

swissBOUNDARIES3D
-----------------

Source: http://data.geo.admin.ch/

[EPSG:4326](4326)

```batchfile
ogr2ogr -f "GeoJSON" -t_srs EPSG:4326 -select "NAME, ICC, EINWOHNERZ" -where "NAME = 'Schweiz'" 4326/Switzerland.geojson source/swissBOUNDARIES3D_1_2_TLM_LANDESGEBIET.shp
ogr2ogr -f "GeoJSON" -t_srs EPSG:4326 -select "NAME, KANTONSNUM, EINWOHNERZ" 4326/Switzerland_Cantons.geojson source/swissBOUNDARIES3D_1_2_TLM_KANTONSGEBIET.shp
ogr2ogr -f "GeoJSON" -t_srs EPSG:4326 -select "NAME, BFS_NUMMER, EINWOHNERZ" -where "OBJEKTART = 'Gemeindegebiet'" 4326/Switzerland_Communes.geojson source/swissBOUNDARIES3D_1_2_TLM_HOHEITSGEBIET.shp
```

[EPSG:21781](21781)

```batchfile
ogr2ogr -f "GeoJSON" -t_srs EPSG:21781 -select "NAME, ICC, EINWOHNERZ" -where "NAME = 'Schweiz'" 21781/Switzerland.geojson source/swissBOUNDARIES3D_1_2_TLM_LANDESGEBIET.shp
ogr2ogr -f "GeoJSON" -t_srs EPSG:21781 -select "NAME, KANTONSNUM, EINWOHNERZ" 21781/Switzerland_Cantons.geojson source/swissBOUNDARIES3D_1_2_TLM_KANTONSGEBIET.shp
ogr2ogr -f "GeoJSON" -t_srs EPSG:21781 -select "NAME, BFS_NUMMER, EINWOHNERZ" -where "OBJEKTART = 'Gemeindegebiet'" 21781/Switzerland_Communes.geojson source/swissBOUNDARIES3D_1_2_TLM_HOHEITSGEBIET.shp
```
