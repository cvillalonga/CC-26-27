# Hito 4: Despliegue Continuo (CD), Reconciliación Automatizada y Seguridad

## Objetivo
Automatizar el pipeline de Despliegue Continuo (CD) para desplegar los contenedores en la nube sin intervención manual, integrar un proceso de auditoría del *Reconciler Pattern* dentro del pipeline de CI/CD, implementar controles de seguridad de acuerdo al Modelo de Responsabilidad Compartida y garantizar el cumplimiento del Reglamento General de Protección de Datos (RGPD).

## Descripción
El estudiante conectará los artefactos creados en el Hito 2 (imágenes publicadas en el GitHub Container Registry) con la infraestructura aprovisionada en el Hito 3. Se construirá un workflow de CD en GitHub Actions que se active automáticamente tras superar el proceso de CI, desplegando la nueva versión de los contenedores en la nube mediante estrategias de actualización inmutables.

Además, el pipeline de CD integrará una verificación automatizada del *Reconciler Pattern*: antes de desplegar la aplicación, el pipeline ejecutará una comprobación de estado de la infraestructura. Si los recursos en la nube han sufrido modificaciones manuales, el pipeline detectará la deriva y detendrá el despliegue o forzará la reconciliación. El despliegue en la nube deberá ubicarse en una región geográfica localizada en la Unión Europea para cumplir con el RGPD.

## Entregables
* **Workflow de Despliegue Continuo (`cd.yml`):**
  * Activación automática tras el éxito del pipeline de CI en la rama principal.
  * Despliegue automatizado de las imágenes de contenedores desde el GitHub Container Registry hacia la infraestructura aprovisionada en la nube.
  * Estrategia de actualización que minimice la caída del servicio (*Rolling Update* o reemplazo inmutable).
* **Paso de Auditoría del *Reconciler* en CI/CD:**
  * Inclusión de un *job* previo en el pipeline que ejecute `terraform plan -detailed-exitcode` para auditar automáticamente que la infraestructura no ha sufrido derivas (*drift*) respecto al código antes de desplegar la aplicación.
* **Configuración de Seguridad y Secretos:**
  * Almacenamiento y uso exclusivo de claves de acceso, pares de llaves SSH y credenciales en **GitHub Secrets**.
  * Aplicación del principio de mínimo privilegio en las políticas IAM asignadas al usuario/rol de servicio de GitHub Actions.
* **Gobernanza y Cumplimiento Normativo (RGPD):**
  * Configuración explícita en el código de IaC y en el proveedor cloud demostrando que los recursos de cómputo y datos residen en una región de la Unión Europea.
