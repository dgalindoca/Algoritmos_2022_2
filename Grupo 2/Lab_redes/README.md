README del laboratorio grupal de algorítmo de redes neuronales.

El analisis fue dado en terminos de _n_, donde _n_ representa el numero de entradas del vector al cual se le aplicará la operación ded gradiente. Las asignaciones, operaciones aritméticas y lógicas tienen complejidad constante. Funciones de numpy como "random", "zeros", "matmul", "dot" y "mean" presentan complejidad lineal. Por último, el hecho de iterar sobre el conjunto de entrenamiento por cada entrenamiento, hace que se presente una complejidad cuadrática.
Por esta razón, el resultado de este analisis da que el coste computacional del algoritmo de entrenamiento es de **O(n^2)** al depender del numero de entradas del vector para el numero de operaciones a realizar (hechas con la libreria numpy) y el numero de capas escondidas.