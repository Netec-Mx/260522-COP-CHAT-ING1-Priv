# Creación de casos de negocios, actas, cronogramas preliminares, interesados, lecciones aprendidas y redacción de correos contractuales.

## Metadatos

| Atributo | Detalle |
|---|---|
| **Duración estimada** | 90 minutos |
| **Complejidad** | Media |
| **Nivel Bloom** | Crear |
| **Modalidad** | Práctica guiada individual con revisión en plenaria |
| **Versión del documento** | 1.0 |

---

## Descripción General

En esta práctica aplicarás la metodología **Contexto–Tarea–Formato (CTF)** y la técnica de **prompting en cadena** para generar, en Microsoft Copilot, seis artefactos profesionales de gestión de proyectos: caso de negocio, acta de reunión, cronograma preliminar, matriz de interesados, lecciones aprendidas y correos contractuales. Todos los documentos girarán alrededor de un **escenario ficticio pero realista**: la implementación de un sistema de control de inventarios en la empresa mediana "Distribuidora Andina S.A.". Al finalizar, habrás construido un portafolio documental completo y desarrollado criterio crítico para evaluar y mejorar las respuestas de la IA antes de su uso profesional.

> ⚠️ **Recordatorio de seguridad de datos:** Durante toda la práctica utiliza únicamente los datos ficticios del escenario. **No ingreses** información real de tu organización, clientes, contratos vigentes ni datos financieros reales en Copilot.

---

## Objetivos de Aprendizaje

Al completar este laboratorio serás capaz de:

- [ ] Generar un caso de negocio estructurado con secciones de justificación, beneficios, riesgos y presupuesto usando prompts CTF en Copilot.
- [ ] Crear un acta de reunión profesional con todos sus campos obligatorios (asistentes, acuerdos, responsables y fechas) mediante prompts dirigidos.
- [ ] Elaborar un cronograma preliminar en formato de tabla (fases, hitos, responsables, fechas y estado) usando instrucciones iterativas.
- [ ] Documentar una matriz de interesados con categorización por poder–interés y estrategia de involucramiento.
- [ ] Redactar un documento de lecciones aprendidas y tres correos contractuales profesionales aplicando la metodología CTF.

---

## Prerrequisitos

### Conocimientos previos
- Haber completado **Lab 01-00-01** (Práctica 1) o conocer la metodología Contexto–Tarea–Formato.
- Comprensión básica de qué es un proyecto y sus fases principales (inicio, planificación, ejecución, cierre).
- Familiaridad con la navegación web y el uso de Microsoft Word o Word Online.

### Acceso y cuentas requeridas
- Cuenta Microsoft activa con acceso a **copilot.microsoft.com** (verificar antes de iniciar la sesión).
- Acceso a **Microsoft Word** (Microsoft 365 versión 2308+, Word 2019, o Word Online).

---

## Entorno del Laboratorio

### Configuración inicial del entorno

Antes de comenzar los ejercicios, completa los siguientes pasos de configuración:

**Paso A — Verificar acceso a Copilot:**
1. Abre Microsoft Edge o Chrome.
2. Navega a `https://copilot.microsoft.com`.
3. Inicia sesión con tu cuenta Microsoft.
4. Verifica que la interfaz de chat esté disponible y en idioma español. Si aparece en inglés, escribe en el chat: `Por favor, responde siempre en español neutro a partir de ahora.`

**Paso B — Preparar archivos de trabajo:**
1. Crea una carpeta en tu escritorio llamada `Lab_02_Documentos_Proyecto`.
2. Abre el **Bloc de Notas** y guarda un archivo vacío como `prompts_lab02.txt` dentro de esa carpeta. Aquí copiarás todos los prompts antes de ejecutarlos.
3. Abre **Microsoft Word** (o Word Online) y crea un documento en blanco llamado `Portafolio_Distribuidora_Andina.docx` en la misma carpeta.


> **Escenario ficticio — Distribuidora Andina S.A.**
>
> Distribuidora Andina S.A. es una empresa mediana de distribución de productos de consumo masivo con sede en Bogotá, Colombia. Actualmente gestiona su inventario mediante hojas de cálculo Excel y procesos manuales, lo que genera errores de stock, pérdidas por vencimiento y retrasos en despachos. La gerencia ha aprobado explorar la implementación de un **Sistema de Control de Inventarios (SCI)** basado en software ERP. El proyecto tiene un horizonte de 6 meses, un presupuesto estimado de USD 85.000 y afectará a los departamentos de Logística, Finanzas y Ventas. El patrocinador es la Gerente General, Dra. Laura Mendoza.

