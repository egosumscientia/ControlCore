# Asuntos de decisión — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Registro de asuntos de decisión  
**Versión:** 0.2  
**Estado:** Registro de asuntos de decisión — B2.1 y B2.2.1 resueltos; preguntas técnicas derivadas pendientes  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-20  
**Aprobación:** No aplica — registro de asuntos de decisión

---

## 1. Propósito

Este documento registra los asuntos que requirieron una decisión del responsable del proyecto durante B2.1 y B2.2.1, sus resoluciones en B2.1.1 y B2.2.2, y las preguntas técnicas que permanecen abiertas.

Conserva las alternativas consideradas y la trazabilidad hacia el registro formal de decisiones.

## 2. Alcance

Este registro comprende los asuntos identificados durante B2.1 — Estructura, identificación y trazabilidad de requisitos, sus resoluciones en B2.1.1; las preguntas de B2.2.1 — Identificación de necesidades, actores y escenarios de uso, y sus resoluciones conceptuales en B2.2.2.

No contiene requisitos del producto. Las decisiones aprobadas se registran en `docs/06-decisiones/registro-decisiones.md`.

## 3. Asuntos de B2.1 — resueltos

| Asunto | Decisión | Estado |
|---|---|---|
| Esquema de identificación de requisitos | DEC-GOB-010 | Resuelto |
| Versionado de requisitos | DEC-GOB-011 | Resuelto |
| Estados operativos | DEC-GOB-012 | Resuelto |
| Escala de prioridad | DEC-GOB-013 | Resuelto |
| Trazabilidad de requisitos | DEC-GOB-014 | Resuelto |
| Estructura documental de requisitos | DEC-GOB-015 | Resuelto |

### 3.1. Esquema de identificación de requisitos

- **Necesidad:** la metodología aprobada establece que el esquema definitivo de identificación de requisitos se aprobará al iniciar el bloque de requisitos.
- **Propuesta:** prefijos `RF-###` para requisitos funcionales, `RNF-###` para requisitos no funcionales y `RES-###` para restricciones.
- **Alternativas consideradas:**
  - **A. Prefijos por tipo (recomendada):** `RF-###`, `RNF-###`, `RES-###`.
  - **B. Identificador único con atributo de tipo:** `REQ-###` más un campo `Tipo`.
  - **C. Prefijos adicionales por dominio:** por ejemplo, prefijos específicos para seguridad, comunicaciones o control.
- **Resolución:** Aprobado el esquema `RF-###`, `RNF-###`, `RES-###`, con identificadores únicos por categoría, permanentes y no reutilizables, y versiones independientes.
- **Estado:** Resuelto.
- **Registro formal:** DEC-GOB-010.
- **Autoridad:** Responsable del proyecto.

### 3.2. Esquema de versiones del contenido

- **Necesidad:** distinguir la versión del contenido del identificador estable del requisito y conservar el historial de cambios.
- **Propuesta original (no aprobada):** `0.y` para propuestas y evaluación; `1.0` para la primera aprobación; `1.y` para cambios aprobados que preservan alcance y criterios; `2.0` o superior para cambios que alteran alcance, criterios, dependencias o interfaces.
- **Alternativas consideradas:**
  - **A. Versión semántica simplificada (recomendada):** `0.y`, `1.0`, `1.y`, `2.0`.
  - **B. Numeración entera:** `1`, `2`, `3`, sin distinción de tipo de cambio.
  - **C. Versionado por fecha:** cada aprobación se identifica por fecha.
- **Resolución:** Aprobado el esquema `0.x`, `1.0`, `1.1`, `1.2`, `1.3` y sucesivas. Toda modificación de un requisito aprobado exige evaluación de impacto y nueva aprobación. La conservación del historial es obligatoria. No se utiliza el criterio anterior de versiones mayores y menores según el alcance del cambio.
- **Estado:** Resuelto.
- **Registro formal:** DEC-GOB-011.
- **Autoridad:** Responsable del proyecto.

### 3.3. Estados operativos «En evaluación» y «Retirado»

- **Necesidad:** el ciclo de vida operativo debe distinguir la evaluación formal y el retiro de un requisito aprobado sin sustitución, manteniendo compatibilidad con la metodología aprobada.
- **Propuesta:** añadir **En evaluación** como subestado operativo de **Propuesto** y **Retirado** como estado terminal para un requisito aprobado que se retira sin sustitución. El vocabulario de la metodología aprobada prevalece.
- **Alternativas consideradas:**
  - **A. Usar únicamente los estados de la metodología:** Propuesto, Aprobado, Revisión de requisito aprobado, Sustituido y Rechazado.
  - **B. Añadir los estados operativos propuestos, mapeados a la metodología (recomendada).**
  - **C. Definir un ciclo de vida separado para requisitos, con independencia de la metodología.**
