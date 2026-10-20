# Registro de decisiones — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Registro formal de decisiones  
**Versión del documento:** 0.1  
**Estado:** Registro de decisiones de gobierno y gestión de requisitos — reglas confirmadas y decisiones aprobadas  
**Fase:** Gobierno documental e ingeniería de requisitos  
**Fecha de incorporación:** 2026-10-19

---

## 1. Propósito

Este documento constituye el registro formal de las decisiones de gobierno de ControlCore.

Las decisiones aquí registradas provienen de reglas confirmadas o de decisiones aprobadas por el responsable del proyecto. Su incorporación no crea decisiones nuevas ni modifica su contenido. La aprobación de los documentos sustantivos de gobierno se registra en DEC-GOB-009. Las decisiones DEC-GOB-010 a DEC-GOB-015 aprueban la línea base de gestión de requisitos.

## 2. Convenciones y alcance

- **DEC-GOB-###:** identificador de reglas y decisiones de gobierno y de gestión de requisitos, conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 10.1).
- **ADR-###:** identificador de decisiones arquitectónicas y técnicas, conforme al formato completo de `docs/00-gobierno/metodologia-diseno.md` (sección 10.2).
- **Estado:** situación de la regla o decisión en este registro.
  - **Confirmada:** regla previamente confirmada en `docs/00-gobierno/ESTADO-ACTUAL.md`.
  - **Aprobada:** decisión adoptada expresamente por el responsable del proyecto.
- **Referencia de origen:** documento y sección donde la regla o decisión fue confirmada o aprobada.

La fecha de incorporación al registro no se interpreta como fecha de aprobación original de la decisión.

Este registro contiene decisiones de gobierno y de gestión de requisitos, pero no decisiones técnicas, arquitectónicas ni de selección de componentes. Tampoco sustituye los documentos de requisitos, arquitectura o seguridad industrial.

## 3. Resumen de decisiones registradas

| Identificador | Título | Estado |
|---|---|---|
| DEC-GOB-001 | Naturaleza del producto | Confirmada — regla de gobierno vigente |
| DEC-GOB-002 | Ingeniería antes de implementación | Confirmada — regla de gobierno vigente |
| DEC-GOB-003 | Autoridad sobre el diseño | Confirmada — regla de gobierno vigente |
| DEC-GOB-004 | Evaluación de alternativas | Confirmada — regla de gobierno vigente |
| DEC-GOB-005 | Calidad obligatoria | Confirmada — regla de gobierno vigente |
| DEC-GOB-006 | Repositorio como fuente de referencia | Confirmada — regla de gobierno vigente |
| DEC-GOB-007 | Bitácora al cierre de sesión | Confirmada — regla de gobierno vigente |
| DEC-GOB-008 | Independencia de proveedores y herramientas de IA | Aprobada |
| DEC-GOB-009 | Aprobación de la línea base de gobierno documental | Aprobada |
| DEC-GOB-010 | Esquema de identificación de requisitos | Aprobada |
| DEC-GOB-011 | Versionado de requisitos | Aprobada |
| DEC-GOB-012 | Estados operativos de requisitos | Aprobada |
| DEC-GOB-013 | Escala de prioridad de requisitos | Aprobada |
| DEC-GOB-014 | Trazabilidad de requisitos | Aprobada |
| DEC-GOB-015 | Estructura documental de requisitos | Aprobada |

## 4. Decisiones registradas

### DEC-GOB-001 — Naturaleza del producto

- **Contenido:** ControlCore se desarrollará como producto industrial comercial de makeAutomatic, no como una demostración tecnológica aislada.
- **Justificación documentada:** `README.md` (secciones 1 y 4) define ControlCore como un producto industrial comercial y no como una demostración; `docs/00-gobierno/vision-producto.md` (secciones 1 y 12) orienta el desarrollo a la comercialización profesional y establece que el éxito no se limita a demostrar funcionamiento; `AGENTS.md` (sección 1) prohíbe tratarlo como ejercicio académico o demostración.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-001.

### DEC-GOB-002 — Ingeniería antes de implementación

