# Arrancar la aplicación

## 🎯 Objetivo

Ejecutar la aplicación **Spring Boot** (workflow-app) para verificar que el backend se inicia correctamente.

---

## 🧠 Contexto

En el paso 04 generaste **workflow-app** con el archetype de Camunda. Al arrancar puede que la aplicación inicie el servidor (y el motor, si el archetype incluyó ya la configuración de BD) o que falle por falta de configuración de base de datos. **Si no arranca**, lo normal; en el **lab03** configurarás las dependencias y **application.properties** y la aplicación arrancará correctamente.

---

## 📍 Ir al directorio workflow-app

Abre una **terminal** en VS Code (menú **Terminal** → **New Terminal**). Desde la **raíz del repositorio** (donde están README, **labs** y **workflow-app**), ejecuta:

```bash
cd workflow-app
```

---

## ▶️ Ejecutar la aplicación

Ejecutar el siguiente comando:

```bash
mvn spring-boot:run
```

---

## 📦 Qué ocurre al arrancar

Ejecuta `mvn spring-boot:run`. Si arranca, verás el servidor (y el motor Camunda si ya está configurado).

**Si no arranca** (p. ej. error de datasource o de configuración de BD): abre **workflow-app/src/main/resources/application.properties** y asegúrate de tener al menos esta configuración (añade lo que falte):

```properties
server.port=8080

spring.datasource.url=jdbc:h2:mem:camunda;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update
```

Guarda y ejecuta de nuevo `mvn spring-boot:run`. En el **lab03** revisarás el pom y esta configuración con más detalle.

---

## 📌 Puerto de ejecución

La aplicación se ejecutará en el puerto:

```
8080
```

---

## 🔎 Verificar que la aplicación está funcionando

Abre un **navegador** y en la barra de direcciones escribe:

```
http://localhost:8080
```

Si la aplicación está en ejecución el servidor responderá a las peticiones.

---

## ⚠️ Detener la aplicación

Para detener la aplicación desde la terminal presionar:

```
CTRL + C
```

---

## ✅ Comprobación

El paso se considera completado cuando has ejecutado `mvn spring-boot:run`. Si **arranca**, comprueba que escucha en el puerto **8080**. Si **no arrancaba** y aplicaste el workaround de **application.properties** (H2), vuelve a arrancar hasta que inicie correctamente.
