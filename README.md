# Datos de los casos de COVID-19 en Costa Rica
Este repositorio contiene datos de los casos de la pandemia de [COVID-19](https://es.wikipedia.org/wiki/COVID-19) reportados en Costa Rica. Estos datos han sido recopilados a partir de la [información brindada diariamente por el Ministerio de Salud]().

Se mantienen datos a nivel de país y a nivel de cantón.

Para una visualización geoespacial de estos datos, puede usarse este [tablero de control](https://geocatie.maps.arcgis.com/apps/opsdashboard/index.html#/fb483593297147b7a92e16115e8f931b).

## Datos a nivel de país
**Datos acumulados (1 registro por día)**  
```
cr-covid19-pais-acumulados.csv
```

## Datos a nivel de cantón
**Datos actuales (1 registro por cantón)**  
```
cr-covid19-cantones-actuales.geojson
```

**Datos históricos (1 registro por cantón, correspondiente a un día)**
```
cr-covid19-cantones-20200322-1353.geojson
cr-covid19-cantones-20200321-1728.geojson
...
...
```

**Datos acumulados (1 registro por cantón por día [i.e. por cada día hay 82 registros])**  
Se genera al realizar la unión de los datos (sin las geometrías) de todos los archivos históricos diarios.
```
cr-covid19-cantones-acumulados.csv
```
