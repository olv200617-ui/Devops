# 2. Fases del Ciclo de Vida de DevOps

[← Volver al Índice](index.md)

---

## El Bucle de DevOps

El ciclo de vida de DevOps se representa visualmente como un bucle infinito ($\infty$), lo que refleja que el desarrollo y las operaciones forman un proceso iterativo continuo sin un punto final estático.

---

## Desglose de Fases

### 1. Planificación (*Plan*)
* **Objetivo:** Definir qué se va a construir, identificar requisitos y priorizar tareas.
* **Actividades:** Gestión ágil de proyectos (Scrum/Kanban), gestión de *backlogs*, estimación de esfuerzo y definición de criterios de aceptación.
* **Herramientas representativas:** Jira, Linear, Trello, GitHub Projects.

### 2. Codificación (*Code*)
* **Objetivo:** Desarrollar las funcionalidades garantizando estándares de calidad y colaboración técnica.
* **Actividades:** Escritura de código fuente, revisiones mediante *pull requests* / *merge requests*, y control de versiones distribuido.
* **Herramientas representativas:** Git, GitHub, GitLab, Bitbucket.

### 3. Compilación y Construcción (*Build*)
* **Objetivo:** Transformar el código fuente en artefactos ejecutables y reproducibles.
* **Actividades:** Compilación, resolución de dependencias, empaquetado en binarios o imágenes de contenedores.
* **Herramientas representativas:** Maven, Gradle, Docker, npm/pnpm.

### 4. Pruebas (*Test*)
* **Objetivo:** Validar la calidad, seguridad y rendimiento antes de permitir el despliegue.
* **Actividades:** Ejecución automatizada de pruebas unitarias, de integración, *end-to-end* (E2E) y análisis estático de código (SAST).
* **Herramientas representativas:** Jest, pytest, SonarQube, Selenium, Cypress.

### 5. Lanzamiento y Empaquetado (*Release*)
* **Objetivo:** Aprobar y versionar un artefacto validado para su puesta en producción.
* **Actividades:** Gestión de etiquetas semánticas (*semantic versioning*), almacenamiento de imágenes en registros seguros y gestión de artefactos.
* **Herramientas representativas:** GitHub Packages, Docker Hub, Harbor, Nexus.

### 6. Despliegue (*Deploy*)
* **Objetivo:** Poner el software en funcionamiento en entornos de *staging* y producción de forma desatendida.
* **Actividades:** Estrategias de despliegue controlado (*Blue/Green*, *Canary Releases*, *Rolling updates*).
* **Herramientas representativas:** Argo CD, Kubernetes, Terraform, Helm.

### 7. Operación (*Operate*)
* **Objetivo:** Mantener el software disponible, escalable y seguro mientras atiende peticiones reales.
* **Actividades:** Escalado automático de instancias, gestión de parches de seguridad y administración de infraestructura subyacente.
* **Herramientas representativas:** AWS ECS/EKS, Google Kubernetes Engine (GKE), Azure AKS.

### 8. Monitorización y Observabilidad (*Monitor*)
* **Objetivo:** Obtener visibilidad del estado del sistema, detectar anomalías y retroalimentar la fase de planificación.
* **Actividades:** Centralización de logs, recopilación de métricas de rendimiento y trazado distribuido (*Distributed Tracing*).
* **Herramientas representativas:** Prometheus, Grafana, Datadog, ELK Stack (Elasticsearch, Logstash, Kibana).