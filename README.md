# Archcontrol | Plataforma de Gestión de Activos Arquitectónicos

**Archcontrol** es un ecosistema backend de alto rendimiento diseñado para la administración centralizada de planos, documentos técnicos y activos de proyectos de construcción mejorando el versionado de documentos por parte de los integrantes del equipo.

---

## 🚀 Detalles Técnicos

* **Adopción de Java 25 & Virtual Threads:** Implementación nativa sobre el JDK más reciente, aprovechando los hilos virtuales para optimizar el rendimiento en operaciones de Entrada/Salida (I/O) intensivas, como la carga y procesamiento de planos de gran tamaño.
* **Spring Boot 4 (Next Generation):** Uso de la versión más avanzada del framework, integrando las últimas mejoras en inyección de dependencias y rendimiento de arranque.
* **Persistencia Avanzada con PostgreSQL:** Diseño de esquema relacional normalizado con **Spring Data JPA**, garantizando integridad referencial y eficiencia en consultas mediante relaciones `@ManyToOne` y `@OneToMany`.
* **Seguridad Empresarial:** Arquitectura de seguridad robusta basada en **Spring Security**, con configuración preparada para autenticación **JWT (JSON Web Tokens)** y control de acceso por roles.
* **Infraestructura Contenerizada:** Configuración lista para entornos profesionales mediante **Docker**, asegurando la paridad entre los entornos de desarrollo, testing y producción.

---

## 🛠️ Stack Tecnológico

| Componente | Tecnología |
| :--- | :--- |
| **Lenguaje** | Java 25 |
| **Framework** | Spring Boot 4.0.1 |
| **Base de Datos** | PostgreSQL (Dockerizada) |
| **Persistencia** | Hibernate / Jakarta Persistence (JPA) |
| **Seguridad** | Spring Security |
| **Construcción** | Gradle |

---

## 📂 Arquitectura del Sistema

El proyecto implementa una **Arquitectura por Capas** orientada a la mantenibilidad y escalabilidad (Clean Code):

* **`entity/`**: Modelado del dominio del negocio y mapeo relacional.
* **`dto/`**: Contratos de comunicación externa.
    * `request/`: Objetos de entrada validados.
    * `response/`: Objetos de salida optimizados para el cliente.
    * `mapper/`: Lógica de transformación entre capas.
* **`repository/`**: Abstracción de la capa de datos mediante el patrón *Repository*.
* **`service/`**: Encapsulamiento de la lógica de negocio y reglas de validación.
* **`controller/`**: Exposición de API RESTful con manejo estandarizado de respuestas y códigos de estado HTTP.

---

## ⚙️ Configuración y Despliegue

### Requisitos Previos
* **JDK 25** instalado correctamente.
* **Docker Desktop** para la gestión de la base de datos.