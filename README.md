# BOMBATEMP
Sistema de monitoreo de temperatura para bomba sumergible

## DESCRIPCION DEL SISTEMA
El sistema está conformado por un sensor de temperatura digital DS18B20 que se encarga de medir la temperatura de la carcasa de un boma sumergible. Las lecturas de temperatura del sensor se lee mediante un microcontrolador que está monitoreando continuamente la temperatura y verifica que la misma no sobrepase un unmbral predeterminado por el usuario (Temperatura Alarma). El sistema incluye un relé, el cual cambia de estado si se sobrepasa el umbral de temperatura. Los datos de temperatura actual y el punto umbral de temperatura máxima se muestran en un display.

## UMBRAL DE TEMPERATURA
Para evitar que el relé se active/desactive si la temperatura se encuentra variando muy cerca del punto de temperatura de alarma, se configura también una temperatura menor (temperatura de reestablecimiento) para asegurar el cambio del relé a estado normal cuando la temperatura baje de este valor. Por ejemplo, si la la temperatura de alarma es configurada a 50 grados y la temperatura de reestableciemiento es 47 grados, el sistema opera en modo normal siempre y ciando la temperatura sea menor a 50 grados. Si la temperatura es mayor a 50 grados, el sistema opera en modo de alarma y permanece en este estado hasta que la temperatura disminuya a un valor menor a 47 grados.

## CONFIGURACION DE UMBRALES
La configuración de los valores de umbral se realiza mediante comandos seriales a una velocidad de 9600, 8 , N, 1 los cuales pueden ser enviados desde una PC con un cable USB tipo C estándar

## SENSOR DE TEMPERATURA
El modelo de sensor del DS18B20 utilizado es el mostrado en la figura siguiente:
<img width="800" alt="Sensor de Temperatura" src="https://github.com/Ferivas/BOMBATEMP/blob/main/DOCS/DS18B20.jpg">

el cual tiene un precio referencial en esta página 

[Sensor Temperatura](https://www.sparkfun.com/temperature-sensor-waterproof-ds18b20.html)

## DISPLAY 
El display que se va a utilizar es el SSD1306 que puede conseguirse en el mercado local y es similar al mostrado en la figura siguiente:

<img width="800" alt="Display" src="https://github.com/Ferivas/BOMBATEMP/blob/main/DOCS/Display.jpg">






