
``` python
import turtle

t = turtle.Turtle()   # Crea una tortuga
t.forward(100)        # Avanza 100 unidades
turtle.done()         # Mantiene la ventana abierta
```

``` python
#Reto1. Simula el comportamiento de la tortuga usando solo print y input
# COMENTARIOS
# ACA HACEMOS QUE SE MUEVA HACIA ADELANTE USANDO PRINT Y IMPUT

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

<img width="551" height="582" alt="Captura de pantalla 2025-12-12 093218" src="https://github.com/user-attachments/assets/6e41bef4-fe32-40b0-b63f-bf98af9915c7" />


``` python
#Reto2. Simula la tortuga bajando usando solo print y input
#crea el rastro de una tortuga moviendose hacia abajo usando unicamente print e input.
# COMENTARIOS
# ACA HACEMOS QUE LA TORTUGA SE MUEVA HACIA ABAJO, IGUAL QUE EN EL RETO ANTERIOR LE PEDIMOS DATOS AL USUARIO PARA QUE LA TORTUGA BAJE

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

<img width="681" height="597" alt="Captura de pantalla 2025-12-12 093538" src="https://github.com/user-attachments/assets/02a8e9eb-a664-469a-9b00-57e7a5e61de5" />



``` python
#Reto3. Tortuga avanzando hacia adelante y luego hacia abajo
# Crea el rastro de una tortuga moviendose hacia adelante y luego hacai abajo usando unicamente print e input.
# COMENTARIOS
# ACA PODEMOS VER COMO LA TORTUGA AVANZA Y LUEGO HACE UN GIRO HACIA ABAJO, UTILIZANDO PRIN Y IMPUT E IGUALMENTE PREGUNTANDO AL USUARIO

print("Simulación de tortuga:\n")
# LA TORTUGA REALIZA UN RECORRIDO EN FORMA DE L
# Tramo horizontal
input("Presiona ENTER para avanzar 50 unidades hacia la derecha...")
print("-" * 49 + "→")   # Flecha al final del tramo horizontal

# Tramo vertical hacia abajo
input("Presiona ENTER para avanzar 10 líneas hacia abajo...")
for _ in range(9):
    print(" " * 49 + "|")
print(" " * 49 + "↓")   # Flecha al final del tramo vertical

print("\nLa tortuga ha terminado su recorrido.")
```


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

<img width="727" height="705" alt="Captura de pantalla 2025-12-12 093734" src="https://github.com/user-attachments/assets/4ab9a96b-ffc9-4913-90e8-f795f2c8c21e" />



``` python
#Reto4. Girar y dibujar usando solo print e input.
# ahora la tortuga no solo avanza: tambien gira, observa como lo hace la version grafica.
# COMENTARIOS
EN ESTE EJERCICIO PODEMOS VER COMO YA NO SE PREGUNTAN LOS DATOS AL USUARIO, SI NO QUE SE PROGRAMAN ESOS DATOS PARA QUE SEA DE FORMA AUTOMATICA, OSEA UTILIZANDO FUNCIONES.
#LA TORTUGA DIBUJA 3 ESCALONES  SIGUIENDO INSTRUCCIONES Y DIBUJANDO SU RASTRO

print("Simulación de tortuga dibujando escalones\n")
# --- ESCALÓN 1 ---
print("Escalón 1:")
input("ENTER para avanzar 5...")
print("----" + "→")     # adelante(5) con flecha final

input("ENTER para bajar 2...")
print("    |")
print("    ↓")          # flecha hacia abajo

# --- ESCALÓN 2 ---
print("\nEscalón 2:")
input("ENTER para avanzar 5...")
print("---------" + "→")   # 10 guiones acumulados + flecha

input("ENTER para bajar 2...")
print("         |")
print("         ↓")        # flecha hacia abajo

# --- ESCALÓN 3 ---
print("\nEscalón 3:")
input("ENTER para avanzar 5...")
print("--------------" + "→")   # 15 guiones acumulados + flecha

input("ENTER para bajar 2...")
print("              |")
print("              ↓")        # flecha hacia abajo

print("\nDibujo terminado.")
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


<img width="707" height="842" alt="Captura de pantalla 2025-12-12 093843" src="https://github.com/user-attachments/assets/ead55273-0f9f-4552-88ef-407f62bdc2ec" />
