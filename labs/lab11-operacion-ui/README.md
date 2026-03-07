# Lab 11 — Operación del motor Camunda

## 🎯 Objetivo

Aprender a utilizar las herramientas de Camunda para **operar, administrar y monitorizar procesos en ejecución**.

En este laboratorio se aprenderá a:

* utilizar **Cockpit** para analizar procesos
* utilizar **Tasklist** para gestionar tareas humanas
* utilizar **Admin** para gestionar usuarios y grupos
* inspeccionar instancias de proceso en ejecución

---

# 🧠 Contexto

Camunda incluye varias aplicaciones web que permiten operar el motor de procesos.

Las principales son:

```text
Cockpit
Tasklist
Admin
```

Cada una tiene un propósito diferente dentro del sistema.

---

# 🖥 Cockpit

**Cockpit** es la herramienta utilizada para **monitorizar procesos y diagnosticar problemas**.

Permite:

```text
ver procesos desplegados
analizar instancias activas
inspeccionar variables
identificar incidentes
analizar jobs del motor
```

Esta herramienta suele ser utilizada por **operadores o administradores del sistema**.

---

# 📋 Tasklist

**Tasklist** es la aplicación utilizada por **usuarios de negocio** para trabajar con tareas humanas.

Permite:

```text
ver tareas pendientes
reclamar tareas
completar formularios
avanzar procesos
```

Cuando un proceso llega a una **User Task**, la tarea aparece en Tasklist.

---

# ⚙ Admin

**Admin** permite gestionar la seguridad del sistema.

Permite administrar:

```text
usuarios
grupos
permisos
autorizaciones
```

Esto permite controlar quién puede interactuar con procesos o tareas.

---

# 🔎 Qué vamos a hacer en este laboratorio

En este laboratorio se explorarán las aplicaciones de operación de Camunda para comprender cómo se gestiona un sistema de workflow en funcionamiento.

Durante los ejercicios se aprenderá a:

```text
analizar procesos desde Cockpit
gestionar tareas desde Tasklist
administrar usuarios y grupos
inspeccionar instancias de proceso
```

---

# 📘 Ejercicios del laboratorio

### 01 — Explorar Cockpit

Aprender a visualizar procesos y analizar su estado desde Cockpit.

Archivo:

```text
01-explorar-cockpit.md
```

---

### 02 — Explorar Tasklist

Gestionar tareas humanas desde Tasklist.

Archivo:

```text
02-explorar-tasklist.md
```

---

### 03 — Explorar Admin

Administrar usuarios y grupos desde la herramienta Admin.

Archivo:

```text
03-explorar-admin.md
```

---

### 04 — Inspección de instancias

Analizar instancias de proceso en ejecución.

Archivo:

```text
04-inspeccion-instancias.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá cómo operar un sistema basado en Camunda.

Se podrá:

```text
monitorizar procesos
gestionar tareas humanas
administrar usuarios
analizar instancias en ejecución
```

Estas herramientas son esenciales para operar workflows en entornos reales.

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se explorará cómo **integrar procesos BPMN con sistemas externos**, como bases de datos, APIs o servicios distribuidos.
