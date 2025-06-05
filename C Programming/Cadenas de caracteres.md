#Cstrings
Las cadenas de caracteres son una estructura de datos que almacenas caracteres en sus indices para crear las cadenas de caracteres .
En C las cadenas de caracteres hay que definirlas previamente ya que son variables .
Las cadenas ya definidas no pueden ser redefinidas de ninguna manera.
	Una manera de tomar o (modificar) una cadena es darle un limitador en uno de sus indices es decir asignarle el carácter nulo(\o) a uno de sus indices y la cadena seria de cierta manera valida hasta ese carácter, esto aplica mayormente a palabras pocas veces a oraciones.
	También esta la posibilidad de crear una nueva cadena y tomar solo lo necesario de la cadena anterior para crear una cadena reducida de la original.
## Funciones que ayudan en la manipulación de cadenas

srtlen()	
> [ Devuelve un numero entero con la cantidad de caracteres de la cadena ] size_t strlen(const char \*str);
> Librería <string.h>
		size_t -->es un entero que devuelve strlen con la cantidad de caracteres que tiene la cadena.
		const char -->es el tipo de dato que strlen puede recibir (char).
			const-->constante-->no modificable
			char-->tipo de dato char\[]
		\*str-->es un puntero a el primer carácter de la cadena que quieres determinar.

fgets()
> [ Permite la assignation de valores a una cadena ] char *fgets(char \*str, int n, FILE \*stream);
> Liberia <stdio.h>
> 		char \*str-->Es un puntero o buffer donde se almacenara la cadena (debe ser lo suficientemente grande para almacenar toda la cadena incluido el salto de linea que toma al pulsar la tecla ENTER(\n)).
> 		int n-->Es el numero maximo de caracteres al leer incluyendo el caracter nulo-->fgets toma *x-1 poniendo el salto de linea en la ultima posicion al presionar la telca ENTER.
> 		`FILE *stream`: Es el puntero al flujo de entrada del cual se leerán los datos.
				- Para leer desde el teclado, usas `stdin`.
				- Para leer desde un archivo, usas el puntero de archivo devuelto por `fopen()`.
				- su formato es x\[5] x\[4]='\n'

strcpy()
> [ Copia el contenido de una cadena a otra] char \*strcpy(char \*dest, const char \*src);
> Liberia <string.h>
			`char *dest`: Un puntero a la cadena de destino donde se copiará la cadena.
				Este búfer **debe ser lo suficientemente grande** para contener la cadena de origen (incluido el carácter nulo `\0`).
			`const char *src`: Un puntero a la cadena de caracteres de origen que se va a copiar. El calificador `const` indica que la función no modificará la cadena de origen.

strncmp()

> [Compara dos cadenas desde cierto punto o totalmente] int strncmp(const char *str1, const char *str2, size_t n);
> Liberia <string.h>
			const char *str1--> Un puntero a la primera cadena a comparar. El calificador const indica que la cadena no se modificara.
			const char *str2--> Un puntero a la segunda cadena a comparar. El calificador const indica que la cadena no se modificara.
			size_t n--> Es el numero maximo de caracteres a comparar en cada cadena. La comparación se detendrá solo después de n caracteres o que alguna cadena alcance el caracter nulo(\0)
			### Valor de retorno: ### 
			La función `strncmp()` devuelve un valor entero que indica el resultado de la comparación:
			- **`0`**: Si las primeras `n` (o menos, si una cadena termina antes) caracteres de `str1` son iguales a los de `str2`.
			- **Un valor negativo (< 0)**: Si el primer carácter diferente en `str1` es menor (en valor ASCII) que el carácter correspondiente en `str2`.
			- **Un valor positivo (> 0)**: Si el primer carácter diferente en `str1` es mayor (en valor ASCII) que el carácter correspondiente en `str2`.

strcat()

> [Une dos cadenas(concatenar)] char *strcat(char *dest, const char *src);
> Liberia <string.h>
> 			`char *dest`: Este es un puntero a la cadena de caracteres _destino_. Aquí es donde se copiará el contenido de la cadena fuente. **¡Es crucial que esta cadena tenga suficiente espacio asignado para contener tanto su contenido original como el contenido de la cadena fuente!** Si no hay suficiente espacio, se producirá un **desbordamiento de búfer (buffer overflow)**, lo cual es una vulnerabilidad de seguridad grave y un error común.
> 			`const char *src`: Este es un puntero a la cadena de caracteres _fuente_. Su contenido se añadirá al final de la cadena destino. Se declara como `const` porque la función no modifica la cadena fuente.
> 				
> 				### **¿Cómo realiza la concatenación?** ###
					1. `strcat()` localiza el carácter nulo (`\0`) que marca el final de la cadena `dest`.
					2. A partir de esa posición (justo después del `\0`), comienza a copiar cada carácter de la cadena `src` a la cadena `dest`.
					3. Una vez que ha copiado todos los caracteres de `src`, añade un nuevo carácter nulo (`\0`) al final de la cadena `dest` para asegurar que sea una cadena bien formada














