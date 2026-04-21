# Local Service Quote & Visit Assistant

## Asistente de Presupuestos, Visitas y Seguimiento para Servicios Locales

Proyecto de automatización orientado a negocios de servicios locales que reciben consultas por presupuesto, visita, plazo, zona, desplazamiento, seguimiento, soporte o urgencia y todavía gestionan gran parte de esa primera atención de forma manual.

La solución analiza cada consulta, detecta qué necesita el cliente, identifica qué falta para avanzar, propone una respuesta segura y decide si esa respuesta puede enviarse o requiere revisión humana.

---

## Problema de negocio

Muchos negocios locales reciben consultas como:

- “Quería presupuesto”
- “¿Podéis venir a verlo?”
- “¿Cuánto tardaríais?”
- “¿Trabajáis en mi zona?”
- “¿Cobráis desplazamiento?”
- “Os escribí y sigo esperando”
- “Tengo una incidencia urgente”

Estas consultas suelen llegar incompletas, mezcladas y por distintos canales. Esto genera:

- tiempo manual repetitivo
- peor filtrado comercial
- respuestas tardías
- seguimientos pobres
- y errores al responder temas sensibles como precio, plazo o disponibilidad

---

## Qué hace el sistema

El sistema:

- recibe una consulta
- detecta el tipo de servicio
- detecta la necesidad principal
- identifica datos faltantes
- decide si hacen falta fotos
- decide si hace falta visita
- genera una respuesta sugerida
- decide si esa respuesta se puede enviar
- y guarda el caso en una hoja operativa clara

---

## Qué NO hace esta V2

Esta versión no:

- da presupuestos cerrados automáticos
- promete plazos exactos
- confirma cobertura real sin validación
- calcula desplazamiento sin política definida
- agenda visitas automáticamente
- sustituye criterio técnico humano

Su valor está en ordenar, pedir mejor, responder antes y dejar clara la siguiente acción.

---

## Casos que cubre

### 1. Presupuesto
Ejemplo:
> “Quería presupuesto para instalar dos splits en casa.”

Salida:
- detecta climatización
- detecta presupuesto
- pide datos mínimos
- no inventa precio
- deja respuesta segura

### 2. Visita técnica
Ejemplo:
> “Quiero reformar un baño y me gustaría que vinierais a verlo.”

Salida:
- detecta visita técnica
- sube prioridad
- pide fotos si hace falta
- propone siguiente paso
- no cierra agenda

### 3. Plazo
Ejemplo:
> “Si os paso hoy la información, cuánto tardaríais en venir?”

Salida:
- detecta consulta de plazo
- pide tipo de trabajo
- responde con prudencia
- no promete fecha exacta

### 4. Cobertura o desplazamiento
Ejemplo:
> “¿Trabajáis por esta zona?” / “¿Cobráis desplazamiento?”

Salida:
- no inventa cobertura
- no inventa coste
- pide dato mínimo o deja revisión humana

### 5. Seguimiento
Ejemplo:
> “Os escribí la semana pasada y quería saber si hay novedades.”

Salida:
- deja respuesta simple
- marca seguimiento
- asigna fecha de revisión

### 6. Soporte o urgencia
Ejemplo:
> “No enfría bien.” / “Tengo una fuga de agua.”

Salida:
- distingue soporte de venta nueva
- sube prioridad si toca
- evita autoenvío si hay riesgo
- deja revisión humana

---

## Cómo funciona

### Modo evaluación
Permite probar el sistema con un dataset de casos simulados para validar:

- tipo de servicio
- necesidad principal
- datos faltantes
- visita / fotos
- seguridad de respuesta
- y coherencia general

### Modo real
Permite recibir consultas por webhook, procesarlas con el mismo motor y guardarlas en:

- una hoja técnica
- una hoja operativa para negocio

---

## Arquitectura lógica

1. entra una consulta
2. se normaliza
3. se analiza con IA
4. se parsea la salida
5. se aplican reglas de negocio
6. se decide si puede enviarse o no
7. se guarda en hojas técnica y operativa

---

## Salidas principales

El sistema devuelve, entre otros, estos campos:

- tipo_servicio
- tipo_necesidad
- prioridad
- score_oportunidad
- datos_faltantes
- requiere_visita
- requiere_fotos
- respuesta_lista_para_enviar
- auto_reply_allowed
- estado
- fecha_followup

---

## Hojas del sistema

### Hoja técnica
Pensada para validación, control y seguimiento interno de la automatización.

### Hoja operativa
Pensada para negocio. Resume de forma clara:

- qué tipo de caso es
- qué falta
- si se puede enviar
- qué respuesta propone
- y cuál es el siguiente paso

---

## Posicionamiento correcto

Este proyecto no debe venderse como chatbot.
Tampoco como generador automático de presupuestos.

Debe venderse como:

**asistente de primera atención comercial y operativa para presupuestos, visitas, seguimiento y consultas frecuentes.**

---

## Valor para negocio

- responde antes
- pide mejor los datos
- reduce ida y vuelta innecesaria
- mejora el filtrado comercial
- evita errores en temas sensibles
- organiza mejor la entrada
- y deja revisión humana donde realmente hace falta

---

## Estado actual del proyecto

V2 funcional con:

- modo evaluación
- modo real por webhook
- análisis con IA
- parser
- reglas de negocio
- hoja técnica
- hoja operativa

---

## Posibles ampliaciones futuras

- integración con WhatsApp
- envío automático de email
- conexión con calendario
- política real de zonas
- política real de desplazamiento
- tablas orientativas por servicio
- CRM
- dashboards de seguimiento

---

## Mensaje final

Este sistema no sustituye a la persona.

Le quita la parte repetitiva de la primera atención, organiza mejor la entrada y evita que el negocio tenga que empezar cada consulta desde cero.
