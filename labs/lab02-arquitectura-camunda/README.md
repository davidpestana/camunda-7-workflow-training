# Lab 02 — Arquitectura de Camunda

## 🎯 Objetivo

Comprender cómo está construido **Camunda Process Engine** y cómo ejecuta los procesos BPMN dentro de una aplicación.

En este laboratorio se aprenderá a:

* identificar los componentes del motor Camunda
* entender cómo se integra el motor dentro de una aplicación Spring Boot
* explorar los servicios principales del motor
* comprender el ciclo de ejecución de un proceso

---

# 🧠 Contexto

Cuando un modelo BPMN se ejecuta en Camunda, el proceso es gestionado por el **Process Engine**.

El motor es responsable de:

```id="x4r1w7"
ejecutar procesos BPMN
gestionar el estado de las instancias
persistir información en la base de datos
coordinar tareas humanas y automatizadas
gestionar eventos y temporizadores
```

El motor funciona como una **máquina de ejecución de procesos**.

---

# 🏗 Arquitectura general

En una aplicación típica basada en Camunda, los componentes principales son:

```id="r2y8d1"
Aplicación Spring Boot
        │
        ▼
Camunda Process Engine
        │
        ▼
Base de datos
```

El **Process Engine** interpreta los modelos BPMN y controla la ejecución del flujo.

---

# 🔧 Servicios principales del motor

El motor expone diferentes servicios para interactuar con los procesos.

Algunos de los más importantes son:

```id="n5z6p9"
RuntimeService
TaskService
RepositoryService
HistoryService
ManagementService
```

Cada uno se encarga de una parte del funcionamiento del sistema.

Por ejemplo:

```id="j3v0f2"
RuntimeService → iniciar procesos
TaskService → gestionar tareas humanas
RepositoryService → gestionar modelos BPMN
HistoryService → consultar historial
```

En los siguientes laboratorios se utilizarán estos servicios desde código Java.

---

# 📂 Qué se explorará en este laboratorio

En lugar de limitarse a leer documentación, en este laboratorio se explorará el motor directamente desde el código de la aplicación.

Se realizarán ejercicios para:

```id="g7k4p8"
identificar servicios del motor
analizar cómo se ejecuta un proceso
entender el ciclo de vida de una instancia
```

---

# 📘 Ejercicios del laboratorio

Este laboratorio contiene los siguientes pasos.

---

### 01 — Arquitectura general

Exploración de los componentes principales de Camunda.

Archivo:

```id="y4d1v6"
01-arquitectura-general.md
```

---

### 02 — Componentes del motor

Exploración de los servicios principales del Process Engine desde código Java.

Archivo:

```id="s9h8x2"
02-componentes-del-motor.md
```

---

### 03 — Motor embebido vs standalone

Comprender los distintos modos de despliegue del motor Camunda.

Archivo:

```id="q1k2b5"
03-motor-embebido-vs-standalone.md
```

---

### 04 — Ciclo de ejecución

Análisis de cómo el motor ejecuta una instancia de proceso paso a paso.

Archivo:

```id="m3t6r9"
04-ciclo-de-ejecucion.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá:

```id="f7v1y3"
cómo se integra Camunda en una aplicación
qué componentes forman el motor
cómo se ejecuta un proceso BPMN
```

Esto permitirá entender qué ocurre internamente cuando un proceso se ejecuta.

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se instalará y configurará el **motor Camunda dentro de la aplicación Spring Boot**.
