# Verificación de variables del proceso

## 🎯 Objetivo

Inspeccionar las **variables creadas durante la ejecución del proceso** y comprobar cómo se almacenan en el motor Camunda.

---

## 🧠 Contexto

Durante los ejercicios anteriores se han creado variables en distintos puntos del proceso:

Variables creadas desde **Java**:

```
solicitante
importe
tipoSolicitud
estadoSolicitud
```

Variable creada desde **el formulario de la tarea**:

```
aprobada
```

Todas estas variables forman parte de la **instancia del proceso**.

El motor Camunda almacena estas variables en la base de datos del proceso.

---

# Abrir Camunda Cockpit

Abrir el navegador y acceder a:

```
http://localhost:8081/camunda
```

Entrar en la aplicación **Cockpit**.

---

# Abrir el proceso

Ir a la sección:

```
Processes
```

Seleccionar el proceso:

```
approval-process
```

---

# Abrir una instancia del proceso

En la página del proceso localizar la sección:

```
Process Instances
```

Seleccionar una instancia del proceso.

---

# Ver las variables

Dentro de la instancia del proceso abrir la pestaña:

```
Variables
```

Deberían aparecer las variables generadas durante la ejecución.

Ejemplo:

```
solicitante = juan
importe = 5000
tipoSolicitud = compra
estadoSolicitud = VALIDADA
aprobada = true
```

---

# Ver el historial de variables

Ir a la pestaña:

```
History
```

Aquí se puede observar:

* cuándo se creó cada variable
* qué valor tenía en cada momento
* en qué actividad se modificó

Esto permite analizar la evolución de los datos dentro del proceso.

---

# Qué significa esto

Las variables permiten que el proceso transporte información entre sus distintas actividades.

El flujo de datos sería:

```
Aplicación Java
      │
      ▼
Variables iniciales
      │
      ▼
Service Task modifica variables
      │
      ▼
Formulario crea nuevas variables
      │
      ▼
Variables disponibles durante todo el proceso
```

---

# Comprobación

El ejercicio se considera completado cuando:

* se accede a **Cockpit**
* se abre una instancia del proceso
* se visualizan las variables creadas durante la ejecución.