- **Contenido:** La implementación deberá estar precedida por definiciones suficientes de requisitos, arquitectura, interfaces, comportamiento y aceptación.
- **Justificación documentada:** `README.md` (sección 3) establece un proceso estructurado de ingeniería previo a la implementación; `AGENTS.md` (sección 6) exige definiciones suficientes antes de programar; `docs/00-gobierno/principios-ingenieria.md` (sección 3) establece requisitos antes de implementación; `docs/00-gobierno/metodologia-diseno.md` (sección 2) exige ingeniería estructurada antes de construir.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-002.

### DEC-GOB-003 — Autoridad sobre el diseño

- **Contenido:** Las decisiones relevantes deberán ser aprobadas por el responsable del proyecto. Los agentes de IA no podrán aprobar decisiones por iniciativa propia.
- **Justificación documentada:** `README.md` (secciones 5 y 10) atribuye al responsable del proyecto la selección de alternativas y la aprobación de fases; `AGENTS.md` (sección 2) define la autoridad del responsable y prohíbe la aprobación implícita por parte del agente; `docs/00-gobierno/metodologia-diseno.md` (sección 3.1) enumera las responsabilidades del responsable del proyecto.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-003.

### DEC-GOB-004 — Evaluación de alternativas

- **Contenido:** Las decisiones técnicas relevantes seguirán la metodología de análisis de alternativas establecida en `docs/00-gobierno/metodologia-diseno.md`.
- **Justificación documentada:** `README.md` (sección 5) establece rondas estructuradas de decisiones con alternativas A, B y C; `AGENTS.md` (sección 15) exige presentar preferiblemente tres alternativas con ventajas, desventajas y riesgos; `docs/00-gobierno/metodologia-diseno.md` (secciones 4 y 5) desarrolla el método de análisis y la regla de una decisión por interacción.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-004.

### DEC-GOB-005 — Calidad obligatoria

- **Contenido:** La calidad estructural, la seguridad, la confiabilidad y la verificabilidad serán condiciones fundamentales del desarrollo.
- **Justificación documentada:** `AGENTS.md` (secciones 7 y 10) establece criterios de ingeniería industrial y calidad estructural obligatoria; `docs/00-gobierno/principios-ingenieria.md` (sección 10) exige calidad de firmware y software; `docs/00-gobierno/criterios-calidad.md` (secciones 1 y 2) define la calidad como condición del producto y no como resultado de una funcionalidad aparente; `docs/00-gobierno/metodologia-diseno.md` (sección 18) exige calidad de implementación.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-005.

### DEC-GOB-006 — Repositorio como fuente de referencia

- **Contenido:** La continuidad del proyecto deberá basarse en la documentación vigente del repositorio y no exclusivamente en el historial de conversaciones.
- **Justificación documentada:** `README.md` (sección 8) establece el repositorio como fuente documental de referencia; `AGENTS.md` (secciones 3 y 14) obliga a consultar el repositorio y a no depender de recuerdos de conversaciones; `docs/00-gobierno/metodologia-diseno.md` (secciones 19 y 20) define el repositorio como memoria técnica y la bitácora como punto de recuperación.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-006.

### DEC-GOB-007 — Bitácora al cierre de sesión

- **Contenido:** `docs/00-gobierno/ESTADO-ACTUAL.md` se actualizará al finalizar las sesiones de ingeniería, una vez completadas las actividades correspondientes.
- **Justificación documentada:** `AGENTS.md` (sección 14) exige recuperar el estado vigente y preparar un resumen estructurado al cierre de sesión; `docs/00-gobierno/metodologia-diseno.md` (sección 22) define el procedimiento de cierre; `docs/00-gobierno/definicion-de-terminado.md` (sección 27) establece la bitácora como registro de continuidad y cierre.
- **Estado:** Confirmada — regla de gobierno vigente.
- **Referencia de origen:** `docs/00-gobierno/ESTADO-ACTUAL.md`, sección 8, DEC-GOB-007.

### DEC-GOB-008 — Independencia de proveedores y herramientas de IA

- **Contenido:** Las instrucciones, procedimientos y reglas de ingeniería de ControlCore deberán ser independientes de proveedores, modelos y herramientas específicas de inteligencia artificial. Cualquier agente que participe en el proyecto deberá cumplir las mismas obligaciones de consulta del repositorio, respeto por las decisiones aprobadas, trazabilidad, seguridad, calidad y autoridad del responsable del proyecto.
- **Justificación documentada:** `README.md` (sección 7) y `AGENTS.md` (secciones 1 y 4) establecen reglas aplicables a cualquier agente, independientemente de su proveedor, modelo o herramienta; `docs/00-gobierno/metodologia-diseno.md` (secciones 3.2, 17, 19, 21 y 23) aplica la misma independencia a los procedimientos de ingeniería.
- **Estado:** Aprobada.
- **Referencia de origen:** Aprobación expresa del responsable del proyecto durante B1.1 y autorización de formalización durante B1.2.

