``` python
import turtle

t = turtle.Turtle()   # Crea una tortuga
t.forward(100)        # Avanza 100 unidades
turtle.done()         # Mantiene la ventana abierta
```

``` python
#Reto1. Simula el comportamiento de la tortuga usando solo print y input

print("Simulación de tortuga:")
# Se POSICIONO LA TORTUGA EN LA POSICION INICIAL 0 Y AVANZA 50 UNIDADES DIBUJANDO SU RASTRO
# Posición inicial
posicion = 0
print("La tortuga está en la posición:", posicion)

# Avanzar
input("Presiona ENTER para avanzar 50 unidades...")

# Dibujar rastro con '-' + flecha al final
pasos = 50
print("-" * (pasos - 1) + "→")   # 49 guiones + flecha

# Actualizar posición
posicion += pasos

# Mostrar nueva posición
print("La tortuga avanzó", pasos, "unidades.")
print("La nueva posición es:", posicion)
```


    Simulación de tortuga:
    La tortuga está en la posición: 0
    -------------------------------------------------→
    La tortuga avanzó 50 unidades.
    La nueva posición es: 50


``` python
#Reto2. Simula la tortuga bajando usando solo print y input
#crea el rastro de una tortuga moviendose hacia abajo usando unicamente print e input.

print("Simulación de tortuga bajando:")
#la tortuga avanza hacia abajo dejando el rastro de su movimiento
pasos = 10  # cantidad de pasos hacia abajo

input("Presiona ENTER para que la tortuga comience a bajar...")

for i in range(pasos):
    print("|")

print("↓")  # flechita SOLO al final
```


    Simulación de tortuga bajando:
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




``` python
#Reto3. Tortuga avanzando hacia adelante y luego hacia abajo
# Crea el rastro de una tortuga moviendose hacia adelante y luego hacai abajo usando unicamente print e input.

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

    Simulación de tortuga:


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




``` python
#Reto4. Girar y dibujar usando solo print e input.
# ahora la tortuga no solo avanza: tambien gira, observa como lo hace la version grafica.
#LA TORTUGA DIBUJA 3 ESCALONES  SIGUIENDO INSTRUCCIONES Y DIBUJANDO SU RASTRO
# Posición horizontal acumulada
posicion_x = 0

def adelante(n):
    """
    Movimiento hacia la derecha (→) por n pasos
    conservando la posición acumulada
    """
    global posicion_x
    input(f"Presiona ENTER para avanzar {n}...")
    print(" " * BASE + "-" * (n - 1 + posicion_x) + "→")
    posicion_x += n - 1


def abajo(n):
    """
    Movimiento hacia abajo (↓) por n pasos
    alineado con el final del tramo horizontal
    """
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
Simulación de tortuga dibujando escalones

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
