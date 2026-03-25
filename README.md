# 🚀 App Serverless CI/CD con AWS SAM y GitHub Actions

📌 Descripción:

Este proyecto implementa una aplicación serverless en AWS utilizando AWS SAM (Serverless Application Model) y un pipeline de CI/CD automatizado con GitHub Actions.

El objetivo es demostrar buenas prácticas de DevSecOps y automatización, incluyendo validaciones, análisis de seguridad, despliegue continuo y validación post deploy.

# 🧱 Arquitectura

La solución está compuesta por:
	•	AWS Lambda → Función backend
	•	Amazon API Gateway → Exposición del endpoint HTTP
	•	AWS CloudFormation (SAM) → Infraestructura como código 
	•	GitHub Actions → Pipeline CI/CD

# ⚙️ Flujo del Pipeline

El pipeline está dividido en tres etapas principales: 

## 🧪 1. Validate & Security Checks
    •	Descargar el repositorio
    •	Validación del template 
    •	Litting de la infraestructura 
    •	Escaneo de seguridad utilizando Chevkov

## 🏗️ 2. Build

    •   Construcción de la aplicación
    •   Generación del artefacto:
    •   Guardar el artefacto en memoria - github actions

## 🚀 3. Deploy

    •   Descargar el artefacto guardado
    •   Ejecución de comando para el deploy
    •   Autenticación con cuenta AWS
    •   Despliegue SAM.

