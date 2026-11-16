# Casos de prueba – v1.1

| ID | Requisito | CU | Descripción | Datos de entrada | Resultado esperado |
|---|---|---|---|---|---|
| PRB-001 | REQ-F-001 | CU-001 | Registrar un usuario con datos válidos | Nombre, tipo, correo | Usuario registrado |
| PRB-002 | REQ-F-001 | CU-001 | Registrar un usuario sin nombre | Nombre vacío | El sistema muestra error |
| PRB-003 | REQ-F-002 | CU-002 | Buscar libro por título existente | Título: "Ingeniería de Software" | Se muestra el libro |
| PRB-004 | REQ-F-003 | CU-003 | Prestar un libro disponible (regresión) | Usuario sin multa, libro disponible | Préstamo registrado |
| PRB-005 | REQ-F-003 | CU-003 | Prestar un libro no disponible (regresión) | Libro ya prestado | Rechaza y ofrece reservar |
| PRB-006 | REQ-F-004 | CU-004 | Devolver un libro prestado (regresión) | Código del libro | Libro disponible |
| PRB-007 | REQ-F-005 | CU-005 | Reservar un libro no disponible | Usuario válido, libro prestado | Reserva registrada |
| PRB-008 | REQ-F-006 | CU-006 | Notificar un día antes del vencimiento | Préstamo con vencimiento mañana | Aviso enviado |
| PRB-009 | REQ-N-001 | transversal | Medir el tiempo de una búsqueda | Búsqueda en el catálogo | Respuesta menor a 3 s |
| PRB-010 | REQ-F-004, REQ-F-007 | CU-004, CU-007 | Devolver con 3 días de retraso | Vencimiento 10/11, devolución 13/11 | Multa de S/ 3.00 |
| PRB-011 | REQ-F-004, REQ-F-007 | CU-004, CU-007 | Devolver dentro del plazo | Devolución antes del vencimiento | No se genera multa |
| PRB-012 | REQ-F-003, REQ-F-007 | CU-003, CU-007 | Prestar a usuario con multa pendiente | Usuario con multa de S/ 3.00 | El sistema rechaza el préstamo |
