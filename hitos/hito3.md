# Hito 3: Aprovisionamiento con Infraestructura como Código (IaC) y Verificación del Reconciler Pattern

## Objetivo
Aprovisionar la infraestructura Cloud en un proveedor público gratuito (o de pago pero gratuito durante un tiempo o para un nivel determinado servicio) utilizando Terraform de forma declarativa y modular, gestionar el estado de manera remota y segura, y demostrar empíricamente el funcionamiento del patrón *Reconciler* mediante un experimento guiado de detección y corrección de deriva de configuración (*drift*).

## Descripción
En este hito se inicia el trabajo en la nube pública. El estudiante escribirá código de Terraform para definir la infraestructura de red, seguridad y cómputo necesaria para alojar la aplicación. Se configurará un backend remoto seguro con bloqueo de estado para evitar condiciones de carrera o corrupción.

Como demostración práctica del **Patrón *Reconciler***, el alumno inducirá intencionadamente una alteración manual (*drift*) en la infraestructura desde la consola web del proveedor (por ejemplo, cambiando la regla de un grupo de seguridad o el tamaño de una instancia). A continuación, utilizará Terraform para observar cómo detecta el desvío entre el estado deseado (declarado en código) y el estado real (observado en la nube), ejecutando finalmente la reconciliación para devolver el sistema a su estado correcto. Por último, ejecutará y documentará el proceso de destrucción de infraestructura necesario para controlar el gasto por el uso de la nube.

## Entregables
* **Código de Terraform Modularizado:**
  * Código fuente estructurado en archivos estándar (`main.tf`, `variables.tf`, `outputs.tf`, `providers.tf`).
  * **Capa de Red:** VPC, subredes públicas/privadas, tablas de enrutamiento y grupos de seguridad con reglas de acceso restringido (mínimo privilegio).
  * **Capa de Cómputo:** Instancias IaaS o servicio PaaS ligero configurado para ejecutar contenedores.
  * **Capa de Persistencia:** Almacenamiento en bloque o base de datos gestionada.
* **Gestión de Estado Remoto y Credenciales:**
  * Configuración de backend remoto.
  * Aislamiento estricto de secretos: variables declaradas y exclusión de `.tfvars` del repositorio Git.
* **Documentación del Experimento Práctico del *Reconciler Pattern*:**
  * `README.md` documentando con capturas de pantalla y trazas de comandos el siguiente flujo:
    1. **Estado Deseado:** Estado inicial de la infraestructura tras aplicar el código (`terraform apply`).
    2. **Inducción de Drift:** Modificación manual realizada en la consola web del proveedor cloud sobre un recurso.
    3. **Fase de Observación:** Salida del comando `terraform plan` donde se identifica la discrepancia exacta entre el estado deseado y el estado real observado.
    4. **Fase de Reconciliación:** Salida del comando `terraform apply` mostrando cómo el motor corrige la infraestructura real devolviéndola al estado definido en código.
* **Verificación de Apagado (*Teardown Verification*):**
  * Evidencia documental del comando `terraform destroy` ejecutado con éxito para certificar que la infraestructura no queda activa generando costes fuera de las horas de laboratorio.