---

## Instrucciones Paso a Paso

> 📌 **Nota sobre variabilidad de respuestas:** Copilot puede generar respuestas diferentes cada vez que se ejecuta el mismo prompt. Esto es normal. El objetivo es obtener una respuesta de **alta calidad** que cumpla los criterios del prompt, no una respuesta idéntica a la del instructor.

---

### BLOQUE 1: Caso de Negocio 

#### Paso 1 — Construir y ejecutar el prompt para el caso de negocio

**Objetivo:** Generar un caso de negocio estructurado de una página para el proyecto SCI de Distribuidora Andina S.A.

**Instrucciones:**

1. Abre el Bloc de Notas (`prompts_lab02.txt`) y escribe el siguiente prompt. Revísalo completo antes de copiarlo a Copilot:

```text
Contexto: Actúa como un PMO (Project Management Officer) senior con experiencia en proyectos 
de implementación de sistemas ERP en empresas medianas de distribución en Latinoamérica. 
La empresa es Distribuidora Andina S.A., con sede en Bogotá. Actualmente gestiona su 
inventario con hojas de cálculo Excel, lo que genera errores de stock, pérdidas por 
vencimiento y retrasos en despachos. El presupuesto estimado es USD 85.000 y el horizonte 
del proyecto es 6 meses.

Tarea: Crea un caso de negocio ejecutivo de una página para justificar la implementación 
de un Sistema de Control de Inventarios (SCI) basado en ERP. El documento debe incluir 
las siguientes secciones en este orden:
1. Problema/Oportunidad
2. Alternativas evaluadas (3 opciones: continuar igual, ERP en la nube, desarrollo a medida)
3. Análisis costo-beneficio resumido
4. Beneficios esperados con KPIs medibles
5. Riesgos principales y mitigación inicial
6. Recomendación y criterios de éxito

Formato: Documento estructurado con títulos de sección en negrita, viñetas para listas, 
tono ejecutivo formal, máximo 600 palabras, en español neutro latinoamericano. 
Usa datos ficticios pero realistas y coherentes con el escenario descrito.
```

2. Copia el prompt completo y pégalo en el chat de Copilot. Presiona **Enter** o haz clic en el botón de envío.
3. Espera la respuesta completa (puede tardar entre 15 y 30 segundos).
4. Lee la respuesta completa antes de continuar.

**Salida esperada:** Un documento de aproximadamente 400–600 palabras con seis secciones claramente diferenciadas, viñetas, KPIs numéricos (por ejemplo: "reducir errores de stock en 40%") y una recomendación clara hacia la opción ERP en la nube.

---

#### Paso 2 — Refinar el caso de negocio con prompt de seguimiento

**Objetivo:** Practicar el refinamiento iterativo para mejorar una sección específica del documento generado.

**Instrucciones:**

1. Identifica en la respuesta anterior la sección de **"Análisis costo-beneficio"**. Si consideras que es demasiado genérica, envía el siguiente prompt de seguimiento en la **misma conversación** (sin abrir un chat nuevo):

```text
Mejora únicamente la sección "Análisis costo-beneficio" del caso de negocio anterior. 
Agrega una tabla comparativa con tres columnas: Concepto, Costo estimado (USD) y 
Beneficio esperado (USD/año). Incluye al menos 4 filas con datos ficticios pero 
coherentes con el proyecto de USD 85.000 a 6 meses. Mantén el resto del documento sin cambios.
```

2. Revisa la tabla generada. Verifica que los números sean internamente consistentes (por ejemplo, que el total de costos no supere el presupuesto de USD 85.000).
3. Si los números son inconsistentes, anota las correcciones necesarias a mano o en el Bloc de Notas. **No dependas de la IA para validar cifras financieras.**

**Salida esperada:** Una tabla de 4+ filas con valores numéricos ficticios pero coherentes, integrada en el contexto del caso de negocio.

---

#### Paso 3 — Guardar el caso de negocio en Word

**Instrucciones:**

1. Selecciona todo el texto del caso de negocio generado por Copilot (incluyendo la tabla refinada).
2. Copia el texto (Ctrl+C).
3. Abre el documento `Portafolio_Distribuidora_Andina.docx`.
4. Escribe el título: **`SECCIÓN 1: CASO DE NEGOCIO`** en negrita, tamaño 16.
5. Pega el contenido debajo del título (Ctrl+V).
6. Agrega al final del caso de negocio la siguiente nota en cursiva:
7. Guarda el documento (Ctrl+S).

