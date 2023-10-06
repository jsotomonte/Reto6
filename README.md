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
def calcular_r1_r2(diametro_esfera, diametro_cono):
    # Calcula el radio de la esfera (r1) como la mitad del diámetro
    r1 = diametro_esfera / 2.0

    # Calcula el radio de la base del cono (r2) como la mitad del diámetro del cono
    r2 = diametro_cono / 2.0

    return r1, r2

def calcular_h(altura_total, r1):
    # Calcula la altura del cono (h) restando la altura total menos el radio de la esfera
    h = altura_total - r1

    return h

# Solicita al usuario ingresar los valores del diámetro de la esfera, diámetro del cono y altura total
diametro_esfera = float(input("Ingresa el diámetro de la esfera: "))
diametro_cono = float(input("Ingresa el diámetro de la base del cono: "))
altura_total = float(input("Ingresa la altura total de la figura: "))

r1, r2 = calcular_r1_r2(diametro_esfera, diametro_cono)
h = calcular_h(altura_total, r1)

print(f"Radio de la Esfera (r1): {r1}")
print(f"Radio de la Base del Cono (r2): {r2}")
print(f"Altura del Cono (h): {h}")
```
1. Se definen dos funciones:
  - **calcular_r1_r2(diametro_esfera, diametro_cono)**: Esta función coge dos argumentos, **diametro_esfera** y **diametro_cono**. Dentro de esta funcion se calcula:
    - El radio de la esfera (r1) como la mitad del diámetro de la esfera
    $$diametro_esfera / 2.0$$
    - El radio de la base del cono (r2) como la mitad del diametro del cono
    $$diametro_cono / 2.0$$
    - La función retorna ambos valores *r1* y *r2* como una dupla.
    - calcular_h(altura_total, r1)**: Esta función toma dos argumentos, **altura_total** y **r1**. Dentro de esta función se calcula:
    - La altura del cono (*h*) restando la altura total de la figura (**altura_total**) menos el radio de la esfera (*r1*). Esto se hace porque la altura del cono es la altura total menos la altura ocupada por la esfera.
    - La función retorna el valor de h.
2. En la función principal:
    - Se solicita al usuario un ingreso por teclado de los valores del diámetro de la esfera , el diámetro de la base del cono y la altura total de la figura.
    - Se llama a la funcion **calcular_r1_r2** con los valores ingresados de **diametro_esfera** y **diametro_cono**. Los valores de *r1* y *r2* se almacenan en las variables **r1** y **r2**, respectivamente.
    - Por ultimo se imprimen los resultados en la pantalla utilizando la función **print**, mostrando los valores de *r1*, *r2* y *h*.
___
### Punto 1.3
+ Como se usa el valor de pi importando math y math.pi
#### Solución 
1. Importar el módulo **math**: para usar el valor de π y otras funciones y constantes matemáticas se puede hacer de la siguiente manera:
```python
import math
```
Esto permitirá acceder a todas las funciones y constantes matemáticas que contiene **math**.
2. Acceder a π usando **math.pi**: Una vez importa el modulo **math**, puedes acceder al valor de utilizando la constante **math.pi**. De la siguiente manera se ve en codigo:
```python
valor_de_pi = math.pi
```
En este caso le asignamos el valor de π a la variable **valor_de_pi**.
3.Ejemplo de uso 
```python
radio = 5
area_del_circulo = math.pi * radio**2
```
___
## Punto 2 
2. Dado la figura de la imagen, desarrolle:

<div align='center'>
<figure> <img src="https://i.postimg.cc/1t4MrzsL/image.png" alt="" width="400" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

+ Una función matemática para calcular el área y el perimetro.
+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado `r`, `a` y `b`.
+ Revise como utilizar el valor de `pi` usando *import math* y *math.pi*
## Solución 
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
1. Se importa el modulo **math*+ para poder utilizar la constante matemática π y realizar los cálculos matemáticos.
2. Se definen cuatro funciones para calcular cada una de las áreas y perimetros solicitados
  - **area_circunferencia(r)**: Esta función toma el radio (*r*) de una circunferencia como argumento y calcula el área de la circunferencia utilizando la fórmula
    $$A = πr^2.$$
    Luego, retorna a el área calculada.
  - **primetro_circunferencia(r)**: Esta función toma el radio(*r*) de una circunfencia como argumento y calcula el perúimetro de la circunferencia utilizando la fórmula
    $$P = 2πr$$
    Luego, retorna a el perímetro calculado.
  - **area_rectangulo(a, b)**: Estan función toma dos argumentos, **a** y **b**, que representan la altura y el largo de un rectángulo. Calcula el área del rectangulo utilizando la fórmula
    $$A = a*b
    Luego, retorna a el área calculada.
  - **perimetro_rectangulo(a, b)**: Esta función también toma dos argumentos **a y b**, que representan la altura y el largo de un rectángulo y calcula el perímetro del rectangulo utilizando la fórmula
    $$P = 2a+2b
    Luego, retorna al perímetro calculado.
3. En la función principal:
  - Se le pide al usuario un ingreso por teclado de los tres valores:
    - **radio_circunferencia**. El radio de la circunferencia.
    - **altura_rectangulo**: la altura del rectángulo.
    - **largo_rectangulo**: El largo del rectángulo.
4. Se utilizan las funciones previamente definidas para calcular el área y el pe´rimetro de la circunferencia y el rectángulo utilizando los valores ingresado por teclado.
5. Finalmente, se imprimen los resultados en la pantalla utilziando la función **print**, mostrando el área y el perímetro de la circunferencia, así como el área y el perímetro del rectangulo.
### Punto 2.2
+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado `r`, `a` y `b`.

# PUNTO 9
1. Módulos mas conocidos que se pueden instalar con PIP:
```
pip install numpy
```
2. Pandas: Biblioteca para análisis de datos en Python.
```
pip install pandas
```
3. Matplotlib: Biblioteca para crear gráficos y visualizaciones.
```
pip install matplotlib
```
4.Requests: Biblioteca para realizar solicitudes HTTP en Python.
```
pip install requests
```
5. Django: Un popular framework web de Python.
```
pip install django
```
6.Flask: Otro framework web de Python, ligero y flexible.
```
pip install flask
```
7. TensorFlow: Biblioteca de código abierto para aprendizaje automático y redes neuronales.
```
pip install tensorflow
```
8. PyTorch: Biblioteca de aprendizaje profundo ampliamente utilizada.
```
pip install torch
```
9. Scikit-learn: Biblioteca para aprendizaje automático y minería de datos.
```
pip install scikit-learn
```
10. Beautiful Soup: Biblioteca para analizar documentos HTML y XML.
```
pip install beautifulsoup4
```
