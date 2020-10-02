# Introducción

## :trophy: A.1.2 Actividad de aprendizaje

## Objetivo

Realizar un sensor medidor de luz (lux) a través de un circuito electrónico, utilizando un simulador, y  un **LDR (Light dependent Resistor)**.

### :blue_book: Instrucciones

- Se sugiere para el desarrollado de la presenta actividad, utilice uno de los siguientes simuladores: [Autodesk Tinkercad](https://www.tinkercad.com/), [Virtual BreadBoard](http://www.virtualbreadboard.com/), [Easy EDA](https://easyeda.com/) por lo cual habrá que familiarizarse antes, e incluso instalarse o registrarse dentro de la plataforma.
- Toda actividad o reto se deberá realizar, utilizando el estilo **MarkDown con extension .md** y el entorno de desarrollo VSCode, debiendo ser elaborado como un documento **single page**, es decir si el documento cuanta con imágenes, enlaces o cualquier documento externo debe ser accedido desde etiquetas y enlaces, y debe ser nombrado con la nomenclatura **A1.2_NombreApellido_Equipo.pdf.**
- Es requisito que el .MD contenga una etiqueta del enlace al repositorio de su documento en GITHUB, por ejemplo **Enlace a mi GitHub** y al concluir el reto se deberá subir a github.
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


### :pencil2: Desarrollo

1. Utilice el siguiente listado de materiales para la elaboración de la actividad y agregue en la columna Fuente de consulta su enlace _bibliográfico_.

    | Cantidad | Descripción                      | Fuente de consulta |
    | -------- | -------------------------------- | ------------------ |
    | 1        | Sensor Fotoresistencia LDR de 2M |          [**Prometec**](https://prometec.mx/producto/ldr-sensor-de-luz/)          |
    | 1        | Resistencia 1k                   |         [**Tostranic**](https://tostatronic.com/store/es/componentes-pasivos/887-resistencia-1k-ohms-14w.html)           |
    | 1        | Fuente de alimentación de 5v.    |          [**YescomUSA**](https://www.yescomusa.com/products/30v-precision-variable-voltage-power-supply-dc-converter)          |

2. Considerando que el elemento LDR es un sensor fotoresistivo es decir varia su resistencia en base a la cantidad de luz que incide sobre el, **Que observa en el grafico siguiente?** 
   
<p align="center">
    <img alt="Logo" src="../img/C1.x_Sensor_FotoresistenciaLDR.png" width=600 height=300>
</p>

**RESPUESTA** :white_check_mark: 
 ```
Pudimos observar que las resistencias varían su valor en función dependiendo de la luz que estas reciben, como se puede ver en el gráfico, mientras mas oscuridad haya en el ambiente estas presentaran una resistencia muy alta, disminuyendo a medida que incrementamos la luz ambiental.
  ```
3. Ensamble el circuito que se muestra utilizado el simulador que halla considerado, colocando la fotorresistencia en la posición LDR y resistencia de acuerdo con la imagen del esquemático:

    <p align="center"> 
        <img alt="Logo" src="../img/C1.x_CircuitoSensorFotoresistivo.png" width=300 height=400>
    </p>
4. coloque la imagen finalmente obtenida del circuito ensamblado dentro de su simulador.
<p align="center"> 
        <img alt="Logo" src="../img/Circuito_JMM.png" width=600 height=250>
    </p>

 :triangular_flag_on_post: [**Circuito**](https://www.tinkercad.com/things/1RyyKQroxP4-fantastic-wolt/editel?sharecode=a88lhImA07olOdHAHvHAqd5zVrPjvTXvJsbPsjEvN_k&fbclid=IwAR1hQEEy_ABRN7-9rLbJR7Eos8RpJeTo7NoYPCGMCXhLjXg7FcRCg-k2r_I)

5. Mida la **resistencia** de la fotorresistencia con el ohmetro bajo las siguientes condiciones: ausencia de luz u oscuridad,  luz ambiente, luz intensiva y registre en la tabla correspondiente.
6. Calcule el **valor de voltaje Vout teórico** para cada una de las condiciones antes indicadas asi como el valor de voltaje Vout medido  y registre en la tabla correspondiente.
7. Calcule el **valor de exactitud** de voltaje entre lo teórico y lo medido para cada condición  y registre en la tabla correspondiente.

    | Condicion          |  Impedancia en fotoresistencia | Voltaje Vout teórico | Voltaje Vout medido | %  V.Medido/ V.Teórico |
    | --------------- | ----------------------------- | -------------------- | ------------------- | ---------------------- |
    | Ausencia de luz |**180 kohms** | **0.027V** | **0.0277V** | **100 %** |
    | Luz ambiental   |**979ohms** | **2.526V** | **2.52V** | **99.76 %** |
    | Luz intensa     |**506omhs** | **3.320V** | **3.32V** | **100 %** |

### **Desarollo**
**AUSENCIA DE LUZ** :white_check_mark:
 ```
 Vout = Vin * R2 / R1+R2
 Vout = 5 * 1000 / 180000 + 1000 
 Vout = 0.027V

 Porcentaje = V.Medido / V. Teórico * 100
 Porcentaje = 0.0277V / 0.027V = 1 *(100)
 Porcentaje = 100%
 
  ```
**LUZ AMBIENTAL** :white_check_mark:
 ```
 Vout = Vin * R2 / R1+R2
 Vout = 5 * 1000 / 979 + 1000 
 Vout = 2.526V

 Porcentaje = V.Medido / V. Teórico * 100
 Porcentaje = 2.52V / 2.526V = 0.9976 *(100)
 Porcentaje = 99.76%
 
  ```

  **LUZ INTENSA** :white_check_mark:
 ```
 Vout = Vin * R2 / R1+R2
 Vout = 5 * 1000 / 506 + 1000 
 Vout = 3.320V

 Porcentaje = V.Medido / V. Teórico * 100
 Porcentaje = 3.32V / 3.320V = 1 *(100)
 Porcentaje = 100%
 
  ```
8. **Grafique** a través de los valores registrados en la tabla anterior de tal manera que se pueda observar el comportamiento de la curva del componente LDR e **inserte la grafica**.

 <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/Grafica.png">
    </p>


9.  Inserte imágenes de **evidencias** tales como son reuniones  de los integrantes del equipo realizadas para el desarrollo de la actividad

 <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E1.png" width=400 height=350>
    </p>
 <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E2.png" width=400 height=400>
    </p>
     <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E3.png" width=400 height=350>
    </p>
     <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E4.png" width=400 height=300>
    </p>
     <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E5.png" width=500 height=200>
    </p>
    <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E6.png" width=500 height=200>
    </p>
    <p align="center"> 
        <img alt="Logo" src="../img/Evidencias/E7.png" width=500 height=200>
    </p>


10. Incluya las conclusiones individuales y resultados observados durante el desarrollo de la actividad.

### **Conclusion**
**HERNANDEZ QUEZADA MARTIN**
 ```
Los sensores LDR son algo que muchas personas desconocemos su funcionamiento, en lo personal jamás había utilizado (por lo menos simulado en Tinkercad) este sensor me resulta realmente interesante el poder ver que entre menos luz haya la resistencia es mucho mayor, pues cualquiera pensaría que esto seria totalmente al revés, una vez que logramos implementarlo, me dio la oportunidad de conocer un poco mas de los sensores, que hasta el momento sigo aprendiendo sobre ellos y espero seguir mejorando en el tema, además claro el haber utilizado la herramienta Tinkercad para realizarlo es una manera muy útil de ejecutar la simulación de estas practicas. 
  ```

**NAVARRO ROSAS MARTIN IVAN**
 ```
Como conclusion podemos decir que los LDR tienen un funcionamiento muy interesante debido a que estos varian su resistencia en funcion de las luces que estos mismos reciben, si estos reciben mas luz su resistencia sera mas alta por lo que el voltaje disminuye y viceversa si este no recibe luz. Se podrian utilizar en diversos circuitos donde se requiera como un tipo sensor de luz practicamente el LDR e implementarlo como lo hicimos en esta practica.
  ```
**SANDOVAL GORGONIO JUAN PABLO**
 ```
Esta practica me pareció interesante al realizar por primera vez una simulación en Tinkercad además de utilizar el sensor LDR, aunque al principio me confundía mucho, al final de la practica y con ayuda del profesor mediante las clases, pude comprender mejor como realizar esta practica para poder entregarla con éxito.
  ```


### :bomb: Rubrica

| Criterios     | Descripción                                                                                  | Puntaje |
| ------------- | -------------------------------------------------------------------------------------------- | ------- |
| Instrucciones | Se cumple con cada uno de los puntos indicados dentro del apartado Instrucciones?            | 10      |  | 5 |
| Desarrollo    | Se respondió a cada uno de los puntos solicitados dentro del desarrollo de la actividad?     | 60      |
| Demostración  | El alumno se presenta durante la explicación de la funcionalidad de la actividad?            | 20      |
| Conclusiones  | Se incluye una opinión personal de la actividad  por cada uno de los integrantes del equipo? | 10      |

**Repositorios**

:house: [**Repositorio - HERNANDEZ QUEZADA MARTIN**](https://github.com/MartinHQ23/SistemasProgramables)

:house: [**Repositorio - NAVARRO ROSAS MARTIN IVAN**](https://github.com/MartinNavarro17/REPOSITORIO-SISTEMAS-PROGRAMABLES)

:house: [**Repositorio - SANDOVAL GORGONIO JUAN PABLO**](https://github.com/JuanPSG/SistemasProgramables)
