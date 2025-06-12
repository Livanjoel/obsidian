Las matrices es una estructura de datos que permiten almacenar u conjunto datos del mismo tipo.
Lo primero que se define es la cantidad de filas y luego la cantidad de columnas.
Las filas y las columnas comienzan a numerarse a partir de cero similar a los vectores.
## Definición de una matriz
```plaintext
int matriz[4][4]
						|   |
					line  column
```
## Acceder a determinada posicion de la matriz
```plaintext
#|w|w|w
w|#|w|w
w|w|#|w
w|w|w|#
```
Los indices de la matriz comienzan en cero(0) es decir que \#INDICES\[x]\[x] = \#DEFINIDOS\[x-1]\[x-1]
EJEMPLO

```plaintext
char matriz[1][2]
|A|B| - este es todo el contenido de la matriz una fila dos columnas 
```
```plaintext
printf(val[0][0])--accedeiendo a la posicion linea 1 posicion 1 |||  indice = declaracion-1
OUTPUT
A -- este valor corresponde a la posicion linea 1 columna 1
```
## Accediendo a determinada fila de la matriz
```plaintext
char matriz[1][2]
|A|B| - este es todo el contenido de la matriz una fila dos columnas
```

Para invertir intercambiar valores dentro de una matriz sin crear una nueva matriz es necesario crear una copia del contenido de los indices que van a tomar el valor de otra posicion recursivamente 
Pasar el contenido a remplazar dentro del indice indicado pero que ya su contenido esta en la variable temporal.
Por ultimo pasar el contenido de la variable temporal a la segunda posicion que fue reescrita en la primera posicion