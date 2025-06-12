son variables que almacenan una direccion de memoria al hcaerlo literalmente acceden a todo el contenido del programa pudiendo almacenar cualquier valor en el mismo .
Al acceder a las direcciones de memoria de otras variables en si su uso es idirecto porque al modificar el contenido de un puntero que apunta a determinada variable se modifica la variable es si misma .

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

La direccion a la que apunta un puntero puede ser modificada es lo que los hace tan potentes solo hay que declarar nuevamente a que tipo de varible apuntar en caso de ser necesario y de pasarle la direccion de memoria de la variable a la que apuntara .

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