# Condiciones en los flujos

## 🎯 Objetivo

Configurar **condiciones en los flujos del Exclusive Gateway** para que el proceso elija automáticamente el camino correcto.

---

## 🧠 Contexto

En el ejercicio anterior se añadió un **Exclusive Gateway** con dos posibles caminos:

```id="c0w4nh"
Aprobada
Rechazada
```

Sin embargo, el gateway aún **no sabe qué camino elegir**.

Para tomar la decisión se utilizan **condiciones basadas en variables del proceso**.

En este caso utilizaremos la variable creada por el formulario:

```id="ux2s89"
aprobada
```

---

# Abrir el modelo BPMN

Abrir el archivo:

```id="kq3b0e"
model/approval-process.bpmn
```

Editar el modelo utilizando **Camunda Modeler**.

---

# Seleccionar el flujo "Aprobada"

Seleccionar el **sequence flow** que sale del gateway hacia el final **aprobado**.

En el panel de propiedades localizar:

```id="f3w1az"
Condition Expression
```

Configurar la expresión:

```id="v7y6nb"
${aprobada == true}
```

Esto indica que el flujo se seguirá cuando la variable `aprobada` sea verdadera.

---

# Seleccionar el flujo "Rechazada"

Seleccionar el segundo flujo que sale del gateway.

Configurar la condición:

```id="z6s2pt"
${aprobada == false}
```

---

# Marcar un flujo por defecto

Opcionalmente se puede marcar un flujo como **default flow**.

Seleccionar el flujo **Rechazada**.

Activar la opción:

```id="1o9u8q"
Default Flow
```

Esto se utilizará si ninguna condición se cumple.

---

# Guardar el modelo

Guardar el archivo:

```id="7xg0rf"
model/approval-process.bpmn
```

---

# Copiar el modelo al backend

Actualizar el modelo desplegado:

```bash id="0m0c9r"
cp model/approval-process.bpmn backend/src/main/resources/processes/
```

---

# Ejecutar la aplicación

Ir al backend:

```bash id="j2r7sh"
cd backend
```

Ejecutar la aplicación:

```bash id="8nq0ky"
mvn spring-boot:run
```

---

# Probar el flujo

Abrir Tasklist:

```
http://localhost:8081/camunda/app/tasklist
```

Completar la tarea **Aprobar solicitud**.

Probar dos casos:

### Caso 1

Formulario:

```
Solicitud aprobada = true
```

El proceso seguirá el flujo:

```
Aprobada → Fin
```

---

### Caso 2

Formulario:

```
Solicitud aprobada = false
```

El proceso seguirá el flujo:

```
Rechazada → Fin
```

---

# Flujo completo

El proceso ahora funciona así:

```id="1z2qv9"
Inicio
   │
   ▼
Validar solicitud
   │
   ▼
Aprobar solicitud
   │
   ▼
Exclusive Gateway
   ├── aprobada == true → Fin aprobado
   └── aprobada == false → Fin rechazado
```

---

# Comprobación

El ejercicio se considera completado cuando:

* el gateway tiene **condiciones en los flujos**
* las condiciones utilizan la variable `aprobada`
* el proceso sigue caminos diferentes según el formulario.
