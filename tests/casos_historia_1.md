# Casos de Prueba – Historia 1: Login y Seguridad

**Historia de usuario:** Como administrador, quiero iniciar sesión con credenciales seguras (Hash) para proteger la información sensible de los huertos.

**Criterios de aceptación:**
- Contraseñas encriptadas en BDD.
- Bloqueo tras 3 intentos fallidos.
- Redirección correcta según Rol (Admin/Usuario).

---

## TC-001 – Inicio de sesión exitoso con credenciales válidas y redirección según rol

- **Objetivo:** Validar que un administrador puede iniciar sesión con credenciales válidas y es redirigido correctamente según su rol (Admin).
- **Precondiciones:**
  - Existe un usuario con rol "Administrador" registrado en la base de datos, con la contraseña almacenada en formato hash.
  - La aplicación está desplegada y accesible.
- **Datos de prueba:**
  - Correo: `admin@huertos.com`
  - Contraseña: `Admin$2025`
  - Rol esperado: `Administrador`
- **Pasos:**
  1. Abrir la pantalla de inicio de sesión.
  2. Ingresar el correo `admin@huertos.com`.
  3. Ingresar la contraseña `Admin$2025`.
  4. Presionar el botón "Iniciar sesión".
- **Resultado esperado:** El sistema valida el hash de la contraseña contra la BDD, autentica al usuario y lo redirige a la vista correspondiente al rol "Administrador" (panel de administración).
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_

---

## TC-002 – Bloqueo de cuenta tras 3 intentos fallidos de inicio de sesión

- **Objetivo:** Validar que el sistema bloquea el acceso a la cuenta luego de 3 intentos consecutivos con credenciales incorrectas, como medida de seguridad.
- **Precondiciones:**
  - Existe un usuario válido registrado: `admin@huertos.com`.
  - La cuenta no está bloqueada al iniciar la prueba.
- **Datos de prueba:**
  - Correo: `admin@huertos.com`
  - Contraseña incorrecta (intento 1): `ClaveMala1`
  - Contraseña incorrecta (intento 2): `ClaveMala2`
  - Contraseña incorrecta (intento 3): `ClaveMala3`
- **Pasos:**
  1. Abrir la pantalla de inicio de sesión.
  2. Ingresar el correo `admin@huertos.com` y la contraseña `ClaveMala1`. Presionar "Iniciar sesión".
  3. Repetir con `ClaveMala2` (intento 2).
  4. Repetir con `ClaveMala3` (intento 3).
  5. Intentar un cuarto inicio de sesión, incluso con la contraseña correcta (`Admin$2025`).
- **Resultado esperado:** Tras el tercer intento fallido, el sistema bloquea la cuenta y muestra un mensaje indicando el bloqueo. En el cuarto intento, aunque la contraseña sea correcta, el acceso sigue denegado mientras la cuenta esté bloqueada.
- **Resultado obtenido:** _(Pendiente de ejecución)_
- **Estado:** Pendiente
- **Notas/Evidencias:** _(Se agregará captura/log tras la ejecución)_
