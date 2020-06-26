# Diseno_Digital
# Timmers y control de iluminación 
A continuación se muestra un ejercicio ue consiste en la interrupción de un Led mediante un timmer, se prentende mostrar la cofiguración de los timmers como tema cetral, pero tambien se mostrará como es la configuración de otors periféricos.
Se trabajó con la tarjeta SYM32L476RG y como salida se utilizará el led del sistema de desarrollo.

para la configuración de la salida se utilizará el GPIOA configurando así.

## Habilitar AHB2ENR
imagen

Ahora se configura que el pin del GPIO
## Pin 5
imagen

Se configura el pin como salida

## pin 5 output


Ahora se procede a configurar el reloj del timmer 2

## Habilitar APB1ENR1

Ahora se activa SYSCFG clock para los perifiercos del sistema 