---

### BLOQUE 2: Acta de Reunión

#### Paso 4 — Generar el acta de reunión de kick-off

**Objetivo:** Crear un acta de reunión profesional para la reunión de inicio del proyecto SCI.

**Instrucciones:**

1. En el Bloc de Notas, escribe y revisa el siguiente prompt:

```text
Contexto: Eres el asistente de documentación de proyectos de Distribuidora Andina S.A. 
Se acaba de realizar la reunión de kick-off del proyecto "Implementación del Sistema de 
Control de Inventarios (SCI-2026)" el día 15 de enero de 2026, de 9:00 a 11:00 horas, 
en la Sala de Juntas Principal. 

Los asistentes fueron:
- Dra. Laura Mendoza – Gerente General (Patrocinadora)
- Ing. Carlos Ríos – Gerente de Logística
- Lic. Patricia Vargas – Gerente de Finanzas
- Ing. Andrés Suárez – Líder de TI
- Lic. Mónica Torres – Gerente de Ventas
- Ing. Diego Herrera – Gerente de Proyecto (PM)

Los temas tratados y acuerdos fueron:
- Se aprobó el inicio formal del proyecto con presupuesto de USD 85.000
- Se definió que el PM es Diego Herrera con dedicación del 80%
- TI debe entregar el análisis de infraestructura actual antes del 30 de enero
- Finanzas debe confirmar la disponibilidad presupuestaria antes del 22 de enero
- Se acordó reunión de seguimiento semanal los martes a las 10:00 horas
- Se identificó como riesgo la resistencia al cambio en el área de Logística
- Próxima reunión: 22 de enero de 2026

Tarea: Redacta un acta de reunión formal y completa que incluya: encabezado con datos 
generales, lista de asistentes con roles, resumen de temas tratados, tabla de acuerdos 
(con columnas: N°, Acuerdo, Responsable, Fecha compromiso, Estado), riesgos identificados 
y próximos pasos.

Formato: Documento formal con encabezado institucional ficticio para Distribuidora Andina 
S.A., secciones claramente delimitadas con títulos en negrita, la tabla de acuerdos en 
formato de tabla, pie de página con líneas de firma para PM y Patrocinadora, 
en español neutro latinoamericano.
```

2. Copia el prompt y pégalo en Copilot. Presiona **Enter**.
3. Lee la respuesta completa.

**Salida esperada:** Un acta de reunión de 2–3 páginas equivalentes con encabezado, lista de asistentes, tabla de acuerdos con al menos 5 filas, sección de riesgos y próximos pasos, y líneas de firma al final.

---

#### Paso 5 — Guardar el acta en Word

**Instrucciones:**

1. Copia el acta generada por Copilot.
2. En el documento `Portafolio_Distribuidora_Andina.docx`, agrega un salto de página (Ctrl+Enter) y escribe el título: **`SECCIÓN 2: ACTA DE REUNIÓN DE KICK-OFF`**.
3. Pega el contenido del acta.
4. Agrega la nota de validación pendiente (igual que en el Paso 3, actualizando la sección).
5. Guarda el documento.

---

### BLOQUE 3: Cronograma Preliminar 

#### Paso 6 — Generar el cronograma preliminar en formato de tabla

**Objetivo:** Elaborar un cronograma preliminar con fases, hitos, responsables, fechas y estado del proyecto SCI.

**Instrucciones:**

1. **Importante:** Abre una **nueva conversación** en Copilot (busca el botón "Nueva conversación" o "New chat") para evitar que el contexto de los prompts anteriores interfiera. Luego escribe el siguiente prompt:

```text
Contexto: Eres el Gerente de Proyecto del proyecto "Implementación del Sistema de Control 
de Inventarios (SCI-2026)" en Distribuidora Andina S.A. El proyecto inicia el 15 de enero 
de 2026 y debe concluir antes del 15 de julio de 2026 (6 meses). El equipo incluye: 
PM (Diego Herrera), Líder de TI (Andrés Suárez), Analista de Negocio (a contratar), 
Proveedor ERP (empresa externa), y representantes de Logística, Finanzas y Ventas.

Tarea: Crea un cronograma preliminar de proyecto que incluya las siguientes 5 fases con 
sus hitos principales:
Fase 1: Inicio y diagnóstico (2 semanas)
Fase 2: Selección y contratación del proveedor ERP (3 semanas)
Fase 3: Configuración e implementación (8 semanas)
Fase 4: Pruebas piloto y capacitación (4 semanas)
Fase 5: Go-live y cierre (2 semanas)

Para cada fase incluye al menos 3 actividades o hitos específicos con fechas estimadas 
de inicio y fin calculadas desde el 15 de enero de 2026.

Formato: Una tabla con las siguientes columnas exactas:
| N° | Fase | Actividad/Hito | Responsable | Fecha Inicio | Fecha Fin | Duración | Estado |
Usa fechas en formato DD/MM/AAAA. El campo Estado debe decir "Pendiente" para todas las 
actividades. Agrega una fila de HITO CLAVE al final de cada fase. 
Responde en español neutro latinoamericano.
```

