# productiveChainTime
Visual Analytics for network data of exportation and importation of productive chain of coffe.

Propuesta tarea 4 - Visualización de redes
Por Edison Suarez Ducon - 201627395

What: datos
------------------------
dataset1. Tabla con Importaciones de cadena de producción de cafe.
https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Caf-Importaciones/gxbt-i3rd

dataset2. Tabla con Exportaciones de cadena de producción de cafe.
https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Caf-Exportaciones/gzwq-vje7

Atributos dataset1 (importaciones): anio,mes,CodigoPais, PaisOrigen, CodigoDepartamento, DepartamentoDestino, Partida, Cadena, Producto, CodigoUnidad, CantidadUnidad, ValorMilesCIFDol, ValorMilesPesos, ValorMilesFOBDol, VolúmenToneladas.
items dataset1: 1.345 rows con datos correspondientes entre 2006 Enero hasta 2017 Junio.

Atributos dataset2 (exportaciones): anio,mes,CodigoPais, PaisDestino, CodigoDepartamento, DepartamentoOrigen, Partida, Cadena, Producto, CodigoUnidad, CantidadUnidad, ValorMilesCIFDol, ValorMilesPesos, ValorMilesFOBDol, VolúmenToneladas.
Items dataset2: 37.012 rows con datos correspondientes entre 2006 Enero hasta 2017 Junio.

Para acondicionarlo a una network, se tiene entonces:
Del dataset1(importaciones) se filtran los datos por Anio = 2017.
name  :  colombia.DepartamentoDestino.
Size: Suma de VolumenToneladas
Imports: PaisOrigen1, PaisOrigen2, ...

Y del dataset2 (exportaciones) se filtran los datos por Anio = 2017
name  :  clusterN.PaisDestino.
Size: Suma de VolumenToneladas
Imports: DepartamentoOrigen1, DepartamentoOrigen2, ….

Cada nodo se agrupa segun la region del mundo. Se definen cinco grupos: 1)Departamentos de Colombia, 2)Suramerica, 3)Norteamerica, 4)Europa, 5)Africa, 6)Asia.

Why: tareas
------------------------
Tarea1. Explore topology. Con esta conexiones se muestran los países importan de cada uno de los departamentos.

Tarea2. Explore topology. Con esta conexiones se muestran a los países a los que exporta cada uno de los departamentos.

- Hipotesis: No necesariamente el pais que mas importe cafe es el compra de todos los departamentos.

How:
------------------------
Tarea 1 y 2. Hierarchical Edge Bundling
Marcas: Lineas de conexion entre paises y departamentos
Canales:
Posicion: Para la vsualizacion de orden por SIZE, se ordena de izquierda a derecha cada grupo de paises, de manera descendente.
Color azul en el enlace. Verde para enlaces que entran (importaciones). Rojo para enlaces que salen (exportaciones).


En la pagina, se le presenta al usuario la posibilidad de ver la red ordenando por enlaces o por tamaño. Ordernar por enlaces (SortByImports) muestra de manera descendente los paises que compran productos de cada de los departamentos. En el ordenamiento por tamaño, se muestran de manera descentende (de izquierda a derecha) los paises que mas compran cafe.
