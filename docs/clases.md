# Clases del sistema – v1.1

| Clase | Atributos principales | Métodos principales | Cambio |
|---|---|---|---|
| CLS-Usuario | idUsuario, nombre, tipo, correo | registrar(), **tieneMultaPendiente()** | Modificada |
| CLS-Libro | codigo, titulo, autor, estado | buscar(), cambiarEstado() | |
| CLS-Catalogo | libros | buscarPorTitulo(), buscarPorAutor(), buscarPorCodigo() | |
| CLS-Prestamo | idPrestamo, fechaPrestamo, fechaVencimiento, fechaDevolucion | registrar(), registrarDevolucion(), **calcularMulta()** | Modificada |
| CLS-Reserva | idReserva, fechaReserva, estado | reservar(), cancelar() | |
| CLS-Notificador | medio | enviarAviso() | |
| **CLS-Multa** | idMulta, monto, diasRetraso, estado, fechaPago | generar(), registrarPago() | **Nueva** |

## Relaciones nuevas
- Prestamo 1 — 0..1 Multa
- Usuario 1 — 0..* Multa