2. Pega el prompt en Copilot y presiona **Enter**.
3. Revisa que las fechas sean cronológicamente consistentes (que la Fecha Fin sea siempre posterior a la Fecha Inicio y que las fases se sucedan lógicamente).
4. Si detectas inconsistencias de fechas, anótalas en el Bloc de Notas para corregirlas manualmente en Word.

**Salida esperada:** Una tabla de aproximadamente 20–25 filas con 8 columnas, fechas calculadas desde el 15/01/2026, hitos clave al final de cada fase y estado "Pendiente" en todas las filas.

---

#### Paso 7 — Agregar supuestos y restricciones al cronograma

**Objetivo:** Practicar el prompting en cadena añadiendo información complementaria al cronograma.

**Instrucciones:**

1. En la **misma conversación** del Paso 6, envía el siguiente prompt de seguimiento:

```text
Basándote en el cronograma anterior, agrega debajo de la tabla una sección titulada 
"Supuestos y Restricciones del Cronograma" con dos subsecciones:

Supuestos (mínimo 4 puntos):
- Relacionados con disponibilidad del equipo, decisiones del proveedor y aprobaciones internas.

Restricciones (mínimo 3 puntos):
- Relacionadas con el presupuesto de USD 85.000, la fecha límite del 15 de julio de 2026 
  y la disponibilidad de infraestructura de TI.

Formato: Lista de viñetas para cada subsección, tono profesional, máximo 150 palabras en total.
```

2. Copia tanto la tabla del cronograma como la nueva sección de supuestos y restricciones.

**Salida esperada:** La sección de supuestos con 4+ puntos y la sección de restricciones con 3+ puntos, redactadas en tono profesional.

---

#### Paso 8 — Guardar el cronograma en Word

**Instrucciones:**

1. Copia el cronograma completo (tabla + supuestos y restricciones).
2. En el documento Word, agrega un salto de página y el título: **`SECCIÓN 3: CRONOGRAMA PRELIMINAR`**.
3. Pega el contenido. Si la tabla no se formatea correctamente al pegar, usa **Pegado especial → Solo texto** y recrea la tabla manualmente, o usa la opción "Mantener formato de origen".
4. Agrega la nota de validación pendiente.
5. Guarda el documento.

---

### BLOQUE 4: Matriz de Interesados

#### Paso 9 — Generar la matriz de interesados

**Objetivo:** Identificar y documentar los interesados del proyecto SCI con categorización por poder–interés.

**Instrucciones:**

1. Abre una **nueva conversación** en Copilot. Escribe el siguiente prompt:

```text
Contexto: Eres un analista de proyectos especialista en gestión de interesados (stakeholder 
management) según el estándar PMBOK. Trabajas en el proyecto "Implementación del Sistema 
de Control de Inventarios (SCI-2026)" en Distribuidora Andina S.A. El proyecto afecta 
a los departamentos de Logística, Finanzas, Ventas y TI. Existen también interesados 
externos: el proveedor ERP seleccionado, los clientes de la distribuidora y el ente 
regulador tributario (DIAN ficticia).

Tarea: Crea una matriz de interesados completa para este proyecto. Incluye al menos 
10 interesados diferentes (internos y externos). Para cada interesado incluye todos 
los campos de la tabla.

Formato: Una tabla con las siguientes columnas exactas:
| N° | Nombre/Rol | Tipo (Interno/Externo) | Nivel de Poder (Alto/Medio/Bajo) | Nivel de Interés (Alto/Medio/Bajo) | Cuadrante P-I | Expectativas principales | Estrategia de involucramiento | Canal de comunicación | Frecuencia |

Después de la tabla, agrega una leyenda que explique los 4 cuadrantes del modelo 
Poder-Interés (Gestionar de cerca, Mantener satisfecho, Mantener informado, Monitorear). 
Responde en español neutro latinoamericano.
```

