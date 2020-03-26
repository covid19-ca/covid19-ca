# Datos de los casos de COVID-19 en Centro América

## Datos a nivel de país

# Comandos
## Obtención de datos
Las capas geoespaciales de los países de Centro América se descargaron del sitio:  
[GADM](https://gadm.org/)

Descompresión de las capas de nivel 0:
```terminal
$ unzip gadm36_BLZ_shp.zip gadm36_BLZ_0.* 
$ unzip gadm36_CRI_shp.zip gadm36_CRI_0.*
$ unzip gadm36_GTM_shp.zip gadm36_GTM_0.*
$ unzip gadm36_HND_shp.zip gadm36_HND_0.*
$ unzip gadm36_NIC_shp.zip gadm36_NIC_0.*
$ unzip gadm36_PAN_shp.zip gadm36_PAN_0.*
$ unzip gadm36_SLV_shp.zip gadm36_SLV_0.*
```

Unión de los países en una sola capa:
```terminal
ogr2ogr -f "GeoJSON" capa_paises gadm36_BLZ_0.shp
ogr2ogr -f "GeoJSON" -append -update paises gadm36_CRI_0.shp
ogr2ogr -f "GeoJSON" -append -update paises gadm36_GTM_0.shp
ogr2ogr -f "GeoJSON" -append -update paises gadm36_HND_0.shp
ogr2ogr -f "GeoJSON" -append -update paises gadm36_NIC_0.shp
ogr2ogr -f "GeoJSON" -append -update paises gadm36_PAN_0.shp
ogr2ogr -f "GeoJSON" -append -update paises gadm36_SLV_0.shp
```
