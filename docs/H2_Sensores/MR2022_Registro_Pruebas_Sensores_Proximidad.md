# MR2022 -- Registro Experimental de Pruebas de Sensores de Proximidad

## Curso: Análisis de Elementos de Mecatrónica

## Práctica: Conexión y validación de sensores con Siemens LOGO

## Equipo: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Integrantes: Daniel Sopeña Zamora/Adolfo-Javier Barrientos López Victor/Manuel Zamudio Zazueta/Leopoldo Ramírez Sánchez

## Fecha: 25/02/2026

------------------------------------------------------------------------

# 1️⃣ Identificación del Sensor

# Sensor Inductivo

  |Parámetro                             |Información|
  |------------------------------------- |---------------------------------------------|
|  Tipo de sensor           |             Inductivo|
|  Marca / Modelo                      |  LJ12A3-4-Z/BX |
 | Tipo de salida                       | NPN |
 | Alimentación                         | 6–36 VDC |
 | Distancia nominal (según datasheet)  | 4 mm ± 10% |
 | Tipo de conexión al LOGO             | Digital|
 | Observaciones iniciales              | Detecta solo materiales metálicos. |

------------------------------------------------------------------------

------------------------------------------------------------------------

# Sensor Capacitivo
  
|  Parámetro                          |     Información  |
|  -------------------------------------| ---------------------------------------------|
|  Tipo de sensor                   |     Capacitivo |
|  Marca / Modelo                      |  LJC18A3-B-Z/BX   | 
 | Tipo de salida                     |   NPN |
|  Alimentación                       |   6–36 VDC |
|  Distancia nominal (según datasheet)  | 10 mm (ajustable) |
|  Tipo de conexión al LOGO          |    Digital / Analógica |
 | Observaciones iniciales            |   En algunos materiales no requiere contacto de una superficie.|

------------------------------------------------------------------------

# Sensor Magnético

|  Parámetro                             |Información |
|  ------------------------------------- |--------------------------------------------- |
|  Tipo de sensor                        |Magnético |
|  Marca / Modelo                        |FESTO SME-8M-DS-24V-K-2,5-OE |
|  Tipo de salida                        |PNP |
|  Alimentación                          |10–30 VDC (versión 24V DC) |
|  Distancia nominal (según datasheet)   |(Depende de la potencia del imán) |
|  Tipo de conexión al LOGO              |Digital |
|  Observaciones iniciales               |Dependiendo de la zona del imán tiene un mayor o menor campo magnético por lo que detecta o no en base a eso. |

------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------

# Sensor Óptico

|  Parámetro                    |         Información |
|-------------------------------------|---------------------------------------------|
|  Tipo de sensor                     |   Óptico |
|  Marca / Modelo                      |  E3F-DS30P1 |
|  Tipo de salida                       | PNP |
|  Alimentación                         | 6–36  VDC |
|  Distancia nominal (según datasheet)  | 30 cm (ajustable) |
|  Tipo de conexión al LOGO              | Digital |
|  Observaciones iniciales              | Detecta a distancias largas muchos objetos. |

-------------------------------------------------------------------------------

------------------------------------------------------------------------


# 2️⃣ Resultados por Material Evaluado

> Registrar comportamiento REAL medido en laboratorio.

