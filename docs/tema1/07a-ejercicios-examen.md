# Ejercicios de examen

## **TIPO 1: Encontrar y corregir errores en el código**

*Instrucción para el alumnado: En cada uno de los siguientes programas hay 1 o 2 errores que impiden que el código funcione correctamente o que provocan un resultado no deseado. Identifica los errores y dí en qué consisten.*

### **Ejercicio 1**

```python linenums="1"
for i in range(5):
print(f"Número: {i}")
```

**Solución**: El error está en que faltan espacios delante de la línea 2 para *indentar* esa línea y que forme parte del bucle `for`.

### **Ejercicio 2**

```python linenums="1"
numero1 = input("Introduce el primer número: ")
numero2 = input("Introduce el segundo número: ")
suma = numero1 + numero2
print(f"La suma es: {suma}")
```

### **Ejercicio 3**

```python linenums="1"
nota = 7.5
if nota = 10:
    print("¡Nota máxima!")
```

### **Ejercicio 4**

```python linenums="1"
nombre = "Lucía"
puntos = 100
print("El jugador nombre tiene puntos puntos")
```

### **Ejercicio 5**

```python linenums="1"
# Queremos imprimir los números del 1 al 10 inclusive
for i in range(1, 10):
    print(i)
```

### **Ejercicio 6**

```python linenums="1"
mensaje = "Hola mundo'
print(mensaje)
```

## **TIPO 2: ¿Qué se imprime en pantalla?**

*Instrucción para el alumnado: Lee atentamente cada bloque de código y escribe exactamente qué se mostrará en la pantalla cuando se ejecute la última línea (`print`).*

### **Ejercicio 7**

```python linenums="1"
x = 10
y = 5
z = x + y * 2
print(z)
```

**Solución**: Este programa calcula $z = 10 + 5 * 2$ cuyo resultado es $20$. Por tanto el número $20$ es lo que se muestra al final.

### **Ejercicio 8**

```python linenums="1"
puntos = 45
if puntos >= 50:
    resultado = "Aprobado"
else:
    resultado = "Insuficiente"
print(f"Estado: {resultado}")
```

### **Ejercicio 9**

```python linenums="1"
palabra = "python linenums="1""
contador = 0
for letra in palabra:
    contador = contador + 1
print(contador)
```

### **Ejercicio 10**

```python linenums="1"
suma = 0
for i in range(1, 5):
    suma = suma + i
print(suma)
```

### **Ejercicio 11**

```python linenums="1"
texto = "Ja"
resultado = texto * 3
print(resultado)
```

### **Ejercicio 12**

```python linenums="1"
numero = 14
resto = numero % 3
print(resto)
```

## **TIPO 3: Crear programas**

### **Ejercicio 13**

Tengo un videojuego con las variables:

- *vida* que vale 100.
- *golpes* que vale 5.
- *pociones* que vale 2.

Cada golpe implica restar 10 puntos a la vida. Cada poción restaura 50 puntos a la vida.

Haz un programa que calcule cuánta vida le queda al personaje del juego.


### **Ejercicio 14**

Pide al usuario del programa que escriba en qué año nació.

- Si es antes del año 2000 el programa tiene que decir: "Eres del siglo XX.".
- En otro caso, el programa tiene que decir: "Eres del siglo XXI.".


### **Ejercicio 15**

Escribe un programa utilizando un bucle `for` que muestre los 10 primeros múltiplos del número 7.