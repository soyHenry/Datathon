![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

# Datathon

¡Bienvenidos al Datathon de Henry! Durante esta semana estarán poniendo en práctica sus habilidades en el campo de la predicción. Deberán usar cierta métrica para medir la performance del modelo y que, a su vez, será usada para elegir los mejores modelos.

## Información relevante

Esta datathon es una instancia de evaluación, por lo cual es INDIVIDUAL e OBLIGATORIO para los alumnos de Data Science de Henry. Se disponibilizará un google forms y pueden cargarse los resultados las veces que quieran. Es obligatorio que todos disponibilicen el código utilizado, para validar los modelos construidos.

## Programa de bicicletas compartidas (Bicycle share scheme)

Los sistemas de bicicletas compartidas están ganando terreno como alternativa de movilización a nivel mundial, debido a su aporte al descongestionamiento de ciudades, a la disminución de emisiones contaminantes y a mejora de la salud de las personas. Este, es un sistema práctico y al alcance de todos, en donde el usuario puede alquilar fácilmente una bicicleta y/o una bicicleta eléctrica desde cierta posición en particular, los cuales son estacionamientos específicos según la entidad que entrega el servicio, y con la opción de devolverla en otro punto de estacionamiento. 

Por otro lado, desde el punto de vista de la ciencia de datos y la investigación, este sistema de bicicletas compartidas toma un papel fundamental en la detección de eventualidades y análisis del comportamiento dentro de una ciudad. Esto debido a que, a diferencia de transportes como buses, metro o automóviles, gracias a los sensores incorporados se puede registrar la información exacta del viaje, como por ejemplo la duración, punto de inicio y punto de llegada. 

## Descripción del problema

Poniéndonos en la situación de que somos parte del equipo de la empresa Rent-Cycle en Wachington DC, y nuestro Team Leader nos da la tarea de implementar un modelo que nos permita predecir la cantidad de bicicletas que se alquilan según la información contenida en el dataset puesto a disposición.

## Métrica a utilizar

Como método de evaluación del desempeño del modelo, se utilizará la Raíz del Error Cuadrático Medio (RECM o RMSE por sus siglas en inglés: Root Mean Square Error).

$$ RMSE=\sqrt{\frac{1}{n}\sum_{i=1}^n(p_i-a_i)^2}$$

siendo $p_i$ el valor pronosticado y $a_i$ el valor observado.

## Archivos provistos

Se proveen los archivos:
- 'Bike_train.xlsx', con 11999 observaciones y 17 dimensiones, incluyendo la cantidad de bicicletas rentadas en el momento del registro. 
- 'Bike_test.xlsx', con 5380 observaciones y 16 dimensiones, sin incluir la cantidad de bicicletas rentadas en el momento del registro.

## Descripción de las dimensiones

- instant: identificador del registro.
- dteday: fecha del registro.
- season: temporada (1: primavera, 2: verano, 3: otoño, 4: invierno).
- yr: año del registro (0: 2011, 1:2012).
- mnth: mes del registro (1 a 12).
- hr: hora del registro (0 a 23).
- holiday: si el día meteorológico es feriado toma el valor 1, sino toma el valor 0 (extraído desde http://dchr.dc.gov/page/holiday-schedule).
- weekday: día de la semana.
- workingday: si el día es laboral toma el valor 1, sino 0. Un día laboral es un día no feriado ni fin de semana.
- weathersit: indica el tipo de clima que hubo el momento del registro, las opciones son:
	- 1: Despejado, algunas nubes o parcialmente nublado.
	- 2: Neblina con nubes, neblina con nubes fragmentadas, neblina con algunas nubes o sólo neblina.
	- 3: Nieve ligera, llovizna con tormenta eléctrica y nubes dispersas o llovizna con nubes dispersas. 
	- 4: Lluvia fuerte con granizos, tormenta eléctrica y neblina, o nieve con niebla.
- temp: temperatura normalizada en grados Celsius. La escala llega hasta un máximo de temperatura de 41ºC.
- atemp: sensación térmica normalizada en grados Celsius. La escala llega hasta un máximo de 50ºC.
- hum: nivel de humedad normalizada. La escala llega hasta un máximo de 100.
- windspeed: velocidad del viento normalizada. La escala llega hasta un máximo de 67 km/h.
- casual: cantidad de usuarios casuales en el registro, siendo aquellos que no están registrados. 
- registered: cantidad de usuarios registrados en el registro.
- cnt: Cantidad total de bicicletas rentadas en el registro, incluyendo ambos tipos de usuarios (casuales y registrados).

## Sugerencias

- Exploren el dataset. Saquen medidas resumen, vean distribuciones de los datos, etc.
- Piensen que tipo de modelo podría ser aplicable según la descripción del problema y el tipo de variable de salida.
- Busquen información sobre la métrica aplicada, cada métrica tiene pros y contras.
- En cuanto a la utilización de git, recuerden que si quieren hacer un cambio experimental pero no quieren romper el modelo, pueden utilizar [branching](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
- Aprovechen esta instancia de aprendizaje, experimenten y, sobre todo, diviértanse!

