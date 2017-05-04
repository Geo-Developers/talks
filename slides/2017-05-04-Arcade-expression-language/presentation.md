<!-- .slide: class="title" -->

## Arcade Expression Language
Raúl Jiménez ([@hhkaos](//twitter.com/hhkaos))

[bit.ly/BigArcGIS](http://bit.ly/BigArcGIS)

---

<!-- .slide: class="section" -->

### ¿Qué es Arcade?

> Es un `lenguaje portable` para definir expresiones para calcular campos al vuelo y así personalizar renderizadores y etiquetas

--

### Portable

> Puede ser consumido desde: el `editor de mapa de ArcGIS Online, ArcGIS Pro`, etc. pero también desde las `SDKs y APIs`.

---

<!-- .slide: class="section" -->

### Datos: Silicon Valley ([overpass-turbo.eu](http://overpass-turbo.eu/))

```
[out:json][timeout:200];
(
node["name"~"Evernote",i]({{bbox}});
way["name"~"Evernote",i]({{bbox}});
relation["name"~"Evernote",i]({{bbox}});

node["name"~"facebook",i]({{bbox}});
way["name"~"facebook",i]({{bbox}});
relation["name"~"facebook",i]({{bbox}});

node["name"~"linkedin",i]({{bbox}});
way["name"~"linkedin",i]({{bbox}});
relation["name"~"linkedin",i]({{bbox}});

node["name"~"stanford",i]({{bbox}});
way["name"~"stanford",i]({{bbox}});
relation["name"~"stanford",i]({{bbox}});

node["name"~"Apple, Inc",i]({{bbox}});
way["name"~"Apple, Inc",i]({{bbox}});
relation["name"~"Apple, Inc",i]({{bbox}});

node["name"~"google",i]({{bbox}});
way["name"~"google",i]({{bbox}});
relation["name"~"google",i]({{bbox}});

node["name"~"salesforce",i]({{bbox}});
way["name"~"salesforce",i]({{bbox}});
relation["name"~"salesforce",i]({{bbox}});

node["name"~"twitter",i]({{bbox}});
way["name"~"twitter",i]({{bbox}});
relation["name"~"twitter",i]({{bbox}});

node["name"~"vmware",i]({{bbox}});
way["name"~"vmware",i]({{bbox}});
relation["name"~"vmware",i]({{bbox}});

node["name"~"adobe",i]({{bbox}});
way["name"~"adobe",i]({{bbox}});
relation["name"~"adobe",i]({{bbox}});

node["name"~"ebay",i]({{bbox}});
way["name"~"ebay",i]({{bbox}});
relation["name"~"ebay",i]({{bbox}});

node["name"~"netflix",i]({{bbox}});
way["name"~"netflix",i]({{bbox}});
relation["name"~"netflix",i]({{bbox}});

node["name"~"Yahoo",i]({{bbox}});
way["name"~"Yahoo",i]({{bbox}});
relation["name"~"Yahoo",i]({{bbox}});

node["name"~"cisco",i]({{bbox}});
way["name"~"cisco",i]({{bbox}});
relation["name"~"cisco",i]({{bbox}});

node["name"~"intel",i]({{bbox}});
way["name"~"intel",i]({{bbox}});
relation["name"~"intel",i]({{bbox}});

node["name"~"ricoh",i]({{bbox}});
way["name"~"ricoh",i]({{bbox}});
relation["name"~"ricoh",i]({{bbox}});

node["name"~"microsoft",i]({{bbox}});
way["name"~"microsoft",i]({{bbox}});
relation["name"~"microsoft",i]({{bbox}});

node["name"~"ibm",i]({{bbox}});
way["name"~"ibm",i]({{bbox}});
relation["name"~"ibm",i]({{bbox}});

node["name"~"amazon",i]({{bbox}});
way["name"~"amazon",i]({{bbox}});
relation["name"~"amazon",i]({{bbox}});
);
// print results
out body;
>;
out skel qt;
```

---

<!-- .slide: class="section" -->

### ArcGIS Online

demo

---

<!-- .slide: class="section" -->

### ArcGIS API for JS

demo

---

<!-- .slide: class="section" -->

### Awesome ArcGIS


[![](imgs/awesome-arcgis2.png)](https://esri-es.github.io/awesome-arcgis/arcgis/arcade/)

+500 [awesome lists](https://github.com/search?utf8=%E2%9C%93&q=topic%3Aawesome-list&type=Repositories) on Github


---

<!-- .slide: class="centered" -->

## ¿Preguntas?

* Raúl Jiménez: raul.jimenez@esri.es

Slides: [bit.ly/BigArcGIS](http://bit.ly/BigArcGIS)

---

<!-- .slide: class="end" -->
#
