README del Taller 1 Grupal - Grupo 2

Input:
- Arreglo de parámetros del polinomio grado 4 (longitud arreglo = 5).
- Valor mínimo del intervalo en el que se buscará la raiz.
- Valor máximo del intervalo en el que se buscará la raiz.

Análisis de la complejidad:

Para este análisis se añadieron comentarios al frente de cada linea del archivo llamado "find_root.ipynb",
por lo cuál se agruparán varios tipos de operaciones para calcular la complejidad del algoritmo.

- Las operaciones de asignación son de orden O(1).
- Las operaciones de comparación son de orden O(1).
- Las operaciones aritméticas son de orden O(1).
- Las operaciones de evaluar el polinómio para un valor de x usando la función "f" son de orden O(n).
- El hecho de iterar el método hasta tener un valor de 0 acorde al error máximo incluido, representa una complejidad
  de O(log_2(n)), esto ya que el intervalo adopta la mitad de su tamaño en cada iteración.

Se puede concluir que la complejidad del algoritmo es O(n*log_2(n)).