- **Resolución:** Aprobados los estados operativos **En evaluación** y **Retirado**, integrados con **Propuesto**, **Aprobado**, **Revisión de requisito aprobado**, **Sustituido** y **Rechazado**. Se conservan las reglas de transición, revisión y autoridad establecidas en B2.1.
- **Estado:** Resuelto.
- **Registro formal:** DEC-GOB-012.
- **Autoridad:** Responsable del proyecto.
- **Nota:** la aprobación no modifica la metodología de gobierno.

### 3.4. Escala de prioridad

- **Necesidad:** el atributo Prioridad requiere una escala común para comparar y ordenar requisitos.
- **Propuesta:** escala cualitativa `Crítica`, `Alta`, `Media`, `Baja`.
- **Alternativas consideradas:**
  - **A. Escala cualitativa de cuatro niveles (recomendada).**
  - **B. Escala numérica de 1 a 5.**
  - **C. Clasificación MoSCoW:** Must, Should, Could, Won't.
- **Resolución:** Aprobada la escala **Crítica**, **Alta**, **Media** y **Baja**, con las definiciones del bloque B2.1.1. La prioridad no sustituye la evaluación de riesgos ni la clasificación de seguridad industrial.
- **Estado:** Resuelto.
- **Registro formal:** DEC-GOB-013.
- **Autoridad:** Responsable del proyecto.

### 3.5. Referencias de necesidades y vínculos futuros

- **Necesidad:** la trazabilidad requiere referenciar necesidades y, en el futuro, elementos de arquitectura, implementación, pruebas y evidencias.
- **Propuesta:** utilizar documento y sección para las necesidades y los artefactos existentes; definir identificadores específicos cuando los elementos correspondientes sean creados. Registrar los vínculos no disponibles como **Pendiente** o **No aplica**.
- **Alternativas consideradas:**
  - **A. Referencias documentales y secciones, con identificadores posteriores (recomendada).**
  - **B. Definir ahora identificadores para necesidades, arquitectura, implementación, pruebas y evidencias.**
  - **C. No formalizar vínculos hasta que exista la arquitectura.**
- **Resolución:** Aprobado el criterio de trazabilidad: necesidades por documento y sección; requisitos por identificador; decisiones por `DEC-GOB` o `ADR`; arquitectura, implementación, pruebas y evidencias con identificadores definidos cuando existan sus sistemas documentales; estados **Existente**, **Pendiente** y **No aplica**. No se inventan referencias ni artefactos futuros.
- **Estado:** Resuelto.
- **Registro formal:** DEC-GOB-014.
- **Autoridad:** Responsable del proyecto.

### 3.6. Aprobación de la estructura documental de requisitos

- **Necesidad:** el índice y los tres registros de requisitos son propuestas y no deben utilizarse como convenciones aprobadas.
- **Propuesta:** aprobar la estructura documental, las convenciones y los criterios de calidad definidos en `docs/01-requisitos/`.
- **Alternativas consideradas:**
  - **A. Aprobar la estructura completa y las convenciones asociadas (recomendada).**
  - **B. Aprobar únicamente la estructura y mantener las convenciones pendientes.**
  - **C. Devolver la estructura para correcciones.**
- **Resolución:** Aprobados los cuatro documentos de requisitos, incluyendo estructura, convenciones, atributos y criterios de calidad. No constituye aprobación de requisitos concretos del producto.
- **Estado:** Resuelto.
- **Registro formal:** DEC-GOB-015.
- **Autoridad:** Responsable del proyecto.

## 4. Asuntos de B2.2.1 — resueltos en B2.2.2

Las quince preguntas fueron resueltas conceptualmente por el responsable del proyecto y registradas en DEC-GOB-017 a DEC-GOB-021. La resolución conceptual no equivale a una especificación técnica completa. El contenido íntegro de cada decisión se encuentra en `docs/06-decisiones/registro-decisiones.md`.

