# Registro de decisiones — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Registro formal de decisiones  
**Versión del documento:** 0.3  
**Estado:** Registro de decisiones de gobierno, gestión de requisitos, alcance conceptual y comportamiento conceptual — reglas confirmadas y decisiones aprobadas hasta DEC-GOB-030  
**Fase:** Gobierno documental e ingeniería conceptual  
**Fecha de incorporación:** 2026-10-19  
**Fecha de actualización:** 2026-10-20

---

## 1. Propósito

Este documento constituye el registro formal de las decisiones de gobierno, de gestión de requisitos, de alcance conceptual y de comportamiento conceptual del producto de ControlCore.

Las decisiones aquí registradas provienen de reglas confirmadas o de decisiones aprobadas por el responsable del proyecto. Su incorporación no crea decisiones nuevas ni modifica su contenido. La aprobación de los documentos sustantivos de gobierno se registra en DEC-GOB-009. Las decisiones DEC-GOB-010 a DEC-GOB-015 aprueban la línea base de gestión de requisitos. DEC-GOB-016 aprueba las necesidades, actores y escenarios del producto. DEC-GOB-017 a DEC-GOB-021 formalizan las respuestas a las preguntas `PREG-P-01` a `PREG-P-15`. DEC-GOB-022 a DEC-GOB-030 consolidan las decisiones conceptuales `D01` a `D63` adoptadas en B2.3, conservando su identificador de origen y sin convertirlas en requisitos, arquitectura o autorización de implementación.

## 2. Convenciones y alcance

- **DEC-GOB-###:** identificador de reglas y decisiones de gobierno, de gestión de requisitos, de alcance conceptual y de comportamiento conceptual del producto, conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 10.1).
- **ADR-###:** identificador de decisiones arquitectónicas y técnicas, conforme al formato completo de `docs/00-gobierno/metodologia-diseno.md` (sección 10.2).
- **Estado:** situación de la regla o decisión en este registro.
  - **Confirmada:** regla previamente confirmada en `docs/00-gobierno/ESTADO-ACTUAL.md`.
  - **Aprobada:** decisión adoptada expresamente por el responsable del proyecto.
  - **Aprobada — alcance conceptual:** decisión adoptada expresamente, limitada a alcance o comportamiento conceptual; no aprueba arquitectura, requisitos concretos ni implementación.
- **Referencia de origen:** documento y sección donde la regla o decisión fue confirmada o aprobada.

La fecha de incorporación al registro no se interpreta como fecha de aprobación original de la decisión.

Este registro contiene decisiones de gobierno, gestión de requisitos, alcance conceptual y comportamiento conceptual del producto. No contiene arquitectura aprobada, selección de componentes, protocolos, lenguajes, herramientas ni tecnologías de implementación. Tampoco sustituye los documentos de requisitos, arquitectura o seguridad industrial.

Las decisiones DEC-GOB-016 a DEC-GOB-021 formalizan aprobaciones y alcances conceptuales del producto; DEC-GOB-022 a DEC-GOB-030 consolidan el alcance y el comportamiento conceptual de B2.3. Se registran en la familia DEC-GOB por autorización expresa del responsable del proyecto. No seleccionan arquitecturas, tecnologías ni componentes concretos y no sustituyen los futuros registros ADR.

Las decisiones DEC-GOB-016 a DEC-GOB-021 conservan su contenido y su estado; B2.3 no las modifica.

Las decisiones DEC-GOB-022 a DEC-GOB-030 se registran con fecha de formalización 2026-10-20. La sesión de B2.3 no consignó una fecha de adopción distinta. Esa fecha de formalización no se interpreta como aprobación de arquitectura, requisitos concretos o implementación.

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
| DEC-GOB-016 | Aprobación de necesidades, actores y escenarios | Aprobada |
| DEC-GOB-017 | Seguridad industrial, responsabilidades y normativa | Aprobada |
| DEC-GOB-018 | Aplicación objetivo, motores y entorno | Aprobada |
| DEC-GOB-019 | Capacidades y exclusiones de la primera versión | Aprobada |
| DEC-GOB-020 | Integración, perfiles funcionales y registro de información | Aprobada |
| DEC-GOB-021 | Aceptación, validación y documentación | Aprobada |
| DEC-GOB-022 | Alcance, evolución y primer incremento | Aprobada — alcance conceptual |
| DEC-GOB-023 | Control de movimiento y adquisición | Aprobada — alcance conceptual |
| DEC-GOB-024 | Supervisión, fallas, alarmas y recuperación | Aprobada — alcance conceptual |
| DEC-GOB-025 | Operación, mando y estados | Aprobada — alcance conceptual |
| DEC-GOB-026 | Configuración, persistencia, registros y acceso | Aprobada — alcance conceptual |
| DEC-GOB-027 | Diagnóstico, mantenimiento y actualización de firmware | Aprobada — alcance conceptual |
| DEC-GOB-028 | Interfaces, modularidad y simulación | Aprobada — alcance conceptual |
| DEC-GOB-029 | Verificación, evidencia y cierre de incrementos | Aprobada — alcance conceptual |
| DEC-GOB-030 | Cierre de las decisiones conceptuales | Aprobada |

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

