# Lab 08 — Despliegue y versionado de procesos

## 🎯 Objetivo

Comprender cómo Camunda gestiona el **despliegue de procesos BPMN**, cómo se crean **nuevas versiones** de un proceso y cómo se gestionan **instancias existentes** cuando el modelo cambia.

En este laboratorio se aprenderá a:

* desplegar procesos BPMN en el motor
* entender el versionado automático de Camunda
* ejecutar múltiples versiones de un proceso
* migrar instancias de una versión a otra

---

# 🧠 Contexto

Cuando un modelo BPMN se despliega en Camunda, el motor crea una **definición de proceso**.

Cada vez que se despliega una nueva versión del mismo modelo:

```text id="u2m5z9"
Camunda crea una nueva versión del proceso
```

Por ejemplo:

```text id="n7k1y3"
approval-process v1
approval-process v2
approval-process v3
```

Las instancias existentes continúan ejecutándose en la versión con la que fueron iniciadas.

Esto permite **actualizar procesos sin interrumpir ejecuciones en curso**.

---

# 🔎 Qué vamos a hacer en este laboratorio

Se modificará el proceso BPMN existente para crear **nuevas versiones del modelo**.

Posteriormente se observará cómo el motor:

* mantiene versiones anteriores
* ejecuta nuevas instancias con la última versión
* permite migrar instancias entre versiones

---

# 📘 Ejercicios del laboratorio

### 01 — Despliegue de modelos

Desplegar un modelo BPMN en el motor Camunda.

Archivo:

```text id="g9r3c2"
01-despliegue-modelos.md
```

---

### 02 — Versionado de procesos

Modificar el modelo BPMN y desplegar una nueva versión.

Archivo:

```text id="b4s6f8"
02-versionado-procesos.md
```

---

### 03 — Múltiples versiones

Observar cómo Camunda gestiona varias versiones del mismo proceso.

Archivo:

```text id="q2y7t1"
03-multiples-versiones.md
```

---

### 04 — Migración de instancias

Migrar instancias de proceso de una versión a otra.

Archivo:

```text id="k8w0d5"
04-migracion-instancias.md
```

---

# 🧪 Resultado esperado

Al finalizar este laboratorio se comprenderá cómo Camunda gestiona:

```text id="v5p9x1"
versiones de procesos
instancias activas
actualizaciones del modelo
```

Esto permitirá evolucionar procesos BPMN sin interrumpir ejecuciones existentes.

---

# 🔜 Próximo laboratorio

En el siguiente laboratorio se aprenderá a **interactuar con el motor Camunda desde código Java y mediante API REST**.
