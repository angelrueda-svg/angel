## 🧪 Ejemplo inicial con `turtle`

```python
import turtle

t = turtle.Turtle()   # Crea una tortuga
t.forward(100)        # Avanza 100 unidades
turtle.done()         # Mantiene la ventana abierta
```

Este ejemplo usa la librería `turtle` para mostrar cómo se mueve gráficamente una tortuga.

---

## 🟢 Reto 1: Avanzar hacia adelante

**Objetivo:** Simular que la tortuga avanza hacia adelante dibujando su rastro con caracteres.

```python
print("Simulación de tortuga:")

# Posición inicial
posicion = 0
print("La tortuga está en la posición:", posicion)

# Avanzar
input("Presiona ENTER para avanzar 50 unidades...")

# Dibujar rastro con '-' y flecha
pasos = 50
print("-" * (pasos - 1) + "→")

# Actualizar posición
posicion += pasos

# Mostrar nueva posición
print("La tortuga avanzó", pasos, "unidades.")
print("La nueva posición es:", posicion)
```

### 📤 Salida esperada

```
Simulación de tortuga:
La tortuga está en la posición: 0
-------------------------------------------------→
La tortuga avanzó 50 unidades.
La nueva posición es: 50
```

---

## 🔽 Reto 2: Movimiento hacia abajo

**Objetivo:** Simular el descenso de la tortuga usando líneas verticales.

```python
print("Simulación de tortuga bajando:")

pasos = 10
input("Presiona ENTER para que la tortuga comience a bajar...")

for i in range(pasos):
    print("|")

print("↓")
```

### 📤 Salida esperada

```
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

## ↘️ Reto 3: Avanzar y luego bajar (forma de L)

**Objetivo:** Representar un recorrido en forma de **L**.

```python
print("Simulación de tortuga:\n")

# Tramo horizontal
input("Presiona ENTER para avanzar 50 unidades hacia la derecha...")
print("-" * 49 + "→")

# Tramo vertical
input("Presiona ENTER para avanzar 10 líneas hacia abajo...")
for _ in range(9):
    print(" " * 49 + "|")
print(" " * 49 + "↓")

print("\nLa tortuga ha terminado su recorrido.")
```

### 📤 Salida esperada

```
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

## 🧱 Reto 4: Dibujar escalones (giro automático)

**Objetivo:** Simular giros y movimientos automáticos para formar escalones.

```python
print("Simulación de tortuga dibujando escalones\n")

# ESCALÓN 1
print("Escalón 1:")
input("ENTER para avanzar 5...")
print("----→")

input("ENTER para bajar 2...")
print("    |")
print("    ↓")

# ESCALÓN 2
print("\nEscalón 2:")
input("ENTER para avanzar 5...")
print("---------→")

input("ENTER para bajar 2...")
print("         |")
print("         ↓")

# ESCALÓN 3
print("\nEscalón 3:")
input("ENTER para avanzar 5...")
print("--------------→")

input("ENTER para bajar 2...")
print("              |")
print("              ↓")

print("\nDibujo terminado.")
```

### 📤 Salida esperada

```
Escalón 1:
----→
    |
    ↓

Escalón 2:
---------→
         |
         ↓

Escalón 3:
--------------→
              |
              ↓

Dibujo terminado.