### DEC-GOB-016 — Aprobación de necesidades, actores y escenarios

- **Asunto:** Aprobación de las necesidades del producto, los actores y los escenarios de uso identificados en B2.2.1.
- **Contenido aprobado:**
  - Se aprueban las diez necesidades `NEC-P-01` a `NEC-P-10`.
  - Se aprueban los siete actores `ACT-P-01` a `ACT-P-07` y sus responsabilidades generales.
  - Se aprueban los diez escenarios `ESC-P-01` a `ESC-P-10` como base conceptual de ingeniería.
  - La aprobación de necesidades no las convierte en requisitos implementables ni obliga a incluir todas las capacidades en la primera versión.
  - La aprobación de actores no define autenticación ni una matriz detallada de permisos. Los actores organizacionales se distinguen de los perfiles funcionales de acceso de DEC-GOB-020.
  - La aprobación de escenarios no aprueba todos sus detalles, interfaces, protocolos, tiempos, algoritmos ni comportamientos de seguridad.
  - Documentos aprobados: `docs/01-requisitos/necesidades-producto.md`, `docs/01-requisitos/actores-uso.md` y `docs/01-requisitos/escenarios-uso.md`, versión 0.2.
- **Justificación documentada:** Las necesidades, actores y escenarios fueron revisados individualmente por el responsable del proyecto y constituyen la base conceptual para derivar requisitos verificables. La aprobación preserva la distinción entre necesidades, hipótesis y requisitos.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Revisión individual en conversación con el responsable del proyecto; formalización en B2.2.2.
- **Referencias:** `docs/01-requisitos/necesidades-producto.md`; `docs/01-requisitos/actores-uso.md`; `docs/01-requisitos/escenarios-uso.md`; DEC-GOB-017 a DEC-GOB-021.
- **Condiciones y límites:** No aprueba requisitos `RF-###`, `RNF-###` o `RES-###`; no aprueba arquitectura, tecnologías, protocolos, prestaciones cuantitativas ni funciones de seguridad certificadas.

### DEC-GOB-017 — Seguridad industrial, responsabilidades y normativa

- **Asunto:** Funciones y responsabilidades de seguridad, proceso de evaluación de riesgos, normativa aplicable y estados seguros.
- **Contenido aprobado:**
  - ControlCore será responsable de las funciones de control y diagnóstico expresamente especificadas y validadas.
  - ControlCore no sustituirá automáticamente los sistemas de protección de las máquinas.
  - Las responsabilidades de makeAutomatic, los fabricantes de máquinas y los integradores deberán delimitarse documentalmente.
  - Se adoptará un proceso documentado de identificación de peligros, evaluación y reducción de riesgos.
  - Las normas aplicables se determinarán según las funciones, aplicaciones y mercados previstos. Se considerarán ISO 12100, IEC 60204-1, ISO 13849-1 e IEC 62061 cuando corresponda.
  - No se declarará conformidad ni certificación sin evidencias.
  - Los estados seguros dependerán del análisis de riesgos de cada aplicación. Deberán definirse las condiciones de transición, responsabilidades, recuperación y reinicio.
  - No se asumirá que detener un motor o cortar su alimentación constituye siempre una condición segura.
