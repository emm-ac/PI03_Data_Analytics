# <h1 align=center> **PROYECTO INDIVIDUAL Nº3** </h1>

# <h1 align=center>**'Data Analyst'**</h1>

# <h1 align=center>**'Informe del EDA realizado'**</h1>

## **Introducción**

En el presente informe intentaré explicar los datos que fueron extraídos de la web de Enacom, los motivos de su elección, qué transformaciones fueron realizadas y, por último, la información que pretendo obtener de ellos.
<br>
<br>

## **Story Telling**

Previo a detallar lo anteriormente expuesto, intentaré explicar el contexto del trabajo realizado, marcando el punto de partida de todo el estudio.
El Cliente, una empresa prestadora de servicios de telecomunicaciones, me encarga realizar un análisis que permita conocer el comportamiento de su sector a nivel nacional. Es importante destacar que la principal actividad de
esta empresa es brindar Acceso a internet.
Así, con el fin de monitorear la eficacia de los objetivos de la empresa, me han solicitado realizar un dashboard con 4 KPIs que considere oportunos.

Lo que quiero exponer al Cliente es cómo ha crecido el servicio de internet en el país los últimos años. Para completar este panorama enseñaré también el nivel de acceso que tienen los medios tradicionales, la tendencia de comunicación celular y la evolución/avance de la tecnología y velocidad de internet. Esta información servirá para conocer si las estrategias planteadas por la Dirección han sido certeras o, si por el contrario, se deben realizar cambios en ellas.
<br>
<br>

## **Datos extraídos del Enacom**

Luego de analizar el trabajo demandado y revisar la información disponible, mi enfoque estará en exponer la evolución que han tenido los medios tradicionales de telecomunicaciones y los servicios de conexión a internet.
Para este trabajo he diseñado 4 KPIs:

_ Variacion porcentual trimestral del servicio de internet cada 100 hogares por provincia.<br>
Para dar viabilidad a este KPI, fue necesario extraer la tabla que exponía el acceso a internet por cada 100 hogares.

_ Evolución de la distribución de Medios de Telecomunicación por año.<br>
Este KPI requirió de 3 tablas distintas, siendo las correspondientes a los registros de accesos a Internet, Telefonía Fija y TV por suscripción, también cada 100 hogares.

_ Evolución de la comunicación por Telefonía Movil por año.<br>
Para este KPI fue necesario extraer la información de dos tablas que exponen la evolución de la comunicación por SMS y llamadas de telefonía móvil. 

_ Evolución de la velocidad y tecnología de conexión a internet por año y provincia.<br>
Por último, para dar base a este KPI, fue necesario utilizar los datos de dos tablas: la primera con datos de acceso a internet por velocidad; y la segunda por tecnología.


Planteado el objetivo del trabajo, considero que estos datos serán suficientes para que la Dirección pueda acceder a información que les muestre la situación actual (y pasada) de los Medios de Telecomunicaciones.
<br>
<br>

## **EDA realizado**

Los archivos CSV con los datos correspondientes a cada tabla, fueron almacenados en una carpeta en crudo y utilizando un nombre con el que fuera posible identificar fácilmente su contenido y el KPI de destino.

Si bien los archivos de cada KPI fueron tratados individualmente, las tareas de análisis y transformación fueron similares en todos:
_ Luego de importar cada tabla y darle una estructura de DataFrame, el primer paso consistió en analizar la estructura y composición de cada una (número de columnas, valores nulos y cantidad de elementos por columna).

_ Los últimos 3 KPIs estaban compuestos por más de una tabla, por lo que luego de verificar que sus estructuras fueran idénticas, procedí a reordenar los datos y re setear los índices. Con ello obtuve tablas con los datos igualmente ordenados, previendo el cruzamiento o desorden de datos.

_ Teniendo las tablas ordenadas, el siguiente paso fue eliminar las columnas innecesarias y repetidas. Luego unifiqué las tablas de cada KPI concatenando las tablas y verificando su estructura.

_ El último paso consistió en exportar la tabla necesaria para aborar cada KPI a una carpeta en limpio, identificando a cuál indicador corresponde cada una.