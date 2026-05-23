# Cómo hablarle a la IA: Contexto, Tarea y Formato

## Metadatos

| Campo            | Detalle                                      |
|------------------|----------------------------------------------|
| **Duración**     | 60 minutos                                   |
| **Complejidad**  | Fácil                                        |
| **Nivel Bloom**  | Crear                                        |
| **Modalidad**    | Individual / Guiada por instructor           |
| **Versión**      | 1.0                                          |

---

## Descripción General

Esta práctica establece los fundamentos del curso al enseñar cómo comunicarse de manera efectiva con una IA generativa usando el modelo **CTF: Contexto, Tarea y Formato**. El participante explorará la interfaz de Microsoft Copilot, comparará resultados de prompts vagos versus prompts estructurados, y construirá prompts originales aplicando la metodología CTF en escenarios laborales reales. Al finalizar, el participante contará con una plantilla reutilizable y criterio propio para iterar y mejorar sus instrucciones a la IA.

---

## Objetivos de Aprendizaje

Al completar esta práctica, el participante será capaz de:

- [ ] Identificar los tres componentes del modelo CTF (Contexto, Tarea, Formato) y explicar la función de cada uno.
- [ ] Comparar la calidad de respuestas generadas por prompts vagos versus prompts estructurados en Copilot.
- [ ] Construir al menos cinco prompts originales aplicando la metodología CTF para diferentes situaciones laborales.
- [ ] Evaluar una respuesta de IA usando criterios de aceptación definidos en el prompt.
- [ ] Refinar iterativamente un prompt para mejorar la precisión y utilidad de la respuesta generada.

---

## Requisitos Previos

### Conocimientos

| Conocimiento requerido                                    | Nivel mínimo     |
|-----------------------------------------------------------|------------------|
| Navegación web básica (abrir pestañas, copiar, pegar)     | Básico           |
| Redacción de mensajes en español                          | Básico           |
| Noción general de qué es una IA conversacional            | Introductorio    |

### Acceso y Cuentas

