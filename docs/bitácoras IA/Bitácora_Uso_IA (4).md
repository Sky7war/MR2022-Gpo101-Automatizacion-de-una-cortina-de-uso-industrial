```markdown
# Bitácora de Uso de Inteligencia Artificial (IA)

## Información general
- **Equipo:**  
- **Integrantes:**  Daniel Sopeña Zamora, Adolfo Javier Barrientos López, Leopoldo Ramírez Sánchez, Victor Manuel Zamudio Zazueta
- **Semana / Hito:** (H4)  
- **Fecha:**  11/03/2026

---

## 1️⃣ Uso de IA en esta etapa
Marca una opción:

- ⬜ No se utilizó IA en esta etapa  
- 🟩 Sí se utilizó IA de forma puntual  
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

Se utilizó la IA para buscar soluciones acerca de como podemos reducir el peso del tubo inferior para que la cortina tenga un mejor movimiento de subida. 

```

---

## 3️⃣ Herramienta(s) de IA utilizada(s)
Marca las que apliquen:

- 🟩 ChatGPT  
- ⬜ Copilot  
- ⬜ Otra (especificar): ______________________  

---

## 4️⃣ Prompts relevantes utilizados
Copia **solo los prompts más importantes** (no todos).

> Regla: si no puedes mostrar el prompt, no lo declares como uso válido.

**Prompt 1:**
```

En el proyecto de cortina industrial hay un problema, la cortina tardó en subir debido al peso del tubo Diámetros del tubo original Interno 15 mm Externo 21.34 mm ¿Debería cambiarlo por un tubo un poco mas pequeño si consideramos que el tubo de arriba tiene las mismas medidas?

```

**Prompt 2 (opcional):**
```

¿alguna otra alternativa puede ser retirar el tubo y dejar solamente la cortina con el imán? (recordemos que el objetivo es que el imán pase por los sensores magnéticos para que ocurra la apertura y cierre de la cortina)

```

---

## 5️⃣ Respuesta(s) obtenida(s) de la IA
Resume o copia los fragmentos **relevantes** de la respuesta.

```

Sí, puede ser buena idea reducir el diámetro, pero hay que analizar dos cosas importantes en tu caso de la cortina industrial:

1️⃣ Peso del tubo
2️⃣ Rigidez (que no se doble)

En tu proyecto de cortina industrial tipo enrollable (como las que se usan en sistemas automatizados con PLC), el tubo superior funciona como eje de enrollado, por lo que:

Si el tubo es muy pesado, el motor o mecanismo tarda más en subir la cortina.

Si el tubo es muy delgado, puede flexionarse o doblarse por el peso de la cortina.

1. Qué está pasando con tu tubo actual

Tienes:

Diámetro interno: 15 mm

Diámetro externo: 21.34 mm

Espesor de pared:

𝑡
=
21.34
−
15
2
≈
3.17
 mm
t=
2
21.34−15
	​

≈3.17 mm

Es un tubo relativamente grueso, lo que significa:

más peso

más inercia

más torque necesario para girarlo

Por eso la cortina tarda en subir.

2. Si reduces el diámetro

Si cambias a algo como:

Interno: 12 mm

Externo: 16–18 mm

obtienes:

✔ menos masa
✔ menos momento de inercia
✔ el motor lo levanta más rápido

Pero cuidado con:

❌ que el tubo se flexione en el centro.

3. Regla práctica para cortinas enrollables

Para cortinas ligeras/medianas normalmente se usan:

tubos de 16–20 mm de diámetro externo

con pared de 1.5–2 mm

Tu tubo actual (21.34 mm con 3.17 mm de pared) está sobredimensionado para un prototipo.

4. Recomendación para tu proyecto

Yo probaría algo como:

Opción ideal para prototipo

Diámetro externo: 18 mm

Diámetro interno: 14–15 mm

o incluso

Externo: 16 mm

Interno: 12 mm

Eso reduce bastante el peso.

5. Otra solución que casi nadie considera

En proyectos de automatización como el de Flexi (pick-to-light / cortina industrial) también puedes:

✔ cambiar el tubo a aluminio en vez de acero
✔ mantener el mismo diámetro pero reducir peso 60-70%

Esto suele funcionar mejor que bajar el diámetro.

✅ Conclusión:
Sí, puedes usar un tubo más pequeño, pero lo ideal es:

reducir espesor o material antes que reducir demasiado el diámetro

mantener al menos 16–18 mm externo para que no se doble.

Respuesta 2:
Sí, es una alternativa posible, pero depende de cómo esté diseñado el movimiento de la cortina. Vamos a analizarlo como si fuera una decisión de ingeniería para tu proyecto.

1. Quitar el tubo y dejar solo la cortina con el imán

Podría funcionar si el objetivo principal es únicamente que el imán pase frente a los sensores magnéticos para activar:

apertura

cierre

En ese caso, el tubo no es estrictamente necesario.

Ventajas:

✔ reduces mucho el peso
✔ el sistema sube más rápido
✔ el motor o actuador requiere menos torque
✔ simplifica el sistema

2. Problema que puede aparecer

Si quitas el tubo, la cortina puede:

❌ no enrollarse correctamente
❌ subir torcida
❌ arrugarse o atorarse

El tubo normalmente sirve para:

dar rigidez

enrollar la cortina de forma uniforme

3. Alternativa muy usada en automatización

En muchos sistemas industriales se hace esto:

NO se usa un tubo pesado arriba, sino:

una varilla ligera

una barra delgada de aluminio

o solo un refuerzo horizontal

y el imán se coloca en:

la parte inferior de la cortina

Así el sistema funciona como:

cortina tipo persiana simple

4. Solución muy recomendable para tu proyecto

Para tu estación con sensores magnéticos:

Quita el tubo pesado

Coloca un refuerzo ligero (varilla o perfil delgado)

Coloca el imán en la parte inferior de la cortina

Cuando la cortina sube o baja:

el imán pasa por el sensor reed

el PLC detecta posición

Esto reduce muchísimo el esfuerzo del sistema.

5. Cómo se hace en proyectos académicos similares

Se usa:

cortina ligera

imán pequeño de neodimio

sensor reed o hall

motor pequeño o actuador lineal

Es suficiente para demostrar:

control

sensado

automatización

6. Conclusión

Sí, puedes retirar el tubo, pero lo ideal es:

✔ dejar algún refuerzo ligero
✔ mantener tensión en la cortina
✔ colocar el imán en el borde inferior

Así tendrás:

menor peso

movimiento más rápido

sensores funcionando correctamente.

```

