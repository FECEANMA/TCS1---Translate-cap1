<img src="./img/Figura 1-5. La vista del navegador de You Type It….png"/>

*Figura 1-5. La vista del navegador de You Type It…*

## Métodos estandarizados

Ambas solicitudes HTTP de Alice utilizaron GET como su método HTTP. Pero hay un poco de HTML 
en la última representación que activará una solicitud HTTP POST si Alice hace clic 
en el botón publicar:

```
<form action="http://youtypeitwepostit.com/messages" method="post">
    <input type="text" name="message" value="" required="true"
        maxlength="6"/>
    <input type="submit" />
 </form>
```

El estándar HTTP (RFC 2616) define ocho métodos que un cliente puede aplicar a un recurso.
En este libro, me centraré en cinco de ellos: GET, HEAD, POST, PUT y DELETE. En el <span style="color: red;">Capítulo 3</span>, cubriré estos métodos en detalle, junto con un método de extensión, PATCH, diseñado específicamente para su uso en APIs web. En este momento, lo importante a tener en cuenta es que hay un pequeño número de métodos estándar.

No es imposible inventar un nuevo método HTTP (sucedió con PATCH), pero es un gran asunto. Esto no es como un lenguaje de programación, donde puedes nombrar tus métodos como quieras. Cuando construí el simple sitio web de microblogging para usar en este ejemplo, no definí nuevos métodos HTTP como GETHOMEPAGE y HELLOPLEASESHOWMETHEMESSAGELISTTHANKSBYE. Usé GET tanto para "mostrar la página de inicio" como para "mostrar la lista de mensajes", porque en ambos casos GET ("dame una representación de este recurso") era la mejor opción entre la interfaz de HTTP y lo que quería hacer. Distingui entre la página de inicio y la lista de mensajes no definiendo nuevos métodos, sino tratando esos dos documentos como recursos separados, cada uno con su propia URL, accesibles a través de GET.
