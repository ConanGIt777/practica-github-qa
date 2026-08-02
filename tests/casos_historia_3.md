# Casos de Prueba – Historia 3: Calendario de Riego

**Historia de usuario:** Como usuario, quiero ver un calendario visual con fechas de riego y cosecha marcadas para no olvidar las tareas de mantenimiento.

**Criterios de aceptación:**
- Los días de riego deben aparecer en color azul y cosecha en verde.
- El usuario debe poder cambiar de mes en el calendario.
- Las fechas pasadas deben mostrarse deshabilitadas/gris.

---

## TC-005 – Visualización correcta de colores por tipo de evento y navegación entre meses

- **Objetivo:** Validar que el calendario muestra los días de riego en azul, los de cosecha en verde, y que el usuario puede cambiar de mes correctamente.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - Existen eventos de riego y de cosecha programados para el mes actual y el mes siguiente.
- **Datos de prueba:**
  - Evento de riego: `05/08/2026`
  - Evento de cosecha: `20/08/2026`
- **Pasos:**
  1. Ingresar a la sección "Calendario de riego".
  2. Verificar que el día `05/08/2026` (riego) se muestra en color azul.
  3. Verificar que el día `20/08/2026` (cosecha) se muestra en color verde.
  4. Presionar el botón/flecha para avanzar al siguiente mes.
- **Resultado esperado:** Los colores de los días coinciden con el tipo de evento (azul = riego, verde = cosecha) y el calendario navega correctamente al mes siguiente, mostrando sus propios eventos.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-006 – Fechas pasadas mostradas como deshabilitadas/gris

- **Objetivo:** Validar que las fechas anteriores a la fecha actual se muestran deshabilitadas (en gris) y no son seleccionables/editables por el usuario.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - La fecha actual del sistema es `01/08/2026`.
- **Datos de prueba:**
  - Fecha pasada a verificar: `25/07/2026`
- **Pasos:**
  1. Ingresar a la sección "Calendario de riego".
  2. Ubicar el día `25/07/2026` en el calendario (fecha anterior a la actual).
  3. Intentar hacer clic o interactuar con dicho día (por ejemplo, para agregar/editar un evento).
- **Resultado esperado:** El día `25/07/2026` se visualiza en color gris/deshabilitado y el sistema no permite crear ni editar eventos sobre esa fecha.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
