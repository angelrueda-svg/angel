# 🐢 Simulación de la Tortuga (print e input)

---

## Ejemplo inicial con `turtle`

```python
import turtle

t = turtle.Turtle()   # Crea una tortuga
t.forward(100)        # Avanza 100 unidades
turtle.done()         # Mantiene la ventana abierta
```

---

## Reto 1 – Avance hacia adelante

```python
print("Simulación de tortuga:")

# Posición inicial
posicion = 0
print("La tortuga está en la posición:", posicion)

# Avanzar
input("Presiona ENTER para avanzar 50 unidades...")

# Dibujar rastro con '-' + flecha al final
pasos = 50
print("-" * (pasos - 1) + "→")

# Actualizar posición
posicion += pasos

# Mostrar nueva posición
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

---

## Reto 2 – Movimiento hacia abajo

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

## Reto 3 – Avanzar y luego bajar (forma de L)

```python
# Posición horizontal global de la tortuga
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

---

## Reto 4 – Dibujar escalones (posición acumulada)

```python
# Posición horizontal acumulada
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

print("    Escalón 1:")
adelante(5)
abajo(2)

print("\n    Escalón 2:")
adelante(5)
abajo(2)

print("\n    Escalón 3:")
adelante(5)
abajo(2)

print("\n    Dibujo terminado.")
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

