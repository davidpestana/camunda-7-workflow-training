# Lab 14 — Testing y monitorización

## 🎯 Objetivo

Aprender a **probar, depurar y monitorizar procesos BPMN** ejecutados en el motor Camunda.

En este laboratorio se aprenderá a:

* crear tests automatizados para procesos BPMN
* depurar la ejecución de un proceso desde el código
* monitorizar la actividad del motor
* analizar el historial de ejecución de procesos

---

# 🧠 Contexto

En sistemas de workflow en producción es importante poder:

```text id="b2n4z6"
probar procesos antes de desplegarlos
analizar errores en ejecución
monitorizar el sistema
auditar ejecuciones pasadas
```

Camunda proporciona distintas herramientas para realizar estas tareas.

---

# 🧪 Testing de procesos

Los procesos BPMN pueden probarse mediante **tests automatizados**.

Estos tests permiten:

```text id="p5x7c1"
iniciar procesos
verificar variables
comprobar el flujo de ejecución
validar reglas de negocio
```

El motor Camunda puede ejecutarse dentro de los tests para simular el comportamiento real del sistema.

---

# 🐞 Debug de procesos

Cuando un proceso no se comporta como se espera, es posible depurarlo utilizando:

```text id="q8d3v9"
logs del sistema
breakpoints en el código
herramientas del motor
```

Esto permite observar variables, estados y decisiones del flujo.

---

# 📊 Monitorización del motor

Camunda incluye herramientas para observar el estado del sistema en ejecución.

Entre ellas:

```text id="f4g2k8"
Cockpit
logs del sistema
métricas del motor
```

Estas herramientas permiten detectar problemas y analizar el comportamiento del workflow.

---

# 📜 Historial de procesos

El motor almacena información histórica sobre la ejecución de los procesos.

Este historial permite analizar:

```text id="r9m5t7"
actividades ejecutadas
variables utilizadas
duración de tareas
estado final del proceso
```

Esto es útil para auditoría y análisis del sistema.

---

# 🔎 Qué vamos a hacer en este laboratorio

Durante este laboratorio se aprenderá a observar y analizar procesos en ejecución.

Se realizarán ejercicios para:

```text id="n7y4p3"
crear tests para procesos
depurar tareas automáticas
monitorizar el motor
analizar ejecuciones históricas
```

---

# 📘 Ejercicios del laboratorio

### 01 — Testing de procesos

Crear tests automatizados que verifiquen la ejecución de un proceso BPMN.

Archivo:

```text id="t6x1k4"
01-testing-procesos.md
```

---

### 02 — Debug de instancias

Depurar la ejecución de un proceso utilizando el debugger del IDE.

Archivo:

```text id="m2f8v6"
02-debug-instancias.md
```

---

### 03 — Monitorización del motor

Utilizar Cockpit para observar el estado del motor y los procesos.

Archivo:

```text id="g3y7r9"
03-monitorizacion-motor.md
```

---

### 04 — Historial de procesos

Analizar ejecuciones pasadas utilizando el historial del motor.

Archivo:

```text id="p1w6c8"
04-historial-procesos.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá cómo:

```text id="k5z2x7"
probar procesos BPMN
analizar errores
monitorizar ejecuciones
auditar procesos ejecutados
```

Esto permite mantener y operar sistemas de workflow en entornos reales.
