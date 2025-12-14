
---

# 🐢 Simulación de la Tortuga (Python)

---

## Ejemplo inicial con `turtle`

```python
import turtle

t = turtle.Turtle()   # Crea una tortuga
t.forward(100)        # Avanza 100 unidades
turtle.done()         # Mantiene la ventana abierta
```

---

## Reto 1 –Simula el comportamiento de la tortuga usando solo print y input
Avance hacia adelante
# SE POSICIONO LA TORTUGA EN LA POSICION INICIAL 0 Y AVANZA 50 UNIDADES DIBUJANDO SU RASTRO
### Código

```python
print("Simulación de tortuga:")

posicion = 0
print("La tortuga está en la posición:", posicion)

input("Presiona ENTER para avanzar 50 unidades...")

pasos = 50
print("-" * (pasos - 1) + "→")

posicion += pasos

print("La tortuga avanzó", pasos, "unidades.")
print("La nueva posición es:", posicion)
```

### Salida

```text
Simulación de tortuga:
La tortuga está en la posición: 0
-------------------------------------------------→
La tortuga avanzó 50 unidades.
La nueva posición es: 50
```
<img width="600" height="165" alt="Captura de pantalla 2025-12-14 093112" src="https://github.com/user-attachments/assets/f1de8c72-8267-4f24-bc97-352def62f9f0" />

---

## Reto 2 – Simula la tortuga bajando usando solo print y input
# crea el rastro de una tortuga moviendose hacia abajo usando unicamente print e input.
Movimiento hacia abajo

### Código

```python
print("Simulación de tortuga bajando:")

pasos = 10
input("Presiona ENTER para que la tortuga comience a bajar...")

for i in range(pasos):
    print("|")

print("↓")
```

### Salida

```text
|
|
|
|
|
|
|
|
|
|
↓
```

---

## Reto 3 – Girar y dibujar usando solo print() e input()
# Tortuga avanzando hacia adelante y luego hacia abajo
# Crea el rastro de una tortuga moviendose hacia adelante y luego hacai abajo usando unicamente print e input.
Avanzar y luego bajar (forma de L)

### Código

```python
posicion_x = 0

def adelante(n):
    global posicion_x
    input(f"Presiona ENTER para avanzar {n} unidades hacia la derecha...")
    print("-" * (n - 1) + "→")
    posicion_x += n - 1

def abajo(n):
    input(f"Presiona ENTER para avanzar {n} líneas hacia abajo...")
    for _ in range(n - 1):
        print(" " * posicion_x + "|")
    print(" " * posicion_x + "↓")

print("Simulación de tortuga:\n")
adelante(50)
abajo(10)
print("\nLa tortuga ha terminado su recorrido.")
```

### Salida

```text
-------------------------------------------------→
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 |
                                                 ↓

La tortuga ha terminado su recorrido.
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/a6bbba4f-f3d5-40bc-9924-d6bc96bcdb49" width="550" alt="Salida Reto 3" />
</p>

---

## Reto 4 – : Encapsula los comportamientos anteriores usando funciones
Dibujar escalones (posición acumulada)

### Código

```python
posicion_x = 0
BASE = 4

def adelante(n):
    global posicion_x
    input(f"Presiona ENTER para avanzar {n}...")
    print(" " * BASE + "-" * (n - 1 + posicion_x) + "→")
    posicion_x += n - 1

def abajo(n):
    input(f"Presiona ENTER para bajar {n}...")
    for _ in range(n - 1):
        print(" " * (BASE + posicion_x) + "|")
    print(" " * (BASE + posicion_x) + "↓")

print("Simulación de tortuga dibujando escalones\n")

print("Escalón 1:")
adelante(5)
abajo(2)

print("\nEscalón 2:")
adelante(5)
abajo(2)

print("\nEscalón 3:")
adelante(5)
abajo(2)

print("\nDibujo terminado.")
```

### Salida

```text
Escalón 1:
----→
    |
    ↓

Escalón 2:
--------→
        |
        ↓

Escalón 3:
------------→
            |
            ↓

Dibujo terminado.
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/a733f49b-f0e1-4fb4-8b8f-663f9f419b21" width="450" alt="Salida Reto 4" />
</p>

---
