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
| Sensor magnético inferior (I6) | Detectar la cortina en la posición inferior | El motor se detiene, se enciende la lámpara verde y después de 10 segundos comienza a subir|El motor se detuvo, se encendió la lámpara verde y después de 10 segundos inició la subida,, pero necesitaba mayor rango de detección al igualq ue el superior y el medio|

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
  
Con el LOGO utilizamos muchas compuertas lógicas de And y Or, con el fin de establecer condiciones base de funcionamiento de la cortina, además de establecer un temporizador de 10 segundos cuando se detectara en el magnético inferior. Para los interlocks que se utilizaron pues fue básicamente que cualquier sensor ajeno a los magnéticos el cual estuviera detectando, tendría que detener por completo la cortina para asegurar la seguridad y resguardo del operador. Se utilizó una programación cíclica para que las pruebas del manejo de la cortina fueran más naturales y seguidas. También, dentro del circuito se utilizó una clema que permitía cerrar y abrir el circuito con el fin de proteger y facilitar la conexión al circuito (Principalmente el LOGO) en caso de algún incidente, fue utilizado de manera recurrente para reiniciar el sistema en un estado de "cortina cerrada" durante las múltiples pruebas del sistema

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
- Cableado ✔ (Con gran área de oportunidad
- Seguridad ✔
- Evidencias (video/fotos) ✔
---
## Reflexión breve del equipo
¿Qué fue lo más crítico de esta etapa?
- Lo más crítico en esta parte fue el montaje y la prueba de la programación con los componente ya armados, haciendo énfasis en el montaje debido a que hubo problemas con la manufactura de las piezas que al final se resolvió simplificando el sistema y cambiando de material de impresión; Para la parte de la programación fue un momento crítico porque tuvimos que revisar unos cuantos bugs que aparecían en la lógica del programa haciendo activación de sensores, pero al final se pudo resolver rápidamente. Aprendimos mucho sobre esta experiencia porque copmrendimos la importancia de tener medidas milimétricas y pensar a fondo los posibles errores de lógica y seguridad que podrían tener nuestros proyectos para pdoer administrar e integrar correctamente los interlocks que consideremos necesarios

## Tabla Pass or FAIL

| # Intento  | Resultado obtenido |
|--- | ---------------------- | 
| 1 | FAIL |
|2 | FAIL |
|3 | PASS |
| 4 | FAIL |
|5 | FAIL |
|6 | FAIL |
| 7 | FAIL |
|8 | FAIL |
|9 | PASS |
| 10 | FAIL |
|11 | FAIL |
|12 | FAIL |
| 13 | FAIL |
|14 | PASS |
|15 | PASS |
| 16 | PASS |
|17 | PASS |
|18 | PASS |
|19 | PASS |
|20 | PASS |

Se realizaron un total de aproximadamente 20 pruebas con el fin de obtener resultados satisfactorios o incluir mejoras para el sistema, después de una larga racha de FAIL y unos cuantos milagros de PASS, resolvimos unos problemas con el diseño y el hardware de nuestro sistema y las pruebas comenzaron a presentar estado "PASS". A pesar de no tener evidencia debido a situación momentánea para corregir el proyecto, el profesor estuvo presente durante casi todas las pruebas viendo nuestro progreso, al final en la última prueba el profesor observó de manera directa nuestra prueba exitosa para poder darle el "visto bueno".
