## Sistema de Seguridad y Preservación del Acervo de la Biblioteca Histórica UJAT José Martí

![](https://github.com/AlbertoPachecoDev/Capstone-Proy-Camaras-Inteligentes/blob/main/logos.jpg)

## Proyecto Capstone Diplomado IoT de Samsung Innovación Campus y Código IoT

### Integrantes:
 - Alberto Pacheco González (UACH) [Representante]
 - Erika Yunuen Morales Mateos (UJAT)
 - Rosalino Ovando Chio (UJAT)

### Problema

La UJAT cuenta con una colección de libros antiguos que datan de 300 años, dicha colección necesita una infraestructura especial que permita ofrecer un tratamiento especial de restauración y conservación. Entre los factores que afectan estos libros se encuentran: la humedad, la temperatura, las plagas, entre otros. Otros requerimientos importantes son: el control de acceso restringido, la seguridad y vigilancia de este patrimonio cultural e histórico y ofrecer además estas facilidades a un costo razonable.

### Objetivo

Implementar un sistema de seguridad y preservación del acervo de libros antiguos de la Biblioteca Histórica José Martí de la UJAT utilizando diversos sensores, actuadores y videocámara motorizada. 

### Objetivos Específicos

- Medir la humedad y temperatura
- Detectar humo y plagas
- Controlar la iluminación: ahorro de energía, seguridad y preservación
- Controlar cámaras motorizadas de vigilancia
- Controlar ventiladores para  climatizar salas
- Controlar ventiladores en modo de extractor

### Beneficios
 - Ahorro de energía
   -  Iluminación: encendido/apagado programado, intensidad auto-ajustable
   -  Vigilancia: activación y posicionamiento de cámaras basada en el contexto
 - Ahorro de memoria (registro datos)
 - Acopio y analítica de datos
 - Probar distintos algoritmos/modelos

### Antecedentes (Contexto)

La biblioteca “José Martí” perteneciente al Sistema Bibliotecario de la Universidad Juárez Autónoma de Tabasco es la más antigua de las nueve que lo conforman. Su historia ha estado vinculada con la vida cultural e intelectual de la ciudad, pues fue inaugurada el 12 de octubre de 1944.
En la actualidad  es la  biblioteca histórica de la UJAT, siendo uno de los principales repositorios de la historia del estado. Cuenta con un acervo aproximado de más de 30,000 volúmenes, entre los que se cuentan obras de cultura general y colecciones locales únicas en su género.

Aunado a estas valiosas colecciones tenemos obras que datan de  más de dos siglos como Las Obras de Santa Teresa, 1670 o Vida y hechos del Ingenioso Caballero don Quijote de la Mancha, de don   Miguel de Cervantes Saavedra., en una edición de 1732. Se cuenta con una de las dos hemerotecas organizadas del estado, la que alberga materiales documentales valiosos para la vida de Tabasco como son colecciones de periódicos y revistas locales desde  finales del siglo XIX  (Reforma desde 1869, El Progreso, Revistas Alfa y Alba, Revista Azul, etc.), el periódico Redención  de la época del Lic. Tomás Garrido Canabal, y colecciones casi completas y desde los primeros números de periódicos locales como Presente, Rumbo Nuevo, Avance, entre otros.


### Descripción

Implementar un sistema de preservación y protección del acervo de libros antiguos de la Biblioteca Histórica José Martí de la UJAT. El sistema consta de un conjunto de sensores para la detección de humedad, temperatura, humo y presencia. Dichos sensores permiten monitorear y registrar los rangos actuales e históricos para la adecuada preservación del acervo. En caso de que los sensores de humedad, temperatura y humo queden fuera de rango, se activarán los ventiladores y el deshumidificador. Los detectores de presencia permiten activar los actuadores para controlar los motores para ubicar las cámaras de vigilancia y la iluminación adecuada de las obras en exhibición.

La vigilancia y preservación de bienes es una de las acciones que toman diariamente organizaciones, instituciones y ciudadanía. Por lo que se plantea un proyecto que puede ser aplicable en diferentes sectores que tengan estas necesidades: vigilancia externa y cuidado interno de un inmueble, dados los objetos que resguardan.

Se propone vigilancia externa con optimización en cuanto a la iluminación y uso de cámaras, así como el cuidado y preservación de objetos, realizando la detección y registro de la humedad, temperatura, humo, y plagas, así como actuadores que ayudarán a mantener controlado el entorno. Esto mediante el uso de una red de sensores que se encuentren capturando y transmitiendo datos, se analizan los datos, permitiendo una mejor toma de decisiones sobre las condiciones que deben tener los espacios que guardan los objetos.
 
Para la vigilancia externa, el control automatizado de registro visual y auditivo se efectúa en base al procesamiento de datos recolectados en un arreglo de micrófonos y sensores de presencia. Los micrófonos y detectores de presencia ubicados en los extremos de las zonas de interés permiten iluminar las zonas activadas y controlar en base al análisis de los datos captados, la posición de la cámara activando el respectivo motor CD de forma continua y en tiempo real. El registro visual y auditivo del evento solo se efectúa cuando se activa y posiciona la cámara, optimizando de esta forma la seguridad, almacenamiento y uso de energía.

### Tareas:
- Integrante #1:
>
> 1. Capturar señal micrófono
> 2. Capturar señal detector presencia
> 3. Analizar señales
> 4. Obtener hora/día del RTC
> 5. Noche? encender luz 

- Integrante #2:
>
> 6. Grabar señales (audio) 
> 7. Transmitir datos evento(s) por I2C
> 8. Identificar y seleccionar evento 
> 9. Notificar evento: alerta local
> 10. Notificar evento MQTT

- Integrante #3:
>
> 11. Grabar evento en datalog (sd-card)
> 13. Seleccionar cámara y calcular posición
> 14. Mover cámara (motor-pasos)
> 15. Tomar foto(s)
> 16. Grabar foto(s) en sd-card

### Requerimientos de Complejidad:

80% Análisis Datos:  Análisis señales captadas
- Escalable
- Análisis de información
 - Audio: potencia RMS (energía)
 - Ultrasonido: distancia objeto detectado
 - Detectar patrones
 - Triangular fuente
 - Funciones de control y alerta

### Red de sensores vía I2C

![](https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/09/I2C-communication-protocol-ESP32.png?quality=50&strip=all&ssl=1)

### Componentes:

- **ESP32-CAM OV2640 Wifi Bluetooth.**                       1       $220.11
- **Convertidor USB Serial FTDI TTL FT232RL.**               1       $98.00
- **Cable USB a Mini USB Tipo B.**                           1       $64.00
- **Módulo Ads1115.**                                        1       $161.00
- **Fuente de Alimentación 5V 2A / 9V 1A / 12V 1A.**         1       $62.00
- **Led Amarillos 5mm.**                                     5       $15.00
- **Led Rojos 5mm.**                                         5       $15.00
- **Led Verdes 5mm.**                                        5       $15.00
- **Cables Dupont Largos h-h (hembra-hembra).**              40      $93.00
- **Buzzer.**                                                1       $36.00
- **Resistencias.**          

### Software
- **Arduino IDE**
- **MQTT**
- **Node-red**
- **MySQL**
- **Grafana**

### Subsistema de Iluminación y Vigilancia Inteligente

 - **Subproblema #1 De noche:** Fusionar red de sensores para controlar iluminación, posicionamiento, detección y registro. 
 
 - **Subproblema #2 De día:** Ignorar ruidos no "sospechosos". 

  > ![Sistema de Iluminación y Vigilancia Inteligente](https://github.com/AlbertoPachecoDev/Capstone-Proy-Camaras-Inteligentes/blob/72070e9e05f125d2737b1563c9dbbdb86ad8301a/CamaraMotorizada-demo-i2c.png)
  >
  > Sistema de Iluminación y Vigilancia Inteligente

Arreglo de micrófonos vía I2C:
1. [QuadMic 4-Microphone Array](https://makersportal.com/shop/quadmic-4-microphone-array)

  > [Application Note: Audio Processing with The QuadMic 4-Microphone Array on the Raspberry Pi](https://makersportal.com/blog/audio-processing-with-the-quadmic-4-microphone-array-on-the-raspberry-pi)

![](https://images.squarespace-cdn.com/content/v1/59b037304c0dbfb092fbe894/1610935560928-8R5BB4TPYTCFYAVHF664/quadmic_red_LEDs.JPG?format=1000w)


2. [INMP441 MEMS I2S Microphone](https://makersportal.com/shop/i2s-mems-microphone-for-raspberry-pi-inmp441)

![](https://images.squarespace-cdn.com/content/v1/59b037304c0dbfb092fbe894/1606076376715-ZNHI468TMG4K8DOWP24Y/INMP441_zoom_port_writing.JPG?format=1000w)

![](https://images.squarespace-cdn.com/content/v1/59b037304c0dbfb092fbe894/1606076409876-LWA5AQR2Q79B5364TWHF/i2s_rpi_INMP441_stereo.png?format=1000w)

![image](https://user-images.githubusercontent.com/80423661/160221127-5ddf85e7-97df-4790-93e5-e60db830fa95.png)

3. [PCF8574 I2C Port Expander](https://create.arduino.cc/projecthub/Samhain/pcf8574-expander-with-4-inputs-4-outputs-9a80ef)

https://www.instructables.com/PCF8574-GPIO-Extender-With-Arduino-and-NodeMCU/

![](https://www.pcboard.ca/image/catalog/products/pcf8574/pcf8574-addressing.jpg)

----

## Introducción

## Alcances

## Justificación

## Funcionamiento Esperado

## Circuito a realizar

## Conclusiones

## Trabajo a futuro

## Referencias




