# Uso de Copilot para priorizar listas de pendientes, estructurar pasos para una tarea técnica y extraer puntos clave de manuales extensos.

## 1. Metadatos

| Campo            | Detalle                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Duración**     | 90 minutos                                                              |
| **Complejidad**  | Media                                                                   |
| **Nivel Bloom**  | Crear                                                                   |
| **Modalidad**    | Individual / Guiada por instructor                                      |
| **Versión**      | 1.0                                                                     |

---

## 2. Descripción General

Esta práctica transforma tres desafíos cotidianos de productividad —la sobrecarga de tareas, la ambigüedad en procedimientos técnicos y la densidad de manuales extensos— en resultados claros y accionables usando Microsoft Copilot. A través de tres bloques progresivos, el participante aplicará el patrón de prompting **CTF (Contexto, Tarea, Formato)** para priorizar pendientes con marcos estructurados (MoSCoW y Eisenhower), generar guías técnicas paso a paso con puntos de control, y extraer síntesis ejecutivas de documentos largos. Al finalizar, habrá construido una biblioteca personal de prompts reutilizables adaptados a su área de trabajo.

---

## 3. Objetivos de Aprendizaje

Al completar esta práctica, el participante será capaz de:

- [ ] Construir prompts CTF completos que produzcan listas de pendientes priorizadas con criterios explícitos (MoSCoW, Eisenhower, puntaje ponderado) y un plan de acción de 90 minutos.
- [ ] Generar una guía técnica estructurada con pre-requisitos, pasos secuenciales, puntos de control, riesgos, mitigaciones y criterios de aceptación para una tarea de su área.
- [ ] Extraer resúmenes ejecutivos, riesgos críticos, glosarios y checklists de inspección a partir de un texto extenso usando instrucciones de delimitación y restricción de longitud.
- [ ] Aplicar técnicas avanzadas de prompting: definición de rol, pesos ponderados, delimitadores de texto (`<<< >>>`), solicitud de supuestos no confirmados y restricciones de longitud.
- [ ] Evaluar críticamente las respuestas de Copilot identificando omisiones, supuestos implícitos y necesidades de validación humana.

---

## 4. Prerrequisitos

### Conocimiento Previo

| Requisito | Descripción |
|-----------|-------------|
| Lab 01-00-01 completado | El participante conoce la interfaz de Copilot y el patrón básico CTF |
| Concepto de priorización | Familiaridad básica con términos como urgencia, impacto y esfuerzo |
| Lectura previa | Haber revisado el material de la Lección 3.1 de este curso |

### Materiales que el Participante Debe Traer

| Material | Descripción | Alternativa si no se tiene |
|----------|-------------|---------------------------|
| Lista de pendientes | Mínimo 8 ítems reales o simulados de trabajo (anonimizados) | Usar la lista de ejemplo proporcionada en el **Paso 1** de este lab |
| Texto técnico extenso | Fragmento de manual, procedimiento o normativa (800–1200 palabras) de su empresa (anonimizado) | Usar el **Texto de Muestra del Instructor** incluido en el **Paso 3** de este lab |

> ⚠️ **IMPORTANTE — Datos sensibles:** No ingrese nombres reales de clientes, contratos vigentes ni información financiera confidencial en Copilot. Use siempre datos ficticios o anonimizados.

---

## 5. Entorno de Laboratorio

### Configuración Inicial del Entorno

Ejecute los siguientes pasos de preparación **antes de iniciar los bloques de práctica**. Tiempo estimado: 5 minutos.

**1. Verificar acceso a Copilot:**
```
1. Abrir Microsoft Edge o Chrome
2. Navegar a: https://copilot.microsoft.com
3. Iniciar sesión con cuenta Microsoft (corporativa o personal)
4. Confirmar que la interfaz de chat está disponible
```

**2. Configurar idioma en Copilot:**
```
1. En la interfaz de Copilot, verificar que las respuestas aparecen en español
2. Si aparece en otro idioma, escribir en el chat:
   "Por favor, responde siempre en español a partir de ahora."
3. Confirmar que Copilot responde en español
```

**3. Preparar archivo de trabajo en Bloc de Notas:**
```
1. Abrir Bloc de Notas (Notepad)
2. Guardar un archivo nuevo como: Lab03_Prompts_[TuNombre].txt
3. Este archivo servirá para preparar y editar prompts antes de pegarlos en Copilot
```

**4. Crear documento Word para resultados:**
```
1. Abrir Microsoft Word
2. Crear documento nuevo
3. Guardar como: Lab03_Resultados_[TuNombre].docx
4. Agregar tres secciones con los títulos:
   - Bloque 1: Priorización de Pendientes
   - Bloque 2: Guía Técnica Estructurada
   - Bloque 3: Extracción de Puntos Clave
```

