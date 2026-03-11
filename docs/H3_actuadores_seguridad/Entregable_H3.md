# Hito 3 – Control e Integración

## Descripción de la lógica de control
Explica la secuencia o lógica implementada en LOGO.
El logo se programó de una manera un poco diferente a los demás equipos, de manera en que el funcionamiento es el siguiente:
- Cuando se detecta la cortina arriba esta procede a bajar hasta llegar a la parte de abajo donde se detiene por 10 segundos antes de volver a subir, y en el momento en el que llega a la parte de arriba vuelve a bajar de manera inmediata.
- Cuando la cortina está en movimiento, ya sea arriba o hacia abajo se enciende la luz roja.
- Cuando la cortina se detiene en la parte de abajo se enciende la luz verde.
- Cuando el sensor óptico detecta se encienden ambas luces a manera de precaución, de que hay alguien cerca de la cortina, si se está bajando la cortina esta se detiene con esta detección hasta que pase la persona, pero si se está subiendo no se detiene, simplemente se encienden las dos luces, lo mismo pasa con el inductivo, ya que estos están conectados por una compuerta "or".
- Cuando el sensor capacitivo detecta se detiene el motor, esté donde esté, y se encienden ambas luces, este es un botón de emergencia para detener el movimiento de la cortina. 
- En situaciones imposibles como la detección de la cortina en dos puntos diferentes se detiene el motor y se encienden ambas luces.

## Entradas y salidas
| Entrada | Tipo | Función |
|--------|------|---------|
| Sensor capacitivo (I1) | Digital | Su función es detener el motor en el estado en el que esté, es un botón de emergencia que detendrá el funcionamiento del sistema y además encenderá luces de alerta que son la verde y roja al mismo tiempo |
| Sensor inductivo (I2) | Digital | Su función, en conjunto con el óptico, es detectar si hay algo por debajo de la cortina, de manera que si lo hay mientras baja se detiene el motor, y si lo hay mientras sube solo se encienden las luces de alerta |
| Sensor óptico (I3) | Digital | Su función, en conjunto con el indcutivo, es detectar si hay algo por debajo de la cortina, de manera que si lo hay mientras baja se detiene el motor, y si lo hay mientras sube solo se encienden las luces de alerta |
| Sensor magnético (I4) | Digital | Este sensor detecta cuando la cortina se encuentra arriba, de manera en que al llegara este punto deje de subir y vuelve a bajar |
| Sensor magnético (I5) | Digital | Este sensor detecta cuando la cortina está en medio, de manera que el motor mantenga el giro que lleva | 
| Sensor magnético (I6) | Digital | Este sensor detecta cuando la cortina está abajo, de manera en que el motor se detiene al llegar hasta abajo y la luz verde se enciende, mientras se esperan 10 segundos para volver a subir |   

| Salida | Tipo | Función |
|--------|------|---------|
| Motor bajar (Q1) | (Se toma como) Digital | Sirve para bajar la cortina una vez llega arriba, se detiene al llegar abajo, cuando se presiona el botón de precaución y cuando se detecta presencia | 
| Motor subir (Q2) | (Se toma como) Digital | Sirve para subir la cortina una vez llega abajo y pasan los respectivos 10 segundos y se detiene al llegar arriba y cuando se presiona el sensor de emergencia (capacitivo) |
| Lámpara roja (Q3) | (Se toma como) Digital | Se enciende sola cuando se detiene el motor en la parte de abajo y en conjunto con la luz verde en las luces de alerta cuando se enciende el inductivo o se detecta presencia, también se encienden en los casos de error como detección de cortina en dos lugares diferentes | 
| Lámpara verde (Q4) | (Se toma como) Digital | Se enciende sola cuando se detiene el motor en la parte de abajo y en conjunto con la luz roja en las luces de alerta cuando se enciende el inductivo o se detecta presencia, también se encienden en los casos de error como detección de cortina en dos lugares diferentes | 

## Pruebas realizadas
| Prueba | Resultado esperado | Resultado obtenido |
|--------|------|-----|
| Poner dos imanes en dos sensores diferentes | Que el motor se detenga y se enciendan los focos rojo y verde | Se detuvo el motor y se encendieron ambas luces | 
| Poner un objeto frente al sensor óptico y/o inductivo mientras baja el motor | Que el motor se detenga y se enciendan los focos rojo y verde | Se detuvo el motor y se encendieron ambas luces |
| Poner un objeto frente al sensor óptico y/o inductivo mientras sube el motor | Que el motor no se detenga, solo se encienden los focos rojo y verde | Se encendieron ambas luces sin detenerse el motor |
| Pulsar el sensor capacitivo mientras el motor sube y mientras baja | Que el motor se apague y se enciendan ambas luces roja y verde | El motor se apagó y se encendieron ambas luces roja y verde |

## Ajustes realizados
Las pruebas anteriores se realizaron después de corregir un error en el que código que alteraba todo el funcionamiento del sistema, y es que el sensor inductivo funciona de manera inversa, marca 1 al no detectar y 0 al detectar, por lo que se tuvo que poner una negación en este, pero a partir de esto el funcionamiento ya fue el esperado. 