2. Pega el prompt en Copilot y presiona **Enter**.
3. Revisa que la clasificación de cuadrantes sea coherente con los niveles de poder e interés asignados (por ejemplo, Alto Poder + Alto Interés = "Gestionar de cerca").

**Salida esperada:** Una tabla de 10+ filas con 9 columnas, interesados internos y externos identificados, cuadrantes correctamente asignados, y leyenda de los 4 cuadrantes al final.

**Verificación:**
- [ ] La tabla tiene al menos 10 interesados.
- [ ] Hay interesados internos Y externos.
- [ ] Los cuadrantes son coherentes con los niveles de Poder e Interés asignados.
- [ ] La leyenda de los 4 cuadrantes está presente.
- [ ] La columna "Estrategia de involucramiento" tiene contenido específico para cada interesado.

---

#### Paso 10 — Guardar la matriz de interesados en Word

**Instrucciones:**

1. Copia la matriz completa (tabla + leyenda).
2. En el documento Word, agrega un salto de página y el título: **`SECCIÓN 4: MATRIZ DE INTERESADOS`**.
3. Pega el contenido.
4. Agrega la nota de validación pendiente.
5. Guarda el documento.

---

### BLOQUE 5: Lecciones Aprendidas

#### Paso 11 — Generar el documento de lecciones aprendidas

**Objetivo:** Redactar un documento de lecciones aprendidas a partir de la descripción de un proyecto similar concluido.

**Instrucciones:**

1. Abre una **nueva conversación** en Copilot. Escribe el siguiente prompt:

```text
Contexto: Eres el Gerente de Proyecto de Distribuidora Andina S.A. El proyecto 
"Implementación del Sistema de Control de Inventarios (SCI-2026)" acaba de concluir. 
Durante el proyecto ocurrieron los siguientes eventos relevantes:
- Los requerimientos cambiaron 6 veces en los primeros 2 meses por falta de definición inicial
- El proveedor ERP entregó con 3 semanas de retraso el módulo de reportes
- La capacitación al equipo de Logística fue muy exitosa y redujo la resistencia al cambio
- El presupuesto se excedió en USD 9.200 (10.8%) principalmente por horas adicionales de consultoría
- La comunicación semanal con el patrocinador fue clave para resolver bloqueos rápidamente
- No se documentaron los cambios de requerimientos formalmente hasta la semana 8

Tarea: Genera un documento formal de lecciones aprendidas con 6 lecciones (3 positivas 
y 3 de mejora). Para cada lección incluye todos los campos de la estructura.

Formato: Para cada lección usa la siguiente estructura en formato de tarjeta o sección:
**Lección N°X – [Título descriptivo]**
- Tipo: Positiva / De mejora
- Contexto: [descripción breve de la situación]
- Qué ocurrió: [descripción del evento]
- Análisis (causa raíz): [causa principal]
- Impacto: [efecto en tiempo, costo, calidad o alcance]
- Recomendación: [acción sugerida para futuros proyectos]
- Acción preventiva/correctiva: [medida concreta]
- Propietario: [rol responsable]
- Fecha de registro: 16 de julio de 2026

Al final agrega una tabla resumen con las 6 lecciones, su tipo y la recomendación principal.
Responde en español neutro latinoamericano.
```

2. Pega el prompt y presiona **Enter**.
3. Verifica que haya exactamente 3 lecciones positivas y 3 de mejora.

**Salida esperada:** Seis secciones de lecciones aprendidas con todos los campos completados, seguidas de una tabla resumen de 6 filas.

---

#### Paso 12 — Guardar las lecciones aprendidas en Word

**Instrucciones:**

1. Copia el documento de lecciones aprendidas completo.
2. En el documento Word, agrega un salto de página y el título: **`SECCIÓN 5: LECCIONES APRENDIDAS`**.
3. Pega el contenido.
4. Agrega la nota de validación pendiente.
5. Guarda el documento.

---

### BLOQUE 6: Correos Contractuales 

#### Paso 13 — Correo 1: Solicitud de cotización

**Objetivo:** Redactar un correo contractual formal de solicitud de cotización al proveedor ERP.

**Instrucciones:**

1. Abre una **nueva conversación** en Copilot. Escribe el siguiente prompt:

