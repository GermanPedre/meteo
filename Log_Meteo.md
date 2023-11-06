# Dashboard
Seguimiento de tareas realizadas en la creación del dashboard para el PTS "Administración y visualización de datos meteorológicos" 

Reuniones 2do Cuatrimestre 2022:
  - Tuvimos una charla introductoria al proyecto para estar en tema sobre qué tareas podían resultar beneficiosas para el uso general del público.
  - Se eligió que una de las tareas es realizar un dashboard para la representación de datos meteorológicos.
  - Evaluamos cuáles son las alternativas para llevar el dashboard a los usuarios (pagina web, aplicación, etc).
  - Se buscaron servicios que puedan servir para realizar gráficos y mostrarlos al usuario.

17/3/23
  - Planteamos y evaluamos usar Power BI, Grafana, Remote y Node-Red.
  - Se recibieron datos mostrados por consola de valores modificados a mano mediante HTTP Request.

22/3/23
  - Comparamos diseños de dashboards para encontrar uno que se adecúe a la información que podemos mostrar de las estaciones que se instalaron.

23/3/23
  - * hay que aclarar el tema del dominio y qué servicio se utiliza finalmente *

  - Evaluamos crear una página en HTML para representar un dashboard sencillo que muestre datos actualizados acompañados de un mapa interactivo, con ajustes de diseño     utilizando CSS. Luego se estudió la posibilidad de llevar la idea a PHP.
   
  - Se creó la primera versión de la página en HTML (y CSS).

  - Se eligió como una buena alternativa modificar los dashboards que ofrece Weewx, en particular las skins de Mobile y Smartphone, para mostrar información de más de     una estación, con actualizaciones cada vez que el usuario recargue la página.

  - Dashboard de Matthew (el que tiene la posta) https://github.com/weewx/weewx/wiki/dashboards la idea es tomar el skin "Mobile" y tunearlo para que tome más de una       estación.

  - Para varias instancias de weewx matthew preparó esto
    https://raw.githubusercontent.com/weewx/weewx/master/util/init.d/weewx-multi

  - Estaciones: https://www.wunderground.com/dashboard/pws/ISANCARL19 idepar138, idepar123, iloslago6, isanca60

  - Para leer el wunderground en real 
    curl "https://api.weather.com/v2/pws/observations/current?stationId=IDEPAR138&format=json&units=m&apiKey=70137fca2938429c937fca2938329c39"

  - https://weewx.com/docs/setup.html  acordate de ubicar setup.cfg (después no precisás sudo) mover la base de datos weewx/sdb a directorio weewx/archive (crear           archivo)

26/3/23
  - Data para correr más de una instancia de weewx https://github.com/weewx/weewx/wiki/weewx-multi
  - Generación del dahboard comenzada. Se eligió modificar una skin de los reportes de weewx.
  
28/3/23
  - Primer diseño del logotipo a partir del nombre Meteo.
  - Prueba insertando una ventana de Google Maps en el index.

29/3/23
  - Prueba de dasbhoard mostrando 4 tablas distintas (e individuales) de datos en simultaneo.
  - Pruebas varias de distintos logotipos. Finalmente el diseño actual se armó mediante Photoshop (MeteO con un sol en la O).

02/4/23
  - Más pruebas de cambios de diseño.

07/04/23
  - Se muestra dashboard en una sola tabla que contiene la información de cada estación en una columna aparte, de manera que se puedan comparar datos rápidamente.
  - Se insertó un footer de prueba.

10/04/23
  - Se añadió una página extra "Nosotros" donde se explica con más profundidad el propósito del proyecto, enfocado sobre todo en el desarrollo de la página web y el dashboard.
  - Se crearon los hipervínculos para ir desde "Home" a "Nosotros" y viceversa.
  - Clickear Home desde el Home o Nosotros desde Nosotros ahora refresca la página.

