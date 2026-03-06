# Eventos temporizador

## 🎯 Objetivo

Añadir un **evento temporizador** al proceso para simular un **tiempo de espera antes de ejecutar una actividad**.

---

## 🧠 Contexto

En BPMN los **Timer Events** permiten introducir esperas temporales dentro del proceso.

Se utilizan para:

* esperar cierto tiempo antes de continuar
* programar ejecuciones
* implementar reintentos o recordatorios

Ejemplos reales:

* esperar 24h antes de enviar un recordatorio
* esperar 5 minutos antes de reintentar una operación
* programar tareas periódicas

En este ejercicio añadiremos una **espera de 10 segundos** antes de ejecutar la validación.

---

# Abrir el modelo BPMN

Abrir el archivo:

```
model/approval-process.bpmn
```

Editar el modelo con **Camunda Modeler**.

---

# Insertar un Timer Event

Seleccionar el elemento:

```
Intermediate Event
```

Insertarlo **entre el evento Inicio y la tarea Validar solicitud**.

---

# Convertir el evento en Timer Event

Seleccionar el evento creado.

Cambiar su tipo a:

```
Intermediate Timer Event
```

---

# Configurar el temporizador

En el panel de propiedades buscar la sección:

```
Timer Definition
```

Seleccionar el tipo:

```
Duration
```

Introducir el valor:

```
PT10S
```

Esto significa:

```
P = periodo
T = tiempo
10S = 10 segundos
```

---

# Flujo del proceso

El flujo ahora debería ser:

```
Inicio
   │
   ▼
Esperar 10 segundos
   │
   ▼
Validar solicitud
   │
   ▼
Aprobar solicitud
   │
   ▼
Gateway decisión
```

---

# Guardar el modelo

Guardar el archivo:

```
model/approval-process.bpmn
```

---

# Copiar el modelo al backend

Actualizar el modelo desplegado:

```bash
cp model/approval-process.bpmn backend/src/main/resources/processes/
```

---

# Ejecutar la aplicación

Ir al backend:

```bash
cd backend
```

Arrancar la aplicación:

```bash
mvn spring-boot:run
```

---

# Observar el comportamiento

Cuando se inicie el proceso:

1. el proceso comenzará
2. llegará al **Timer Event**
3. el motor esperará **10 segundos**
4. después continuará con **Validar solicitud**

Durante esos 10 segundos el proceso permanecerá en estado de espera.

---

# Ver el estado en Cockpit

Abrir:

```
http://localhost:8081/camunda
```

Ir a **Cockpit**.

Abrir la instancia del proceso.

Durante el temporizador se podrá observar que la instancia está detenida en el **Timer Event**.

---

# Qué ocurre internamente

Cuando el proceso alcanza el temporizador:

```
Proceso llega al Timer Event
       │
       ▼
Camunda crea un Job
       │
       ▼
El Job Executor espera el tiempo definido
       │
       ▼
El proceso continúa
```

El temporizador se gestiona mediante el **Job Executor** del motor.

---

# Comprobación

El ejercicio se considera completado cuando:

* el modelo contiene un **Intermediate Timer Event**
* el temporizador está configurado con `PT10S`
* el proceso espera antes de ejecutar la Service Task.
