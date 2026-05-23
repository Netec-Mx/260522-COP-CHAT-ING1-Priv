# 1. Práctica 4. Creación de borradores para reportes de turno, listas de verificación de seguridad y formatos de inspección simple.

## Metadatos

| Campo            | Detalle                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Duración**     | 90 minutos                                                              |
| **Complejidad**  | Media                                                                   |
| **Nivel Bloom**  | Crear                                                                   |
| **Modalidad**    | Individual con discusión grupal al cierre                               |
| **Versión**      | 1.0 — 20260523-Rev1                                                     |

---

## Descripción General

En esta práctica aplicarás las técnicas de prompting estructurado (Contexto, Tarea y Formato) aprendidas en el curso para generar tres tipos de documentos operativos críticos: reportes de turno, listas de verificación de seguridad y formatos de inspección simple. Partirás de notas desordenadas y datos simulados para producir borradores profesionales con Microsoft Copilot, y luego los refinarás y exportarás a Word o Excel. La práctica cierra con una reflexión guiada sobre la validación humana de documentos generados por IA en entornos de seguridad y operaciones.

> ⚠️ **Aviso importante sobre datos:** No ingreses datos reales, confidenciales o de clientes de tu organización en Copilot. Usa exclusivamente los datos ficticios proporcionados en esta guía o crea tus propios datos de práctica anonimizados.

> ⚠️ **Validación humana obligatoria:** Los documentos generados en esta práctica son borradores de aprendizaje. Cualquier lista de verificación de seguridad o formato de inspección que desees implementar oficialmente en tu organización **debe ser revisado y validado por expertos humanos calificados** antes de su uso.

---

## Objetivos de Aprendizaje

Al completar esta práctica serás capaz de:

- [ ] Crear un borrador completo de reporte de turno usando Copilot a partir de notas operativas desordenadas, aplicando la plantilla de estructura mínima viable con campos obligatorios.
- [ ] Generar una lista de verificación de seguridad personalizada con criterios objetivos, escala OK/No OK/N.A. y evaluación global de aptitud.
- [ ] Diseñar un formato de inspección simple con campos de captura, clasificación de severidad y acción correctiva usando Copilot como asistente de diseño.
- [ ] Adaptar y personalizar los documentos generados por IA para que cumplan con estándares de estructura, trazabilidad y nomenclatura profesional.
- [ ] Exportar los documentos finales a Word o Excel y reflexionar sobre las mejores prácticas de validación antes del uso oficial.

---

## Prerrequisitos

### Conocimiento previo
- Haber completado la Práctica 1 (Lab 01-00-01) y preferiblemente la Práctica 2 (Lab 02-00-01).
- Comprender la estructura de prompts con Contexto, Tarea y Formato.
- Conocimiento básico del área operativa o de mantenimiento del participante (para personalizar los ejercicios opcionales).
- Familiaridad básica con Microsoft Word o Excel para copiar, pegar y formatear texto.

