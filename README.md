<p align="center">
    <a href="https://www.beercss.com" target="_blank" rel="noopener noreferrer"><img src="https://www.beercss.com/logo.png" alt="Logotipo de Beer CSS"></a>
</p>
<p align="center">
    <a href="https://github.com/beercss/beercss/blob/main/LICENSE"><img src="https://img.shields.io/github/license/beercss/beercss" alt="Licencia"></a>
    <a href="https://github.com/beercss/beercss"><img src="https://img.shields.io/jsdelivr/npm/hy/beercss" alt="Descargas"></a>
    <a href="https://github.com/beercss/beercss"><img src="https://img.badgesize.io/beercss/beercss/main/dist/cdn/beer.min.css?compression=brotli" alt="Tamaño"></a>
    <a href="https://www.npmjs.com/package/beercss"><img src="https://img.shields.io/npm/v/beercss" alt="Versión"></a>
    <a href="https://github.com/beercss/beercss/pulls"><img src="https://img.shields.io/github/issues-pr/beercss/beercss" alt="Solicitud de extracción"></a>
    <a href="https://github.com/beercss/beercss/issues"><img src="https://img.shields.io/github/issues/beercss/beercss" alt="Problemas"></a>
</p>

# Beer CSS

Construye interfaces de Material Design en tiempo récord... 

...sin estrés para los desarrolladores 🍺💛

## Recuerda que :
> [!NOTE]  
> si puedes imaginarlo puedes programarlo
> 
>  - Alejandro Taboada
<br>
<br>
Beer CSS es un proyecto de código abierto con licencia MIT cuyo desarrollo continuo es posible gracias al apoyo de estos increíbles patrocinadores y colaboradores. Si desea unirse a ellos, considere patrocinar el desarrollo de Beer CSS.


## ¿Por qué? ##

- El primer framework CSS basado en Material Design 3.
- 10x más pequeño que otros frameworks CSS basados en Material Design.  
- Traduce Material Design a los estándares semánticos de HTML.
- Listo para usar con cualquier framework JS. 
- Altamente enfocado en la experiencia de desarrollo (DX).

## ¿Aplicando "la forma cervecera" en CSS?

Este proyecto fue guiado por la **“Ley de Pureza de la Cerveza Alemana”** o **“Reinheitsgebot”** creada en 1516. Esta ley establece que la cerveza solo debe elaborarse con los siguientes ingredientes: **agua**, **malta de cebada** y **lúpulo**. Solo 3 ingredientes. ¡Emocionante, ¿no?! Así que pensamos en ello y nuestros 3 ingredientes son: **configuraciones**, **elementos** y **ayudantes**. Esto suena extraño al principio, porque no es BEM, OOCSS, SMACSS, ITCSS, "Utility first" ni ningún otro enfoque. Nuestro enfoque no evita algunas malas prácticas, pero es ligero, sabroso y puro como una cerveza. ¡Solo pruébalo y siéntelo! 😁

```
|  CONFIGURACIONES |       // Las configuraciones afectan a todo el documento  
|------------------|----|
|                  |    |
|  ELEMENTOS       |    | // Los elementos son los componentes, widgets o etiquetas
|                  |    |  
|------------------|    |
|                  |    |
|                  |    |
|  AYUDANTES       |----| // Los ayudantes comunes hacen los elementos más escalables y personalizables  
|                  |
|                  |
|------------------|
```

### HACER:

```
// 1 configuración para 1 documento
<body class="dark|light">...</body>

// 1 elemento para N ayudantes
<elemento class="ayudante ayudante">...</elemento>
<div class="elemento ayudante ayudante">...</div>

// elementos nav antes que todos los demás
<body>
  <nav class="left|right|top|bottom">...</nav>
  ...
</body>

<div id="app">
  <nav class="left|right|top|bottom">...</nav>
  ...  
</div>

// escribir css así  
.elemento.ayudante {...}
.elemento > .elemento {...}  
.elemento > .ayudante {...}
```

### NO HACER:  

```
// N elementos para 1 etiqueta
<div class="elemento elemento ayudante">...</div>

// elemento con dependencias  
<div class="elemento">
  <div class="elemento-header">...</div>
  <div class="elemento-content">...</div>
  <div class="elemento-footer">...</div>
</div>

// elementos nav después de todos los demás
<body>
  ...
  <nav class="left|right|top|bottom">...</nav> 
</body>

<div id="app">
  ...
  <nav class="left|right|top|bottom">...</nav>  
</div>
  
// escribir css así
.elemento.elemento {...}
.elemento .elemento {...}  
.elemento .ayudante {...}
```

## Comenzando  

### CDN  

Desde jsdelivr.net.

