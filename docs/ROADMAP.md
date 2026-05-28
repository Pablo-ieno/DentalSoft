# Roadmap — DentalSoft

Funciones sugeridas para versiones futuras, ordenadas por prioridad.

---

## Prioridad alta

### Backend con base de datos real
- Motor: Node.js + Express + SQLite (local) o PostgreSQL (nube)
- Los datos dejan de estar hardcodeados en el HTML
- Persistencia real de pacientes, turnos e historias clínicas
- Sincronización entre PC y celular si se despliega en la nube

### Recordatorios automáticos (WhatsApp Business API)
- Los mensajes se envían solos la noche anterior al turno, sin intervención manual
- Requiere cuenta en Meta Business y número dedicado (~USD 15-30/mes)
- Posibilidad de que el paciente responda confirmando o cancelando

### Login con contraseñas reales
- Base de datos de usuarios con contraseñas hasheadas (bcrypt)
- Sesiones con JWT o cookies seguras
- Recuperación de contraseña por email

---

## Prioridad media

### PWA instalable (Progressive Web App)
- Instalar como app en Android/iOS desde el navegador
- Ícono en la pantalla de inicio, funciona sin abrir el navegador
- Caché offline para usar sin internet

### Adjuntos almacenados en servidor
- En la versión actual, los archivos se adjuntan solo visualmente (demo)
- Con backend: subida real a disco o a un servicio de almacenamiento (S3, Google Cloud Storage)

### Múltiples profesionales
- Soporte para consultorios con más de un odontólogo
- Cada profesional tiene su propia agenda y pacientes
- El administrador puede ver el panorama general

### Reportes y estadísticas
- Facturación por período, por tratamiento, por obra social
- Pacientes más frecuentes
- Días y horarios con más demanda
- Exportación a Excel o PDF

### Gestión de obras sociales y aranceles
- Base de datos de prestaciones con códigos y aranceles
- Generación de planillas para presentar a la obra social

---

## Prioridad baja / futuro

### Recordatorios de pacientes que no volvieron
- Lista de pacientes sin turno en los últimos N meses
- Mensaje de "te extrañamos" vía WhatsApp

### Firma digital de consentimientos
- El paciente firma desde la pantalla del celular
- El documento se adjunta automáticamente a la historia clínica

### Integración con radiografías digitales
- Importación directa desde equipos de RX compatibles

### Facturación electrónica (ARCA/AFIP)
- Emisión de facturas electrónicas directamente desde el sistema
- Para profesionales que facturan honorarios

---

## Notas técnicas para el desarrollador

- El frontend actual es 100% vanilla JS, sin frameworks. Para escalar conviene migrar a **React + Vite**.
- El sistema de permisos usa `localStorage`; con backend real se reemplaza por claims en el JWT.
- Los colores del sistema están en variables CSS bajo `:root` — fácil de rebranding cambiando `--v*` values.
- La integración WhatsApp usa `wa.me` links; la migración a API Business no requiere cambios en el frontend, solo agregar un endpoint en el backend que llame a la API de Meta.
