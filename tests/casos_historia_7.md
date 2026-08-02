# Casos de Prueba – Historia 7: Reportes PDF Mensuales

**Historia de usuario:** HU-07: Reportes PDF Mensuales

Como supervisor, quiero generar y descargar un reporte mensual en PDF con el resumen de cosechas y riegos de los huertos, para llevar un control histórico de la productividad y compartir la información con otros interesados.

**Criterios de aceptación:**
- El PDF debe incluir el logotipo del proyecto en el encabezado.
- Debe mostrar tabla resumen de cosechas y riegos del mes.
- La descarga debe iniciar en menos de 5 segundos.

---

## TC-013 – Generación y descarga exitosa del reporte PDF con logotipo y tabla resumen

- **Objetivo:** Validar que el usuario puede generar el reporte mensual en PDF, que este incluye el logotipo del proyecto en el encabezado y una tabla resumen de cosechas y riegos, y que la descarga inicia en menos de 5 segundos.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - Existen registros de cosechas y riegos para el mes en curso.
- **Datos de prueba:**
  - Mes seleccionado: `Julio 2026`
  - Riegos registrados: `10`
  - Cosechas registradas: `4`
- **Pasos:**
  1. Ingresar a la sección "Reportes".
  2. Seleccionar el mes `Julio 2026`.
  3. Presionar el botón "Generar reporte PDF".
  4. Medir el tiempo desde que se presiona el botón hasta que inicia la descarga.
  5. Abrir el PDF descargado y revisar su contenido.
- **Resultado esperado:** La descarga del PDF inicia en menos de 5 segundos. El archivo generado contiene el logotipo del proyecto en el encabezado y una tabla resumen con los datos de cosechas y riegos del mes seleccionado.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-014 – Error al generar el reporte de un mes sin datos de cosechas ni riegos

- **Objetivo:** Validar que el sistema responde adecuadamente cuando se solicita el reporte PDF de un mes sin registros de cosechas ni riegos, en lugar de generar un PDF vacío, corrupto o fallar sin aviso.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - No existen registros de cosechas ni riegos para el mes seleccionado.
- **Datos de prueba:**
  - Mes seleccionado: `Enero 2020` (mes sin actividad registrada)
- **Pasos:**
  1. Ingresar a la sección "Reportes".
  2. Seleccionar el mes `Enero 2020`.
  3. Presionar el botón "Generar reporte PDF".
- **Resultado esperado:** El sistema muestra un mensaje indicando que no hay datos disponibles para ese periodo y no genera un archivo PDF vacío o con errores; opcionalmente, permite generar un PDF indicando explícitamente "Sin registros este mes" en la tabla resumen.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
