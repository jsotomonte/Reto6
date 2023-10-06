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
##  PUNTO 3
```python
def calcular_cantidad_carne(N, M, K):
    # Peso de una gallina, un gallo y un pollito en kilos
    peso_gallina = 6
    peso_gallo = 7
    peso_pollito = 1

    # Calcular el peso total de las gallinas, gallos y pollitos
    peso_total_gallinas = N * peso_gallina
    peso_total_gallos = M * peso_gallo
    peso_total_pollitos = K * peso_pollito

    # Calcular el peso total de carne de aves en kilos
    peso_total_carne = peso_total_gallinas + peso_total_gallos + peso_total_pollitos

    return peso_total_carne

# Solicitar al usuario ingresar la cantidad de gallinas, gallos y pollitos
N = int(input("Ingresa la cantidad de gallinas: "))
M = int(input("Ingresa la cantidad de gallos: "))
K = int(input("Ingresa la cantidad de pollitos: "))

# Calcular la cantidad total de carne de aves y mostrar el resultado
total_carne = calcular_cantidad_carne(N, M, K)
print(f"La cantidad total de carne de aves es de {total_carne} kilos.")
```
1.Se definió una función llamada calcular_cantidad_carne que toma tres parámetros: N, M y K. Estos parámetros representan la cantidad de gallinas, gallos y pollitos, respectivamente.

2.Dentro de la función, se declaran tres variables: peso_gallina, peso_gallo y peso_pollito, que representan el peso en kilogramos de una gallina, un gallo y un pollito, respectivamente. Estos valores se utilizan más adelante en los cálculos.

3.Luego, se calcula el peso total de las gallinas multiplicando la cantidad de gallinas (N) por el peso de una gallina (peso_gallina).

4.Se calcula el peso total de los gallos de manera similar multiplicando la cantidad de gallos (M) por el peso de un gallo (peso_gallo).

5.se calcula el peso total de los pollitos multiplicando la cantidad de pollitos (K) por el peso de un pollito (peso_pollito).

6.A continuación, se suma el peso total de las gallinas, gallos y pollitos para obtener el peso total de carne de aves en kilogramos y se almacena en la variable peso_total_carne.

7.Finalmente, la función retorna el valor de peso_total_carne.Fuera de la función, el programa solicita al usuario que ingrese la cantidad de gallinas, gallos y pollitos mediante  la función input(). Los valores ingresados por el usuario se convierten en enteros utilizando la función int() y se almacenan en las variables N, M y K.

8.Luego, se llama a la función calcular_cantidad_carne con los valores ingresados por el usuario (N, M y K) como argumentos, y el resultado se almacena en la variable total_carne.
Finalmente, se muestra en pantalla el resultado utilizando una cadena formateada (f-string) que incluye el valor de total_carne, informando al usuario de la cantidad total de 
carne de aves en kilogramos.
## PUNTO 4
```python
def Calcular_Vueltas(P,M,H,Precio_Panes,Precio_Bolsas,Precio_Huevos,Valor_Del_Billete):

    #Precio de productos de canasta familiar que pidió la mamá
    Precio_Panes = 300
    Precio_Bolsas = 3300
    Precio_Huevos = 350 

    #Calcular el costo total de los productos
    Precio_total = (P * Precio_Panes) + (M * Precio_Bolsas) + (H * Precio_Huevos)

    #Calcular las vueltas
    vueltas = Valor_Del_Billete - Precio_total

    return vueltas 

#Solicitar al usuario que ingrese la cantidad de productos(Función principal) 
P = int(input('ingrese la cantidad de panes')) 
M = int(input('ingrese la cantidad de bolsas'))
H = int(input('ingrese la cantidad de huevos'))
Valor_Del_Billete = float(input('ingrese el valor del billete en pesos'))

# Precios de los productos
precio_panes = 300
precio_leche = 3300
precio_huevos = 350

# Calcular las vueltas o lo que se debe
vueltas = Calcular_Vueltas(P, M, H, precio_panes, precio_leche, precio_huevos, Valor_Del_Billete)

# Mostrar el resultado
if vueltas >= 0:
    print(f"Las vueltas son: {vueltas} pesos.")
else:
    print(f"Debes: {abs(vueltas)} pesos.")
```
1.Se define una función llamada Calcular_Vueltas que toma siete parámetros: P, M, H, Precio_Panes, Precio_Bolsas, Precio_Huevos y Valor_Del_Billete. Estos parámetros representan la cantidad de panes, bolsas y huevos comprados, así como los precios de estos productos y el valor del billete que el cliente proporciona.

