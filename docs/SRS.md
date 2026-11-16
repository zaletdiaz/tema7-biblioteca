# SRS – Sistema de Gestión de Biblioteca Universitaria
**Versión:** 1.1 (incluye CR-001)

## 1. Propósito
Gestionar el catálogo, los usuarios, los préstamos y las multas de la biblioteca universitaria.

## 2. Actores
Estudiante, Docente, Bibliotecario.

## 3. Requisitos funcionales
| ID | Requisito | Prioridad | Cambio |
|---|---|---|---|
| REQ-F-001 | El sistema debe registrar usuarios (estudiantes y docentes). | Alta | |
| REQ-F-002 | El sistema debe buscar libros por título, autor o código. | Alta | |
| REQ-F-003 | El sistema debe registrar el préstamo de un libro disponible, siempre que el usuario **no tenga multa pendiente**. | Alta | Modificado (CR-001) |
| REQ-F-004 | El sistema debe registrar la devolución de un libro y, si es posterior a la fecha de vencimiento, **calcular la multa** correspondiente. | Alta | Modificado (CR-001) |
| REQ-F-005 | El sistema debe permitir reservar un libro no disponible. | Media | |
| REQ-F-006 | El sistema debe notificar la fecha de vencimiento del préstamo. | Media | |
| REQ-F-007 | El sistema debe registrar y cobrar multas de S/ 1.00 por día de retraso. | Alta | **Nuevo (CR-001)** |

## 4. Requisitos no funcionales
| ID | Requisito | Prioridad |
|---|---|---|
| REQ-N-001 | El sistema debe responder las consultas en menos de 3 segundos. | Media |
