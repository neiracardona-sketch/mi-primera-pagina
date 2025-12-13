# Tarea 2 - Ejercicios Unidad 1  
## Aprendiendo a programar como una tortuga

---

## 🐢 Reto 1: Simular el comportamiento de la tortuga 
*Enunciado:*  
Simular el movimiento de una tortuga usando solo print() e input().
Este es el código paso hacia adelante y pide los pasos (n) 
tortuga = ">"
pasos_adelante= int (input("Ingrese el número de pasos hacia adelante: "))
print ("- " * (pasos_adelante ) + tortuga)

### ✅ Solución en Python
<img width="691" height="135" alt="image" src="https://github.com/user-attachments/assets/6ac3d429-9aa3-456b-93c6-4ccf3e5e5203" />


## 🐢 Reto 2: Tortuga bajando
*Enunciado:* 
Crea el rastro de una tortuga moviéndose hacia abajo usando únicamente print() e input().

Este es el código paso hacia abajo pide los paso 
tortuga = "v"
pasos_abajo= int (input("Ingrese el número de pasos hacia abajo: "))
print ("|\n" * (pasos_abajo ) + tortuga)

### ✅ Solución en Python
<img width="694" height="184" alt="image" src="https://github.com/user-attachments/assets/06f3c764-bab3-42e5-971c-6bccb5cb89e5" />

## 🐢 Reto 3: Girar y dibujar usando texto
*Enunciado:* 
Simula el movimiento: avanzar y luego girar a la derecha para volver a avanzar.
Pide al usuario los paso adelante y abajo
tortuga = ">"
tortuga_abajo= "v"
pasos_adelante= int (input("Ingrese el número de pasos hacia adelante: "))
print ("- " * (pasos_adelante )+tortuga )
espacios = "  " * pasos_adelante 
camino_abajo = espacios + "|\n"
pasos_abajo= int (input("Ingrese el número de pasos hacia abajo: "))
print(camino_abajo * (pasos_abajo), end='')
print(espacios+tortuga_abajo)

### ✅ Solución en Python
<img width="701" height="190" alt="image" src="https://github.com/user-attachments/assets/14b01b16-c856-4bfb-8dbf-9cd4edc927ec" />

## 🐢 Reto 4: Encapsular con funciones
*Enunciado:* 
Crear funciones adelante(n) y abajo(n) que simulen los movimientos.
Reescribe los retos anteriores creando funciones que representen los movimientos de la tortuga solo con texto.


tortuga = ">"
tortuga_abajo = "v"
adelante = 5    # Dibuja el movimiento hacia la derecha (→) por n pasos
abajo = 3       # Dibuja el movimiento hacia abajo (↓) por n pasos
print("- " * adelante + tortuga)
espacios = "  " * adelante 
camino_abajo = espacios + "|\n"
print(camino_abajo * abajo, end='')
print(espacios + tortuga_abajo)

### ✅ Solución en Python
<img width="698" height="201" alt="image" src="https://github.com/user-attachments/assets/a9b1a590-d79d-410d-b4c9-4f0479e20521" />

## 🐢 Reto 5: La tortuga baja las escaleras
*Enunciado:* 
Ajusta las funciones para que la tortuga baje escalones.
# Variable global para recordar dónde estamos (la sangría)
espacios_acumulados = ""
# --- Definición de las funciones ---

def adelante(pasos):
    global espacios_acumulados
    # 1. Imprime los espacios que llevamos + los guiones + la flecha
    print(espacios_acumulados + "- " * pasos + ">")
    
    # 2. Actualiza la variable de espacios para el futuro.
    #    (Agregamos 2 espacios vacíos por cada paso dado)
    espacios_acumulados = espacios_acumulados + ("  " * pasos)

def abajo(pasos):
    # Dibuja las líneas verticales usando los espacios acumulados
    linea_vertical = espacios_acumulados + "|\n"
    print(linea_vertical * pasos, end='')

# --- EJECUCIÓN DEL DIBUJO ---

# Escalón 1
adelante(5)
abajo(2)

# Escalón 2
adelante(5)
abajo(2)

# Escalón 3
adelante(5)
abajo(2)

# Final (Opcional: pone la "v" al final de todo)
print(espacios_acumulados + "v")

### ✅ Solución en Python
![Uploading image.png…]()






