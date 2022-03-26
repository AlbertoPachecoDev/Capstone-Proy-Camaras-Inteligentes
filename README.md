# Sistema de Vigilancia con Cámaras Inteligentes

![](https://github.com/AlbertoPachecoDev/Capstone-Proy-Camaras-Inteligentes/blob/main/logos.jpg)

## Proyecto Capstone Diplomado IoT de Samsung Innovación Campus y Código IoT

### Integrantes:
 - Representante: Alberto Pacheco González (UACH)
 
### Descripción del proyecto:

El sistema consiste en un conjunto de cámaras de video (ESP32-Cam) capaces de ser controladas de forma automática en base a las señales de entrada proveniente de un arreglo de micrófonos y sensores de presencia, en principio, provenientes de un conjunto de módulos que permiten configurar un un arreglo de micrófonos ubicados endistintas zonas de vigilancia o interés, de tal forma que, dependiendo de la intensidad de las señales de audio y proximidad obtenidas (sensores micrófonos y ultrasonido), donde se determinará en base al análisis de los datos captados, ubivar la zona de interés, seleccionar la cámara adecuada y controlar su posición para desplazar angularmente con la ayuda de motores ubicados en la base de cada cámara, la posición de la cámara de vigilancia respectiva (control motor CD).


### Requerimientos de Complejidad:

80% Análisis Datos:  Análisis señales captadas
- Audio: potencia RMS (energía)
- Ultrasonido: distancia objeto detectado
- Detectar patrones
- Triangular fuente
- Funciones de control y alerta

### Red de sensores vía I2C

![](https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/09/I2C-communication-protocol-ESP32.png?quality=100&strip=all&ssl=1)

### Tareas:
 1. Capturar señal micrófono
 2. Capturar señal detector presencia
 3. Analizar señales
 4. Obtener hora/día del RTC
 5. Noche? encender luz 
 6. Grabar señales (audio) 
 7. Transmitir datos evento(s) por I2C
 8. Identificar y seleccionar evento 
 9. Notificar evento: alerta local
10. Grabar evento en datalog (sd-card) 
11. Seleccionar cámara y calcular posición
12. Mover cámara (motor-pasos)
13. Tomar foto(s)
14. Grabar foto(s) en sd-card
15. Notificar evento MQTT

### Componentes:

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
