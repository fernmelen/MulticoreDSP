![alter text](https://tectijuana.edu.mx/wp-content/uploads/2014/11/Heading-Ing-sistemas-2048x672.png)
### Lenguajes de Interfaz
### Docente: René Solís Reyes
### Proyecto: Multicore DSP
### Semestre: enero - junio 2020

### 17212143  Hector Armando Jaramillo Regino
### 17211505 Alejandro Castillo Licea
### 1721…. Gloria Alejandra Jimenez Mayoral
### 17212183 Alberto Sánchez Barroterán
### 17211539 Melendez Palafox Fernando Esaú
### 17211555 Ramos Cedeño Kevin Enrique
### Tijuana B.C. a 20 de mayo de 2020

----------------------------------------------------------------------------------------------------------------------------------------
Índice
Planteamiento del problema
DPS
DSP y Microprocesador
ADC
Señal Analogica Y Digital
Digitalización
Pasos para la Digitalización de una señal digital
MUESTREO
CUANTIZACIÓN
CODIFICACIÓN
Funcionamiento DSP
Aplicaciones del DPS
Campos de aplicación del DPS
Arquitectura
Mejoras más importantes
Portafolio de procesamiento integrado
Programación y Herramientas de Programación
Conclusión
Bibliografía

----------------------------------------------------------------------------------------------------------------------------------------
## Planteamiento del problema.
Comenzamos explicando un poco sobre las señales por un lado tenemos el procesamiento de señales analogicas y por el otro el procesamiento de señales digitales. En todo esto hay un inconveniente y es que si nos ponemos a ver detenidamente podemos observar que puede llegar a ver distorsión a la hora de que alguna señal analogica ocupe ser procesada. Es por eso que se optó por el procesamiento digital de señales “DSP” ya que este ofrece la gran ventaja de que esta distorsión es disminuida.

Ahora tenemos el multicore qué significa multinúcleo el cual sí vemos su especificación dice que es aquel que combina dos o más microprocesadores independientes en un solo paquete, y que a menudo es un solo circuito integrado. 

Entonces con estas dos partes explicadas podemos ver que un multicore dsp por un lado trabaja combinando núcleos y que también trabaja de manera digital. Ahora se procederá a la explicación de todo lo que conlleva el  multicore dsp, qué es, cómo funciona, aplicaciones, etc. 

## DPS: 
También llamado Procesador Digital de Señales o por sus siglas en ingles digital signal processor es un sistema basado en un procesador o microprocesador que posee un conjunto de instrucciones, un hardware y un software optimizados para aplicaciones que requieran operaciones numéricas a muy alta velocidad. Debido a esto es especialmente útil para el procesado y representación de señales analógicas en tiempo real.
Dicho sistema trabaja en tiempo real en el cual se reciben muestras normalmente provenientes de un conversor analógico/digital (ADC).

## ADC: 
La conversión analógica-digital consiste en la transcripción de señales analógicas en señal digital, con el propósito de facilitar su procesamiento y hacer la señal resultante (digital) más inmune al ruido y otras interferencias a las que son más sensibles las señales analógicas.

## Aplicaciones del DPS:
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

## Campos de aplicación del DPS:

- Telecomunicaciones: En el campo de las telecomunicaciones, los productos que utilizan frecuentemente microcontroladores son los teléfonos móviles.
- Productos de gran consumo: En los productos de gran consumo se utilizan microcontroladores en muchos electrodomésticos de línea blanca (lavadoras, lavavajillas, microondas, etc.) y de línea marrón (televisores, reproductores de DVD, aparatos de radio, etc.).
- Automoción: En la industria del automóvil se utilizan microcontroladores para controlar buena parte de los sistemas del coche; por ejemplo, para controlar los airbags, o el frenado.
- Informática: En la industria informática hay muchos dispositivos periféricos que integran microcontroladores: ratones, teclados, impresoras, escáneres, discos duros, etc.
- Industria: En el mundo industrial se utilizan en diferentes ámbitos, como la robótica o el control de motores.

----------------------------------------------------------------------------------------------------------------------------------------
Software:
https://es.wikipedia.org/wiki/Procesador_digital_de_se%C3%B1ales
https://es.wikipedia.org/wiki/Conversi%C3%B3n_anal%C3%B3gica-digital
http://cv.uoc.edu/annotation/8255a8c320f60c2bfd6c9f2ce11b2e7f/619469/PID_00218274/PID_00218274.html
----------------------------------------------------------------------------------------------------------------------------------------

## Entorno DSP
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-05-30%20192954.jpg?raw=true)
La arquitectura interna de la DSP multinúcleo tiene 8 unidades funcionales que pueden ejecutar 8 instrucciones por ciclo, en términos de "núcleos CUDA" cada DSP tiene 16 "núcleos" . En C6678, HYPER LINK permite conectar DSP en pares para que pueda obtener 32 núcleos a 1,2 GHz.

## Portafolio de procesamiento integrado
![alter text](https://github.com/fernmelen/MulticoreDSP/blob/master/Imagenes%20Multicore%20DSP/Anotaci%C3%B3n%202020-05-30%20193832.jpg?raw=true)

http://cv.uoc.edu/annotation/8255a8c320f60c2bfd6c9f2ce11b2e7f/619469/PID_00218274/PID_00218274.html
----------------------------------------------------------------------------------------------------------------------------------------
Aplicaciones:
http://cv.uoc.edu/annotation/8255a8c320f60c2bfd6c9f2ce11b2e7f/619469/PID_00218274/PID_00218274.html
----------------------------------------------------------------------------------------------------------------------------------------
