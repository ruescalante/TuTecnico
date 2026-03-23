# TuTécnico: Documento de Control y Planeación (agents.md)

## 📌 Resumen del Proyecto
**TuTécnico** es un marketplace de servicios técnicos a domicilio en El Salvador. Su objetivo es conectar de manera eficiente, segura y estructurada a usuarios que necesitan servicios cotidianos (electricidad, fontanería, reparación de electrodomésticos, etc.) con técnicos independientes capacitados.

## 🛠️ Stack Tecnológico
* **Backend:** PHP Puro (sin frameworks).
* **Base de Datos:** MySQL / MariaDB.
* **Frontend:** HTML5, CSS3, JavaScript (Vanilla). *Considerar Tailwind CSS o Bootstrap para agilizar el diseño.*
* **Arquitectura:** Patrón MVC (Modelo-Vista-Controlador) implementado de forma nativa para mantener el orden.

## 👥 Actores de la Plataforma (Agentes)
1.  **Usuario (Cliente):** Busca servicios, compara perfiles, contrata y deja reseñas.
2.  **Técnico:** Ofrece sus servicios, gestiona su perfil, recibe solicitudes y construye su reputación.
3.  **Administrador:** Modera la plataforma, verifica identidades de técnicos, gestiona disputas y analiza métricas.

## 🚀 Funcionalidades Clave (MVP - Producto Mínimo Viable)
* [ ] **Sistema de Autenticación:** Registro e inicio de sesión seguro (separando roles de Usuario y Técnico).
* [ ] **Gestión de Perfiles:** * Usuarios: Información de contacto y direcciones.
    * Técnicos: Portafolio, áreas de especialidad, zonas de cobertura y carga de documentos de identidad (para confianza).
* [ ] **Motor de Búsqueda:** Filtros por tipo de servicio (ej. "Electricista") y ubicación.
* [ ] **Sistema de Solicitud/Cotización:** El usuario puede contactar al técnico para solicitar un servicio.
* [ ] **Sistema de Reseñas y Calificaciones:** Fundamental para construir la confianza y reputación que plantea el problema original.

## 🗺️ Hoja de Ruta (Roadmap) y Avances

### Fase 1: Planificación y Diseño (En curso ⏳)
- [x] Definir planteamiento del problema y estado del arte.
- [x] Crear documento inicial de planeación (`agents.md`).
- [ ] Diseñar el modelo relacional de la base de datos (Entidad-Relación).
- [ ] Definir la estructura de carpetas (MVC en PHP puro).
- [ ] Crear wireframes básicos (bocetos visuales) de las pantallas principales.

### Fase 2: Backend Base y Autenticación (Pendiente 🕒)
- [ ] Configurar conexión a la base de datos con PDO (PHP Data Objects).
- [ ] Crear sistema de ruteo básico en PHP (`index.php` como Front Controller).
- [ ] Implementar registro de usuarios (con hash de contraseñas seguro).
- [ ] Implementar login y manejo de sesiones.

### Fase 3: Desarrollo de Módulos Core (Pendiente 🕒)
- [ ] Crear el panel (dashboard) del Técnico.
- [ ] Crear el panel del Usuario.
- [ ] Desarrollar el listado público de técnicos con buscador.
- [ ] Implementar el flujo de contacto/solicitud de servicio.

### Fase 4: Refinamiento y Detalles (Pendiente 🕒)
- [ ] Añadir sistema de calificaciones de 1 a 5 estrellas.
- [ ] Validaciones de seguridad (protección contra inyecciones SQL, XSS, CSRF).
- [ ] Mejorar la interfaz de usuario (UI) y experiencia de usuario (UX).

## 📝 Notas y Observaciones Libres
* *Espacio para anotar ideas que surjan durante el desarrollo, enlaces útiles, o dudas a resolver...*
* Recordar investigar: ¿Cómo se verificará la identidad de los técnicos salvadoreños para garantizar seguridad? (Ej. DUI, antecedentes).