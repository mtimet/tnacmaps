tnacmaps
========
ogr2ogr -f 'ESRI Shapefile' shp/delegations.shp shp/delegations.geojson -lco ENCODING=UTF-8

ogrinfo -al -geom=SUMMARY shp/delegations.shp

topojson --id-property adm_id -o topojson/delegations.json geojson/delegations.geojson

inspirations:
- swiss cantons and municipalities: http://bl.ocks.org/d/4327678/
- us counties: http://bl.ocks.org/4122298