- **Justificación documentada:** El control de motores y actuadores puede producir movimiento y condiciones peligrosas. La delimitación de responsabilidades y el análisis de riesgos son condiciones previas para especificar funciones de seguridad y para evitar declaraciones de conformidad sin evidencia.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Respuestas a `PREG-P-01`, `PREG-P-02` y `PREG-P-03`, revisadas individualmente y formalizadas en B2.2.2.
- **Referencias:** `PREG-P-01`, `PREG-P-02`, `PREG-P-03`; `NEC-P-07`, `NEC-P-08`; `ESC-P-06`, `ESC-P-09`; `docs/03-seguridad-industrial/` (pendiente de desarrollo).
- **Condiciones y límites:** No define la arquitectura de seguridad, las funciones de seguridad concretas, los niveles de integridad o desempeño, los estados seguros de una aplicación específica ni la aplicabilidad definitiva de cada norma. No constituye certificación ni declaración de conformidad.

### DEC-GOB-018 — Aplicación objetivo, motores y entorno

- **Asunto:** Aplicación industrial objetivo, familias de motores y actuadores, y entorno de operación.
- **Contenido aprobado:**
  - ControlCore será una plataforma modular y genérica de control industrial, independiente de una máquina, fabricante o proceso específico.
  - El objetivo es la extensibilidad hacia motores DC, motores paso a paso, servomotores, motores AC y otros actuadores.
  - La extensibilidad no implica implementar ni validar todas las familias en la primera versión. El soporte inicial concreto permanece pendiente de definición.
  - El entorno objetivo es industrial real. El laboratorio podrá utilizarse para desarrollo y validación, pero las pruebas de laboratorio no bastarán por sí solas para autorizar el uso industrial.
  - Las condiciones cuantitativas y las normas aplicables se determinarán posteriormente.
- **Justificación documentada:** Define el contexto de aplicación sin seleccionar una máquina, una familia de motores ni una tecnología concreta, y evita confundir validación de laboratorio con aptitud industrial.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Respuestas a `PREG-P-04`, `PREG-P-05` y `PREG-P-06`, revisadas individualmente y formalizadas en B2.2.2.
- **Referencias:** `PREG-P-04`, `PREG-P-05`, `PREG-P-06`; `NEC-P-01`, `NEC-P-06`, `NEC-P-07`, `NEC-P-09`; `ESC-P-01`, `ESC-P-03`.
- **Condiciones y límites:** No selecciona la familia de motores o actuadores del primer incremento, las condiciones eléctricas, ambientales o de instalación cuantitativas, ni las normas aplicables.

### DEC-GOB-019 — Capacidades y exclusiones de la primera versión

- **Asunto:** Capacidades funcionales objetivo, exclusiones de la primera versión y nivel funcional inicial.
- **Contenido aprobado:**
  - Capacidades objetivo: control de motores y actuadores; supervisión; diagnóstico; configuración; integración externa; registro de eventos y datos.
  - El desarrollo será incremental, sin obligación de implementar todas las capacidades simultáneamente.
  - Se excluyen de la primera versión:
    - Soporte simultáneo de todas las familias de motores.
    - Control coordinado de múltiples ejes.
    - Algoritmos avanzados de optimización.
    - Integración con múltiples protocolos industriales.
    - Funciones de seguridad certificadas, mientras no exista el proceso de análisis y evaluación de conformidad correspondiente.
  - Las exclusiones no eliminan la obligación de evaluar y tratar los riesgos aplicables.
  - Nivel funcional inicial:
    - Configuración: establecer y consultar parámetros operativos.
    - Supervisión: consultar estados, variables y condiciones anormales.
    - Diagnóstico: identificar fallas detectables y facilitar su investigación.
  - Las interfaces, los algoritmos y las prestaciones permanecen pendientes.
- **Justificación documentada:** Delimita el alcance funcional inicial y evita implementar capacidades no autorizadas o declarar funciones de seguridad sin el proceso de conformidad correspondiente.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Respuestas a `PREG-P-07`, `PREG-P-08` y `PREG-P-09`, revisadas individualmente y formalizadas en B2.2.2.
- **Referencias:** `PREG-P-07`, `PREG-P-08`, `PREG-P-09`; `NEC-P-01` a `NEC-P-10`; `ESC-P-02`, `ESC-P-04`, `ESC-P-05`.
- **Condiciones y límites:** No define el alcance exacto del primer incremento implementable, las interfaces, los algoritmos ni las prestaciones cuantitativas. Las exclusiones no eliminan la evaluación de riesgos.

### DEC-GOB-020 — Integración, perfiles funcionales y registro de información

