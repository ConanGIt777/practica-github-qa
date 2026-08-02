# Casos de Prueba – Historia 2: CRUD Plantas e Inventario

**Historia de usuario:** Como administrador, quiero registrar, editar y listar las plantas disponibles para mantener un inventario digital actualizado.

**Criterios de aceptación:**
- Validación de campos obligatorios (Nombre, Especie).
- No permitir duplicados de ID de planta.
- Confirmación visual "Guardado con éxito".

---

## TC-003 – Registro exitoso de una nueva planta con confirmación visual

- **Objetivo:** Validar que el administrador puede registrar una nueva planta con un ID único y datos completos, y que el sistema muestra la confirmación visual "Guardado con éxito".
- **Precondiciones:**
  - El administrador ha iniciado sesión correctamente.
  - No existe ninguna planta registrada con el ID `P-101`.
- **Datos de prueba:**
  - ID de planta: `P-101`
  - Nombre: `Tomate Cherry`
  - Especie: `Solanum lycopersicum`
- **Pasos:**
  1. Ingresar a la sección "Inventario de plantas".
  2. Presionar el botón "Agregar planta".
  3. Completar el formulario con ID `P-101`, Nombre `Tomate Cherry` y Especie `Solanum lycopersicum`.
  4. Presionar el botón "Guardar".
- **Resultado esperado:** La planta se registra correctamente, aparece listada en el inventario, y el sistema muestra el mensaje de confirmación "Guardado con éxito".
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-004 – Rechazo al registrar planta con campos obligatorios vacíos y con ID duplicado

- **Objetivo:** Validar que el sistema impide guardar una planta cuando faltan los campos obligatorios (Nombre, Especie) y cuando el ID de planta ya existe.
- **Precondiciones:**
  - El administrador ha iniciado sesión correctamente.
  - Ya existe una planta registrada con el ID `P-101`.
- **Datos de prueba:**
  - Caso A (campos vacíos): ID `P-102`, Nombre: _(vacío)_, Especie: _(vacío)_
  - Caso B (ID duplicado): ID `P-101` (ya existente), Nombre: `Lechuga`, Especie: `Lactuca sativa`
- **Pasos:**
  1. Ingresar a la sección "Inventario de plantas" y presionar "Agregar planta".
  2. **Caso A:** Ingresar ID `P-102`, dejar Nombre y Especie vacíos, y presionar "Guardar".
  3. Verificar que se muestra un mensaje de validación de campos obligatorios y que la planta no se guarda.
  4. **Caso B:** Repetir el registro usando el ID `P-101` (ya existente) con Nombre `Lechuga` y Especie `Lactuca sativa`, y presionar "Guardar".
- **Resultado esperado:** En el Caso A, el sistema muestra un mensaje de validación indicando que Nombre y Especie son obligatorios y no guarda el registro. En el Caso B, el sistema rechaza el guardado por ID duplicado y muestra un mensaje de error correspondiente.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
