# Gráficos con SVG, CSS y JavaScript

### Clase 06 → 11/04/2022

**JavaScript es un lenguaje de programación con el que las páginas web se hacen interactivas mediante el control de cada navegador web y su Modelo de Objetos de Documento ([DOM; Document Object Model](https://es.wikipedia.org/wiki/Document_Object_Model))**: Con JavaScript se controla, a través de pequeños programas (o *scripts*), la "comprensión de lectura" del navegador web. Por este motivo pueden haber diferencias entre **ver código fuente** e [**inspeccionar elementos**](https://support.hostinger.es/es/articles/2333029-como-inspeccionar-los-elementos-del-sitio-web).

Dominar JavaScript, o cualquier lenguaje de programación, toma más tiempo de estudio y práctica del que puede tomarnos dominar un lenguaje de descripción. Esto no solo aplica a diseñadores, también aplica a programadores; por esta razón, es común verles programar con ayudar de *frameworks* y *libraries*:

- una *library* ofrece ingredientes seleccionados y preparados para que "cocines" un plato específico con el menor esfuerzo posible. 

- un *framework* es una cocina dispuesta para que prepares un tipo de comida específica, con eficacia y eficiencia (una cocina de restaurant que ofrece sushi es distinta de una de restaurant de pasas o parrilladas).

Pero si no sabes hervir agua ni diferenciar sal de azúcar, difícilmente podrás sacar provecho de cualquier ayuda para cocinar.

Por eso vamos a partir con un pequeño programa (o *script*), el que debes copiar y pegar en la consola de JavaScript de tu navegador:

```
var retinal = ["size","value","texture","color","orientation","shape"]
retinal.sort();
retinal.forEach(element => console.log(element));
```

En las tres línea del pequeño programa (o *script*) tenemos: 

1. Una declaración de variable de nombre `retina`, que contiene un arreglo con 6 cadenas de caracteres.

2. Una reorganización alfabética del arreglo contenido por la variable de nombre `retina`, mediante el [método `sort()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)

3. La repetición de un *log* en la consola para cada cadena en el arreglo ya ordenado alfabéticamente, mediante el [método `forEach()`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

Con lo dicho, ya podríamos preguntarnos: ¿Podría vincular datos a elementos dentro de un SVG? ¡Si, se puede!

Hagamos algo como eso, sin alejarnos muchos del pequeño programa (o *script*) escrito más arriba. Copiemos y peguemos lo siguiente en un editor de código fuente. Una vez pegado allí, guardemos el documento como `ejemplo.html`

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Un poquito de JavaScript</title>
    </head>
    <body>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 200"><g id="aqui"></g></svg>
        <script>
            var retinal = ["size", "value", "texture", "color", "orientation", "shape"];
            retinal.sort();
            retinal.forEach(function (element, i) {
                document.querySelector("#aqui").innerHTML += '<text x="50" y="' + 20 * (i + 1) + '">' + element + "</text>";
            });
        </script>
    </body>
</html>
```

Si revisan el `ejemplo.html` en su navegador, verán cada string dentro de un `<text></text>`. Todos ellos están, a su vez, dentro del grupo de identidad aqui `<g id="aqui"></g>`. Esto es algo que puedes ver dentro de la ventana del navegador, y también lo puedes ver al [**inspeccionar elementos**](https://support.hostinger.es/es/articles/2333029-como-inspeccionar-los-elementos-del-sitio-web), pero no lo encontrarás al "Ver el código fuente". Porque JavaScript no modifica lo escrito por el programador, sino la "comprensión de lectura" del navegador web.


- - - - - - - 
 
#### TAREA

Revisar en YouTube el primer video de HTML y CSS curso práctico 💪 Desde cero [Tutorial Español]

https://youtu.be/rr2H086z16s

- - - - - - - -

###### [← CLASE PASADA](https://github.com/profesorfaco/dno075-2022-1/tree/main/clase-05) — [CLASE SIGUIENTE →](https://github.com/profesorfaco/dno075-2022-1/tree/main/clase-07) 

