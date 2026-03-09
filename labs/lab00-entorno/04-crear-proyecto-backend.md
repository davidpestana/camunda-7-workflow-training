# Crear el proyecto workflow-app

## 🎯 Objetivo

Generar el proyecto **workflow-app** con **Maven** (`mvn archetype:generate`) usando el archetype de Camunda para Spring Boot. Luego validarás que compila (paso 05) y arranca (paso 06); en el **lab03** revisarás y validarás las dependencias hasta dejar el proyecto listo para los labs.

---

## 📍 Generar el proyecto

En la **raíz del repositorio**, ejecuta:

```bash
mvn archetype:generate \
  -DarchetypeGroupId=org.camunda.bpm.archetype \
  -DarchetypeArtifactId=camunda-archetype-spring-boot \
  -DarchetypeVersion=7.19.0 \
  -DgroupId=com.example.workflow \
  -DartifactId=workflow-app \
  -Dversion=1.0-SNAPSHOT \
  -Dpackage=com.example.workflow \
  -DinteractiveMode=false
```

Maven crea la carpeta **workflow-app** con el proyecto (pom, **src**, clase principal, etc.). Si el archetype generara el contenido en el directorio actual en lugar de en una subcarpeta, mueve los archivos a una carpeta **workflow-app** para mantener la estructura del curso.

---

## ✅ Comprobación

* Existe **workflow-app** con **pom.xml** y **src**.

En el **paso 05** compilarás; en el **06** arrancarás. En el **lab03** validarás las dependencias (y las ajustarás si hace falta) hasta que compile y arranque correctamente.
