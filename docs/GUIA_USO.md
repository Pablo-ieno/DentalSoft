# Guía de uso — DentalSoft

## Inicio de sesión

Al abrir la aplicación aparece la pantalla de login. Seleccioná el perfil:

- **Odontólogo** — acceso completo a todas las secciones, incluida configuración y backup.
- **Secretaria** — acceso a agenda, turnos, pacientes y recordatorios. Las historias clínicas, pagos y facturación dependen de los permisos que configure el odontólogo.

---

## Inicio (Dashboard)

La pantalla principal muestra:
- Estadísticas del día: turnos, pacientes activos, recordatorios pendientes y facturación del mes.
- Lista de turnos del día con estado (Confirmado / Pendiente).
- Panel de recordatorios urgentes: pacientes con turno al día siguiente.
- Acciones rápidas: nuevo turno, nuevo paciente, ver recordatorios.

---

## Agenda

Vista de calendario mensual. Los días con turnos muestran el nombre del primer paciente (y un contador si hay más).

- **Navegar meses**: botones ‹ › en la parte superior.
- **Ver turnos de un día**: click sobre cualquier día — se despliegan en el panel lateral derecho.
- **Agregar turno**: botón "+ Nuevo turno" (arriba a la derecha) o desde el panel lateral.

---

## Turnos del día

Vista horaria de 9:00 a 18:00 del día actual.

- Los horarios ocupados muestran nombre del paciente y tratamiento con fondo violeta.
- Los horarios libres se pueden clickear para abrir el formulario de nuevo turno.

---

## Pacientes

Grilla de tarjetas con todos los pacientes registrados. Incluye buscador por nombre, DNI o teléfono.

Clickeando en una tarjeta se abre la **ficha completa** del paciente con:
- Datos personales y de contacto.
- Estadísticas rápidas (visitas totales y última visita).
- Historia clínica completa (si el rol tiene permiso).
- Botón para abrir WhatsApp con mensaje pre-armado.

---

## Historias clínicas

Vista de historial cronológico por paciente. Cada entrada registra:
- Fecha y tratamiento realizado.
- Notas clínicas del profesional.
- Registro de pago (monto y método).
- Archivos adjuntos: RX, análisis, imágenes (JPG, PNG, PDF hasta 20 MB).

Para agregar una entrada: botón "+ Registrar atención" dentro de la historia del paciente.

---

## Recordatorios

Lista de pacientes con turno al día siguiente que aún no recibieron aviso.

- **Enviar recordatorio**: click en "📲 Enviar recordatorio" — se abre una vista previa del mensaje.
- **Vista previa**: el sistema genera automáticamente el mensaje con nombre del paciente, fecha, hora y tratamiento.
- **Abrir WhatsApp**: al confirmar, se abre WhatsApp con el mensaje listo. Solo hay que presionar Enviar.

---

## Configuración (solo Odontólogo)

### Datos del consultorio
Nombre del profesional, especialidad, teléfono, WhatsApp para recordatorios y dirección.

### Horario de atención
Hora de inicio y fin, duración de cada turno (30, 45 o 60 minutos) y días activos.

### Usuarios y permisos
Gestión de permisos de la secretaria. Los permisos configurables son:
- **Historias clínicas**: ver y registrar entradas clínicas.
- **Registrar pagos**: ver y cargar montos cobrados.
- **Ver facturación**: acceso al resumen de ingresos del mes.

Los cambios aplican en el próximo inicio de sesión de la secretaria.

---

## Backup (solo Odontólogo)

- **Google Drive**: genera una copia comprimida de la base de datos en la carpeta "DentalSoft Backups" de tu Drive personal.
- **Exportar local**: descarga el archivo a tu PC o pen drive.
- El historial muestra los últimos backups con estado y hora.

---

## Preguntas frecuentes

**¿Necesita internet para funcionar?**
Solo para cargar las fuentes tipográficas (Google Fonts). El resto funciona sin conexión.

**¿Dónde se guardan los datos?**
En esta versión beta, los datos están incluidos en el archivo HTML como ejemplo. En la versión con backend real, se guardarían en una base de datos local (SQLite) o en la nube (PostgreSQL).

**¿Los permisos se mantienen si cierro el navegador?**
Sí, los permisos se guardan en el almacenamiento local del navegador (`localStorage`) y persisten entre sesiones en el mismo dispositivo.

**¿Puedo usar esto en el celular?**
Sí. El diseño es responsive y funciona en navegadores móviles. Para instalarlo como app en el celular (sin la barra del navegador), se puede convertir en una PWA en la versión con backend.
