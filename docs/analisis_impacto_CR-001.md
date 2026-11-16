# Análisis de impacto – CR-001

## Impacto por dimensión
| Dimensión | Impacto | Nivel |
|---|---|---|
| Alcance | Se agrega REQ-F-007; se modifican REQ-F-003 y REQ-F-004. Nuevo CU-007; se modifican CU-003 y CU-004. Nueva clase CLS-Multa; se modifican CLS-Prestamo y CLS-Usuario. | Medio |
| Tiempo | 12 horas: análisis (2), modelado (3), documentación (2), pruebas (3), revisión (2). La entrega se extiende 1 día. | Medio |
| Calidad | 3 pruebas nuevas (PRB-010 a PRB-012) y regresión de PRB-004, PRB-005 y PRB-006. | Medio |
| Costo | Sin costo adicional de herramientas; solo horas del equipo. | Bajo |

## Artefactos afectados
| Tipo | Artefactos |
|---|---|
| Requisitos (SRS) | REQ-F-003, REQ-F-004, REQ-F-007 |
| Casos de uso | CU-003, CU-004, CU-007 |
| Clases | CLS-Prestamo, CLS-Usuario, CLS-Multa |
| Pruebas | PRB-004, PRB-005, PRB-006, PRB-010, PRB-011, PRB-012 |

## Riesgos y mitigación
| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| Error en el cálculo de días de retraso | Media | Alto | Pruebas con casos límite (mismo día, 1 día, 30 días) |
| Bloqueo de préstamos por multas mal registradas | Baja | Alto | Regresión sobre CU-003 y anulación de multa por el administrador |
| Inconsistencia entre SRS y modelos UML | Media | Medio | Actualizar primero la matriz y revisar por pares antes del tag |
| Desviación de alcance | Media | Medio | Todo cambio adicional entra como un nuevo CR |

## Decisión
Aprobado. Se implementa en la rama `cr-001-multas` y se publica como v1.1.
