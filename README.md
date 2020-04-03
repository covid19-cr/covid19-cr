# Datos de los casos de COVID-19 en Costa Rica
Se mantienen datos a nivel de país y a nivel de cantón.

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
