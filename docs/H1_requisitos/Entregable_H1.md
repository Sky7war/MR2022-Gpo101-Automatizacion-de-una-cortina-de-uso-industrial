# Hito 1 – Análisis y Requerimientos

## Descripción del problema
Diseñar, implementar y validar la automatización de una cortina industrial considerando: operación (modos manual/automático), seguridad (interlocks y respuesta a fallas), selección de componentes (sensores/actuadores) e interfaz de usuario (HMI).

## Requerimientos del sistema
### Funcionales
- Lámpara ANDON, 2 colores para indicar el estado de la cortina (verde: funcionando, rojo: parado).
- Implementación de botones para subir, bajar y parar la cortina.
- Activar motor DC 24V por x segundos cuando se cumplan condiciones.
- Modo automático con ciclo programado de subida, bajada o parar.
- Configuración de parámetros como velocidad o tiempos desde la interfaz HMI.
- Detección de obstáculos cuando la cortina baja.

### Técnicos
- Implementación de un PLC Logo V8 12/24 rce de marca siemens
- Implementación de sensores (infrarrojo, magnético de proximidad, inductivo y capacitivo) para detección de posición y presencia.
- Cableado organizado y seguro
- Motor con engrane 24VDC para la apertura y cierre de la cortina
- Programa basado en el diagrama de bloques

### Seguridad
- Integración de un botón de emergencia que corta la fuente de energía
- Señalización y protección de cables y/o componentes delicados
- Semáforo que indica el comportamiento del sistema
- El motor no se acciona si el sensor reporta condición inválida.

## Diagrama de bloques
![085ea6ac-c8a1-46de-853e-d9e94174b5d2](https://github.com/user-attachments/assets/0afdb905-0b1a-4b25-98d7-ba782ae465a9)


## Conclusiones del análisis
Este análisis nos permite estructurar de una manera más clara los componentes que conforman el proyecto y cómo éstos trabajarán en conjunto dentro del sistema mecatónico de la cortina, ahora bien, esto sienta las bases para poder empezar con pruebas de los componentes, analizando sus parámetros, verificando que cumpla su funcionamiento junto con los demás, configurándolos de tal forma que cumpla con lo esperado. 

