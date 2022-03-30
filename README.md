# Sistema de Iluminación y Vigilancia Inteligente 

![](https://github.com/AlbertoPachecoDev/Capstone-Proy-Camaras-Inteligentes/blob/main/logos.jpg)

## Proyecto Capstone Diplomado IoT de Samsung Innovación Campus y Código IoT

### Integrantes:
 - Representante: Alberto Pacheco González (UACH)
 - Integrante #2
 - Integrante #3

### Problema
En una casa-habitación, en vez de instalar muchas cámaras de vigilancia, es posible mover una sola cámara hacia algunas fuentes de ruido?

 - **Subproblema #1 De noche:** Identificar determinados ruidos nocturnos (energía-patrón y análisis de datos) se fusiona con los sensores de presencia para filtrar eventos de interés y activar además la iluminación de una manera más adecuada y eficiente. 
 
 - **Subproblema #2 De día:** Los ruidos "sospechosos", su frecuencia e intensidad cambia en el día (tráfico vehículos)

### Objetivo

Implementar un sistema de iluminación y vigilancia basado en arreglo de sensores y videocámaras con seguimiento inteligente (_automatic motion tracking_) pensado inicialmente para exteriores de casas habitación.

### Descripción

El control automatizado de registro visual y auditivo se efectua en base al procesamiento de datos recolectados en un arreglo de micrófonos y sensores de presencia. Los micrófonos y detectores de presencia ubicados en los extremos de las zonas de interés, permiten iluminar las zonas activadas y controlar en base al análisis de los datos captados, la posición de la cámara activando el respectivo motor CD de forma continua y en tiempo real. El registro visual y auditivo del evento solo se efectúa cuando se activa y posiciona la cámara, optimizando de esta forma la seguridad, almacenamiento y uso de energía.

  > ![Sistema de Iluminación y Vigilancia Inteligente](https://github.com/AlbertoPachecoDev/Capstone-Proy-Camaras-Inteligentes/blob/72070e9e05f125d2737b1563c9dbbdb86ad8301a/CamaraMotorizada-demo-i2c.png)
  >
  > Sistema de Iluminación y Vigilancia Inteligente

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