```html 
// con html
<link href="https://cdn.jsdelivr.net/npm/beercss@3.4.13/dist/cdn/beer.min.css" rel="stylesheet" />
<script type="module" src="https://cdn.jsdelivr.net/npm/beercss@3.4.13/dist/cdn/beer.min.js"></script>
<script type="module" src="https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.0/dist/cdn/material-dynamic-colors.min.js"></script>
```

```css 
// con css 
@import "https://cdn.jsdelivr.net/npm/beercss@3.4.13/dist/cdn/beer.min.css";
```

```js
// con javascript  
import "https://cdn.jsdelivr.net/npm/beercss@3.4.13/dist/cdn/beer.min.js";
import "https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.0/dist/cdn/material-dynamic-colors.min.js";  
```

### NPM  

Puede obtener la última versión usando NPM. Esta versión contiene archivos fuente así como los archivos CSS y JavaScript compilados.

```js  
// instalando  
npm i beercss
npm i material-dynamic-colors
```  

```js
// importando como window.beercss y window.materialDynamicColors
import "beercss";
import "material-dynamic-colors";  
```  

```js
// importando como beercss y materialDynamicColors   
import beercss from "beercss";
import materialDynamicColors from "material-dynamic-colors";
```

```js
// importando manualmente desde dist  
import "beercss/dist/cdn/beer.min.css";
import beercss from "beercss/dist/cdn/beer.min.js";
import materialDynamicColors from "material-dynamic-colors/dist/cdn/material-dynamic-colors.min.js";
```

```js
// importando manualmente desde src
import "beercss/src/cdn/beer.css";
import beercss from "beercss/src/cdn/beer.ts";
import materialDynamicColors from "material-dynamic-colors/src/cdn/material-dynamic-colors.js";
```

### HTML

Puede usar este html para configurar su proyecto. Ver en [Codepen](https://codepen.io/leo-bnu/pen/yLKLPxj). Más información en [Diseño principal](docs/MAIN_LAYOUT.md).

```html
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="google" content="notranslate"> 
    <title>Hola Mundo</title>
    <link href="https://cdn.jsdelivr.net/npm/beercss@3.4.13/dist/cdn/beer.min.css" rel="stylesheet">
    <script type="module" src="https://cdn.jsdelivr.net/npm/beercss@3.4.13/dist/cdn/beer.min.js"></script>
    <script type="module" src="https://cdn.jsdelivr.net/npm/material-dynamic-colors@1.1.0/dist/cdn/material-dynamic-colors.min.js"></script>
  </head>
  <body class="dark">
    <nav class="left drawer l">  
      <header>
        <nav>
          <img src="https://www.beercss.com/favicon.png" class="circle">
          <h6>Salud</h6> 
        </nav>
      </header>
      <a> 
        <i>home</i>
        <div>Inicio</div>
      </a>
      <a>
        <i>search</i>
        <div>Buscar</div>  
      </a>
      <a>
        <i>share</i>
        <div>Compartir</div>
      </a>
      <a>
        <i>more_vert</i>
        <div>Más</div>
      </a>
      <div class="divider"></div>
      <label>Etiqueta</label>
      <a>
        <i>widgets</i> 
        <div>Widgets</div>  
      </a>
      <a>
        <i>chat</i>
        <div>Chat</div>
      </a>
      <a>
        <i>help</i>
        <div>Ayuda</div> 
      </a>   
    </nav>

    <nav class="left m">
      <header> 
        <img src="https://www.beercss.com/favicon.png" class="circle">
      </header>
      <a>
        <i>home</i>
        <div>Inicio</div> 
      </a>
      <a>
        <i>search</i>
        <div>Buscar</div>
      </a>
      <a>
        <i>share</i>
        <div>Compartir</div>
      </a>
      <a> 
        <i>more_vert</i>
        <div>Más</div>
      </a>
    </nav>

    <nav class="bottom s">  
      <a>
        <i>home</i> 
      </a>
      <a>
        <i>search</i>
      </a>
      <a> 
        <i>share</i>
      </a>
      <a>
        <i>more_vert</i>
      </a> 
    </nav>

    <main class="responsive">
      <img src="https://www.beercss.com/beer-and-woman.jpg" class="responsive round">
      <h3>Bienvenido</h3> 
      <h5>¡La cerveza está lista!</h5>
    </main>
  </body>
</html>
```

**Recomendamos usar material-dynamic-colors solo cuando su aplicación necesite cambiar el tema en tiempo de ejecución.**

## Documentación  

Documentación y ejemplos completos disponibles en:
  
- **[Documentación](docs/INDEX.md)**  
- **[Página de inicio](https://www.beercss.com)**  

## Guía para contribuir  

## Licencia  

[MIT](https://opensource.org/licenses/MIT)

## Salud a todas las personas aquí 🍻 

### Dev By Arturo 