```text
Contexto: Eres Diego Herrera, Gerente de Proyecto de Distribuidora Andina S.A. Necesitas 
solicitar una cotización formal al proveedor de software ERP "TechSoluciones Latam S.A.S." 
para la implementación de su módulo de control de inventarios. El proyecto tiene un 
presupuesto máximo de USD 85.000 y debe implementarse en 6 meses a partir del 
1 de febrero de 2026.

Tarea: Redacta un correo electrónico formal de solicitud de cotización (RFQ - Request 
for Quotation) que incluya:
1. Descripción breve de la empresa y la necesidad
2. Alcance específico requerido (módulos de inventario, integración con facturación, 
   capacitación a 25 usuarios, soporte post-implementación por 3 meses)
3. Información que debe incluir la cotización (desglose por componente, cronograma 
   propuesto, garantías, condiciones de pago)
4. Fecha límite para recibir la cotización: 25 de enero de 2026
5. Datos de contacto del PM

Formato: Correo electrónico formal con campos Para/CC/Asunto/Cuerpo/Firma claramente 
delimitados. Tono profesional y preciso. Máximo 300 palabras en el cuerpo del correo. 
Español neutro latinoamericano.
```

2. Pega el prompt en Copilot y presiona **Enter**.
3. Verifica que el correo incluya todos los elementos solicitados y que el tono sea apropiado para una comunicación contractual.

**Salida esperada:** Un correo con campos Para, CC, Asunto, cuerpo de 200–300 palabras y firma profesional. El asunto debe ser descriptivo e incluir referencia al proyecto.

---

#### Paso 14 — Correo 2: Confirmación de acuerdo

**Objetivo:** Redactar un correo de confirmación de acuerdo contractual con el proveedor seleccionado.

**Instrucciones:**

1. En la **misma conversación** del Paso 13, envía el siguiente prompt:

```text
Ahora redacta un segundo correo diferente. 

Contexto adicional: TechSoluciones Latam S.A.S. fue seleccionado como proveedor. 
Se firmó el Contrato ERP-2026-007 el 5 de febrero de 2026 por un valor de USD 78.500. 
El proveedor ha confirmado verbalmente que puede iniciar el 10 de febrero, pero aún 
no ha enviado confirmación escrita del cronograma de implementación.

Tarea: Redacta un correo de confirmación de acuerdo y solicitud de documentación 
pendiente que incluya:
1. Referencia explícita al Contrato ERP-2026-007 y su fecha de firma
2. Confirmación de los términos acordados (valor, fecha de inicio, alcance principal)
3. Lista de documentos que el proveedor debe entregar antes del 8 de febrero de 2026:
   - Cronograma detallado de implementación
   - Plan de gestión de riesgos del proveedor
   - Lista del equipo asignado con roles y experiencia
4. Consecuencia si no se reciben los documentos en el plazo indicado
5. Solicitud de acuse de recibo

Formato: Correo electrónico formal con todos los campos. Tono firme pero colaborativo. 
Máximo 250 palabras en el cuerpo. Referencia el número de contrato en el asunto. 
Español neutro latinoamericano.
```

2. Revisa que el correo referencie explícitamente el número de contrato y la fecha límite.

**Salida esperada:** Un correo con referencia al contrato ERP-2026-007, lista de documentos pendientes, fecha límite del 8 de febrero y consecuencia clara en caso de incumplimiento.

---

#### Paso 15 — Correo 3: Notificación de incumplimiento

**Objetivo:** Redactar el correo contractual más delicado: una notificación formal de incumplimiento.

**Instrucciones:**

1. En la **misma conversación**, envía el siguiente prompt:

```text
Redacta un tercer correo, diferente a los anteriores.

Contexto: Es 20 de marzo de 2026. TechSoluciones Latam S.A.S. debía entregar el 
módulo de reportes avanzados el 15 de marzo de 2026 según el Contrato ERP-2026-007, 
Cláusula 5.3, Entregable E-04. A la fecha no se ha recibido el entregable ni 
comunicación formal del proveedor explicando el retraso. El retraso impacta el 
cronograma del proyecto en al menos 3 semanas.

Tarea: Redacta una notificación formal de incumplimiento contractual que incluya:
1. Referencia específica al contrato, cláusula y entregable incumplido
2. Descripción objetiva del incumplimiento (qué se debía entregar, cuándo y qué ocurrió)
3. Impacto documentado en el proyecto (tiempo: +3 semanas; costo: horas adicionales 
   de equipo interno estimadas en USD 4.200)
4. Solicitud formal de Plan de Recuperación por escrito antes del 24 de marzo de 2026
5. Advertencia de que el incumplimiento persistente activará las penalidades del 
   Contrato ERP-2026-007, Cláusula 8.1
6. Copia a: Gerente General (Dra. Laura Mendoza), Departamento Jurídico, PMO

Formato: Correo electrónico formal con todos los campos. Tono firme, objetivo y 
documentado (sin lenguaje agresivo). Máximo 300 palabras en el cuerpo. 
Asunto debe incluir la palabra "NOTIFICACIÓN FORMAL". Español neutro latinoamericano.
```

