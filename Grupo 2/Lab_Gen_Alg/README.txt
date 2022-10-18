README del laboratorio grupal de algorítmo genético.


Para demostrar cómo reacciona el algoritmo a variadas funciones de optimización 
(lineal, oscilantes(varias frecuencias), etc) se dispusieron 11 tests, en los que 
se cambia la función de optimización y algunos parámetros, los cuales permiten
describir su comportamiento. Cabe destacar que en todas estas pruebas las poblaciones
convergen a un máximo local o global en el rango de búsqueda.

Como se puede observar en los tests 8 a 11, al correrse el algoritmo en funciones con 
varios máximos locales de valores similares, al ser las probabilidades de reproducción 
de los máximos locales similar a aquella del máximo absoluto en el intervalo evaluado, 
el éxito del algoritmo fue menor, especialmente para la representación decimal de los 
genomas. En el test 9 se han variado la cantidad de individuos por generación, y la 
posibilidad de mutación, y en general se observa que el error promedio se mantiene 
relativamente constante a partir de la generación 100 en los casos en que la 
probabilidad de mutación no se aumentó. Más, sin embargo, aun en los casos en que se 
converge a una respuesta, esta raramente es el máximo del intervalo evaluado, aun 
cuando se tiene una gran población. Los mejores resultados para estos experimentos 
con funciones de varios máximos locales de valores similares se obtuvieron en el test 11, 
mediante la representación binaria de los genomas. Cierto es que para mejorar la 
precisión de las respuestas con esta representación, los genomas tuvieron que multiplicar 
su longitud, pero gracias a ello se obtuvo una ganancia en estabilidad y un mejor 
desempeño por parte del algoritmo, sumado al hecho de que se alcanzaron resultados 
satisfactorios manteniendo un número conservador de individuos por generación.

Conclusiones

Teniendo en cuenta que el método principal de la clase Function es simulate_maximum, 
el tiempo computacional ocupado por la clase Function para encontrar optimos locales 
utilizando una adaptación del método genético visto en clase es de:

O(population)+O(generations)*(O(population_size)*O(decimal_places)+O(population)*
O(decimal_places)) 
= O(generation*population_size*decimal_places)

Esta complejidad en función de los parámetros especificados puede ser simplificada en 
terminos de n, por lo que esta sería O(n^3).

En cuanto a la relación de los parámetros del algoritmo con el costo (en espacio)
podemos afirmar que:

El número de elementos de "population" y de "fitness" es igual al número de elementos 
en el parámetro "Tamaño_población".

El número de elementos de "errors" y "top_individuals" es igual al número de elementos 
en la genaración actual.

El algoritmo llega al la mayor cantidad de información almacenada en 
memoria en un mismo instante de tiempo al terminar de evaluar la última generación, 
cuando están almacenados tamaño_poblacion cantidad de arreglos con tamaño_genoma cantidad 
de elementos, además de datos de errores promedio y mejores individuos para cada 
generación, la complejidad espacial crece con respecto a: 
tamaño_poblacion*tamaño_genoma + generaciones.

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

El parámetro que más directamente ha influido en la velocidad de convergencia de la 
respuesta en nuestro algoritmo ha sido la probabilidad de mutar un genoma.
