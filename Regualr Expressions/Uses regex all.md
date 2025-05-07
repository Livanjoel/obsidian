[[Using grep]]
##  [] Coincide con cualquier carácter dentro  
```bash
	[bnmf]inario
```
	Coincide con cualquier palabra que comienza con (bnmf) y termina en inario.
## [^] Coincide con cualquier carácter diferente
```bash
[^n]inario = binario linario Winario
```
	Coincide con cualquier palabra que comienza con cualquier letra diferente de (n)
	Puede usarse en rangos tambien [^a-z] = diferente de ese rango case sentitive
## [char(1)-char(2)] Coincide con cualquier carácter dentro de determinado rango
```bash
	[a-z]inario 
```
		Coincide con cualquier carcter dentro del rango a - z (case sensitive)
```bash
  [A-Z]inario 
```
		Coincide con cualquier caracter en el rango A - Z (case sensitive)

## () Grupos de captura 
```
	
```
## ^ Hace referencia al inicio de la cadena
```plaintext
	^[a-z]{7} = binario = cualquier palabra de 7 carcteres case sensitive al inicio de una cadena
```

## $ Hace referencia al final de la cadena
```bash
	$binario = a la palabra binario al final de una cadena 
```

## | Es equivalente a or 
```plaintext
	[a-z]{3}|[0-9]{3} = cualquier palabra o numero de 3 caracteres (case sensitive) = www 333 lol 999 117 mio
```
## + Hace coincidir infinitamente el anterior token
```bash
	[b]+inario = bbbbbbbbbinario binario bbinario
	[b]+[i]+inario = binario bbbbbbbiiiiiinario 
```
	Coincide cualquier cantidad de repeticiones al carcter
## {} Magnificador hace coincidir el anterior token determinada cantidad de veces
```bash
	[b]{3}inario = bbbinario
```
	Solo hace coincidir determinada cantidada de veces
	Puede tambien ser dentro de un rango determinador de repeticiones {4,8},{2,5}... 

## ? Coincide una vez o ninguna (opcional)
```bash
	binario? = bianr binario 
```

## . Coincide con cualquier carácter pero no puede ser en blanco
```bash
	binari. = binario binaria binari% binariA
```

## * Coincide con el anterior token 0 o ilimitadas veces similar a +
```bash
	bianri* = binari binariiiiiiiiiiiiiiiiiii
	[a-z]* = cualquier palabra (case sensitive)
```
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
```bash
	\s = indentaciones(Tab) y cualquier espacio en blanco
```

## \ Carácter de escape
```bash
	binari\* = binari*
```
		Cnacela el comportamineto de los metacaracteres convirtiendolos en solo caracteres 