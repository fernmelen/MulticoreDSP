![alter text](https://tectijuana.edu.mx/wp-content/uploads/2014/11/Heading-Ing-sistemas-2048x672.png)
### Lenguajes de Interfaz
### Docente: René Solís Reyes
### Proyecto: Multicore DSP
### Semestre: enero - junio 2020

### 17212143  Hector Armando Jaramillo Regino
### 17211505 Alejandro Castillo Licea
### 17212146 Gloria Alejandra Jimenez Mayoral
### 17212183 Alberto Sánchez Barroterán
### 17211539 Melendez Palafox Fernando Esaú
### 17211555 Ramos Cedeño Kevin Enrique
### Tijuana B.C. a 20 de mayo de 2020

----------------------------------------------------------------------------------------------------------------------------------------
# Índice  
Planteamiento del problema  
DSP  
DSP y Microprocesador  
ADC  
Señal Analogica Y Digital  
Digitalización  
Pasos para la Digitalización de una señal digital
    MUESTREO  
    CUANTIZACIÓN  
    CODIFICACIÓN  
Funcionamiento DSP  
Aplicaciones del DSP  
Campos de aplicación del DSP  
Arquitectura  
    Diseño de Arquitectura DSP  
    Entorno DSP  
Mejoras a la arquitectura DSP  
    Mejoras más importantes  
Portafolio de procesamiento integrado  
Programación y Herramientas de Programación  
Conclusión  
Referencias  

----------------------------------------------------------------------------------------------------------------------------------------

# Planteamiento del problema.
Comenzaremos explicando un poco sobre las señales. Las señales tienen una gran importancia, ya que para instalar un sistema de red o realizar la interconexión de los diferentes dispositivos, es necesario entender cómo funcionan, sus tipos, características y sistemas con los que interactúan. Por un lado tenemos el procesamiento de señales analogicas y por el otro,  el procesamiento de señales digitales.

Señal analógica: una señal de este tipo, varía de forma continua en el tiempo. Representan alguna magnitud física.

Señal digital: Las señales digitales son discretas (valores finitos) en el tiempo y en amplitud; esto significa que la señal sólo puede tomar uno de dos valores —0 o 1— en intervalos definidos de tiempo.

Si bien a la hora de trabajar con este tipo de señales, nos pueden mostrar una serie de inconvenientes, como lo son las distorsiones (atenuación, distorsión de retardo y/o ruido) en el momento en que una señal analógica necesite ser procesada. Es por esto que se optó por el procesamiento digital de señales DSP ya que este ofrece la gran ventaja de poder disminuir este tipo de problemas o distorsiones.

Ahora tenemos el multicore qué significa multinúcleo el cual sí vemos su especificación dice que es aquel que combina dos o más microprocesadores independientes en un solo paquete, y que a menudo es un solo circuito integrado. 

Entonces con estas dos partes explicadas podemos ver que un multicore dsp por un lado trabaja combinando núcleos y que también trabaja de manera digital. Ahora se procederá a la explicación de todo lo que conlleva el  multicore dsp, qué es, cómo funciona, aplicaciones, etc. 

----------------------------------------------------------------------------------------------------------------------------------------

# DSP: 
También llamado Procesador Digital de Señales o por sus siglas en inglés digital signal processor es un sistema basado en un procesador o microprocesador que posee un conjunto de instrucciones, un hardware y un software optimizados para aplicaciones que requieran operaciones numéricas a muy alta velocidad. Debido a esto es especialmente útil para el procesado y representación de señales analógicas en tiempo real.
Dicho sistema trabaja en tiempo real en el cual se reciben muestras normalmente provenientes de un conversor analógico/digital (ADC).

La mayoría de los sistemas de audio, video y transmisión de datos digitales usados en la actualidad, requieren algoritmos de una elevada complejidad matemática. La solución que aportan los DSP es que pueden realizar operaciones matemáticas complejas en un solo ciclo de reloj por lo que el procesado (de señales de audio, de video, etc.) es el ideal, en contraposición a lo que aportan los microprocesadores convencionales (cualquiera de los que tienen nuestros PC de casa).

Los elementos básicos que componen un DSP son:
- Conversores en las entradas y salidas
- Memoria de datos, memoria de programa y DMA.
- MACs: multiplicadores y acumuladores.
- ALU: Unidad aritmético-lógica.
- Registros.
- PLL: Bucles enganchados en fase.
- PWM: Módulos de control de ancho de pulso.

----------------------------------------------------------------------------------------------------------------------------------------

# DSP y Microprocesador:
- El DSP es muy rápido para un tipo de operaciones concretas, ya que tiene instrucciones especiales para ellas, y las puede DSPs realizar de forma paralela, su velocidad de procesamiento es más baja que un procesador convencional pero para las operaciones que debe realizar es suficiente.
- Un microprocesador convencional posee una velocidad de procesamiento mucho mayor que un DSP aunque como no tiene instrucciones concretas, ni es específico para un tipo de operaciones es más lento que el DSP para las operaciones específicas para las que se han diseñado éstos.

----------------------------------------------------------------------------------------------------------------------------------------

# ADC: 
La conversión analógica-digital consiste en la transcripción de señales analógicas en señal digital, con el propósito de facilitar su procesamiento y hacer la señal resultante (digital) más inmune al ruido y otras interferencias a las que son más sensibles las señales analógicas.

----------------------------------------------------------------------------------------------------------------------------------------

# Señal Analogica Y Digital:
- Una señal analógica es aquella cuya amplitud (típicamente tensión de una señal que proviene de un transductor y amplificador) puede tomar en principio cualquier valor, esto es, su nivel en cualquier muestra no está limitado a un conjunto finito de niveles predefinidos como es el caso de las señales cuantificadas.es representable por una función matemática continua en la que es variable su amplitud y periodo (representando un dato de información) en función del tiempo. Algunas magnitudes físicas comúnmente portadoras de una señal de este tipo son eléctricas como la intensidad, la tensión y la potencia, pero también pueden ser hidráulicas como la presión y térmicas como la temperatura.

![alter text](https://upload.wikimedia.org/wikipedia/commons/0/09/Se%C3%B1al_Continua.png)

- La señal digital es un tipo de señal en que cada signo que codifica el contenido de la misma puede ser analizado en término de algunas magnitudes que representan valores discretos, en lugar de valores dentro de un cierto rango.

![alter text](https://upload.wikimedia.org/wikipedia/commons/5/53/S_digital.PNG)

----------------------------------------------------------------------------------------------------------------------------------------

# Digitalización:
La digitalización es un proceso mediante el cual, algo real (físico, tangible) es pasado a datos digitales para que pueda ser manejado por una computadora (de naturaleza, a su vez, digital), modelando, modificándolo, y aprovechándose para otros propósitos distintos de su cometido o función originales.
Pasos para la Digitalización de una señal digital:  
1. MUESTREO:
Toda la tecnología digital (audio, video) está basado en la técnica de muestreo (sampling en inglés). En música, cuando una grabadora digital toma una muestra, básicamente toma una fotografía fija de la forma de onda y la convierte en bits, los cuales pueden ser almacenados y procesados. Comparado con la grabación analógica, la cual está basada en registros de voltaje como patrones de magnetización en las partículas de óxido de la cinta magnética. El muestreo digital convierte el voltaje en números (0s y 1s) los cuales pueden ser fácilmente representados y vueltos nuevamente a su forma original.  
![alter text](https://lh3.googleusercontent.com/proxy/49Ay7D7hlostZWoziBAsmLjrzbr-QLsCR9mXxlqsVk-gurlfZU3jbZfm99oHYYltkXtKfLA3r6ukbP1ekFWwshi3wgWFw2yqCZT6PYTr1QdSZVy_q0v0fP6gV1ZyWESxwcY2ZlAF) ![alter text](http://www.asifunciona.com/electronica/af_conv_ad/img_conv_ad/af_000014_12.gif)

2. CUANTIZACIÓN:
Una vez realizado el muestreo, el siguiente paso es la cuantización (quantization) de la señal analógica. Para esta parte del proceso los valores continuos de la sinusoide se convierten en series de valores numéricos decimales discretos correspondientes a los diferentes niveles o variaciones de voltajes que contiene la señal analógica original.
Por tanto, la cuantización representa el componente de muestreo de las variaciones de valores de tensiones o voltajes tomados en diferentes puntos de la onda sinusoidal, que permite medirlos y asignarles sus correspondientes valores en el sistema numérico decimal, antes de convertir esos valores en sistema numérico binario.  
![alter text](http://www.asifunciona.com/electronica/af_conv_ad/img_conv_ad/af_000014_14.gif)

3. CODIFICACIÓN:
Después de realizada la cuantización, los valores de las tomas de voltajes se representan numéricamente por medio de códigos y estándares previamente establecidos. Lo más común es codificar la señal digital en código numérico binario.
La codificación permite asignarle valores numéricos binarios equivalentes a los valores de tensiones o< voltajes que conforman la señal eléctrica analógica original.
En este ejemplo gráfico de codificación, es posible observar cómo se ha obtenido una señal digital y el código binario correspondiente a los niveles de voltaje.  
![alter text](http://www.asifunciona.com/electronica/af_conv_ad/img_conv_ad/af_000014_15.gif) 

|Valores en volt en Sistema Decimal|Conversión a Código Binario|
|----------------------------------|---------------------------|
|               0                	|             000            |
|               1                	|             001            |
|               2                	|             010            |
|               3                	|             011            |
|               4                	|             100            |
|               5                	|             101            |
|               6                	|             110            |
|               7                	|             111            |


----------------------------------------------------------------------------------------------------------------------------------------

# Funcionamiento DSP:
DSP son convolución, correlación, filtrado, transformaciones discretas, etc. todas orientadas al tratamiento digital de señal. La función principal de un DSP es la siguiente, que se puede observar en la figura. 
- La entrada es una señal analógica, ya sea audio, video, cualquier señal recibida por cable, o por otro medio.
- El DSP convierte la señal analógica a digital para su posterior procesado 
- Procesado matemático de la representación de la señal. 
- Se vuelve a convertir la señal obtenida de digital a analógica. 
- Se da a la salida una señal analógica. De esta forma se obtiene un procesamiento en tiempo real de la representación matemática de la señal.
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-06-01%20015237.jpg?raw=true)

----------------------------------------------------------------------------------------------------------------------------------------

# Aplicaciones del DSP:
Algunas de las aplicaciones más habituales de los DSP son el procesamiento de audio digital, la compresión de audio, el procesamiento de imágenes digitales, la compresión de vídeo, el procesamiento de voz, el reconocimiento de voz, las comunicaciones digitales, el radar, el sonar, la sismología y la medicina.
Algunos ejemplos concretos de estas aplicaciones son los teléfonos móviles, los reproductores de audio digital (MP3), los módems ADSL, los sistemas de telefonía de manos libres (con reconocimiento de voz) y los osciloscopios.

**Misión crítica**
- Militar
- Aviónica
- Seguridad Pública

**Imagenes medicas**
- Ultrasonido
- Endoscopia
- MRI / CT Scan
- Modalidades emergentes

**Prueba y automatización**
- Inspección de obleas / LCD
- Nicho de impresión / escaneo
- Video emergente

----------------------------------------------------------------------------------------------------------------------------------------

# Campos de aplicación del DSP:

- Telecomunicaciones: En el campo de las telecomunicaciones, los productos que utilizan frecuentemente microcontroladores son los teléfonos móviles.
- Productos de gran consumo: En los productos de gran consumo se utilizan microcontroladores en muchos electrodomésticos de línea blanca (lavadoras, lavavajillas, microondas, etc.) y de línea marrón (televisores, reproductores de DVD, aparatos de radio, etc.).
- Automoción: En la industria del automóvil se utilizan microcontroladores para controlar buena parte de los sistemas del coche; por ejemplo, para controlar los airbags, o el frenado.
- Informática: En la industria informática hay muchos dispositivos periféricos que integran microcontroladores: ratones, teclados, impresoras, escáneres, discos duros, etc.
- Industria: En el mundo industrial se utilizan en diferentes ámbitos, como la robótica o el control de motores.

----------------------------------------------------------------------------------------------------------------------------------------

# Arquitectura
La arquitectura convencional de DSP, introducida en los años 80, se separan los buses de datos y de memoria y ofrecen las instrucciones de anchura fija, ejecutando una instrucción por ciclo de reloj.
Las instrucciones pueden ser bastante complejas. Una sola instrucción puede incorporar dos movimientos de los datos, una operación del MAC, y dos actualizaciones del puntero. Estas instrucciones complejas hacen que el DSP convencional posea alto grado de densidad de código al realizar operaciones matemáticas repetitivas. Las instrucciones de anchura fija son ineficaces cuando las tareas realizan incrementos simples del contador como parte de un lazo de control.
Debido a su potencia de cómputo, los DSPs convencionales ganaron presencia en aplicaciones para comunicaciones y aplicaciones media. Los dispositivos para comunicaciones, incluyen el módem y procesadores de telefonía, codificación de voz y filtros. Usos en aplicaciones media, incluye audio digital, vídeo, y proyección de imagen.

## Diseño de Arquitectura DSP
![alter text](https://image.slidesharecdn.com/dsp-architecture-130206021715-phpapp01/95/dsp-architecture-35-638.jpg?cb=1360117114)

## Entorno DSP
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-05-30%20192954.jpg?raw=true)

----------------------------------------------------------------------------------------------------------------------------------------

# Mejoras a la arquitectura  DSP
A mediados de los 90s, comenzó a emerger el DSP mejorado. Una característica común de estos DSPs mejorados es la presencia de un segundo MAC, que permite un cierto paralelismo en el cómputo. En muchos casos, este paralelismo se extiende a otros elementos en el DSP, permitiendo que el dispositivo realice en una sola instrucción, operaciones de múltiples datos (SIMD Single Instruction Multiple Data). Esto se logra a menudo con el empaquetamiento de los datos, que permite a los registros, y a los data-path, manejar dos “medias palabras” (half-words) como operandos en cada ciclo de reloj. Junto con el empaquetamiento de datos, muchos DSPs mejorado permiten instrucciones con anchuras fraccionarias de palabra, lo cual permite lanzar instrucciones múltiples simultáneamente. El DSP mejorado también tiende a incorporar características para aumentar la velocidad de ejecución de algoritmos en un espacio de aplicación específico, así como agregar periféricos de propósito especial y memoria. La naturaleza exacta de la especialización varía con el uso al que va destinado el DSP mejorado, que hace que las comparaciones entre ellos sean las instrucciones en la que una de ellas dependa de los resultados de la otra. No todo el software de uso de DSP tiene una estructura adecuada para la ejecución de lanzamiento múltiple, pero cuando es posible, se consiguen DSP con un rendimiento más alto.
Actualmente la arquitectura interna de la DSP multi núcleo tiene 8 unidades funcionales que pueden ejecutar 8 instrucciones por ciclo, en términos de "núcleos CUDA" cada DSP tiene 16 "núcleos" . En C6678, HYPER LINK permite conectar DSP en pares para que pueda obtener 32 núcleos a 1,2 GHz.

## Mejoras más importantes
VLIW + memoria + consumo + complejidad de programación 
SIMD + memoria + consumo + complejidad de programación 
Sets de instrucciones más simple aumenta la velocidad + memoria 
Mezcla de longitudes de las palabras para reducir la memoria que se usa 
Segmentado de la máquina cada vez mayor para aumentar la velocidad del reloj + memoria + consumo + complejidad de programación  
DSPs unidos con procesadores de propósito general · Se busca que exista la mayor compatibilidad posible

----------------------------------------------------------------------------------------------------------------------------------------

# Portafolio de procesamiento integrado
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-05-30%20193832.jpg?raw=true)

## Comparación de los DSP más modernos
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-06-01%20021127.jpg?raw=true)

----------------------------------------------------------------------------------------------------------------------------------------

# Programación y Herramientas de Programación
Flujo de Compilación
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-06-01%20021520.jpg?raw=true)

SImulink + RealTime WorkShop + Embbeded Target
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-06-01%20021653.jpg?raw=true)

Labview + DSP Module
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-06-01%20021812.jpg?raw=true)

