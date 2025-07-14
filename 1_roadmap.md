# 🗓️ Cronograma de Desarrollo – Plataforma Concursos Comerciales AVIACIÓN

Este documento detalla el cronograma de desarrollo del MVP de la plataforma de concursos

---

## 📑 Índice

- [✅ Resumen General](#-resumen-general)
- [📅 Cronograma por Semana](#-cronograma-por-semana)
- [📌 Consideraciones](#-consideraciones)
- [📘 Entregables por Fase](#-entregables-por-fase)

---

## ✅ Resumen General
🟡 Esto es bajo el supuesto de que los recursos esten dedicados 100%

🟡 Este analisis esta fundamentado principalmente en el recurso de backend.

| Fase  | Objetivos | Dias | 
|------ |-----------|------|
| 1. Diseño y Preparación | Infraestructura, diseño UI/UX, arquitectura técnica | 4 | 184
| 2. Desarrollo Base | Autenticación, inscripción, acceso seguro a documentos | 18 | 826
| 3. Funcionalidades Clave | Consultas, entrega digital de ofertas, evaluación | 18 | 826
| 4. Integración + QA | Pruebas funcionales, mejoras, validaciones finales | 18 | 826
| 5. Cierre y Release | Despliegue, documentación, capacitación y entrega | 2 | 92
| TOTAL | |60|

---

## 📅 Cronograma por Semana

### 🟨 Semana 1 – 4 dias
- Diseño de arquitectura técnica (infraestructura, backend, seguridad)
- Configuración inicial de AWS (Cognito, S3, RDS, SES)
- Diseño de UI/UX (flujos: inscripción, entrega, consulta)
- Estructura de repositorio + CI/CD base (GitHub Actions, Docker)

---

### 🟩 Semana 2 – 4 dias
- Módulo de inscripción de proveedores
- Integración de autenticación con Cognito (frontend + backend)
- Inicio de sistema de roles y permisos básicos

---

### 🟩 Semana 3 – 4 dias
- Subida de documentos al portal del proveedor
- Descarga protegida con pre-signed URLs (AWS S3)
- Registro de descargas por proveedor (auditoría básica)

---

### 🟩 Semana 4 – 4 dias
- Revisión y prueba del flujo de inscripción
- Implementación de correos automáticos (confirmaciones)
- Desarrollo inicial del módulo de consultas y respuestas

---

### 🟨 Semana 5 – 4 dias
- Consola de gestión de consultas (usuario interno)
- Flujo de validación legal/técnica y publicación de respuestas
- Inicio de módulo de entrega de ofertas (doble sobre)

---

### 🟨 Semana 6 – 4 dias
- Finalización de carga de sobres técnicos y económicos
- Validaciones y firma digital de la entrega
- Confirmación de recepción para el proveedor

---

### 🟨 Semana 7 – 4 dias
- Evaluación de propuestas (panel del comité evaluador)
- Ingreso de puntajes y generación de actas
- Inicio de pruebas funcionales del flujo completo

---

### 🟦 Semana 8 – 4 dias
- Pruebas QA completas de todos los módulos
- Corrección de errores y validaciones cruzadas
- Pruebas de carga básicas (múltiples usuarios)

---

### 🟦 Semana 9 – 4 dias
- Validaciones legales finales del proceso
- Integración de mejoras tras feedback QA/stakeholders
- Revisión de logs, auditoría y validación de integridad

---

### 🟦 Semana 10 – 4 dias
- Documentación técnica y manual de uso
- Preparación de backups, errores críticos y monitoreo
- Configuración final del entorno de producción

---

### 🚀 Semana 11–12 – 1 dia
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
  
➡️ [Volver al inicio](./README.md)