Sensor inductivo
 | Material |¿Detecta? (Sí/No) |Distancia mínima (mm) |Distancia máxima (mm)|Distancia promedio (mm) |Zona inestable (mm) |Falsas detecciones |Observaciones|   
 |----------|------------------|----------------------|---------------------|------------------------|--------------------|-------------------|-------------|
 |Acero     | Sí | 6.5 mm | 0 mm | 3.5 mm | 6.6 mm | No hay | Es preciso |                                                                           
 |Aluminio |Sí  | 2.5 mm | 0 mm| 1.25 mm  | 2.9 mm | No hay | Está muy bonito |                                                                              
 |Cobre | Sí | 1 mm | 0 mm | 0 mm | 1.1 mm | No hay | Se midió con cable de cobre, no con un objeto rígido |                                                       
 |Plástico | No | NA | NA | NA | NA | NA | NA |                                                                            
 |Madera  | No | NA | NA | NA | NA | NA | NA |                                                                          
 |Vidrio | No | NA | NA | NA | NA | NA | NA |                                                                                 
 |Agua  | No | NA | NA | NA | NA | NA | NA |                                                                                  
 |Imán | Sí | 5 mm | 0 mm | 3 mm | Cuando se acerca mucho a la parte magnética se vuelve muy inestable | No detecta al estar cerca de la parte magnética | El imán altera el campo magnético del inductor y provoca que deje de detectar al acercarse |                                                                                    
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

Sensor capacitivo
 | Material |¿Detecta? (Sí/No) |Distancia mínima (mm) |Distancia máxima (mm)|Distancia promedio (mm) |Zona inestable (mm) |Falsas detecciones |Observaciones|   
 |----------|------------------|----------------------|---------------------|------------------------|--------------------|-------------------|-------------|
 |Acero     | Sí | 7 mm | 0 mm | 3.5 mm | 7.1 mm | No hay | Es preciso |                                                                           
 |Aluminio |Sí  | 8 mm | 0 mm| 4 mm  | 8.1 mm | No hay | Está muy bonito |                                                                              
 |Cobre | Sí | 5 mm | 0 mm | 2.5 mm | 5.1 mm | No hay | Se midió con cable de cobre, no con un objeto tan rígido |                                                 
 |Plástico | No | NA | NA | NA | NA | NA | NA |                                                                            
 |Madera  | Sí | 3 mm | 0 mm | 1.25 mm | 3.1 mm | No hay | Muy estable |                                                                          
 |Vidrio | Sí | 2.5 mm | 0 mm | 1.25 mm | 2.6 mm | No hay | Sí lo detectó en todo punto |                                                                          
 |Agua  | Sí | 6 mm | 0.1 mm | 3 mm | 6.1 | No hay | Sí mide el agua a través de la botella pero no la botella vacía |                                             
 |Imán | Sí | 9 mm | 0 mm | 5 mm | 10 mm | No hay | El imán no altera la detección, porque funciona con capacitor|                                                                                    
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

Sensor magnético
 | Material |¿Detecta? (Sí/No) |Distancia mínima (mm) |Distancia máxima (mm)|Distancia promedio (mm) |Zona inestable (mm) |Falsas detecciones |Observaciones|   
 |----------|------------------|----------------------|---------------------|------------------------|--------------------|-------------------|-------------|
 |Acero     |  No | NA | NA | NA | NA | NA | NA |                                                                             
 |Aluminio | No | NA | NA | NA | NA | NA | NA |                                                                                
 |Cobre |  No | NA | NA | NA | NA | NA | NA |                                                   
 |Plástico | No | NA | NA | NA | NA | NA | NA |                                                                            
 |Madera  |  No | NA | NA | NA | NA | NA | NA |                                                                         
 |Vidrio |  No | NA | NA | NA | NA | NA | NA |                                                                      
 |Agua  |  No | NA | NA | NA | NA | NA | NA |                                             
 |Imán | Sí | 45 mm | 0 mm | 22.5 mm | Detecta bien en las caras de área grande, en las demás es menor | No hay | Entre mayor es el área, mayor es el campo magnético y detecta de mayor distancia|                                                                                    
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

