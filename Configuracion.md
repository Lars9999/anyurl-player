# Introducción #


Felicitaciones, felices poseedores de una Raspberry Pi (RPI) decorada a mano con un diseño único (sí, cada una es diferente).

Su RPI es más que decorativa, viene con OpenELEC pre-instalado. OpenELEC es un media center basado en Kodi (alias XBMC), e incluye muchísimas funciones basadas en addons, tanto oficiales como de terceros.

## ADVERTENCIA! ##

Estas instrucciones están incompletas y contienen erratas, porque las estoy escribiendo de memoria. Si tienen problemas no duden en escribirme, para arreglar las instrucciones y en algún momento publicarlas en una wiki.



# Enlaces generales #

  * Sitio oficial de Kodi.
  * Wiki de Kodi.
  * Foro de usuarios Kodi.
  * OpenELEC.
  * Wiki OpenELEC.
  * tvaddons.tv


Comenzando:

La configuración básica del sistema incluye:

> Conectar la RPI al televisor.
> Conectar un teclado USB.
> Conectar la electricidad, y ejecutar OpenELEC por primera vez.
> Configurar el wifi.
> Configurar los servicios, habilitando Samba y SSH (usuario "root", contraseña "openelec").
> Compartir la carpeta "plugins" usando Samba.


Instalando Addons:

La mayor fortaleza de Kodi es su sistema basado en addons, que le permite mostrar contenido de múltiples sitios en internet.

Para instalar un addon de video es suficiente con seleccionar Videos->Addons, y luego ir a la última línea "Get More". El mismo procedimiento aplica para addons de música (por ejemplo radio por internet).

Addons no oficiales:

Por defecto, OpenELEC sólo incluye los addons oficiales de Kodi. Para instalar addons adicionales es necesario instalar tvaddons.tv.

> Ir a "system->settings".
> Ir a "Addons".
> Install from zip file.
> Root filesystem.
> Storage.
> Plugins.
> plugin.program.addoninstaller-1.2.0.zip
> Repetir pasos 1-6.
> plugin.video.hubwizard-1.1.9.zip

Los addons adicionales se encuentran ahora disponibles en el menú Home, seleccionando "Programs" y luego "Addon Installer".

Los mejores addons se encuentran en "Featured addons", y el más recomendado para ver películas es "1channel".

Arreglando 1channel:

El plugin oficial de 1channel es dolorosamente lento (+3 minutos) para abrir las películas. Afortunadamente hay una versión no-oficial mucho más rápida, pero desafortunadamente olvidé incluirla en la carpeta de plugins en la versión que ustedes recibieron.

Para arreglar el problema, les estoy adjuntando dos archivos para eso:

> script.module.urlresolver.zip
> script.video.anyurl.zip

Esos archivos hay que copiarlos a la carpeta /Storage/plugins usando el explorador de archivos de windows o SSH, e instalarlos siguiendo el procedimiento para addons no oficiales.

Arreglando Youtube:

Google tiene la costumbre de deshabilitar funciones para evitar que los clientes no oficiales vean videos musicales y otro videos por el estilo. Afortunadamente la mayoría de cambios son fáciles de seguir.

Después de instalar el plugin oficial (video->addons, get more), hay que repetir los pasos 1-6 de addons no oficiales, y seleccionar "plugin.video.youtube.zip".

Control Remoto:

El control remoto para Android se llama Yatse y está disponible en PlayStore. La wiki de Kodi incluye una lista de Apps para teléfonos/tabletas.

También es posible habilitar una interfaz web, mi interfaz favorita, y la que considero más funcional es Chorus.

Integración con el PC:

Si usan Firefox o Chrome, es posible explorar YouTube, TED Talks y otras en el computador y reproducir los videos en la RPI con un solo click! Es suficiente con Instalar Greasemoney para Firefox, o Tampermonkey para Chrome y luego instalar Play\_on\_XBMC.user.js, siguiendo el enlace.

Ahora al reproducir un video en YouTube, aparecerán unos botones en la parte inferior izquierda:
Botones para controlar Kodi


El botón de play reproduce el video actual inmediatamente.
El botón de más (+) envía el video actual a la lista de reproducción (y crea una lista de reproducción si esta no existe).
El botón >| salta al siguiente video en la lista de reproducción.


Buena suerte, y esperamos disfruten el regalo :-)