# Casos de Prueba – Historia 5: Microservicio de Consejos

**Historia de usuario:** Como usuario inexperto, quiero recibir consejos automáticos sobre el cuidado de cada planta para evitar errores en el cultivo y mejorar la producción.

**Criterios de aceptación:**
- El sistema debe devolver un consejo distinto según la etapa (Siembra, Crecimiento, Cosecha).
- El tiempo de respuesta del servicio debe ser < 1 segundo.

---

## TC-009 – Consejo correcto según la etapa de la planta y tiempo de respuesta adecuado

- **Objetivo:** Validar que el microservicio devuelve un consejo distinto y coherente según la etapa de la planta (Siembra, Crecimiento, Cosecha), y que responde en menos de 1 segundo.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - Existe una planta registrada en etapa "Crecimiento".
  - El microservicio de consejos está operativo.
- **Datos de prueba:**
  - Planta: `Tomate Cherry`
  - Etapa: `Crecimiento`
- **Pasos:**
  1. Ingresar a la sección "Consejos" y seleccionar la planta `Tomate Cherry`.
  2. Solicitar el consejo del sistema.
  3. Registrar el tiempo transcurrido desde la solicitud hasta la respuesta.
  4. Repetir la solicitud cambiando la etapa de la planta a "Siembra" y luego a "Cosecha", comparando los consejos recibidos.
- **Resultado esperado:** El sistema devuelve un consejo específico y coherente con la etapa "Crecimiento" (diferente a los de "Siembra" y "Cosecha"), y el tiempo de respuesta es menor a 1 segundo en todos los casos.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-010 – Manejo de error cuando la etapa de la planta no está definida o el servicio excede el tiempo límite

- **Objetivo:** Validar que el sistema responde adecuadamente cuando la planta no tiene una etapa válida asignada, o cuando el microservicio no responde dentro del tiempo esperado.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - Existe una planta registrada sin etapa asignada (campo "Etapa" vacío o nulo).
- **Datos de prueba:**
  - Planta: `Planta sin etapa`
  - Etapa: _(vacío/null)_
- **Pasos:**
  1. Ingresar a la sección "Consejos" y seleccionar la planta `Planta sin etapa`.
  2. Solicitar el consejo del sistema.
- **Resultado esperado:** El sistema no genera un error crítico ni deja la pantalla en blanco; muestra un mensaje indicando que no se puede generar un consejo sin una etapa definida (o, si el servicio no responde en el tiempo esperado, muestra un mensaje de "tiempo de espera agotado").
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