Sensor óptico
| Material |¿Detecta? (Sí/No) |Distancia mínima (mm) |Distancia máxima (mm)|Distancia promedio (mm) |Zona inestable (mm) |Falsas detecciones |Observaciones|   
|----------|--------------|------------------|-----------------|--------------------|-----------------|-------------------|-------------|
|Acero     |  Si | 450 mm | 0 mm | 225 mm | 451 mm | No hay | La detección fue precisa para el sensor, ya que el material cuenta con un tamaño aceptable |            
|Aluminio | Si | 340 mm | 0 mm | 170 mm | 341 mm | No hay | La plataforma se movía constantemente, al equilibrarla el sensor pudo reconocerla con facilidad |  
|Cobre |  Si | 110 mm | 0 mm | 55 mm | 111 mm | No hay | A pesar del tamaño del cable de cobre utilizado para la detección, el sensor logró detectarlo desde una distancia clave y precisa |                                                   
|Plástico | Si | 490 mm | 0 mm | 245 mm | 491 mm | No hay | El tamaño de la plataforma fue aceptable  |                                  
|Madera  | Si | 487 mm | 0 mm | 243.5 mm| 488 mm | No hay | Al igual que el plástico |                                                   
|Vidrio |  Sí | 220 mm | 0 mm | 100 mm | 221 mm | No hay | El vidrio no era transparente por completo |
|Agua  |  Sí | 310 mm | 0 mm | 150 mm | 311 mm | No hay | Solo detectó la parte de la botella llena de agua  |                            
|Imán | Sí | 220 mm | 0 mm | 110 mm | 221 mm | No hay | Igual al vidrio, a pesar de que el material y color de su superficie no eran tan parecidos|       
-----------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

# 3️⃣ Prueba de Distancia Incremental

> Mover el objeto en incrementos regulares y registrar comportamiento
> del LED y del LOGO.

Sensor magnético
  -------------------------------------------------------------------------------
  | Distancia (mm) |  LED del sensor (ON/OFF) |  Entrada en LOGO (1/0) |  ¿Detección consistente? | Comentarios |
  |-----------| ----------------|--------------| --------------------- |-------------|
  | 0 | ON | 1 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición  |            
  | 2 | ON | 1 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |            
  | 4 | ON | 1 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |            
  | 8 | ON | 1 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |        
  | 16 | ON | 1 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |            
  | 20 | ON | 1 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |    
  | 25 | OFF | 0 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |
  | 30 | OFF | 0 | Sí | Se usó un imán diferente al de la primer prueba, un poco menos potente, lo que afecta a la medición |
    -------------------------------------------------------------------------------

Sensor capacitivo
  -------------------------------------------------------------------------------
  | Distancia (mm) |  LED del sensor (ON/OFF) |  Entrada en LOGO (1/0) |  ¿Detección consistente? | Comentarios |
  |-----------| ----------------|--------------| --------------------- |-------------|
  | 0 | ON | 1 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera  |            
  | 2 | ON | 1 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |            
  | 4 | ON | 1 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |            
  | 8 | ON | 1 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |        
  | 12 | OFF | 0 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |            
  | 16 | OFF | 0 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |    
  | 40 | OFF | 0 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |
  | 50 | OFF | 0 | Sí | Se usó en una superficie diferente a las previas, en tela de una cartuchera |
    -------------------------------------------------------------------------------

 Sensor inductivo
  -------------------------------------------------------------------------------
  | Distancia (mm) |  LED del sensor (ON/OFF) |  Entrada en LOGO (1/0) |  ¿Detección consistente? | Comentarios |
  |-----------| ----------------|--------------| --------------------- |-------------|
  | 0 | ON | 0 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |            
  | 2 | ON | 0 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |            
  | 4 | ON | 0 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |            
  | 6 | OFF | 1 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1 |        
  | 8 | OFF | 1 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |            
  | 12 | OFF | 1 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |    
  | 14 | OFF | 1 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |
  | 16 | OFF | 1 | No | Está invertido, cuando no detecta el LOGO marca 0, y cuando sí detecta marca 1  |
    -------------------------------------------------------------------------------
 
 Sensor óptico
  -------------------------------------------------------------------------------
  | Distancia (mm) |  LED del sensor (ON/OFF) |  Entrada en LOGO (1/0) |  ¿Detección consistente? | Comentarios |
  |-----------| ----------------|--------------| --------------------- |-------------|
  | 0 | ON | 1 | Sí | Es el que detecta desde distancias más largas  |            
  | 10 | ON | 1 | Sí | Es el que detecta desde distancias más largas  |            
  | 20 | ON | 1 | Sí | Es el que detecta desde distancias más largas  |            
  | 40 | ON | 1 | Sí | Es el que detecta desde distancias más largas |        
  | 60 | ON | 1 | Sí | Es el que detecta desde distancias más largas  |            
  | 100 | ON | 1 | Sí | Es el que detecta desde distancias más largas  |    
  | 200 | ON | 1 | Sí | Es el que detecta desde distancias más largas  |
  | 500 | OFF | 0 | Sí | Es el que detecta desde distancias más largas  |
    -------------------------------------------------------------------------------

