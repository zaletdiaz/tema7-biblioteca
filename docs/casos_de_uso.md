# Casos de uso – v1.1

| ID | Nombre | Actor | Requisito | Cambio |
|---|---|---|---|---|
| CU-001 | Registrar usuario | Bibliotecario | REQ-F-001 | |
| CU-002 | Buscar libro | Estudiante, Docente | REQ-F-002 | |
| CU-003 | Prestar libro | Bibliotecario | REQ-F-003 | Modificado (CR-001) |
| CU-004 | Devolver libro | Bibliotecario | REQ-F-004 | Modificado (CR-001) |
| CU-005 | Reservar libro | Estudiante, Docente | REQ-F-005 | |
| CU-006 | Notificar vencimiento | Sistema | REQ-F-006 | |
| CU-007 | Cobrar multa | Bibliotecario | REQ-F-007 | **Nuevo (CR-001)** |

## CU-003 Prestar libro (modificado)
- **Precondición:** el usuario está registrado y el libro está disponible.
- **Flujo principal:** 1) El bibliotecario ingresa el código del usuario. 2) **El sistema verifica que no tenga multa pendiente.** 3) Ingresa el código del libro. 4) El sistema registra el préstamo y calcula la fecha de vencimiento. 5) Marca el libro como prestado.
- **A1:** libro no disponible → ofrece reservarlo (CU-005).
- **A2 (nuevo):** el usuario tiene multa pendiente → el sistema rechaza el préstamo e indica el monto adeudado.

## CU-004 Devolver libro (modificado)
- **Precondición:** existe un préstamo activo.
- **Flujo principal:** 1) El bibliotecario ingresa el código del libro. 2) El sistema registra la devolución. 3) **Si la fecha de devolución supera la de vencimiento, el sistema calcula la multa (CU-007).** 4) Marca el libro como disponible.
- **A2 (nuevo):** el usuario paga la multa en el momento → se registra el pago y la multa queda como pagada.

## CU-007 Cobrar multa (nuevo)
- **Actor:** Bibliotecario.
- **Precondición:** existe una multa pendiente.
- **Flujo principal:** 1) El bibliotecario consulta las multas del usuario. 2) Registra el pago. 3) El sistema cambia el estado de la multa a "pagada".
