# Lab 04 — Modelado de procesos

## 🎯 Objetivo

Diseñar y desplegar un **proceso BPMN ejecutable** utilizando Camunda Modeler y conectarlo con la aplicación Spring Boot.

En este laboratorio se aprenderá a:

* crear modelos BPMN ejecutables
* utilizar eventos de inicio y fin
* definir tareas automáticas y tareas humanas
* desplegar un modelo en el motor Camunda

---

# 🧠 Contexto

El motor Camunda ejecuta **modelos BPMN**.

Estos modelos describen el flujo de un proceso utilizando elementos gráficos como:

```text
eventos
tareas
gateways
flujos de secuencia
```

Cuando un modelo BPMN se despliega en el motor:

```text
BPMN Model
      │
      ▼
Process Engine
      │
      ▼
instancias de proceso
```

Cada vez que se inicia un proceso, el motor crea una **instancia de ese modelo**.

---

# 🔎 Qué vamos a hacer en este laboratorio

En este laboratorio se diseñará un proceso de ejemplo que representa un **flujo de aprobación de solicitudes**.

El proceso incluirá:

```text
evento de inicio
tareas automáticas
tareas humanas
evento de finalización
```

Posteriormente el modelo se desplegará en el motor Camunda para ejecutarlo.

---

# 📘 Ejercicios del laboratorio

### 01 — Crear modelo con Camunda Modeler

Crear un nuevo modelo BPMN dentro del directorio `model`.

Archivo:

```text
01-crear-modelo-modeler.md
```

---

### 02 — Eventos de inicio y fin

Añadir eventos que definan el inicio y final del proceso.

Archivo:

```text
02-eventos-inicio-fin.md
```

---

### 03 — Service Task

Añadir una tarea automática que será ejecutada por código Java.

Archivo:

```text
03-service-task.md
```

---

### 04 — User Task

Añadir una tarea humana que será completada desde Tasklist.

Archivo:

```text
04-user-task.md
```

---

### 05 — Despliegue del proceso

Copiar el modelo al proyecto y desplegarlo en el motor Camunda.

Archivo:

```text
05-despliegue-proceso.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se habrá creado un proceso BPMN completo que incluye:

```text
evento de inicio
service task
user task
evento de fin
```

El proceso estará desplegado en el motor y listo para ejecutarse.

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se implementará la **lógica Java que ejecuta las tareas automáticas del proceso**.
