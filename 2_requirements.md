# 🧩 Módulos Funcionales – Plataforma de Concursos Comerciales (AVIACIÓN)

Este documento detalla los módulos funcionales que componen la plataforma digital destinada a la gestión segura, trazable y eficiente de concursos comerciales en el sector aeronáutico.

---

## 🗂️ Módulos Principales

### 1. 📝 Inscripción y Registro de Proveedores
- Formulario de inscripción con validaciones.
- Confirmación por correo electrónico (Amazon Cognito + SES).
- Generación y asignación de claves de acceso seguras.
- Gestión del estado del proveedor (activo, pendiente, descalificado).
- Registro histórico de inscripción.

---

### 2. 📁 Acceso a Documentación
- Portal seguro con autenticación por proveedor.
- Listado de documentos disponibles para cada concurso.
- Descarga protegida (S3 + pre-signed URLs).
- Registro de cada descarga por proveedor (para trazabilidad).
- Visibilidad de cambios o versiones de documentos.

---

### 3. ❓ Gestión de Consultas y Respuestas
- Formulario de consultas por concurso.
- Asignación interna de consultas (jurídico, técnico, etc.).
- Consola para consolidación y validación de respuestas.
- Publicación de respuestas oficiales con control de visibilidad.
- Alerta automática a proveedores cuando una nueva consulta/respuesta es publicada.

---

### 4. 🔄 Publicación de Modificaciones
- Gestión de modificaciones al pliego o documentos del concurso.
- Control de versiones y descripción de cambios.
- Notificaciones automáticas a todos los proveedores activos.
- Registro histórico de todas las modificaciones publicadas.

---

### 5. 📤 Entrega Digital de Ofertas (Doble Sobre)
- Subida segura de dos archivos separados:
  - **Sobre Técnico** (documentación, experiencia, etc.)
  - **Sobre Económico** (propuesta económica cifrada)
- Validaciones de formato, tamaño y nombre de archivos.
- Confirmación y firma digital de la entrega.
- Estatus de recepción visible para el proveedor (sin ver contenido).
- Fecha y hora de corte automática.

---

### 6. 📊 Evaluación y Adjudicación
- Acceso exclusivo al comité evaluador.
- Visualización secuencial de sobres (primero técnico, luego económico).
- Ingreso de puntajes y observaciones.
- Cálculo automático de resultados según criterios definidos.
- Generación de acta de adjudicación.
- Notificación de resultados a todos los participantes.

---

### 7. ✅ Cierre del Concurso
- Desactivación de subida y acceso para proveedores.
- Archivo de documentos, propuestas y comunicaciones.
- Generación automática de un expediente digital.
- Bitácora completa de interacciones (quién, qué, cuándo).
- Exportación de reportes finales (PDF, Excel).

---

## 🧾 Funcionalidades Transversales (No especificas a un modulo en especifo)

### 🔐 Seguridad y Accesos
- Autenticación con Amazon Cognito (MFA opcional).
- Control de roles: proveedor, legal, comité evaluador, administrador.
- Auditoría completa de accesos y acciones.
- Validación de integridad de archivos entregados.

---

### 📬 Notificaciones Automáticas
- Correos electrónicos transaccionales:
  - Confirmaciones, recordatorios, avisos de cambios o plazos.
- Integración con Amazon SES.

---

### 🗃️ Soporte de Archivos
- Formatos soportados: PDF, Word, Excel, ZIP.
- Almacenamiento en S3 con rutas segregadas por concurso y proveedor.
- Eliminación automática o manual según políticas de retención.

---

## 📋 Consideraciones Técnicas
- Plataforma web responsive (React + FastAPI).
- Backend asincrónico con FastAPI y PostgreSQL.
- Almacenamiento seguro en S3.
- Registro de todas las acciones en base de datos.
- Integración CI/CD con GitHub Actions.

---
