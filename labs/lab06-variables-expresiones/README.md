# Lab 06 — Variables y expresiones

## 🎯 Objetivo

Comprender cómo los procesos BPMN gestionan **datos mediante variables** y cómo estas variables pueden utilizarse en el flujo del proceso.

En este laboratorio se aprenderá a:

* crear y utilizar variables de proceso
* modificar variables desde código Java
* utilizar expresiones dentro del modelo BPMN
* trabajar con formularios en tareas humanas
* verificar las variables durante la ejecución del proceso

---

# 🧠 Contexto

Los procesos BPMN no solo definen el flujo de actividades, también gestionan **información del proceso**.

Esta información se almacena en **variables de proceso**.

Ejemplos de variables:

```text id="4i5v7y"
solicitante
importe
tipoSolicitud
estadoSolicitud
aprobada
```

Estas variables permiten que el proceso:

* tome decisiones
* pase información entre tareas
* interactúe con usuarios o sistemas externos

---

# 🔎 Qué vamos a hacer en este laboratorio

En este laboratorio se ampliará el proceso de aprobación para trabajar con **datos reales del proceso**.

Durante la ejecución del proceso:

* se crearán variables
* se modificarán desde código Java
* se utilizarán en formularios
* se inspeccionarán desde Cockpit

Esto permitirá entender cómo los procesos gestionan información.

---

# 📘 Ejercicios del laboratorio

### 01 — Variables de proceso

Introducción a las variables utilizadas dentro de un proceso BPMN.

Archivo:

```text id="k5p0u2"
01-variables-proceso.md
```

---

### 02 — Modificar variables desde Java

Modificar variables dentro de un `JavaDelegate`.

Archivo:

```text id="x8s4t9"
02-setear-variables-java.md
```

---

### 03 — Expresiones EL

Utilizar expresiones para acceder a variables dentro del modelo BPMN.

Archivo:

```text id="b9e7w3"
03-expresiones-el.md
```

---

### 04 — Formularios

Utilizar formularios en tareas humanas para introducir datos en el proceso.

Archivo:

```text id="c1n6z8"
04-formularios.md
```

---

### 05 — Verificación de variables

Inspeccionar las variables del proceso utilizando Cockpit.

Archivo:

```text id="s7k2d5"
05-verificacion-variables.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá cómo los procesos BPMN gestionan información mediante variables.

El proceso será capaz de:

```text id="n3v4g1"
almacenar datos del proceso
modificar variables durante la ejecución
utilizar variables en decisiones del flujo
mostrar datos en tareas humanas
```

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se introducirán **gateways y eventos**, que permiten crear flujos de proceso más complejos y reactivos.