*(Ajustar rango según especificación del sensor)*

------------------------------------------------------------------------

# 4️⃣ Comparación vs Especificación del Fabricante

|  Parámetro                       |  Valor Datasheet |  Valor Experimental |  Error (%) |
|  --------------------------------- | ----------------- | -------------------- | ----------- |
|  Distancia nominal del sensor magnético |   NA | NA | NA |
|  Distancia nominal del sensor capacitivo | 10 mm | 9 mm | 10% |
|  Distancia nominal del sensor inductivo | 4 mm | 6.5 mm | 62.5% |
|  Distancia nominal del sensor óptico | 300 mm | 450 mm | 50% |
|  Tiempo de respuesta (si aplica)  | NA en ninguno | NA en ninguno | NA en ninguno |                                        
------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------

| Sensor | Tipo de material recomendado |  
| ------ | ---------------------------- |
| Magnético | Imanes |
| Capacitivo | Materiales metálicos y sólidos |
| Inductivo | Metálicos |
| Óptico | Objetos no transparentes |
------------------------------------------------------------------------
------------------------------------------------------------------------

# 5️⃣ Análisis Técnico del Equipo

## 5.1 ¿Coincide la distancia real con la nominal?

Respuesta:
En el caso del magnético, esta distancia es bastante variable por la potencia del imán, como se mostró en su distancia máxima al cambiar los imanes, por su parte en el sensor capacitivo hubo una pequeña diferencia a favor de la medición experimental, mientras que en el inductivo la diferencia sí es mucho más grande, sin embargo no es tan descabellado debido a que son distancias muy pequeñas, y, por último, el sensor óptico también tuvo una gran diferencia, sin embargo no es tan raro debido a que la distancia de medición es ajustable, y la de 300 mm era la predeterminada, pero podría haberse calibrado un poco diferente el que nosotros tenemos.

## 5.2 ¿Qué fenómeno físico explica el comportamiento observado?

(Ejemplo: corrientes de Foucault, constante dieléctrica, reflexión
óptica, campo magnético)

Respuesta:
- El fenómeno físico que explica los cambios de distancia de medición en los sensores magnéticos es el campo magnético, lo cual explica que cada imán tiene un campo magnético diferente, y su geometría provoca que el campo también cambie, en donde hay un mayor campo magnético es en el centro de las caras, y en las caras que abarcan mayor área.
- El sensor óptico batalla detectando objetos transparentes por su transmitancia óptica, el plástico o vidrio puede desviar el haz de luz del sensor por refracción, lo que hace que el receptor no la capte de nuevo y no detecte presencia de un objeto.
- El sensor inductivo funciona mediante una bobina, cuando el metal se acerca se generan corriente (Corrientes de Foucault) que consumen energía del campo, y el sensor detecta esta pérdida, al acercar un imán su campo magnético interfiere saturando el núcleo, lo que impide que la bobina oscile y se presente un "error".
- El sensor capacitivo detecta cambios en la capacitancia del sistema, donde el sensor funciona como una placa del capacitor y el objeto detectado funciona como dieléctrico, pero cuando la constante dieléctrica de este material es muy baja, no se detecta un gran cambio en la capacitancia, ergo, no se detecta el objeto, como puede pasar con el plástico.     