2. Lee cuidadosamente el correo generado. Evalúa si el tono es apropiado: debe ser firme y objetivo, pero no agresivo ni amenazante de forma desproporcionada.
3. Si el tono no es el adecuado, usa el siguiente prompt de ajuste:

```text
El correo anterior tiene un tono demasiado [agresivo / pasivo]. 
Por favor, ajusta únicamente el tono para que sea más [firme y profesional / directo 
pero colaborativo], manteniendo todos los datos y referencias contractuales sin cambios.
```

**Salida esperada:** Un correo con asunto que incluye "NOTIFICACIÓN FORMAL", referencias a la Cláusula 5.3 y al Entregable E-04, impactos cuantificados, plazo para el Plan de Recuperación y advertencia sobre penalidades de la Cláusula 8.1.

---

#### Paso 16 — Guardar los correos contractuales en Word

**Instrucciones:**

1. Copia los tres correos contractuales (del chat de Copilot).
2. En el documento Word, agrega un salto de página y el título: **`SECCIÓN 6: CORREOS CONTRACTUALES`**.
3. Agrega subtítulos para cada correo:
   - `6.1 Solicitud de Cotización (RFQ)`
   - `6.2 Confirmación de Acuerdo`
   - `6.3 Notificación de Incumplimiento`
4. Pega cada correo bajo su subtítulo correspondiente.
5. Agrega la nota de validación pendiente al final de la sección.
6. Guarda el documento.

---

### BLOQUE 7: Revisión y Consolidación Final 

#### Paso 17 — Revisar y editar el portafolio completo

**Objetivo:** Aplicar criterio crítico para evaluar y mejorar los documentos generados antes de su uso profesional.

**Instrucciones:**

1. Abre el documento `Portafolio_Distribuidora_Andina.docx` y revisa las 6 secciones completas.
2. Para cada sección, verifica los siguientes criterios usando la lista de comprobación:

| Criterio de revisión | Sec. 1 | Sec. 2 | Sec. 3 | Sec. 4 | Sec. 5 | Sec. 6 |
|---|---|---|---|---|---|---|
| ¿El contenido es coherente con el escenario de Distribuidora Andina? | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ |
| ¿Las fechas son lógicamente consistentes? | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ |
| ¿Los nombres y roles son consistentes entre secciones? | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ |
| ¿El tono es apropiado para el tipo de documento? | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ |
| ¿Hay información genérica o "relleno" que deba eliminarse? | ☐ | ☐ | ☐ | ☐ | ☐ | ☐ |

3. Corrige manualmente en Word cualquier inconsistencia que encuentres. Los tipos de errores más comunes incluyen:
   - Nombres de personas que cambian entre secciones (por ejemplo, "Carlos Ríos" vs. "Carlos Río").
   - Fechas que no coinciden con el cronograma establecido.
   - Cifras financieras inconsistentes con el presupuesto de USD 85.000.
   - Frases genéricas como "según las mejores prácticas de la industria" sin contexto específico.

4. Agrega una **portada** al documento con la siguiente información:
   - Nombre del proyecto: Implementación del Sistema de Control de Inventarios (SCI-2026)
   - Empresa: Distribuidora Andina S.A. (FICTICIO – Solo para práctica)
   - Preparado por: [Tu nombre]
   - Fecha: [Fecha actual]
   - Versión: Borrador 1.0 – Generado con asistencia de IA

5. Guarda el documento final.

**Salida esperada:** Un documento Word de 15–25 páginas con portada, 6 secciones bien estructuradas, inconsistencias corregidas y notas de validación pendiente en cada sección.

---

## Limpieza del Entorno

Al finalizar el laboratorio, realiza los siguientes pasos de limpieza:

1. **Guardar trabajo final:**
   - Confirma que `Portafolio_Distribuidora_Andina.docx` está guardado en `Lab_02_Documentos_Proyecto`.
   - Confirma que `prompts_lab02.txt` contiene todos los prompts utilizados (para referencia futura).

2. **Cerrar conversaciones de Copilot:**
   - En Copilot, cierra o limpia el historial de conversaciones si tu organización tiene políticas de privacidad que lo requieran.
   - Cierra las pestañas del navegador con Copilot abierto.

