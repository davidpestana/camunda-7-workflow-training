# Lab 05 — Service Tasks y User Tasks

## 🎯 Objetivo

Implementar la lógica de negocio del proceso utilizando **Service Tasks** y gestionar **tareas humanas** mediante **User Tasks**.

En este laboratorio se aprenderá a:

* crear un `JavaDelegate` que implemente una Service Task
* conectar el modelo BPMN con código Java
* definir tareas humanas en el proceso
* asignar tareas a usuarios o grupos
* ejecutar el proceso completo

---

# 🧠 Contexto

En BPMN existen distintos tipos de tareas.

Las dos más importantes en aplicaciones reales son:

```text id="6m92mq"
Service Task
User Task
```

Una **Service Task** representa trabajo automatizado ejecutado por el sistema.

Ejemplos:

```text id="w3n6k3"
validar datos
llamar a una API
guardar información en base de datos
```

Una **User Task** representa trabajo realizado por una persona.

Ejemplos:

```text id="a0y5e4"
aprobar solicitud
revisar documento
validar información
```

El motor Camunda gestiona ambos tipos de tareas dentro del mismo proceso.

---

# 🔎 Qué vamos a hacer en este laboratorio

Se ampliará el proceso BPMN creado en el laboratorio anterior para incluir:

```text id="0x1o8k"
una Service Task implementada en Java
una User Task gestionada desde Tasklist
```

El flujo del proceso será similar a:

```text id="9cfz7y"
Inicio
  │
  ▼
Validar solicitud (Service Task)
  │
  ▼
Aprobar solicitud (User Task)
  │
  ▼
Fin
```

---

# 📘 Ejercicios del laboratorio

### 01 — Crear JavaDelegate

Crear una clase Java que implemente la lógica de una Service Task.

Archivo:

```text id="2g9n7o"
01-crear-java-delegate.md
```

---

### 02 — Configurar Service Task

Conectar la Service Task del modelo BPMN con el `JavaDelegate`.

Archivo:

```text id="p0o1w9"
02-configurar-service-task.md
```

---

### 03 — Crear User Task

Añadir una tarea humana al proceso BPMN.

Archivo:

```text id="u4y8l2"
03-crear-user-task.md
```

---

### 04 — Asignación de usuarios

Configurar cómo se asignan las tareas humanas a usuarios o grupos.

Archivo:

```text id="y1q3n5"
04-asignacion-usuarios.md
```

---

### 05 — Ejecución del proceso

Ejecutar el proceso completo y completar la tarea humana desde Tasklist.

Archivo:

```text id="b6z8e0"
05-ejecucion-proceso.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio el proceso incluirá:

```text id="n9v3x6"
automatización mediante Java
interacción humana mediante Tasklist
```

El motor Camunda ejecutará automáticamente la Service Task y esperará a que un usuario complete la User Task.

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se trabajará con **variables de proceso, formularios y expresiones**, que permiten gestionar los datos dentro del workflow.
