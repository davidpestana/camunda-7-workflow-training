# Lab 10 — Errores e incidentes

## 🎯 Objetivo

Aprender a gestionar **errores de negocio y errores técnicos** dentro de procesos BPMN ejecutados por Camunda.

En este laboratorio se aprenderá a:

* manejar errores BPMN dentro del flujo del proceso
* entender cómo funcionan los reintentos automáticos del motor
* analizar incidentes generados por fallos técnicos
* utilizar compensaciones para revertir operaciones

---

# 🧠 Contexto

En procesos reales siempre pueden ocurrir errores.

Estos errores pueden ser de dos tipos:

```text id="p9c7z1"
errores de negocio
errores técnicos
```

Los **errores de negocio** representan situaciones esperadas dentro del proceso.

Ejemplo:

```text id="q5t2x8"
importe demasiado alto
datos inválidos
solicitud rechazada
```

Estos errores se gestionan dentro del modelo BPMN mediante **BPMN Error Events**.

---

Los **errores técnicos** representan fallos del sistema.

Ejemplo:

```text id="r8d4m3"
fallo en una API
error de base de datos
problema de red
```

El motor Camunda gestiona estos errores mediante:

```text id="k6y1n7"
reintentos automáticos
incidentes
```

Esto permite crear procesos robustos capaces de recuperarse de fallos.

---

# 🔎 Qué vamos a hacer en este laboratorio

Se ampliará el proceso de aprobación para introducir distintos escenarios de error.

Durante los ejercicios se aprenderá a:

```text id="n2g6v9"
capturar errores BPMN
provocar fallos técnicos
analizar incidentes en Cockpit
revertir acciones mediante compensaciones
```

Esto permitirá entender cómo el motor gestiona situaciones de error.

---

# 📘 Ejercicios del laboratorio

### 01 — Errores BPMN

Gestionar errores de negocio dentro del flujo del proceso.

Archivo:

```text id="w4j7k3"
01-errores-bpmn.md
```

---

### 02 — Retry de jobs

Provocar un error técnico y observar los reintentos automáticos del motor.

Archivo:

```text id="x2c8h5"
02-retry-jobs.md
```

---

### 03 — Incidentes

Analizar cómo Camunda crea incidentes cuando una tarea falla repetidamente.

Archivo:

```text id="v6n1y4"
03-incidentes.md
```

---

### 04 — Compensaciones

Implementar mecanismos de compensación para revertir operaciones previas.

Archivo:

```text id="p7z0f8"
04-compensaciones.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá cómo Camunda gestiona errores dentro de un proceso.

El sistema será capaz de:

```text id="j3m5s2"
manejar errores de negocio
reintentar tareas automáticamente
detectar incidentes
revertir operaciones mediante compensaciones
```

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se explorarán las herramientas de **operación del motor Camunda**, utilizadas para administrar y monitorizar procesos en ejecución.
