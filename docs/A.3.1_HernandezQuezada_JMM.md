# :trophy: A.3.1 Actividad de aprendizaje

Circuito sensor de detección de objetos, utilizando un Arduino, un sensor ultrasonico y un Display I2C LCD 16x2.
___

## Instrucciones

* Realizar un sistema simulado, capaz de detectar la presencia y/o ausencia de un objeto, a través de un circuito electrónico, utilizando un Arduino, y un **Sensor Ultrasonico HC-SR04**.
* Toda actividad o reto se deberá realizar utilizando el estilo **MarkDown con extension .md** y el entorno de desarrollo VSCode, debiendo ser elaborado como un documento **single page**, es decir si el documento cuanta con imágenes, enlaces o cualquier documento externo debe ser accedido desde etiquetas y enlaces, y debe ser nombrado con la nomenclatura **A3.1_NombreApellido_Equipo.pdf.**
* Es requisito que el .md contenga una etiqueta del enlace al repositorio de su documento en GITHUB, por ejemplo **Enlace a mi GitHub** y al concluir el reto se deberá subir a github.
* Desde el archivo **.md** exporte un archivo **.pdf** que deberá subirse a classroom dentro de su apartado correspondiente, sirviendo como evidencia de su entrega, ya que siendo la plataforma **oficial** aquí se recibirá la calificación de su actividad.
* Considerando que el archivo .PDF, el cual fue obtenido desde archivo .MD, ambos deben ser idénticos.
* Su repositorio ademas de que debe contar con un archivo **readme**.md dentro de su directorio raíz, con la información como datos del estudiante, equipo de trabajo, materia, carrera, datos del asesor, e incluso logotipo o imágenes, debe tener un apartado de contenidos o indice, los cuales realmente son ligas o **enlaces a sus documentos .md**, _evite utilizar texto_ para indicar enlaces internos o externo.
* Se propone una estructura tal como esta indicada abajo, sin embargo puede utilizarse cualquier otra que le apoye para organizar su repositorio.
  
```
* readme.md
  - blog
    - C3.1_TituloActividad.md
    - C3.2_TituloActividad.md
    - C3.3_TituloActividad.md
    - C3.4_TituloActividad.md
    - C3.5_TituloActividad.md
    - C3.6_TituloActividad.md
    - C3.7_TituloActividad.md
    - C3.8_TituloActividad.md
  - img
  - docs
    - A3.1_TituloActividad.md
    - A3.2_TituloActividad.md
    - A3.3_TituloActividad.md
```
___

## Desarrollo

1. Utilizar el siguiente listado de materiales para la elaboración de la actividad

