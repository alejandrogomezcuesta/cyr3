# Ejercicios de examen

## **TIPO 1: Encontrar y corregir errores en el código**

*En cada uno de los siguientes programas hay errores que impiden que el código funcione correctamente o que provocan un resultado no deseado. Identifica los errores y dí en qué consisten.*

### **Ejercicio 1** (1 punto)

Este programa:

```python linenums="1"
numero1 = input("Introduce el primer número: ")
numero2 = input("Introduce el segundo número: ")
multi = numero1 * numero2
print(f"La multiplicación es: {multi}")
```

produce este error:

```txt
Introduce el primer número: 4
Introduce el segundo número: 6
Traceback (most recent call last):
  File "c:\Users\Alejandro\github\cyr3\docs\tema1\ejecucion.py", line 3, in <module>
    multi = numero1 * numero2
            ~~~~~~~~^~~~~~~~~
TypeError: can't multiply sequence by non-int of type 'str'
```

Corrige el programa.

### **Ejercicio 2** (1 punto)
 
Este programa:

```python linenums="1"
nota = 1.5
if nota <= 10:
    print("¡Nota máxima!")
else:
    print("No tienes la nota máxima")
```

produce esta salida:

```txt
¡Nota máxima!
```

Corrige el error.

### **Ejercicio 3** (1 punto)

Este programa:

```python linenums="1"
# Queremos imprimir los números del 1 al 100 inclusive
for i in range(1, 5):
    print(i)
```

produce esta salida en la pantalla:

```txt
1
2
3
4
```

Corrige el programa.

## **TIPO 2: ¿Qué se imprime en pantalla?**

*Instrucción para el alumnado: Lee atentamente cada bloque de código y escribe exactamente qué se mostrará en la pantalla cuando se ejecute la última línea (`print`).*

### **Ejercicio 4** (1 punto)

```python linenums="1"
x = 2
y = 4
z = x + y * 3
print(z)
```

### **Ejercicio 5** (1 punto)

```python linenums="1"
puntos = 45
if puntos >= 50:
    puntos = puntos * 2

print(f"Tienes: {puntos} puntos")
```

### **Ejercicio 6** (1 punto)

```python linenums="1"
m = 1
for i in range(1, 4):
    m = m * i
print(m)
```

## **TIPO 3: Crear programas**

### **Ejercicio 7** (2 puntos)

Pide al usuario del programa que escriba cuántos años tiene. Suponiendo que esa persona ya ha cumplido los años este año 2026, el programa tiene que calcular en qué año nació esa persona.

La salida del programa tiene que ser un f-string de la siguiente forma:

*Como tienes **edad** años has nacido en el año **anio_nacimiento**.*

Un ejemplo de la ejecución de este programa sería:

```txt
Díme tu edad: 16.
Como tienes 16 años has nacido en el año 2010.
```
```txt
Díme tu edad: 20.
Como tienes 20 años has nacido en el año 2006.
```

### **Ejercicio 8** (2 puntos)

Haz un programa que le pida al usuario un número con decimales. El programa tiene que decir si ese número es positivo o negativo. Suponemos que el 0 también es positivo.

La salida del programa tiene que ser un f-string de la siguiente forma:

*El número **numero_introducido** es **positivo_o_negativo**.*

Ejemplos de la ejecución de este programa serían:

```txt
Díme un número con decimales: -0.3.
El número -0.3 es negativo.
```

```txt
Díme un número con decimales: 50.
El número 50 es positivo.
```

