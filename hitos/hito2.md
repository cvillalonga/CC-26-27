# Hito 2: Empaquetado Cloud Native, Entorno Local e Integración Continua (CI)

## Objetivo
Contenerizar de forma optimizada e inmutable cada uno de los microservicios de la aplicación, orquestar el sistema completo en un entorno de desarrollo local reproducible e implementar un proceso de Integración Continua (CI) que valide el código y publique los artefactos resultantes.

## Descripción Detallada
El estudiante aplicará los principios *Cloud Native* empaquetando cada componente software en contenedores independientes. Deberá aplicar buenas prácticas de seguridad e inmutabilidad en las imágenes (reducción de tamaño, separación de capas de compilación y ejecución, uso de usuarios no privilegiados). 

Posteriormente, creará un manifiesto de Docker Compose que levante todo el entorno local (microservicios, bases de datos con almacenamiento persistente en volúmenes y redes internas) ejecutable mediante un único comando. Por último, configurará un flujo de trabajo de CI en GitHub Actions que, ante cada cambio en el código, valide la calidad del software, ejecute las pruebas unitarias e integradas y publique automáticamente las imágenes construidas en el registro de contenedores GitHub Container Registry.

## Entregables
* **Archivos `Dockerfile` de Producción (uno por microservicio):**
  * Construcción multietapa (*multi-stage builds*) para aislar el entorno de compilación del de ejecución.
  * Elección fundamentada de imágenes base minimalistas.
  * Principio de mínimo privilegio: creación y ejecución explícita bajo usuario no root.
  * Optimización de la capa de caché de Docker y exposición de puertos.
* **Manifiesto de Orquestación Local (`compose.yaml`):**
  * Definición de un clúster local funcional compuesto por un mínimo de 3 contenedores (ej. Backend API, Servicio Auxiliar/Frontend y Base de Datos/Caché).
  * Declaración de redes virtuales aisladas para la comunicación inter-contenedor.
  * Mapeo de volúmenes persistentes gestionados para garantizar la durabilidad de los datos de la base de datos al reiniciar los contenedores.
  * Configuración de variables de entorno mediante un archivo de ejemplo `.env.example` (sin credenciales reales).
* **Workflow de Integración Continua (`ci.yml`):**
  * Ejecución automatizada ante eventos `push` y `pull_request` a la rama principal.
  * Paso de linters de código y linters de sintaxis para Dockerfiles.
  * Ejecución automatizada de pruebas unitarias y de integración.
  * Construcción y publicación automatizada de las imágenes en **GitHub Container Registry**, etiquetadas con la versión semántica o el hash del commit.
