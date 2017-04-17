Bibliografía
Structural and Sampling (JavaScript) Profiling in Google Chrome
https://www.youtube.com/watch?v=nxXkquTPng8

Sampling: mide ejemplos (se cogen muestras en intervalos pero no sabes q pasa de vez en cdo)
Structural: mide tiempos, o markers/ (flujo ejecution) -> entrys and exits.
- Incluse tº q pasa dentro de la func y sus hijos
- exclusive es sin el tiempo de los hijos
- call count ctas veces se ha llamado

Dos los tienen pros y cons, por lo q hay que usar los dos.

Sampling is for CPU overhead


Crear ejemplos

- renderers

¿Cambian los datos con frecuencia?
¿No cambian? -> Cacheado
Necesitas que sean interactivos?
Control de escala
Leaflet tb peta
Cuánto pesan tus datos
Coste de descarga de los datos vs coste de pintarlos

-----

https://esri-es.github.io/awesome-arcgis/arcgis/best-practices/performance/
https://www.esri.com/training/catalog/57630434851d31e02a43ef39/drawing-millions-of-features-in-arcgis:-advanced-techniques/

[The Million Points on a Map Problem - Advanced Techniques](https://www.youtube.com/watch?v=rMwZTlFAeg8)

-> 14:04 Pre calcular con ArcMap hexagons (cuenta de puntos)-> https://youtu.be/rMwZTlFAeg8?t=14m4s
-> 28:30 Spatial database native RDBMS SQL
[Drawing Millions of Features in ArcGIS: Advanced Techniques]


Spatial agregation ->
En lugar de raw -> agregated counts (o estadísticas; cuenta o suma de un atributo)
Rectangular bins o hexagons -> o límites administrativos.
Shape->generar los poligos a diferentes niveles.
Agregation al vuelo? o pre-calculado?

Millones de datos no tiene sentido ni con smart symbology

Time enable?

- Ejemplos: tornados, terremotos, vuelos , agua en ríos o tráfico en carreteras... - (B2B O B2C)
- Puntos, líneas, polígonos -

Pre-calculated opciones:
1) Geoprocessing -> ArcMap o ArcGIS Pro
2) Native RDBMS SQL
-> Detalles en la charla de "Drawing..."


Generalizar --> poligonos y líneas

--------------------

ArcGIS Online - Web, native, ..
Static data (updated)
- Precalculado - Bins, rectangular,
- Renderers: heatmap
- ...

OnDemand...

Real time
- GeoEvent
- Dynamic ...
