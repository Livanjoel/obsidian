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













