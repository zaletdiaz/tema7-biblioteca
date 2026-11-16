# Clases del sistema – v1.0

| Clase | Atributos principales | Métodos principales |
|---|---|---|
| CLS-Usuario | idUsuario, nombre, tipo, correo | registrar() |
| CLS-Libro | codigo, titulo, autor, estado | buscar(), cambiarEstado() |
| CLS-Catalogo | libros | buscarPorTitulo(), buscarPorAutor(), buscarPorCodigo() |
| CLS-Prestamo | idPrestamo, fechaPrestamo, fechaVencimiento, fechaDevolucion | registrar(), registrarDevolucion() |
| CLS-Reserva | idReserva, fechaReserva, estado | reservar(), cancelar() |
| CLS-Notificador | medio | enviarAviso() |

## Relaciones
- Usuario 1 — 0..* Prestamo
- Libro 1 — 0..* Prestamo
- Usuario 1 — 0..* Reserva
- Libro 1 — 0..* Reserva
- Catalogo 1 — 0..* Libro
- Notificador usa Prestamo
