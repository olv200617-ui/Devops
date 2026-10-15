# 4. Automatización de Procesos

[← Volver al Índice](index.md)

---

## El Rol de la Automatización en DevOps

La automatización es el motor principal que permite escalar los procesos de entrega de software de forma predecible y segura, eliminando tareas manuales repetitivas (*toil*) y reduciendo los tiempos de configuración.

---

## Pilares de la Automatización

### 1. Infraestructura como Código (IaC)
Práctica que consiste en gestionar y aprovisionar recursos informáticos (servidores, redes, bases de datos) mediante archivos de definición legibles por máquina, en lugar de interactuar manualmente con consolas web o interfaces de usuario.

* **Ventajas:** Versionado en Git, reproducibilidad de entornos e idoneidad para auditorías de seguridad.
* **Herramientas destacadas:**
  * **Terraform / OpenTofu:** Lenguaje declarativo (HCL) multicloud para gestionar recursos en AWS, Azure, GCP, etc.
  * **AWS CloudFormation / Azure Bicep:** Soluciones nativas declarativas de proveedores de nube específicos.

### 2. Gestión de Configuración (*Configuration Management*)
Garantiza que el software y las dependencias dentro de los servidores se encuentren en el estado deseado de forma homogénea e idempotente.

* **Ventajas:** Elimina el fenómeno de los "servidores mascota" (*snowflake servers*) que nadie sabe cómo se configuraron.
* **Herramientas destacadas:**
  * **Ansible:** Modelo sin agentes (*agentless*) que opera mediante SSH usando *playbooks* en YAML.
  * **Puppet / Chef:** Modelos cliente-servidor para infraestructuras masivas y políticas estrictas de cumplimiento.

### 3. Contenedores y Orquestación
La contenerización resuelve el problema clásico de *"en mi máquina sí funciona"*, empaquetando el código junto con sus bibliotecas y dependencias en un artefacto autocontenido.

* **Docker:** Motor de contenedores estándar para construir, compartir y ejecutar entornos aislados.
* **Kubernetes (K8s):** Estándar de la industria para la orquestación a gran escala: gestiona el ciclo de vida, balanceo de carga, autoreparación (*self-healing*) y escalado automático de contenedores.

### 4. DevSecOps (Automatización de Seguridad)
Integración temprana de comprobaciones de seguridad (*Shift Left*):
* **Escaneo de dependencias:** Detección de vulnerabilidades conocidas (CVEs) en bibliotecas externas (ej. Snyk, Trivy).
* **Análisis estático (SAST):** Detección de patrones inseguros y fugas de contraseñas/claves API en el código fuente.