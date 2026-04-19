# lab22026v
[![CI/CD Pipeline](https://github.com/laboratorio2arquitectura/Lab-2-Arquitectura-de-sofware/actions/workflows/build.yml/badge.svg)](https://github.com/laboratorio2arquitectura/Lab-2-Arquitectura-de-sofware/actions/workflows/build.yml)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware&metric=bugs)](https://sonarcloud.io/summary/new_code?id=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware)
[![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware&metric=coverage)](https://sonarcloud.io/summary/new_code?id=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=laboratorio2arquitectura_Lab-2-Arquitectura-de-sofware)


# LAB2026V - Aplicación de Generación de Datos Aleatorios

Aplicación desarrollada con Spring Boot que expone servicios REST para la generación de datos aleatorios. Este proyecto hace parte de un laboratorio de CI/CD e integra herramientas de calidad de código y automatización.

---

## Funcionalidades

La aplicación permite:

- Obtener países aleatorios
- Obtener monedas aleatorias
- Obtener datos de aviación
- Consultar la versión de la aplicación
- Verificar el estado del servicio (health check)

---

## Tecnologías utilizadas

- Java 11
- Spring Boot
- Maven
- Docker
- GitHub Actions
- SonarCloud
- JaCoCo
- Coveralls
- Snyk

---

## Estructura del proyecto

```
lab22026v/
├── .github/workflows/build.yml
├── src/main/java/com/udea/lab2026v
│   ├── Application.java
│   └── DataController.java
├── src/test/java/com/udea/lab2026v
│   └── ApplicationTests.java
├── src/main/resources/
├── Dockerfile
├── pom.xml
└── README.md
```

---

## Cómo ejecutar la aplicación

### Requisitos

- Java 11
- Maven

### Ejecución en local

```bash
mvn clean spring-boot:run
```

---

## Endpoints disponibles

Una vez ejecutada la aplicación:

- http://localhost:8080/ → Health check  
- http://localhost:8080/version → Versión  
- http://localhost:8080/nations → Países  
- http://localhost:8080/currencies → Monedas  
- http://localhost:8080/aircraft → Aviación  

---

## Ejecución de pruebas

```bash
mvn test
```

---

## Cobertura de código

```bash
mvn clean verify
```

El reporte se genera en:

```
target/site/jacoco/index.html
```

---

## Construcción del proyecto

```bash
mvn clean package
```

---

## Uso con Docker

### Construir imagen

```bash
docker build -t lab2026v:latest .
```

### Ejecutar contenedor

```bash
docker run -p 8080:8080 lab2026v:latest
```

---

## Integración CI/CD

El proyecto incluye:

- Ejecución automática de pruebas
- Análisis de calidad de código
- Reporte de cobertura
- Escaneo de vulnerabilidades
- Pipeline automatizado con GitHub Actions

---

## Configuración de SonarCloud

Configurar el siguiente secret en GitHub:

- SONAR_TOKEN

Y definir en el archivo `pom.xml`:

```xml
sonar.organization=TU_ORGANIZACION
sonar.projectKey=TU_PROJECT_KEY
```

---

## Objetivo del proyecto

Este laboratorio tiene como propósito:

- Implementar un pipeline de integración continua
- Evaluar la calidad del código
- Automatizar pruebas
- Desplegar aplicaciones usando contenedores

---
