# Asuntos de decisión — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Registro de asuntos de decisión  
**Versión:** 0.1  
**Estado:** Registro de asuntos resueltos — B2.1  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** No aplica — registro histórico

---

## 1. Propósito

Este documento registra los asuntos que requirieron una decisión del responsable del proyecto durante B2.1 y sus resoluciones en B2.1.1.

Conserva las alternativas consideradas y la trazabilidad hacia el registro formal de decisiones.

## 2. Alcance

Este registro comprende los asuntos identificados durante B2.1 — Estructura, identificación y trazabilidad de requisitos y sus resoluciones en B2.1.1.

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

## 4. Reglas de gestión

- Los asuntos de B2.1 fueron resueltos en B2.1.1.
- La aprobación correspondió al responsable del proyecto.
- Las resoluciones se registraron en DEC-GOB-010 a DEC-GOB-015.
- Las alternativas no seleccionadas se conservan como historial.
- La incorporación de una propuesta al repositorio no constituye aprobación.

## 5. Referencias

- `docs/00-gobierno/metodologia-diseno.md` (secciones 9, 24, 25 y 26)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`

## 6. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** registro inicial de asuntos pendientes de la estructura de requisitos.
- **0.1 — 2026-10-19 — B2.1.1:** resolución de los seis asuntos y registro formal DEC-GOB-010 a DEC-GOB-015.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