2.Dentro de la función, se calcula el costo total de los productos multiplicando la cantidad de cada producto por su precio correspondiente y sumándolos en la variable Precio_total.Luego, se calcula la cantidad de vueltas restando el Valor_Del_Billete al Precio_total, y ese valor se almacena en la variable vueltas.
La función retorna el valor de vueltas.

3.Fuera de la función, el programa solicita al usuario que ingrese la cantidad de panes, bolsas y huevos comprados, así como el valor del billete que proporciona.

4.Se define nuevamente el precio de los productos (precio_panes, precio_leche, precio_huevos) aunque ya se habían definido anteriormente, pero estos valores no se utilizan en el cálculo principal.

5.Luego, se llama a la función Calcular_Vueltas con los valores ingresados por el usuario (P, M, H, precio_panes, precio_leche, precio_huevos, Valor_Del_Billete) como argumentos, y el resultado se almacena en la variable vueltas.

6.Se verifica si el valor de vueltas es mayor o igual a cero. Si es mayor o igual a cero, se muestra en pantalla un mensaje que indica las vueltas que se deben entregar al cliente. Si es negativo, se muestra un mensaje que indica la cantidad que el cliente debe adicionalmente.

## PUNTO 5 
```python
def Calcular_Valor_Prestamo(P, I, N, Meses):
    #Convertir tasa de interés anual a tasa de interés mensual 
    I_Mensual = I / 12 / 100 

    #Calcular el valor total del préstamo con interés compuesto 
    C = P * (1 + I_Mensual / N)**(N * Meses)
    return C

# Solicitar al usuario ingresar los datos del préstamo
P = float(input("Ingresa la cantidad principal (Prestada): "))
I = float(input("Ingresa la tasa de interés anual (en porcentaje): "))
N = int(input("Ingresa el número de veces que se compone el interés por año: "))
Meses = int(input("Ingresa el número de meses para el préstamo: "))

# Calcular el valor total del préstamo con interés compuesto
valor_prestamo = Calcular_Valor_Prestamo(P, I, N, Meses)

# Mostrar el resultado
print(f"El valor total del préstamo con interés compuesto es: {valor_prestamo:.2f}")
```
1.Se define una función llamada Calcular_Valor_Prestamo que toma cuatro parámetros: P (cantidad principal prestada), I (tasa de interés anual en porcentaje), N (número de veces que se compone el interés por año) y Meses (número de meses para el préstamo).

2.Dentro de la función, se convierte la tasa de interés anual (I) en una tasa de interés mensual (I_Mensual) dividiendo I entre 12 (número de meses en un año) y luego dividiendo nuevamente por 100 para obtener el valor en decimales.
3.La función retorna el valor calculado de C.

4.Fuera de la función, el programa solicita al usuario ingresar los datos del préstamo:

P: La cantidad principal prestada (monto del préstamo).
I: La tasa de interés anual en porcentaje.
N: El número de veces que se compone el interés por año.
Meses: El número de meses para el préstamo.
Se calcula el valor total del préstamo con interés compuesto llamando a la función Calcular_Valor_Prestamo con los valores ingresados por el usuario (P, I, N, Meses).

5.Finalmente, se muestra el resultado en pantalla utilizando una cadena formateada (f-string) que incluye el valor calculado de valor_prestamo con dos decimales, indicando el valor total del préstamo con interés compuesto.

