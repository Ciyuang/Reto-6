# RETO 6 👌

## Ejercicio 1
- Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
```python
# Inicializa la variable n1 con 1
n1: int = 1

# Mientras n1 sea menor o igual a 100
while n1 <= 100:
    # Imprime el número y su cuadrado, separados por coma
    print(n1, n1**2, sep=", ")
    # Incrementa n1 en 1
    n1 = n1 + 1
```
**Diagrama de Flujo**
``` mermaid
---
config:
  theme: redux
---
flowchart TD
    A[Inicio] --> B[n1 = 1]
    B --> C{¿n1 <= 100?}
    C -- Sí --> D[Imprimir n1, n1^2]
    D --> E[n1 = n1 + 1]
    E --> C
    C -- No --> F[Fin]
```

## Ejercicio 2
- Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
```python
# Inicializa las variables a y b con 1
a = 1
b = 1

# Mientras a ≤ 999 y b ≤ 1000
while a <= 999 and b <= 1000:
    # Incrementa ambos valores en 1
    a = a + 1
    b = b + 1

    # Si a es impar, se imprime
    if a % 2 != 0:
        print(a)
    
    # Si b es par, se imprime
    if b % 2 == 0:
        print(b)
    
    # Imprime los valores actuales de a y b, separados por coma
    print(a, b, sep=", ")

```
**Diagrama de Flujo**
``` mermaid
---
config:
  theme: redux
---
flowchart TD
    A[Inicio] --> B[a = 1, b = 1]
    B --> C{¿a <= 999 y b <= 1000?}
    C -- Sí --> D[a = a + 1, b = b + 1]
    D --> E{¿a es impar?}
    E -- Sí --> F[Imprimir a]
    E -- No --> G
    F --> G{¿b es par?}
    G -- Sí --> H[Imprimir b]
    G -- No --> I
    H --> I[Imprimir a, b]
    I --> C
    C -- No --> J[Fin]
```

## Ejercicio 3
- Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado.
```python
# Solicita un número entero mayor que 2
numero = int(input("Ingresar un numero mayor que 2: "))

# Mientras el número sea mayor o igual que 2
while numero >= 2:
    # Si es par, se imprime
    if numero % 2 == 0:
        print(numero)
    # Se decrementa el número en 1
    numero = numero - 1
```

**Diagrama de Flujo**
``` mermaid
---
config:
  theme: redux
---
flowchart TD
    A[Inicio] --> B[Leer número]
    B --> C{¿número >= 2?}
    C -- Sí --> D{¿número es par?}
    D -- Sí --> E[Imprimir número]
    D -- No --> F
    E --> F[número = número - 1]
    F --> C
    C -- No --> G[Fin]
```

## Ejercicio 4
- Imprimir el factorial de un número natural n dado.
```python
# Solicita al usuario un número natural
n = int(input("Ingrese un número natural: "))

# Verifica que sea un número natural (opcional)
if n < 0:
    print("El número debe ser natural (mayor o igual a 0).")
else:
    # Inicializa el factorial en 1 y un contador
    factorial = 1
    contador = 1

    # Calcula el factorial usando un ciclo while
    while contador <= n:
        factorial *= contador
        contador += 1

    # Imprime el resultado del factorial
    print(f"El factorial de {n} es {factorial}")
```

**Diagrama de Flujo**
``` mermaid
---
config:
  theme: redux
---
flowchart TD
    A[Inicio] --> B[Leer n]
    B --> C{¿n < 0?}
    C -- Sí --> D[Imprimir error] --> E[Fin]
    C -- No --> F[factorial = 1, contador = 1]
    F --> G{¿contador <= n?}
    G -- Sí --> H[factorial *= contador]
    H --> I[contador += 1]
    I --> G
    G -- No --> J[Imprimir factorial]
    J --> K[Fin]
```

## Ejercicio 5
- Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
```python
# Solicita al usuario un número entre 2 y 50
n = int(input("Ingrese un número entre 2 y 50: "))

# Verifica si el número está dentro del rango válido
if n < 2 or n > 50:
    print("El número debe estar entre 2 y 50.")
else:
    divisor = 1 # Inicializa el divisor en 1

    print(f"Los divisores de {n} son:")

    # Bucle while para encontrar los divisores de n
    while divisor <= n:
        if n % divisor == 0: # Si el residuo es 0, entonces es divisor
            print(divisor) # Imprime el divisor
        divisor += 1 # Incrementa el divisor en 1
```

**Diagrama de Flujo**
``` mermaid
---
config:
  theme: redux
---
flowchart TD
    A[Inicio] --> B[Pedir al usuario un número entre 2 y 50]
    B --> C{¿n está entre 2 y 50?}
    C -- No --> D[Mostrar mensaje de error: Número fuera de rango]
    D --> E[Fin]
    C -- Sí --> F[Inicializar divisor = 1]
    F --> G{¿divisor <= n?}
    G -- Sí --> H{¿n % divisor == 0?}
    H -- Sí --> I[Imprimir divisor]
    H -- No --> J[No hacer nada]
    I --> K[Incrementar divisor en 1]
    J --> K
    K --> G
    G -- No --> L[Fin]
```

# Autor 🤖
- [Juan Carlos Polania Bolivar](https://github.com/Ciyuang)
