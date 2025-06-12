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