# Reto6
Saludos, está reposición es la solución a los ejercicios del reto 6 de la clase 9 del curso progrmamación de computadores 
___
## punto 1 
1.Dado la figura de la imagen, desarrolle:

<div align='center'>
<figure> <img src="https://i.postimg.cc/FRvCmpxx/image.png" alt="" width="400" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

+ Una función matemática para calcular el volumen y el área superficial.
+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.
+ Revise como utilizar el valor de pi usando import math y math.pi
  
#### Solución 
```python
import math

def calcular_volumen_y_area(r1, r2, h):

    # Calcular el volumen de la esfera
    volumen_esfera = (4/3) * math.pi * r1**3

    # Calcular el volumen del cono
    volumen_cono = (1/3) * math.pi * r2**2 * h

    #Calcular el volumen total 
    volumen_total = volumen_esfera + volumen_cono

    # Calcula el área superficial de la esfera
    area_esfera = 4 * math.pi * r1**2

    # Calcula el área superficial del cono
    area_cono = math.pi * r2 * math.sqrt(r2**2 + h**2) + math.pi * r2**2

    # Calcula el área superficial total
    area_total = area_esfera + area_cono
```
1. Primero se importa el modulo **math** para utilizar funciones matemáticas como **pi** y **sqrt**
2. La función **Calcular_Volumen_Y_Área** coge tres argumentos: **r1** (qué sería el radio de la esfera), **r2** (qé sería el radio de la base del cono) y **h** (qué sería la altura del cono)
3. Dentro de la función se calcula:
     - El volumen de la esfera utilizando la fórmula $$V= 4/3 * πr * 3/1.$$
     - El volumen del cono utilizando la fórmula $$V = 1/3 * πr^2h$$
     - Se suma el volumen de la esfera y el volumen del cono para sacar el volumen total.
     - Se calcula el área superficial de la esfera utilizando la fórmula $$A = 4πr * 2/1$$
     - Se calcula el área superficial del cono utilizando la fórmula $$A = π * r2 * √(r2^2 + h^2) + π * r2^2$$
     - Se suma el área superficial de la esfera y el área superficial del cono para obtener el área superficial total.
4. después la función retorna un diccionario que contiene los resultados calculados.
5. Fuera de la función, se le pide al usuario un ingreso por teclado de los valores de **r1**, **r2** y **h**.
6. Se llama a la función **Calcular_Volumen_Y_Área** con los valores ingresados y se almacenan los resultados en un diccionario llamado **Resultados**
7. Se interacciona a través de los elementos del diccionarios **Resultados** y se imprimen los valores de las cantidades calculadas junto con sus valores correspondientes.
___
### Punto 1.2
+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.
### Solución
```python
import math

# Función para calcular el área de una circunferencia
def area_circunferencia(r):
    return math.pi * r**2

# Función para calcular el perímetro de una circunferencia
def perimetro_circunferencia(r):
    return 2 * math.pi * r

# Función para calcular el área de un rectángulo
def area_rectangulo(a, b):
    return a * b

# Función para calcular el perímetro de un rectángulo
def perimetro_rectangulo(a, b):
    return 2 * a + 2 * b

# Solicita al usuario ingresar el radio de la circunferencia, la altura y el largo del rectángulo
radio_circunferencia = float(input("Ingresa el radio de la circunferencia: "))
altura_rectangulo = float(input("Ingresa la altura del rectángulo: "))
largo_rectangulo = float(input("Ingresa el largo del rectángulo: "))

# Calcula y muestra el área y el perímetro de la circunferencia y el rectángulo
print(f"Área de la circunferencia: {area_circunferencia(radio_circunferencia)}")
print(f"Perímetro de la circunferencia: {perimetro_circunferencia(radio_circunferencia)}")
print(f"Área del rectángulo: {area_rectangulo(altura_rectangulo, largo_rectangulo)}")
print(f"Perímetro del rectángulo: {perimetro_rectangulo(altura_rectangulo, largo_rectangulo)}")
```
Nos están pidiendo que calculemos 
1. Se importa el módulo **math** para utilizar la constante matemática **pi** y realizar cálculos matemáticos.
2. se definen cuatro funciones para calcular las siguientes propiedades geométricas:
  - **Área_Circunferencia(r)**: Calcula el Área de una circunferencia con radio **r** utilizando la fórmula $$A =  πr^2$$
  - **Preimetro_Circunferencia(
