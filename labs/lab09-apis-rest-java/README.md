# Lab 09 — APIs REST y Java

## 🎯 Objetivo

Aprender a interactuar con el motor Camunda utilizando **la API Java** y **la API REST**.

En este laboratorio se aprenderá a:

* iniciar procesos desde código Java
* utilizar los servicios del motor Camunda
* interactuar con el motor mediante API REST
* consultar instancias de proceso

---

# 🧠 Contexto

El motor Camunda puede controlarse desde distintos tipos de interfaces.

Las dos más importantes son:

```text id="a4h7j1"
Java API
REST API
```

La **Java API** se utiliza cuando el motor está embebido dentro de una aplicación.

Ejemplo:

```text id="f7k2d8"
RuntimeService
TaskService
RepositoryService
```

La **REST API** permite interactuar con el motor desde sistemas externos.

Ejemplo:

```text id="m6q1z4"
iniciar procesos
consultar instancias
gestionar tareas
```

Esto permite integrar Camunda con otras aplicaciones o microservicios.

---

# 🔎 Qué vamos a hacer en este laboratorio

Se explorarán dos formas de interactuar con el motor:

1. Desde **código Java dentro de la aplicación**
2. Desde **peticiones HTTP a la API REST**

Esto permitirá controlar los procesos desde diferentes puntos del sistema.

---

# 📘 Ejercicios del laboratorio

### 01 — RuntimeService

Explorar el servicio que permite iniciar procesos desde Java.

Archivo:

```text id="p8w3g6"
01-runtime-service.md
```

---

### 02 — Iniciar procesos desde Java

Crear código que inicie una instancia de proceso.

Archivo:

```text id="k2v4t1"
02-iniciar-procesos-java.md
```

---

### 03 — API REST de Camunda

Interactuar con el motor utilizando peticiones HTTP.

Archivo:

```text id="d9n6r5"
03-rest-api-camunda.md
```

---

### 04 — Consultar instancias

Consultar instancias de proceso activas utilizando la API REST.

Archivo:

```text id="s5x8y2"
04-consultar-instancias.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá cómo:

```text id="h3f7v1"
iniciar procesos desde código
interactuar con el motor mediante HTTP
consultar información del workflow
```

Esto permite integrar el motor Camunda con **otras aplicaciones y servicios**.

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se trabajará con **gestión de errores, reintentos e incidentes**, permitiendo crear procesos más robustos y resilientes.
