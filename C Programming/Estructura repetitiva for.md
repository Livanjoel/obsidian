## La estructura repetitiva `for` en el lenguaje C es una de las herramientas más fundamentales para controlar el flujo de un programa, permitiendo ejecutar un bloque de código un número específico de veces. Es especialmente útil cuando se conoce de antemano cuántas iteraciones se necesitan.

### Sintaxis General

La sintaxis básica de un bucle `for` en C es la siguiente:

```plaintext
for (inicializacion; condicion; actualizacion) {
    // Bloque de código a repetir
}
```

Cada una de las tres partes dentro de los paréntesis está separada por un punto y coma (`;`).

### Partes del Bucle `for`

1. **Inicialización (`inicializacion`)**:
    
    - Esta parte se ejecuta _una sola vez_ al inicio del bucle, antes de que comience la primera iteración.
    - Se utiliza comúnmente para declarar e inicializar una variable de control (un contador) que se usará para gestionar el número de repeticiones.
    - Puedes inicializar múltiples variables separándolas por comas.
    - **Ejemplo:** `int i = 0;`
2. **Condición (`condicion`)**:
    
    - Esta expresión booleana se evalúa _antes de cada iteración_ del bucle.
    - Si la condición es verdadera (distinta de cero), el bloque de código dentro del `for` se ejecuta.
    - Si la condición es falsa (cero), el bucle `for` termina y el control del programa pasa a la siguiente instrucción después del bucle.
    - Si la condición se omite, se asume que es verdadera, lo que resulta en un bucle infinito a menos que haya una instrucción `break` o `return` dentro del cuerpo del bucle.
    - **Ejemplo:** `i < 10;`
3. **Actualización (`actualizacion`)**:
    
    - Esta parte se ejecuta _después de cada iteracción_ del bloque de código del bucle.
    - Se utiliza para modificar el valor de la variable de control (generalmente incrementarla o decrementarla) para que la condición eventualmente se vuelva falsa y el bucle termine.
    - Puedes realizar múltiples operaciones de actualización separadas por comas.
    - **Ejemplo:** `i++` (incrementa `i` en 1), `i += 2` (incrementa `i` en 2).

### Cómo Funciona el Bucle `for` Paso a Paso

1. **Paso 1: Inicialización**. La expresión de inicialización se ejecuta una vez.
2. **Paso 2: Evaluación de la Condición**. La condición se evalúa.
    - Si es `true` (verdadera), se pasa al Paso 3.
    - Si es `false` (falsa), el bucle termina.
3. **Paso 3: Ejecución del Cuerpo del Bucle**. El bloque de código dentro del `for` se ejecuta.
4. **Paso 4: Actualización**. La expresión de actualización se ejecuta.
5. **Paso 5: Regreso a la Condición**. El control vuelve al Paso 2 (evaluación de la condición).

## Este ciclo continúa hasta que la condición se vuelve falsa.


```plaintext
#include <stdio.h> // Incluye la biblioteca estándar de entrada/salida

int main() {
    // Declaramos la variable de control 'i'
    int i; 

    // El bucle for:
    // 1. Inicialización: i se inicializa en 1.
    // 2. Condición: El bucle continúa mientras i sea menor o igual a 5.
    // 3. Actualización: i se incrementa en 1 después de cada iteración.
    for (i = 1; i <= 5; i++) {
        printf("%d\n", i); // Imprime el valor actual de i
    }

    return 0; // Indica que el programa finalizó correctamente
}

```

### Salida del código :

```plaintext
1
2
3
4
5
```
