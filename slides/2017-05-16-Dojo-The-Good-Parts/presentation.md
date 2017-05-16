## Dojo: The Good Parts
Raúl Jiménez ([@hhkaos](https://twitter.com/hhkaos))
Carlos Herrera ([@MundoGister](https://twitter.com/MundoGister))

---
### ¿Qué es Dojo Toolkit?

---

### Antecedentes
   * Tecnología  que surgió en 2004 de la mano de Alex Russell
   * Comunidad muy activa en el proyecto
   * A partir de 2005, las contribuciones de la comunidad empezaba a pesar más que las del propio equipo de desarrolladores
   * Las contribuciones por parte de la comunidad vienen de más de 60 desarrolladores
   * Empresas que usan Dojo:
      * Cisco
      * IBM
      * Esri

---

   * [dojo](https://dojotoolkit.org/reference-guide/1.10/dojo/index.html#dojo-index) - Core. Tiene distintas funcionalidades (manipular DOM, llamadas AJAX, etc)
   * [dijit](https://dojotoolkit.org/reference-guide/1.10/dijit/index.html#dijit-index) - Interfaces de usuario
   * [dojox](https://dojotoolkit.org/reference-guide/1.10/dojox/index.html#dojox-index) - Funcionalidad basada en los módulos anteriores
   * [utils](https://dojotoolkit.org/reference-guide/1.10/util/index.html#util-index) - Herramientas de apoyo

---

### Primeros pasos

   * CDN   `<script src=”//ajax.googleapis.com/ajax/libs/dojo/1.10.4/dojo/dojo.js”></script>`
   * `define` `require`
   * [Hola Mundo!](https://github.com/MundoGister/Seminario_Dojo/blob/gh-pages/holamundo_dojo.html)

---

### Animaciones y efectos

   * Animaciones y efectos `dojo/_base/fx`

```
require(["dojo/_base/fx", "dojo/on", "dojo/dom", "dojo/domReady!"],     function(fx, on, dom) {
            var fadeOutButton = dom.byId("fadeOutButton"),
                    fadeInButton = dom.byId("fadeInButton"),
                    fadeTarget = dom.byId("fadeTarget");

            on(fadeOutButton, "click", function(evt){
                fx.fadeOut({ node: fadeTarget }).play();
            });
            on(fadeInButton, "click", function(evt){
                fx.fadeIn({ node: fadeTarget }).play();
            });
        });
```
[Ejemplo en funcionamiento](https://mundogister.github.io/Seminario_Dojo/effects/fade.html)

---

   * Efectos

```
require(["dojo/_base/fx", "dojo/on", "dojo/dom", "dojo/domReady!"], function(baseFx, on, dom) {
                var startButton = dom.byId("startButton"),
                    reverseButton = dom.byId("reverseButton"),
                    borderbox = dom.byId("borderbox");

                    // Establecemos el controlador on
                    on(startButton, "click", function(evt){
                        baseFx.animateProperty({
                            node: borderbox,
                            properties: { borderWidth: 100 }
                        }).play();
                    });
```
[Ejemplo en funcionamiento](https://mundogister.github.io/Seminario_Dojo/effects/animateBorder.html)

---

   * Combinar

```
function swapAnim(node1, node2) {
                    var posn1 = parseInt(domStyle.get(node1, "left")),
                        posn2 = parseInt(domStyle.get(node2, "left"));

                    return moveNodes = fx.combine([
                        fx.slideTo({
                            duration: 1200,
                            node: node2,
                            left: posn1
                        }),
                        fx.slideTo({
                            duration: 1200,
                            node: node1,
                            left: posn2
                        })
                    ]);
                }
```
```
on(swapButton, "click", function(evt){

                    // chain the swap nodes animation
                    // with another to fade out a background color in our container
                    var anim = fx.chain([
                        swapAnim(c1, c2),
                        baseFx.animateProperty({
                            node: container,
                            properties: {
                                backgroundColor: "#fff"
                            }
                        })
                    ]);
                    // before the animation begins, set initial container background
                    aspect.before(anim, "beforeBegin", function(){
                        domStyle.set(container, "backgroundColor", "#eee");
                    });

                    // when the animation ends, toggle the originalOrder
                    on(anim, "End", function(n1, n2){
                        originalOrder = !originalOrder;
                    });

                    anim.play();
                });
```

[Ejemplo en funcionamiento](https://mundogister.github.io/Seminario_Dojo/effects/combine_chain.html)

---

### Dijit

`dojo/parser` es un módulo opcional que se utiliza para convertir los nodos "decorados" en el DOM y convertirlos a dijits.
```
var dojoConfig = { parseOnLoad: true }

```

---

`dijit/layout` proporciona una serie de elementos para organizar nuestra interfaz.
   * `dijit/layout/BorderContainer`
   * `dijit/layout/ContentPane`
   * `dijit/layout/AccordionContainer`
   * `dijit/layout/AccordionPane`
   * `dijit/layout/LayoutContainer`
   * `dijit/layout/StackContainer`
   * `dijit/layout/TabContainer`

---

```
![Layouts](imgs/layoutBlock.png)[https://dojotoolkit.org/reference-guide/1.10/_images/layoutBlock.png]

```
---

### Forms
