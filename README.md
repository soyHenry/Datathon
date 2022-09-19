![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

# Datathon

¡Bienvenidos al Datathon de Henry! Durante esta semana estarán poniendo en práctica sus habilidades en el campo de la predicción. Deberán usar cierta métrica para medir la performance del modelo y que, a su vez, será usada para elegir los mejores modelos.

## Información relevante

Esta datathon es una instancia de evaluación, por lo cual es INDIVIDUAL y OBLIGATORIO para los alumnos de Data Science de Henry. Se disponibilizará un google forms y pueden cargarse los resultados las veces que quieran. Es obligatorio que todos disponibilicen el código utilizado, para validar los modelos construidos.

## Logística del comercio mundial

La logística es un mercado vital en el mundo globalizado y conectado donde vivimos, coordinar el transporte de toda la cadena de suministros desde donde son producidos los bienes hasta que llegan al cliente final es una tarea compleja, que debe ser planificada y ejecutada correctamente para el funcionamiento del comercio, tanto local como mundial. 

Gracias a las nuevas herramientas como el uso de geolocalizadores, registros digitales de entrada/salida de los centros de distribución, distintos medios de transporte terrestres, marítimos y aéreos, además de las herramientas de IoT en toda la cadena de suministro y producción, es posible acumular muchísimos datos, que pueden ser analizados para optimizar los procesos logísticos.

## Descripción del problema

Somos parte de una empresa de logística que trabaja para un portal importante de E-Commerce, y nuestro Team Leader nos da la tarea de implementar un modelo que nos permita predecir si un envío llegará a tiempo o no, según la información contenida en el dataset puesto a disposición para poder prestar atención y mejor seguimiento a aquellos envíos que pueden llegar a dar problemas.

## Entrega
Deben tener el código en un archivo .py o un Jupyter Notebook .ipynb. Debe incluir un buen análisis EDA, feature engineerging explicar paso a paso en el notebook qué hicieron y por qué o adjuntar documentación en archivo PDF o presentación. Es obligatorio que el script genere un archivo .csv sólo con las predicciones, una columna que debe llamarse 'pred' y tenga todos los valores de las predicciones, un valor por fila. De no llamarse así la columna, nuestro script de validación NO LO VA A TOMAR. El nombre del archivo debe ser su usuario de github, si su usuario de github es 'pjr95', el archivo .csv con las predicciones debe llamarse 'pjr95.csv'. Vamos a validar tanto los datos que suban como el código.

## Métrica a utilizar

Como método de evaluación del desempeño del modelo, se utilizará Exhaustividad (Recall) de la matriz de confusión (Confusion Matrix)

$$ Recall=\frac{TP}{TP+FN}$$

siendo $TP$ los verdaderos positivos, $TN$ verdaderos negativos y $FN$ los falsos negativos.

## Archivos provistos

Se proveen los archivos:
- 'E-Commerce_train.xlsx', con 8998 observaciones y 12 dimensiones, incluyendo información sobre si el envío llegó a tiempo o no en el momento del registro. 
- 'E-Commerce_test.xlsx', con 2000 observaciones y 11 dimensiones, sin incluir información sobre si el envío llegó a tiempo o no en el momento del registro.

## Descripción de las dimensiones

- ID: identificador del registro de orden (valor entero).
- Warehouse_block: Almacén de distribución de donde salió la orden (A a F).
- Mode_of_Shipment: Medio de transporte (Flight, Road, Ship).
- Customer_care_calls: Número de llamadas a atención al cliente que hubo por esa orden. (valores enteros del 2 al 7)
- Customer_rating: Puntaje del cliente (valores enteros 1 al 5).
- Cost_of_the_Product: Costo del producto (valor numérico entero de 96 a 310).
- Prior_purchases: Número de compras previas realizadas por el cliente (valor numérico entero de 2 a 10).
- Product_importance: Nivel de importancia del producto (low, medium, high).
- Gender: Género del comprador (F, M).
- Discount_offered: Porcentaje de descuento ofrecido por esa compra (valor numérico entero de 1 a 65):
- Weight_in_gms: Peso del paquete de la orden, en gramos (valor numérico entero de 1001 a 7846).
- Reached.on.Time_Y.N: Información sobre la llegada del paquete a destino (1 si llegó a tiempo, 0 si no llegó a tiempo).


## Sugerencias

- Exploren el dataset. Saquen medidas resumen, vean distribuciones de los datos, analicen bien el tipo de problema, etc.
- Piensen que tipo de modelo podría ser aplicable según la descripción del problema y el tipo de variable de salida.
- Busquen información sobre la métrica aplicada, cada métrica tiene pros y contras.
- En cuanto a la utilización de git, recuerden que si quieren hacer un cambio experimental pero no quieren romper el modelo, pueden utilizar [branching](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).
- Aprovechen esta instancia de aprendizaje, experimenten y, sobre todo, diviértanse!

