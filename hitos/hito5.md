# Hito 5: Observabilidad, Pruebas de Carga y Release Final

## Objetivo
Implementar mecanismos de observabilidad y comprobación de salud en la aplicación, evaluar el comportamiento y resiliencia del despliegue en la nube en escenarios de estrés mediante pruebas de carga automatizadas, consolidar la documentación técnica y publicar la versión final del software (*Release v1.0.0*).

## Descripción
El estudiante validará la operabilidad real de su sistema en producción. Implementará puntos de comprobación de salud (*health checks*) en los microservicios y estructurará los registros de logs en formato JSON para su inspección en la consola del proveedor cloud.

Someterá el endpoint público a una batería de pruebas de carga y estrés utilizando herramientas de código abierto, evaluando cómo responde la infraestructura elástica frente a picos de demanda (latencia, tasa de errores HTTP 5xx y uso de recursos). Para finalizar, consolidará la documentación técnica y publicará la *Release v1.0.0* oficial en el repositorio de GitHub.

## Entregables
* **Pila de Observabilidad y Telemetría:**
  * Implementación de un endpoint `/health` o `/healthz` en los microservicios que valide el estado de la ejecución y la conectividad con la base de datos o servicios dependientes.
  * Emisión de logs estructurados en formato JSON a través de `stdout`/`stderr` en los contenedores para facilitar su análisis y centralización.
* **Pruebas de Carga y Resiliencia:**
  * Utilizando herramientas de código abierto para pruebas de carga y rendimiento, implementación de un script que simule usuarios concurrentes contra el endpoint público.
  * Documentación analizando los resultados obtenidos: RPS, latencia (percentiles p95 y p99), tasa de errores y comportamiento ante la sobrecarga.
* **Entrega Oficial del Proyecto y Documentación Final:**
  * Documentación técnica final consolidada en el `README.md` (manual de arquitectura, guía de reproducción local, guía de despliegue y enlace público a la aplicación en vivo).
  * Etiquetado y publicación oficial de una **GitHub Release (`v1.0.0`)** vinculada al commit final de la entrega.
