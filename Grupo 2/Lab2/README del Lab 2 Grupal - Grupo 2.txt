README del Lab 2 Grupal - Grupo 2

Implementación 1:
Input: 
- Genoma: longitud = n
- Subcadena objetivo: longitud = m
Análisis de la complejidad:
- Las operaciones de asignación son de orden O(1)
- Las operaciones de comparación son de orden O(1)
- Las operaciones aritméticas son de orden O(1)
- El bucle1 se va a ejecutar la cantidad de caracteres del genoma, por lo tanto es de orden O(n)
- El blucle2 se va a ejecutar la cantidad de veces que sea encontrado la subcadena objetivo, en nuestro caso particular, es de orden O(1). Sin embargo, la implementación hace que pueda llegar a ser O(n)
Por lo tanto, la implementación 1 es de orden O(n)

Implementación 2:
Input: 
- Genoma: longitud = n
- Subcadena objetivo: longitud = m
Análisis de la complejidad:
- Las operaciones de asignación son de orden O(1)
- Las operaciones de comparación son de orden O(1)
- La operación de comparación entre dos cadenas es de orden O(m)
- Las operaciones aritméticas son de orden O(1)
- El bucle1 se va a ejecutar la cantidad de caracteres del genoma, y dentro de este, se hace en cada iteración una comparación entre una subcadena del genoma y la subcadena objetivo, por lo tanto es de orden O(n*m)
- El blucle2 se va a ejecutar la cantidad de veces que sea encontrado la subcadena objetivo, en nuestro caso particular, es de orden O(1). Sin embargo, la implementación hace que pueda llegar a ser O(n)
Es posible suponer que m < n, ya que buscar una subcadena de longitud más grande que la cadena en donde se pretende buscar es algo ilógico. 
Por lo tanto, se puede concluir que la implementación 1 es de orden O(n)