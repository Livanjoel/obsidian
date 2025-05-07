[[Using grep]]
##  [] Coincide con cualquier carácter dentro  
```bash
	[bnmf]inario
```
	Coincide con cualquier palabra que comienza con (bnmf) y termina en inario.
## [^] Coincide con cualquier carácter diferente
```bash
[^n]inario
```
	Coincide con cualquier palabra que comienza con cualquier letra diferente de (n) ^
## [char(1)-char(2)] Coincide con cualquier carácter dentro de determinado rango
```bash
	[a-z]inario 
```
		Coincide con cualquier carcter dentro del rango a - z (case sensitive)
```bash
  [A-Z]inario 
```
		Coincide con cualquier caracter en el rango A - Z (case sensitive)
## + Hace coincidir infinitamente el anterior token
```bash
	[b]+inario = bbbbbbbbbinario binario bbinario
	[b]+[i]+inario = binario bbbbbbbiiiiiinario 
```
	Coincide cualquier cantidad de repeticiones al carcter
## {} Magnificador hace coincidir el anterior (token) determinada cantidad de veces
```bash
	[b]{3}inario = bbbinario
```
	Solo hace coincidir determinada cantidada de veces
	Puede tambien ser dentro de un rango determinador de repeticiones {4,8},{2,5}... 

## ? Coincide una vez o ninguna 
```bash
	binario? = bianr binario 
```

## . Coincide con cualquier carácter pero no puede ser en blanco
```bash
	binari. = binario binaria binari% binariA
```

## * Coincide con cualquier carácter o ninguno similar a +
	bianri* = binari binariiiiiiiiiiiiiiiiiii
## \d Coincide con cualquier carácter numérico
```bash
	\d = 1 al 9 equivalent [0-9]
```

## \D Coincide con cualquier carácter no numérico
```bash
	\D = a hasta z (case insnsitive) and @$)_+=^&$*... equivalent [^0-9]
```

## \w Coincide con cualquier carácter
```bash
	\w = equivalent [0-9a-zA-Z_] 
```

## \s Coincide con cualquier espacio en blanco
	\s = indentaciones(Tab) y cualquier espacio en blanco