- **Asunto:** Integración con sistemas externos, perfiles funcionales de acceso y registro de información.
- **Contenido aprobado:**
  - Se utilizarán interfaces documentadas y una arquitectura independiente de protocolos específicos.
  - La integración con PLC, HMI, SCADA y otros sistemas industriales será progresiva. No implica compatibilidad inmediata con todos ellos.
  - Se aprueban tres perfiles funcionales de acceso:
    - Operador.
    - Técnico/Integrador.
    - Administrador técnico.
  - Los perfiles tendrán responsabilidades diferenciadas.
  - No se selecciona todavía el mecanismo de autenticación ni una matriz detallada de permisos.
  - Los controles de acceso no sustituyen las protecciones industriales.
  - Se registrará la siguiente información:
    - Eventos operativos.
    - Fallas y alarmas.
    - Cambios de configuración.
    - Información de diagnóstico.
  - Se utilizarán referencias temporales apropiadas. La retención, el almacenamiento y los mecanismos técnicos permanecen pendientes.
- **Justificación documentada:** Define el marco de integración y de acceso sin seleccionar protocolos, tecnologías de autenticación ni mecanismos de almacenamiento, y establece la información mínima que deberá poder registrarse.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Respuestas a `PREG-P-10`, `PREG-P-11` y `PREG-P-12`, revisadas individualmente y formalizadas en B2.2.2.
- **Referencias:** `PREG-P-10`, `PREG-P-11`, `PREG-P-12`; `NEC-P-02`, `NEC-P-03`, `NEC-P-06`, `NEC-P-09`; `ACT-P-01` a `ACT-P-07`; `ESC-P-04`, `ESC-P-05`, `ESC-P-08`.
- **Condiciones y límites:** Los perfiles funcionales son distintos de los actores organizacionales `ACT-P-01` a `ACT-P-07`; su asignación concreta y los permisos están pendientes. No selecciona protocolos, interfaces concretas, autenticación, retención ni almacenamiento.

### DEC-GOB-021 — Aceptación, validación y documentación

- **Asunto:** Criterios de aceptación, niveles de validación y documentación exigible.
- **Contenido aprobado:**
  - Se exigirán criterios objetivos, medibles y verificables para:
    - Funcionamiento.
    - Prestaciones.
    - Comportamiento ante fallas.
    - Reproducibilidad de pruebas.
    - Evidencia documental.
    - Evaluación de riesgos.
  - Los valores cuantitativos y los procedimientos específicos permanecen pendientes.
  - Se distinguen dos niveles de validación:
    - Banco de pruebas de ingeniería.
    - Validación en entorno industrial real.
  - La validación de laboratorio no sustituye la evaluación necesaria para autorizar el uso industrial.
  - Se entregarán cinco conjuntos de documentación:
    - Documentación técnica.
    - Instalación y puesta en servicio.
    - Operación.
    - Mantenimiento y diagnóstico.
    - Validación y conformidad.
  - La documentación será versionada y coherente con las capacidades realmente implementadas y validadas.
- **Justificación documentada:** Establece las condiciones de aceptación y la documentación mínima sin fijar valores, procedimientos ni formatos no definidos, y evita que la validación de laboratorio se presente como autorización industrial.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Respuestas a `PREG-P-13`, `PREG-P-14` y `PREG-P-15`, revisadas individualmente y formalizadas en B2.2.2.
- **Referencias:** `PREG-P-13`, `PREG-P-14`, `PREG-P-15`; `NEC-P-09`, `NEC-P-10`; todos los escenarios; `docs/05-validacion/` (pendiente de desarrollo).
- **Condiciones y límites:** No define los criterios cuantitativos, los procedimientos de prueba, el banco o máquina de referencia, los formatos documentales ni la aceptación de una aplicación industrial concreta.

Las decisiones DEC-GOB-016 a DEC-GOB-021 formalizan aprobaciones conceptuales. No constituyen requisitos concretos, arquitectura aprobada, selección tecnológica, certificación industrial ni autorización de implementación.

### DEC-GOB-022 — Alcance, evolución y primer incremento

- **Asunto:** Familia inicial de motores, extensibilidad, estrategia incremental y alcance funcional del primer incremento.
- **Contenido aprobado:**
  - **D01 —** La primera familia de motores es la de motores DC con escobillas.
  - **D04 —** La solución deberá ser extensible a varios motores; la implementación inicial considerará un solo motor.
  - **D12 —** La validación se realizará primero en laboratorio y posteriormente mediante un piloto industrial.
  - **D13 —** La implementación será incremental.
  - **D24 —** Se mantendrá el alcance objetivo de la primera versión, distribuido en incrementos verificables.
  - **D25 —** El primer incremento comprenderá un motor DC, arranque y parada, control por PWM, regulación de velocidad, inversión de giro, medición de velocidad y control en lazo abierto y cerrado.
