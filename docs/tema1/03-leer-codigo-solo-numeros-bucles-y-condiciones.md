# Ejercicios de leer código con bucles y condiciones

**Tema:** Bucles `for` y condiciones

---

## Antes de empezar

En estos ejercicios se utiliza `range(inicio, final)` para repetir instrucciones desde `inicio` hasta `final - 1`. La variable del bucle, llamada `indice`, toma un valor diferente en cada repetición.

Lee cada programa paso a paso, completa una tabla de variables y escribe qué muestra por pantalla.

---

## Bloque 1: Bucles `for` con cálculos

## ¿Cómo funciona un bucle `for`?

Un bucle `for` repite un grupo de instrucciones varias veces. En cada repetición, una variable recibe el siguiente valor de una secuencia.

La estructura básica es:

```python
for variable in range(inicio, final):
    instrucciones
```

La función `range(inicio, final)` empieza en `inicio` y termina antes de llegar a `final`. Primero podemos observar únicamente los valores que toma la variable:

```python
for numero in range(1, 4):
    print(numero)
```

El bucle se repite tres veces y muestra:

| Repetición | Valor de `numero` | Salida |
| :--- | :---: | :---: |
| 1 | 1 | 1 |
| 2 | 2 | 2 |
| 3 | 3 | 3 |

```text
1
2
3
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 1]
    B --> C{indice < 4}
    C -- Sí --> D[/Mostrar indice/]
    D --> E[indice = siguiente valor]
    E --> C
    C -- No --> F([Fin])
```

Después podemos utilizar ese índice para realizar un cálculo:

```python
for numero in range(1, 4):
    doble = numero * 2
    print(doble)
```

En este caso, el programa muestra:

```text
2
4
6
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[numero = 1]
    B --> C{numero < 4}
    C -- Sí --> D[doble = numero * 2]
    D --> E[/Mostrar doble/]
    E --> F[numero = siguiente valor]
    F --> C
    C -- No --> G([Fin])
```

### Ejercicio 1: Dobles de los números

```python
for indice in range(1, 6):
    doble = indice * 2
    print(doble)
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 1]
    B --> C{indice < 6}
    C -- Sí --> D[doble = indice * 2]
    D --> E[/Mostrar doble/]
    E --> F[indice = siguiente valor]
    F --> C
    C -- No --> G([Fin])
```

**Tarea:** Escribe todos los valores que muestra el programa.

---

### Ejercicio 2: Cuadrados de los números

```python
for indice in range(2, 7):
    cuadrado = indice * indice
    print(indice, cuadrado)
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 2]
    B --> C{indice < 7}
    C -- Sí --> D[cuadrado = indice * indice]
    D --> E[/Mostrar indice y cuadrado/]
    E --> F[indice = siguiente valor]
    F --> C
    C -- No --> G([Fin])
```

**Tarea:** Completa una tabla con las columnas `indice` y `cuadrado`.

---

### Ejercicio 3: Cálculo de puntos

```python
for indice in range(0, 5):
    puntos = indice * 10 + 5
    print(puntos)
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 0]
    B --> C{indice < 5}
    C -- Sí --> D[puntos = indice * 10 + 5]
    D --> E[/Mostrar puntos/]
    E --> F[indice = siguiente valor]
    F --> C
    C -- No --> G([Fin])
```

**Tarea:** Indica qué valor de `puntos` se obtiene en cada repetición.

---

## Bloque 2: Bucle `for` con `if`

### Ejercicio 4: Múltiplos de tres

```python
for indice in range(1, 11):
    if indice % 3 == 0:
        resultado = indice * 3
        print(resultado)
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 1]
    B --> C{indice < 11}
    C -- Sí --> D{indice % 3 == 0}
    D -- Sí --> E[resultado = indice * 3]
    E --> F[/Mostrar resultado/]
    D -- No --> G[indice = siguiente valor]
    F --> G
    G --> C
    C -- No --> H([Fin])
```

**Tarea:** Explica qué números pasan la condición y qué valores se muestran.

---

