# Hito 3 – Control e Integración

## Descripción de la lógica de control
Explica la secuencia o lógica implementada en LOGO.

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
|------|------------------|------------------|

## Ajustes realizados
Describe cambios hechos tras las pruebas.
