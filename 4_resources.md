# 👥 Estimación de Recursos – Desarrollo con 2 Personas

Este documento detalla el enfoque, alcance y riesgos para desarrollar la **Plataforma de Concursos Comerciales AVIACIÓN** con solo **2 desarrolladores full stack** trabajando a tiempo completo, durante **9 semanas**, con fecha de entrega el **1 de septiembre de 2025**.

---

## ✅ ¿Es viable el desarrollo con solo 2 personas?

Sí, pero bajo las siguientes condiciones:

- Ambos desarrolladores deben ser **full stack** con experiencia en:
  - React (frontend)
  - FastAPI + PostgreSQL (backend)
  - AWS (Cognito, S3, SES, RDS)
  - Docker y GitHub Actions
- Ambos deben estar **100% dedicados durante 9 semanas**
- Se debe limitar el desarrollo al **MVP estricto**, postergando funcionalidades secundarias

---

## 📦 Alcance funcional viable

| Módulo | ¿Incluido? | Comentario |
|--------|------------|------------|
| Inscripción de proveedores | ✅ | Flujo completo con validación y notificación |
| Acceso a documentación | ✅ | Con trazabilidad básica y permisos por proveedor |
| Entrega de sobres (doble sobre) | ✅ | Separación técnica/económica, sin cifrado complejo |
| Gestión de consultas | ✅ | Simple, con validación interna básica |
| Evaluación y adjudicación | ✅ | Ingreso manual de puntajes, resultados |
| Auditoría y trazabilidad | 🔸 Parcial | Registro de acciones clave únicamente |
| Reportes o dashboards | ❌ | Pospuestos para una segunda fase |
| Firma digital avanzada | ❌ | Requiere integración externa (fuera del alcance actual) |

---

## 📅 Cronograma resumido (para 2 personas)

| Semana | Actividades |
|--------|------------|
| 1 | Setup, arquitectura, auth Cognito, base UI |
| 2 | Registro de proveedores + envío de correos (SES) |
| 3 | Documentación: subida, descarga, control por proveedor |
| 4 | Consultas y respuestas (frontend + backend) |
| 5 | Entrega digital de ofertas (doble sobre) |
| 6 | Evaluación de propuestas, notificación de resultados |
| 7 | Correcciones, validaciones internas, checklist QA |
| 8 | Seguridad, revisión de trazabilidad, entorno final |
| 9 | Documentación, despliegue final, capacitación básica |

---

## 👨‍💻 Roles por Recurso

| Área | Recurso 1 | Recurso 2 |
|------|-----------|-----------|
| Backend (FastAPI, PostgreSQL) | ✅ | ✅ |
| Frontend (React) | ✅ | ✅ |
| AWS (S3, Cognito, SES, RDS) | ✅ | ✅ |
| CI/CD + Docker | ✅ | ✅ |
| Testing funcional | 🔄 Compartido | 🔄 Compartido |
| Validación funcional con stakeholders | 🔄 Compartido | 🔄 Compartido |

---

## ⚠️ Riesgos y Recomendaciones

| Riesgo | Mitigación |
|--------|------------|
| Sobrecarga de trabajo | Enfocarse en el MVP real |
| Ausencia de QA/Testers | Pruebas cruzadas entre desarrolladores |
| Diseño limitado | Uso de UI kits (ej. MUI, Bootstrap, ShadCN) |
| Falta de tiempo para pruebas | Agendar días específicos de validación |
| Bugs en producción | Pruebas completas en staging antes del go-live |

---

## 🧰 Herramientas Recomendadas

- **UI Kits:** MUI, Bootstrap o ShadCN para evitar diseñar desde cero
- **Testing manual:** Postman, Swagger UI, validación funcional interna
- **Gestión del proyecto:** GitHub Projects o Trello
- **CI/CD:** GitHub Actions + Docker
- **Documentación:** Markdown (`/docs`) o Notion

---

## 💵 Estimación de Costo – Recurso Backend

El recurso backend estima dedicar aproximadamente 78 horas al proyecto.

Tarifa por hora: $46 USD

Costo total estimado: $3,588 USD