### Ejercicio 5: Mayores que cinco

```python
for indice in range(1, 9):
    if indice > 5:
        resultado = indice + 10
        print(resultado)
```

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 1]
    B --> C{indice < 9}
    C -- Sí --> D{indice > 5}
    D -- Sí --> E[resultado = indice + 10]
    E --> F[/Mostrar resultado/]
    D -- No --> G[indice = siguiente valor]
    F --> G
    G --> C
    C -- No --> H([Fin])
```

**Tarea:** Escribe los valores de `indice` que cumplen la condición y el resultado correspondiente.

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

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 1]
    B --> C{indice < 7}
    C -- Sí --> D{indice % 2 == 0}
    D -- Sí --> E[resultado = indice * 2]
    D -- No --> F[resultado = indice + 1]
    E --> G[/Mostrar resultado/]
    F --> G
    G --> H[indice = siguiente valor]
    H --> C
    C -- No --> I([Fin])
```

**Tarea:** Completa una tabla con `indice`, la rama que se ejecuta y `resultado`.

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

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[indice = 10]
    B --> C{indice < 16}
    C -- Sí --> D{indice >= 13}
    D -- Sí --> E[categoria = 1]
    D -- No --> F[categoria = 0]
    E --> G[/Mostrar indice y categoria/]
    F --> G
    G --> H[indice = siguiente valor]
    H --> C
    C -- No --> I([Fin])
```

**Tarea:** Indica qué temperaturas reciben la categoría `0` y cuáles reciben la categoría `1`.

---

## Retos para el alumnado

### Reto 0: Del diagrama de flujo al código

Observa el siguiente diagrama de flujo y escribe el programa Python equivalente. El programa debe mostrar la suma de los números pares del `1` al `6`.

```mermaid
flowchart TD
    A([Inicio]) --> B[suma = 0]
    B --> C[indice = 1]
    C --> D{indice < 7}
    D -- Sí --> E{indice % 2 == 0}
    E -- Sí --> F[suma = suma + indice]
    E -- No --> G[indice = siguiente valor]
    F --> G
    G --> D
    D -- No --> H[/Mostrar suma/]
    H --> I([Fin])
```

**Restricción:** Utiliza un bucle `for`, una condición `if` y una variable acumuladora llamada `suma`.

---

### Reto 1: Tabla de multiplicar

Crea un programa que utilice un bucle `for` para mostrar la tabla de multiplicar del número `7`, desde `7 x 1` hasta `7 x 10`.

**Restricción:** Utiliza el índice del bucle para calcular cada producto.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

---

### Reto 2: Suma de números

Crea un programa que recorra los números del `1` al `10` y muestre el doble de cada número.

**Restricción:** Utiliza un bucle `for` y una variable llamada `doble`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

---

### Reto 3: Números divisibles

Crea un programa que recorra los números del `1` al `20` y muestre solamente los que sean divisibles entre `4`.

**Restricción:** Utiliza un bucle `for`, una condición `if` y el operador `%`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

---

### Reto 4: Clasificador de edades

Crea un programa que recorra las edades del `12` al `18`. Para cada edad, muestra el texto o código que indique si es menor de edad o si ha alcanzado la mayoría de edad.

**Restricción:** Utiliza un bucle `for` y una estructura `if` / `else`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.

---

### Reto 5: Puntuación por rondas

Un juego tiene `8` rondas numeradas del `1` al `8`. Crea un programa que recorra todas las rondas y calcule los puntos de cada una:

- En las rondas impares (`1`, `3`, `5` y `7`) se obtienen `10` puntos.
- En las rondas pares (`2`, `4`, `6` y `8`) se obtienen `20` puntos.

El programa debe mostrar el número de cada ronda y los puntos conseguidos en ella. Por ejemplo, la ronda `1` tendría `10` puntos y la ronda `2` tendría `20` puntos.

**Restricción:** Utiliza un bucle `for`, una estructura `if` / `else` y el operador `%`.
**Además:** Dibuja el diagrama de flujo correspondiente al programa.
