README del laboratorio grupal de algorítmo genético.


Para demostrar cómo reacciona el algoritmo a variadas funciones de optimización 
(lineal, oscilantes(varias frecuencias), etc) se dispusieron 11 tests, en los que 
se cambia la función de optimización y algunos parámetros, los cuales permiten
describir su comportamiento. Cabe destacar que en todas estas pruebas las poblaciones
convergen a un máximo local o global en el rango de búsqueda.


Conclusiones

Teniendo en cuenta que el método principal de la clase Function es _simulate_maximum_, 
el tiempo computacional ocupado por la clase Function para encontrar optimos locales 
utilizando una adaptación del método genético visto en clase es de:

O(population)+O(generations)*(O(population\_size)*O(decimal\_places)+O(population)*
O(decimal\_places)) 
= O(generation*population\_size*decimal\_places)

Esta complejidad en función de los parámetros especificados puede ser simplificada en 
terminos de n, por lo que esta sería O(n^3).

En cuanto a la relación de los parámetros del algoritmo con el costo (en espacio)
podemos afirmar que:

El número de elementos de "population" y de "fitness" es igual al número de elementos 
en el parámetro "Tamaño_población".

El número de elementos de "errors" y "top_individuals" es igual al número de elementos 
en la genaración actual.

Teniendo esto en cuenta, podemos afirmar que el costo en cuanto a espacio es:

O(Tamaño_población)+O(generaciones) = O(Tamaño_población+generaciones)

Que simplificado sería O(n+m).

Cuando nos enfocamos en acelerar la convergencia, destaca la influencia de 2 parámetros 
específicos. el primero de ellos es la generación de la población inicial, ya que 
aunque habitualmente esta se genera escogiendo números al azar, existen trabajos sobre 
que es lo que sucedería si los individuos de la población inicial se obtuviesen como 
resultado de alguna técnica heurística o de optimización local, hallando que puede 
acelerar la convergencia del Algoritmo Genético. 
  
Por otro lado, es clara también la importancia de la probabilidad de mutación, pues se 
encarga de asegurar que ningún punto del espacio de búsqueda tenga probabilidad cero 
de ser examinado, lo que tiene una gran importancia para asegurar la convergencia del 
Algoritmo.