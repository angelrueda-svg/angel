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
print("Simulacion de los pasos de una tortuga") 

Pasos_adelante =int(input("¿Cuántos pasos quieres que avance la tortuga? "))
Pasos_abajo = int(input("¿Cuántos pasos quieres que baje la tortuga? "))

print("La tortuga avanza", Pasos_adelante, "pasos.")
print("La tortuga baja", Pasos_abajo, "pasos.")


print("🏁" + "-" * Pasos_adelante )

for i in range(Pasos_abajo):
    print(" " * (Pasos_adelante + 2 ) + "|" )

print(" " * (Pasos_adelante + 1) + "🐢")

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

# --- ESCALÓN 1 ---
print("Escalón 1:")
adelante(5)
abajo(2, 4)

# --- ESCALÓN 2 ---
print("\nEscalón 2:")
adelante(10)
abajo(2, 9)

# --- ESCALÓN 3 ---
print("\nEscalón 3:")
adelante(15)
abajo(2, 14)

print("\nDibujo terminado.")

### 📤 Salida esperada

```
Simulación de tortuga dibujando escalones

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
