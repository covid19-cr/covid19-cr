# COVID-19 en Costa Rica
Este repositorio contiene datos de los casos de la pandemia de [COVID-19](https://es.wikipedia.org/wiki/COVID-19) reportados en Costa Rica y un conjunto de comandos y programas para su procesamiento.

Para visualizar la distribución geográfica de COVID-19 en Costa Rica, con base en estos datos, puede utilizar los siguientes tableros de control:

- [Distribución geográfica de casos de COVID-19 en Costa Rica - Versión para escritorio](https://arcg.is/1HKq9i)
- [Distribución geográfica de casos de COVID-19 en Costa Rica - Versión para móviles](https://arcg.is/1uTiWT)

Para clonar este repositorio, ejecute el comando:
```terminal
$ git clone https://github.com/covid19-cr/covid19-cr.git
```

## Datos
Los datos han sido recopilados a partir de la [información brindada diariamente por el Ministerio de Salud de Costa Rica](https://github.com/covid19-cr/covid19-cr/tree/master/prensa/comunicados-ministerio-salud). Se mantienen datos a nivel de país y a nivel de cantones.

### Datos a nivel de país
**Datos acumulados (1 registro por día)**  
[datos/pais/acumulados](https://github.com/covid19-cr/covid19-cr/tree/master/datos/pais/acumulados)
```
cr-covid19-pais-acumulados.csv
```

### Datos a nivel de cantones
**Datos actuales (1 registro por cantón)**  
[datos/cantones/actuales](https://github.com/covid19-cr/covid19-cr/tree/master/datos/cantones/actuales)
```
cr-covid19-cantones-actuales.geojson
```

**Datos históricos (1 registro por cantón, por día)**  
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

## Comandos y programas

### Creación de un ambiente en Conda
```
$ conda create -n covid19 python=3
$ conda activate covid19
$ conda install -c conda-forge qgis
```

### Descarga de la capa de cantones
```
$ ogr2ogr \
    -f "GeoJSON" \
    -t_srs EPSG:4326 \
    -simplify 0.9 \
    capa_cantones.geojson \
    WFS:"http://geos.snitcr.go.cr/be/IGN_5/wfs?" limitecantonal_5k
```    

### Descarga de la imagen de SARS-CoV-2
```terminal
$ wget https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/SARS-CoV-2_without_background.png/512px-SARS-CoV-2_without_background.png
$ cp 512px-SARS-CoV-2_without_background.png 512px-SARS-CoV-2-logo-github.png
```

Metadatos y condiciones de uso de la imagen:  
[https://commons.wikimedia.org/wiki/File:SARS-CoV-2_without_background.png](https://commons.wikimedia.org/wiki/File:SARS-CoV-2_without_background.png)
