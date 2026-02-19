```markdown
# Bitácora de Uso de Inteligencia Artificial (IA)

## Información general
- **Equipo:**  
- **Integrantes: Daniel Sopeña Zamora, Adolfo Javier Barrientos López, Leopoldo Ramírez Sánchez, Victor Manuel Zamudio Zazueta 
- **Semana / Hito:** (H1)  
- **Fecha: 18/02/26

---

## 1️⃣ Uso de IA en esta etapa
Marca una opción:

- ⬜ No se utilizó IA en esta etapa  
- ✅ Sí se utilizó IA de forma puntual  
- ⬜ Sí se utilizó IA de forma recurrente  

> ⚠️ Si marcas “No se utilizó IA”, completa únicamente las secciones 7, 8 y 9.

---

## 2️⃣ Objetivo del uso de IA
Describe **para qué** se utilizó la IA (no qué herramienta).

Ejemplos:
- Comprender un concepto técnico
- Generar alternativas de diseño
- Revisar redacción técnica
- Proponer estructura de pruebas
- Detectar errores lógicos

**Descripción del objetivo:**
```

La IA se utilizó para la generación de ideas para encontrar soluciones más óptimas acorde a lo que queremos buscar como objetivo principal para la cortina, se utilizó también para buscar una comprensión de varios términos útiles para la investigación, tratando de buscar un significado que esté acorde a lo que queremos definir correctamente para este proyecto. 

```

---

## 3️⃣ Herramienta(s) de IA utilizada(s)
Marca las que apliquen:

- ✅ ChatGPT  
- ⬜ Copilot  
- ✅ Otra (especificar): _Gemini_  

---

## 4️⃣ Prompts relevantes utilizados
Copia **solo los prompts más importantes** (no todos).

> Regla: si no puedes mostrar el prompt, no lo declares como uso válido.

**Prompt 1:**
```

Crea 10 ejemplos de requisitos de seguridad para una cortina industrial que funciona con un plc LOGO con clemas
(imagen adjuntada del diagrama)
```

**Prompt 2 (opcional):**
```

En base a la tabla de entradas y al esquemático que te mandé, existen salidas para este sistema?
(Imagen adjunta)

```

---

## 5️⃣ Respuesta(s) obtenida(s) de la IA
Resume o copia los fragmentos **relevantes** de la respuesta.

```

Estás trabajando con un Siemens LOGO! alimentado con 24VDC, con entradas I1–I8 y salidas Q1–Q4 cableadas a sensores y actuadores (S1–S8).
Veo que tienes:

Sensores capacitivos e inductivos

Sensores magnéticos (cortina arriba/medio/abajo)

Salidas con protección

Clemas distribuidoras de 24V y 0V

Ahora sí, te actualizo los 10 requisitos de seguridad completamente alineados a TU esquema real 👇

🛑 Requisitos de Seguridad – Cortina con LOGO! y Clemas (Versión Ajustada al Diagrama)
1️⃣ Estado seguro al energizar

RS-01: Al aplicar alimentación 24VDC al PLC, todas las salidas Q1–Q4 deberán iniciar en estado desactivado.

2️⃣ Interbloqueo de salidas

RS-02: El sistema no deberá activar simultáneamente Q1 (subir) y Q2 (bajar).

(Protección del motor y relevadores)

3️⃣ Supervisión de sensor magnético superior

RS-03: Si el sensor S4 (Cortina ARRIBA) está activo, el sistema deberá bloquear cualquier orden de subida.

4️⃣ Supervisión de sensor magnético inferior

RS-04: Si el sensor S6 (Cortina ABAJO) está activo, el sistema deberá bloquear cualquier orden de bajada.

5️⃣ Protección por tiempo de recorrido

RS-05: Si después de activar una orden de movimiento no se detecta cambio en los sensores S4, S5 o S6 dentro del tiempo esperado, el PLC deberá desactivar el motor.

6️⃣ Bloqueo por falla de sensor crítico

RS-06: Si los sensores S4 y S6 se detectan activos simultáneamente, el sistema deberá entrar en estado de bloqueo.

(Condición físicamente imposible → error lógico)

7️⃣ Protección ante activación permanente

RS-07: Si el sensor capacitivo (S1) permanece activado por más de X segundos, el sistema no deberá mantener movimiento continuo.

8️⃣ Reinicio controlado

RS-08: Después de una interrupción de energía, el sistema deberá requerir una nueva señal válida para iniciar movimiento.

9️⃣ Separación de potencia y señal

RS-09: El cableado de las salidas Q1–Q4 deberá estar separado físicamente del cableado de entradas I1–I8 en las clemas.

🔟 Estado seguro ante pérdida de señal

RS-10: Si durante el movimiento se pierde la señal de alimentación de sensores, el PLC deberá desactivar las salidas de movimiento.


