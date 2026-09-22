# Ejercicios de Programación en Python para 3º ESO

**Tema:** Bucles `for` y condiciones - soluciones

---

## Antes de empezar

En estos ejercicios se utiliza `range(inicio, final)` para repetir instrucciones desde `inicio` hasta `final - 1`. La variable del bucle toma un valor diferente en cada repetición.

Las tablas de traza muestran cómo cambian las variables mientras avanza el bucle. El símbolo `-` indica que todavía no se ha calculado ningún valor.

---

## Bloque 1: Bucles `for` con cálculos

## ¿Cómo funciona un bucle `for`?

Un bucle `for` repite un grupo de instrucciones varias veces. En cada repetición, una variable recibe el siguiente valor de una secuencia.

La estructura básica es:

```python
for variable in range(inicio, final):
    instrucciones
```

La función `range(inicio, final)` empieza en `inicio` y termina antes de llegar a `final`.

### Ejemplo 1: Mostrar el índice

```python
for numero in range(1, 4):
    print(numero)
```

| Repetición | Valor de `numero` | Salida |
| :--- | :---: | :---: |
| 1 | 1 | 1 |
| 2 | 2 | 2 |
| 3 | 3 | 3 |

**Salida final:**

```text
1
2
3
```

### Ejemplo 2: Calcular el doble

```python
for numero in range(1, 4):
    doble = numero * 2
    print(doble)
```

| Repetición | Valor de `numero` | Valor de `doble` | Salida |
| :--- | :---: | :---: | :---: |
| 1 | 1 | 2 | 2 |
| 2 | 2 | 4 | 4 |
| 3 | 3 | 6 | 6 |

**Salida final:**

```text
2
4
6
```

---

### Ejercicio 1: Dobles de los números

```python
for indice in range(1, 6):
    doble = indice * 2
    print(doble)
```

| Repetición | `indice` | `doble` | Salida |
| :--- | :---: | :---: | :---: |
| 1 | 1 | 2 | 2 |
| 2 | 2 | 4 | 4 |
| 3 | 3 | 6 | 6 |
| 4 | 4 | 8 | 8 |
| 5 | 5 | 10 | 10 |

**Salida final:** `2`, `4`, `6`, `8`, `10`.

---

### Ejercicio 2: Cuadrados de los números

```python
for indice in range(2, 7):
    cuadrado = indice * indice
    print(indice, cuadrado)
```

| Repetición | `indice` | `cuadrado` | Salida |
| :--- | :---: | :---: | :---: |
| 1 | 2 | 4 | `2 4` |
| 2 | 3 | 9 | `3 9` |
| 3 | 4 | 16 | `4 16` |
| 4 | 5 | 25 | `5 25` |
| 5 | 6 | 36 | `6 36` |

---

### Ejercicio 3: Cálculo de puntos

```python
for indice in range(0, 5):
    puntos = indice * 10 + 5
    print(puntos)
```

| Repetición | `indice` | `puntos` | Salida |
| :--- | :---: | :---: | :---: |
| 1 | 0 | 5 | 5 |
| 2 | 1 | 15 | 15 |
| 3 | 2 | 25 | 25 |
| 4 | 3 | 35 | 35 |
| 5 | 4 | 45 | 45 |

---

## Bloque 2: Bucle `for` con `if`

### Ejercicio 4: Múltiplos de tres

```python
for indice in range(1, 11):
    if indice % 3 == 0:
        resultado = indice * 3
        print(resultado)
```

| Repetición | `indice` | ¿`indice % 3 == 0`? | `resultado` | Salida |
| :--- | :---: | :---: | :---: | :---: |
| 1 | 1 | Falso | - | - |
| 2 | 2 | Falso | - | - |
| 3 | 3 | Verdadero | 9 | 9 |
| 4 | 4 | Falso | 9 | - |
| 5 | 5 | Falso | 9 | - |
| 6 | 6 | Verdadero | 18 | 18 |
| 7 | 7 | Falso | 18 | - |
| 8 | 8 | Falso | 18 | - |
| 9 | 9 | Verdadero | 27 | 27 |
| 10 | 10 | Falso | 27 | - |

**Salida final:** `9`, `18`, `27`.

---

### Ejercicio 5: Mayores que cinco

```python
for indice in range(1, 9):
    if indice > 5:
        resultado = indice + 10
        print(resultado)
```

| Repetición | `indice` | ¿`indice > 5`? | `resultado` | Salida |
| :--- | :---: | :---: | :---: | :---: |
| 1 | 1 | Falso | - | - |
| 2 | 2 | Falso | - | - |
| 3 | 3 | Falso | - | - |
| 4 | 4 | Falso | - | - |
| 5 | 5 | Falso | - | - |
| 6 | 6 | Verdadero | 16 | 16 |
| 7 | 7 | Verdadero | 17 | 17 |
| 8 | 8 | Verdadero | 18 | 18 |

**Salida final:** `16`, `17`, `18`.

---

## Bloque 3: Bucle `for` con `if` / `else`

### Ejercicio 6: Par o impar

```python
for indice in range(1, 7):
    if indice % 2 == 0:
        resultado = indice * 2
    else:
        resultado = indice + 1
    print(resultado)
```

| Repetición | `indice` | Rama | `resultado` | Salida |
| :--- | :---: | :--- | :---: | :---: |
| 1 | 1 | `else` | 2 | 2 |
| 2 | 2 | `if` | 4 | 4 |
| 3 | 3 | `else` | 4 | 4 |
| 4 | 4 | `if` | 8 | 8 |
| 5 | 5 | `else` | 6 | 6 |
| 6 | 6 | `if` | 12 | 12 |

**Salida final:** `2`, `4`, `4`, `8`, `6`, `12`.

---

### Ejercicio 7: Clasificación de temperaturas

```python
for indice in range(10, 16):
    if indice >= 13:
        categoria = 1
    else:
        categoria = 0
    print(indice, categoria)
```

| Repetición | `indice` | ¿`indice >= 13`? | Rama | `categoria` | Salida |
| :--- | :---: | :---: | :--- | :---: | :---: |
| 1 | 10 | Falso | `else` | 0 | `10 0` |
| 2 | 11 | Falso | `else` | 0 | `11 0` |
| 3 | 12 | Falso | `else` | 0 | `12 0` |
| 4 | 13 | Verdadero | `if` | 1 | `13 1` |
| 5 | 14 | Verdadero | `if` | 1 | `14 1` |
| 6 | 15 | Verdadero | `if` | 1 | `15 1` |

---

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
