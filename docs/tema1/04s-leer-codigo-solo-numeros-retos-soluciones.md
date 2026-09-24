# Retos de leer código con bucles y condiciones (Soluciones)

## Retos para el alumnado

Los siguientes retos son los mismos que en el fichero de ejercicios. Aquí se incluye una posible solución para cada uno.

### Reto 0: Del diagrama de flujo al código

```python
suma = 0
for indice in range(1, 7):
    if indice % 2 == 0:
        suma = suma + indice
print(suma)
```

El programa muestra `12`.

### Reto 1: Tabla de multiplicar

Crea un programa que utilice un bucle `for` para mostrar la tabla de multiplicar del número `7`, desde `7 x 1` hasta `7 x 10`.

**Restricción:** Utiliza el índice del bucle para calcular cada producto.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

```python
for indice in range(1, 11):
    resultado = 7 * indice
    print(resultado)
```

---

### Reto 2: Suma de números

Crea un programa que recorra los números del `1` al `10` y muestre el doble de cada número.

**Restricción:** Utiliza un bucle `for` y una variable llamada `doble`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

```python
for indice in range(1, 11):
    doble = indice * 2
    print(doble)
```

---

### Reto 3: Números divisibles

Crea un programa que recorra los números del `1` al `20` y muestre solamente los que sean divisibles entre `4`.

**Restricción:** Utiliza un bucle `for`, una condición `if` y el operador `%`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

```python
for indice in range(1, 21):
    if indice % 4 == 0:
        print(indice)
```

---

### Reto 4: Clasificador de edades

Crea un programa que recorra las edades del `12` al `18`. Para cada edad, muestra el texto o código que indique si es menor de edad o si ha alcanzado la mayoría de edad.

**Restricción:** Utiliza un bucle `for` y una estructura `if` / `else`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

```python
for edad in range(12, 19):
    if edad >= 18:
        categoria = 1
    else:
        categoria = 0
    print(edad, categoria)
```

---

### Reto 5: Puntuación por rondas

Un juego tiene `8` rondas numeradas del `1` al `8`. Crea un programa que recorra todas las rondas y calcule los puntos de cada una:

- En las rondas impares (`1`, `3`, `5` y `7`) se obtienen `10` puntos.
- En las rondas pares (`2`, `4`, `6` y `8`) se obtienen `20` puntos.

El programa debe mostrar el número de cada ronda y los puntos conseguidos en ella. Por ejemplo, la ronda `1` tendría `10` puntos y la ronda `2` tendría `20` puntos.

**Restricción:** Utiliza un bucle `for`, una estructura `if` / `else` y el operador `%`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

```python
for ronda in range(1, 9):
    if ronda % 2 == 0:
        puntos = 20
    else:
        puntos = 10
    print(ronda, puntos)
```