> 💡 **Alternativa de respaldo:** Si Copilot no está disponible por restricciones corporativas, usar ChatGPT en https://chat.openai.com con los mismos prompts. Los resultados serán equivalentes para los propósitos de esta práctica.

---

### BLOQUE 1: Priorización de Pendientes 

---

#### Paso 1 — Preparar la Lista de Pendientes

**Objetivo:** Construir una lista de pendientes laborales anonimizada y bien redactada lista para ingresar a Copilot.

**Instrucciones:**

1. Abra su archivo `Lab03_Prompts_[TuNombre].txt` en Bloc de Notas.

2. Si trajo su propia lista de pendientes, escríbala en el archivo, asegurándose de:
   - Tener entre 8 y 15 ítems.
   - Redactar cada ítem como una acción concreta (verbo + objeto).
   - Eliminar cualquier nombre real de persona o empresa (use "Proveedor A", "Cliente X", "Sistema Y").

3. Si no trajo lista propia, copie la siguiente lista de ejemplo en su archivo:

```text
Lista de pendientes — Semana del [fecha actual]:

1. Redactar correo a Proveedor A por retraso en entrega de piezas de repuesto.
2. Actualizar firmware de switches del piso 3 (versión 2.4.1 pendiente desde hace 3 semanas).
3. Preparar informe de avance mensual para dirección general (entrega: viernes 5 p.m.).
4. Documentar procedimientos de respaldo semanal del servidor de base de datos.
5. Investigar alerta intermitente en servidor de BD (error código 5023, aparece cada 4 horas).
6. Revisar y aprobar solicitudes de acceso VPN de 4 usuarios nuevos.
7. Capacitar a técnico junior en uso del sistema de tickets de soporte.
8. Renovar licencias de antivirus (vencen en 15 días, requiere aprobación de presupuesto).
9. Actualizar diagrama de red con los cambios del último trimestre.
10. Responder auditoria interna sobre cumplimiento de política de contraseñas.
11. Probar plan de recuperación ante desastres (DRP) — ejercicio programado para este mes.
12. Coordinar con RRHH la baja de cuentas de 2 empleados que salieron la semana pasada.
```

4. Guarde el archivo.

**Resultado Esperado:** Una lista de 8–15 pendientes, anonimizada, con cada ítem redactado como acción concreta, guardada en su archivo de texto.

---

#### Paso 2 — Aplicar Priorización con MoSCoW y Puntaje Ponderado

**Objetivo:** Usar Copilot con un prompt CTF completo para obtener una tabla de priorización con categorías MoSCoW y puntaje ponderado.

**Instrucciones:**

1. En su archivo de Bloc de Notas, copie y complete el siguiente prompt. Reemplace `[PEGA AQUÍ TU LISTA]` con la lista del Paso 1:

```text
Contexto: Soy coordinador de TI en una empresa mediana. Necesito priorizar 
mis pendientes para esta semana considerando cuatro criterios: Impacto en 
operación del negocio, Urgencia por plazos o consecuencias inmediatas, 
Esfuerzo estimado en horas, y Riesgo operativo si no se atiende.

Tarea: Analiza la siguiente lista de pendientes y realiza dos cosas:
1) Clasifica cada ítem según el método MoSCoW (Must Have, Should Have, 
   Could Have, Won't Have esta semana).
2) Asigna un puntaje de 0 a 100 usando estos pesos: 
   Impacto 40% + Urgencia 30% + Esfuerzo inverso 20% + Riesgo 10%.
   Justifica cada puntaje en máximo una frase.

Formato:
- Tabla con columnas: N° | Tarea | Categoría MoSCoW | Puntaje (0-100) | Justificación (1 frase)
- Ordena la tabla de mayor a menor puntaje.
- Al final, agrega una sección "Top 3 para hoy" con un plan de 90 minutos 
  dividido en bloques de 30 minutos, incluyendo un criterio de éxito 
  verificable para cada bloque.

Pendientes:
[PEGA AQUÍ TU LISTA]
```

2. Revise el prompt en Bloc de Notas para asegurarse de que la lista está correctamente pegada.

3. Seleccione todo el texto del prompt (`Ctrl+A`), cópielo (`Ctrl+C`).

