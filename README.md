# puzzleZigZag_v1

El puzzle zigzag consiste en una matriz de números comprendidos entre el 1 y el 9, y el objetivo es encontrar un camino en la matriz comenzando por la esquina superior izquierda, y finalizando por la esquina inferior derecha, de forma tal que se pase por todos los números de la matriz en orden ascendente circular (al número más grande le seguirá el más pequeño) una única vez y sin que el camino se cruce. Se permiten movimientos horizontales, verticales y diagonales de longitud 1, es decir siempre a posiciones de la matriz contiguas.


La salida que debe producir el programa es el número de soluciones posibles y distintas al puzzle y a continuación cada una de las soluciones dadas en orden lexicográfico respecto a las coordenadas de los lugares de la matriz que el camino va visitando. Las posiciones de la matriz se identifican de la forma habitual por fila columna comenzando en la esquina superior izquierda. Se recuerda que el orden lexicográfico para pares de valores se define del siguiente modo: abrir paréntesis x subíndice 1 coma y subíndice 1 cerrar paréntesis menor que abrir paréntesis x subíndice 2 coma y subíndice 2 cerrar paréntesis si x subíndice 1 menor que x subíndice 2 o x subíndice 1 igual x subíndice 2 y y subíndice 1 menor que y subíndice 2. Dadas dos secuencias de pares de valores s igual paréntesis izquierdo s subíndice 1 coma espacio s subíndice 2 coma espacio... coma espacio s subíndice n paréntesis derecho y v igual paréntesis izquierdo v subíndice 1 coma espacio v subíndice 2 coma espacio... coma espacio v subíndice n paréntesis derecho , tendremos que  s espacio menor que espacio v en orden lexicográfico si existe i con 1 menor o igual que i menor o igual que n  tal que s subíndice k igual v subíndice k para todo k menor que i espacioy s subíndice i menor que v subíndice i.

La entrada consistirá en una única matriz dada por filas y con un número de filas o de columnas menor o igual a 10. Cada fila de la matriz irá en una línea distinta y cada número de la fila estará separado por un único blanco del siguiente. No habrá blanco ni al principio de la línea ni después del último número.

La salida contendrá en la primera línea el número de soluciones existentes al puzzle y a continuación se dará cada solución separadas entre sí por una línea en blanco (la última solución no irá seguida de una línea en blanco) y ordenadas en orden lexicográfico respecto a las coordenadas de los números del camino.

Cada solución vendrá dada por la matriz de entrada pero separando cada fila de la matriz por una línea adicional que contendrá tantos caracteres como cada una de las filas. Se usarán 5 caracteres entre las posiciones de la matriz para indicar el camino solución. Esos caracteres serán o el caracter blanco o uno de los caracteres '-', '/', '\', '|'. El caracter blanco indicará que dos posiciones no están seguidas en el camino solución; el carácter guión se utilizará para mostrar dos números seguidos en el camino que están en la misma fila de la matriz; el carácter línea vertical '|' se utilizará para mostrar números seguidos en el camino que están en la misma columna pero en filas distintas; el carácter barra inclinada '/' se utilizará para mostrar números seguidos que estando en filas distintas están o bien una columna posterior si es hacia arriba o bien en una columna anterior si es hacia abajo; por último el carácter barra inclinada inversa '\' es el contrario al anterior.

Para ver mejor como se debe formar cada una de las matrices solución es conveniente poner los caracteres en un tabla. Por ejemplo la primera solución del ejemplo que aparece más abajo se ubica en un grid de la siguiente forma:

1 	  	3 	- 	1
| 	/ 		  / 	
2 	  	2 	  	2
  	/ 		  / 	|
3 	- 	1 	  	3

teniendo en cuenta que en las casillas vacías debe ir un espacio en blanco.

Si no hay solución al puzzle dado en la entrada, la salida será simplemente un 0 en una única línea.

Si la entrada al programa es sintacticamente incorrecta la salida será la cadena "Entrada incorrecta."

Ejemplo
Entrada

1 3 1
2 2 2
3 1 3

 

Salida

2
1 3-1
|/ / 
2 2 2
 / /|
3-1 3

1 3-1
| | |
2 2 2
| | |
3-1 3
