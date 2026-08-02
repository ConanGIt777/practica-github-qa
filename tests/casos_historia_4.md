# Casos de Prueba – Historia 4: Geolocalización y Mapas

**Historia de usuario:** Como usuario, quiero visualizar la ubicación de las parcelas en un mapa interactivo para identificar mi zona de trabajo y rutas de acceso.

**Criterios de aceptación:**
- El mapa debe centrarse automáticamente en las coordenadas de Quito.
- Al hacer clic en un marcador, debe mostrar el nombre de la parcela y el responsable.

---

## TC-007 – El mapa se centra automáticamente en las coordenadas de Quito

- **Objetivo:** Validar que, al ingresar a la sección de mapas, el mapa se carga y se centra automáticamente en las coordenadas de Quito.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - Existen parcelas registradas con coordenadas geográficas válidas.
- **Datos de prueba:**
  - Coordenadas esperadas de centrado: `-0.1807, -78.4678` (Quito, Ecuador)
- **Pasos:**
  1. Ingresar a la sección "Mapa" / "Geolocalización".
  2. Esperar a que el mapa cargue completamente.
  3. Verificar el punto central del mapa mostrado.
- **Resultado esperado:** El mapa se carga sin errores y su centro coincide con las coordenadas de Quito (`-0.1807, -78.4678`), independientemente de la ubicación real del dispositivo.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-008 – Error al hacer clic en un marcador con datos de parcela incompletos o inexistentes

- **Objetivo:** Validar que el sistema responde adecuadamente cuando se hace clic en un marcador cuya parcela no tiene información de responsable registrada (dato faltante), sin romper la interfaz.
- **Precondiciones:**
  - El usuario ha iniciado sesión correctamente.
  - Existe una parcela en el mapa (`Parcela Norte`) registrada sin un responsable asignado.
- **Datos de prueba:**
  - Parcela: `Parcela Norte`
  - Responsable: _(vacío / no asignado)_
- **Pasos:**
  1. Ingresar a la sección "Mapa" / "Geolocalización".
  2. Ubicar el marcador correspondiente a `Parcela Norte`.
  3. Hacer clic sobre el marcador.
- **Resultado esperado:** El sistema muestra el nombre de la parcela (`Parcela Norte`) y, ante la ausencia de responsable, muestra un valor por defecto controlado (ej. "Sin asignar") en lugar de un error o campo vacío/roto.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
