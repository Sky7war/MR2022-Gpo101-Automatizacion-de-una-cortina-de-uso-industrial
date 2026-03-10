| N° | Condición del sistema | S1 | S2 | S3 | S4 | S5 | S6 | Q1 SUBIR | Q2 BAJAR | Q3 LUZ ROJA | Q4 LUZ VERDE | Interlock aplicado |
|----|-----------------------|----|----|----|----|----|----|----------|----------|-------------|--------------|--------------------|
| 1  |    Sistema en reposo  |  0 |  0 |  0 |  X |  X |  X |    0     |    0     |      0      |       1      |  Sistema Listo     |
| 2  | Cortina completamente arriba  |  X |  X |  X |  1 |  0 |  0 |    0     |    1     |      0      |       1      |  Bloqueo de subida     |
| 3  | Cortina completamente abajo |  X |  X |  X | 0  |  0  |  1  |  1  |   0  |    0   |   1   |  Bloqueo de bajada |
| 4  | Cortina en posición media |  X |  X |  X |  0  |   1 |   0  |  1  |   1   |  0    |   1   |  Movimiento permitido |
| 5  | Objeto detectado (zona insegura) | 1/0 | 1/0 | 1  |  X |  X  |  X |   0   |  0  |  1  |  0 | Paro de seguridad |
| 6  | Zona libre de objetos |  0 |  0 |  0 |  X |  X |  X | según orden | según orden |  0  |  1 | Operación normal | 
| 7  | Orden subir activa |  0 |  0 |  0 |  0 |  X |  0 |  1 |  0  |  0  |  1  | Interlock motor |
| 8  | Orden bajar activa |  0 |  0 |  0 |  0 |  X |  0 |  0 |  1  |  0  |  1  | Interlock motor |
| 9  | Orden subir y bajar simultanea |  X |  X |  X |  X |  X |  X | 0  | 0  |  1  |  0  | Interlock obligatorio |

0 = apagado 
------------
1 = encendido
------------
X = cualquier valor
------------
según orden = depende de la orden del operador o del PLC
------------
