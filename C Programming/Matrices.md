Las matrices es una estructura de datos que permiten almacenar u conjunto datos del mismo tipo.
Lo primero que se define es la cantidad de filas y luego la cantidad de columnas.
Las filas y las columnas comienzan a numerarse a partir de cero similar a los vectores.

```plaintext
int matriz[4][4]
						|   |
					line  column
```

```plaintext
#|w|w|w
w|#|w|w
w|w|#|w
w|w|w|#
```


Para invertir intercambiar valores dentro de una matriz sin crear una nueva matriz es necesario crear una copia del contenido de los indices que van a tomar el valor de otra posicion recursivamente 
Pasar el contenido a remplazar dentro del indice indicado pero que ya su contenido esta en la variable temporal.
por ultimo pasar el contenido de la variable temporal a la segunda posicion que fue reescrita en la primera posicion