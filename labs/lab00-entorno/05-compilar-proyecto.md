# Compilar el proyecto

## 🎯 Objetivo

Compilar la aplicación backend (**workflow-app**) utilizando **Maven** para verificar que el proyecto puede construirse correctamente.

---

## 🧠 Contexto

En el paso anterior creaste el proyecto **workflow-app**. En este paso lo compilas para comprobar que el entorno funciona. Solo necesitas ejecutar el comando de Maven; el resto del proyecto Maven (estructura, fases, etc.) se explora en el **lab03**.

---

## 📍 Ir al directorio workflow-app

Abre una **terminal** en VS Code (menú **Terminal** → **New Terminal**). Desde la **raíz del repositorio** (donde están el README, las carpetas **labs** y **workflow-app**), cambia al directorio del proyecto:

```bash
cd workflow-app
```

---

## 🔧 Compilar el proyecto

Ejecutar el siguiente comando:

```bash
mvn clean install
```

---

## 📌 Nota

La primera compilación puede tardar unos minutos (Maven descargará dependencias). Si todo va bien verás **BUILD SUCCESS**. En el **lab03** explorarás la estructura del proyecto Maven y qué hace cada parte.

---

## 📌 Resultado esperado

Si la compilación es correcta, al final de la ejecución aparecerá un mensaje similar a:

```
BUILD SUCCESS
```

---

## 📁 Directorio generado

Después de compilar, Maven creará el directorio:

```
target/
```

Este directorio contiene los artefactos generados durante la compilación.

---

## 🔎 Verificar el resultado

Puedes comprobar el contenido generado ejecutando:

```bash
ls target
```

Debería aparecer un archivo `.jar` correspondiente a la aplicación.

---

## ⚠️ Si la compilación falla

* Comprueba que estás **dentro** de `workflow-app` y que **Java 17** y **Maven** están bien (pasos 02 y 03).
* **Workaround:** Si el error está relacionado con la versión de Spring Boot o del parent, abre **workflow-app/pom.xml** y revisa el `<parent>`: debe ser `spring-boot-starter-parent` con **version 2.7.18**. Si el archetype generó otra (p. ej. 3.x), cámbiala a **2.7.18**. Revisa también que `<java.version>` sea **17**. Guarda y ejecuta de nuevo `mvn clean install`.

---

## ✅ Comprobación

El paso se considera completado cuando:

* el comando `mvn clean install` finaliza correctamente
* aparece el mensaje **BUILD SUCCESS**
* existe el directorio `target` en el proyecto workflow-app.
