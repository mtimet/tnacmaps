tnacmaps
========
ogr2ogr -f 'ESRI Shapefile' shp/delegations.shp geojson/delegations.geojson -lco ENCODING=UTF-8

ogrinfo -al -geom=SUMMARY shp/delegations.shp

topojson --id-property adm_id -p -o topojson/delegations.json geojson/delegations.geojson

inspirations:
- swiss cantons and municipalities: http://bl.ocks.org/d/4327678/
- us counties: http://bl.ocks.org/4122298

modifications:
- Renamed Bouhaira to Le Kram in  Tunis governorate
- On Manouba Governorate merge Manouba delegation with Douar Hicher delegation (false positions)
  Then moved Mnouba delegation back to Manouba governorate(instead of Tunis governorate)
- Add Jarzouna delegation to Bizerte governorate. (by hand replicating images found in the web like: http://www.mdci.gov.tn/tn/Gov/Bizerte.html and http://www.zonu.com/imapa/africa/Carte_Gouvernorat_Bizerte_Tunisie.jpg)


