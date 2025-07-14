# 🗓️ Cronograma de Desarrollo – Plataforma Concursos Comerciales AVIACIÓN

Este documento detalla el cronograma de desarrollo del MVP de la plataforma de concursos, con fecha de entrega final planificada para el **1 de septiembre de 2025**.

---

## ✅ Resumen General

| Fase | Fechas | Objetivos |
|------|--------|-----------|
| 1. Diseño y Preparación | 24–28 junio | Infraestructura, diseño UI/UX, arquitectura técnica |
| 2. Desarrollo Base | 1–19 julio | Autenticación, inscripción, acceso seguro a documentos |
| 3. Funcionalidades Clave | 22 jul – 9 ago | Consultas, entrega digital de ofertas, evaluación |
| 4. Integración + QA | 12–30 agosto | Pruebas funcionales, mejoras, validaciones finales |
| 5. Cierre y Release | 30 ago – 1 sep | Despliegue, documentación, capacitación y entrega |

---

## 📅 Cronograma por Semana

### 🟨 Semana 1 – *24 al 28 de junio*
- Diseño de arquitectura técnica (infraestructura, backend, seguridad)
- Configuración inicial de AWS (Cognito, S3, RDS, SES)
- Diseño de UI/UX (flujos: inscripción, entrega, consulta)
- Estructura de repositorio + CI/CD base (GitHub Actions, Docker)

---

### 🟩 Semana 2 – *1 al 5 de julio*
- Módulo de inscripción de proveedores
- Integración de autenticación con Cognito (frontend + backend)
- Inicio de sistema de roles y permisos básicos

---

### 🟩 Semana 3 – *8 al 12 de julio*
- Subida de documentos al portal del proveedor
- Descarga protegida con pre-signed URLs (AWS S3)
- Registro de descargas por proveedor (auditoría básica)

---

### 🟩 Semana 4 – *15 al 19 de julio*
- Revisión y prueba del flujo de inscripción
- Implementación de correos automáticos (confirmaciones)
- Desarrollo inicial del módulo de consultas y respuestas

---

### 🟨 Semana 5 – *22 al 26 de julio*
- Consola de gestión de consultas (usuario interno)
- Flujo de validación legal/técnica y publicación de respuestas
- Inicio de módulo de entrega de ofertas (doble sobre)

---

### 🟨 Semana 6 – *29 julio al 2 agosto*
- Finalización de carga de sobres técnicos y económicos
- Validaciones y firma digital de la entrega
- Confirmación de recepción para el proveedor

---

### 🟨 Semana 7 – *5 al 9 de agosto*
- Evaluación de propuestas (panel del comité evaluador)
- Ingreso de puntajes y generación de actas
- Inicio de pruebas funcionales del flujo completo

---

### 🟦 Semana 8 – *12 al 16 de agosto*
- Pruebas QA completas de todos los módulos
- Corrección de errores y validaciones cruzadas
- Pruebas de carga básicas (múltiples usuarios)

---

### 🟦 Semana 9 – *19 al 23 de agosto*
- Validaciones legales finales del proceso
- Integración de mejoras tras feedback QA/stakeholders
- Revisión de logs, auditoría y validación de integridad

---

### 🟦 Semana 10 – *26 al 30 de agosto*
- Documentación técnica y manual de uso
- Preparación de backups, errores críticos y monitoreo
- Configuración final del entorno de producción

---

### 🚀 Semana 11–12 – *30 agosto al 1 septiembre*
- **Despliegue oficial**
- **Capacitación interna**
- **Entrega final y cierre del proyecto**

---

## 📌 Consideraciones

- Reuniones de seguimiento técnico y funcional semanales
- Validaciones internas cada 2 semanas
- Uso de GitHub Projects, Jira o Trello para gestión ágil
- Seguridad y pruebas de acceso crítico a partir de semana 7

---

## 📘 Entregables por Fase

- Arquitectura técnica y diagramas (semana 1)
- MVP funcional completo (semana 7)
- Plataforma probada y documentada (semana 10)
- Versión final operativa (1 de septiembre de 2025)
