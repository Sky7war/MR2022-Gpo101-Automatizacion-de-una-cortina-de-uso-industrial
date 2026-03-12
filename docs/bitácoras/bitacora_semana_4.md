# Bitácora – Semana 4

## Tema de la semana
(HMI)
## Actividades realizadas
Se realizaorn los procesos finales de conexión y prueba para la cortina industrial, además se implementó una pantalla HMI para

## Decisiones de ingeniería
| Decisión | Alternativas | Justificación |
|--------|-------------|---------------|
|Agregar una condición NOT a la compuerta de unión AND para evitar que los motores giraran a lados opuestos.|Cambiar de otra manera el código, aun cuando el avance fue significativo. |Los motores giraban para lados opuestos, esto debido a que las dos condiciones de funcionamiento estaban en una compuerta AND, al momento de negar una de las dos entradas esa condición cambiaba por completo a una de giro simultáneo que va para el mismo lado.|
|Eliminar el tubo inferior para reducir el peso.|Retirar el tubo para analizar detalladamente el peso necesario del tubo inferior.|El tubo inferior de la cortina tenía un peso que impedía la subida de la cortina, se decidió retirarlo de la cortina, esto para evitar problemas de peso mayor y que la cortina pueda subir correctamente.|

## Problema técnico encontrado
La cortina bajaba y subía a una velocidad considerablemente acelerada que impedía la detección del primer sensor magnético

## Solución aplicada
Al principio se optó por colocar un imán con un tamaño un poco más grande, sin embargo afectaba al peso de la cortina, por lo que otra solución fue ajustar la estructura tanto del sensor magnético inferior como del sensor magnético superior, dicha solución fue efectiva para el funcionamiento de la cortina. 

## Conexión con el curso
Se aplicó de nueva cuenta el concepto de funcionamiento de los sensores para tener una recapitulación más clara de como podíamos improvisar mejor su funcionamiento, con lo visto las clases pasadas se logró el objetivo de continuar con la reestructuración de los sensores, asimismo se aplicaron los principios básicos de la programación hecha para la interfaz humano-máquina, mejorando la eficacia de la cortina con los fundamentos correctos que necesita para su implementación 


## Autoevaluación
- ⬜ Muy perdido
- ⬜ Con dudas
- 🟩 Entendiendo
- ⬜ Dominando
