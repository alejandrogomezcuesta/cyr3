# Ejercicios de leer código con acumuladores

**Tema:** Bucles, condiciones y variables acumuladoras

---

## ¿Qué es una variable acumuladora?

Una variable acumuladora guarda un resultado que se va actualizando en cada repetición del bucle. Normalmente empieza con un valor inicial, como `0`, y después se modifica usando su valor anterior.

Por ejemplo, en `total = total + numero`, la variable `total` conserva lo acumulado hasta ese momento y añade el nuevo `numero`.

---

## Ejercicio 1: Suma de números positivos

```python
suma = 0

for numero in range(1, 8):
    if numero % 2 == 0:
        suma = suma + numero

print(suma)
```

La variable `suma` acumula únicamente los números pares. El programa muestra `12`.

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[suma = 0]
    B --> C[numero = 1]
    C --> D{numero < 8}
    D -- Sí --> E{numero % 2 == 0}
    E -- Sí --> F[suma = suma + numero]
    E -- No --> G[numero = siguiente valor]
    F --> G
    G --> D
    D -- No --> H[/Mostrar suma/]
    H --> I([Fin])
```

---

## Ejercicio 2: Media de varias notas

```python
suma = 0
cantidad = 0

for nota in range(5, 10):
    suma = suma + nota
    cantidad = cantidad + 1

media = suma / cantidad
print(media)
```

Las variables `suma` y `cantidad` se actualizan en cada vuelta. Al final, `media` contiene la media de las notas `5`, `6`, `7`, `8` y `9`. El programa muestra `7.0`.

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[suma = 0<br>cantidad = 0]
    B --> C[nota = 5]
    C --> D{nota < 10}
    D -- Sí --> E[suma = suma + nota]
    E --> F[cantidad = cantidad + 1]
    F --> G[nota = siguiente valor]
    G --> D
    D -- No --> H[media = suma / cantidad]
    H --> I[/Mostrar media/]
    I --> J([Fin])
```

---

## Ejercicio 3: Cuenta de números mayores que cinco

```python
cantidad = 0

for numero in range(1, 11):
    if numero > 5:
        cantidad = cantidad + 1

print(cantidad)
```

La variable `cantidad` cuenta cuántos números son mayores que `5`. El programa muestra `5`.

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[cantidad = 0]
    B --> C[numero = 1]
    C --> D{numero < 11}
    D -- Sí --> E{numero > 5}
    E -- Sí --> F[cantidad = cantidad + 1]
    E -- No --> G[numero = siguiente valor]
    F --> G
    G --> D
    D -- No --> H[/Mostrar cantidad/]
    H --> I([Fin])
```

---

## Ejercicio 4: Suma de múltiplos de tres

```python
suma = 0

for numero in range(1, 13):
    if numero % 3 == 0:
        suma = suma + numero

print(suma)
```

La variable `suma` acumula los múltiplos de `3`: `3`, `6`, `9` y `12`. El programa muestra `30`.

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[suma = 0]
    B --> C[numero = 1]
    C --> D{numero < 13}
    D -- Sí --> E{numero % 3 == 0}
    E -- Sí --> F[suma = suma + numero]
    E -- No --> G[numero = siguiente valor]
    F --> G
    G --> D
    D -- No --> H[/Mostrar suma/]
    H --> I([Fin])
```

---

## Ejercicio 5: Mayor valor encontrado

```python
mayor = 0

for numero in range(1, 10):
    valor = numero * 3 - 2
    if valor > mayor:
        mayor = valor

print(mayor)
```

La variable `mayor` conserva el valor más grande encontrado hasta cada momento. El programa muestra `25`.

**Diagrama de Flujo:**

```mermaid
flowchart TD
    A([Inicio]) --> B[mayor = 0]
    B --> C[numero = 1]
    C --> D{numero < 10}
    D -- Sí --> E[valor = numero * 3 - 2]
    E --> F{valor > mayor}
    F -- Sí --> G[mayor = valor]
    F -- No --> H[numero = siguiente valor]
    G --> H
    H --> D
    D -- No --> I[/Mostrar mayor/]
    I --> J([Fin])
```

---
