# Convención de identificadores

| Tipo de artefacto | Formato | Ejemplo |
|---|---|---|
| Requisito funcional | REQ-F-NNN | REQ-F-003 |
| Requisito no funcional | REQ-N-NNN | REQ-N-001 |
| Caso de uso | CU-NNN | CU-003 |
| Clase | CLS-Nombre | CLS-Prestamo |
| Caso de prueba | PRB-NNN | PRB-005 |
| Solicitud de cambio | CR-NNN | CR-001 |

Los números son correlativos y no se reutilizan.

## Convención de commits
`tipo(ID): descripción`

Tipos: `docs`, `feat`, `test`, `fix`.
Ejemplo: `feat(REQ-F-007): agrega cálculo de multa por retraso`

## Convención de ramas y tags
- `main`: versión estable
- `cr-NNN-descripcion`: rama de trabajo para cada solicitud de cambio
- Tags: `v1.0` (línea base), `v1.1` (con CR-001)
