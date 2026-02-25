# MR2022 -- Registro Experimental de Pruebas de Sensores de Proximidad

## Curso: Análisis de Elementos de Mecatrónica

## Práctica: Conexión y validación de sensores con Siemens LOGO

## Equipo: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Integrantes: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## Fecha: 25/02/2026

------------------------------------------------------------------------

# 1️⃣ Identificación del Sensor

  Parámetro                             Información
  ------------------------------------- ---------------------------------------------
  Tipo de sensor                        Inductivo / Capacitivo / Óptico / Magnético
  Marca / Modelo                        
  Tipo de salida                        PNP / NPN / Relé
  Alimentación                          
  Distancia nominal (según datasheet)   
  Tipo de conexión al LOGO              Digital / Analógica
  Observaciones iniciales               

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
 |----------|------------------|----------------------|---------------------|------------------------|--------------------|-------------------|-------------|
 |Acero     |  Si | 450 mm | 0 mm | 225 mm | NA | 0.1 mm | La detección fue precisa para el sensor, ya que el material cuenta con un tamaño aceptable |            
 |Aluminio | Si | 340 mm | 0 mm | 170 mm | NA | 0.1 mm | La plataforma se movía constantemente, al equilibrarla el sensor pudo reconocerla con facilidad |  
 |Cobre |  Si | 110 mm | 0 mm | 55 mm | NA | 0.1 mm | A pesar del tamaño del cable de cobre utilizado para la detección, el sensor logró detectarlo desde una distancia clave y precisa |                                                   
 |Plástico | Si | 490 mm | 0 mm | 245 mm | NA | 0.1 mm | El tamaño de la plataforma fue aceptable  |                                                               
 |Madera  | Si | 487 mm | 0 mm | 243.5 mm| NA | 0.1 mm | Al igual que el  |                                                                         
 |Vidrio |  Sí | 220 mm | 0 mm | NA | NA | NA | NA |                                                                      
 |Agua  |  Sí | 310 mm | 0 mm | NA | NA | NA | NA |                                             
 |Imán | Sí | 220 mm | 0 mm | 22.5 mm | Detecta bien en las caras de área grande, en las demás es menor | No hay | Entre mayor es el área, mayor es el campo magnético y detecta de mayor distancia|                                                                                    
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

# 3️⃣ Prueba de Distancia Incremental

> Mover el objeto en incrementos regulares y registrar comportamiento
> del LED y del LOGO.

  -------------------------------------------------------------------------------
  Distancia   LED del sensor   Entrada en     ¿Detección            Comentarios
  (mm)        (ON/OFF)         LOGO (1/0)     consistente? (Sí/No)  
  ----------- ---------------- -------------- --------------------- -------------
  0                                                                 

  2                                                                 

  4                                                                 

  6                                                                 

  8                                                                 

  10                                                                

  12                                                                

  14                                                                

  16                                                                
  -------------------------------------------------------------------------------

*(Ajustar rango según especificación del sensor)*

------------------------------------------------------------------------

# 4️⃣ Comparación vs Especificación del Fabricante

  Parámetro                         Valor Datasheet   Valor Experimental   Error (%)
  --------------------------------- ----------------- -------------------- -----------
  Distancia nominal                                                        
  Tiempo de respuesta (si aplica)                                          
  Tipo de material recomendado                                             

------------------------------------------------------------------------

# 5️⃣ Análisis Técnico del Equipo

## 5.1 ¿Coincide la distancia real con la nominal?

Respuesta:

------------------------------------------------------------------------

## 5.2 ¿Qué fenómeno físico explica el comportamiento observado?

(Ejemplo: corrientes de Foucault, constante dieléctrica, reflexión
óptica, campo magnético)

Respuesta:

------------------------------------------------------------------------

## 5.3 ¿Qué materiales generan mejor desempeño? ¿Por qué?

Respuesta:

------------------------------------------------------------------------

## 5.4 ¿Detectaron zonas muertas o inestabilidad?

Respuesta:

------------------------------------------------------------------------

## 5.5 ¿Este sensor sería adecuado para la situación problema del curso?

Justificar técnica y económicamente.

Respuesta:

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
