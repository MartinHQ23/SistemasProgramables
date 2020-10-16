# Sensores

## :trophy: A.1.4 Actividad de aprendizaje

## Objetivo

Realizar un sensor medidor de temperatura a través de un circuito electrónico, utilizando un simulador, y  un **Transistor TMP36** lineal de temperatura y un **amplificador operacional LM741**.

## :blue_book: Instrucciones

- Se sugiere para el desarrollado de la presenta actividad, utilice uno de los siguientes simuladores: [Autodesk Tinkercad](https://www.tinkercad.com/), [Virtual BreadBoard](http://www.virtualbreadboard.com/), [Easy EDA](https://easyeda.com/) por lo cual habrá que familiarizarse antes, e incluso instalarse o registrarse dentro de la plataforma.
- Toda actividad o reto se deberá realizar utilizando el estilo **MarkDown con extension .md** y el entorno de desarrollo VSCode, debiendo ser elaborado como un documento **single page**, es decir si el documento cuanta con imágenes, enlaces o cualquier documento externo debe ser accedido desde etiquetas y enlaces, y debe ser nombrado con la nomenclatura **A1.4_NombreApellido_Equipo.pdf.**
- Es requisito que el .md contenga una etiqueta del enlace al repositorio de su documento en GITHUB, por ejemplo **Enlace a mi GitHub** y al concluir el reto se deberá subir a github.
- Desde el archivo **.md** exporte un archivo **.pdf** que deberá subirse a classroom dentro de su apartado correspondiente, sirviendo como evidencia de su entrega, ya que siendo la plataforma **oficial** aquí se recibirá la calificación de su actividad.
- Considerando que el archivo .PDF, el cual fue obtenido desde archivo .MD, ambos deben ser idénticos.
- Su repositorio ademas de que debe contar con un archivo **readme**.md dentro de su directorio raíz, con la información como datos del estudiante, equipo de trabajo, materia, carrera, datos del asesor, e incluso logotipo o imágenes, debe tener un apartado de contenidos o indice, los cuales realmente son ligas o **enlaces a sus documentos .md**, _evite utilizar texto_ para indicar enlaces internos o externo.
- Se propone una estructura tal como esta indicada abajo, sin embargo puede utilizarse cualquier otra que le apoye para organizar su repositorio.
  
```
- readme.md
  - blog
    - C0.1_x.md
    - C0.2_x.md
  - img
  - docs
    - A0.1_x.md
    - A0.2_x.md
    - A1.2_x.md
    - A1.3_x.md
```

## :pencil2: Desarrollo

1. Utilice el siguiente listado de materiales para la elaboración de la actividad

    | Cantidad | Descripción                       | Fuente de consulta |
    | -------- | --------------------------------- | ------------------ |
    | 1        | Sensor temperatura TMP36          |      [**ElectroCrea**](https://electrocrea.com/products/sensor-de-temperatura-tmp36)              |
    | 1        | Potenciómetro 10k                 |       [**ElectroCrea**](https://electrocrea.com/products/potenciometro-lineal-de-carbon?_pos=1&_sid=de719769e&_ss=r)              |
    | 2        | Resistencias de 220               |    [**Geekbot Electronics**](http://www.geekbotelectronics.com/producto/resistencia-220-ohm-14-w/)                 |
    | 1        | Amplificador LM741                |   [**Carrrod Electronica**](https://www.carrod.mx/products/lm741-amplificador-operacional)                 |
    | 1        | Fuente de alimentación de 5Volts. |      [**YescomUSA**](https://www.yescomusa.com/products/30v-precision-variable-voltage-power-supply-dc-converter)              |

    Para mayor información acceder a los siguientes enlaces:

    - Información y especificaciones del [Sensor TMP36](https://components101.com/sites/default/files/component_pin/TMP36-Sensor-Pinout.png)  
    - Información y especificaciones del [Amplificador operacional LM741](https://ortegamraul.files.wordpress.com/2014/03/741-interno.png)

2. Basado en la imagen ensamble mediante un simulador el circuito electrónico etapa 1, colocando el transistor LM35 en la posición indicada. 

<p align="center">
    <img alt="Logo" src="../img/C1.x_CircuitoLM35_Etapa1.png" width=250 height=250>
</p>

<p align="center">
    <img alt="Logo" src="../img/C1.4_.png" width=400 height=300>
</p>

3. Calcule, mida y registre los valores solicitados para Vout1, bajos las 3 condiciones requeridas en la tabla anexa.

| Numero | Condición | Voltaje Vout1 medido | Voltaje en R1 medido | Temperatura indicada |
| ------ | --------- | -------------------- | -------------------- | -------------------- |
| 1      | Mínima    |       **99.9mV**           |      **11mV**                |      **-40 °C**                |
| 2      | Media     |     **749mV**              |          **11mV**            |        **25 °C**              |
| 3      | Máxima    | **1.75 V**                 |        **11mV**              |             **125 °C**         |

4. Utilizando la imagen del transistor TMP36 que corresponde a la etapa 1, conecte la terminal Vout1 a la terminal no inversora del LM741, y ensamble el circuito correspondiente a la etapa 2.

<p align="center">
    <img alt="Logo" src="../img/C1.x_CircuitoLM741_Etapa2.png") width=400 height=300>

</p>

<p align="center">
    <img alt="Logo" src="../img/C1.4-2.png") width=400 height=300>
</p>


5. **Que valor deberá tener R3 en el circuito Etapa 2, para lograr obtener Vout2 = 5 volts,** para la condición máxima de temperatura que el sensor es capaz de detectar? Como se puede observar la resistencia R3 corresponde a un potenciómetro, sin embargo se pueden hacer arreglos de resistencias para lograr un ajuste fino.  Cual cree que sea la razón por la cual se esta solicitando un **ajuste a 5 Volts**?

**RESPUESTA** :white_check_mark:
 ```
 Vout = vin * (1+(R2/R1))
 Vout = 5V
 Vin = 1.75
 R2 = 220 ohms

 Despeje
 ((5/ 1.75)-1) * 220 ohms = 408.57
 R2 = 408.57 ohms
 ```
Cual cree que sea la razón por la cual se esta solicitando un **ajuste a 5 Volts**?
 ```
 Al ser la fuente de 5 voltios, esta es su maxima capacidad por lo que se amplia el rango para utilizar en comparacion al original de 1.75V, ademas de tener una mayor resolucion en el momento que se desea leer los valores.
  ```

6. Una vez que se ha ajustado el valor R3 dejalo asi y registre los valores solicitados para Vout2, para las 3 condiciones requeridas en la tabla anexa.

| Numero | Condición        | Voltaje en R2 medido | Voltaje en Vout2 medido | Temperatura indicada |
| ------ | ---------------- | -------------------- | ----------------------- | -------------------- |
| 1      | Condición mínima |             **99.9mV**         |    **286mV**                     |   **-40 °C**                   |
| 2      | Condición media  |       **949mV**               |   **2.71mV**                      |       **44 °C**               |
| 3      | Condición máxima |       **1.74V**               |    **4.53mV**                     |         **125 °C**             | 

7. Grafique Vout1 y Vout2, para las tres condiciones anteriores, considerando en "X" los valores de temperatura y para "Y" los valores de voltaje, y coloque dentro de este apartado.

<p align="center">
    <img alt="Logo" src="../img/1.4_graf.png") width= height=>
</p>

8. Inserte imágenes de evidencias tales como son reuniones de los integrantes del equipo realizadas para
el desarrollo de la actividad

<p align="center">
    <img alt="Logo" src="../img/Evidencias/1.4_E1.png") width= height=>
</p>

<p align="center">
    <img alt="Logo" src="../img/Evidencias/1.4_E2.png") width= height=>
</p>  

<p align="center">
    <img alt="Logo" src="../img/Evidencias/1.4_E3.png") width= height=>
</p>
<p align="center">
    <img alt="Logo" src="../img/Evidencias/1.4_E4.png") width= height=>
</p>

9. Incluya las **conclusiones** individuales y resultados observados durante el desarrollo de la actividad.
    
 **-Hernández Quezada Martín :** 
```
El sensor de temperatura TMP36 me parece una herramienta útil al momento de necesitar conocer valores en las temperaturas, por su parte el amplificador que a pesar de nunca haberlo utilizado antes y desconocer su funcionamiento, me permitió darme cuenta de el alto rango de capacidad que puedo aumentar gracias a este, tal vez en un futuro vaya a necesitar el uso de ambos y gracias a esta practica, los podre utilizar de la manera esperada.
```
 **-Navarro Rosas Martin Ivan :**
```
El comportamiento del sensor de temperatura tmp36 como pudimos apreciar nos puede ser muy util a la hora de realizar practicas que requieran de un control de temperatura, asi como un invernadero o ya sea para un gestiones termicas de algun producto electronico, asi como el uso de amplificadores operacionales para aumentan la salida de voltaje de estos mismos.
```
 **-Sandoval Gorgonio Juan Pablo :**
```
En esta practica se observa el comportamiento del sensor TMP36, pudimos observar que el voltaje que consume es proporcional a la temperatura registrada.
Y que es una buena opción si se desea obtener temperaturas ya que es muy preciso y facil de usar.
```
___

### :bomb: Rubrica

| Criterios     | Descripción                                                                                  | Puntaje |
| ------------- | -------------------------------------------------------------------------------------------- | ------- |
| Instrucciones | Se cumple con cada uno de los puntos indicados dentro del apartado Instrucciones?            | 10      |
| Desarrollo    | Se respondió a cada uno de los puntos solicitados dentro del desarrollo de la actividad?     | 60      |
| Demostración  | El alumno se presenta durante la explicación de la funcionalidad de la actividad?            | 20      |
| Conclusiones  | Se incluye una opinión personal de la actividad  por cada uno de los integrantes del equipo? | 10      |

**Repositorios**

:house: [**Repositorio - HERNANDEZ QUEZADA MARTIN**](https://github.com/MartinHQ23/SistemasProgramables)

:house: [**Repositorio - NAVARRO ROSAS MARTIN IVAN**](https://github.com/MartinNavarro17/REPOSITORIO-SISTEMAS-PROGRAMABLES)

:house: [**Repositorio - SANDOVAL GORGONIO JUAN PABLO**](https://github.com/JuanPSG/SistemasProgramables)
