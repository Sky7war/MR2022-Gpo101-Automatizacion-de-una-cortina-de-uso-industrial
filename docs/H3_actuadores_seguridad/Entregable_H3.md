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

## Pruebas realizadas
| Prueba | Resultado esperado | Resultado obtenido |
|------|------------------|------------------|

## Ajustes realizados
Describe cambios hechos tras las pruebas.
