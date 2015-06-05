# OpenGrab Electro Permananet Imán #

EPM688-5, EPM688-5-S

## Descripción general ##

El EPM688-5 y EPM688-5-S son imanes Electro Permanentes, combinando las ventajas de electroimanes y permanentes. Este dispositivo viene con electrónicos integrados que pueden ser operados con señales TTL de 3.3 y 5V y utiliza VCC de 5V.

<img width='600' align='right' src='http://i.imgur.com/xrnK6WM.jpg' />
## Aplicaciones ##
  * El trabajo de agarre de brazo robotico
  * Ascensor de carga para Vehiculos Aereos No Tripulados
  * Demostración de educación de las propiedades magnéticas

## Características ##

  * 5V Vcc
  * 3,3 o 5 V TTL señal
  * Mínimo de energía en estado estacionario <1mW
  * Revestimiento de resistente al agua
  * Shocks 330V son posibles al tocar la unidad (pendiente la patente de encendido automatico)




## Condiciones operativas recomendadas ##

| **Símbolo** | **Parámetro** | **Clasificación** | **Unidades** |
|:-------------|:---------------|:-------------------|:-------------|
| Vcc          | Alimentación Tensión  | 5                  | V            |
| Imax         | Corriente de alimentación máxima | 1.5                | A            |
| Vsig low     | baja tensión máxima de la señal [1](1.md) | 2.2                | V            |
| Vsig high    | alto voltaje de señal mínimo[1](1.md) | 2.8                | V            |
| Vsig max     | Tensión máxima de la señal | 5                  | V            |
| Tmax         | Temperatura máxima [2](2.md) | 50                 | deg C        |
| Tcharge      | Tiempo de carga | 3                  | s            |
| Fmax         | Max fuerza de retención | 80                 | N            |
| M            | Masa           | 55                 | gram         |



[1](1.md) Vsig no esta definida entre 2.2 y 2.8V. Operacion de esta señal en esta zona puede causar el apagado prematuro de los IGBT bajo alta corriente y causar daño permamente. Oscilaciones en cualquiera de Vsig o Vcc puede causar el rapido apagado y encendido de los IGBT. Esto se puede evitar mediante el uso de una fuente de alimentación limpio. [4HC\_HCT32.pdf](http://www.nxp.com/documents/data_sheet/74HC_HCT32.pdf) debe ser consultado.


[2](2.md) Sin electrolítico condensador 80 ° C


## Funciones de los Pins ##

### Gnd (Pin 1 and 6) ###
Pin de tierra
### Vcc (Pin 2 and 5) ###
5V <ondulación 100mV
### S\_off (Pin 3) ###
Poner este pin alto (1 kohm pull-down) hace que el imán se apague si se carga el condensador, la descarga se detendrá automáticamente en 300US incluso si se mantiene alto. Manteniendo este pin a alto por 3s carga el condensador lleno y está listo para el siguiente ciclo. La relativa alta tasa de autodescarga del condensador debe ser tomado en cuenta, tiempo recomendado es <10s.


### S\_on (Pin 4) ###

Igual que S\_off

### Gehäuse 1-6 ###
Breakout de los 6 puntos de contacto para el uso para el contacto eléctrico

## Operación ##

El EPM688-5 está diseñado para sujetar una carga de 1 kg y encender y apagar con eficacia con bajo consumo de energía. 800mA a 5V para 3S o 3.4J por ciclo.

Bajo la condición de descarga del condensador poner S\_On o S\_off alta> 2,8 V durante 3 segundos y luego baja. El condensador está completamente cargada y el dispositivo está listo para el ciclo. Poner S\_On o S\_off alta hace que el campo magnético se mueva, ya sea en el estado encendido o apagado. Se debe tener cuidado de que el S\_On o S\_off están en lo alto de no menos de 500uS, de lo contrario IGBT apagado bajo condiciones de alta corriente puede provocar daños.
Poner S\_On o S\_off baja después de que >500uS han expirado hace que el controlador cargue el condensador, deteniéndose automáticamente una vez que alcance 330V, a unos 3 segundos.



## Dibujo ##
<img width='1000' align='right' src='http://i.imgur.com/CgFtE4d.jpg' />

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br><br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>