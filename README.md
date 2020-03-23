# Datos de los casos de COVID-19 en Costa Rica
Se mantienen datos a nivel de país y a nivel de cantón.


## Datos a nivel de país
**Archivo con los datos actuales**  
Se genera al guardar la última línea de la hoja en Google Sheets. Debe usarse para actualizar la capa alojada en ArcGIS Online.
```
cr-covid19-pais-actual.csv
```

**Archivos históricos diarios**  
Se generan al guardar la capa de datos actuales alojada en ArcGIS Online, antes de actualizarla con el archivo que tiene los datos actuales.
```
cr-covid19-pais-20200322-1353.csv
cr-covid19-pais-20200321-1728.csv
...
```

**Archivo histórico acumulado (1 registro por día)**  
Se genera al exportar en formato CSV la hoja en Google Sheets.
```
cr-covid19-pais-historico.csv
```

## Datos a nivel de cantón
**Archivo con los datos actuales**  
Solamente se mantiene en ArcGIS Online, como una capa alojada. Se originó al subir y modificar la capa de cantones del IGN en el SNIT (ver la sección de comandos), agregando los campos relacionados con COVID-19 (confirmados, recuperados, activos, etc.). Debe modificarse manualmente con los datos que facilita diariamente el Ministerio de Salud.

**Archivos históricos diarios**
Se generan al guardar la capa de datos actuales alojada en ArcGIS Online, antes de actualizarla manualmente con los datos del Ministerio de Salud.
```
cr-covid19-cantones-20200322-1353.csv
cr-covid19-cantones-20200321-1728.csv
...
```

**Archivo acumulado (1 registro por cantón por día [i.e. por cada día hay 82 registros])**  
Se genera al realizar la unión de los datos (¿sin las geometrías?) de todos los archivos históricos diarios.
```
cr-covid19-cantones-historico.csv
```