## 5.3 ¿Qué materiales generan mejor desempeño? ¿Por qué?

Respuesta:
- Para los magnéticos únicamente los imanes, porque funcionan con el campo magnético del objeto detectado.
- Para los ópticos, cualquier objeto que sea de un color sólido, porque reflejará el haz de luz sin desviarlo.
- Para los inductivos, los objetos metálicos son la mejor opción porque son los que consumen energía del campo.
- Para los capacitivos, los mejores objetos serían los que tengan una constante dieléctrica alta, como los metales, agua y otros materiales diferentes al plástico.   

## 5.4 ¿Detectaron zonas muertas o inestabilidad?

Respuesta:
Sí, las más evidentes e importantes son la falla en el sensor inductivo al acercar imanes y la nula detección de plástico por parte del capacitivo, sin embargo, contemplando la investigación y los materiales para los que se debe hacer, se vió bastante congruencia entre el funcionamiento que registramos y el material y precisión con la que se esperaría por parte de estos sensores.  

## 5.5 ¿Este sensor sería adecuado para la situación problema del curso?

Justificar técnica y económicamente.

Respuesta:
- Inductivo: Sí sería adecuado pues garantiza que el motor se detenga con precisión al detectar in marco metálico y es el más barato en cuestión de precio y mantenimiento.
- Capacitivo: No sería adecuado debido a que es muy sensible y necesita mucho mantenimiento, a pesar de no ser un sensor relativamente caro.
- Magnético: Sí sería adecuado para reforzar la seguridad de la cortina y confirmar que esté cerrada y bloqueada, además de ser muy económico y duradero.
- Óptico: Sí es adecuado porque es capaz de detectar una persona y actúa como "protección" para evitar accidentes, solo que es muy costoso pero nada vale más que la seguridad
------------------------------------------------------------------------

# 6️⃣ Matriz de Decisión Técnica

  ----------------------------------------------------------------------------
  Criterio      Peso (1--5)  Evaluación del sensor (1--5) Resultado ponderado
  ------------- ------------ ---------------------------- --------------------
  Precisión                                               

  Distancia                                               
  útil                                                    

  Robustez                                                
  industrial                                              

  Inmunidad a                                             
  ruido                                                   

  Costo                                                   

  Facilidad de                                            
  integración                                             
  con LOGO                                                

  **TOTAL**                                               
  ----------------------------------------------------------------------------

------------------------------------------------------------------------

# 7️⃣ Conclusión Ingenieril

Redactar una conclusión técnica defendible:

-   ¿Recomendarían este sensor?
-   ¿En qué condiciones sí?
-   ¿En qué condiciones no?
-   ¿Qué riesgos industriales identifican?

Conclusión:
En base a la evaluación de la matriz podemos concluir que los sensores ópticos serán los más recomendables a utilizar para el proyecto de la cortina industrial ya que destacan en la mayoría de los criterios presentados, siendo bastante útiles en las condiciones requeridas de la situación problema al ser un espacio cerrado y controlado.

Sin embargo, para aplicaciones más complejas y en entornos con más variables presentes como humedad, suciedad, vibraciones, entre otros, se requerirían componentes de mejor calidad y alcance para un funcionamiento más eficiente y profesional, y así, evitar riesgos como cortocircuitos o fallos en la detección de elementos en el área industrial.

------------------------------------------------------------------------

# 8️⃣ Evidencia

-   Fotografías del montaje:
-   Capturas del programa en LOGO:
-   Video corto de funcionamiento:
-   Datasheet utilizado (link o archivo en repositorio):

------------------------------------------------------------------------

# 9️⃣ Bitácora de Aprendizaje

¿Qué aprendieron técnicamente sobre sensores de proximidad que no sabían
antes?

Respuesta:

------------------------------------------------------------------------

> ⚙️ Este documento forma parte del proceso de validación experimental
> para la selección de sensores dentro del proyecto integrador MR2022.