### DEC-GOB-009 — Aprobación de la línea base de gobierno documental

- **Contenido:** El responsable del proyecto aprobó formalmente los cinco documentos sustantivos de gobierno en versión 0.1.
- **Documentos aprobados:** `docs/00-gobierno/vision-producto.md`, `docs/00-gobierno/principios-ingenieria.md`, `docs/00-gobierno/metodologia-diseno.md`, `docs/00-gobierno/criterios-calidad.md` y `docs/00-gobierno/definicion-de-terminado.md`.
- **Versiones:** 0.1 para los cinco documentos.
- **Fecha:** 2026-10-19.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Justificación documentada:** La auditoría B1, versión 0.2, no identificó hallazgos bloqueantes ni pendientes de H-01 a H-06 y recomendó presentar los cinco documentos para aprobación formal.
- **Fundamento de auditoría:** `docs/00-gobierno/auditoria-gobierno-B1.md`, versión 0.2.
- **Alcance:** Gobierno documental e inicio de la ingeniería de requisitos. No autoriza la implementación de hardware, firmware o software.
- **Condiciones:** Sin condiciones documentales pendientes.
- **Estado:** Aprobada.
- **Referencia de origen:** Aprobación formal del responsable del proyecto durante B1.4.

### DEC-GOB-010 — Esquema de identificación de requisitos

- **Contenido:** Se aprueba el esquema de identificación de requisitos: `RF-###` para requisitos funcionales, `RNF-###` para requisitos no funcionales y `RES-###` para restricciones. Los identificadores son únicos dentro de cada categoría, permanentes y no reutilizables. Las versiones del contenido son independientes de los identificadores.
- **Justificación documentada:** Permite identificar de forma estable y trazable cada requisito, evitar ambigüedades y preservar la trazabilidad cuando cambie su contenido. La metodología aprobada exige un esquema de identificación aprobado al iniciar el bloque de requisitos.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-19.
- **Origen:** Autorización expresa del responsable del proyecto.
- **Referencia:** B2.1.1; `docs/01-requisitos/README.md` (sección 3.1).

### DEC-GOB-011 — Versionado de requisitos

- **Contenido:** Se aprueba el esquema de versionado de requisitos: `0.x` para versiones propuestas no aprobadas; `1.0` para la primera versión aprobada; `1.1`, `1.2`, `1.3` y sucesivas para revisiones posteriores aprobadas. Toda modificación de un requisito aprobado exige evaluación de impacto y nueva aprobación. La conservación del historial es obligatoria. No se utiliza el criterio anterior que diferenciaba versiones mayores y menores según el alcance del cambio.
- **Justificación documentada:** Distingue las propuestas de las versiones aprobadas, asegura que todo cambio aprobado sea evaluado y conserva el historial. La metodología aprobada exige control de cambios y aprobación expresa.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-19.
- **Origen:** Autorización expresa del responsable del proyecto.
- **Referencia:** B2.1.1; `docs/01-requisitos/README.md` (sección 3.2).

### DEC-GOB-012 — Estados operativos de requisitos

- **Contenido:** Se aprueban los estados operativos **En evaluación** y **Retirado**. Se integran con los estados **Propuesto**, **Aprobado**, **Revisión de requisito aprobado**, **Sustituido** y **Rechazado**. Se conservan las reglas de transición, revisión y autoridad establecidas en B2.1. La aprobación no modifica silenciosamente la metodología de gobierno.
- **Justificación documentada:** Permite distinguir la evaluación formal y el retiro de un requisito aprobado sin sustitución, manteniendo la compatibilidad con la metodología aprobada.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-19.
- **Origen:** Autorización expresa del responsable del proyecto.
- **Referencia:** B2.1.1; `docs/01-requisitos/README.md` (sección 5).

### DEC-GOB-013 — Escala de prioridad de requisitos

