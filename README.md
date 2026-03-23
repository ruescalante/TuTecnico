# 🛠️ TuTécnico

**Marketplace de Servicios Técnicos a Domicilio en El Salvador**

TuTécnico es una plataforma digital desarrollada en PHP puro que busca solucionar la informalidad en la contratación de servicios técnicos para el hogar (electricidad, fontanería, reparación de electrodomésticos, etc.). Conecta a usuarios que necesitan soluciones confiables con técnicos independientes capacitados, dentro de un entorno seguro, estructurado y basado en la reputación.

---

## 📖 Planteamiento del Problema
En la actualidad, la búsqueda de técnicos a domicilio se realiza mayormente mediante recomendaciones empíricas o redes sociales. Esto genera:
- Falta de información verificable sobre el técnico.
- Ausencia de garantías sobre la calidad del servicio.
- Riesgos relacionados con la seguridad del usuario.
- Dificultad para los técnicos independientes de construir una reputación profesional y escalar sus oportunidades laborales.

**La Solución:** Una plataforma centralizada que permite identificar técnicos, comparar perfiles, solicitar servicios y dejar reseñas públicas tras la finalización del trabajo.

---

## ⚙️ Lógica de Negocio y Flujo Principal
El ecosistema de TuTécnico se basa en la confianza y el seguimiento de cada solicitud. El flujo de vida de un servicio es el siguiente:

1. **Descubrimiento:** El Usuario filtra técnicos por categoría (ej. "Electricista") y ubicación.
2. **Contacto / Solicitud:** El Usuario revisa el perfil, portafolio y reseñas del Técnico, y envía una "Solicitud de Servicio" en estado *Pendiente*.
3. **Respuesta:** El Técnico recibe la solicitud y puede aceptarla (cambia a *En Progreso*), rechazarla o comunicarse con el cliente para cotizar.
4. **Ejecución:** El trabajo físico se realiza en el domicilio. (El pago se maneja por fuera de la plataforma en esta fase inicial).
5. **Cierre y Calificación:** El Técnico marca el trabajo como *Completado*. El sistema habilita al Usuario para dejar una calificación de 1 a 5 estrellas y una reseña escrita, alimentando la reputación pública del Técnico.

---

## 🚀 Características Principales (MVP)

### 👤 Para Usuarios (Clientes)
- Registro y autenticación segura.
- Motor de búsqueda por oficios y zonas de cobertura.
- Historial de solicitudes de servicio.
- Sistema de evaluación y reseñas (solo habilitado para servicios completados).

### 👷 Para Técnicos
- Perfil profesional público (foto, descripción, especialidades).
- Panel de control (Dashboard) para gestionar solicitudes entrantes.
- Sistema de verificación de identidad (DUI/Antecedentes) administrado por la plataforma.
- Historial de trabajos y visualización de su reputación global.

### 🛡️ Para Administradores
- Aprobación o rechazo de perfiles de técnicos nuevos.
- Moderación de reseñas y cuentas suspendidas.

---

## 💻 Tecnologías Utilizadas
Este proyecto está construido sin frameworks para mantener un control absoluto sobre el rendimiento y la arquitectura, aplicando buenas prácticas de desarrollo.

- **Backend:** PHP (Implementación nativa del patrón MVC - Modelo, Vista, Controlador).
- **Base de Datos:** MySQL / MariaDB (Conexión segura mediante PDO).
- **Frontend:** HTML5, CSS3, JavaScript (Vanilla).
- **Seguridad:** Consultas preparadas para evitar SQL Injection, hashing de contraseñas seguro (Argon2/Bcrypt).

---

## 📂 Estructura del Proyecto (Patrón MVC)
```text
/tutecnico
├── /app
│   ├── /Controllers
│   ├── /Models
│   ├── /Views
│   └── /Core            # Router, Request, Response, DB base
├── /public              # ← Document root del servidor
│   ├── index.php        # ← Front controller aquí, no en la raíz
│   ├── /css
│   ├── /js
│   └── /img
├── /config
│   ├── app.php
│   └── database.php
├── /database
│   ├── /migrations      # Estructura de tablas versionada
│   └── /seeders         # Datos de prueba
├── /routes
│   └── web.php          # Definición de rutas
├── /tests
│   ├── /Unit
│   └── /Integration
├── /storage
│   └── /logs
├── .env.example
├── .env                 # ← en .gitignore
├── composer.json
└── README.md