| Identificador | Pregunta | Decisión | Resolución (síntesis) | Estado |
|---|---|---|---|---|
| `PREG-P-01` | ¿Qué funciones y responsabilidades de seguridad corresponden a ControlCore frente a la máquina y a los sistemas externos? | `DEC-GOB-017` | ControlCore es responsable de las funciones de control y diagnóstico especificadas y validadas; no sustituye automáticamente las protecciones de la máquina; las responsabilidades de makeAutomatic, fabricantes e integradores deben delimitarse documentalmente. | Resuelta conceptualmente |
| `PREG-P-02` | ¿Qué análisis de riesgos y qué marco normativo deben aplicarse según el uso previsto y el mercado? | `DEC-GOB-017` | Se adopta un proceso documentado de identificación, evaluación y reducción de riesgos; las normas se determinan según función, aplicación y mercado; se consideran ISO 12100, IEC 60204-1, ISO 13849-1 e IEC 62061 cuando corresponda; no se declara conformidad sin evidencias. | Resuelta conceptualmente |
| `PREG-P-03` | ¿Qué condiciones deben considerarse estados seguros y quién los define? | `DEC-GOB-017` | Los estados seguros dependen del análisis de riesgos de cada aplicación; deben definirse transiciones, responsabilidades, recuperación y reinicio; no se asume que detener un motor o cortar su alimentación sea siempre seguro. | Resuelta conceptualmente |
| `PREG-P-04` | ¿Qué aplicaciones, máquinas y procesos industriales son prioritarios para la primera versión? | `DEC-GOB-018` | ControlCore será una plataforma modular y genérica de control industrial, independiente de una máquina, fabricante o proceso específico. | Resuelta conceptualmente |
| `PREG-P-05` | ¿Qué tipos de motores y actuadores deben considerarse en el alcance inicial? | `DEC-GOB-018` | Se busca extensibilidad hacia motores DC, paso a paso, servomotores, motores AC y otros actuadores; no implica implementar ni validar todas las familias en la primera versión; el soporte inicial permanece pendiente. | Resuelta conceptualmente |
| `PREG-P-06` | ¿Qué condiciones eléctricas, ambientales y de instalación deben soportarse? | `DEC-GOB-018` | El entorno objetivo es industrial real; el laboratorio sirve para desarrollo y validación, pero no basta para autorizar el uso industrial; las condiciones cuantitativas y normas se determinarán posteriormente. | Resuelta conceptualmente |
| `PREG-P-07` | ¿Qué capacidades del alcance conceptual forman parte de la primera versión? | `DEC-GOB-019` | Capacidades objetivo: control de motores y actuadores; supervisión; diagnóstico; configuración; integración externa; registro de eventos y datos. Desarrollo incremental. | Resuelta conceptualmente |
| `PREG-P-08` | ¿Qué capacidades quedan explícitamente fuera de la primera versión? | `DEC-GOB-019` | Se excluyen: soporte simultáneo de todas las familias de motores; control coordinado de múltiples ejes; algoritmos avanzados de optimización; integración con múltiples protocolos industriales; funciones de seguridad certificadas mientras no exista el proceso de análisis y conformidad. Las exclusiones no eliminan la evaluación de riesgos. | Resuelta conceptualmente |
| `PREG-P-09` | ¿Qué nivel de configuración, supervisión y diagnóstico se requiere inicialmente? | `DEC-GOB-019` | Configuración: establecer y consultar parámetros operativos. Supervisión: consultar estados, variables y condiciones anormales. Diagnóstico: identificar fallas detectables y facilitar su investigación. Interfaces, algoritmos y prestaciones pendientes. | Resuelta conceptualmente |
| `PREG-P-10` | ¿Con qué sistemas externos debe integrarse ControlCore y qué información debe intercambiar? | `DEC-GOB-020` | Interfaces documentadas y arquitectura independiente de protocolos; integración progresiva con PLC, HMI, SCADA y otros sistemas; no implica compatibilidad inmediata con todos. | Resuelta conceptualmente |
| `PREG-P-11` | ¿Qué actores deben operar, configurar y mantener el sistema, y qué responsabilidades y restricciones de acceso deben definirse? | `DEC-GOB-020` | Perfiles funcionales: Operador, Técnico/Integrador y Administrador técnico, con responsabilidades diferenciadas; autenticación y matriz detallada pendientes; los controles de acceso no sustituyen las protecciones industriales. | Resuelta conceptualmente |
| `PREG-P-12` | ¿Qué información debe registrarse y conservarse para operación, diagnóstico y auditoría? | `DEC-GOB-020` | Se registran eventos operativos, fallas y alarmas, cambios de configuración e información de diagnóstico; referencias temporales apropiadas; retención, almacenamiento y mecanismos técnicos pendientes. | Resuelta conceptualmente |
| `PREG-P-13` | ¿Qué criterios de aceptación y qué evidencia deben exigirse para la primera versión? | `DEC-GOB-021` | Criterios objetivos, medibles y verificables para funcionamiento, prestaciones, comportamiento ante fallas, reproducibilidad de pruebas, evidencia documental y evaluación de riesgos; valores y procedimientos pendientes. | Resuelta conceptualmente |
| `PREG-P-14` | ¿Qué entorno de pruebas, banco o máquina de referencia se utilizará para verificar y validar el producto? | `DEC-GOB-021` | Dos niveles: banco de pruebas de ingeniería y validación en entorno industrial real; la validación de laboratorio no sustituye la evaluación necesaria para autorizar el uso industrial. | Resuelta conceptualmente |
| `PREG-P-15` | ¿Qué documentación y soporte técnico debe entregarse con el producto? | `DEC-GOB-021` | Cinco conjuntos: documentación técnica; instalación y puesta en servicio; operación; mantenimiento y diagnóstico; validación y conformidad. Documentación versionada y coherente con las capacidades implementadas y validadas. | Resuelta conceptualmente |

