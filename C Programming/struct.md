Los tipos de datos son un conjunto de datos agrupados en un solo lugar que son los struct . No tienen que tener el mismo tipo de dato los datos almacenados dentro del struct, pueden ser todos diferentes o todos iguales . Si tienen que tener algun tipo de relacion entre si ya pudieran ser caracteriisticas de determinada cosa como ---> precio , nombre , edad , cantidad de memoria etc...

Los struct son declarados globalmente sino hay que declararlos en cada funcion directamente . A cada estructura de cada una hay que declararle un nombre para despues las variables sepan que tipo  de datos van a almacenar dentro.


```plaintext
#include <stdio.h>
#include <string.h>
-----------------------
struct productos {
  char nombre[50];    ------------------> declaracion global de la estructura de das variables
  float precio;
};
----------------------

struct productos cargarProducto(){     |----> declaracion de la varible con la estructura 
    struct productos producto;  -------|
    printf("Ingrese nombre del producto: ");
    fgets(producto.nombre, 49, stdin);
    printf("Ingrese precio del producto: ");
    scanf("%f", &producto.precio);
    return producto;  --------------------------> retorna un struct 
}                                                  util para modificar varibles dentro de la funcion main

void imprimir(struct productos p){
  printf("%s\n", p.nombre);
  printf("%.2f\n", p.precio);
}

int main()
{
  struct productos productos1; -------------------> declaracion de la variable con el tipo de 
  productos1=cargarProducto();  ---------> la funcion retorna un struct 
  imprimir(productos1);                    por eso modifica la varibles 
}                                          en la funcion main


```

Las funcoines pueden retornar struct y tomarlos como parametros a la vez . Esto es util para modificar las variables dentro de la funcion main.
Las funciones que no retornan datos(void) al pasarle como parametros struct no modifican esos struct porque son variables que se almacenan localmente

Los stuct tambien pueden tener struct anidadas dentro de ellos 