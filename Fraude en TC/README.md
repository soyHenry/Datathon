![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

# Fraude en TC

¡Bienvenidos al segundo dataset del Hackathon! Nos ponemos ahora en la piel de un Junior Data Scientist trabajando para la financiera Plasma S.A., dedicada a emitir las tarjetas AMEX en distintos países de latinoamerica. 

## Descripción del Problema

Con los últimos avances tecnológicos en lo que respecta a pagos digitales, nuevas generaciones de ciber delincuentes entran en juego y burlan los sistemas de los mayores bancos y compañías financieras del mundo.

El fraude continua siendo muy común para compras online y presenciales. Al existir una magnitud gigante de transacciones que ocurren diariamente, la detección de fraude se presenta como un desafío para los autores involucrados, tanto compañías financiaras como instituciones gubernamentales.

Debido a la situación actual, se crea un equipo antifraude perteneciente al área de Data Science. Como primer task a realizar en el recién creado equipo, nuestro Team Lider nos pide que armemos un modelo para predecir si cierta transacción realizada con tarjeta de crédito es fraudulenta o no, para agilizar los procesos.

Nuestra meta es plantear un modelo (o serie de ellos), correrlo y utilizar la métrica definida para testear su performance.

## Métrica a utilizar

Se utilizará para evaluar el desempeño del/los modelo/s la precisión (acurracy) de la matriz de confusión (confusion matrix).

$$ Accuracy=\frac{TP+TN}{P+N}$$

siendo $TP$ los verdaderos positivos, $TN$ verdaderos negativos y $P+N$ población total.


## Archivos provistos

Nos proveen el archivo fraude_tc.csv, un  .csv con 1M filas (sin contar header) y 8 columnas con información sobre compras con tarjeta de crédito, entre las cuales se incluye la variable a predecir.

## Descripción de las dimensiones

distancefromhome - la distancia a la que la transacción ocurrió desde la dirección de facturación
distancefromlast_transaction - la distancia de la última transacción
ratiotomedianpurchaseprice - ratio de el monto de transacción sobre la mediana 
repeat_retailer - si la transacción se dió sobre un retailer repetido
used_chip - si la transacción es por chip
usedpinnumber - si la transacción es por PIN
online_order - si la transacción es online
fraud - si la transacción fue o no fraudulenta



