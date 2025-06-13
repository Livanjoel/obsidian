#C #punteros
son variables que almacenan una dirección de memoria al hacerlo literalmente acceden a todo el contenido del programa pudiendo almacenar cualquier valor en el mismo .
Al acceder a las direcciones de memoria de otras variables en si su uso es indirecto porque al modificar el contenido de un puntero que apunta a determinada variable se modifica la variable es si misma .

```palintext
int numero = 10;
int *ptr = &numero;

printf("Valor de numero: %d\n", numero);    // Imprime 10
printf("Direccion de numero: %p\n", &numero); // Imprime la direccion de numero (formato hexadecimal)
printf("Valor almacenado en ptr (la direccion de numero): %p\n", ptr); // Imprime la misma direccion
printf("Valor al que apunta ptr: %d\n", *ptr); // Imprime 10 (accede al valor en la direccion que guarda ptr)

*ptr = 20; // Modifica el valor en la direccion a la que apunta ptr
           // Esto cambia el valor de 'numero' a 20
printf("Nuevo valor de numero: %d\n", numero); // Imprime 20
```

necesariamente primero hay que indicarle a que direccion de memoria va a acceder(variables) 
```bash
int *ptr = &numero; ----->se debe indicar que va a apuntar a una varible tipo int y se le pasa su direccion
```

La dirección a la que apunta un puntero puede ser modificada es lo que los hace tan potentes solo hay que declarar nuevamente a que tipo de varible apuntar en caso de ser necesario y de pasarle la direccion de memoria de la variable a la que apuntara .

```plainetxt
#include <stdio.h>
#include <stdlib.h> // Para malloc y free

int main() {
    int a = 10;
    int b = 20;
    int c = 30;

    int *ptr; // Declara un puntero a un entero

    // 1. ptr inicialmente apunta a 'a'
    ptr = &a;
    printf("ptr apunta a 'a'. Valor: %d, Direccion de ptr: %p, Contenido de ptr: %p\n", *ptr, (void*)&ptr, (void*)ptr);

    // 2. ptr ahora apunta a 'b' (se ha modificado la direccion que contiene ptr)
    ptr = &b;
    printf("ptr ahora apunta a 'b'. Valor: %d, Direccion de ptr: %p, Contenido de ptr: %p\n", *ptr, (void*)&ptr, (void*)ptr);

    // 3. ptr ahora apunta a 'c'
    ptr = &c;
    printf("ptr ahora apunta a 'c'. Valor: %d, Direccion de ptr: %p, Contenido de ptr: %p\n", *ptr, (void*)&ptr, (void*)ptr);

    // 4. ptr puede apuntar a memoria dinámica
    int *dinamic_int = (int*)malloc(sizeof(int));
    if (dinamic_int == NULL) {
        fprintf(stderr, "Error al asignar memoria.\n");
        return 1;
    }
    *dinamic_int = 100;
    ptr = dinamic_int; // ptr ahora apunta al entero en memoria dinámica
    printf("ptr ahora apunta a memoria dinamica. Valor: %d, Direccion de ptr: %p, Contenido de ptr: %p\n", *ptr, (void*)&ptr, (void*)ptr);

    free(dinamic_int); // Liberar la memoria dinámica

    return 0;
}
```
## OJO
Al declarar el tipo de variable a la que apuntara el puntero y pasarle la direccion de memoria de la variable en la misma linea el puntero hay que representarlo con su \*

Si el caso fuese que ya el puntero se le declaro el tipo de variable a la que va a apuntar el puntero no debe ser representado con el *

Por decirlo de alguna manera son un tipo de dato que de cierta manera se reduce a la expresión  y = &x ---> almacenar memoria y en ese lugar de la memoria se encuentran los datos de la variable.
## Relación de punteros con vectores y matrices
[[struct]][[Matrices]]
Los punteros tienen mucha relacion\ con los vectores y matrices ya que al hacer la asignacion de memoria al vector se le puede pasar el mismo vector o matriz .
```plaintext
#include <stdio.h>

// los vectores son punteros que almacena la direccion del primer componente //
int main() {
  int vec[] = {22, 32,
               44}; // vec almacena la direccion de el primer componente  //
  int *punt;
  punt = vec; // por eso esta asignacion de direccion de memoria es valida
              // porque vec[] almacena la direccion del primer componente //
  for (int l = 0; l < 3; l++) {
    printf("%d|", punt[l]); // aqui hay algo de abstraccion ya que se puede
                            // acceder a los subindices de la variable vec[]
                            // pero usando el puntero como la misma variable
                            // ahora se puede acceder al contenido del vector
                            // desde cualquiera de las dos variable //
  }
}
```
## Operadores de punteros
Las matrices y vectores son punteros pero que apuntan a varias direcciones de memoria aumentando en un byte para cada indice
al intentar aumentar o decrementar una matriz o vector el mismo compilador no permite dicha acción.
Pero si a otro puntero no declarado como un vector o matriz le asignamos la dirección de memoria de una matriz o vector si se podrá operar con ese puntero deccrementandolo o aumentándolo
```plaintext
#include <stdio.h>

void cargar(char *ptr){
  for (int l=0; l<5; l++,ptr++) {
    scanf("%c", ptr);
    getchar(); // sino se consume el salto de linea que deja scanf produce una
               // incorrecta introducion de datos //
  }
}

int main() {
  char palabra[5];
  char *ptr;
  ptr=palabra;
  cargar(ptr);
  printf("%c|%p\n", *ptr, ptr); //el puntero apuntara 1byte delantae en cada interaccion (el siguiente caracter)
  ptr++;
  printf("%c|%p\n", *ptr, ptr);
  ptr++;
  printf("%c|%p\n", *ptr, ptr);
  ptr++;
  printf("%c|%p\n", *ptr, ptr);
  ptr++;
  printf("%c|%p\n", *ptr, ptr);
  printf("Variable\n");
  printf("%s", palabra);
}
```

## OJO
Para acceder a los campos de un \*struct se puede utilizar el operador flecha -> pero hay que seguir usando el amperssan
ya que el operador flecha su función es especificar la ruta hacia los campos de \*struct no se accede a la direccion de la memoria sino al contenido de la memoria de el campo especificado
```bash
struc producto{
	char nobmbre[50];
	float precio;
}

scanf("%f", &mi_struct->precio)
```

## Asterisco(Desreferenciacion*)
La desreferenciacion de un puntero es el proceso para acceder al valor almacenado en la direccion de memoria a la que apunta el puntero > Se realiza mediante el operador de desreferenciacion \*

El asterisco se usa siempre que se va a declarar un puntero.
Al no usarlo se indica que se quiere acceder a la dirección de memoria del puntero.
Al usarlo se indica que se quiere acceder al contenido de la dirección de memoria.
Al usarlo en la declaracion y asignacion de un puntero su función es declaratoria no de acceso a su contenido.