## PUNTO 6
```python
def Calcular_Contagiados_Nuncalandia(C, D):
    Total_Contagiados = C * (2 ** D)
    return Total_Contagiados

# Solicitar al usuario ingresar el número actual de contagiados y los días a futuro
C = int(input("Ingresa el número actual de contagiados: "))
D = int(input("Ingresa el número de días a partir de hoy: "))

# Calcular el número total de contagiados después de D días
total_contagiados = Calcular_Contagiados_Nuncalandia(C, D)

# Mostrar el resultado
print(f"Después de {D} días, el número total de contagiados será: {total_contagiados}")
```
1.Se define una función llamada Calcular_Contagiados_Nuncalandia que toma dos parámetros: C (el número actual de contagiados) y D (el número de días a futuro). Esta función utiliza una fórmula para calcular el número total de contagiados después de D días.

2.Dentro de la función, se calcula el Total_Contagiados multiplicando el número actual de contagiados (C) por 2 elevado a la potencia D (2^D). Esto implica un crecimiento exponencial en el número de contagiados en "Nuncalandia".La función retorna el valor calculado de Total_Contagiados.

5.Fuera de la función, el programa solicita al usuario ingresar dos valores:

C: El número actual de contagiados en "Nuncalandia".
D: El número de días a partir de hoy para calcular el número total de contagiados.
Se calcula el número total de contagiados después de D días llamando a la función Calcular_Contagiados_Nuncalandia con los valores ingresados por el usuario (C y D).

6.Finalmente, se muestra el resultado en pantalla utilizando una cadena formateada (f-string) que incluye el valor calculado de total_contagiados, indicando cuántos contagiados habrá después de D días en "Nuncalandia".

## PUNTO 7 
```python
from operaciones import *

# Solicitar al usuario ingresar 5 números reales
numeros = []
for i in range(5):
    numero = float(input(f"Ingresa el número {i+1}: "))
    numeros.append(numero)

# Calcular y mostrar los resultados utilizando las funciones del archivo "operaciones.py"
print(f"Promedio: {calcular_promedio(numeros)}")
print(f"Mediana: {calcular_mediana(numeros)}")
print(f"Promedio Multiplicativo: {calcular_promedio_multiplicativo(numeros)}")
print(f"Números Ordenados Ascendentemente: {ordenar_ascendente(numeros)}")
print(f"Números Ordenados Descendentemente: {ordenar_descendente(numeros)}")
print(f"Potencia del Mayor Elevado al Menor: {calcular_potencia_menor_al_mayor(numeros)}")
print(f"Raíz Cúbica del Menor Número: {calcular_raiz_cubica_menor(numeros)}")
```
1.En la primera línea del programa, se importan todas las funciones definidas en el archivo "operaciones.py" utilizando la sintaxis from operaciones import *. Esto significa que todas las funciones definidas en "operaciones.py" estarán disponibles para su uso en este programa.

2.Luego, el programa solicita al usuario ingresar 5 números reales. Utiliza un bucle for que se ejecuta 5 veces para obtener estos números. Cada número ingresado se convierte en un valor de punto flotante (float) y se agrega a la lista numeros.

3.A continuación, el programa utiliza las funciones importadas desde "operaciones.py" para realizar varios cálculos utilizando la lista de números ingresados:

4.Se calcula el promedio de los números utilizando la función calcular_promedio(numeros) y se muestra en pantalla.

5.Se calcula la mediana de los números utilizando la función calcular_mediana(numeros) y se muestra en pantalla.

6.Se calcula el promedio multiplicativo de los números utilizando la función calcular_promedio_multiplicativo(numeros) y se muestra en pantalla.

7.Se ordenan los números en orden ascendente utilizando la función ordenar_ascendente(numeros) y se muestran en pantalla.

8.Se ordenan los números en orden descendente utilizando la función ordenar_descendente(numeros) y se muestran en pantalla.

