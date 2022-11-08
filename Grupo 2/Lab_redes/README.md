README del laboratorio grupal de algorítmo de redes neuronales.

El analisis fue dado en terminos de _n_, donde _n_ representa el numero de entradas del vector al cual se le aplicará la operación ded gradiente. Las asignaciones, operaciones aritméticas y lógicas tienen complejidad constante. Funciones de numpy como "random", "zeros", "matmul", "dot" y "mean" presentan complejidad lineal. Por último, el hecho de iterar sobre el conjunto de entrenamiento por cada entrenamiento, hace que se presente una complejidad cuadrática.
Por esta razón, el resultado de este analisis da que el coste computacional del algoritmo de entrenamiento es de **O(n^2)** al depender del numero de entradas del vector para el numero de operaciones a realizar (hechas con la libreria numpy) y el numero de capas escondidas.

Se construyó un nuevo experimento que permite conocer el número de épocas necesarias para entrenar la red neuronal. Para esto se estableció una precisión deseada de 0.7, y se determino que el entrenamiento terminara en caso de que la precisión sea igual a esta precisión deseada o cuando esta precisión no cambie entre épocas. 

Finalmente, se probó cambiando la función de activación para las neuronas de la capa oculta por tanh(), hallando así que aunque la precisión se mantiene igual a cuando se empleó la función sigmoide (0.65), el costo de entrenamiento promedio fue mayor usando esta nueva función de activación, pues en cada iteración este costo superaba al que presentó el experimento anterior.
