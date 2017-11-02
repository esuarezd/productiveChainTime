# productiveChainTime
Visual Analytics for temporal data of exportation of productive chain of coffee.

Propuesta Tarea 3 - Visualización de tiempo
Por Edison Suarez Ducon - 201627395

what: (datos)
-------------------------

dataset1: temporales de exportaciones desde 2006 de cacao:
https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Cacao-Exportaciones/chbq-w5mx

dataset2- temporales de exportaciones desde 2006 de cafe : https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Caf-Exportaciones/gzwq-vje7

Dataset3- temporales de exportaciones desde 2006 de Algodon : https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Algod-n-Exportaciones/ttwt-pzeg

Dataset4- temporales de exportaciones desde 2006 de Flores:
https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Flores-Exportaciones/hieb-cqrb

Atributos del dataset-type temporal : anio,mes,CodigoPais, PaisDestino, CodigoDepartamento, DepartamentoOrigen, Partida, Cadena, Producto, CodigoUnidad, CantidadUnidad, ValorMilesCIFDol, ValorMilesPesos, ValorMilesFOBDol, VolúmenToneladas.
Items de todos los datasets: 620.373 rows con datos correspondientes entre 2006 Enero hasta 2017 Junio.


Why: tareas
------------------------
Tarea1. Compare similarities. Comparar similaridades de valores de exportacion de volumen de toneladas.
Tarea2. Compare similarities. Comparar similaridades de valores de exportacion de millones de dolares..
Tarea3. Compare similarities. Comparar similaridades de valores de precios de cadena de produccion por tonelada en usd/toneladas.

- Hipotesis: SE espera un aumento de exportaciones de todos los distintos productos de cadena de exportacion.

How:
------------------------
Tareas: Stacked Area Chart
Marcas: areas para cada dataset
Canales:
Posicion: Una para cada dataset, de abajo hacia arriba. Cacao abajo, algodón encima, despues flores y finalmente cafe.
Color azul de manera degradada: cacao (azul más oscuro oscuro),..., cafe (azul las claro)
Size: Lenght. Es la longitud que va desde termina el canal anterior. La longitus esta asociada con los valores de Volumen, milles de dolares, y relacion de vaor de dolares por tonelada.
