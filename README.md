# Datos de los casos de COVID-19 en Costa Rica
Este repositorio contiene datos de los casos de la pandemia de [COVID-19](https://es.wikipedia.org/wiki/COVID-19) reportados en Costa Rica. Han sido recopilados a partir de la [información brindada diariamente por el Ministerio de Salud](https://github.com/covid19-cr/covid19-cr/tree/master/prensa/comunicados-ministerio-salud). Se mantienen datos a nivel de país y a nivel de cantones.

Para una visualización geoespacial de estos datos, puede consultarse este [tablero de control](https://geocatie.maps.arcgis.com/apps/opsdashboard/index.html#/fb483593297147b7a92e16115e8f931b).

## Datos a nivel de país
**Datos acumulados (1 registro por día)**  
[datos/pais/acumulados](https://github.com/covid19-cr/covid19-cr/tree/master/datos/pais/acumulados)
```
cr-covid19-pais-acumulados.csv
```

## Datos a nivel de cantón
**Datos actuales (1 registro por cantón)**  
[datos/cantones/actuales](https://github.com/covid19-cr/covid19-cr/tree/master/datos/cantones/actuales)
```
cr-covid19-cantones-actuales.geojson
```

**Datos históricos (1 registro por cantón, correspondiente a un día)**  
[datos/cantones/historicos](https://github.com/covid19-cr/covid19-cr/tree/master/datos/cantones/historicos)
```
cr-covid19-cantones-20200322-1353.geojson
cr-covid19-cantones-20200321-1728.geojson
...
...
```

**Datos acumulados (1 registro por cantón por día [i.e. por cada día hay 82 registros])**  
Se genera al realizar la unión de los datos (sin las geometrías) de todos los archivos históricos diarios.  
[datos/cantones/acumulados](https://github.com/covid19-cr/covid19-cr/tree/master/datos/cantones/acumulados)
```
cr-covid19-cantones-acumulados.csv
```
