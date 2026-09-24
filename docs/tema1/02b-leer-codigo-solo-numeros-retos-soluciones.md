# Retos de leer código solo con números (Soluciones)

## Bloque 5: Ejercicios de Creación para el Alumnado

### Reto 0: Del diagrama de flujo al código

```python
nota = 7
if nota >= 5:
    resultado = 10
else:
    resultado = 0
print(resultado)
```

El programa muestra `10`.

---

### Reto 1: Conversor de Temperatura

* **Enunciado:** Crea un programa que declare una variable `celsius` con el valor `25`. Calcula la temperatura equivalente en grados Fahrenheit utilizando la fórmula $F = C \times 1.8 + 32$ y guarda el resultado en una variable llamada `fahrenheit`. Finalmente, muestra el valor de `fahrenheit`.
* **Restricción:** Utiliza únicamente operaciones aritméticas básicas.
* **Además:** Dibuja el diagrama de flujo correspondiente al programa.

---

### Reto 2: Control de Aforo

* **Enunciado:** Una sala de juegos tiene un límite de capacidad de 30 personas. Crea un programa que tenga una variable `personas` con el valor `34`.
  * Si la variable `personas` es mayor que 30, define una variable `exceso` que contenga cuántas personas están por encima del límite y muestra `exceso`.
  * En caso contrario (si es menor o igual a 30), asigna el valor `0` a `exceso` y muéstralo.
* **Restricción:** Usa una estructura `if` / `else`.
* **Además:** Dibuja el diagrama de flujo correspondiente al programa.

---

### Reto 3: Calificador de Rangos Numéricos

* **Enunciado:** Crea un programa con una variable `num` inicializada en `45`.
  * Si `num` es menor que `0`, guarda en la variable `categoria` el valor `-1`.
  * Si `num` está entre `0` y `50` (incluidos), guarda en `categoria` el valor `0`.
  * Si `num` es mayor que `50`, guarda en `categoria` el valor `1`.
  * Al final, muestra la variable `categoria`.
* **Restricción:** Utiliza estructuras `if` / `else` anidadas y solo expresiones numéricas/comparaciones básicas.
* **Además:** Dibuja el diagrama de flujo correspondiente al programa.

```python
celsius = 25
fahrenheit = celsius * 1.8 + 32
print(fahrenheit)
```

El programa muestra `77.0`.

```python
personas = 34
if personas > 30:
    exceso = personas - 30
else:
    exceso = 0
print(exceso)
```

El programa muestra `4`.

```python
num = 45
if num < 0:
    categoria = -1
else:
    if num <= 50:
        categoria = 0
    else:
        categoria = 1
print(categoria)
```

El programa muestra `0`.
