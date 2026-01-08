# 🚀 Celeris CH4 - Sistema de Gestión Logística Inteligente v4.6

**Celeris CH4** es una plataforma integral de logística interna diseñada para optimizar el flujo de trabajo, la comunicación en tiempo real y el control de gastos operativos. Transformamos la gestión de mensajería, transporte y servicios externos en una experiencia digital fluida, segura y visualmente impactante.

---

## 🌟 ¿Qué hace a Celeris único? (Lo mejor de este sistema)

*   **⚡ Omnipresencia en Tiempo Real**: Gracias a la integración con **Socket.io**, cada cambio en el sistema (nueva solicitud, comentario o cambio de estado) se refleja instantáneamente en todas las pantallas sin necesidad de recargar.
*   **📈 Inteligencia de Negocio**: Panel de Gerencia con gráficas dinámicas (**Chart.js**) que analizan tendencias, tipos de servicio y productividad de los solicitantes.
*   **💰 Control Total de Gastos**: Módulo especializado para el registro de compras externas (monto, detalle, método de pago) y control de combustible (litros y costo) integrado en el flujo de finalización del servicio.
*   **🔔 Notificaciones Niveles Pro**: Sistema de alertas con **Toasts**, sonidos cinemáticos y **Notificaciones Nativas** del sistema para que nunca se pierda un comentario o asignación, incluso con la aplicación en segundo plano.
*   **🎨 Diseño "Premium" Glassmorphism**: Una interfaz moderna y viva, con soporte nativo para **Modo Oscuro/Claro** y efectos de transparencia que proporcionan una experiencia de usuario de nivel empresarial.
*   **🔒 Seguridad Robusta**: Autenticación basada en **JWT** (JSON Web Tokens), encriptación de contraseñas con **Bcrypt** y protección contra ataques XSS mediante sanitización automática de datos.

---

## � Funcionalidades por Rol

### 👔 Gerencia (Panel de Control y Operación)
*   **Dashboard Directivo**: Visualización de métricas críticas (promedios de tiempo, servicios totales, cargas de trabajo).
*   **Creación Directiva**: Capacidad de generar solicitudes con prioridad especial sin necesidad de cambiar de cuenta.
*   **Auditoría y Exportación**: Historial completo de la empresa con opción de **exportación a CSV** para reportes mensuales en Excel.

### ⚙️ Soporte / Admin (Gestión Total)
*   **Control de Usuarios**: Creación, edición, reseteo de contraseñas y suspensión de personal.
*   **Visualización Global**: Monitor de todas las solicitudes activas en el sistema para intervención inmediata.

### 🚗 Choferes (Gestión de Campo)
*   **Control de Disponibilidad**: Sistema de estados (Disponible/Ocupado) con registro de motivos.
*   **Flujo de Servicio**: Cronómetro automático que mide tiempos de respuesta y ejecución desde el inicio hasta el fin.
*   **Registro de Gastos**: Entrada forzada de datos para compras o gasolina al finalizar servicios específicos.

### 👤 Empleados (Solicitantes)
*   **Creación de Solicitudes**: Formulario inteligente con destinos predefinidos y personalizados.
*   **Seguimiento Real**: Visualización del estado del chofer (en camino, completado) y sistema de chat/comentarios directo.

---

## 🛠️ Stack Tecnológico

| Capa | Tecnología |
| :--- | :--- |
| **Frontend** | HTML5, CSS3 (Vanilla), JavaScript (ES6 Modules) |
| **Backend** | Node.js, Express.js |
| **Base de Datos** | MySQL 8.0+ |
| **Comunicación** | Socket.io 4.7.2 (Websockets) |
| **Seguridad** | JWT, BcryptJS, Crypto (UUID v4) |
| **Visualización** | Chart.js 4.4.0 |
| **Caché/PWA** | Service Workers nativos |

---

## ⚙️ Configuración y Mantenimiento

### 📊 Base de Datos
1.  Importar esquema: `server/schema.sql`.
2.  (Opcional) Actualizar a v4.6: `server/update_schema_v4.6.sql`.

### 🔑 Variables de Entorno (.env)
Configura los accesos en `/server/.env`:
```env
DB_HOST=tu_servidor
DB_USER=tu_usuario
DB_PASSWORD=tu_password
DB_NAME=celery_db
JWT_SECRET=tu_secreto_seguro
```

### 🚢 Despliegue en Producción
```bash
# Sincronizar archivos
sudo cp -rv /ruta/origen/* /var/www/celeris/

# Reiniciar servicios
pm2 restart celeris-api
sudo systemctl reload nginx
```

---

## 📝 Historial de Versión (v4.6)
*   **Reloj Manual 24h**: Sistema de tiempo forzado independiente del navegador.
*   **Ajuste de Texto Inteligente**: Eliminación de scrollbars horizontales mediante `word-wrap` avanzado.
*   **Panel de Gerencia Híbrido**: Nueva capacidad de crear servicios desde la vista directiva.
*   **Manager de Notificaciones**: Centralización de alertas visuales y auditivas.

---
© 2026 **Alexei - CH4** | Proyecto Celeris - Logística Express.
