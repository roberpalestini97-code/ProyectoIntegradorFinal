CI/CD con GitHub Actions + Terraform + Docker
Integrantes
[Edgardo Ale Chamorro]
[Roberto Adrian Palestini]
[Sebastian Cacace]
[Pablo Bagliere]

Descripción del Proyecto

Este proyecto implementa un pipeline completo de CI/CD utilizando GitHub Actions, integrando herramientas de infraestructura como código, contenedores y seguridad automatizada.

La solución permite:

Compilar y testear una aplicación generada con IA.
Construir y publicar imágenes Docker.
Provisionar infraestructura mediante Terraform.
Ejecutar controles de seguridad y análisis de calidad.
Generar un SBOM (Software Bill of Materials).
Monitorear métricas mediante Prometheus y Grafana.



El workflow de GitHub Actions realiza automáticamente las siguientes tareas:

1. Checkout del repositorio

Obtiene el código fuente desde GitHub.

2. Instalación de dependencias

Instala librerías y herramientas necesarias para la compilación.

3. Testing

Ejecuta pruebas automatizadas para validar el funcionamiento de la aplicación.

4. Análisis de calidad y seguridad

Se integran herramientas como:

ESLint
SonarQube
Snyk

Para detectar:

Vulnerabilidades
Código inseguro
Problemas de calidad
5. Generación de imagen Docker

La aplicación se empaqueta dentro de un contenedor Docker.

6. Generación de SBOM

Se genera un inventario completo de dependencias utilizando:

CycloneDX
SPDX
7. Despliegue con Terraform

Terraform aprovisiona automáticamente la infraestructura requerida en AWS.

Infraestructura Terraform

Terraform administra:

Instancias EC2
Redes
Security Groups
Docker Host
Recursos asociados
Inicialización
terraform init
Planificación
terraform plan
Despliegue
terraform apply
Docker
Construcción de la imagen
docker build -t app-image .
Ejecución local
docker run -p 8080:8080 app-image
Seguridad

El pipeline incluye controles automáticos:

ESLint / SonarQube

Validación de calidad y buenas prácticas.

Snyk

Escaneo de:

Dependencias vulnerables
Imágenes Docker
Riesgos de seguridad
Monitoreo
Prometheus

Recolecta métricas de la aplicación y la infraestructura.

Grafana

Visualiza dashboards con métricas como:

CPU
Memoria
Estado de contenedores
Disponibilidad
Entregables

El archivo comprimido incluye:

Workflow .yml de GitHub Actions
Archivos .tf de Terraform
Dockerfile
Artefacto generado
SBOM
Capturas de Grafana/Prometheus

Proyecto desarrollado para la materia/práctica de:

CI/CD con GitHub Actions + Terraform + Docker
