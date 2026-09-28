# Entregas

Este directorio contiene los ficheros de seguimiento para la entrega de cada uno de los hitos:

* 📄 [`entrega1.md`](./entrega1.md) — **Hito 1:** Definición del Proyecto, Modelo de Negocio y Arquitectura de Referencia
* 📄 [`entrega2.md`](./entrega2.md) — **Hito 2:** Empaquetado Cloud Native, Entorno Local e Integración Continua (CI)
* 📄 [`entrega3.md`](./entrega3.md) — **Hito 3:** Aprovisionamiento con Infraestructura como Código (IaC) y Verificación del Reconciler Pattern
* 📄 [`entrega4.md`](./entrega4.md) — **Hito 4:** Despliegue Continuo (CD), Reconciliación Automatizada y Seguridad
* 📄 [`entrega5.md`](./entrega5.md) — **Hito 5:** Observabilidad, Pruebas de Carga y Release Final

> Para cada entrega, deberás editar el archivo del hito correspondiente añadiendo la URL de tu repositorio personal en la fila con tus datos.

## Procedimiento de Entrega

Para realizar la entrega de cada hito, el alumnado debe subir el código fuente y la documentación a su propio repositorio de GitHub, incluir el enlace correspondiente en el archivo de entregas del repositorio del profesor y realizar un **Pull Request**.

Cada estudiante tendrá su *propio repositorio* público en GitHub para el proyecto. La documentación del proyecto se estructurará mediante archivos Markdown. En cada entrega, el archivo `README.md` describirá el estado actual del proyecto y enlazará a archivos secundarios con documentación adicional cuando sea necesario.

Cuando se incluya material adicional externo (por ejemplo, capturas de pantalla de la configuración de Git, uso de claves SSH o pruebas de ejecución), se deben enlazar de forma clara desde el `README.md` principal del proyecto.

### 1. Realizar un Fork del repositorio del profesor (Solo la primera vez)
1. Accede al repositorio del profesor: `https://github.com/cvillalonga/CC-26-27`.
2. Haz clic en el botón **Fork** (esquina superior derecha) para crear una copia del repositorio en tu cuenta personal de GitHub.

> **Nota:** El *Fork* solo se realiza una vez al inicio del curso. Para los siguientes hitos, únicamente deberás sincronizar tu copia antes de realizar una nueva entrega.

### 2. Sincronizar el Fork antes de cada entrega
Antes de realizar la entrega de cualquier hito, asegúrate de actualizar tu repositorio con los últimos cambios del profesor:
1. En tu *Fork*, haz clic en el botón **Sync fork**.
2. Selecciona **Update branch** si hay cambios pendientes.

### 3. Editar el archivo de entrega `entregas/entregaN.md`
1. Dentro de tu *Fork*, navega a la carpeta `entregas/` y selecciona el archivo del hito correspondiente a la entrega (ej. `entrega1.md`, `entrega2.md`, ..., `entrega6.md`).
2. Edita el archivo e introduce la dirección URL de tu repositorio personal en la fila de la tabla donde aparezcan tus iniciales y nombre.
3. Haz clic en **Commit changes...** escribiendo un mensaje descriptivo (ej. `docs: añade enlace de entrega para hito N`).

### 4. Crear un Pull Request
1. Ve a la pestaña **Pull Requests** en tu *Fork* de GitHub.
2. Haz clic en el botón **New Pull Request**.
3. Verifica que la comparación apunte correctamente:
   - **base repository**: `cvillalonga/CC-26-27` (rama `main`)
   - **head repository**: `tu-usuario-github/CC-26-27` (rama `main`)
4. Revisa los cambios propuestos para confirmar que únicamente has modificado tu línea en la tabla.
5. Haz clic en **Create Pull Request**, asigna un título claro (ej. `Entrega Hito N - Nombre Alumno`) y confirma con **Create Pull Request**.

Una vez enviado, el profesor revisará la solicitud y la aceptará si cumple los requisitos. Tras el *merge*, tu enlace aparecerá publicado en el archivo `entregas/entregaN.md` del repositorio principal.