### Acceso y cuentas requeridas
- Acceso activo a **Microsoft Copilot** en [copilot.microsoft.com](https://copilot.microsoft.com) (cuenta Microsoft personal o corporativa).
- Acceso a **Microsoft Word** (Microsoft 365 o Word 2019) o **Word Online**.
- Acceso a **Microsoft Excel** (Microsoft 365 o Excel 2019) o **Excel Online**.
- Bloc de Notas (Notepad) o equivalente para preparar prompts antes de enviarlos.

> 💡 **Alternativa:** Si Copilot no está disponible por restricciones corporativas, puedes usar ChatGPT en [chat.openai.com](https://chat.openai.com). Los prompts de esta práctica son compatibles con ambas herramientas.

---

## Entorno de Laboratorio

### Requisitos de hardware

| Componente        | Mínimo requerido                              | Recomendado                          |
|-------------------|-----------------------------------------------|--------------------------------------|
| Procesador        | Intel Core i5 / AMD Ryzen 5 (4 núcleos)       | Intel Core i7 / AMD Ryzen 7          |
| Memoria RAM       | 8 GB                                          | 16 GB                                |
| Almacenamiento    | 2 GB libres en disco                          | 5 GB libres                          |
| Monitor           | 1280×768 px                                   | 1920×1080 px                         |
| Conexión a Internet | 10 Mbps de descarga                         | 25 Mbps o superior                   |
| Periféricos       | Teclado y ratón funcionales                   | Teclado ergonómico, monitor dual     |

### Requisitos de software

| Software                  | Versión mínima                        | Uso en esta práctica                         |
|---------------------------|---------------------------------------|----------------------------------------------|
| Microsoft Edge o Chrome   | Versión 120 o superior                | Acceder a Copilot                            |
| Microsoft Copilot (web)   | Versión web actual                    | Generar todos los borradores                 |
| Microsoft Word / Word Online | Microsoft 365 v2308 o Word 2019   | Formatear y guardar reporte de turno         |
| Microsoft Excel / Excel Online | Microsoft 365 v2308 o Excel 2019 | Formatear y guardar checklist e inspección   |
| Bloc de Notas / Notepad   | Cualquier versión del SO              | Preparar y almacenar prompts                 |

### Preparación del entorno (antes de comenzar)

Realiza los siguientes pasos de configuración **antes** de iniciar los ejercicios:

1. Abre tu navegador (Edge o Chrome) y navega a [copilot.microsoft.com](https://copilot.microsoft.com).
2. Inicia sesión con tu cuenta Microsoft. Verifica que la interfaz esté en **español**. Si no lo está, haz clic en el ícono de configuración (⚙️) y selecciona **Español** como idioma preferido.
3. Abre el **Bloc de Notas** (Notepad). Lo usarás para preparar y guardar tus prompts antes de enviarlos a Copilot.
4. Abre **Microsoft Word** (o Word Online en [office.com](https://office.com)) y crea un documento en blanco. Guárdalo con el nombre:
   ```
   Lab04_ReporteTurno_[TusIniciales]_[Fecha].docx
   ```
   Ejemplo: `Lab04_ReporteTurno_ATR_20260523.docx`
5. Abre **Microsoft Excel** (o Excel Online) y crea un libro en blanco. Guárdalo con el nombre:
   ```
   Lab04_Checklist_Inspeccion_[TusIniciales]_[Fecha].xlsx
   ```
6. Ajusta las ventanas en pantalla para poder alternar fácilmente entre Copilot, Word y Excel (se recomienda usar `Alt+Tab` o tener dos monitores si están disponibles).
7. En Copilot, inicia una **nueva conversación** haciendo clic en el botón **"Nueva conversación"** o el ícono de lápiz (✏️). Esto garantiza que no haya contexto previo que interfiera con los ejercicios.

---

## Ejercicios Paso a Paso

> 📋 **Estructura de la práctica:**
> - **Ejercicio 1** (30 min): Reporte de turno desde notas desordenadas
> - **Ejercicio 2** (25 min): Lista de verificación de seguridad
> - **Ejercicio 3** (20 min): Formato de inspección simple
> - **Cierre y reflexión** (15 min): Validación humana y mejores prácticas

---

### Ejercicio 1: Reporte de Turno desde Notas Operativas Desordenadas

**Objetivo del ejercicio:** Transformar un conjunto de notas breves y desordenadas (que simulan las anotaciones reales de un operador durante su turno) en un reporte de turno estructurado, profesional y completo usando Copilot.

**Tiempo estimado:** 30 minutos

---

#### Paso 1.1 — Revisar y preparar las notas de entrada

**Objetivo:** Familiarizarte con los datos de entrada antes de construir el prompt.

**Instrucciones:**

1. Lee con atención las siguientes notas ficticias que simulan las anotaciones de un operador del turno nocturno en una planta de utilidades industriales:

   ```
   NOTAS TURNO NOCHE — 22:00 a 06:00 — Área: Utilidades
   Operador saliente: A. Torres
   Operador entrante: M. Rivas

   - bomba B-12 empezó a vibrar mucho como a las 2am, medí 9.2 mm/s, 
     el límite es 7.5, activé la standby B-12S sin problemas, producción 
     no se afectó, abrí ticket de mantenimiento
   - reposición de EPP en almacén: guantes, lentes, tapones - ya hay 
     stock para más de 2 semanas
   - tormenta eléctrica prevista mañana entre 8am y 12pm según meteorología
   - compresor C-05 funcionando normal, temp 68°C (límite 85°C), 
     presión 6.2 bar (límite 8 bar)
   - válvula V-34 tiene goteo leve, no es urgente pero hay que revisarla 
     esta semana, le avisé a mecánico Pérez
   - el turno anterior dejó pendiente la calibración del sensor PT-201, 
     todavía sin hacer, vence el 25 de mayo
   - consumo energético del área: 847 kWh (normal para este turno)
   - sin accidentes ni incidentes de seguridad en el turno
   ```

2. En el **Bloc de Notas**, copia estas notas y guárdalas. Las usarás como entrada en el prompt.

3. Analiza las notas e identifica mentalmente:
   - ¿Cuántos incidentes hay y cuál es su severidad?
   - ¿Qué pendientes requieren transferencia al turno entrante?
   - ¿Qué información faltaría para un reporte completo?

**Salida esperada:** Comprensión clara del contenido de las notas y preparación mental para estructurar el prompt.

**Verificación:** Puedes continuar al siguiente paso cuando hayas identificado al menos 1 incidente (bomba B-12), 2 pendientes (calibración PT-201, válvula V-34) y 1 riesgo próximo (tormenta eléctrica).

---

#### Paso 1.2 — Construir y enviar el prompt de reporte de turno

**Objetivo:** Redactar un prompt completo con Contexto, Tarea y Formato para generar el reporte de turno.

**Instrucciones:**

1. En el **Bloc de Notas**, escribe el siguiente prompt. Puedes copiarlo y adaptarlo:

   ```
   CONTEXTO:
   Soy supervisor de operaciones en una planta industrial de utilidades.
   Necesito transformar notas desordenadas de un operador en un reporte
   de turno profesional y estructurado. El reporte debe ser claro,
   trazable y listo para firmar y distribuir al equipo gerencial.

   TAREA:
   Genera un borrador completo de Reporte de Turno usando las siguientes
   notas de entrada:

   [NOTAS DE ENTRADA]
   - bomba B-12 empezó a vibrar mucho como a las 2am, medí 9.2 mm/s,
     el límite es 7.5, activé la standby B-12S sin problemas, producción
     no se afectó, abrí ticket de mantenimiento
   - reposición de EPP en almacén: guantes, lentes, tapones - ya hay
     stock para más de 2 semanas
   - tormenta eléctrica prevista mañana entre 8am y 12pm según meteorología
   - compresor C-05 funcionando normal, temp 68°C (límite 85°C),
     presión 6.2 bar (límite 8 bar)
   - válvula V-34 tiene goteo leve, no es urgente pero hay que revisarla
     esta semana, le avisé a mecánico Pérez
   - el turno anterior dejó pendiente la calibración del sensor PT-201,
     todavía sin hacer, vence el 25 de mayo
   - consumo energético del área: 847 kWh (normal para este turno)
   - sin accidentes ni incidentes de seguridad en el turno
   [FIN NOTAS]

   FORMATO:
   Usa exactamente esta estructura en Markdown:

   # Reporte de Turno — ID: RT-20260523-Noche
   Fecha/Hora: 22:00 a 06:00 | Área: Utilidades
   Líder saliente: A. Torres | Líder entrante: M. Rivas

   ## Resumen Ejecutivo (máx. 5 viñetas priorizadas por riesgo)
   ## Novedades por Área/Activo (tabla con columnas: Área/Activo, Estado, Cambio Clave, Riesgo, KPI)
   ## Incidentes/Observaciones (con ID, Severidad Alta/Media/Baja, Descripción, Mitigación)
   ## Pendientes y Transferencias (con Responsable, Fecha de vencimiento, Estado)
   ## Decision Log (decisiones tomadas con hora y fundamento)

   Usa lenguaje profesional, frases cortas y voz activa. Asigna
   severidad a cada incidente. Genera IDs ficticios para incidentes
   (formato INC-###). Responde en español.
   ```

2. Copia el prompt completo del Bloc de Notas.

3. En Copilot, pega el prompt en el campo de texto y presiona **Enter** o haz clic en el botón de enviar.

4. Espera la respuesta completa de Copilot (puede tomar entre 15 y 45 segundos).

**Salida esperada:** Copilot generará un reporte de turno estructurado en Markdown con todas las secciones solicitadas, incluyendo tabla de novedades, incidente de la bomba B-12 con severidad asignada, pendientes con responsables y fechas, y al menos una entrada en el Decision Log.

**Verificación:** El reporte generado debe contener:
- [ ] Encabezado con ID de reporte, fecha/hora, área y nombres de líderes
- [ ] Al menos 3 viñetas en el Resumen Ejecutivo priorizadas por riesgo
- [ ] Tabla de Novedades con al menos 2 filas (B-12 y C-05)
- [ ] Incidente INC-### con severidad Media para la bomba B-12
- [ ] Al menos 2 pendientes con responsable y fecha de vencimiento
- [ ] Al menos 1 entrada en el Decision Log

---

#### Paso 1.3 — Refinar el reporte con un prompt de seguimiento

**Objetivo:** Practicar la iteración y mejora del borrador mediante un prompt de refinamiento.

**Instrucciones:**

1. Revisa el reporte generado por Copilot. Identifica al menos **dos aspectos** que quieras mejorar. Ejemplos comunes:
   - El Resumen Ejecutivo no está ordenado por nivel de riesgo.
   - Falta la sección de adjuntos/evidencia.
   - El tono no es suficientemente formal.
   - La tabla de novedades no incluye el KPI de consumo energético.

2. En la **misma conversación** de Copilot (sin iniciar una nueva), escribe un prompt de refinamiento. Adapta el siguiente ejemplo según lo que hayas identificado:

   ```
   Por favor mejora el reporte anterior con los siguientes cambios:
   1. Reordena el Resumen Ejecutivo colocando primero la alerta de
      tormenta eléctrica (mayor impacto potencial), luego el incidente
      de B-12, y al final las novedades de rutina.
   2. Agrega una sección "Adjuntos/Evidencia" al final con una lista
      de archivos ficticios (foto de vibrómetro, ticket de mantenimiento).
   3. Agrega una línea de "Distribución" indicando que el reporte debe
      enviarse a: Gerencia de Operaciones, Mantenimiento Rotativo,
      Seguridad Industrial.
   4. Mantén el mismo formato Markdown y el mismo nivel de detalle.
   ```

3. Envía el prompt y espera la respuesta refinada.

4. Compara la versión original y la versión refinada. Anota en el Bloc de Notas qué cambios realizó Copilot y si los cambios fueron satisfactorios.

**Salida esperada:** Una versión mejorada del reporte con el Resumen Ejecutivo reordenado, la sección de adjuntos agregada y la línea de distribución incluida.

**Verificación:** Confirma que la versión refinada:
- [ ] Muestra la alerta de tormenta como primera viñeta del Resumen Ejecutivo
- [ ] Incluye una sección de Adjuntos/Evidencia con al menos 2 ítems ficticios
- [ ] Incluye la línea de Distribución con los tres destinatarios indicados

---

#### Paso 1.4 — Exportar el reporte a Microsoft Word

**Objetivo:** Guardar el reporte profesional en un documento Word listo para distribución.

**Instrucciones:**

1. En la respuesta final de Copilot, selecciona **todo el texto del reporte** (desde el título `# Reporte de Turno...` hasta la última línea).

2. Copia el texto seleccionado (`Ctrl+C`).

3. Cambia a tu documento **Word** (`Lab04_ReporteTurno_[TusIniciales]_[Fecha].docx`).

4. Pega el contenido (`Ctrl+V`). Word puede pegarlo como texto plano o intentar interpretar el Markdown.

5. Aplica formato básico manualmente:
   - El título principal: **Estilo Título 1** (selecciona la línea del título → pestaña Inicio → Estilos → Título 1).
   - Los encabezados de sección (`##`): **Estilo Título 2**.
   - Convierte la tabla de Novedades: si se pegó como texto, selecciónala → pestaña Insertar → Tabla → Convertir texto en tabla.
   - Ajusta los márgenes a 2.5 cm en todos los lados (Diseño de página → Márgenes → Márgenes personalizados).

6. Guarda el documento (`Ctrl+S`).

7. Toma una **captura de pantalla** del documento formateado en Word y guárdala como:
   ```
   Lab04_Captura1_ReporteTurno_[TusIniciales].png
   ```

**Salida esperada:** Documento Word con el reporte de turno formateado, con estilos de título aplicados y tabla visible.

**Verificación:** El archivo `.docx` debe estar guardado y el documento debe mostrar claramente todas las secciones con jerarquía visual correcta (título principal más grande que los encabezados de sección).

---

### Ejercicio 2: Lista de Verificación de Seguridad

**Objetivo del ejercicio:** Generar una lista de verificación de seguridad personalizada con criterios objetivos, estados OK/No OK/N.A. y evaluación global de aptitud, usando Copilot con un prompt detallado.

**Tiempo estimado:** 25 minutos

---

#### Paso 2.1 — Definir el contexto de la checklist

**Objetivo:** Seleccionar el proceso o área para la checklist y preparar el prompt.

**Instrucciones:**

1. Para esta práctica, usarás el escenario de **arranque de compresor centrífugo en planta de utilidades**. Si prefieres usar un contexto más cercano a tu área de trabajo real, puedes adaptarlo (recuerda: sin datos confidenciales reales).

2. Antes de construir el prompt, define mentalmente los aspectos que debe cubrir una checklist de arranque de compresor:
   - EPP requerido para el operador
   - Condiciones del área (ventilación, accesos despejados, señalización)
   - Verificación del equipo antes del arranque (niveles de aceite, temperatura, presión)
   - Sistemas de seguridad activos (válvulas de alivio, paros de emergencia)
   - Comunicación con sala de control
   - Procedimientos de emergencia disponibles

3. En el **Bloc de Notas**, escribe el prompt que construirás en el siguiente paso.

**Salida esperada:** Claridad sobre los aspectos a cubrir y prompt preparado en el Bloc de Notas.

**Verificación:** Puedes continuar cuando tengas identificadas al menos 5 categorías de verificación para el arranque de compresor.

---

#### Paso 2.2 — Generar la lista de verificación con Copilot

**Objetivo:** Enviar el prompt estructurado y obtener una checklist completa y funcional.

**Instrucciones:**

1. En Copilot, inicia una **nueva conversación** (clic en el ícono de lápiz ✏️ o botón "Nueva conversación").

2. Copia y pega el siguiente prompt desde el Bloc de Notas:

   ```
   CONTEXTO:
   Soy técnico de seguridad industrial en una planta de utilidades.
   Necesito una lista de verificación formal para el arranque seguro
   de un compresor centrífugo (equipo C-05). Esta checklist será
   usada por operadores certificados antes de cada arranque y debe
   cumplir con estándares de seguridad industrial.

   TAREA:
   Crea una Lista de Verificación de Seguridad completa para el
   arranque del compresor C-05 con las siguientes características:
   - Mínimo 12 ítems distribuidos en al menos 4 categorías:
     (1) EPP del operador, (2) Condiciones del área,
     (3) Verificación del equipo, (4) Sistemas de seguridad.
   - Cada ítem debe tener un criterio de aceptación objetivo y
     medible (no subjetivo).
   - Marca 2 ítems como "No OK" con observación y acción inmediata.
   - Incluye una regla de evaluación global clara:
     "Apto para arranque" solo si TODOS los ítems críticos son OK.
   - Agrega un bloque de firmas al final.

   FORMATO:
   Presenta la checklist como una tabla Markdown con estas columnas:
   | # | Categoría | Ítem de Verificación | Criterio de Aceptación | Estado (OK/No OK/N.A.) | Evidencia Requerida | Observaciones |

   Después de la tabla, agrega:
   - Evaluación Global: Apto / No Apto para arranque
   - Acciones Inmediatas requeridas (lista numerada)
   - Bloque de firmas: Inspector, Supervisor, Fecha/Hora

   Usa lenguaje técnico preciso. Responde en español.
   ```

3. Envía el prompt y espera la respuesta.

4. Lee la checklist generada con atención crítica. Pregúntate:
   - ¿Los criterios de aceptación son realmente objetivos y medibles?
   - ¿Hay ítems críticos de seguridad que Copilot omitió?
   - ¿Las acciones inmediatas para los ítems "No OK" son específicas y realizables?

**Salida esperada:** Una tabla Markdown con al menos 12 ítems de verificación organizados en 4 categorías, 2 ítems marcados como "No OK" con observaciones, evaluación global y bloque de firmas.

**Verificación:** La checklist generada debe contener:
- [ ] Al menos 12 ítems en la tabla
- [ ] Las 4 categorías solicitadas (EPP, Condiciones, Equipo, Seguridad)
- [ ] Criterios de aceptación con valores numéricos o condiciones verificables (no frases como "en buen estado")
- [ ] Exactamente 2 ítems marcados como "No OK" con observación y acción
- [ ] Evaluación global con regla explícita
- [ ] Bloque de firmas al final

---

#### Paso 2.3 — Solicitar versión para Excel

**Objetivo:** Obtener la checklist en un formato optimizado para Excel con campos adicionales de utilidad práctica.

**Instrucciones:**

1. En la **misma conversación**, envía el siguiente prompt de seguimiento:

   ```
   Ahora necesito adaptar esta checklist para usarla en Microsoft Excel.
   Por favor:
   1. Reformatea la tabla para que sea más compacta y adecuada para Excel
      (elimina la columna de Evidencia Requerida y agrégala como nota
      dentro de Observaciones).
   2. Agrega una columna "Crítico (S/N)" que indique si el ítem es
      crítico para la seguridad (un No OK en un ítem crítico bloquea
      el arranque automáticamente).
   3. Agrega una fila de encabezado adicional antes de la tabla con:
      - Nombre del documento: Lista de Verificación de Arranque C-05
      - Versión: 1.0
      - Fecha de vigencia: 2026-05-23
      - Próxima revisión: 2026-11-23
   4. Presenta el resultado como texto separado por tabulaciones (TSV)
      para facilitar el pegado directo en Excel.
   ```

2. Envía el prompt y espera la respuesta.

3. Copia el contenido TSV generado por Copilot.

4. Abre tu archivo **Excel** (`Lab04_Checklist_Inspeccion_[TusIniciales]_[Fecha].xlsx`).

5. Haz clic en la celda **A1** de la primera hoja. Renombra la hoja como `Checklist_C05` (doble clic en la pestaña de la hoja → escribe el nuevo nombre → Enter).

6. Pega el contenido (`Ctrl+V`). Si Excel no separa correctamente las columnas:
   - Selecciona la columna A completa.
   - Ve a **Datos** → **Texto en columnas** → **Delimitado** → marca **Tabulación** → **Finalizar**.

7. Aplica formato básico:
   - Fila de encabezados (metadatos): fondo **azul oscuro**, texto **blanco**, fuente en negrita.
   - Fila de títulos de columna: fondo **azul claro**, texto en negrita.
   - Ítems marcados "No OK": fondo **rojo claro** (selecciona las celdas de estado → Inicio → Color de relleno → rojo claro).
   - Ítems marcados "OK": fondo **verde claro**.
   - Ajusta el ancho de columnas (selecciona todas → doble clic en borde de columna para autoajustar).

8. Guarda el archivo (`Ctrl+S`).

**Salida esperada:** Hoja de Excel con la checklist formateada, columna "Crítico (S/N)" visible, ítems No OK resaltados en rojo y metadatos de versión en el encabezado.

**Verificación:** El archivo Excel debe mostrar:
- [ ] Encabezado con metadatos del documento (nombre, versión, fecha)
- [ ] Columna "Crítico (S/N)" correctamente poblada
- [ ] Celdas de ítems "No OK" con fondo rojo claro
- [ ] Todas las columnas visibles sin texto cortado

---

### Ejercicio 3: Formato de Inspección Simple

**Objetivo del ejercicio:** Diseñar un formato de inspección simple con secciones estructuradas, campos de captura, escala de severidad y acción correctiva, usando Copilot como asistente de diseño.

**Tiempo estimado:** 20 minutos

---

#### Paso 3.1 — Generar el formato de inspección con prompt detallado

**Objetivo:** Crear un formato de inspección completo para un hallazgo específico.

**Instrucciones:**

1. En Copilot, inicia una **nueva conversación** (clic en ✏️).

2. En el **Bloc de Notas**, prepara el siguiente prompt:

   ```
   CONTEXTO:
   Soy inspector de mantenimiento en una planta industrial. Durante
   una ronda de inspección detecté una fuga menor en la válvula V-102
   del sistema de vapor de baja presión (línea de 3 bar). Necesito
   documentar este hallazgo en un formato de inspección formal que
   sea trazable, auditable y que defina claramente la acción
   correctiva con responsable y plazo.

   TAREA:
   Genera un Formato de Inspección Simple completo para este hallazgo
   con las siguientes secciones y requisitos:

   SECCIÓN 1 - IDENTIFICACIÓN:
   - ID de inspección (formato: INSP-20260523-001)
   - Nombre del activo y código de etiqueta (V-102)
   - Sistema al que pertenece
   - Ubicación exacta (área, fila, nivel)
   - Nombre del inspector (usa nombre ficticio)
   - Fecha y hora del hallazgo

   SECCIÓN 2 - DESCRIPCIÓN DEL HALLAZGO:
   - Condición encontrada (descripción técnica breve)
   - Estándar esperado o referencia normativa
   - Comparación condición vs. estándar
   - Estimación del impacto si no se atiende

   SECCIÓN 3 - CLASIFICACIÓN:
   - Severidad: Alta / Media / Baja (con justificación)
   - Prioridad de atención: Inmediata / 24h / 48h / 1 semana
   - Riesgo principal: Seguridad / Producción / Calidad / Ambiental

   SECCIÓN 4 - ACCIÓN CORRECTIVA:
   - Acción propuesta (qué debe hacerse)
   - Responsable asignado (nombre y área)
   - Fecha objetivo de cierre
   - Número de Orden de Trabajo (ficticio, formato OT-XXXXX)

   SECCIÓN 5 - EVIDENCIA:
   - Lista de fotos tomadas (nombres de archivo ficticios)
   - Documentos de referencia

   SECCIÓN 6 - CIERRE Y VERIFICACIÓN:
   - Estado actual: Abierto
   - Campos para fecha de cierre y verificación de eficacia
   - Firmas: Inspector, Supervisor, Responsable de cierre

   FORMATO:
   Presenta cada sección claramente delimitada con título en negrita.
   Usa una combinación de campos etiquetados (Etiqueta: Valor) y
   tablas donde sea apropiado. Al final, agrega una versión compacta
   en formato YAML del mismo hallazgo (solo los campos clave).
   Responde en español.
   ```

3. Envía el prompt y espera la respuesta completa.

4. Revisa el formato generado verificando que todas las secciones estén presentes y que la información sea técnicamente coherente (por ejemplo, que una fuga de vapor de 3 bar tenga severidad Media o Alta, no Baja).

**Salida esperada:** Un formato de inspección completo con las 6 secciones solicitadas, información técnicamente coherente para una fuga de válvula, y una versión YAML compacta al final.

**Verificación:** El formato debe contener:
- [ ] Las 6 secciones claramente delimitadas con títulos
- [ ] ID de inspección en formato INSP-20260523-001
- [ ] Clasificación de severidad con justificación (no solo la etiqueta)
- [ ] Acción correctiva con responsable, fecha y número de OT ficticio
- [ ] Lista de evidencias (fotos ficticias)
- [ ] Versión YAML al final con campos clave

---

#### Paso 3.2 — Crear un formato de inspección genérico y reutilizable

**Objetivo:** Transformar el formato específico en una plantilla en blanco reutilizable para cualquier activo.

**Instrucciones:**

1. En la **misma conversación**, envía el siguiente prompt:

   ```
   Excelente. Ahora necesito convertir ese formato en una PLANTILLA
   EN BLANCO reutilizable. Por favor:
   1. Reemplaza todos los valores específicos de la válvula V-102 con
      campos vacíos o marcadores de posición en formato {{campo}}.
   2. En los campos de selección (como Severidad, Prioridad, Riesgo),
      mantén todas las opciones disponibles y agrega instrucciones
      breves entre corchetes, por ejemplo:
      Severidad: [ ] Alta  [ ] Media  [ ] Baja
   3. Agrega al inicio del documento un bloque de control con:
      - Nombre del documento
      - Código del documento (FORM-INSP-001)
      - Versión (1.0)
      - Fecha de emisión
      - Departamento responsable
      - Frecuencia de uso recomendada
   4. Mantén la versión YAML al final, también con campos vacíos.
   5. El resultado debe poder imprimirse en 1-2 páginas tamaño carta.
   ```

2. Envía el prompt y espera la respuesta.

3. Copia el contenido de la plantilla generada.

4. En tu archivo **Excel**, crea una **segunda hoja** y renómbrala como `Formato_Inspeccion`.

5. En la celda A1, pega el contenido de la plantilla. Aplica formato básico:
   - Títulos de sección: negrita, tamaño de fuente 12, fondo gris claro.
   - Campos de captura: celdas con borde visible para facilitar el llenado.
   - Ajusta el ancho de columna A a 180 px para que el texto sea legible.

6. Alternativamente, puedes pegar la plantilla en tu documento **Word** en una nueva página después del reporte de turno, si prefieres trabajar en un solo archivo.

7. Guarda el archivo.

**Salida esperada:** Plantilla de inspección en blanco con campos {{marcadores}}, casillas de selección para clasificación, bloque de control con metadatos del documento y versión YAML vacía.

**Verificación:** La plantilla debe:
- [ ] Tener bloque de control con código FORM-INSP-001 y versión 1.0
- [ ] Mostrar campos vacíos en formato {{campo}} en lugar de valores específicos
- [ ] Incluir casillas de selección para Severidad, Prioridad y Riesgo
- [ ] Estar guardada en Excel o Word

---

#### Paso 3.3 — Generar un segundo ejemplo con escala numérica de calificación

**Objetivo:** Practicar la creación de un formato de inspección alternativo que use escala numérica en lugar de categórica.

**Instrucciones:**

1. En la **misma conversación**, envía el siguiente prompt:

   ```
   Para complementar el formato anterior, crea una versión alternativa
   de formato de inspección que use una ESCALA NUMÉRICA de calificación
   del 1 al 5, donde:
   1 = Crítico (requiere parada inmediata)
   2 = Deficiente (acción en 24 horas)
   3 = Regular (acción en 1 semana)
   4 = Aceptable (monitoreo)
   5 = Excelente (sin acción requerida)

   El formato debe ser para inspección de condición general de una
   subestación eléctrica (área ficticia: Sub-E01). Incluye al menos
   8 puntos de inspección distribuidos en:
   - Condición física del equipo (3 puntos)
   - Sistemas de protección (3 puntos)
   - Condiciones del área (2 puntos)

   Para cada punto incluye: descripción, calificación (1-5), observación.
   Al final calcula un "Índice de Condición General" como el promedio
   de todas las calificaciones y define rangos de interpretación:
   - 4.0 - 5.0: Condición satisfactoria
   - 3.0 - 3.9: Requiere atención programada
   - 2.0 - 2.9: Requiere atención urgente
   - 1.0 - 1.9: Requiere parada y acción inmediata

   Presenta el resultado como tabla Markdown. Responde en español.
   ```

2. Envía el prompt y revisa la tabla generada.

3. Copia la tabla y pégala en una **tercera hoja** de tu archivo Excel, renombrada como `Inspeccion_Numerica`.

4. En Excel, agrega una fórmula para calcular automáticamente el Índice de Condición General:
   - Identifica la columna de calificaciones (supongamos que es la columna C, filas 3 a 10).
   - En la celda C12, escribe:
     ```
     =PROMEDIO(C3:C10)
     ```
   - En la celda D12, escribe una fórmula condicional para mostrar la interpretación:
     ```
     =SI(C12>=4,"Condición satisfactoria",SI(C12>=3,"Requiere atención programada",SI(C12>=2,"Requiere atención urgente","Requiere parada inmediata")))
     ```
   - Ajusta los rangos de fila según cómo Copilot haya estructurado la tabla.

5. Guarda el archivo.

**Salida esperada:** Tabla de inspección de subestación eléctrica con escala 1-5, al menos 8 puntos de inspección y fórmula de Índice de Condición General funcionando en Excel.

**Verificación:** 
- [ ] La tabla tiene al menos 8 puntos de inspección en 3 categorías
- [ ] La fórmula `=PROMEDIO(...)` calcula un valor numérico visible
- [ ] La fórmula `=SI(...)` muestra la interpretación textual correcta
- [ ] El archivo Excel tiene las 3 hojas: Checklist_C05, Formato_Inspeccion, Inspeccion_Numerica

---

### Cierre y Reflexión: Validación Humana y Mejores Prácticas

**Objetivo:** Consolidar el aprendizaje mediante reflexión crítica sobre el uso responsable de IA para documentación de seguridad y operaciones.

**Tiempo estimado:** 15 minutos

---

#### Paso 4.1 — Autoevaluación de los documentos generados

**Instrucciones:**

1. Revisa los tres documentos que generaste durante la práctica:
   - Reporte de Turno (Word)
   - Lista de Verificación de Seguridad (Excel, hoja Checklist_C05)
   - Formato de Inspección (Excel, hojas Formato_Inspeccion e Inspeccion_Numerica)

2. Para cada documento, responde las siguientes preguntas en el **Bloc de Notas**:

   ```
   AUTOEVALUACIÓN DE DOCUMENTOS GENERADOS POR IA
   ================================================

   REPORTE DE TURNO:
   - ¿El resumen ejecutivo está ordenado por nivel de riesgo? (S/N)
   - ¿Todos los pendientes tienen responsable y fecha de vencimiento? (S/N)
   - ¿El lenguaje es claro, conciso y en voz activa? (S/N)
   - ¿Qué información crítica podría haber omitido Copilot? (texto libre)

   LISTA DE VERIFICACIÓN:
   - ¿Los criterios de aceptación son objetivos y medibles? (S/N)
   - ¿La regla de evaluación global es inequívoca? (S/N)
   - ¿Hay ítems de seguridad críticos que no aparecen? (texto libre)
   - ¿Usarías esta checklist directamente sin revisión experta? (S/N + justificación)

   FORMATO DE INSPECCIÓN:
   - ¿La clasificación de severidad es técnicamente correcta? (S/N)
   - ¿La acción correctiva es específica y accionable? (S/N)
   - ¿El formato captura suficiente información para una auditoría? (S/N)
   - ¿Qué campo adicional agregarías para tu contexto real? (texto libre)
   ```

3. Guarda el archivo de autoevaluación con el nombre:
   ```
   Lab04_Autoevaluacion_[TusIniciales]_[Fecha].txt
   ```

**Salida esperada:** Archivo de autoevaluación completado con reflexiones críticas sobre cada documento.

---

#### Paso 4.2 — Enviar prompt de reflexión a Copilot

**Objetivo:** Usar Copilot para obtener una lista de mejores prácticas de validación, complementando la reflexión propia.

**Instrucciones:**

1. En Copilot, inicia una **nueva conversación**.

2. Envía el siguiente prompt:

   ```
   CONTEXTO:
   Soy supervisor de operaciones y acabo de usar IA generativa para
   crear borradores de: (1) un reporte de turno, (2) una lista de
   verificación de seguridad para arranque de compresor, y (3) un
   formato de inspección industrial.

   TAREA:
   Genera una guía concisa de MEJORES PRÁCTICAS para validar
   documentos de seguridad y operaciones generados por IA antes
   de su implementación oficial. La guía debe incluir:

   1. Los 5 riesgos principales de usar documentos de IA sin validación
      en entornos de seguridad industrial.
   2. Un proceso de revisión en 4 pasos para validar checklists de
      seguridad con expertos humanos.
   3. Criterios mínimos de aceptación que debe cumplir un documento
      de IA antes de ser aprobado para uso oficial.
   4. Roles responsables de la validación (quién debe revisar qué).

   FORMATO:
   Usa encabezados numerados, listas con viñetas y un cuadro resumen
   final. Máximo 1 página. Responde en español.
   ```

3. Copia la respuesta generada y pégala en tu documento **Word**, en una nueva página al final del reporte de turno, con el título: **"Anexo: Mejores Prácticas para Validación de Documentos Generados por IA"**.

4. Guarda el documento Word.

**Salida esperada:** Guía de mejores prácticas de validación integrada como anexo en el documento Word, con los 5 riesgos, proceso de 4 pasos, criterios de aceptación y roles de validación.

**Verificación:**
- [ ] La guía está pegada en el documento Word como anexo
- [ ] Cubre los 4 puntos solicitados en el prompt
- [ ] El documento Word está guardado con el anexo incluido

---

## Validación y Pruebas Finales

Antes de cerrar la práctica, realiza la siguiente verificación integral de todos los entregables:

### Lista de verificación de entregables

| # | Entregable | Criterio de Éxito | ¿Completado? |
|---|------------|-------------------|--------------|
| 1 | `Lab04_ReporteTurno_[TusIniciales]_[Fecha].docx` | Contiene reporte refinado con 5 secciones + Anexo de mejores prácticas | [ ] |
| 2 | `Lab04_Checklist_Inspeccion_[TusIniciales]_[Fecha].xlsx` — Hoja `Checklist_C05` | Checklist con ≥12 ítems, columna Crítico, formato de colores aplicado | [ ] |
| 3 | `Lab04_Checklist_Inspeccion_[TusIniciales]_[Fecha].xlsx` — Hoja `Formato_Inspeccion` | Plantilla en blanco con campos {{marcadores}} y bloque de control | [ ] |
| 4 | `Lab04_Checklist_Inspeccion_[TusIniciales]_[Fecha].xlsx` — Hoja `Inspeccion_Numerica` | Tabla con escala 1-5 y fórmulas de promedio e interpretación funcionando | [ ] |
| 5 | `Lab04_Autoevaluacion_[TusIniciales]_[Fecha].txt` | Autoevaluación completada para los 3 documentos | [ ] |
| 6 | Captura de pantalla del reporte en Word | Imagen guardada mostrando formato aplicado | [ ] |

### Prueba de calidad de prompts

Para verificar que dominaste la técnica de prompting estructurado, responde las siguientes preguntas sin consultar la guía:

1. ¿Cuáles son los tres componentes del prompt estructurado aplicados en esta práctica?
2. ¿Qué diferencia hay entre un criterio de aceptación objetivo y uno subjetivo en una checklist?
3. ¿Por qué se recomienda iniciar una nueva conversación en Copilot para cada ejercicio diferente?
4. ¿Qué campos mínimos debe tener un formato de inspección para ser auditable?

> 💡 **Respuestas esperadas:** (1) Contexto, Tarea y Formato. (2) Objetivo: valor numérico o condición verificable; subjetivo: "en buen estado". (3) Para evitar que el contexto de conversaciones anteriores contamine las nuevas respuestas. (4) ID, activo, inspector, fecha, condición encontrada, estándar esperado, severidad, acción correctiva y evidencia.

---

## Solución de Problemas

### Problema 1: Copilot genera la respuesta en inglés o mezcla idiomas

**Síntoma:** La respuesta de Copilot aparece total o parcialmente en inglés, a pesar de que el prompt fue escrito en español.

**Causa probable:** La configuración de idioma de Copilot está establecida en inglés, o el navegador tiene preferencia de idioma en inglés, lo que puede influir en el idioma de las respuestas.

**Solución:**

1. Al final de tu prompt, agrega explícitamente la instrucción: `Responde completamente en español. No uses inglés en ninguna parte de la respuesta.`
2. Si el problema persiste, verifica la configuración de idioma de Copilot: haz clic en el ícono de configuración (⚙️) en la esquina superior derecha → busca la opción de idioma → selecciona **Español (España)** o **Español (México)** según tu preferencia.
3. Verifica también que el idioma de tu navegador esté configurado en español: en Edge, ve a **Configuración** → **Idiomas** → asegúrate de que el español aparezca primero en la lista.
4. Si usas la alternativa ChatGPT, escribe al inicio de cada prompt: `Por favor responde siempre en español.`

---

### Problema 2: Las tablas generadas por Copilot no se pegan correctamente en Excel

**Síntoma:** Al copiar una tabla Markdown de Copilot y pegarla en Excel, todo el contenido aparece en una sola columna (columna A), sin separación entre celdas, o los caracteres `|` aparecen como texto literal.

**Causa probable:** Excel no interpreta el formato de tabla Markdown directamente. El contenido se pega como texto plano sin reconocer los separadores de columna.

**Solución — Método 1 (Texto en columnas):**
1. Pega el contenido en la columna A de Excel.
2. Selecciona toda la columna A.
3. Ve a la pestaña **Datos** → **Texto en columnas**.
4. Selecciona **Delimitado** → **Siguiente**.
5. Marca la casilla **Otro** e ingresa el carácter `|` en el campo de texto → **Siguiente** → **Finalizar**.
6. Elimina las columnas vacías que se generan al inicio y al final (resultado de los `|` de los bordes de la tabla Markdown).

**Solución — Método 2 (Solicitar TSV a Copilot):**
1. En lugar de copiar la tabla Markdown directamente, envía un prompt adicional a Copilot: `Por favor, convierte la tabla anterior a formato TSV (valores separados por tabulaciones) para poder pegarla directamente en Excel.`
2. Copia el resultado TSV y pégalo directamente en Excel. Las columnas se separarán automáticamente.

**Solución — Método 3 (Word como intermediario):**
1. Pega la tabla Markdown en Microsoft Word.
2. Word generalmente convierte las tablas Markdown automáticamente.
3. Selecciona la tabla ya formateada en Word → cópiala → pégala en Excel.

---

## Limpieza y Cierre

Al finalizar la práctica, realiza los siguientes pasos de cierre:

1. **Guarda todos los archivos** una última vez:
   - `Ctrl+S` en Word
   - `Ctrl+S` en Excel
   - Guarda el archivo `.txt` de autoevaluación en el Bloc de Notas

2. **Organiza los archivos** en una carpeta dedicada:
   ```
   Mis Documentos/
   └── Curso_Copilot/
       └── Lab04_Practica4/
           ├── Lab04_ReporteTurno_[TusIniciales]_[Fecha].docx
           ├── Lab04_Checklist_Inspeccion_[TusIniciales]_[Fecha].xlsx
           ├── Lab04_Autoevaluacion_[TusIniciales]_[Fecha].txt
           └── Lab04_Captura1_ReporteTurno_[TusIniciales].png
   ```

3. **Cierra las conversaciones de Copilot:** No es necesario eliminarlas, pero es buena práctica cerrar las pestañas del navegador usadas durante la práctica para liberar memoria.

4. **Guarda tus prompts favoritos:** Si identificaste prompts que funcionaron especialmente bien durante la práctica, cópialos en un archivo separado llamado `MisPrompts_Lab04.txt`. Estos prompts son reutilizables en tu trabajo diario.

5. **Reflexión final (opcional):** Antes de cerrar, escribe en el Bloc de Notas una respuesta breve a esta pregunta: *"¿Cuál de los tres tipos de documentos (reporte de turno, checklist de seguridad, formato de inspección) representa el mayor ahorro de tiempo para tu trabajo actual, y por qué?"* Esta reflexión puede compartirse en la discusión grupal de cierre del curso.

---

## Resumen

### Lo que aprendiste en esta práctica

En esta práctica aplicaste las técnicas de prompting estructurado al contexto más exigente del curso: la documentación de seguridad y operaciones industriales, donde la claridad, trazabilidad y precisión no son opcionales sino críticas.

**Conceptos clave consolidados:**

- **Estructura mínima viable:** Los tres tipos de documentos (reporte de turno, checklist, inspección) comparten principios de campos obligatorios, trazabilidad y decisión guiada. El prompt debe especificar exactamente qué campos incluir para obtener un borrador completo.

- **Prompting iterativo:** Ningún documento quedó perfecto en el primer intento. Aprendiste a enviar prompts de refinamiento en la misma conversación para mejorar el orden, agregar secciones faltantes o cambiar el formato de salida.

- **Adaptación de formato:** Copilot puede generar el mismo contenido en Markdown, tabla, YAML o TSV según lo que necesites. Especificar el formato de salida en el prompt es tan importante como especificar el contenido.

- **Validación humana como principio no negociable:** Los documentos generados por IA son borradores de alta calidad, no documentos oficiales. En entornos de seguridad industrial, la validación por expertos humanos calificados es obligatoria antes de cualquier implementación oficial.

- **Criterios objetivos vs. subjetivos:** Una checklist de seguridad solo es útil si sus criterios de aceptación son medibles y verificables. Aprendiste a pedir a Copilot criterios con valores numéricos o condiciones específicas, no frases vagas.

### Próximos pasos recomendados

- Adapta las plantillas generadas en esta práctica a tu área de trabajo real (con datos anonimizados) y compártelas con tu equipo para obtener retroalimentación.
- Crea una biblioteca personal de prompts para los documentos que generas con mayor frecuencia en tu rol.
- Explora la integración de Copilot directamente en Word y Excel (Microsoft 365 Copilot) para generar documentos sin salir de las aplicaciones de Office.
- Revisa las referencias normativas (ISO 45001, OSHA) para asegurarte de que tus checklists de seguridad cubren los requisitos regulatorios aplicables a tu industria.

### Referencias y recursos adicionales

| Recurso | Descripción | URL |
|---------|-------------|-----|
| ISO 45001 | Sistemas de gestión de seguridad y salud en el trabajo | [iso.org/standard/63787.html](https://www.iso.org/standard/63787.html) |
| OSHA Small Business Handbook | Guía práctica de seguridad y salud ocupacional | [osha.gov/smallbusiness](https://www.osha.gov/smallbusiness) |
| HSE — Gestión del riesgo | Principios y guía para gestión de riesgos | [hse.gov.uk/risk](https://www.hse.gov.uk/risk/) |
| PlainLanguage.gov | Guía de lenguaje claro para documentos técnicos | [plainlanguage.gov/guidelines](https://www.plainlanguage.gov/guidelines/) |
| Microsoft Copilot | Acceso a la herramienta principal del curso | [copilot.microsoft.com](https://copilot.microsoft.com) |

---

> 🏆 **¡Felicitaciones!** Has completado la Práctica 4 y con ella el ciclo completo del curso. Ahora cuentas con las competencias para usar Microsoft Copilot como asistente de productividad real en la generación de documentación profesional operativa, con criterio crítico para validar y mejorar los resultados generados.