3. **Archivar los archivos de práctica:**
   - Comprime la carpeta `Lab_02_Documentos_Proyecto` en un archivo ZIP: clic derecho → "Enviar a" → "Carpeta comprimida (zip)".
   - Nombra el ZIP: `Lab02_[TuNombre]_[FechaActual].zip`.
   - Guarda el ZIP en la ubicación indicada por el instructor (OneDrive, carpeta compartida, o correo electrónico).

4. **Verificar que no se guardó información sensible:**
   - Abre el documento Word y confirma que no contiene datos reales de tu organización.
   - Abre el archivo `prompts_lab02.txt` y verifica lo mismo.

5. **Cerrar aplicaciones:**
   - Cierra Microsoft Word.
   - Cierra el Bloc de Notas.
   - Cierra el navegador o las pestañas relevantes.

---

## Resumen

### Lo que aprendiste en este laboratorio

En esta práctica de 180 minutos construiste un **portafolio documental completo de gestión de proyectos** utilizando Microsoft Copilot como asistente de productividad. Los logros clave fueron:

| Artefacto generado | Técnica de prompting aplicada | Habilidad desarrollada |
|---|---|---|
| Caso de negocio | CTF + prompt de refinamiento | Justificación de inversión con KPIs |
| Acta de reunión | CTF con campos obligatorios definidos | Documentación formal de acuerdos |
| Cronograma preliminar | CTF + prompting en cadena | Planificación por fases e hitos |
| Matriz de interesados | CTF con estructura de tabla definida | Análisis poder–interés |
| Lecciones aprendidas | CTF con contexto narrativo | Mejora continua y trazabilidad |
| Correos contractuales (×3) | CTF + ajuste de tono iterativo | Comunicación contractual precisa |

### Principios clave reforzados

- **La IA acelera, el profesional valida:** Todos los documentos generados son borradores que requieren revisión humana antes de su uso oficial.
- **El prompt determina la calidad:** Un prompt con Contexto, Tarea y Formato claros produce resultados significativamente mejores que preguntas genéricas.
- **El prompting en cadena multiplica el valor:** Usar el resultado de un prompt como base para el siguiente permite construir documentos complejos de forma incremental.
- **La consistencia es responsabilidad tuya:** La IA puede ser inconsistente entre conversaciones; la revisión cruzada de datos (fechas, nombres, cifras) es una habilidad crítica.
- **Referencia contractual = trazabilidad:** En correos y documentos contractuales, siempre referenciar el número de contrato y la cláusula específica.

### Recursos adicionales recomendados

- [Guía PMBOK – Estándares PMI](https://www.pmi.org/pmbok-guide-standards/foundational/pmbok) — Referencia para los artefactos de gestión de proyectos.
- [PMI – Stakeholder Engagement](https://www.pmi.org/learning/library/stakeholder-analysis-techniques-11051) — Profundizar en análisis de interesados.
- [Microsoft Copilot – Centro de ayuda](https://support.microsoft.com/copilot) — Documentación oficial y consejos de uso.
- [NASA Lessons Learned](https://llis.nasa.gov) — Repositorio de referencia para lecciones aprendidas en proyectos complejos.
- **Práctica recomendada:** Toma uno de los documentos generados hoy y aplícalo a un proyecto real de tu organización (con datos anonimizados). Mide el tiempo que tardas en adaptarlo vs. el tiempo que tardarías en crearlo desde cero.

---

### Resultado Esperado

- Portafolio Documental Consolidado: El participante genera un expediente con 6 artefactos de gestión alineados al escenario de "Distribuidora Andina S.A.", asegurando la consistencia de nombres, roles, fechas y del presupuesto base de USD 85.000.

- Dominio del Prompting en Cadena e Iterativo: Capacidad para estructurar instrucciones complejas y refinar los resultados de Copilot dentro de una misma conversación .

- Desarrollo de Criterio Crítico: El estudiante aplica listas de comprobación (checklists) para identificar y corregir manualmente "alucinaciones" de la IA, variaciones de nombres o inconsistencias cronológicas antes de una firma ejecutiva.

- Trazabilidad y Gobierno: Incorporación obligatoria de notas de descargo (disclaimers) que especifican que el contenido fue asistido por IA y requiere validación humana experta.

---

> 🏁 **¡Laboratorio completado!** Has generado seis artefactos profesionales de gestión de proyectos en una sola sesión de trabajo. El portafolio que construiste hoy representa el tipo de documentación que normalmente tomaría varios días producir. Con práctica y refinamiento de tus prompts, este proceso seguirá mejorando en calidad y velocidad.
