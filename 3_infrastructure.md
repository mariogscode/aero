# 🛠️ Plan de Infraestructura – Plataforma de Concursos Comerciales AVIACIÓN (Despliegue en AWS con Cognito)

Este documento describe los recursos de infraestructura en la nube necesarios para desplegar la plataforma de gestión de concursos comerciales en el sector de aviación utilizando **Amazon Web Services (AWS)**. Incluye soporte para autenticación y autorización mediante **Amazon Cognito**.

---

## ☁️ Recursos en AWS

### 1. 🖥️ Servidor de Aplicaciones (Frontend + Backend)
- **Servicio:** Amazon EC2
- **Instancias recomendadas:**
  - Desarrollo: `t3.medium` (2 vCPU, 4 GB RAM)
  - Producción: `t3.large` o `m5.large` (4 vCPU, 8 GB RAM)
- **Sistema Operativo:** Ubuntu 22.04 LTS
- **Stack de despliegue:** Docker + Uvicorn + Gunicorn
- **Costo estimado:** ~35–70 USD/mes

---

### 2. 🗄️ Base de Datos Relacional
- **Servicio:** Amazon RDS para PostgreSQL
- **Tipo de instancia:** `db.t3.medium` o `db.t3.large`
- **Almacenamiento:** 20–50 GB SSD
- **Backups:** Respaldos automáticos diarios
- **Costo estimado:** ~50–120 USD/mes

---

### 3. 📁 Almacenamiento de Archivos
- **Servicio:** Amazon S3
- **Configuración del bucket:** Privado, con versionado y políticas de ciclo de vida
- **Uso:** Almacenamiento seguro de documentos de licitación (PDF, DOCX, XLSX)
- **Acceso:** Subida y descarga mediante URLs pre-firmadas
- **Costo estimado:** ~5 USD/mes

---

### 4. 🔐 Autenticación y Autorización
- **Servicio:** Amazon Cognito
- **Componentes:**
  - **User Pool:** Registra y autentica usuarios, con soporte para MFA, recuperación de contraseña, verificación por correo.
  - **App Client:** Genera tokens de acceso e identificación (JWT) para el frontend.
  - **Hosted UI (opcional):** Interfaz de login basada en OAuth2.
- **Frontend:** Integración con AWS Amplify o la librería `amazon-cognito-identity-js`.
- **Backend (FastAPI):**
  - Verifica los tokens JWT mediante el JWKS endpoint de Cognito.
  - Aplica control de acceso por roles.
- **Seguridad adicional:** Verificación por correo, soporte para login federado (Google, SAML).
- **Costo estimado:** Gratis para los primeros 50,000 usuarios activos por mes.

---

### 5. 📬 Notificaciones por Correo
- **Servicio:** Amazon SES (Simple Email Service)
- **Uso:** Envío automático de correos a proveedores (registro, cambios, recordatorios).
- **Requisito:** Dominio verificado en DNS.
- **Costo estimado:** Gratis hasta 62,000 correos/mes si se envía desde EC2.

---

### 6. 🔄 CI/CD (Integración y Despliegue Continuos)
- **Control de versiones:** GitHub
- **Automatización:** GitHub Actions
- **Despliegue:** Build con Docker, deploy por SSH a EC2
- **Alternativa:** AWS CodeDeploy, ECS o Amplify Hosting

---

### 7. 📦 Gestión del Proyecto e Incidentes
- **Herramientas recomendadas:**
  - **GitHub Issues:** Seguimiento de bugs y tareas técnicas.
  - **Jira:** Gestión de sprints e incidencias (gratis hasta 10 usuarios).
  - **Trello:** Gestión visual estilo Kanban.

---

## 🧰 Mejoras Opcionales

| Funcionalidad | Servicio AWS | Propósito |
|---------------|--------------|-----------|
| 🔍 Logs | CloudWatch Logs | Registro de logs del backend y frontend |
| 📈 Monitoreo | CloudWatch / Grafana | Visualización de métricas de rendimiento |
| 🛡️ Seguridad | AWS WAF | Protección contra ataques web comunes |
| 📊 Pruebas de Carga | EC2 + JMeter | Simulación de múltiples usuarios simultáneos |

---

## 💰 Costo Estimado Mensual (Producción)

| Recurso | Costo estimado |
|---------|----------------|
| EC2 (Servidor de Aplicaciones) | ~70 USD |
| RDS (Base de Datos) | ~80 USD |
| S3 (Almacenamiento) | ~5 USD |
| SES (Correos) | ~5 USD |
| Cognito | Gratis (hasta 50,000 usuarios activos) |
| Route 53 + ACM | ~1–2 USD |
| **Total aproximado** | **160–200 USD/mes** |

---

## 📝 Flujo de Autenticación con Cognito

### ➕ Registro e Inicio de Sesión
- Gestionado por el **User Pool de Cognito**
- El usuario se registra desde el frontend
- Recibe correo de verificación
- Cognito devuelve tokens de acceso e identificación (ID Token + Access Token)