| Cantidad | Descripción                                                                                                                                                                                                                        |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1        | [Sensor Ultrasonico HC-SR04](https://www.amazon.com.mx/SainSmart-HC-SR04-Ranging-Detector-Distance/dp/B004U8TOE6/ref=sr_1_5?__mk_es_MX=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=hc-sr04&qid=1599005012&sr=8-5)            |
| 1         | [Display LCD de 16x2](https://www.steren.com.mx/display-lcd-2x16.html)
| 1        | [Fuente de voltaje de 5V](https://www.yescomusa.com/products/30v-precision-variable-voltage-power-supply-dc-converter)  |
| 1        | [1 Potenciómetro 10k ](https://www.amazon.com.mx/Uxcell-a15011600ux0235-Linear-Rotary-Potentiometer/dp/B01DKCUVMQ/ref=sr_1_1?__mk_es_MX=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=potenciometro+10k&qid=1599005041&sr=8-1) |
| 1        | [Arduino UNO](https://www.amazon.com.mx/Progressive-Automations-LC-066-Arduino-Rev3/dp/B00WH5XOJK/ref=sr_1_7?__mk_es_MX=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=arduino+uno&qid=1599005073&sr=8-7)                       |

2. Basado en la imágen que se muestra, ensamble dentro del simulador a utilizar, el circuito electrónico indicado en la **Figura 1**.

<p align="center"> 
    <strong>Figura 1 Sensor Ultrasonico</strong>
    <img alt="Logo" src="../img/C3.x_ArduinoEsquematicoSensorUltrasonico.png"
    width=550 height=350>
</p>


3. Realice el programa que permita a través de una de las entradas del Arduino, recibir el valor que registra el **Sensor Ultrasonico** al acercarse un objeto a distintas distancias.

<p align="center"> 
    <img alt="Logo" src="../img/A3.1_Codigo.png"
    width= height=>
</p>

4. Considerando que el sensor ultrasonico tiene un rango mínimo y máximo de detección basado en el tiempo de retorno de la señal sonica, que valores se obtienen en la simulación bajo las **siguientes condiciones:**

| Numero | Condición 1                   | Condición2                                 | El objeto es detectado? |
| ------ | ----------------------------- | ------------------------------------------ | ----------------------- |
| 1      | 5 cm de distancia al sensor   | 0 grados al eje perpendicular del sensor   | Si es Detectado
| 2      | 50 cm de distancia al sensor  | 35 grados al eje perpendicular del sensor  | No es Detectado
| 3      | 100 cm de distancia al sensor | -35 grados al eje perpendicular del sensor | No es Detectado
| 4      | 5 cm de distancia al sensor   | 90 grados al eje perpendicular del sensor  | No es Detectado
| 5      | 50 cm de distancia al sensor  | -60 grados al eje perpendicular del sensor | No es Detectado
| 6      | 350 cm de distancia al sensor | 0 grados al eje perpendicular del sensor   | No es Detectado

5. Una vez completados los puntos anteriores, agregue a la Figura 1, **un Display I2C 16x2 LCD**, y coloque la imagen del circuito completado hasta este apartado.

<p align="center"> 
    <img alt="Logo" src="../img/A3.1_Circuito.png"
    width= height=>
</p>


6. Al haber completado la integración del Display I2C, ajuste el programa que le permita a través del display mostrar el siguiente mensaje, **"Objetivo detectado a ? cm** , y en caso de no lograr la detección indicar el mensaje **"Objetivo fuera de rango"**
<p align="center"> 
    <img alt="Logo" src="../img/A3.1_Codigo2.png"
    width= height=>
</p>

<p align="center"> 
    <img alt="Logo" src="../img/A3.1_Circuito1.png"
    width= height=>
</p>

<p align="center"> 
    <img alt="Logo" src="../img/A3.1_Circuito2.png"
    width= height=>
</p>

7. Coloque aqui evidencias que considere importantes durante el desarrollo de la actividad.
<p align="center"> 
    <img alt="Logo" src="../img/Evidencias/3.1_E1.png"
    width= height=>
</p>

<p align="center"> 
    <img alt="Logo" src="../img/Evidencias/3.1_E2.png"
    width= height=>
</p>

<p align="center"> 
    <img alt="Logo" src="../img/Evidencias/3.1_E3.png"
    width= height=>
</p>

8.  Incluya las **conclusiones** individuales y resultados observados durante el desarrollo de la actividad.

- **Hernández Quezada Martín**

Esta actividad nos dio a conocer como trabajan y funcionan los sensores de ultrasónicos de proximidad, específicamente el HC-SR04 de 3 pines, donde gracias a la simulación se pudo ver de una manera mas amplia como trabaja dicho sensor y como al colocar objetos muy cerca no los detecta, al igual que si se ponen objetos a mas de 335cm, en la actividad colocamos nuestro código en arduino, ampliando así nuestro conocimiento en dicho programa para poder implementar la función de este y así poder completar con éxito la actividad.

- **Navarro Rosas Martín Ivan**

En conclusión podemos decir que los sensores ultrasónicos son detectores de proximidad que trabajan libres de roces mecánicos, estos pueden ser de gran ayuda a la hora de crear robots que caminen por si solos para que no colisiones con algún objeto que se encuentre sobre su camino, en cuanto al microcontrolador arduino se pudo desarrollar un programa que pudiera mostrar a que distancia se encuentra el objeto que se quiere detectar, asi como mediante una pantalla LCD mostrar los datos y esto puede ser de gran ayuda para futuras practicas que se deseen realizar.

- **Sandoval Gorgonio Juan Pablo** 

En esta práctica aprendí sobre el funcionamiento de los sensores ultrasónicos los cuales trabajan como detectores de proximidad, que se usan en maquinas utilizadas en fábricas, autos inteligentes, incluso en nuestros celulares. En la actividad se requiere detectar la distancia que se encuentra el objeto y mostrarlo en una pantalla.
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