- **Justificación documentada:** Delimita el primer alcance implementable y la estrategia de evolución sin seleccionar hardware, electrónica de potencia, sensores ni prestaciones cuantitativas. Es coherente con `DEC-GOB-018` y `DEC-GOB-019`, que aprobaron la extensibilidad y el desarrollo incremental, y resuelve conceptualmente la familia inicial que `DEC-GOB-018` había dejado pendiente.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D01`, `D04`, `D12`, `D13`, `D24` y `D25` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D01`, `D04`, `D12`, `D13`, `D24`, `D25`; `DEC-GOB-018`, `DEC-GOB-019`, `DEC-GOB-021`; `NEC-P-01`, `NEC-P-04`, `NEC-P-07`; `ESC-P-02`, `ESC-P-03`.
- **Condiciones y límites:** No selecciona modelo de motor, tensión, corriente, potencia, electrónica de potencia, sensor de velocidad, plataforma de control ni parámetros cuantitativos. No define medidas de protección ni estados seguros. La validación en laboratorio y el piloto industrial no autorizan por sí solos el uso industrial. No autoriza la implementación.

### DEC-GOB-023 — Control de movimiento y adquisición

- **Asunto:** Funciones de control, regulación de velocidad, adquisición y ajuste del controlador.
- **Contenido aprobado:**
  - **D02 —** El alcance comprende arranque, parada, PWM, inversión de giro y transiciones controladas.
  - **D03 —** El control podrá operar en lazo abierto y en lazo cerrado.
  - **D05 —** Se supervisarán velocidad, dirección, tensión, corriente, temperatura y anomalías.
  - **D26 —** La estructura de algoritmos será extensible; el primer algoritmo implementado será PI.
  - **D27 —** La salida del PI incorporará limitación y anti-windup.
  - **D28 —** La interfaz de adquisición será compatible con distintos sensores de velocidad.
  - **D29 —** El filtrado de la velocidad medida será configurable.
  - **D31 —** Las rampas de aceleración y desaceleración serán configurables.
  - **D32 —** La inversión de giro será configurable y estará condicionada por la evaluación de riesgos.
  - **D33 —** Los límites de velocidad serán configurables, validados y sujetos a permisos.
  - **D34 —** La transición entre lazo abierto y lazo cerrado será supervisada.
  - **D35 —** El ajuste del PI podrá ser manual y asistido, con validación.
- **Justificación documentada:** Define el comportamiento conceptual de control y adquisición necesario para el primer incremento y para la evolución del producto, sin fijar algoritmos concretos, parámetros ni tecnología. Se apoya en `D25` y en las capacidades aprobadas en `DEC-GOB-019`.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D02`, `D03`, `D05`, `D26`, `D27`, `D28`, `D29`, `D31`, `D32`, `D33`, `D34` y `D35` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D02`, `D03`, `D05`, `D26`, `D27`, `D28`, `D29`, `D31`, `D32`, `D33`, `D34`, `D35`; `DEC-GOB-019`; `DEC-GOB-022`; `NEC-P-01`, `NEC-P-02`; `ESC-P-03`, `ESC-P-04`.
- **Condiciones y límites:** No selecciona tipo de sensor, frecuencia de PWM, frecuencia de muestreo, ganancias, rangos de filtro o de rampa, límites de velocidad, procedimiento de ajuste ni criterios cuantitativos. Las respuestas y transiciones condicionadas por riesgos o permisos permanecen sujetas a las decisiones y análisis correspondientes. No autoriza la implementación.

### DEC-GOB-024 — Supervisión, fallas, alarmas y recuperación

