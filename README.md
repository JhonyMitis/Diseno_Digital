# Diseno_Digital
# Timmers y control de iluminación 
A continuación se muestra un ejercicio ue consiste en la interrupción de un Led mediante un timmer, se prentende mostrar la cofiguración de los timmers como tema cetral, pero tambien se mostrará como es la configuración de otors periféricos.
Se trabajó con la tarjeta SYM32L476RG y como salida se utilizará el led del sistema de desarrollo.

La configuración de los periféricos se hace de la siguiente manera.

## Habilitar AHB2ENR
Se configura la el reloj para el GPIOA así:
![AHB2ENR](AHB2ENR.PNG)


## GPIOx_MODER
Ahora se configura que pin se va a escoger del GPIOA en este caso el pin 5
![GPIO_MODER](GPIO_MODER.PNG)


## GPIOx_ODR
Se configura el pin 5 como salida

![GPIO_ODER](GPIO_ODER.PNG)

## Habilitar APB1ENR1
Ahora se procede a configurar el reloj del timmer 2
![APB1ENR1](APB1ENR1.PNG)

## Habilitar APB2ENR
Ahora se activa SYSCFG clock para los perifiercos del sistema 
![APB2ENR](APB2ENR.PNG)

## Definir Preescaler
En este registro se almacnea el preescalador del reloj
![ESCALER](ESCALER.PNG)

## Definir el periodo
Este registro almacena la información del la duración del periodo del pulso.
![ARRAN](ARRAN.PNG)

## Definir el timmer como interrupción de prioridad 1

_NVIC_SetPriority(TIM2_IRQn, 1);_

## Activar interrupcion del timmer

_NVIC_EnableIRQ(TIM2_IRQn);_


## Tarea

Configurar un otro timmer para alternar la interrupcion entre encendido y apagado con distinta duración