9.Se calcula la potencia del número mayor elevado al número menor utilizando la función calcular_potencia_menor_al_mayor(numeros) y se muestra en pantalla.

10.Se calcula la raíz cúbica del número menor utilizando la función calcular_raiz_cubica_menor(numeros) y se muestra en pantalla.

## PUNTO 8
```python
import math

def calcular_promedio(numeros):
    return sum(numeros) / len(numeros)

def calcular_mediana(numeros):
    numeros_ordenados = sorted(numeros)
    n = len(numeros_ordenados)
    
    if n % 2 == 0:
        medio_izquierdo = numeros_ordenados[n // 2 - 1]
        medio_derecho = numeros_ordenados[n // 2]
        mediana = (medio_izquierdo + medio_derecho) / 2
    else:
        mediana = numeros_ordenados[n // 2]
    
    return mediana

def calcular_promedio_multiplicativo(numeros):
    producto = 1
    for num in numeros:
        producto *= num
    return producto ** (1 / len(numeros))

def ordenar_ascendente(numeros):
    return sorted(numeros)

def ordenar_descendente(numeros):
    return sorted(numeros, reverse=True)

def calcular_potencia_menor_al_mayor(numeros):
    menor = min(numeros)
    mayor = max(numeros)
    return mayor ** menor

def calcular_raiz_cubica_menor(numeros):
    menor = min(numeros)
    return math.pow(menor, 1/3)
```
1.En la primera línea del programa, se importan todas las funciones definidas en el archivo "operaciones.py" utilizando la sintaxis from operaciones import *. Esto significa que todas las funciones definidas en "operaciones.py" estarán disponibles para su uso en este programa.

2.Luego, el programa solicita al usuario ingresar 5 números reales. Utiliza un bucle for que se ejecuta 5 veces para obtener estos números. Cada número ingresado se convierte en un valor de punto flotante (float) y se agrega a la lista numeros.

3.A continuación, el programa utiliza las funciones importadas desde "operaciones.py" para realizar varios cálculos utilizando la lista de números ingresados:

4.Se calcula el promedio de los números utilizando la función calcular_promedio(numeros) y se muestra en pantalla.

5.Se calcula la mediana de los números utilizando la función calcular_mediana(numeros) y se muestra en pantalla.

6.Se calcula el promedio multiplicativo de los números utilizando la función calcular_promedio_multiplicativo(numeros) y se muestra en pantalla.

7.Se ordenan los números en orden ascendente utilizando la función ordenar_ascendente(numeros) y se muestran en pantalla.

8.Se ordenan los números en orden descendente utilizando la función ordenar_descendente(numeros) y se muestran en pantalla.

9.Se calcula la potencia del número mayor elevado al número menor utilizando la función calcular_potencia_menor_al_mayor(numeros) y se muestra en pantalla.

Se calcula la raíz cúbica del número menor utilizando la función calcular_raiz_cubica_menor(numeros) y se muestra en pantalla.

#  PUNTO #9
#  Consultar qué es y cómo funciona pip en python:
PIP en Python es como una tienda de aplicaciones para tu código, donde se puede:

-Descarga de Paquetes: PIP te permite buscar y descargar paquetes de Python desde Internet, como descargar aplicaciones en tu teléfono.

-Instalación de Paquetes: Después de descargar un paquete, PIP lo coloca en tu computadora para que puedas usarlo en tu código. Es como instalar una aplicación en tu teléfono.

-Actualización de Paquetes: PIP también puede actualizar tus paquetes para asegurarte de que tengas las últimas versiones.

-Eliminar Paquetes: Si ya no necesitas un paquete, PIP te ayuda a eliminarlo de tu computadora, como desinstalar una aplicación en tu teléfono.

# PUNTO 10
#   Recuerdar que se debe ejecutar estos comandos en la terminal de acuerdo con el módulo específico que deseas instalar.
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
