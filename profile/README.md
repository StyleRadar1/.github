<div align="center">

  <a href="https://github.com/StyleRadar1">
    <img src="https://raw.githubusercontent.com/JUANNICOLASA/Frontend-Style-Radar/main/styleradar-frontend-v3/assets/logo/styleradar-logo.svg" width="360" alt="StyleRadar Logo Oficial" />
  </a>

  <h1>STYLE RADAR</h1>

  <p align="center">
    <a href="https://styleradar-backend-prod.azurewebsites.net">
      <img src="https://img.shields.io/badge/CLOUD-AZURE-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white" alt="Azure Active" />
    </a>
    <a href="#convenciones-oficiales-de-ingeniería">
      <img src="https://img.shields.io/badge/JAVA-21_LTS-12063A?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21 LTS" />
    </a>
    <a href="#convenciones-oficiales-de-ingeniería">
      <img src="https://img.shields.io/badge/SPRING_BOOT-3.2.x-5600EF?style=for-the-badge&logo=spring&logoColor=white" alt="Spring Boot 3.2" />
    </a>
    <a href="#convenciones-oficiales-de-ingeniería">
      <img src="https://img.shields.io/badge/ARQUITECTURA-HEXAGONAL-16A34A?style=for-the-badge" alt="Arquitectura Hexagonal" />
    </a>
    <a href="https://styleradar.atlassian.net">
      <img src="https://img.shields.io/badge/JIRA-MANAGEMENT-0052CC?style=for-the-badge&logo=jira&logoColor=white" alt="Jira" />
    </a>
    <a href="<URL_SONARQUBE>">
      <img src="https://img.shields.io/badge/SONARQUBE-QUALITY_GATE-16A34A?style=for-the-badge&logo=sonarqube&logoColor=white" alt="SonarQube" />
    </a>
  </p>

  <p align="center">
    <strong>Descubre tu estilo. En tu ciudad.</strong><br />
    <em>Plataforma de comercio electrónico de moda local con inventario geolocalizado en tiempo real, probador virtual impulsado por IA y arquitectura distribuida de microservicios para Bogotá.</em>
  </p>

</div>

---

### Ecosistema de Repositorios (Arquitectura de Microservicios)

| Repositorio | Tipo / Rol | Squad Responsable | Stack Tecnológico | Estado |
| :--- | :--- | :--- | :--- | :---: |
| `styleradar-frontend` | Frontend SPA / PWA | Frontend Squad | React 18, TypeScript, Tailwind | Producción |
| `sr-api-gateway` | API Gateway & Routing | Squad Infraestructura | Spring Cloud Gateway, Redis | Activo |
| `ms-autenticacion` | Microservicio (Seguridad / Auth) | Squad 1 (Identidad) | Spring Security 6, JWT, Redis | Activo |
| `ms-usuarios` | Microservicio (Perfiles / Cuentas) | Squad 1 (Identidad) | Java 21, Spring Boot 3.2, PostgreSQL | Activo |
| `ms-tiendas` | Microservicio (Gestión de Tiendas) | Squad 1 (Identidad) | Java 21, Spring Boot 3.2, PostGIS | Activo |
| `ms-item-catalogo` | Microservicio (Catálogo & Prendas) | Squad 2 (Catálogo) | Java 21, Spring Boot 3.2, PostgreSQL | Activo |
| `ms-inventario` | Microservicio (Stock Multi-sede) | Squad 2 (Catálogo) | Java 21, Spring Boot 3.2, PostgreSQL | Activo |
| `ms-geolocalizacion` | Microservicio (Búsqueda Espacial) | Squad 2 (Catálogo) | Java 21, PostgreSQL + PostGIS | Activo |
| `ms-probador-virtual` | Microservicio (Probador IA VTON) | Squad 3 (Experiencia) | Spring Boot 3.2, FASHN AI API | Activo |
| `ms-favoritos-interac` | Microservicio (Playlists & Likes) | Squad 3 (Experiencia) | Java 21, Spring Boot 3.2, PostgreSQL | Activo |
| `ms-resenas` | Microservicio (Reseñas & Feedback) | Squad 3 (Experiencia) | Java 21, Spring Boot 3.2, PostgreSQL | Activo |
| `ms-pagos-suscripc` | Microservicio (Pasarela & Planes) | Squad 4 (Transacciones) | Java 21, Spring Boot 3.2, RabbitMQ | Activo |
| `ms-notificaciones` | Microservicio (Alertas & Mensajería) | Squad 5 (Soporte) | RabbitMQ, Mailgun, WebSocket | Activo |
| `ms-estadisticas` | Microservicio (Analítica & Métricas)| Squad 5 (Soporte) | PostgreSQL Views, RabbitMQ | Activo |
| `ms-auditoria-logs` | Microservicio (Trazabilidad Global) | Squad 5 (Soporte) | PostgreSQL Append-Only, RabbitMQ | Activo |
| `styleradar-infra` | Infraestructura & Cloud | Squad DevOps | Docker Compose, Azure AKS, CI/CD | Activo |

---

### Convenciones Oficiales de Ingeniería

* **Estándar de Arquitectura:** Arquitectura Hexagonal estricta (Dominio desacoplado de Frameworks y Adaptadores).
* **Persistencia:** Patrón *Database-per-Service* (PostgreSQL 16 aislado con schemas independientes).
* **Event-Driven Architecture:** RabbitMQ AMQP mediante Topics, Exchanges durables y Dead Letter Queues (DLQ).
* **Calidad de Código:** Umbral obligatorio de JaCoCo ≥ 85% y Quality Gate de SonarQube Passed en cada Pull Request.
* **Flujo de Trabajo:** GitFlow con Pull Requests obligatorios y revisión de pares hacia `develop` y `main`.