| Recurso                              | Requisito                                                                 |
|--------------------------------------|---------------------------------------------------------------------------|
| Cuenta Microsoft                     | Personal o corporativa activa (para iniciar sesión en Copilot)            |
| Acceso a Internet                    | Conexión estable, mínimo 10 Mbps de descarga                              |
| Microsoft Copilot                    | Acceso verificado en [copilot.microsoft.com](https://copilot.microsoft.com) |
| Alternativa (si Copilot no está disponible) | ChatGPT en [chat.openai.com](https://chat.openai.com)             |

> ⚠️ **Nota de seguridad:** Durante toda la práctica, utilice **únicamente datos ficticios o anonimizados**. No ingrese nombres de clientes reales, contratos vigentes, información financiera ni datos confidenciales de su organización en Copilot.

---

## Entorno de Laboratorio

### Hardware Recomendado

| Componente       | Mínimo requerido                          | Recomendado                        |
|------------------|-------------------------------------------|------------------------------------|
| Procesador       | 4 núcleos (Intel Core i5 / AMD Ryzen 5)   | Intel Core i7 / AMD Ryzen 7        |
| Memoria RAM      | 8 GB                                      | 16 GB                              |
| Almacenamiento   | 2 GB disponibles                          | 5 GB disponibles                   |
| Monitor          | 1280×768 píxeles                          | 1920×1080 píxeles                  |
| Entrada          | Teclado y ratón funcionales               | —                                  |

### Software Requerido

| Software                        | Versión mínima                    | Propósito en la práctica                  |
|---------------------------------|-----------------------------------|-------------------------------------------|
| Microsoft Edge o Google Chrome  | Versión 120 o superior            | Acceder a Copilot                         |
| Microsoft Copilot (web)         | Versión web actual                | Herramienta principal de IA               |
| Bloc de Notas / Notepad         | Cualquier versión del SO          | Preparar y guardar prompts                |
| Microsoft Word (opcional)       | Microsoft 365 / Word 2019         | Guardar resultados finales                |

### Configuración Inicial del Entorno

Realice los siguientes pasos **antes de comenzar los ejercicios**:

**Paso A — Verificar acceso a Copilot:**
```
1. Abra Microsoft Edge o Google Chrome.
2. Navegue a: https://copilot.microsoft.com
3. Inicie sesión con su cuenta Microsoft.
4. Confirme que la interfaz de chat está disponible y responde.
```

**Paso B — Configurar idioma en Copilot:**
```
1. En la interfaz de Copilot, busque el ícono de configuración (⚙️) o el menú de idioma.
2. Seleccione "Español" como idioma preferido si la opción está disponible.
3. Alternativa: escriba su primer mensaje en español; Copilot responderá en el mismo idioma.
```

**Paso C — Preparar el archivo de trabajo:**
```
1. Abra el Bloc de Notas (Notepad).
2. Cree un nuevo archivo.
3. Guárdelo como: Lab01_MisPrompts.txt
   (Ruta sugerida: Escritorio o carpeta Documentos/Lab01)
4. Este archivo será su "cuaderno de trabajo" durante toda la práctica.
```

**Paso D — Verificar alternativa (solo si Copilot no está disponible):**
```
1. Navegue a: https://chat.openai.com
2. Inicie sesión o cree una cuenta gratuita.
3. Confirme que el chat responde en español.
   Nota: Todos los ejercicios de esta práctica funcionan igualmente en ChatGPT.
```

---

## Procedimiento Paso a Paso

---

### Paso 1: Exploración de la Interfaz de Microsoft Copilot

**Objetivo:** Familiarizarse con la interfaz de Copilot antes de comenzar los ejercicios de prompting, identificando los elementos clave que se usarán durante la práctica.

**Tiempo estimado:** 8 minutos

#### Instrucciones

1. Asegúrese de estar en [copilot.microsoft.com](https://copilot.microsoft.com) con sesión iniciada.

2. Observe los elementos principales de la interfaz y localice cada uno:
   - **Campo de texto (chat box):** donde escribirá sus prompts.
   - **Botón de envío:** ícono de flecha o tecla `Enter` para enviar el mensaje.
   - **Historial de conversación:** área superior donde aparecen las respuestas.
   - **Botón "Nueva conversación" / "New topic":** para reiniciar el chat y empezar fresco.
   - **Selector de estilo de respuesta** (si está disponible): opciones como "Más creativo", "Más equilibrado", "Más preciso".

3. Envíe el siguiente mensaje de prueba en el campo de texto para confirmar que Copilot responde en español:

   ```
   Hola. Responde siempre en español. ¿Puedes confirmar que me entiendes?
   ```

4. Espere la respuesta y léala completa.

5. En su archivo `Lab01_MisPrompts.txt`, escriba la siguiente anotación:

   ```
   === PASO 1: EXPLORACIÓN DE INTERFAZ ===
   Fecha: [escriba la fecha de hoy]
   Copilot respondió en español: SÍ / NO (marque el que corresponda)
   Observaciones personales: [escriba qué notó sobre la interfaz]
   ```

6. Haga clic en **"Nueva conversación"** (o equivalente) para limpiar el historial antes del siguiente ejercicio.

#### Resultado Esperado

Copilot responde en español confirmando que entiende el mensaje. El participante identifica visualmente los componentes principales de la interfaz.

#### Verificación

- [ ] Copilot respondió en español.
- [ ] Se anotó la observación en `Lab01_MisPrompts.txt`.
- [ ] El historial fue reiniciado con "Nueva conversación".

---

### Paso 2: Comparación — Prompt Vago vs. Prompt Estructurado

**Objetivo:** Observar directamente cómo la calidad y utilidad de la respuesta de Copilot cambia según el nivel de estructura del prompt. Este es el ejercicio comparativo central de la práctica.

**Tiempo estimado:** 12 minutos

#### Instrucciones

**Parte A — Enviar el prompt vago:**

1. En una nueva conversación de Copilot, escriba y envíe exactamente el siguiente mensaje:

   ```
   Ayúdame con un correo.
   ```

2. Espere la respuesta completa de Copilot.

3. En su archivo `Lab01_MisPrompts.txt`, copie y pegue la respuesta recibida bajo la sección:

   ```
   === PASO 2A: PROMPT VAGO ===
   Prompt enviado: "Ayúdame con un correo."
   Respuesta de Copilot:
   [pegue aquí la respuesta]

   Mis observaciones:
   - ¿La respuesta fue útil para una situación real? SÍ / NO
   - ¿Copilot tuvo que hacer suposiciones? SÍ / NO
   - ¿Qué le faltó a esta respuesta?
   ```

4. Haga clic en **"Nueva conversación"** para reiniciar.

**Parte B — Enviar el prompt estructurado (CTF):**

5. En la nueva conversación, escriba y envíe el siguiente prompt completo. Puede copiarlo desde aquí y pegarlo en Copilot:

   ```
   Contexto: Soy coordinador de logística en una empresa de distribución de alimentos.
   Necesito comunicarme con un proveedor que entregó un pedido incompleto la semana pasada.
   El correo será leído por el gerente de ventas del proveedor.

   Tarea: Redacta un correo profesional solicitando una explicación formal sobre el pedido
   incompleto (Pedido #4521, faltaron 30 unidades de producto) y pidiendo una fecha
   de entrega del faltante no mayor a 48 horas.

   Formato: Correo formal en español, tono firme pero respetuoso, máximo 150 palabras,
   con asunto, saludo, cuerpo en 2 párrafos y despedida. Usa datos ficticios para
   el nombre del proveedor y la empresa.
   ```

6. Espere la respuesta completa de Copilot.

7. En su archivo `Lab01_MisPrompts.txt`, copie y pegue la respuesta bajo la sección:

   ```
   === PASO 2B: PROMPT ESTRUCTURADO (CTF) ===
   Respuesta de Copilot:
   [pegue aquí la respuesta]

   Mis observaciones:
   - ¿La respuesta fue útil para una situación real? SÍ / NO
   - ¿Copilot tuvo que hacer suposiciones? SÍ / NO
   - ¿Qué mejoró respecto al prompt vago?
   ```

**Parte C — Análisis comparativo:**

8. Revise ambas respuestas y complete la siguiente tabla en su archivo de notas:

   ```
   === PASO 2C: TABLA COMPARATIVA ===

   | Criterio                          | Prompt Vago | Prompt CTF |
   |-----------------------------------|-------------|------------|
   | ¿Tiene asunto de correo?          |             |            |
   | ¿Menciona el problema específico? |             |            |
   | ¿El tono es apropiado?            |             |            |
   | ¿Se puede usar directamente?      |             |            |
   | ¿Cumple con un límite de palabras?|             |            |
   ```

#### Resultado Esperado

- El prompt vago genera una respuesta genérica o solicita más información al usuario.
- El prompt CTF genera un correo completo, con asunto, tono apropiado, datos específicos y listo para usar o adaptar con mínimas ediciones.
- El participante documenta las diferencias observadas en su archivo de notas.

#### Verificación

- [ ] Se enviaron ambos prompts en conversaciones separadas.
- [ ] Ambas respuestas fueron copiadas al archivo de notas.
- [ ] La tabla comparativa fue completada con observaciones propias.
- [ ] Se inició una nueva conversación antes del siguiente paso.

---

### Paso 3: Aprendizaje de la Plantilla CTF

**Objetivo:** Internalizar la plantilla reutilizable CTF y practicar su uso con un escenario guiado paso a paso, antes de crear prompts propios.

**Tiempo estimado:** 10 minutos

#### Instrucciones

1. En su archivo `Lab01_MisPrompts.txt`, copie y guarde la siguiente plantilla oficial del curso. La usará como referencia en todos los ejercicios siguientes:

   ```
   === PLANTILLA CTF (GUARDAR ESTA SECCIÓN) ===

   Contexto: [Quién eres, para quién es la salida, propósito, restricciones]
   Tarea: [Verbo principal y alcance] + [Datos/fuentes a considerar]
   Formato: [Estructura/longitud/tono/idioma] + [Criterios de aceptación]

   Datos (opcional):
   """
   [Pega aquí texto, datos, fragmentos relevantes]
   """
   ```

2. Lea atentamente las siguientes notas sobre cada componente:

   ```
   NOTAS SOBRE CADA COMPONENTE:

   CONTEXTO — Responde: ¿Quién soy? ¿Para quién es esto? ¿En qué situación?
   Ejemplo débil:  "Trabajo en una empresa."
   Ejemplo fuerte: "Soy supervisora de RRHH en una empresa de manufactura
                    con 200 empleados. Este mensaje será leído por el equipo
                    directivo en la reunión mensual."

   TAREA — Usa UN verbo principal claro. Evita combinar múltiples tareas.
   Ejemplo débil:  "analiza y resume y sugiere mejoras"
   Ejemplo fuerte: "Resume los tres puntos críticos priorizando impacto económico"

   FORMATO — Define la "forma" del entregable como si fuera un contrato.
   Ejemplo débil:  "en formato bonito"
   Ejemplo fuerte: "Lista de 5 viñetas, máximo 100 palabras, tono ejecutivo,
                    en español, sin tecnicismos. Incluye una recomendación final."
   ```

3. Ahora practique la plantilla con el siguiente escenario guiado. **Construya el prompt** llenando cada sección antes de enviarlo a Copilot:

   **Escenario:** Usted es asistente administrativo en una clínica veterinaria ficticia llamada "Clínica VetNova". Necesita redactar un mensaje para recordar a los clientes sobre sus citas de vacunación programadas para la próxima semana.

4. Complete la plantilla con este escenario en su archivo de notas:

   ```
   === PASO 3: PROMPT GUIADO ===

   Contexto: Soy asistente administrativo en Clínica VetNova, una clínica
   veterinaria de tamaño mediano. El mensaje será enviado por WhatsApp
   a dueños de mascotas que tienen citas de vacunación la próxima semana.

   Tarea: Redacta un mensaje de recordatorio de cita de vacunación para
   enviar por WhatsApp a los clientes.

   Formato: Mensaje corto (máximo 80 palabras), tono amigable y profesional,
   en español, sin tecnicismos médicos. Debe incluir: nombre ficticio de la
   mascota, fecha y hora de la cita (inventadas), nombre de la clínica,
   y un número de teléfono ficticio para confirmar o reagendar.
   ```

5. Copie el prompt completo y envíelo a Copilot en una nueva conversación.

6. Lea la respuesta y evalúe si cumple los criterios del Formato que definió.

7. En su archivo de notas, registre:

   ```
   Respuesta de Copilot:
   [pegue aquí]

   Criterios de aceptación cumplidos:
   - ¿Menos de 80 palabras? SÍ / NO
   - ¿Tono amigable y profesional? SÍ / NO
   - ¿Incluye nombre de mascota ficticio? SÍ / NO
   - ¿Incluye fecha y hora? SÍ / NO
   - ¿Incluye nombre de clínica y teléfono? SÍ / NO
   ```

#### Resultado Esperado

Copilot genera un mensaje de WhatsApp corto, amigable, con todos los elementos solicitados en el Formato. El participante puede verificar el cumplimiento de cada criterio de aceptación definido en el prompt.

#### Verificación

- [ ] La plantilla CTF fue guardada en el archivo de notas.
- [ ] El prompt guiado fue construido completando las tres secciones.
- [ ] La respuesta fue evaluada contra los criterios de aceptación definidos.
- [ ] Se documentaron los resultados en el archivo de notas.

---

### Paso 4: Iteración y Refinamiento de Prompts

**Objetivo:** Practicar la mejora iterativa de un prompt cuando la primera respuesta no cumple completamente los criterios esperados, desarrollando el criterio para identificar qué ajustar.

**Tiempo estimado:** 10 minutos

#### Instrucciones

1. Continúe en la **misma conversación** del Paso 3 (no inicie una nueva). La iteración funciona mejor dentro de la misma sesión porque Copilot recuerda el contexto previo.

2. Revise la respuesta del Paso 3. Identifique al menos **una cosa que mejoraría**. Ejemplos comunes:
   - El mensaje es demasiado largo.
   - El tono es muy formal para WhatsApp.
   - Falta un emoji para hacerlo más cercano.
   - El número de teléfono no parece realista.

3. Envíe uno de los siguientes mensajes de refinamiento (elija el que aplique a su caso, o cree el suyo):

   **Opción A — Si el mensaje es muy largo:**
   ```
   El mensaje es demasiado largo. Por favor, acórtalo a máximo 60 palabras
   manteniendo toda la información esencial. No pierdas la fecha, la hora
   ni el número de contacto.
   ```

   **Opción B — Si el tono es muy formal:**
   ```
   El tono suena muy formal para un mensaje de WhatsApp. Reescríbelo con
   un tono más cálido y cercano, como si lo enviara una persona real,
   no una empresa. Puedes agregar 1 o 2 emojis relevantes.
   ```

   **Opción C — Refinamiento libre:**
   ```
   [Escriba aquí su propio ajuste basado en lo que observó en la respuesta anterior]
   ```

4. Envíe el mensaje de refinamiento y lea la nueva respuesta.

5. Compare la versión original (Paso 3) con la versión refinada. En su archivo de notas, registre:

   ```
   === PASO 4: ITERACIÓN Y REFINAMIENTO ===

   Mensaje de refinamiento enviado:
   [pegue aquí el mensaje que envió]

   Respuesta refinada de Copilot:
   [pegue aquí la nueva respuesta]

   ¿Mejoró la respuesta con el refinamiento? SÍ / NO
   ¿Qué cambió específicamente?
   [describa en 2-3 líneas]

   Lección aprendida sobre iteración:
   [escriba qué aprendió de este ejercicio]
   ```

6. Practique **una segunda iteración**: esta vez, pida a Copilot que genere **tres versiones alternativas** del mismo mensaje para elegir la mejor:

   ```
   Genera 3 versiones alternativas del mensaje de recordatorio, cada una con
   un tono ligeramente diferente: versión 1 muy formal, versión 2 amigable,
   versión 3 breve y directa. Etiquétalas claramente.
   ```

7. Lea las tres versiones y en su archivo de notas indique cuál preferiría usar y por qué.

#### Resultado Esperado

El participante observa que Copilot puede refinar su respuesta dentro de la misma conversación cuando recibe instrucciones específicas de mejora. Las tres versiones alternativas demuestran que el mismo prompt puede producir variaciones útiles según el tono solicitado.

#### Verificación

- [ ] Se envió al menos un mensaje de refinamiento en la misma conversación.
- [ ] Se compararon la respuesta original y la refinada.
- [ ] Se solicitaron tres versiones alternativas.
- [ ] Se documentó la lección aprendida sobre iteración en el archivo de notas.

---

### Paso 5: Construcción de Prompts Propios — Cinco Escenarios Laborales

**Objetivo:** Aplicar de forma autónoma la metodología CTF para construir cinco prompts originales en escenarios laborales variados, demostrando dominio del modelo.

**Tiempo estimado:** 20 minutos (aproximadamente 4 minutos por prompt)

#### Instrucciones

Para cada uno de los cinco escenarios siguientes, el participante debe:
1. Construir el prompt completo usando la plantilla CTF.
2. Enviarlo a Copilot en una **nueva conversación**.
3. Evaluar brevemente la respuesta.
4. Guardar todo en `Lab01_MisPrompts.txt`.

> 💡 **Consejo:** No copie los prompts de ejemplo anteriores. Cree sus propias versiones adaptadas a cada escenario. El objetivo es que usted construya los prompts, no que los copie.

---

**Escenario 5.1 — Resumen ejecutivo de una reunión**

Situación: Usted acaba de salir de una reunión de equipo de 45 minutos donde se discutieron tres temas: retrasos en entregas de un proveedor, propuesta de nuevo horario de turnos, y actualización del inventario de materiales. Necesita enviar un resumen por correo a su jefe, que no asistió.

```
Construya su prompt CTF aquí:

Contexto: [complete]
Tarea: [complete]
Formato: [complete]
```

Envíe su prompt a Copilot y evalúe:
```
=== ESCENARIO 5.1: RESUMEN DE REUNIÓN ===
Mi prompt:
[pegue su prompt]

Respuesta de Copilot:
[pegue la respuesta]

¿Cumple los criterios que definí? SÍ / NO / PARCIALMENTE
¿Qué cambiaría en el prompt si lo repitiera?
```

---

**Escenario 5.2 — Lista de verificación para un proceso**

Situación: Usted es encargado de apertura de una tienda minorista ficticia ("Tienda El Pino"). Necesita una lista de verificación de las tareas que deben realizarse cada mañana antes de abrir al público, incluyendo aspectos de limpieza, caja, inventario visible y seguridad básica.

```
Construya su prompt CTF aquí:

Contexto: [complete]
Tarea: [complete]
Formato: [complete]
```

Envíe su prompt a Copilot y evalúe:
```
=== ESCENARIO 5.2: LISTA DE VERIFICACIÓN ===
Mi prompt:
[pegue su prompt]

Respuesta de Copilot:
[pegue la respuesta]

¿Cumple los criterios que definí? SÍ / NO / PARCIALMENTE
¿Qué cambiaría en el prompt si lo repitiera?
```

---

**Escenario 5.3 — Recomendación para una decisión cotidiana**

Situación: Usted coordina un equipo de 8 personas y debe decidir si implementar reuniones diarias de 15 minutos ("stand-up") o mantener solo la reunión semanal de 1 hora. Quiere que la IA le presente los pros y contras de cada opción para ayudarle a decidir.

```
Construya su prompt CTF aquí:

Contexto: [complete]
Tarea: [complete]
Formato: [complete — piense en cómo quiere ver los pros y contras: tabla, lista, párrafos]
```

Envíe su prompt a Copilot y evalúe:
```
=== ESCENARIO 5.3: RECOMENDACIÓN DE DECISIÓN ===
Mi prompt:
[pegue su prompt]

Respuesta de Copilot:
[pegue la respuesta]

¿Cumple los criterios que definí? SÍ / NO / PARCIALMENTE
¿Qué cambiaría en el prompt si lo repitiera?
```

---

**Escenario 5.4 — Comunicación interna para el equipo**

Situación: La empresa donde trabaja implementará un nuevo sistema de registro de asistencia digital a partir del próximo lunes. Usted debe comunicar este cambio a su equipo de manera clara, indicando qué cambia, cómo usar el nuevo sistema (de forma general) y a quién contactar si hay dudas.

```
Construya su prompt CTF aquí:

Contexto: [complete — invente el nombre de la empresa y del sistema]
Tarea: [complete]
Formato: [complete — decida si prefiere correo, aviso en cartelera, mensaje de chat, etc.]
```

Envíe su prompt a Copilot y evalúe:
```
=== ESCENARIO 5.4: COMUNICACIÓN INTERNA ===
Mi prompt:
[pegue su prompt]

Respuesta de Copilot:
[pegue la respuesta]

¿Cumple los criterios que definí? SÍ / NO / PARCIALMENTE
¿Qué cambiaría en el prompt si lo repitiera?
```

---

**Escenario 5.5 — Prompt libre de su trabajo real (con datos ficticios)**

Situación: Piense en una tarea real y recurrente de su trabajo actual que le tome tiempo o que podría mejorar con ayuda de la IA. Cree un prompt CTF para esa tarea, reemplazando cualquier dato real por datos ficticios o genéricos.

> ⚠️ **Recordatorio:** No ingrese datos reales de su empresa. Use nombres ficticios, montos aproximados o genéricos, y omita información confidencial.

```
Construya su prompt CTF aquí:

Descripción de la tarea real (para sus notas personales, no para Copilot):
[describa brevemente la tarea]

Contexto: [complete con datos ficticios]
Tarea: [complete]
Formato: [complete]
```

Envíe su prompt a Copilot y evalúe:
```
=== ESCENARIO 5.5: PROMPT LIBRE ===
Mi prompt:
[pegue su prompt]

Respuesta de Copilot:
[pegue la respuesta]

¿Cumple los criterios que definí? SÍ / NO / PARCIALMENTE
¿Podría usar esta respuesta (adaptada) en mi trabajo real? SÍ / NO
¿Qué cambiaría?
```

#### Resultado Esperado

El participante genera cinco prompts CTF originales y obtiene respuestas de Copilot para cada uno. Cada respuesta es evaluada contra los criterios de aceptación definidos en el propio prompt. El participante experimenta que la calidad de la respuesta es directamente proporcional a la claridad del prompt.

#### Verificación

- [ ] Se construyeron cinco prompts CTF completos (Contexto + Tarea + Formato en cada uno).
- [ ] Cada prompt fue enviado a Copilot en una nueva conversación.
- [ ] Se documentaron las respuestas y evaluaciones en el archivo de notas.
- [ ] El Escenario 5.5 usa exclusivamente datos ficticios o genéricos.
- [ ] Se identificó al menos una mejora posible en al menos tres de los prompts.

---

## Validación y Pruebas

Al finalizar todos los pasos, realice la siguiente verificación integral de su trabajo:

### Lista de Verificación Final

Revise su archivo `Lab01_MisPrompts.txt` y confirme que contiene:

| # | Elemento a verificar                                                                 | ¿Completado? |
|---|--------------------------------------------------------------------------------------|--------------|
| 1 | Anotación del Paso 1 con observaciones de la interfaz de Copilot                    | ☐            |
| 2 | Prompt vago del Paso 2A con respuesta copiada y observaciones                       | ☐            |
| 3 | Prompt CTF del Paso 2B con respuesta copiada y observaciones                        | ☐            |
| 4 | Tabla comparativa del Paso 2C completada                                             | ☐            |
| 5 | Plantilla CTF guardada (sección "GUARDAR ESTA SECCIÓN")                              | ☐            |
| 6 | Prompt guiado del Paso 3 con evaluación de criterios de aceptación                  | ☐            |
| 7 | Registro de iteración del Paso 4 con lección aprendida                              | ☐            |
| 8 | Cinco prompts originales del Paso 5 (uno por escenario) con respuestas y evaluación | ☐            |
| 9 | Al menos un prompt libre (Escenario 5.5) con datos ficticios                        | ☐            |

### Prueba de Calidad de Prompts

Seleccione **el mejor prompt** que creó durante la práctica (el que produjo la respuesta más útil) y responda las siguientes preguntas en su archivo de notas:

```
=== VALIDACIÓN FINAL: MI MEJOR PROMPT ===

El prompt que selecciono como mi mejor trabajo:
[pegue el prompt completo]

¿Por qué lo considero el mejor?
[explique en 3-5 líneas]

¿Qué elemento CTF fue más difícil de definir para mí: Contexto, Tarea o Formato?
[responda y explique brevemente]

¿Cómo podría mejorar aún más este prompt?
[proponga al menos una mejora concreta]
```

---

## Resolución de Problemas

### Problema 1: Copilot responde en inglés aunque el prompt está en español

**Síntoma:** El participante escribe su prompt en español pero Copilot responde en inglés o en una mezcla de idiomas.

**Causa:** Copilot puede detectar el idioma del sistema operativo o del navegador y priorizar ese idioma, especialmente si la cuenta Microsoft está configurada en inglés. También puede ocurrir cuando el prompt mezcla términos técnicos en inglés.

**Solución:**
```
Opción 1 — Instrucción explícita en el prompt:
Agregue al final de la sección Formato la instrucción:
"Responde ÚNICAMENTE en español. No uses inglés en ninguna parte de tu respuesta."

Opción 2 — Mensaje de corrección en la misma conversación:
Envíe: "Por favor, traduce tu respuesta anterior al español y responde
siempre en español de ahora en adelante en esta conversación."

Opción 3 — Configuración del navegador:
En Microsoft Edge: Configuración > Idiomas > Agregar español como idioma preferido.
Reinicie el navegador y vuelva a acceder a Copilot.
```

---

### Problema 2: Copilot genera respuestas muy diferentes al mismo prompt en dos intentos distintos

**Síntoma:** El participante envía el mismo prompt en dos conversaciones separadas y obtiene respuestas notablemente diferentes en estructura, longitud o contenido, lo que genera confusión sobre si el prompt está bien construido.

**Causa:** Este comportamiento es **normal y esperado** en los modelos de lenguaje. Los modelos de IA generativa incluyen un parámetro de aleatoriedad (llamado "temperatura") que produce variación natural en las respuestas. No indica que el prompt esté mal construido.

**Solución:**
```
1. Comprenda que la variabilidad es una característica, no un error.
   El objetivo no es obtener una respuesta idéntica, sino una respuesta
   de alta calidad que cumpla los criterios del prompt.

2. Para reducir la variabilidad, agregue criterios de aceptación más
   específicos en la sección Formato. Ejemplo:
   En lugar de: "respuesta estructurada"
   Use: "exactamente 5 viñetas, cada una de máximo 20 palabras,
         comenzando con un verbo en infinitivo"

3. Si dos respuestas son igualmente válidas, use ambas como punto de
   partida y combine los mejores elementos de cada una.

4. Si una respuesta es claramente inferior, use la iteración (Paso 4)
   para mejorarla en la misma conversación en lugar de reiniciar.
```

---

## Limpieza del Entorno

Al finalizar la práctica, realice los siguientes pasos de cierre:

1. **Guardar el archivo de trabajo:**
   ```
   1. En el Bloc de Notas, presione Ctrl+S para guardar Lab01_MisPrompts.txt.
   2. Verifique que el archivo está guardado en su ubicación (Escritorio o Documentos/Lab01).
   3. Confirme que el archivo tiene contenido de todos los pasos (1 al 5).
   ```

2. **Exportar respuestas favoritas a Word (opcional pero recomendado):**
   ```
   1. Abra Microsoft Word.
   2. Cree un nuevo documento en blanco.
   3. Copie y pegue los 2 o 3 mejores prompts y sus respuestas desde el archivo de notas.
   4. Guarde como: Lab01_MejoresPrompts.docx
   5. Este archivo le servirá como referencia personal para las prácticas siguientes.
   ```

3. **Cerrar conversaciones de Copilot:**
   ```
   1. En Copilot, haga clic en "Nueva conversación" para limpiar el historial activo.
   2. No es necesario eliminar el historial de conversaciones anteriores,
      pero puede hacerlo desde la configuración si lo prefiere por privacidad.
   ```

4. **Nota sobre datos ingresados:**
   ```
   Recuerde: Todos los datos ingresados en Copilot durante esta práctica
   eran ficticios. Si por error ingresó algún dato real de su organización,
   notifique a su instructor y evite repetirlo en prácticas futuras.
   ```

---

## Resumen

### Lo que aprendió en esta práctica

En esta práctica introductoria usted:

1. **Exploró** la interfaz de Microsoft Copilot e identificó sus componentes principales.
2. **Comparó** directamente la diferencia entre un prompt vago y un prompt estructurado, observando el impacto en la calidad de la respuesta.
3. **Aprendió y aplicó** el modelo CTF (Contexto, Tarea, Formato) como marco para construir instrucciones efectivas a la IA.
4. **Practicó la iteración**, enviando mensajes de refinamiento para mejorar respuestas que no cumplían completamente los criterios esperados.
5. **Construyó cinco prompts originales** para escenarios laborales variados, aplicando de forma autónoma la metodología CTF.

### Conceptos Clave para Recordar

| Concepto                  | Definición práctica                                                                 |
|---------------------------|--------------------------------------------------------------------------------------|
| **Contexto**              | Define quién eres, para quién es la salida y cuál es la situación o restricción.   |
| **Tarea**                 | Describe la acción específica con un verbo claro y único (resumir, redactar, etc.). |
| **Formato**               | Especifica estructura, longitud, tono, idioma y criterios de aceptación.            |
| **Criterios de aceptación** | Condiciones que la respuesta DEBE cumplir para ser considerada válida.            |
| **Iteración**             | Proceso de mejorar un prompt o una respuesta mediante instrucciones de refinamiento.|
| **Variabilidad normal**   | Las respuestas de IA varían entre intentos; esto es esperado y manejable.           |

### Conexión con las Próximas Prácticas

El modelo CTF que aprendió hoy es el **fundamento de todo el curso**. En las prácticas siguientes, aplicará este mismo modelo para generar documentos más complejos:
- **Práctica 2:** Reportes, actas, cronogramas y correos contractuales.
- **Práctica 3:** Automatización de tareas administrativas recurrentes.
- **Práctica 4:** Documentación profesional estandarizada con criterios de validación.

### Recursos de Consulta Adicionales

| Recurso                                          | URL                                                                                  |
|--------------------------------------------------|--------------------------------------------------------------------------------------|
| Guía oficial de Prompt Engineering (OpenAI)      | https://platform.openai.com/docs/guides/prompt-engineering                           |
| Microsoft Learn — Ingeniería de prompts          | https://learn.microsoft.com/es-es/azure/ai-services/openai/concepts/prompt-engineering |
| PromptingGuide.ai — Técnicas y patrones          | https://www.promptingguide.ai/                                                       |
| Nielsen Norman Group — Prompting para todos      | https://www.nngroup.com/articles/prompt-engineering/                                 |
| Centro de ayuda de Microsoft Copilot             | https://support.microsoft.com/es-es/copilot                                          |

---

> 📝 **Nota final para el instructor:** Al concluir esta práctica, dedique 5 minutos a una puesta en común grupal donde 2-3 participantes compartan su "mejor prompt" del Escenario 5.5. Esto refuerza el aprendizaje colaborativo y permite mostrar la diversidad de aplicaciones del modelo CTF en diferentes contextos laborales reales.

---
*Lab 01-00-01 | Versión 1.0 | Curso: Fundamentos de IA Generativa con Microsoft Copilot*
