# Hito Final – Prototipo Funcional

## Descripción del prototipo

En nuestro caso es un funcionamiento cíclico en el cual se encienden los sensores y esto va creando algunas modificaciones en el ciclo, pero este de todas formas se vuelve a iniciar.

- Al encenderse la cortina lo que hace inmediatamente es detectar en donde se encuentra.
- Dependiendo del lugar en el que se encuentre sube o baja, según sea el caso.
- Al terminar de bajar se detiene por 10 segundos antes de volver a subir, pero al subir vuelve a bajar de inmediato.
- Si se detecta alguna persona o algún material por parte de el motor óptico o inductivo se detiene en el caso de estar bajando y se encienden las luces verde y roja a manera de alerta, pero si está subiendo solo se encienden las luces de alerta.
- En cualquier caso, si se presiona el sensor capacitivo (botón de emergencia) se detiene por completo la cortina, y se encienden las luces de alerta.
 
## Evidencias

- Video de evidencia con comprobación de todo el funcionamiento: https://drive.google.com/file/d/1l6njuWS0FrmbVFWxYHiuuphqV2ezXxQm/view?usp=sharing
  
## Validación del sistema

El sistema diseñado para proteger al operador del robot y permitirle poner las piezas y retirarse sin mayor peligro sí es funcional, y auqnue usamos una lógica diferente de la propuesta para ejecutarlo, haciendo el sistema completamente cíclico, creemos que aún así puede ser útil en este reto, el detalle principal es el encendido del sistema que se hace conectando el fusible, esto es un aspecto a mejorar ya que el hecho de que el operador deba conectar el sistema puede no ser tan práctico en un entorno industrial.  

## Reflexión final

Este proyecto fue bastante nutritivo y de mucho aprendizaje, ya que tuvimos nuestro primer gran acercamiento a un sistema mecatrónico como se lleva a cabo en el entorno laboral, y pudimos integrar sensores previamente analizando sus características y en lo que más nos convenía utilizarlos. También tuvimos que hacer el sistema del Puente H con los relevadores, y fue muy importante prestar atención a todas las conexiones para verificar la seguridad del sistema, e integramos aspectos de diseño y realización de esquemáticos para tener claridad en cómo hacer el prototipo en la vida real, tanto conexiones como montaje, asegurándonos de que este fuera bueno desde la computadora. Por último, algo de lo más útil fue la visita que tuvimos a American Axle, donde vimos de una manera mucho más evidente la utilidad de estos sistemas en un entorno laboral y a una mayor escala. Este reto fue bastante interesante y de mucho aprendizaje para nosotros como futuros ingenieros.
