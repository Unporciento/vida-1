# Estándar de desarrollo eficiente

## Propósito

Construir Vida 1% de forma compacta y clara, reduciendo consumo de contexto, tiempo y tokens sin perder calidad, seguridad, estabilidad ni documentación.

## Memoria y documentación

- La memoria principal del proyecto es `README.md`, `AI_HANDOFF.md`, `CHANGELOG.md` y la documentación de arquitectura.
- No se repite la historia completa del proyecto en cada respuesta.
- Cada documento tiene una responsabilidad clara; no se copia el mismo contenido en varios documentos.
- Antes de actuar, se comprende la documentación existente y no se vuelven a preguntar decisiones ya registradas.

## Cambios y revisión

- Revisar a fondo solo los archivos modificados y sus dependencias directas.
- Reservar auditorías completas para migraciones, cambios de seguridad, releases, problemas graves e hitos importantes.
- No reescribir módulos estables sin una razón comprobable.
- No implementar varias fases grandes en un mismo commit.
- Cada módulo tendrá su propia rama, commit y validación.
- Mantener los archivos bajo 400 líneas, salvo una excepción documentada.

## Pruebas y verificación

- Añadir pruebas solo para comportamientos nuevos o regresiones reales.
- No crear pruebas duplicadas ni eliminar pruebas útiles para ahorrar tokens.
- Usar `verify:quick` durante el desarrollo.
- Ejecutar la verificación completa antes de publicar.
- No sacrificar seguridad, reversión, pruebas ni estabilidad para ahorrar recursos.

## Producto y compatibilidad

- Mantener compatibilidad con PC e iPhone.
- Mantener el Módulo UX y la identidad visual separados de las funciones principales.
- Laboratorio es un requisito futuro; no se implementa antes de su fase.

## Formato de cierre

Los reportes finales deben ser breves e indicar:

1. Resultado.
2. Cambios principales.
3. Pruebas aprobadas.
4. Archivos relevantes.
5. Rama y commit.
6. Riesgos.
7. Checklist manual de un máximo de cinco pasos.

