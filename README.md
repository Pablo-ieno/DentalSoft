# DentalSoft 🦷

Sistema de gestión odontológica — aplicación web de archivo único (HTML/CSS/JS), sin dependencias externas ni instalación de servidor. Funciona abriendo `index.html` en cualquier navegador moderno.

---

## Funcionalidades

| Módulo | Descripción |
|--------|-------------|
| **Login con roles** | Odontólogo (admin) y Secretaria (permisos configurables) |
| **Agenda** | Calendario mensual navegable con turnos por día |
| **Turnos del día** | Vista horaria de 9 a 18 hs |
| **Pacientes** | Grilla con búsqueda. Ficha completa por paciente |
| **Historias clínicas** | Timeline cronológico con notas, pagos y archivos adjuntos |
| **Adjuntos** | Soporte para RX, análisis e imágenes (JPG, PNG, PDF hasta 20 MB) |
| **Recordatorios WhatsApp** | Genera mensaje pre-armado y abre WhatsApp listo para enviar |
| **Configuración** | Datos del consultorio, horarios, gestión de permisos por usuario |
| **Backup** | Historial de respaldos, exportación a Google Drive o carpeta local |

---

## Permisos configurables (rol Secretaria)

Desde **Configuración → Usuarios y permisos**, el odontólogo puede activar o desactivar para la secretaria:

- Agenda y turnos *(siempre activo)*
- Pacientes *(siempre activo)*
- Recordatorios WhatsApp *(siempre activo)*
- **Historias clínicas** — desactivado por defecto
- **Registrar pagos** — desactivado por defecto
- **Ver facturación** — desactivado por defecto

Los permisos se guardan en `localStorage` del navegador y aplican en el próximo inicio de sesión.

---

## Cómo usar

```
1. Abrí frontend/index.html con cualquier navegador (Chrome, Firefox, Edge)
2. Seleccioná el perfil (Odontólogo o Secretaria)
3. Ingresá con cualquier usuario/contraseña (demo)
```

No requiere internet, servidor, ni instalación.

---

## Estructura del proyecto

```
dentalsoft/
├── frontend/
│   └── index.html        ← Aplicación completa (HTML + CSS + JS)
├── docs/
│   ├── GUIA_USO.md       ← Manual de uso detallado
│   └── ROADMAP.md        ← Funciones futuras sugeridas
└── README.md
```

---

## Stack

- **HTML5 / CSS3 / JavaScript vanilla** — sin frameworks ni dependencias
- **Google Fonts** — DM Sans + Playfair Display (carga desde CDN)
- **localStorage** — persistencia de permisos entre sesiones
- **WhatsApp Web API** — integración vía `wa.me` links

---

## Versiones

| Versión | Cambios |
|---------|---------|
| v1 | Versión inicial: agenda, pacientes, historias clínicas, WhatsApp |
| v2 | Más presencia del violeta, adjuntos en historias clínicas, roles diferenciados |
| **v3 (actual)** | Sistema de permisos configurables por el administrador |

---

## Próximos pasos sugeridos (ver ROADMAP.md)

- Backend con base de datos real (Node.js + SQLite o PostgreSQL)
- Integración API WhatsApp Business para recordatorios automáticos
- Soporte para múltiples profesionales
- App móvil (PWA instalable)
