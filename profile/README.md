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

| Repositorio | Tipo / Rol | Squad Responsable | Stack Tecnológico | Estado | Base de datos |
| :--- | :--- | :--- | :--- | :--- | :---: |
| `StyleRadar-Frontend` | Frontend SPA / PWA | Frontend Squad | React 18, TypeScript, Tailwind | Producción | No
| `PT8080-ApiGateway-Service` | API Gateway & Routing | PT8080 | Spring Cloud Gateway| Activo | No
| `CADCHE-Authentication-Service` | Microservicio (Seguridad / Auth) | CADCHE | Spring Security 6, JWT| Activo | PostgreSQL + Redis
| `CADCHE-Users-Service` | Microservicio (Perfiles / Cuentas) | CADCHE | Java 21, Spring Boot 3.2| Activo | PostgreSQL con soporte JSONB 
| `CADCHE-Stores-Service` | Microservicio (Gestión de Tiendas) | CADCHE | Java 21, Spring Boot 3.2 | Activo | PostgreSQL +  Blob Storage
| `RST-ItemCatalog-Service` | Microservicio (Catálogo & Prendas) | RST | Java 21, Spring Boot 3.2| Activo | PostgreSQL
| `RST-Inventory-Service` | Microservicio (Stock Multi-sede) | RST | Java 21, Spring Boot 3.2| Activo | PostgreSQL
| `RST-Geolocation-Service` | Microservicio (Búsqueda Espacial) | RST | Java 21| Activo | PostgreSQL + PostGIS 
| `PT8080-VirtualTryOn-Service` | Microservicio (Probador IA VTON) | PT8080 | Spring Boot 3.2, FASHN AI API | Activo | 	PostgreSQL
| `RST-Playlist-Service` | Microservicio (Playlists & Likes) | RST | Java 21, Spring Boot 3.2| Activo | PostgreSQL
| `NQS-Payment-Service` | Microservicio (Pasarela & Planes) | NQS | Java 21, Spring Boot 3.2| Activo | PostgreSQL
| `GJ-Notification-Service` | Microservicio (Alertas & Mensajería) | GJ | RabbitMQ, Mailgun, WebSocket | Activo | PostgreSQL
| `NQS-Statistics-Service` | Microservicio (Analítica & Métricas)| NQS | RabbitMQ | Activo | PostgreSQL Views
| `PT8080-Donations-Service` | Microservicio (Donaciones y segunda vida)| PT8080 | Java 21, Spring Boot 3.2, | Activo | PostgreSQL 

---

### Convenciones Oficiales de Ingeniería

* **Estándar de Arquitectura:** Arquitectura Hexagonal estricta (Dominio desacoplado de Frameworks y Adaptadores).
* **Persistencia:** Patrón *Database-per-Service* (PostgreSQL 16 aislado con schemas independientes).
* **Event-Driven Architecture:** RabbitMQ AMQP mediante Topics, Exchanges durables y Dead Letter Queues (DLQ).
* **Calidad de Código:** Umbral obligatorio de JaCoCo ≥ 85% y Quality Gate de SonarQube Passed en cada Pull Request.
* **Flujo de Trabajo:** GitFlow con Pull Requests obligatorios y revisión de pares hacia `develop` y `main`.