RIDE (Visual Application Builder)
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-06-01%20021857.jpg?raw=true)

----------------------------------------------------------------------------------------------------------------------------------------

# Conclusión
Los DSPs han ido evolucionando desde su creación hasta la actualidad, los cuales se han convertido en un dispositivo muy importante para las comunicaciones en la actualidad, para  la electrónica de consumo y diferentes aplicaciones a las que se ha ido adaptando con el tiempo.
Además los DSPs están diseñados, en su mayor parte, para sistemas embebidos, es decir para sistemas autónomos, como teléfonos móviles, cámaras de fotografiar digitales, etc. En este tipo de aplicaciones el precio, el consumo, el tamaño y la ocupación de memoria son factores básicos a la hora de la comercialización.
Las mejoras que pueden incluir un DSP son varias: se incluyen buses para transferir instrucciones y datos de tamaño superior al necesario, más de un bus de direcciones y de datos para acceder a los datos, implementación de técnicas de paralelismo para permitir la segmentación de la ejecución de las instrucciones y hacer varias operaciones elementales por ciclo, operaciones lógicas y aritméticas complejas, etc.

Pero también podríamos catalogar como problemas para los DSP la creación de nuevas tecnologías como lo son los nuevos dispositivos FPGA que se están convirtiendo en instrumentos increíblemente flexibles, ya que son programables y contienen bloques de lógica cuya interconexión y funcionalidad puede ser configurada en el momento. Además de que sus costes han ido disminuyendo lo cual los hace más accesibles al consumidor.

