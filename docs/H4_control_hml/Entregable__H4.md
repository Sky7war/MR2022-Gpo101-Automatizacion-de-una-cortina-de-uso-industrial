# Hito 4 – Validación Funcional y HMI
## Objetivo del hito
Validar el funcionamiento integrado del sistema mecatrónico y la interacción con el
usuario mediante HMI.

## Estado general del sistema
Marca el estado actual del sistema:
- No funcional ⬜
- Parcialmente funcional ⬜
- Funcional con fallas ⬜
- Funcional estable ✔

## Secuencia de operación validada
Describe paso a paso cómo opera el sistema completo:

En nuestro caso es un funcionamiento cíclico en el cual se encienden los sensores y esto va creando algunas modificaciones en el ciclo, pero este de todas formas se vuelve a iniciar.  

1. Al encenderse la cortina lo que hace inmediatamente es detectar en donde se encuentra.
2. Dependiendo del lugar en el que se encuentre sube o baja, según sea el caso.
3. Al terminar de bajar se detiene por 10 segundos antes de volver a subir, pero al subir vuelve a bajar de inmediato.
4. Si se detecta alguna persona o algún material por parte de el motor óptico o inductivo se detiene en el caso de estar bajando y se encienden las luces verde y roja a manera de alerta, pero si está subiendo solo se encienden las luces de alerta.
5. En cualquier caso, si se presiona el sensor capacitivo (botón de emergencia) se detiene por completo la cortina, y se encienden las luces de alerta.

## Validación de sensores

| Sensor  | Condición probada | Resultado esperado | Resultado obtenido |
|--- | ---------------------- | --------------------- | -----|
| Sensor capacitivo (I1) | Activar el sensor mientras el motor sube o baja | El motor se detiene inmediatamente y se encienden las lámparas roja y verde como señal de alerta | El motor se detuvo inmediatamente y se encendieron ambas lámparas  |
| Sensor inductivo (I2) | Colocar un objeto frente al sensor mientras la cortina baja | El motor se detiene y se encienden las lámparas roja y verde      | El motor se detuvo y se encendieron ambas lámparas    |
| Sensor inductivo (I2) | Colocar un objeto frente al sensor mientras la cortina sube | El motor continúa funcionando y se encienden las lámparas roja y verde   | El motor continuó funcionando y se encendieron ambas lámparas   |
| Sensor óptico (I3) | Colocar un objeto frente al sensor mientras la cortina baja | El motor se detiene y se encienden las lámparas roja y verde   | El motor se detuvo y se encendieron ambas lámparas|
| Sensor óptico (I3) | Colocar un objeto frente al sensor mientras la cortina sube | El motor continúa funcionando y se encienden las lámparas roja y verde    | El motor continuó funcionando y se encendieron ambas lámparas|
| Sensor magnético superior (I4) | Detectar la cortina en la posición superior | El motor deja de subir y comienza el proceso de bajada   | El motor dejó de subir y comenzó a bajar |
| Sensor magnético medio (I5) | Detectar la cortina en la posición media | El motor mantiene el movimiento que llevaba | El motor continuó su movimiento sin cambios 
| Sensor magnético inferior (I6) | Detectar la cortina en la posición inferior | El motor se detiene, se enciende la lámpara verde y después de 10 segundos comienza a subir|El motor se detuvo, se encendió la lámpara verde y después de 10 segundos inició la subida|

## Validación de actuadores

| Actuador| Acción   | Resultado esperado | Resultado obtenido  |
| ----| ------ | ------| ------------|
| Motor bajar (Q1) | Activar el descenso de la cortina    | La cortina baja hasta detectar el sensor inferior o hasta activarse una condición de seguridad | La cortina descendió correctamente y se detuvo cuando correspondía   |
| Motor subir (Q2)| Activar la subida de la cortina después de 10 segundos en la posición inferior | La cortina sube hasta detectar el sensor superior          | La cortina subió correctamente hasta el sensor superior|
| Lámpara roja (Q3)| Activarse durante movimiento del motor o en condiciones de alerta       | La lámpara roja se enciende durante movimiento o junto con la verde en alertas| La lámpara roja se encendió correctamente en las condiciones indicadas|
| Lámpara verde (Q4)| Activarse cuando la cortina está detenida abajo o en condiciones de alerta     | La lámpara verde se enciende al detenerse abajo o junto con la roja en alertas    | La lámpara verde se encendió correctamente según las condiciones establecidas|


## Validación del controlador (LOGO)
Describe:
- Temporizaciones
- Condiciones lógicas
- Interlocks o seguridades implementadas

## HMI – Interfaz Humano-Máquina
Describe:
- Pantallas implementadas
- Variables mostradas
- Acciones disponibles para el usuario
Adjunta captura(s) de pantalla del HMI.

A pesar de sí haber hecho la interfaz en LWE, esta no se pudo implementar dentro del LOGO debido a la imposibilidad de pasar nuestro código del logo a la computadora por conexión alámbrica, por lo que se tiene solo una imagen de cómo estaba pleneada la interfaz humano-máquina de verse 

<img width="618" height="497" alt="image" src="https://github.com/user-attachments/assets/a5c877e4-c37b-4cc3-a3fb-3201291c9b10" />

Debido a todo esto es que no se podrán hacer pruebas con la interfaz correspondientes a las condiciones que probamos en código y en la vida real, por lo que no se incluye matriz de pruebas, resultados de estas ni se realizaron ajustes. 

## Preparación para demostración final
Indica qué está listo y qué falta por afinar:
- Lógica de control ✔
- HMI ✖ (no fue posible de implementar aunque hasta cierto punto se hizo)
- Cableado ✔
- Seguridad ✔
- Evidencias (video/fotos) ✔
---
## Reflexión breve del equipo
¿Qué fue lo más crítico de esta etapa?
