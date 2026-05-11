# 📔 Proyecto Agenda - Examen Unidad 3
**Alumno:** Francisco Javier Sevilla Sanchez (FJSS)

## 🚀 Arquitectura del Proyecto
Este proyecto implementa un ciclo completo de **CI/CD** utilizando las siguientes herramientas:

* **GitHub Actions:** Construye la imagen de Docker y la sube a Docker Hub automáticamente.
* **Docker Hub:** Almacena la imagen del contenedor (`adminjavier/ex_u3_agenda`).
* **Jenkins:** Recibe un Webhook de GitHub y despliega el servicio en el Cluster.
* **Docker Swarm:** Orquestación de contenedores en un cluster (1 Manager, 2 Workers).

## 🛠️ Despliegue
El despliegue se realiza mediante un Stack de Docker:
- **Red:** `examen_FJSS` (Overlay)
- **Base de Datos:** PostgreSQL 16 (Fijada en Worker-2)
- **App:** Flask + Gunicorn (2 réplicas)

## 🌐 Acceso
La aplicación es accesible a través de la IP del Manager en el puerto **5050**.