La solución que aportan los DSP es que pueden realizar operaciones matemáticas complejas en un solo ciclo de reloj por lo que el procesado (de señales de audio, de video, etc.) es el ideal, en contraposición a lo que aportan los microprocesadores convencionales (cualquiera de los que tienen nuestros PC de casa).
El procesamiento digital de señales ha sido una tarea que se distingue por su alto requerimiento de procesamiento de datos, lo que lo hace un área de interés en el diseño de hardware especializado.

----------------------------------------------------------------------------------------------------------------------------------------

# Referencias
colaboradores de Wikipedia. (2019, diciembre 1). Conversión analógica-digital. Recuperado de https://es.wikipedia.org/wiki/Conversi%C3%B3n_anal%C3%B3gica-digital

colaboradores de Wikipedia. (2020a, enero 14). Señal analógica. Recuperado de https://es.wikipedia.org/wiki/Se%C3%B1al_anal%C3%B3gica

colaboradores de Wikipedia. (2020b, febrero 7). Procesador digital de señales. Recuperado de https://es.wikipedia.org/wiki/Procesador_digital_de_se%C3%B1ales

colaboradores de Wikipedia. (2020c, mayo 11). Señal digital. Recuperado de https://es.wikipedia.org/wiki/Se%C3%B1al_digital

ElectronicaSi. (s. f.). DSPs. Recuperado de http://www.electronicasi.com/wp-content/uploads/2013/04/dspElectronica-avanzada.pdf

Farrell, S. I. (2010, febrero). Conversin Analgica Digital. Recuperado de http://www.sceu.frba.utn.edu.ar/dav/archivo/homovidens/farrell/Proy-Final-SFARRELL/Proy-Final/Simulador/conversion.html

González, G. A. (2017, septiembre). Definición de Digitalización. Recuperado de https://www.definicionabc.com/tecnologia/digitalizacion.php

Orenga, M. A., & Manonellas, G. E. (s. f.). Estructura de computadores. Recuperado de http://cv.uoc.edu/annotation/8255a8c320f60c2bfd6c9f2ce11b2e7f/619469/PID_00218274/PID_00218274.html