- **Asunto:** Detección de fallas, alarmas, respuestas diferenciadas, supervisión temporal y recuperación.
- **Contenido aprobado:**
  - **D06 —** Se detectarán fallas, se generarán alarmas y se registrarán eventos. El diagnóstico causal automatizado no forma parte del alcance inicial.
  - **D07 —** Las respuestas ante fallas serán diferenciadas según los riesgos identificados.
  - **D11 —** La recuperación después de interrupciones será configurable y estará condicionada por los riesgos.
  - **D17 —** La respuesta ante pérdida de comunicaciones será configurable y estará condicionada por los riesgos.
  - **D30 —** La respuesta ante pérdida de realimentación estará condicionada por los riesgos.
  - **D38 —** Se dispondrá de watchdog, detección de fallas internas y recuperación condicionada por los riesgos.
  - **D46 —** La gestión de errores de comunicación será configurable.
  - **D47 —** La ejecución será determinista, con prioridades y supervisión temporal.
  - **D48 —** Los incumplimientos temporales se tratarán según su criticidad y los riesgos.
  - **D51 —** La recuperación tras pérdida de alimentación será supervisada.
  - **D54 —** Se realizará un autodiagnóstico supervisado antes de habilitar el motor.
  - **D55 —** Los comandos serán validados integralmente.
  - **D56 —** Las alarmas se clasificarán por severidad, con reconocimiento y condiciones de restablecimiento.
  - **D57 —** Se conservará un historial auditable de alarmas.
- **Justificación documentada:** Establece el tratamiento conceptual de condiciones anormales y recuperación, preservando la dependencia del análisis de riesgos y evitando declarar funciones de seguridad o estados seguros no aprobados. Es coherente con `DEC-GOB-017`, `DEC-GOB-019` y `DEC-GOB-021`.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D06`, `D07`, `D11`, `D17`, `D30`, `D38`, `D46`, `D47`, `D48`, `D51`, `D54`, `D55`, `D56` y `D57` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D06`, `D07`, `D11`, `D17`, `D30`, `D38`, `D46`, `D47`, `D48`, `D51`, `D54`, `D55`, `D56`, `D57`; `DEC-GOB-017`, `DEC-GOB-019`, `DEC-GOB-021`; `NEC-P-03`, `NEC-P-07`, `NEC-P-08`; `ESC-P-06`, `ESC-P-09`.
- **Condiciones y límites:** No define estados seguros, umbrales, tiempos de reacción, prioridades de parada, niveles de integridad o desempeño, algoritmos de diagnóstico, cobertura diagnóstica ni procedimientos de recuperación. No se asume que detener el motor o cortar su alimentación sea siempre seguro. Las respuestas condicionadas por riesgos permanecen abiertas hasta el análisis correspondiente. No autoriza la implementación.

### DEC-GOB-025 — Operación, mando y estados

- **Asunto:** Controles locales, interfaz desde computador, operación autónoma, supervisión remota, arranque y arbitraje de comandos.
- **Contenido aprobado:**
  - **D08 —** Se dispondrá de controles físicos locales y de una interfaz desde computador.
  - **D18 —** Se contempla operación autónoma y supervisión remota, con arbitraje de comandos.
  - **D37 —** El arranque será supervisado.
  - **D49 —** El comportamiento se organizará mediante una máquina de estados supervisada.
  - **D50 —** Los comandos serán arbitrados de forma supervisada.
- **Justificación documentada:** Define el marco conceptual de operación y mando sin seleccionar interfaces, tecnologías ni políticas de prioridad. Se relaciona con los perfiles funcionales de `DEC-GOB-020` y con el tratamiento de fallas de `DEC-GOB-024`.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D08`, `D18`, `D37`, `D49` y `D50` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D08`, `D18`, `D37`, `D49`, `D50`; `DEC-GOB-020`, `DEC-GOB-024`; `NEC-P-02`, `NEC-P-07`; `ESC-P-03`, `ESC-P-04`, `ESC-P-09`.
- **Condiciones y límites:** No define tipos de controles locales, interfaz de computador, protocolos, prioridades de mando, política de arbitraje, estados, transiciones ni funciones de seguridad. No autoriza la implementación.

### DEC-GOB-026 — Configuración, persistencia, registros y acceso

- **Asunto:** Configuración validada, persistencia de parámetros, eventos y registros, tiempo, retención, integridad, auditoría, acceso y exportación.
- **Contenido aprobado:**
  - **D09 —** Se conservarán eventos y variables operativas.
  - **D14 —** La configuración avanzada de parámetros será validada.
  - **D15 —** Se dispondrá de perfiles de operador, técnico/integrador y administrador, con autenticación y auditoría.
  - **D36 —** Los parámetros se conservarán con integridad y recuperación.
  - **D39 —** Los registros diagnósticos incluirán contexto e historial.
  - **D40 —** Se dispondrá de reloj interno, con sincronización externa opcional y detección de cambios horarios.
  - **D41 —** La retención será configurable y se gestionará el almacenamiento lleno.
  - **D42 —** Los registros contarán con integridad, auditoría y control de acceso.
  - **D43 —** La exportación será manual y automática, mediante formatos documentados.
