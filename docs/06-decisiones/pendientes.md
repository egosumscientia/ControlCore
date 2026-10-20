# Asuntos pendientes de decisión — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Registro de asuntos pendientes de decisión  
**Versión:** 0.1  
**Estado:** Registro de asuntos pendientes — no aprobatorio  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** No aplica — registro de pendientes

---

## 1. Propósito

Este documento registra los asuntos que requieren una decisión del responsable del proyecto y que no están cubiertos por la línea base de gobierno aprobada.

Su función es impedir que las convenciones propuestas se utilicen como decisiones aprobadas por el hecho de estar incorporadas al repositorio.

## 2. Alcance

Este registro comprende los asuntos pendientes identificados durante B2.1 — Estructura, identificación y trazabilidad de requisitos.

No contiene decisiones aprobadas ni requisitos del producto. Una vez resueltos, los asuntos se incorporarán al registro formal de decisiones o al documento correspondiente, según su naturaleza.

## 3. Asuntos pendientes de B2.1

### 3.1. Esquema de identificación de requisitos

- **Necesidad:** la metodología aprobada establece que el esquema definitivo de identificación de requisitos se aprobará al iniciar el bloque de requisitos.
- **Propuesta:** prefijos `RF-###` para requisitos funcionales, `RNF-###` para requisitos no funcionales y `RES-###` para restricciones.
- **Alternativas consideradas:**
  - **A. Prefijos por tipo (recomendada):** `RF-###`, `RNF-###`, `RES-###`.
  - **B. Identificador único con atributo de tipo:** `REQ-###` más un campo `Tipo`.
  - **C. Prefijos adicionales por dominio:** por ejemplo, prefijos específicos para seguridad, comunicaciones o control.
- **Estado:** Pendiente.
- **Autoridad:** Responsable del proyecto.

### 3.2. Esquema de versiones del contenido

- **Necesidad:** distinguir la versión del contenido del identificador estable del requisito y conservar el historial de cambios.
- **Propuesta:** `0.y` para propuestas y evaluación; `1.0` para la primera aprobación; `1.y` para cambios aprobados que preservan alcance y criterios; `2.0` o superior para cambios que alteran alcance, criterios, dependencias o interfaces.
- **Alternativas consideradas:**
  - **A. Versión semántica simplificada (recomendada):** `0.y`, `1.0`, `1.y`, `2.0`.
  - **B. Numeración entera:** `1`, `2`, `3`, sin distinción de tipo de cambio.
  - **C. Versionado por fecha:** cada aprobación se identifica por fecha.
- **Estado:** Pendiente.
- **Autoridad:** Responsable del proyecto.

### 3.3. Estados operativos «En evaluación» y «Retirado»

- **Necesidad:** el ciclo de vida operativo debe distinguir la evaluación formal y el retiro de un requisito aprobado sin sustitución, manteniendo compatibilidad con la metodología aprobada.
- **Propuesta:** añadir **En evaluación** como subestado operativo de **Propuesto** y **Retirado** como estado terminal para un requisito aprobado que se retira sin sustitución. El vocabulario de la metodología aprobada prevalece.
- **Alternativas consideradas:**
  - **A. Usar únicamente los estados de la metodología:** Propuesto, Aprobado, Revisión de requisito aprobado, Sustituido y Rechazado.
  - **B. Añadir los estados operativos propuestos, mapeados a la metodología (recomendada).**
  - **C. Definir un ciclo de vida separado para requisitos, con independencia de la metodología.**
- **Estado:** Pendiente.
- **Autoridad:** Responsable del proyecto.
- **Nota:** la aprobación de esta propuesta no modifica por sí misma la metodología aprobada; su relación deberá quedar documentada.

### 3.4. Escala de prioridad

- **Necesidad:** el atributo Prioridad requiere una escala común para comparar y ordenar requisitos.
- **Propuesta:** escala cualitativa `Crítica`, `Alta`, `Media`, `Baja`.
- **Alternativas consideradas:**
  - **A. Escala cualitativa de cuatro niveles (recomendada).**
  - **B. Escala numérica de 1 a 5.**
  - **C. Clasificación MoSCoW:** Must, Should, Could, Won't.
- **Estado:** Pendiente.
- **Autoridad:** Responsable del proyecto.

### 3.5. Referencias de necesidades y vínculos futuros

- **Necesidad:** la trazabilidad requiere referenciar necesidades y, en el futuro, elementos de arquitectura, implementación, pruebas y evidencias.
- **Propuesta:** utilizar documento y sección para las necesidades y los artefactos existentes; definir identificadores específicos cuando los elementos correspondientes sean creados. Registrar los vínculos no disponibles como **Pendiente** o **No aplica**.
- **Alternativas consideradas:**
  - **A. Referencias documentales y secciones, con identificadores posteriores (recomendada).**
  - **B. Definir ahora identificadores para necesidades, arquitectura, implementación, pruebas y evidencias.**
  - **C. No formalizar vínculos hasta que exista la arquitectura.**
- **Estado:** Pendiente.
- **Autoridad:** Responsable del proyecto.

### 3.6. Aprobación de la estructura documental de requisitos

- **Necesidad:** el índice y los tres registros de requisitos son propuestas y no deben utilizarse como convenciones aprobadas.
- **Propuesta:** aprobar la estructura documental, las convenciones y los criterios de calidad definidos en `docs/01-requisitos/`.
- **Alternativas consideradas:**
  - **A. Aprobar la estructura completa y las convenciones asociadas (recomendada).**
  - **B. Aprobar únicamente la estructura y mantener las convenciones pendientes.**
  - **C. Devolver la estructura para correcciones.**
- **Estado:** Pendiente.
- **Autoridad:** Responsable del proyecto.

## 4. Reglas de gestión

- Estos asuntos no están aprobados.
- La aprobación corresponde al responsable del proyecto.
- No se asignarán identificadores formales de decisión a estos asuntos hasta que sean resueltos.
- Una vez resueltos, se registrarán en `docs/06-decisiones/registro-decisiones.md` con el identificador que corresponda, o en el documento de requisitos que resulte aplicable.
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

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
