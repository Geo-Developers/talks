<!-- .slide: class="title" -->

## Arcade Expression Language
Raúl Jiménez ([@hhkaos](//twitter.com/hhkaos))

[bit.ly/ArcadeArcGIS](http://bit.ly/ArcadeArcGIS)

---

<!-- .slide: class="section" -->

### ¿Qué es Arcade?

> Es un `lenguaje portable` para definir expresiones para calcular campos al vuelo y así personalizar renderizadores y etiquetas

--

### Portable

> Puede ser consumido desde: el `editor de mapa/escenas de ArcGIS Online, ArcGIS Pro`, etc. pero también desde las `Runtime SDKs y JS API`.

--

### ¿Dónde se almacena?

[Web map](https://hhkaos2.maps.arcgis.com/sharing/rest/content/items/b7fa3ffb8b3c4a7a98c9bc1327d7dd84/data?f=json) / Web Scene [JSON Spec](https://developers.arcgis.com/web-map-specification/objects/labelExpressionInfo/)

```
{
  visualVariables: [
    {
      type: "sizeInfo",
      field: null,
      valueExpression: "1-($feature.availability_365/365)",
      valueExpressionTitle: "Unavailability_365",
      valueUnit: "unknown",
      minSize: 6,
      maxSize: 15,
      minDataValue: 0.4300000000000001,
      maxDataValue: 1
    },
    {
      type: "transparencyInfo",
      valueExpression: "$feature[\"price\"]/$feature[\"max_price\"]; return strength;",
      stops: [
        {
          value: 50,
          transparency: 85
        },
        {
          value: 97,
          transparency: 0
        }
      ],
      legendOptions: {
        title: "Strength of predominance"
      }
    }
  ]
}
```

---

<!-- .slide: class="section" -->

### Awesome ArcGIS


[![](imgs/awesome-arcgis2.png)](https://esri-es.github.io/awesome-arcgis/arcgis/arcade/)

+500 [awesome lists](https://github.com/search?utf8=%E2%9C%93&q=topic%3Aawesome-list&type=Repositories) on Github


---

<!-- .slide: class="funciones" -->

#

--

<!-- .slide: class="section" -->

### Ejemplos

```
Round($feature.POP2012/$feature.POP2010, 2)
Average($feature.AGE_20_24, $feature.AGE_25_34,$feature.AGE_34_44)


var company = 'Unknown';
var companies = ['Google', 'Facebook', 'Evernote', 'LinkedIn', 'Stanford'];
for(var k in companies) {
    Console('log the value of a variable here: ', companies[k])    
    if(Find(companies[k], $feature.name, 0) != -1){
      company = companies[k];
    }   
}
return company;
```

---

<!-- .slide: class="section" -->

### Datos: Silicon Valley ([overpass-turbo.eu](http://overpass-turbo.eu/))

```
[out:json][timeout:200];
(

node["name"~"facebook",i]({{bbox}});
way["name"~"facebook",i]({{bbox}});
relation["name"~"facebook",i]({{bbox}});

...

node["name"~"google",i]({{bbox}});
way["name"~"google",i]({{bbox}});
relation["name"~"google",i]({{bbox}});

// print results
out body;
>;
out skel qt;
```

---

<!-- .slide: class="section" -->

### ArcGIS Online

Demo renderers: [Open Data Airbnb](https://hhkaos2.maps.arcgis.com/home/webmap/viewer.html?webmap=b17278b4a3e448ccb44b94e24e56726f)

---

<!-- .slide: class="section" -->

### ArcGIS API for JS

* Create a renderer using Arcade Expressions - [3.x](https://jsbin.com/gobore/edit?html,output) - [4.x](https://jsbin.com/hugilun/edit?html,output)
* [Label features using Arcade expressions - 3.x](https://jsbin.com/vugagit/edit?html,output)

---

<!-- .slide: class="section" -->

### ArcGIS Pro

<iframe src="//hhkaos.github.io/youtube-embed-portion/?v=X6_x3SbTeZU&s=11m23s&e=13m55s&m=true" width="560" height="315"></iframe>

> Personalizando etiquetas y renderizadores

---

<!-- .slide: class="centered" -->

## ¿Preguntas?

* Raúl Jiménez: raul.jimenez@esri.es

Slides: [bit.ly/BigArcGIS](http://bit.ly/BigArcGIS)

---

<!-- .slide: class="end" -->
#