4. Vaya a la pestaña del navegador con Copilot (https://copilot.microsoft.com).

5. Haga clic en el campo de chat y pegue el prompt (`Ctrl+V`).

6. Presione `Enter` o haga clic en el botón de enviar.

7. Espere la respuesta completa de Copilot (puede tomar 15–30 segundos).

8. Una vez recibida la respuesta, copie el resultado completo y péguelo en su documento Word, en la sección **"Bloque 1: Priorización de Pendientes"**.

Copilot debe generar una tabla similar a esta (los valores variarán):

| N° | Tarea | Categoría MoSCoW | Puntaje (0-100) | Justificación |
|----|-------|-----------------|-----------------|---------------|
| 5 | Investigar alerta intermitente en servidor de BD | Must Have | 88 | Alto riesgo de caída de sistema con impacto inmediato en operaciones. |
| 3 | Preparar informe de avance para dirección | Must Have | 82 | Plazo fijo el viernes con consecuencia directa ante directivos. |
| 12 | Dar de baja cuentas de empleados salientes | Must Have | 79 | Riesgo de seguridad crítico por accesos activos no autorizados. |
| ... | ... | ... | ... | ... |

Seguido de una sección "Top 3 para hoy" con bloques de 30 minutos.

---

#### Paso 3 — Aplicar la Matriz de Eisenhower como Marco Alternativo

**Objetivo:** Comparar el resultado del Paso 2 con una priorización usando la Matriz de Eisenhower para desarrollar criterio crítico sobre los marcos de priorización.

**Instrucciones:**

1. Inicie una **nueva conversación** en Copilot (busque el botón "Nueva conversación" o equivalente en la interfaz).

> ⚠️ Es importante iniciar nueva conversación para evitar que el contexto anterior influya en este resultado.

2. En Bloc de Notas, prepare el siguiente prompt con su misma lista de pendientes:

```text
Contexto: Soy coordinador de TI. Tengo la misma lista de pendientes de la 
semana y quiero verla desde otra perspectiva de priorización.

Tarea: Clasifica cada ítem de la lista usando la Matriz de Eisenhower con 
sus cuatro cuadrantes:
- Cuadrante 1 (Hacer ahora): Urgente + Importante
- Cuadrante 2 (Planificar): No urgente + Importante  
- Cuadrante 3 (Delegar): Urgente + No importante
- Cuadrante 4 (Eliminar/Posponer): No urgente + No importante

Para cada ítem, explica en una frase por qué lo ubicaste en ese cuadrante.
Después, identifica 2 diferencias notables entre esta clasificación y una 
clasificación MoSCoW típica para este tipo de lista.

Formato: 
- Cuatro secciones, una por cuadrante, con viñetas.
- Cada viñeta: nombre de tarea + justificación de una frase.
- Al final: sección "Comparación MoSCoW vs. Eisenhower" con 2 puntos de diferencia.

Pendientes:
[PEGA AQUÍ TU LISTA]
```

3. Envíe el prompt a Copilot.

4. Copie el resultado al documento Word, en la misma sección **"Bloque 1"**, debajo del resultado anterior.

5. **Análisis personal (2 minutos):** Lea ambos resultados (MoSCoW y Eisenhower) y responda en su documento Word:
   - ¿Qué marco le resultó más útil para SU contexto de trabajo? ¿Por qué?
   - ¿Hubo alguna tarea que Copilot clasificó diferente a como usted la habría clasificado?

---

#### Paso 4 — Refinar con Prompt de Seguimiento

**Objetivo:** Practicar el refinamiento iterativo de prompts usando preguntas de seguimiento en la misma conversación.

**Instrucciones:**

1. En la **misma conversación** del Paso 3 (Eisenhower), escriba el siguiente prompt de seguimiento **sin copiar la lista nuevamente**:

```text
Gracias. Ahora toma solo los ítems del Cuadrante 1 (Urgente + Importante) 
y genera para cada uno:
- Tiempo estimado de resolución (en minutos u horas)
- Una persona o rol que podría apoyar o asumir la tarea
- Una consecuencia concreta si NO se atiende hoy

Formato: Una mini-ficha por tarea con los tres campos anteriores. 
Máximo 3 líneas por ficha.
```

2. Envíe el prompt y espere la respuesta.

3. Copie el resultado al documento Word.

4. **Reflexión de cierre del Bloque 1 (1 minuto):** En su documento Word, escriba una oración respondiendo: *¿Qué elemento del prompt CTF tuvo mayor impacto en la calidad del resultado en este bloque?*

---

### BLOQUE 2: Estructuración de una Tarea Técnica (30 minutos)

---

#### Paso 5 — Definir la Tarea Técnica a Estructurar

**Objetivo:** Seleccionar o definir la tarea técnica que se estructurará en los siguientes pasos.

**Instrucciones:**

1. Elija UNA de las siguientes opciones para su tarea técnica real de su área de trabajo. Ejemplos por sector:
   - **Mantenimiento industrial:** *Realizar mantenimiento preventivo mensual a compresor de aire de 50 HP.*
   - **Calidad:** *Ejecutar auditoría interna de proceso de soldadura según norma ISO 3834.*
   - **Administración:** *Cerrar el proceso de nómina quincenal y generar reportes de dispersión.*
   - **Logística:** *Ejecutar inventario físico cíclico de almacén de materias primas.*

2. En Bloc de Notas, escriba su tarea técnica seleccionada en una sola oración clara.

3. Defina también:
   - **Sistema/equipo involucrado:** (ej. "Ubuntu 22.04", "Compresor marca X modelo Y")
   - **Audiencia del documento resultante:** (ej. "Técnico junior con 1 año de experiencia")
   - **Restricción de tiempo:** (ej. "La tarea debe completarse en un turno de 8 horas")

---

#### Paso 6 — Generar la Guía Técnica Completa

**Objetivo:** Usar un prompt CTF avanzado para obtener una guía técnica estructurada con todos los componentes requeridos para su ejecución segura.

**Instrucciones:**

1. Inicie una **nueva conversación** en Copilot.

2. En Bloc de Notas, construya su prompt usando la siguiente plantilla. Reemplace los campos entre `[corchetes]` con la información de su tarea definida en el Paso 5:

```text
Contexto: Soy [tu rol, ej: "ingeniero de sistemas" / "técnico de mantenimiento" / 
"coordinador de calidad"]. Voy a ejecutar la siguiente tarea técnica: 
[DESCRIBE TU TAREA EN UNA ORACIÓN]. 
Sistema/equipo: [SISTEMA O EQUIPO]. 
La guía será usada por: [AUDIENCIA, ej: "técnico junior con 1 año de experiencia"].
Restricción de tiempo: [TIEMPO DISPONIBLE].

Tarea: Descompón este trabajo en los siguientes componentes:
1. PRE-REQUISITOS: Materiales, herramientas, accesos, conocimientos previos y 
   condiciones de seguridad necesarios antes de iniciar.
2. PASOS DETALLADOS: Secuencia numerada de acciones. Cada paso debe incluir 
   QUÉ hacer, CÓMO hacerlo y POR QUÉ es necesario.
3. PUNTOS DE CONTROL (checkpoints): Verificaciones específicas después de pasos 
   críticos para confirmar que el trabajo va correctamente. Incluye cómo verificar 
   (comando, medición, observación visual).
4. RIESGOS Y MITIGACIONES: Mínimo 3 riesgos con su probabilidad (Alta/Media/Baja), 
   impacto y acción de mitigación.
5. CRITERIOS DE ACEPTACIÓN: Lista de condiciones verificables que confirman que 
   la tarea se completó exitosamente (checklist Go/No-Go).
6. ESTIMACIÓN DE ESFUERZO: Desglose por bloques de 30 minutos indicando qué 
   actividades se realizan en cada bloque.

Formato: 
- Secciones claramente numeradas con los títulos anteriores.
- Pasos en lista numerada; riesgos en tabla (Riesgo | Probabilidad | Impacto | Mitigación).
- Comandos o instrucciones técnicas en bloques de código o formato destacado.
- Checklist Go/No-Go al final con casillas vacías [ ].
- Si falta información crítica para completar alguna sección, formula hasta 
  3 preguntas aclaratorias al INICIO de tu respuesta antes de continuar.
- Lenguaje adaptado para: [AUDIENCIA].
```

3. Revise el prompt, asegurándose de que todos los campos están completados.

4. Copie y pegue el prompt en Copilot. Envíe.

5. Si Copilot formula preguntas aclaratorias al inicio, respóndalas en el mismo chat antes de continuar.

6. Copie el resultado completo al documento Word, sección **"Bloque 2: Guía Técnica Estructurada"**.

---

#### Paso 7 — Adaptar la Guía para una Audiencia Diferente

**Objetivo:** Practicar la reutilización y adaptación de contenido generado por IA para diferentes audiencias usando un prompt de seguimiento.

**Instrucciones:**

1. En la **misma conversación** del Paso 6, envíe el siguiente prompt de seguimiento:

```text
Toma la guía que generaste y crea dos versiones adicionales:

Versión A — Para gerencia (máximo 150 palabras):
Resumen ejecutivo que explique: qué se va a hacer, por qué es necesario, 
qué riesgos existen, cuánto tiempo tomará y qué se necesita aprobar o 
proporcionar. Sin tecnicismos.

Versión B — Tarjeta de bolsillo para el técnico (máximo 20 ítems):
Lista ultra-condensada de los pasos más críticos y los 3 puntos de 
control más importantes. Formato checklist [ ]. 
Lenguaje directo y operativo.
```

2. Envíe y espere la respuesta.

3. Copie ambas versiones al documento Word, debajo de la guía completa.

4. **Reflexión (1 minuto):** En el documento Word, responda: *¿En qué situación real de su trabajo usaría cada una de las tres versiones (completa, gerencial, tarjeta de bolsillo)?*

---

#### Paso 8 — Solicitar Ramas Condicionales para Variantes del Procedimiento

**Objetivo:** Aplicar la técnica de ramas condicionales para manejar variantes de sistema o configuración en un mismo procedimiento.

**Instrucciones:**

1. En la **misma conversación**, envíe:

```text
Identifica los 3 pasos de la guía donde el procedimiento podría variar 
según el sistema operativo o la versión del software. Para cada uno, 
agrega una rama condicional con el formato:

SI [condición A] → [instrucción específica para A]
SI [condición B] → [instrucción específica para B]

Ejemplo de formato:
Paso X: Instalar gestor de paquetes
  SI Ubuntu 22.04 → sudo apt install [paquete] -y
  SI RHEL 9 / CentOS → sudo dnf install [paquete] -y
  SI Windows Server → [instrucción equivalente en PowerShell]
```

2. Envíe y copie el resultado al documento Word.

> 💡 **Nota para participantes de áreas no-TI:** Si su tarea no tiene variantes de sistema operativo, adapte la pregunta: *"Identifica los 3 pasos donde el procedimiento varía según el modelo del equipo / turno de trabajo / nivel de experiencia del técnico."*

---

### BLOQUE 3: Extracción de Puntos Clave de un Manual Extenso

---

#### Paso 9 — Preparar el Texto Fuente

**Objetivo:** Tener listo un texto de 800–1200 palabras para usar como fuente de extracción en los siguientes pasos.

**Instrucciones:**

1. **Si trajo su propio documento técnico:** Seleccione un fragmento de 800–1200 palabras de un manual, procedimiento o normativa de su empresa. Asegúrese de:
   - Eliminar nombres reales de personas, clientes o datos confidenciales.
   - Preferir secciones con procedimientos, normas o especificaciones técnicas.
   - Copiar el texto a su archivo de Bloc de Notas.

2. **Si no trajo documento propio:** Use el siguiente **Texto de Muestra del Instructor** — Fragmento de procedimiento de trabajos en altura (ficticio, solo para fines educativos):

```text
PROCEDIMIENTO OPERATIVO ESTÁNDAR — POE-SEG-017
TRABAJOS EN ALTURA — REVISIÓN 3.2

1. OBJETIVO Y ALCANCE
Este procedimiento establece los requisitos mínimos de seguridad para la 
ejecución de trabajos en altura en instalaciones de la empresa. Se considera 
"trabajo en altura" cualquier actividad realizada a una elevación de 1.8 metros 
o más sobre el nivel del suelo o sobre una superficie de trabajo inferior. 
Este procedimiento aplica a todo el personal propio y contratistas que realicen 
actividades de mantenimiento, construcción, inspección o limpieza en altura.

2. DEFINICIONES CLAVE
- Trabajo en altura: Toda actividad ejecutada a 1.8 m o más sobre nivel de piso.
- Arnés de cuerpo completo: Equipo de protección individual (EPI) que distribuye 
  las fuerzas de una caída en el cuerpo del trabajador. Componentes: correas de 
  hombro, pecho, cintura y piernas.
- Línea de vida: Sistema de cuerda o cable anclado a un punto fijo certificado 
  que permite la movilidad del trabajador manteniendo la protección contra caídas.
- Punto de anclaje: Estructura o elemento certificado capaz de soportar una carga 
  mínima de 2,270 kg (5,000 lb) por trabajador conectado.
- Permiso de trabajo en altura (PTA): Documento formal autorizado por el 
  supervisor de área que habilita la ejecución del trabajo. Válido por un turno.
- Zona de exclusión: Área delimitada debajo del trabajo en altura donde está 
  prohibido el tránsito de personal no autorizado.
- Caída libre: Distancia que recorre un trabajador antes de que el sistema de 
  detención de caídas comience a actuar. No debe exceder 1.8 m.
- Factor de caída: Relación entre la longitud de la caída libre y la longitud 
  del equipo de protección. A menor factor, mayor seguridad.

3. RESPONSABILIDADES
- Supervisor de área: Emitir el Permiso de Trabajo en Altura, verificar 
  condiciones del sitio, asegurar disponibilidad de EPI certificado y 
  designar al vigía de seguridad.
- Trabajador en altura: Inspeccionar su EPI antes de cada uso, reportar 
  cualquier defecto inmediatamente, no iniciar trabajo sin PTA vigente y 
  mantenerse conectado en todo momento mientras esté en altura.
- Vigía de seguridad: Permanecer en el área durante toda la ejecución del 
  trabajo, mantener despejada la zona de exclusión y actuar como primer 
  respondedor en caso de emergencia.
- Departamento de Seguridad: Validar el procedimiento anualmente, capacitar 
  al personal y realizar auditorías trimestrales de cumplimiento.

4. REQUISITOS PREVIOS AL TRABAJO
Antes de iniciar cualquier trabajo en altura se deben cumplir obligatoriamente:
a) Emisión y firma del Permiso de Trabajo en Altura por supervisor autorizado.
b) Inspección visual del arnés, línea de vida y conectores (buscar: cortes, 
   abrasiones, costuras dañadas, corrosión en herrajes, deformaciones).
c) Verificación del punto de anclaje: debe tener etiqueta de certificación 
   vigente y capacidad mínima de 2,270 kg.
d) Delimitación de la zona de exclusión con cinta de advertencia o barreras 
   físicas. Radio mínimo: igual a la altura de trabajo más 1.5 metros.
e) Verificación de condiciones climáticas: suspender trabajos si viento supera 
   50 km/h, si hay lluvia, tormenta eléctrica o visibilidad reducida.
f) Confirmación de que el trabajador recibió capacitación específica en el 
   último año (registro en sistema de RRHH).
g) Disponibilidad de kit de rescate en el área y al menos un trabajador 
   capacitado en rescate en altura.

5. PROCEDIMIENTO DE INSPECCIÓN DEL ARNÉS
5.1 Inspección visual exterior:
- Revisar todas las correas: deben estar íntegras, sin cortes ni abrasiones 
  mayores a 1 cm de profundidad.
- Verificar costuras: no deben presentar hilos sueltos, quemaduras ni 
  decoloración por exposición química.
- Inspeccionar herrajes metálicos (hebillas, conectores D): sin corrosión, 
  deformación ni fisuras visibles.

5.2 Inspección funcional:
- Probar el cierre y apertura de todas las hebillas: deben enclavar y liberar 
  con facilidad y sin fuerza excesiva.
- Verificar que los conectores tipo gancho tengan el seguro de cierre activo 
  y funcional.
- Confirmar que la etiqueta de fabricante es legible e indica: fecha de 
  fabricación, estándar de certificación (ANSI Z359 o equivalente) y 
  fecha de retiro (máximo 10 años desde fabricación o 5 años desde primer uso).

5.3 Criterios de retiro inmediato:
- Cualquier equipo que haya detenido una caída debe retirarse inmediatamente 
  del servicio, independientemente de su apariencia.
- Equipos con fecha de retiro vencida.
- Equipos con daños visibles que no puedan ser claramente evaluados en campo.

6. RESPUESTA A EMERGENCIAS
En caso de caída detenida por el sistema:
a) No intentar que el trabajador descienda solo: el síndrome de suspensión 
   puede causar pérdida de conciencia en 3–30 minutos.
b) Activar el plan de rescate inmediatamente. Llamar al número de emergencias 
   interno: Ext. [NÚMERO INTERNO].
c) Mantener comunicación verbal con el trabajador suspendido para monitorear 
   su estado de conciencia.
d) Si el trabajador pierde conciencia, el equipo de rescate debe actuar en 
   menos de 6 minutos para prevenir consecuencias graves.
e) Tras el rescate, el trabajador debe ser evaluado por personal médico antes 
   de regresar al trabajo, incluso si no presenta lesiones visibles.

7. REGISTROS Y DOCUMENTACIÓN
Todos los Permisos de Trabajo en Altura deben archivarse por un mínimo de 
3 años. Los registros de inspección de EPI deben mantenerse actualizados en 
el sistema de gestión de seguridad. Las no conformidades detectadas durante 
auditorías deben cerrarse en un plazo máximo de 30 días hábiles.
```

3. Confirme que el texto está en su archivo de Bloc de Notas, listo para ser copiado.

---

#### Paso 10 — Extracción Completa: Resumen, Riesgos, Glosario y Checklist

**Objetivo:** Usar el prompt de extracción CTF completo con delimitadores para obtener múltiples tipos de síntesis del documento fuente en una sola interacción.

**Instrucciones:**

1. Inicie una **nueva conversación** en Copilot.

2. En Bloc de Notas, construya el siguiente prompt. Reemplace `[PEGA AQUÍ EL TEXTO FUENTE]` con el texto del Paso 9:

```text
Contexto: Soy [tu rol, ej: "supervisor de seguridad" / "coordinador de área"] 
preparando una charla de capacitación de 10 minutos para [audiencia, ej: 
"técnicos de mantenimiento con experiencia básica en seguridad"]. 
El documento fuente es un procedimiento operativo interno.

Tarea: A partir del texto delimitado entre <<< y >>>, genera los siguientes 
cinco productos. Basa tus respuestas ÚNICAMENTE en el contenido del texto 
proporcionado. Si necesitas afirmar algo que no está explícito en el texto, 
márcalo claramente como "⚠️ Supuesto no confirmado en el texto fuente".

PRODUCTO 1 — Resumen ejecutivo (120–150 palabras):
Describe el propósito del documento, a quién aplica, los requisitos más 
importantes y las consecuencias de incumplimiento.

PRODUCTO 2 — 5 riesgos críticos con mitigación:
Tabla con columnas: Riesgo | Consecuencia | Medida de mitigación del documento.
Solo incluye riesgos mencionados explícita o implícitamente en el texto.

PRODUCTO 3 — Glosario de 8 términos clave:
Tabla con columnas: Término | Definición según el documento | Sección/Párrafo.
Usa las definiciones exactas del texto cuando estén disponibles.

PRODUCTO 4 — Checklist de inspección previa (máximo 10 ítems):
Lista de verificación [ ] con los pasos de preparación obligatorios antes 
de iniciar el trabajo descrito. Cita la sección del documento entre paréntesis.

PRODUCTO 5 — 5 preguntas abiertas para verificar comprensión:
Preguntas que un instructor podría hacer a los participantes para confirmar 
que entendieron los puntos críticos. No incluyas las respuestas.

Formato general: Cada producto claramente separado con su número y título. 
Viñetas o tablas según corresponda. Citas de sección entre paréntesis cuando 
sea posible.

Fuente:
<<<
[PEGA AQUÍ EL TEXTO FUENTE]
>>>
```

3. Revise que el texto fuente esté correctamente delimitado entre `<<<` y `>>>`.

4. Copie y pegue el prompt completo en Copilot. Envíe.

5. Espere la respuesta completa (puede tomar 30–45 segundos por la extensión).

6. Copie el resultado al documento Word, sección **"Bloque 3: Extracción de Puntos Clave"**.

---

#### Paso 11 — Generar Versiones Adicionales con Prompts de Seguimiento

**Objetivo:** Practicar la generación de productos adicionales a partir del mismo documento sin repetir el texto fuente.

**Instrucciones:**

1. En la **misma conversación** del Paso 10, envíe el siguiente prompt de seguimiento:

```text
Usando el mismo documento fuente que analizaste, genera:

A) Una matriz RACI simplificada con los roles mencionados en el documento 
   (filas: actividades clave; columnas: roles). Usa R=Responsable, 
   A=Aprobador, C=Consultado, I=Informado.

B) Un párrafo de "vacíos de información" (máximo 80 palabras): 
   ¿Qué preguntas importantes NO responde este documento que un 
   trabajador o supervisor podría necesitar saber?

C) Una recomendación de cuándo es NECESARIO leer el documento completo 
   vs. cuándo es suficiente el resumen generado. Máximo 3 líneas.
```

2. Envíe y espere la respuesta.

3. Copie el resultado al documento Word, el cual debe ser similar a este:

**Matriz RACI (ejemplo parcial):**
| Actividad | Supervisor | Trabajador | Vigía | Dpto. Seguridad |
|-----------|-----------|-----------|-------|----------------|
| Emitir PTA | A/R | I | I | C |
| Inspeccionar EPI | C | R | I | A |
| Delimitar zona exclusión | R | C | R | I |
| Rescate en emergencia | A | C | R | I |

---

## 7. Limpieza del Entorno

Al finalizar la práctica, realice las siguientes acciones:

**1. Guardar y organizar archivos:**
```
1. Confirmar que los siguientes archivos están guardados:
   - Lab03_Prompts_[TuNombre].txt (Bloc de Notas)
   - Lab03_Resultados_[TuNombre].docx (Word)
   - Lab03_Biblioteca_Prompts_[TuNombre].docx (Word)

2. Crear una carpeta en Documentos llamada: "Curso_Copilot_Labs"
3. Mover los tres archivos a esa carpeta
```

**2. Gestionar el historial de Copilot:**
```
1. En Copilot, revisar si existe opción de limpiar historial de conversaciones
   (depende de la versión y configuración corporativa)
2. Si trabaja en equipo compartido, cerrar sesión de Copilot:
   - Clic en el ícono de perfil (esquina superior derecha)
   - Seleccionar "Cerrar sesión"
3. Cerrar las pestañas del navegador usadas durante la práctica
```

**3. Verificar que no quedaron datos sensibles:**
```
1. Revisar el archivo Lab03_Prompts_[TuNombre].txt
2. Confirmar que no contiene nombres reales de clientes, empleados o 
   información financiera confidencial
3. Si se identifican datos sensibles, eliminarlos del archivo
```

> 💡 **Para llevar:** Los archivos `Lab03_Resultados` y `Lab03_Biblioteca_Prompts` son herramientas de trabajo real que puede usar inmediatamente después del curso. La biblioteca de prompts, en particular, crecerá con cada práctica y se convertirá en su referencia personal de productividad con IA.

---

## 8. Resumen

### Puntos Clave de la Práctica

En esta práctica aplicó el patrón **CTF (Contexto, Tarea, Formato)** en tres escenarios de productividad de alta frecuencia laboral:

| Bloque | Capacidad Desarrollada | Técnicas Clave Aplicadas |
|--------|----------------------|--------------------------|
| **Priorización** | Transformar una lista desordenada en un plan de acción priorizado y justificado | Pesos ponderados (40/30/20/10), MoSCoW, Eisenhower, prompts de seguimiento sin repetir contexto |
| **Estructuración técnica** | Convertir una tarea ambigua en una guía ejecutable con controles de calidad | 6 secciones estructuradas, ramas condicionales, adaptación por audiencia (gerencia vs. técnico) |
| **Extracción de manuales** | Sintetizar documentos extensos en productos accionables con trazabilidad | Delimitadores `<<< >>>`, solicitud de supuestos no confirmados, múltiples formatos de salida |

### Lecciones Aprendidas

1. **La calidad del output depende del Contexto:** Cuanto más específico sea el contexto (rol, sistema, audiencia, restricciones), más útil y preciso será el resultado.

2. **Los prompts de seguimiento son poderosos:** No es necesario repetir toda la información en cada mensaje. Copilot recuerda el contexto de la conversación activa.

3. **La validación humana es irremplazable:** Los resúmenes y guías generados por IA son puntos de partida, no documentos finales. Siempre requieren revisión experta, especialmente en contextos de seguridad.

4. **Los marcos de priorización tienen diferentes fortalezas:** MoSCoW es útil para gestión de proyectos y backlog; Eisenhower es más natural para gestión diaria de tiempo. Ambos son herramientas, no verdades absolutas.

5. **La biblioteca de prompts es un activo profesional:** Los prompts bien construidos y catalogados ahorran tiempo en cada uso futuro y mejoran con la iteración.

### Recursos Adicionales

| Recurso | URL | Relevancia |
|---------|-----|------------|
| Microsoft Learn: Introducción a Copilot para M365 | https://learn.microsoft.com/es-es/microsoft-365-copilot/overview | Fundamentos oficiales de Copilot |
| Ingeniería de prompts — Azure OpenAI | https://learn.microsoft.com/es-es/azure/ai-services/openai/concepts/prompt-engineering | Técnicas avanzadas de prompting |
| Matriz de Eisenhower (Atlassian) | https://www.atlassian.com/time-management/priority-matrix | Referencia del marco de priorización |
| Priorización MoSCoW (ProductPlan) | https://www.productplan.com/glossary/moscow-prioritization/ | Referencia del marco MoSCoW |
| Resumen de documentos con Copilot en Word | https://support.microsoft.com/es-es/office/introducción-a-microsoft-copilot-en-word-91d5b19a-8e61-4c9a-8427-474ce6a579a9 | Aplicación en Microsoft Word |

**Resultado Esperado:** 
- Dominio de Marcos de Priorización: El participante obtiene de Copilot una matriz estructurada (MoSCoW ) con justificaciones claras y un plan de acción de 90 minutos para ejecutar sus tareas operativas prioritarias.

- Ingeniería de Procedimientos Técnicos: Generación de guías técnicas paso a paso enriquecidas con la lógica Qué-Cómo-Por qué, puntos de control (checkpoints), análisis de riesgos y ramificaciones condicionales.
Extracción Controlada de Información: Capacidad de aislar contenido usando delimitadores, restringiendo la longitud de la respuesta y extrayendo simultáneamente resúmenes ejecutivos, tablas de riesgos, glosarios y checklists de inspección basados únicamente en el texto fuente.

- Pensamiento Crítico y Gobierno de Datos: Habilidad para auditar los sesgos o suposiciones de la IA mediante el uso explícito de etiquetas de advertencia antes de aplicar resúmenes o manuales en el entorno real de trabajo.
  
---

*© Material educativo para uso exclusivo en el curso. Los textos de muestra son ficticios y solo tienen propósito pedagógico. Versión 1.0*