- **Justificación documentada:** Define la información y las condiciones de acceso que deben conservarse para operación, diagnóstico y auditoría, sin seleccionar mecanismos técnicos. Es coherente con `DEC-GOB-020` y `DEC-GOB-021`.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D09`, `D14`, `D15`, `D36`, `D39`, `D40`, `D41`, `D42` y `D43` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D09`, `D14`, `D15`, `D36`, `D39`, `D40`, `D41`, `D42`, `D43`; `DEC-GOB-020`, `DEC-GOB-021`; `NEC-P-03`, `NEC-P-05`, `NEC-P-09`; `ESC-P-05`, `ESC-P-07`, `ESC-P-10`.
- **Condiciones y límites:** No selecciona mecanismo de autenticación, matriz de permisos, períodos de retención, tecnología de almacenamiento, formatos de registro o exportación, fuente de reloj ni protocolo de sincronización. Los controles de acceso no sustituyen las protecciones industriales. No autoriza la implementación.

### DEC-GOB-027 — Diagnóstico, mantenimiento y actualización de firmware

- **Asunto:** Diagnóstico, mantenimiento, actualización verificable y recuperación del firmware.
- **Contenido aprobado:**
  - **D16 —** Se contemplan diagnóstico, mantenimiento y actualizaciones controladas y recuperables.
  - **D52 —** La actualización del firmware será verificable y recuperable.
  - **D53 —** Se dispondrá de diagnóstico integral del firmware.
- **Justificación documentada:** Define las condiciones conceptuales de mantenibilidad y actualización sin seleccionar mecanismos ni tecnologías. Se relaciona con la detección de fallas de `DEC-GOB-024` y con la documentación de `DEC-GOB-021`.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D16`, `D52` y `D53` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D16`, `D52`, `D53`; `DEC-GOB-020`, `DEC-GOB-021`, `DEC-GOB-024`; `NEC-P-05`, `NEC-P-10`; `ESC-P-07`, `ESC-P-10`.
- **Condiciones y límites:** No define transporte de actualización, gestor de arranque, firma, verificación criptográfica, mecanismo de reversión, cobertura diagnóstica ni procedimientos de mantenimiento. El diagnóstico causal automatizado continúa excluido del alcance inicial conforme a `D06`. No autoriza la implementación.

### DEC-GOB-028 — Interfaces, modularidad y simulación

- **Asunto:** Interfaces externas, separación entre control y potencia, modularidad, simulación y versionado de interfaces.
- **Contenido aprobado:**
  - **D10 —** Las interfaces externas estarán documentadas; la integración industrial funcional no será obligatoria inicialmente.
  - **D19 —** Se separarán la lógica de control y la electrónica de potencia; los parámetros eléctricos quedan por definir.
  - **D20 —** Se podrá simular el motor, las variables físicas, las anomalías y las interfaces.
  - **D21 —** El simulador será independiente y dispondrá de interfaces equivalentes a las del hardware físico.
  - **D44 —** Las interfaces serán desacopladas, documentadas y verificables.
  - **D45 —** Las interfaces dispondrán de versionado y compatibilidad.
- **Justificación documentada:** Establece principios conceptuales de modularidad, simulación y evolución de interfaces sin aprobar una arquitectura ni seleccionar protocolos. Se relaciona con `DEC-GOB-020` y con la estrategia de verificación de `DEC-GOB-029`.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D10`, `D19`, `D20`, `D21`, `D44` y `D45` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D10`, `D19`, `D20`, `D21`, `D44`, `D45`; `DEC-GOB-017`, `DEC-GOB-019`, `DEC-GOB-020`; `NEC-P-04`, `NEC-P-06`, `NEC-P-10`; `ESC-P-01`, `ESC-P-02`, `ESC-P-08`.
- **Condiciones y límites:** No aprueba arquitectura de hardware, firmware o software, ni protocolos, capas físicas, formatos de datos, tecnología de simulación o criterios de equivalencia. La separación de `D19` es conceptual y no define aislamiento, protecciones ni parámetros eléctricos. No autoriza la implementación.

### DEC-GOB-029 — Verificación, evidencia y cierre de incrementos