## 5. Preguntas técnicas derivadas que permanecen abiertas

Las decisiones DEC-GOB-017 a DEC-GOB-021 resuelven el marco conceptual, pero no especifican los valores, interfaces, arquitecturas ni procedimientos necesarios para implementar y verificar. Permanecen abiertos, al menos:

| Tema | Descripción | Origen |
|---|---|---|
| Familia de motores y actuadores del primer incremento | Selección de la familia o familias que se implementarán y validarán primero. | `PREG-P-05`; `DEC-GOB-018` |
| Prestaciones cuantitativas | Valores medibles de control, supervisión, diagnóstico, respuesta y recuperación. | `PREG-P-13`; `DEC-GOB-021` |
| Condiciones industriales específicas | Rangos eléctricos, ambientales, de instalación y de compatibilidad electromagnética. | `PREG-P-06`; `DEC-GOB-018` |
| Interfaces y protocolos concretos | Sistemas externos, contratos, formatos, temporización y tratamiento de errores. | `PREG-P-10`; `DEC-GOB-020` |
| Arquitectura de seguridad | Funciones de seguridad, estados seguros por aplicación, independencia de protecciones y evaluación de conformidad. | `PREG-P-01`, `PREG-P-02`, `PREG-P-03`; `DEC-GOB-017` |
| Métodos de verificación | Procedimientos, criterios de aceptación cuantitativos, banco o máquina de referencia y evidencia exigible. | `PREG-P-13`, `PREG-P-14`; `DEC-GOB-021` |
| Alcance exacto del primer incremento | Capacidades, límites y priorización del primer incremento implementable. | `PREG-P-07`, `PREG-P-08`, `PREG-P-09`; `DEC-GOB-019` |
| Autenticación, permisos y retención | Mecanismo de autenticación, matriz de permisos, retención y almacenamiento de información. | `PREG-P-11`, `PREG-P-12`; `DEC-GOB-020` |

Estos asuntos no son decisiones aprobadas. Deberán resolverse antes de implementar el alcance afectado.

## 6. Reglas de gestión

- Los asuntos de B2.1 fueron resueltos en B2.1.1 y registrados en DEC-GOB-010 a DEC-GOB-015.
- Las preguntas de B2.2.1 fueron resueltas conceptualmente en B2.2.2 y registradas en DEC-GOB-017 a DEC-GOB-021.
- La aprobación de las necesidades, actores y escenarios se registró en DEC-GOB-016.
- La resolución conceptual no equivale a una especificación técnica completa. Las preguntas técnicas derivadas de la sección 5 permanecen abiertas.
- La aprobación correspondió al responsable del proyecto. Las preguntas técnicas pendientes requieren su decisión.
- Las alternativas no seleccionadas se conservan como historial.
- La incorporación de una propuesta al repositorio no constituye aprobación.

## 7. Referencias

- `docs/00-gobierno/metodologia-diseno.md` (secciones 9, 24, 25 y 26)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/01-requisitos/escenarios-uso.md`

## 8. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** registro inicial de asuntos pendientes de la estructura de requisitos.
- **0.1 — 2026-10-19 — B2.1.1:** resolución de los seis asuntos y registro formal DEC-GOB-010 a DEC-GOB-015.
- **0.1 — 2026-10-19 — B2.2.1:** incorporación de las quince preguntas pendientes de necesidades, actores y escenarios de uso.
- **0.2 — 2026-10-20 — B2.2.2:** resolución conceptual de las quince preguntas y registro DEC-GOB-016 a DEC-GOB-021; incorporación de las preguntas técnicas derivadas que permanecen abiertas.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
