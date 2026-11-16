# Casos de uso – v1.0

| ID | Nombre | Actor | Requisito | Descripción breve |
|---|---|---|---|---|
| CU-001 | Registrar usuario | Bibliotecario | REQ-F-001 | Registra los datos de un estudiante o docente. |
| CU-002 | Buscar libro | Estudiante, Docente | REQ-F-002 | Busca libros por título, autor o código. |
| CU-003 | Prestar libro | Bibliotecario | REQ-F-003 | Registra el préstamo de un libro disponible a un usuario. |
| CU-004 | Devolver libro | Bibliotecario | REQ-F-004 | Registra la devolución y actualiza la disponibilidad del libro. |
| CU-005 | Reservar libro | Estudiante, Docente | REQ-F-005 | Reserva un libro que no está disponible. |
| CU-006 | Notificar vencimiento | Sistema | REQ-F-006 | Envía aviso antes de la fecha de vencimiento del préstamo. |

## Detalle de CU-003 Prestar libro
- **Precondición:** el usuario está registrado y el libro está disponible.
- **Flujo principal:** 1) El bibliotecario ingresa el código del usuario. 2) Ingresa el código del libro. 3) El sistema registra el préstamo y calcula la fecha de vencimiento. 4) El sistema marca el libro como prestado.
- **Flujo alterno A1:** el libro no está disponible → el sistema ofrece reservarlo (CU-005).

## Detalle de CU-004 Devolver libro
- **Precondición:** existe un préstamo activo.
- **Flujo principal:** 1) El bibliotecario ingresa el código del libro. 2) El sistema registra la devolución. 3) El sistema marca el libro como disponible.
