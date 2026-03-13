# Proyecto Mecatrónico – MR2022

## Problema
La situación problema consiste en realizar un sistema mecatrónico donde se diseña, implementa y valida la automatización de una cortina industrial considerando elementos como seguridad, operación, componentes e interfaz de usuario, controlando cuándo se cierra y abre mediante sensores, mejorando así la eficiencia operativa, reduciendo la intervención manual y aumentando la seguridad del usuario. Además, con la opción de poder configurar parámetros como tiempos y velocidades, garantizando un funcionamiento adaptable a los requerimientos.

## Arquitectura del sistema

<img width="600" height="473" alt="Captura" src="https://github.com/user-attachments/assets/dff8c7f9-7511-44b6-8f18-90622c1e9a6d" />

[Sensores] → [Siemens LOGO] → [Relés] → [Motor DC]

## Componentes utilizados
- Sensor inductivo (LJ12A3-4-Z/BX)
- Sensor capacitivo (LJC18A3-B-Z/BX)
- Sensor óptico (E3F-DS30P1)
- Sensor magnético (FESTO SME-8M-DS-24V-K-2,5-OE)
- Siemens LOGO (12/24 RCE)
- Relevador Industrial HH54P (MY4NJ)
- Motor 24VDC
- Torre de luces (ANDON de 3 colores)

## Lógica de control
En nuestro caso es un funcionamiento cíclico en el cual se encienden los sensores y esto va creando algunas modificaciones en el ciclo, pero este de todas formas se vuelve a iniciar.

1. Al encenderse la cortina lo que hace inmediatamente es detectar en donde se encuentra.
2. Dependiendo del lugar en el que se encuentre sube o baja, según sea el caso.
3. Al terminar de bajar se detiene por 10 segundos antes de volver a subir, pero al subir vuelve a bajar de inmediato.
4. Si se detecta alguna persona o algún material por parte de el motor óptico o inductivo se detiene en el caso de estar bajando y se encienden las luces verde y roja a manera de alerta, pero si está subiendo solo se encienden las luces de alerta.
5. En cualquier caso, si se presiona el sensor capacitivo (botón de emergencia) se detiene por completo la cortina, y se encienden las luces de alerta.

## Resultados de pruebas
Pruebas de detección de sensores y pruebas del sistema.

https://github.com/Sky7war/MR2022-Gpo101-Automatizacion-de-una-cortina-de-uso-industrial/blob/main/docs/H2_Sensores/MR2022_Registro_Pruebas_Sensores_Proximidad.md#mr2022----registro-experimental-de-pruebas-de-sensores-de-proximidad

## Video demo
https://drive.google.com/file/d/1l6njuWS0FrmbVFWxYHiuuphqV2ezXxQm/view?usp=sharing

## Evidencias
https://github.com/Sky7war/MR2022-Gpo101-Automatizacion-de-una-cortina-de-uso-industrial/blob/main/docs/evidencia/README_evidencias.md#evidencias-semanales

## Equipo
Integrantes del proyecto:
- Daniel Sopeña Zamora (A00573479) - @Sky7war
- Adolfo Javier Barrientos López (A00573560) - @Modorfeus
- Victor Manuel Zamudio Zazueta (A00573456) - @vicman-6174
- Leopoldo Ramírez Sánchez (A00574867) - @A00574867
