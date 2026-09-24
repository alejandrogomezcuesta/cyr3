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
