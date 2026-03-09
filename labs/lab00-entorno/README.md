# lab00 — Entorno

## Objetivo

Preparar el **entorno de desarrollo** y crear el proyecto **workflow-app** paso a paso con un **pom probado**, de forma que el curso sea reproducible (incluido en **GitHub Codespaces**) y se eviten problemas de dependencias o versiones.

## Línea de trabajo del alumno

1. **01** — Instalar extensiones de VS Code (Java, Maven, Spring Boot, BPMN, Camunda).
2. **02** — Verificar Java 17 (requerido por el pom del curso).
3. **03** — Verificar Maven (compilar y ejecutar el proyecto).
4. **04** — Crear el proyecto **workflow-app** con **base mínima** (carpeta, pom con solo web + test, clase principal, application.properties con puerto, test). Sin Camunda todavía.
5. **05** — Compilar el proyecto y **validar** (`mvn clean install`).
6. **06** — Arrancar la aplicación y **validar** (`mvn spring-boot:run`). Por ahora solo servidor web.
7. **07** — Explorar la estructura del repositorio.

En el **lab03** el alumno irá **añadiendo** al pom las dependencias (Camunda, JPA, H2) **una a una** y **validando** tras cada cambio, hasta tener el mismo pom probado del curso.

## Entorno

- **Java 17** y **Maven** son obligatorios; los pasos 02 y 03 los comprueban antes de crear el proyecto.
- En **Codespaces**, Java y Maven suelen estar preinstalados; aun así conviene ejecutar 02 y 03 para detectar problemas desde el inicio.
- El **pom** se construye paso a paso (base en lab00; Camunda, JPA, H2 en lab03), validando en cada paso como en un proceso real de instalación.

## Resultado esperado

Al final del lab00 el alumno tiene:

- Entorno verificado (Java 17, Maven).
- Proyecto **workflow-app** con base mínima (solo web), compilado y arrancado.
- Conocimiento de la estructura del repositorio (workflow-app, labs, docs, model).