PROMPT 2
Exactamente. Con base en las imágenes y la lista que compartiste, no tienes ninguna salida configurada en esta versión (v1).

Esto se confirma por dos cosas en tu diagrama:

En tu lista de texto: Solo defines sensores (S1 a S6). Los sensores son dispositivos de entrada porque le envían información al PLC (a los bornes I1 a I6). No hay ninguna mención de motores, luces, válvulas o contactores, que serían las salidas.

En tu esquemático: Todos los cables llegan a la parte superior del módulo LOGO! (donde están las entradas "I"). La parte inferior del módulo, que es donde se encuentran los bornes de salida (marcados típicamente como Q1, Q2, Q3, Q4...), está completamente vacía y sin conexiones.
```
---

## 6️⃣ Evaluación crítica del equipo (OBLIGATORIA)

### 6.1 ¿Qué parte fue útil?
```

Algunas ideas que fueron generadas por la IA fueron de gran ayuda y sirvieron de mucha inspiración para varios puntos importantes que hemos querido agregar a este trabajo inicial, algunas ideas nos sirvieron para comprender mejor los temas que se pudieron analizar a gran detalle tanto en los requisitos como en los valores de entrada y de salida, el uso de la IA para investigar complementó en gran medida el aprendizaje del equipo, y fue una herramienta clave para el análisis conceptual de lo que se está realizando en este proyecto.

```

### 6.2 ¿Qué parte fue incorrecta, incompleta o no aplicable?
```

La parte de la función de los actuadores y los bornes de salidas aún no son aplicables para este trabajo

```

### 6.3 Decisión final del equipo
Marca y explica:

- ⬜ Se utilizó tal como lo propuso la IA  
- ✅ Se utilizó parcialmente (adaptado)  
- ⬜ Se rechazó  

**Justificación técnica de la decisión:**
```

Dentro de los resultados encontramos diferentes partes las cuales no eran aplicables para esta fase del proyecto, al igual que datos que simplemente no eran relevantes en lo absoluto para el entregable

```

---

## 7️⃣ Verificación humana (OBLIGATORIA)
Indica **cómo se verificó** la información antes de usarla:

- ⬜ Comparación con apuntes/clase  
- ⬜ Prueba en el sistema real  
- ✅ Discusión en equipo  
- ⬜ Consulta con el profesor  
- ⬜ Otra: ______________________  

**Evidencia o explicación breve de la verificación:**
```

Revisamos y corroboramos entre todos los resultados de cada persona para confirmar que íbamos bien y que concordábamos con los resultados obtenidos.
Las ideas que fueron propuestas por la IA fueron de gran utilidad para el equipo, pues al ser una herramienta con un conocimiento enorme se aprovecharon los recursos generativos que ofrece para buscar nuevas ideas y formas de optimizar nuestro trabajo basados en los conceptos que ofrece, aunque también optamos por usar otros recursos como páginas web que ofrecían un contenido amplio y accesible, a diferencia de la IA, las ideas que propusieron ambos recursos fueron importantes para la creación de este proyecto.

```

---

## 8️⃣ Impacto del uso de IA en el proyecto
Reflexiona brevemente:

- ¿La IA ahorró tiempo?
- ¿Mejoró la comprensión del problema?
- ¿Introdujo confusión?
- ¿Mejoró la calidad del resultado?

```

Nos ahorró tiempo y nos ayudó a comprender mejor nuestros resultados del diagrama, además de mejorar la comprensión en parte del problema
Como equipo trabajamos en como podíamos buscar las soluciones de manera verídica apoyándonos tanto en la IA como en las páginas web, asimismo verificamos que lo que hacíamos era lo correcto, al inicio de la verificación se utilizaron las ideas mas acertadas a lo que fue generado por IA, esas ideas crearon una conexión con los conceptos de este proyecto, y fueron modificadas para que existiera una validación de ideas acorde a lo que se está trabajando.
```

---

## 9️⃣ Aprendizaje del equipo sobre el uso de IA
¿Qué aprendieron sobre **cómo usar (o no usar)** IA en un proyecto de ingeniería?

```

Aprendimos que no toda la información que nos da la IA se puede usar en el momento, tenemos que ser selectivos al momento de realizar los prompts 
y ser más específicos con nuestras solicitudes, además de no solo copiar y pegar los resultaods sino corroborar que estén correctos y tengan coherencia

```

---

## 🔚 Declaración de honestidad
Declaramos que:
- El uso de IA aquí documentado es **veraz y completo**.
- Las decisiones finales fueron tomadas por el equipo.
- La IA fue utilizada como **apoyo**, no como sustituto del criterio ingenieril.

**Firma del equipo (nombres):**
` Daniel Sopeña Zamora, Adolfo Javier Barrientos López, Leopoldo Ramírez Sánchez, Victor Manuel Zamudio Zazueta 


