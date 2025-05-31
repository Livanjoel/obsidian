Aquí tienes una lista de los operadores más comunes en el lenguaje C, clasificados por su función:

### Operadores Aritméticos

Se utilizan para realizar operaciones matemáticas básicas.

- `+`: Suma (ej. `a + b`)
    
- `-`: Resta (ej. `a - b`)
    
- `*`: Multiplicación (ej. `a * b`)
    
- `/`: División (ej. `a / b`)
    
- `%`: Módulo (resto de la división entera) (ej. `a % b`)
    

### Operadores Relacionales

Se utilizan para comparar dos valores y devuelven un valor booleano (verdadero o falso, representado como `1` o `0` en C).

- `==`: Igual a (ej. `a == b`)
    
- `!=`: Diferente de (ej. `a != b`)
    
- `>`: Mayor que (ej. `a > b`)
    
- `<`: Menor que (ej. `a < b`)
    
- `>=`: Mayor o igual que (ej. `a >= b`)
    
- `<=`: Menor o igual que (ej. `a <= b`)
    

### Operadores Lógicos

Se utilizan para combinar o negar expresiones lógicas, y devuelven un valor booleano.

- `&&`: AND lógico (verdadero si ambas expresiones son verdaderas) (ej. `a && b`)
    
- `||`: OR lógico (verdadero si al menos una expresión es verdadera) (ej. `a || b`)
    
- `!`: NOT lógico (invierte el valor booleano de una expresión) (ej. `!a`)
    

### Operadores de Asignación

Se utilizan para asignar un valor a una variable.

- `=`: Asignación simple (ej. `a = 5`)
    
- `+=`: Suma y asignación (ej. `a += b` es equivalente a `a = a + b`)
    
- `-=`: Resta y asignación (ej. `a -= b` es equivalente a `a = a - b`)
    
- `*=`: Multiplicación y asignación (ej. `a *= b` es equivalente a `a = a * b`)
    
- `/=`: División y asignación (ej. `a /= b` es equivalente a `a = a / b`)
    
- `%=`: Módulo y asignación (ej. `a %= b` es equivalente a `a = a % b`)
    

### Operadores de Incremento y Decremento

Se utilizan para aumentar o disminuir el valor de una variable en uno.

- `++`: Incremento (ej. `++a` (pre-incremento), `a++` (post-incremento))
    
- `--`: Decremento (ej. `--a` (pre-decremento), `a--` (post-decremento))
    

### Operadores Bit a Bit (Bitwise)

Operan sobre los bits individuales de los operandos.

- `&`: AND bit a bit (ej. `a & b`)
    
- `|`: OR bit a bit (ej. `a | b`)
    
- `^`: XOR bit a bit (ej. `a ^ b`)
    
- `~`: NOT bit a bit (complemento a uno) (ej. `~a`)
    
- `<<`: Desplazamiento a la izquierda (ej. `a << b`)
    
- `>>`: Desplazamiento a la derecha (ej. `a >> b`)
    

### Operador Condicional (Ternario)

Es el único operador ternario en C, y se utiliza para una expresión condicional.

- `?:`: (ej. `condicion ? expresion1 : expresion2`)
    

### Operadores Especiales

- `,`: Operador coma (evalúa expresiones de izquierda a derecha y devuelve el valor de la última expresión) (ej. `(a++, b++)`)
    
- `sizeof`: Devuelve el tamaño en bytes de una variable o tipo de dato (ej. `sizeof(int)`, `sizeof(variable)`)
    
- `&`: Operador de dirección (devuelve la dirección de memoria de una variable) (ej. `&variable`)
    
- `*`: Operador de indirección o desreferencia (accede al valor en la dirección de memoria apuntada por un puntero) (ej. `*puntero`)
    
- `()`: Paréntesis (para agrupar expresiones y controlar la precedencia)
    
- `[]`: Corchetes (para acceder a elementos de arrays)
    
- `->`: Operador de flecha (para acceder a miembros de una estructura o unión a través de un puntero) (ej. `puntero->miembro`)
    
- `.`: Operador de punto (para acceder a miembros de una estructura o unión) (ej. `estructura.miembro`)