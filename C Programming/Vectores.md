#Ccadenas_numericas_strings
Los vectores son estructuras de datos que permiten almacenar un conjunto de datos del mismo tipo
*Con un único nombre se define un vector y con medio de un subindice se accede a los datos del vector

## Para la declaración de un vector le agregamos corchetes abiertos y cerrados y dentro la cantidad de valores que queremos almacenar dentro del vector

```bash
int vector1[5]
```

## Para cargar cada componente debemos indiciar entre corchetes que elemento del vector estamos accediendo.

```bash
#include <stdio.h>
int sueldos[5];
for ( f = 1; f < 5; f++)
{
	int sueldos[5], f;
	for (f = 0; f < 5; f++) {
		printf(" TABLA DE VECTORES \n");
		scanf("%i", &sueldos[f]);
		printf("| %i | %i | %i | %i | %i | \n", sueldos[0], sueldos[1], sueldos[2], sueldos[3], sueldos[4]);
	}
}
```
*Este es un ejemplo de como se va almacenando los datos en los indices de el vector *
* * El indice del vector comienza a contar en cero no en uno. 
* * El vector tiene la cantidad de indices especificados empezando a contarlos desde el cero 
	es decir un vector con 4 indices la posición de el ultimo indice sera la 3
```plaintext
	| 0 | 1 | 2 | 3 |-----> indice hasta el 3
		1   2   3   4  -----> 4 posiciones 
```

