# TraducirWeb

Web - Traducir web con jquery





### Demo

![alt demo](https://github.com/sbpinilla/TraducirWeb/blob/master/demo/webdemo.gif)


### json

#### page-es.json

```json
{
  "saludo":"Hola mundo!!",
  "texto" :"Lorem Ipsum es simplemente el texto de relleno de las imprentas y archivos de texto. Lorem Ipsum ha sido el texto de relleno estándar de las industrias desde el año 1500, cuando un impresor (N. del T. persona que se dedica a la imprenta) desconocido usó una galería de textos y los mezcló de tal manera que logró hacer un libro de textos especimen. No sólo sobrevivió 500 años, sino que tambien ingresó como texto de relleno en documentos electrónicos, quedando esencialmente igual al original. Fue popularizado en los 60s con la creación de las hojas Letraset, las cuales contenian pasajes de Lorem Ipsum, y más recientemente con software de autoedición, como por ejemplo Aldus PageMaker, el cual incluye versiones de Lorem Ipsum."
}
```
#### page-en.json

```json
 {
  "saludo":"Hellow work !!",
  "texto" :"Lorem Ipsum is simply the fill-in text of the printers and text files. Lorem Ipsum has been the standard filler text for industries since the year 1500, when a printer was unaware of the use of a text gallery and media the way we did. textbook specimen. Not only did he survive 500 years, but he also entered as a filler text in electronic documents, remaining the same as the original. It was popularized in the 60s with the creation of Letraset sheets, which contained passages of Lorem Ipsum, and more recently with desktop publishing software, such as Aldus PageMaker, which includes versions of Lorem Ipsum."
}

```

### Code html
```html
  <h1 data-translate="saludo">Hola mundo</h1>
```

### Code JS

```javascript

<script
src="https://code.jquery.com/jquery-3.3.1.min.js"
integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
crossorigin="anonymous"></script>

<script src="js/jqueryTranslator.min.js" type="text/javascript"></script>

.....
...
....

<script type="text/javascript">

  (function(){
    
    $("[data-translate]").jqTranslate('translate/page',{defaultLang:'es'});

  } )();

  $(document).ready(function(){

    $("#btnEs").on("click",function(event){

       $("[data-translate]").jqTranslate('translate/page',{defaultLang:'en',forceLang:'es',asyncLangLoad:false});     
    
    });

    $("#btnEn").on("click",function(event){

      $("[data-translate]").jqTranslate('translate/page',{defaultLang:'es',forceLang:'en',asyncLangLoad:false});   
    
    });

  });

  </script>



```
