# Lucy AMS - Academic Management System

Sistema de Gestión Académica para la Facultad de Ciencias Económicas de la Universidad Nacional de Río Cuarto (UNRC).

**Versión:** 0.98
**Autor:** Carlos Dagorret
**Licencia:** MIT

---

## 🎯 Características

- **Gestión de Alumnos**: Ingesta automática desde sistema UTI/SIAL
- **Integración con Microsoft Teams**: Creación y gestión de cuentas de estudiantes
- **Integración con Moodle**: Enrollamiento automático en cursos
- **Sistema de Tareas**: Procesamiento asíncrono con Celery
- **Notificaciones por Email**: Plantillas personalizables
- **Panel de Administración**: Django Admin personalizado

---

## 🚀 Inicio Rápido

### Requisitos Previos

- Docker y Docker Compose
- Python 3.12+ (para desarrollo local)
- PostgreSQL 16
- Redis 7

### Instalación

1. **Clonar el repositorio**

```bash
git clone https://github.com/tu-usuario/lucy.git
cd lucy
```

2. **Configurar variables de entorno**

```bash
cp .env.example .env.dev
nano .env.dev
```

3. **Configurar credenciales de servicios**

```bash
cd credenciales/
cp uti_credentials.json.example uti_credentials.json
cp moodle_credentials.json.example moodle_credentials.json
cp teams_credentials.json.example teams_credentials.json
# Edita cada archivo con tus credenciales reales
```

Ver documentación completa: [`CONFIGURACION.md`](CONFIGURACION.md)

4. **Iniciar el sistema**

```bash
./deploy-testing.sh start
```

5. **Acceder**

- Aplicación: http://localhost:8000
- Admin: http://localhost:8000/admin
- MailHog (testing): http://localhost:8025

---

## 📚 Documentación

- [`CONFIGURACION.md`](CONFIGURACION.md) - Guía completa de configuración
- [`credenciales/README.md`](credenciales/README.md) - Configuración de servicios externos

---

## 🔐 Seguridad

Este sistema maneja datos sensibles. Las credenciales se almacenan en:
- Archivos JSON en `credenciales/` (excluidos de Git)
- Variables de entorno
- Base de datos (Admin Django)

**Nunca subas credenciales a Git.**

---

## 📝 Licencia

MIT License - Copyright (c) 2025 Carlos Dagorret

---

**Desarrollado con ❤️ para la FCE-UNRC**
