#C
## Buenas Prácticas Clave


1. **¡PRIORIZA LA SEGURIDAD!** Siempre ten en cuenta el tamaño de tus búferes. Los desbordamientos de búfer son la plaga del código C.
2. **Prefiere funciones que acepten el tamaño del búfer de destino:** `snprintf` es tu mejor amigo para construir y copiar cadenas de forma segura. Si tu entorno lo soporta, las funciones `_s` del Anexo K (como `strcpy_s`, `strcat_s`, `strtok_s`) son también excelentes.
3. **Evita funciones inherentemente inseguras:** Destierra `strcpy`, `strcat`, `sprintf`, y `gets` (esta última ni la mencioné de tan peligrosa que es) de tu código nuevo.
4. **Maneja con cuidado `strncpy` y `strncat`:** Recuerda sus peculiaridades con la terminación nula y el cálculo de `n`.
5. **Asegura la terminación nula:** Todas las cadenas en C deben terminar con `\0`. Muchas funciones lo hacen por ti, pero en algunas (como `strncpy` bajo ciertas condiciones) es tu responsabilidad.
6. **Valida la entrada:** Si trabajas con cadenas que vienen de fuentes externas (usuario, red, archivos), valida su longitud y contenido antes de procesarlas.
7. **Conoce tus herramientas:** Entiende bien lo que hace cada función, sus parámetros y su valor de retorno. Lee la documentación (man pages).
8. **Cuidado con `strtok`:** Si debes usarla, entiende sus limitaciones y prefiere `strtok_r` o `strtok_s`.

Dominar estas funciones y, sobre todo, sus implicaciones de seguridad, te convertirá en un programador de C mucho más eficaz y responsable. ¡La práctica constante con estos conceptos es clave!

Si tienes alguna duda sobre una función específica o un escenario de uso, ¡no dudes en preguntar! Estamos aquí para aprender y construir software robusto.