- **Contenido:** Se aprueba la siguiente escala de prioridad:
  - **Crítica:** indispensable para seguridad, cumplimiento obligatorio o viabilidad esencial del producto.
  - **Alta:** necesaria para cumplir los objetivos principales.
  - **Media:** importante, pero aplazable sin comprometer los objetivos esenciales.
  - **Baja:** complementaria u opcional.

  La prioridad no sustituye la evaluación de riesgos ni la clasificación de seguridad industrial.
- **Justificación documentada:** Proporciona una escala común para ordenar requisitos y apoyar decisiones de alcance, sin reemplazar los análisis de riesgo o seguridad.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-19.
- **Origen:** Autorización expresa del responsable del proyecto.
- **Referencia:** B2.1.1; `docs/01-requisitos/README.md` (sección 3.3).

### DEC-GOB-014 — Trazabilidad de requisitos

- **Contenido:** Se aprueba el siguiente criterio de trazabilidad: las necesidades se referencian mediante documento y sección; los requisitos mediante sus identificadores `RF-###`, `RNF-###` o `RES-###`; las decisiones mediante `DEC-GOB-###` o `ADR-###`; la arquitectura, implementación, pruebas y evidencias mediante identificadores definidos cuando existan sus sistemas documentales. Los estados de vínculo son **Existente**, **Pendiente** y **No aplica**, con justificación cuando corresponda. No se inventan referencias ni artefactos futuros.
- **Justificación documentada:** Permite reconstruir la cadena necesidad-requisito-decisión-arquitectura-implementación-prueba-evidencia sin presuponer artefactos inexistentes.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-19.
- **Origen:** Autorización expresa del responsable del proyecto.
- **Referencia:** B2.1.1; `docs/01-requisitos/README.md` (secciones 3.4 y 7).

### DEC-GOB-015 — Estructura documental de requisitos

- **Contenido:** Se aprueban los siguientes documentos: `docs/01-requisitos/README.md`, `docs/01-requisitos/requisitos-funcionales.md`, `docs/01-requisitos/requisitos-no-funcionales.md` y `docs/01-requisitos/restricciones-sistema.md`. La aprobación comprende estructura, convenciones, atributos y criterios de calidad. No constituye aprobación de requisitos concretos del producto.
- **Justificación documentada:** Establece la línea base documental de gestión de requisitos necesaria para iniciar B2.2 de forma consistente.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-19.
- **Origen:** Autorización expresa del responsable del proyecto.
- **Referencia:** B2.1.1; `docs/01-requisitos/`; `docs/06-decisiones/pendientes.md`.

Las decisiones DEC-GOB-010 a DEC-GOB-015 aprueban la línea base de gestión de requisitos. No forman parte de la línea base de gobierno documental aprobada en DEC-GOB-009 y no aprueban requisitos concretos del producto.

## 5. Estado de los documentos de gobierno

En el momento de la incorporación inicial de este registro, los cinco documentos sustantivos de gobierno se encontraban en estado **Propuesta para aprobación**.

El 2026-10-19, el responsable del proyecto aprobó formalmente los cinco documentos en versión 0.1 mediante DEC-GOB-009. La aprobación quedó registrada conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 24), con versión, fecha y autoridad.

| Documento | Versión | Estado |
|---|---|---|
| `docs/00-gobierno/vision-producto.md` | 0.1 | Aprobado |
| `docs/00-gobierno/principios-ingenieria.md` | 0.1 | Aprobado |
| `docs/00-gobierno/metodologia-diseno.md` | 0.1 | Aprobado |
| `docs/00-gobierno/criterios-calidad.md` | 0.1 | Aprobado |
| `docs/00-gobierno/definicion-de-terminado.md` | 0.1 | Aprobado |

## 6. Identificadores y decisiones futuras

El prefijo **DEC-GOB** queda reservado para reglas y decisiones de gobierno y de gestión de requisitos. El prefijo **ADR** queda reservado para decisiones arquitectónicas futuras.

Las decisiones técnicas y arquitectónicas que se adopten en bloques posteriores deberán registrarse con su propio identificador, su justificación y su estado de aprobación. No deberán incorporarse a este registro como confirmadas sin una decisión expresa del responsable del proyecto.

Los asuntos pendientes se mantienen en `docs/06-decisiones/pendientes.md` y en `docs/00-gobierno/ESTADO-ACTUAL.md`.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