- **Asunto:** Pruebas, validación, cobertura, trazabilidad de evidencias y gestión de cambios.
- **Contenido aprobado:**
  - **D22 —** Se realizarán pruebas unitarias, de integración y de sistema, incluyendo simulación de fallas.
  - **D23 —** El cierre de cada incremento requerirá implementación, documentación, trazabilidad, riesgos, pruebas, evidencias y aprobación.
  - **D58 —** Se realizarán pruebas automatizadas en simulación y pruebas físicas controladas.
  - **D59 —** La validación será automática, con evidencias trazables y revisión de anomalías.
  - **D60 —** La cobertura de pruebas se basará en requisitos y riesgos.
  - **D61 —** Se mantendrá trazabilidad entre requisitos, riesgos, pruebas, resultados y evidencias.
  - **D62 —** La gestión de cambios incluirá análisis de impacto, riesgos y regresión.
- **Justificación documentada:** Define el marco conceptual de verificación y cierre sin fijar herramientas, procedimientos ni umbrales. Es coherente con `DEC-GOB-021` y con la metodología de definición de terminado.
- **Estado:** Aprobada — alcance conceptual.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisiones `D22`, `D23`, `D58`, `D59`, `D60`, `D61` y `D62` adoptadas en la sesión de B2.3 y formalizadas en este bloque.
- **Referencias:** `D22`, `D23`, `D58`, `D59`, `D60`, `D61`, `D62`; `DEC-GOB-021`; `NEC-P-09`, `NEC-P-10`; todos los escenarios aprobados en `DEC-GOB-016`.
- **Condiciones y límites:** No define herramientas, umbrales de cobertura, procedimientos de prueba, valores de aceptación, banco o máquina de referencia, formatos de evidencia ni criterios de aprobación de una aplicación industrial concreta. La aprobación de cierre de cada incremento corresponde al responsable del proyecto. No autoriza la implementación.

### DEC-GOB-030 — Cierre de las decisiones conceptuales

- **Asunto:** Cierre de la fase de decisiones conceptuales, revisión de coherencia y preparación de la formalización documental.
- **Contenido aprobado:**
  - **D63 —** Se cierran las decisiones conceptuales, se revisan su coherencia y redundancias y se prepara su formalización documental.
- **Justificación documentada:** La consolidación permite preservar la trazabilidad de las 63 decisiones, evitar duplicaciones y establecer una base documental revisable antes de derivar requisitos concretos. No crea decisiones técnicas nuevas.
- **Estado:** Aprobada.
- **Fecha de aprobación:** 2026-10-20 — fecha de formalización.
- **Autoridad:** Responsable del proyecto ControlCore — makeAutomatic.
- **Origen:** Decisión `D63` adoptada en la sesión de B2.3; formalización documental en este bloque.
- **Referencias:** `D01` a `D63`; `DEC-GOB-022` a `DEC-GOB-029`; `docs/06-decisiones/consolidacion-decisiones-B2.3.md`.
- **Condiciones y límites:** El cierre es documental y conceptual. No aprueba arquitectura, requisitos concretos, tecnologías, protocolos ni implementación. No resuelve las cuestiones técnicas que permanecen abiertas. La formalización documental queda sujeta a revisión y aprobación del responsable del proyecto.

Las decisiones DEC-GOB-022 a DEC-GOB-030 consolidan decisiones conceptuales. No constituyen requisitos concretos, arquitectura aprobada, selección tecnológica, certificación industrial ni autorización de implementación. Su matriz completa de correspondencia con `D01` a `D63` se encuentra en `docs/06-decisiones/consolidacion-decisiones-B2.3.md`.

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

El prefijo **DEC-GOB** queda reservado para reglas y decisiones de gobierno, de gestión de requisitos, de alcance conceptual y de comportamiento conceptual del producto aprobadas por el responsable del proyecto. El prefijo **ADR** queda reservado para decisiones arquitectónicas y técnicas futuras.

Las decisiones DEC-GOB-022 a DEC-GOB-030 no son ADR: describen alcance y comportamiento conceptual, no una arquitectura seleccionada, un componente, un protocolo ni una tecnología de implementación. Las decisiones arquitectónicas y técnicas que se adopten en bloques posteriores deberán registrarse con su propio identificador, su justificación y su estado de aprobación. No deberán incorporarse a este registro como confirmadas sin una decisión expresa del responsable del proyecto.

Los asuntos pendientes se mantienen en `docs/06-decisiones/pendientes.md` y en `docs/00-gobierno/ESTADO-ACTUAL.md`.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