---

## 6️⃣ Evaluación crítica del equipo (OBLIGATORIA)

### 6.1 ¿Qué parte fue útil?
```

Los aportes obtenidos de la IA fueron usados como base para implementar nuevas ideas de reestructuración.

```

### 6.2 ¿Qué parte fue incorrecta, incompleta o no aplicable?
```

Hasta el momento algunas ideas propuestas por la IA no fueron descartadas, pues consideramos que las ideas que se propusieron fueron mas acorde a lo que queríamos buscar como equipo. 

```

### 6.3 Decisión final del equipo
Marca y explica:

- ⬜ Se utilizó tal como lo propuso la IA  
- 🟩 Se utilizó parcialmente (adaptado)  
- ⬜ Se rechazó  

**Justificación técnica de la decisión:**
```

Se combinaron las ideas tanto nuestras como las ideas propuestas por la IA, esto nos ayudó a construir de nuevo el modelo adecuado para la cortina, y darnos cuenta de otros detalles que pueden funcionar en el prototipo, mejor que las ideas que llegamos a plantear antes de consultar a la IA. 

```

---

## 7️⃣ Verificación humana (OBLIGATORIA)
Indica **cómo se verificó** la información antes de usarla:

- ⬜ Comparación con apuntes/clase  
- 🟩 Prueba en el sistema real  
- ⬜ Discusión en equipo  
- ⬜ Consulta con el profesor  
- ⬜ Otra: ______________________  

**Evidencia o explicación breve de la verificación:**
```

Después de las ideas propuestas por la IA y al combinarlas con algunas de nuestras ideas, se optó por probar algunas de sus ideas, retiramos el tubo inferior porque el peso afectaba en gran medida a la subida de la cortina, y al reemplazar la estrcutrua con una donde el imán se adhiere a la cortina nos dimos cuenta que el prototipo funcionaba, finalmente realizamos los ajustes estructurales para que el funcionamiento del prototipo fuese el adecuado. 

```

---

## 8️⃣ Impacto del uso de IA en el proyecto
Reflexiona brevemente:

- ¿La IA ahorró tiempo?
- ¿Mejoró la comprensión del problema?
- ¿Introdujo confusión?
- ¿Mejoró la calidad del resultado?

```

La IA nos ayudó a implenetar ideas que estuviesen acorde a lo que se quiere establecer realmente con la cortina, pues tanto nuestras ideas como las ideas de la IA se pudieron fusionar para corregir adecuadamente la estrcutura de la cortina, y que otros cambios podemos hacer para que el prototipo funcione de una mejor manera. 

```

---

## 9️⃣ Aprendizaje del equipo sobre el uso de IA
¿Qué aprendieron sobre **cómo usar (o no usar)** IA en un proyecto de ingeniería?

```

La IA es útil para la implementación de ideas que requieren de una o muchas soluciones, es cuestión también que esas ideas puedan implementarse correctamente en el prototipo y puedan generar un cambio significativo en su composición. 
```

---

## 🔚 Declaración de honestidad
Declaramos que:
- El uso de IA aquí documentado es **veraz y completo**.
- Las decisiones finales fueron tomadas por el equipo.
- La IA fue utilizada como **apoyo**, no como sustituto del criterio ingenieril.

**Firma del equipo (nombres):**
``` Daniel Sopeña Zamora, Adolfo Javier Barrientos López, Leopoldo Ramírez Sánchez, Victor Manuel Zamudio Zazueta


