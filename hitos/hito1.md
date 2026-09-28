# Hito 1: Definición del Proyecto, Modelo de Negocio y Arquitectura de Referencia

## Objetivo
Establecer las bases del proyecto, definir una problemática de negocio real que justifique el uso de la nube, diseñar la arquitectura desacoplada en microservicios, configurar el entorno de gestión de ingeniería de software en GitHub y realizar el encuadre teórico del sistema según los estándares del NIST.

## Descripción
El estudiante elegirá libremente una aplicación con lógica de negocio real (evitando sistemas triviales "CRUD"). Diseñará una arquitectura distribuida formada por al menos 2 microservicios/componentes independientes y una capa de persistencia o caché. 

Durante este hito se formalizará el diseño arquitectónico y se justificará el proyecto bajo los marcos teóricos del NIST (SP 800-145 y SP 500-292), analizando las 5 características esenciales de la nube que motivan la solución y mapeando los roles. Asimismo, se dejará preparado el ecosistema de gestión en GitHub (tableros, plantillas y políticas de flujo de trabajo) que se empleará durante todo el curso.

## Entregables
* **Repositorio de GitHub Configurado:**
  * Repositorio individual con archivo `.gitignore` adecuado al *stack* tecnológico.
  * Estrategia de ramas definida (ej. `main` e integración mediante *feature branches*).
  * Adopción de convención de commits semánticos (`feat:`, `fix:`, `docs:`, `refactor:`).
* **Entorno de Gestión de Proyecto:**
  * Tablero activo en **GitHub Projects** organizado en vistas agrupadas por *Milestones* y poblado con el backlog inicial del proyecto.
  * **Historias de Usuario (User Stories):** Registradas explícitamente como *GitHub Issues* siguiendo la estructura estándar (*«Como [rol], quiero [acción], para [beneficio]»*), acompañadas de sus Criterios de Aceptación, la etiqueta `user-story` y una lista de verificación (*checklist*) con las tareas técnicas necesarias para su cumplimiento.
  * **Plantillas de Trabajo:** Archivos de plantilla configurados en `.github/ISSUE_TEMPLATE/user_story.md` para la creación estandarizada de historias de usuario y `.github/PULL_REQUEST_TEMPLATE.md` para formalizar las entregas y revisiones de código.
* **Documentación en `README.md`:**
  * **Descripción del Dominio:** Problema de negocio que resuelve la Aplicación Nativa de la Nube (*Cloud-Native Application*) que se pretende desarrollar y casos de uso principales.
  * **Justificación NIST SP 800-145:** Análisis de cómo la aplicación aprovecha las 5 características esenciales del Cloud (Autoservicio bajo demanda, Acceso amplio a la red, Asignación común de recursos, Rápida elasticidad y Servicio medido).
  * **Mapeo de Actores NIST SP 500-292:** Identificación explícita de los roles de Consumidor, Proveedor, Intermediario, Auditor y Operador, con análisis del impacto económico.
  * **Diagrama de Arquitectura:** Diagrama formal detallando componentes, protocolos de comunicación entre microservicios y almacenamiento.
  * **Especificación de API REST:** Documentación sintética de los endpoints principales (rutas, verbos HTTP, payloads JSON).
