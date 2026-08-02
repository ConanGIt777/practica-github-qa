# Casos de Prueba – Historia 6: Dashboard Estadístico

**Historia de usuario:** Como supervisor, quiero ver gráficos estadísticos sobre el estado de los huertos para tomar decisiones basadas en datos de productividad.

**Criterios de aceptación:**
- Debe incluir un gráfico de barras para "Cosechas por Mes".
- Debe incluir un gráfico de pastel para "Estado de Salud de Plantas".
- Los datos deben actualizarse en tiempo real al cargar la página.

---

## TC-011 – Visualización correcta de los gráficos con datos actualizados

- **Objetivo:** Validar que el dashboard muestra el gráfico de barras "Cosechas por Mes", el gráfico de pastel "Estado de Salud de Plantas", y que ambos reflejan datos actualizados al cargar la página.
- **Precondiciones:**
  - El supervisor ha iniciado sesión correctamente.
  - Existen registros de cosechas de los últimos meses y datos de salud de plantas (Sana, Enferma, En riesgo, etc.).
- **Datos de prueba:**
  - Cosechas registradas: `Julio: 12, Agosto: 5`
  - Estados de salud registrados: `Sana: 8, Enferma: 2, En riesgo: 1`
- **Pasos:**
  1. Ingresar a la sección "Dashboard estadístico".
  2. Esperar a que la página cargue completamente.
  3. Verificar que se muestra el gráfico de barras "Cosechas por Mes" con los valores correspondientes.
  4. Verificar que se muestra el gráfico de pastel "Estado de Salud de Plantas" con los valores correspondientes.
- **Resultado esperado:** Ambos gráficos se renderizan correctamente y muestran datos consistentes con los registros reales, actualizados al momento de cargar la página (sin necesidad de refrescar manualmente).
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-012 – Comportamiento del dashboard cuando no existen datos para alguno de los gráficos

- **Objetivo:** Validar que el sistema maneja adecuadamente la ausencia de datos para alguno de los gráficos requeridos, sin generar errores visuales ni bloquear la carga del dashboard.
- **Precondiciones:**
  - El supervisor ha iniciado sesión correctamente.
  - No existen registros de cosechas para el mes actual, y no hay datos de salud de plantas registrados.
- **Datos de prueba:**
  - Cosechas registradas: `0`
  - Estados de salud registrados: `0`
- **Pasos:**
  1. Ingresar a la sección "Dashboard estadístico" con una cuenta/entorno sin datos.
  2. Esperar a que la página cargue.
- **Resultado esperado:** El sistema muestra un estado vacío controlado (ej. "Sin datos disponibles" en el gráfico correspondiente) en lugar de un gráfico roto, error en consola visible al usuario, o pantalla en blanco.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
