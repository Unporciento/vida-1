# Laboratorio — Especificación base

## Propósito

Laboratorio es un módulo interno para mantener, diagnosticar y evolucionar Vida 1% durante toda su vida útil. No es un panel para programadores ni parte de la experiencia habitual del usuario.

Su salida principal es un informe claro, reproducible y en texto plano que cualquier IA pueda interpretar.

## Principios de seguridad

- Nunca modifica datos automáticamente.
- Nunca elimina información.
- Nunca ejecuta reparaciones sin autorización expresa.
- Nunca envía información a Internet sin consentimiento.
- Primero diagnostica; después propone; finalmente repara solo si el usuario lo autoriza.

## Diagnósticos mínimos

El diseño futuro debe revisar, cuando aplique:

- Errores JavaScript y promesas rechazadas.
- Service Worker, recursos que no cargan y errores HTTP.
- IndexedDB, LocalStorage, SessionStorage y Cache Storage.
- Sincronización, conectividad, estado offline y permisos.
- Memoria aproximada, tiempo de carga y espacio utilizado.
- Módulos no inicializados y componentes con estado inconsistente.
- Archivos, configuraciones o dependencias importantes ausentes o incompatibles.
- Versiones internas y compatibilidad del navegador.

Vida 1% podrá añadir diagnósticos propios de sus módulos.

## Informe de diagnóstico

Se generará siempre como texto plano e incluirá:

- Nombre del proyecto, versión y fecha.
- Navegador, sistema operativo y URL.
- Estado general, errores y advertencias.
- Módulos cargados y módulos con fallo.
- Rendimiento básico, almacenamiento y Service Worker.
- Últimos eventos importantes.
- Posible causa, cuando sea razonablemente deducible.
- Pasos para reproducir y recomendaciones.

La interfaz incluirá el botón **Copiar informe de diagnóstico**, que copiará el informe íntegro al portapapeles.

## Estado de salud

Laboratorio calculará un estado general mediante comprobaciones reales y ponderadas; nunca será aleatorio. La presentación seguirá esta escala orientativa:

| Estado | Rango orientativo |
| --- | --- |
| 🟢 Excelente | 90–100 |
| 🟡 Atención | 70–89 |
| 🔴 Revisión necesaria | 0–69 |

La fórmula, las comprobaciones y sus pesos deberán documentarse al implementar el módulo.

## Registro histórico

Conservará un historial de diagnósticos para comparar cuándo apareció o desapareció un problema y qué versión lo resolvió. El historial respetará las reglas de privacidad y no se enviará fuera del dispositivo sin consentimiento.

## Criterio de diseño

Laboratorio existe para hacer los errores fáciles de encontrar, comprender y resolver; no para ocultarlos.