12/04/23
  - Se modificó el texto en el apartado de "Nosotros".
  - Se hicieron modificaciones a los códigos de index.html y nosotros.html para optimización y mejora de SEO (buena utilizacion de headers, uso permanente de footers, aclaración de párrafo < p >< /p > para el texto en Nosotros) por si en el futuro se intenta alcanzar un buen posicionamiento en los buscadores.

13/04/23
  - El index ahora se adapta bien a cambios de zoom en computadoras.
  - Pensamos y probamos alternativas de diseño para poder agregar nuevas estaciones en el futuro sin modificar la forma de representar los datos en pantalla.
  - Se agregó un slider horizontal a la tabla para agregar tantas estaciones como se necesiten en un futuro (probablemente para muchas estaciones -más de 6 o 7- se necesite agregar alguna herramienta para filtrar las columnas).

14/04/23
  - La página ahora se adapta a teléfonos móviles sin necesidad de crear otro index, ya que se adapta mediante la hoja de estilos.
  - "weewx.css" ahora es "styles.css".

19/04/23
  - Actualización del texto en párrafo en 'Nosotros'.
  - Pequeños cambios en la hoja de estilos.

25/08/23
  - Texto en 'Nosotros' actualizado para que quede bien de tamaño y no se superponga con el pie de página.

01/09/23
  - Nos planteamos usar Json en vez de Weewx para la transmisión de los datos.
  
14/09/23
  - Se acomodó el footer para que se mantenga debajo de todo y se configuró la hoja de estilos para que no tenga bordes indeseados.
  - Se "rompió" la tabla de la página principal intentando que sea fácil agregar estaciones a futuro. Intentamos que las estaciones aparezcan todas horizontalmente para favorecer la experiencia en teléfonos haciendo que se puedan recorrer todas las columnas (estaciones) con un slider horizontal, pero algo falló y quedó desconfigurado. Problema a solucionar.

22/09/23
  - Se actualizó a Meteo v2.2
  - Agregada la página de Proyecto para hacer una explicación extensa del proyecto completo.
  - Footer corregido en Proyecto.
  - Texto en Proyecto Actualizado (inconpleto).
  - Surgió problema en el iframe de la tabla.
  - Se puso un fondo en el header para que al bajar la opacidad no se vea el texto de la página detrás, ya que el blur no solucionó el problema.
  - Se agregó un apartado de "Galería" para publicar imágenes.
  - Se tomó nota de algunos grupos para agregar al apartado de 'Proyecto'.

16/10/23
  - Se agregó el apartado de historiales para publicar actualizaciones de la evolución de los datos.
  - Fueron agregados los títulos explicativos de cada imagen.
  - Se usó el footer del apartado de proyecto para fijarlo en el fondo de la página.
  - Queda sin terminar los textos del apartado de proyecto según indiquen los otros grupos.
  - Se utilizaron 3 imágenes a modificar ya que necesitaba alguna imagen para configurarla correctamente.
  - Agregamos la explicación de cómo actualizar los datos meteorológicos e imágenes de historiales en el archivo README.

17/10/23
  - Se alineó el texto de la columna que indica qué es cada dato con las columnas de los datos.
  - Se necesita poner los datos "time" y "dew point" en renglones aparte para facilitar la correcta visualización de los datos.

18/10/23
  - Acomodamos los archivos de las estaciones (time y dew point) para que pase los datos bien ordenados uno por uno por separado.
  - Se ajustó la altura del 'slider_container' para que el slider no pise el texto de cada columna.
  - Se cambió el color de la letra de los títulos de los historiales al mismo naranja del logo de Meteo.
  - Los cambios en la tabla se hicieron tanto para el modo escritorio como el mobile.
  - Se arreglaron los footer que estaban fallando nuevamente.
  - Queda pendiente acomodar la alineacion de las columnas de datos con la de la izquierda.
  ...
  - Arreglado el footer para la orientación horizontal en teléfonos móviles.

19/10/23
  - Configurado el margen del body del stations_style.css en 13px para que se alineen bien los renglones de la tabla.