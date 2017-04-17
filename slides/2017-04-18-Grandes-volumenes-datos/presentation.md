<!-- .slide: class="title" -->

## Grandes volúmenes de datos en ArcGIS
Marta Dávila ([@marta_davila](https://twitter.com/marta_davila)) & Raúl Jiménez ([@hhkaos](https://twitter.com/hhkaos))

[bit.ly/BigArcGIS](#)

---

<!-- .slide: class="section" -->

### Motivación

> Aprender cómo crear apps que consuman grandes volúmenes de datos y que sean usables usando ArcGIS.

* Usabilidad:
  * Legibilidad de la información
  * Interactividad
  * etc.
* Rendimiento:
  * Tiempos (transferencia datos, primera carga, ...)
  * Consumo de recursos (CPU, memoria & HD)
  * etc.

---

<!-- .slide: class="problems" -->

<div class="only-title">Legibilidad de la información</div>

--

### Solución: Hexabins + Ctrl escala

<iframe src="https://hhkaos.github.io/youtube-embed-portion/?v=rMwZTlFAeg8&s=20m43s&e=20m55s" width="560" height="315"></iframe>

[The Million Points on a Map Problem - Advanced Techniques](https://youtu.be/rMwZTlFAeg8?t=20m43s)


--

### Solución: Hexabins + Timeslider

<iframe src="https://hhkaos.github.io/youtube-embed-portion/?v=rMwZTlFAeg8&s=33m11s&e=33m21s&imgId=2&m=true" width="560" height="315"></iframe>

[The Million Points on a Map Problem - Advanced Techniques](https://youtu.be/rMwZTlFAeg8?t=33m11s)

--

### Solución: Hexabins + Definition Queries

<iframe src="https://hhkaos.github.io/youtube-embed-portion/?v=rMwZTlFAeg8&s=52m09s&e=52m39s&imgId=3&m=true" width="560" height="315"></iframe>

[The Million Points on a Map Problem - Advanced Techniques](https://youtu.be/rMwZTlFAeg8?t=52m09s)

---

### Factores que influyen en la solución

1. Tecnologías:
  * Cloud vs On-premise
  * Web vs Nativo
2. Naturaleza de la información:
  * Estática vs dinámica
  * Tipo: Puntos vs líneas vs polígonos
  * Big data vs "Small" data
3. Técnicas de visualización:
  * Agregaciones: Geoprocesamientos, SQL,
  * Control de escala, renderización, ...
4. Público objetivo
* Etc.

---

<!-- .slide: class="section" -->

## ArcGIS Online

[www.arcgis.com](http://www.arcgis.com)

`Servicio en la nube gestionado por Esri`



---

<!-- .slide: class="section" -->

## Polígonos

asdasd

--

### Solución: Generalizar polígonos

API para  [generalizar](http://tasks.arcgisonline.com/arcgis/rest/services/Geometry/GeometryServer/generalize) ([documentación](http://resources.arcgis.com/en/help/rest/apiref/index.html?generalize.html))

![Img](https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Douglas-Peucker_animated.gif/440px-Douglas-Peucker_animated.gif)

[Algoritmo de Douglas-Peucker](https://en.wikipedia.org/wiki/Ramer%E2%80%93Douglas%E2%80%93Peucker_algorithm)

---

### Tendencias


[<video src="videos/Animated3DMeshes.mp4" width="400" autoplay loop></video>](https://coolmaps.esri.com/Dashboards/CrimeTrends/)
[<video src="videos/GPU.mp4" width="400" autoplay loop></video>](https://youtu.be/rG-rw1ZJBDc?t=16m41s)

---

<!-- .slide: class="agenda" -->

### Recursos

* [Awesome ArcGIS: ArcGIS Best Practices](https://esri-es.github.io/awesome-arcgis/arcgis/best-practices/performance/)
* [The Million Points on a Map Problem - Advanced Techniques](https://www.youtube.com/watch?v=rMwZTlFAeg8)
* [Drawing millions of features in ArcGIS: Advanced techniques](https://www.esri.com/training/catalog/57630434851d31e02a43ef39/drawing-millions-of-features-in-arcgis:-advanced-techniques/)
* [](https://www.youtube.com/playlist?list=PLaPDDLTCmy4Z844nQ0aFdRCTICoNDPf7E)

---

<!-- .slide: class="questions centered" -->

## Questions?

* Raul Jimenez:
  * [twitter.com/hhkaos](https://twitter.com/hhkaos)
  * [github.com/hhkaos](https://github.com/hhkaos)
  * [youtube.com/hhkaos](https://youtube.com/hhkaos)

Slides: [esri-es.github.io/demos/2017/terraformer](https://esri-es.github.io/demos/2017/terraformer)

---

<!-- .slide: class="end" -->
#
