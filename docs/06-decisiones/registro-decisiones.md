# Registro de decisiones — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Registro formal de decisiones  
**Versión del documento:** 0.1  
**Estado:** Registro de decisiones de gobierno — reglas confirmadas y decisión aprobada  
**Fase:** Gobierno documental  
**Fecha de incorporación:** 2026-10-19

---

## 1. Propósito

Este documento constituye el registro formal de las decisiones de gobierno de ControlCore.

Las decisiones aquí registradas provienen de reglas ya confirmadas en `docs/00-gobierno/ESTADO-ACTUAL.md`. Su incorporación no crea decisiones nuevas, no modifica su contenido y no altera el estado de los documentos sustantivos de gobierno, que permanecen en estado **Propuesta para aprobación** mientras no exista una aprobación expresa del responsable del proyecto.

## 2. Convenciones y alcance

- **DEC-GOB-###:** identificador de reglas y decisiones de gobierno, conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 10.1).
- **ADR-###:** identificador de decisiones arquitectónicas y técnicas, conforme al formato completo de `docs/00-gobierno/metodologia-diseno.md` (sección 10.2).
- **Estado:** situación de la regla o decisión en este registro.
  - **Confirmada:** regla previamente confirmada en `docs/00-gobierno/ESTADO-ACTUAL.md`.
  - **Aprobada:** decisión adoptada expresamente por el responsable del proyecto.
- **Referencia de origen:** documento y sección donde la regla o decisión fue confirmada o aprobada.

La fecha de incorporación al registro no se interpreta como fecha de aprobación original de la decisión.

Este registro no contiene decisiones técnicas, arquitectónicas ni de selección de componentes. Tampoco sustituye los documentos de requisitos, arquitectura o seguridad industrial.

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

## 5. Documentos de gobierno que permanecen como propuestas

El registro de estas reglas y la aprobación de DEC-GOB-008 no implican la aprobación de los documentos sustantivos de gobierno.

A la fecha de incorporación de este registro, los siguientes documentos permanecen en estado **Propuesta para aprobación**:

- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/criterios-calidad.md`
- `docs/00-gobierno/definicion-de-terminado.md`

La aprobación formal deberá registrarse conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 24), con versión, fecha y autoridad.

## 6. Identificadores y decisiones futuras

El prefijo **DEC-GOB** queda reservado para reglas de gobierno. El prefijo **ADR** queda reservado para decisiones arquitectónicas futuras.

Las decisiones técnicas y arquitectónicas que se adopten en bloques posteriores deberán registrarse con su propio identificador, su justificación y su estado de aprobación. No deberán incorporarse a este registro como confirmadas sin una decisión expresa del responsable del proyecto.

Los asuntos pendientes se mantienen en `docs/06-decisiones/pendientes.md` y en `docs/00-gobierno/ESTADO-ACTUAL.md`.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
