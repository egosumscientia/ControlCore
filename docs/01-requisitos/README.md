# Índice y convenciones de requisitos — ControlCore

**Proyecto:** ControlCore
**Empresa:** makeAutomatic
**Tipo de proyecto:** Desarrollo de producto industrial comercial
**Documento:** Índice y convenciones de requisitos
**Versión:** 0.3
**Estado:** Revisión de documento aprobado — propuesta de requisitos candidatos B2.4
**Fase:** Ingeniería de requisitos
**Fecha de revisión:** 2026-10-20
**Aprobación:** Versión 0.1 aprobada el 2026-10-19 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.3 pendiente de aprobación

---

## 1. Propósito

Este documento establece la estructura común, el esquema de identificación, los atributos, los estados y los mecanismos de trazabilidad para los requisitos de ControlCore.

Su finalidad es que distintos agentes de IA y colaboradores puedan proponer, revisar y verificar requisitos de forma consistente, sin introducir decisiones técnicas no aprobadas.

La creación de este índice evita duplicar las convenciones comunes en los tres registros de requisitos.

## 2. Alcance

Este documento y los tres registros asociados constituyen la estructura y los candidatos de la ingeniería de requisitos.

No aprueban funcionalidades concretas, no seleccionan tecnologías, no establecen arquitecturas y no convierten los candidatos en línea base.

Los requisitos se registrarán en:

- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`

La línea base de gestión de requisitos fue aprobada en B2.1.1 (DEC-GOB-010 a DEC-GOB-015). No existe todavía una línea base de requisitos concretos.

B2.4 incorporó 39 requisitos candidatos: 27 `RF-###`, 5 `RNF-###` y 7 `RES-###`. Los candidatos están en estado **Propuesto**, no están aprobados y no sustituyen la línea base de gestión.

## 3. Convenciones

### 3.1. Identificadores

Se aprueba el siguiente esquema (DEC-GOB-010):

| Prefijo | Tipo | Registro |
|---|---|---|
| `RF-###` | Requisito funcional | `docs/01-requisitos/requisitos-funcionales.md` |
| `RNF-###` | Requisito no funcional | `docs/01-requisitos/requisitos-no-funcionales.md` |
| `RES-###` | Restricción | `docs/01-requisitos/restricciones-sistema.md` |

Reglas:

- El identificador se compone de un prefijo y un número secuencial de tres dígitos.
- Es único dentro de su tipo.
- Es estable: no cambia aunque cambie el contenido del requisito.
- No se reutiliza aunque el requisito sea rechazado, sustituido o retirado.
- La versión del contenido es independiente del identificador.
- No se asigna un identificador hasta que exista un requisito definido y registrado.
- Si se agota la numeración de tres dígitos, se requerirá una decisión de gobierno para ampliar el formato; no se reutilizarán identificadores.
- Este esquema fue aprobado en B2.1.1 (DEC-GOB-010). La metodología aprobada establece que el esquema definitivo se aprueba al iniciar el bloque de requisitos.

### 3.2. Versiones del contenido

Se aprueba el siguiente esquema de versiones, independiente del identificador (DEC-GOB-011):

| Versión | Uso |
|---|---|
| `0.x` | Requisito propuesto o en evaluación; todavía no aprobado. |
| `1.0` | Primera versión aprobada del requisito. |
| `1.1`, `1.2`, `1.3` y sucesivas | Revisiones posteriores aprobadas. |

Reglas:

- Toda modificación de un requisito aprobado exige evaluación de impacto y nueva aprobación.
- La versión aprobada es la que se referencia en la línea base de requisitos.
- Una versión anterior no se elimina del historial; la conservación del historial es obligatoria.
- La versión no sustituye al identificador ni al estado.
- La versión de este documento es independiente de la versión de cada requisito individual.
- No se utiliza un criterio de versiones mayores y menores basado en el alcance del cambio.

### 3.3. Prioridad

Se aprueba la siguiente escala (DEC-GOB-013):

- **Crítica:** indispensable para seguridad, cumplimiento obligatorio o viabilidad esencial del producto.
- **Alta:** necesaria para cumplir los objetivos principales.
- **Media:** importante, pero aplazable sin comprometer los objetivos esenciales.
- **Baja:** complementaria u opcional.

La prioridad no sustituye la evaluación de riesgos ni la clasificación de seguridad industrial.

Mientras no se determine la prioridad de un requisito, el atributo se registrará como **Pendiente de determinar**.

### 3.4. Referencias y vínculos

Se aprueba el siguiente criterio de trazabilidad (DEC-GOB-014):

- Las referencias documentales utilizan rutas relativas a la raíz del repositorio.
- Las necesidades se referencian mediante documento y sección.
- Los requisitos se referencian mediante sus identificadores `RF-###`, `RNF-###` o `RES-###`.
- Las decisiones se referencian mediante `DEC-GOB-###` o `ADR-###`.
- Los vínculos hacia arquitectura, implementación, pruebas y evidencias utilizarán los identificadores que se definan cuando existan sus sistemas documentales.
- No se inventan referencias ni artefactos futuros.
- Los estados de un vínculo son:
  - **Existente:** el elemento referenciado existe y está identificado.
  - **Pendiente:** el elemento se espera, pero todavía no existe o no está identificado.
  - **No aplica:** el vínculo no corresponde, con justificación documentada.

## 4. Atributos y ficha normalizada

### 4.1. Atributos

| Atributo | Obligatoriedad | Descripción |
|---|---|---|
| Identificador | Obligatorio desde el registro | Identificador único y estable según la sección 3.1. |
| Título | Obligatorio desde el registro | Denominación breve y descriptiva. |
| Descripción verificable | Obligatorio desde el registro | Comportamiento o condición observable y comprobable. Puede refinarse durante la evaluación, pero no puede aprobarse sin ser verificable. |
| Tipo | Obligatorio desde el registro | `RF`, `RNF` o `RES`. |
| Justificación | Obligatorio desde el registro | Razón por la que el requisito es necesario. |
| Origen | Obligatorio desde el registro | Necesidad, fuente externa o documento que lo origina. Si se desconoce, se registra **Pendiente de determinar**; no se inventa. |
| Prioridad | Obligatorio para aprobación | Puede ser **Pendiente de determinar** durante la propuesta o evaluación. |
| Estado | Obligatorio desde el registro | Estado del ciclo de vida definido en la sección 5. |
| Versión | Obligatorio desde el registro | Versión del contenido según la sección 3.2. |
| Dependencias | Obligatorio desde el registro | Requisitos o decisiones de los que depende. Debe indicarse **Ninguna** o **No aplica** cuando corresponda; no se omite. |
| Riesgos relacionados | Obligatorio desde el registro | Riesgos identificados. Debe indicarse **Ninguno identificado** cuando corresponda; no se omite. |
| Criterio de aceptación | Obligatorio para aprobación | Condición objetiva que permite aceptar el requisito. Puede ser **Pendiente de determinar** durante la propuesta o evaluación. |
| Método de verificación | Obligatorio para aprobación | Inspección, análisis, prueba, demostración u otro método aplicable. Puede ser **Pendiente de determinar** durante la propuesta o evaluación. |
| Evidencia de verificación | Opcional hasta la verificación | Referencia a la evidencia cuando exista. Obligatorio cuando se declare el requisito verificado o aceptado. |
| Decisiones relacionadas | Opcional hasta que existan | Referencias a `DEC-GOB-###` o `ADR-###`. Si no corresponde, **No aplica**. |
| Responsable de aprobación | Obligatorio para aprobación | Rol con autoridad para aprobar. Corresponde al responsable del proyecto. No se atribuye a un agente de IA. |

**Pendiente de determinación** es un valor permitido para atributos todavía desconocidos. No autoriza a omitir condiciones de aprobación ni a inventar valores.

### 4.2. Ficha normalizada

La siguiente es una plantilla. No constituye un requisito registrado ni asigna un identificador:

```markdown
### <ID> — <Título>

- **Identificador:** <ID>
- **Título:** <Título>
- **Descripción verificable:** <Descripción>
- **Tipo:** <RF | RNF | RES>
- **Justificación:** <Justificación>
- **Origen:** <Origen | Pendiente de determinar>
- **Prioridad:** <Prioridad | Pendiente de determinar>
- **Estado:** <Estado>
- **Versión:** <Versión>
- **Dependencias:** <IDs | Ninguna | No aplica>
- **Riesgos relacionados:** <Referencias | Ninguno identificado>
- **Criterio de aceptación:** <Criterio | Pendiente de determinar>
- **Método de verificación:** <Método | Pendiente de determinar>
- **Evidencia de verificación:** <Referencia | Pendiente | No aplica>
- **Decisiones relacionadas:** <Referencias | No aplica>
- **Responsable de aprobación:** <Responsable del proyecto | Pendiente>
```

## 5. Estados y ciclo de vida

### 5.1. Estados

El modelo operativo aprobado distingue los siguientes estados y su relación con la metodología aprobada:

| Estado | Definición | Relación con la metodología |
|---|---|---|
| **Propuesto** | Requisito identificado y registrado, todavía no sometido a evaluación formal. | Equivale a **Propuesto**. |
| **En evaluación** | Requisito sometido a revisión técnica, análisis de consistencia y verificación de criterios. | Subestado operativo de **Propuesto**; aprobado en B2.1.1 (DEC-GOB-012). |
| **Aprobado** | Requisito aceptado por el responsable del proyecto como base de diseño, implementación o verificación. | Equivale a **Aprobado**. |
| **Revisión de requisito aprobado** | Requisito previamente aprobado sujeto a un cambio controlado. | Equivale a **Revisión de requisito aprobado**. |
| **Sustituido** | Requisito reemplazado formalmente por otro requisito aprobado. | Equivale a **Sustituido**. |
| **Retirado** | Requisito aprobado que se retira del alcance sin sustitución, después de un cambio controlado. | No tiene equivalente exacto en la metodología; estado operativo adicional aprobado en B2.1.1 (DEC-GOB-012). |
| **Rechazado** | Requisito propuesto que se descarta antes de su aprobación, conservando el registro. | Equivale a **Rechazado**. |

El vocabulario de la metodología aprobada prevalece. Los estados operativos **En evaluación** y **Retirado** fueron aprobados en B2.1.1 (DEC-GOB-012) y no modifican la metodología de gobierno.

### 5.2. Transiciones permitidas

| Desde | Hacia | Condición |
|---|---|---|
| Propuesto | En evaluación | Se inicia la revisión formal. |
| En evaluación | Propuesto | Se devuelve para aclaración o reformulación. |
| En evaluación | Aprobado | Se cumplen las condiciones de aprobación y el responsable del proyecto aprueba. |
| En evaluación | Rechazado | Se descarta el requisito; se conserva el registro. |
| Aprobado | Revisión de requisito aprobado | Se propone un cambio controlado. |
| Revisión de requisito aprobado | Aprobado | Se aprueba una nueva versión. |
| Revisión de requisito aprobado | Sustituido | Otro requisito aprobado lo reemplaza formalmente. |
| Revisión de requisito aprobado | Retirado | Se retira sin sustitución, con justificación aprobada. |
| Sustituido | — | Estado terminal. |
| Retirado | — | Estado terminal. |
| Rechazado | — | Estado terminal. |

No se permite aprobar directamente desde **Propuesto** ni modificar un requisito **Aprobado** sin pasar por **Revisión de requisito aprobado**.

### 5.3. Autoridad y condiciones de aprobación

La aprobación de requisitos corresponde al responsable del proyecto. Los agentes de IA pueden proponer, analizar y recomendar, pero no aprobar.

Para aprobar un requisito deberán cumplirse, como mínimo:

1. Estado **En evaluación**.
2. Descripción verificable.
3. Justificación y origen documentados.
4. Prioridad determinada.
5. Criterio de aceptación objetivo.
6. Método de verificación definido.
7. Dependencias y riesgos identificados, o declarados como inexistentes.
8. Trazabilidad hacia la necesidad u origen.
9. Ausencia de contradicciones conocidas sin resolver.
10. Registro de la aprobación con versión, fecha y autoridad.

No se establecen aprobaciones automáticas.

### 5.4. Cambios e historial

- Todo cambio sobre un requisito aprobado se inicia en **Revisión de requisito aprobado**.
- El cambio deberá identificar motivo, alcance, impacto en requisitos relacionados, decisiones, arquitectura, verificación y trazabilidad.
- La nueva versión deberá ser aprobada por el responsable del proyecto antes de utilizarse como base.
- Cada requisito conservará un historial de versiones con fecha, estado, autoridad y motivo del cambio.
- El historial podrá mantenerse en el registro o en un registro de cambios vinculado.
- La versión anterior no se elimina.

### 5.5. Línea base de requisitos

Un conjunto de requisitos aprobados para un alcance constituye una línea base de requisitos.

La línea base se identificará por fecha y por el conjunto de versiones aprobadas. Su identificador formal se definirá cuando exista la primera línea base.

Las modificaciones posteriores a una línea base requerirán control de cambios y una nueva aprobación.

No existe todavía una línea base de requisitos concretos.

## 6. Criterios de calidad

Los requisitos deberán ser, según corresponda:

- Claros y comprensibles.
- Necesarios para el alcance aprobado.
- Verificables mediante criterios objetivos.
- Consistentes entre sí.
- Trazables hacia su origen y hacia la verificación.
- Técnicamente viables.
- Suficientemente precisos para evitar interpretaciones incompatibles.
- Ajenos a decisiones de diseño, tecnología o implementación no aprobadas.

No se aceptarán expresiones ambiguas como «rápido», «robusto», «seguro» o «eficiente» como únicos criterios de aceptación.

Cada registro de requisitos añade criterios específicos según su tipo.

## 7. Trazabilidad

### 7.1. Cadena de trazabilidad

La trazabilidad deberá permitir relacionar, cuando corresponda:

**Necesidad del producto → Requisito → Decisión → Elemento de arquitectura → Implementación → Prueba → Evidencia.**

No se presupone que todos los elementos existan actualmente.

### 7.2. Registro de vínculos

Los vínculos se registrarán en una tabla con la siguiente estructura:

| Requisito | Tipo de vínculo | Referencia | Estado del vínculo | Observación |
|---|---|---|---|---|
| `<ID>` | Necesidad, Decisión, Arquitectura, Implementación, Prueba o Evidencia | Referencia o descripción | Existente, Pendiente o No aplica | Justificación o acción pendiente |

Reglas:

- Un requisito puede tener más de un vínculo del mismo tipo.
- Los vínculos **Pendiente** deberán indicar qué falta y no podrán presentarse como evidencia de cobertura.
- Los vínculos **No aplica** deberán justificarse.
- Las decisiones se referencian mediante `DEC-GOB-###` o `ADR-###`.
- Las decisiones de B2.4 se referencian como `B2.4-D##` por instrucción expresa de ese bloque. Esta referencia es de trazabilidad documental y no crea una nueva familia formal de decisiones ni sustituye `DEC-GOB` o `ADR`.
- Los demás vínculos utilizarán el esquema que se defina cuando exista el elemento correspondiente.

### 7.3. Requisitos huérfanos, duplicados, contradictorios y no verificables

- **Huérfano:** requisito sin vínculo de necesidad existente o pendiente. Deberá marcarse y no podrá aprobarse hasta resolver el vínculo. Las restricciones con origen externo podrán usar **No aplica** con la fuente documentada.
- **Duplicado:** dos requisitos con el mismo propósito o comportamiento. Deberán fusionarse o diferenciarse explícitamente; no se admitirán identificadores duplicados.
- **Contradictorio:** requisitos incompatibles. La contradicción se registrará en `docs/06-decisiones/pendientes.md` y en `docs/00-gobierno/ESTADO-ACTUAL.md`, y no se aprobará hasta su resolución.
- **No verificable:** requisito sin criterio de aceptación objetivo o método de verificación. No podrá aprobarse; deberá reformularse o permanecer pendiente.

## 8. Pendientes

No quedan convenciones pendientes de aprobación para la estructura de requisitos.

Las seis decisiones de B2.1 fueron aprobadas en B2.1.1 y registradas como DEC-GOB-010 a DEC-GOB-015.

B2.2 aprobó las necesidades, actores y escenarios (DEC-GOB-016) y resolvió conceptualmente las preguntas de producto (DEC-GOB-017 a DEC-GOB-021). B2.3 consolidó las decisiones conceptuales de alcance y comportamiento en DEC-GOB-022 a DEC-GOB-030.

B2.4 consolidó las 60 decisiones de la ronda posterior a B2.3 y preparó 27 requisitos funcionales, 5 no funcionales y 7 restricciones candidatas. Todos están en estado **Propuesto**. No existe línea base de requisitos concretos.

El siguiente paso es revisar y completar los criterios pendientes, aprobar o rechazar los candidatos y establecer una línea base. No se inicia automáticamente.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md` (secciones 24, 25 y 26)
- `docs/00-gobierno/criterios-calidad.md` (secciones 3 y 13)
- `docs/00-gobierno/definicion-de-terminado.md` (secciones 7, 19 y 20)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.4.md`
- `docs/03-seguridad-industrial/analisis-riesgos.md`
- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`
- `docs/02-arquitectura/` (futuro)
- `docs/05-validacion/` (futuro)

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** estructura inicial, convenciones, atributos, estados y trazabilidad propuestos.
- **0.1 — 2026-10-19 — B2.1.1:** aprobación de la línea base de gestión de requisitos (DEC-GOB-010 a DEC-GOB-015).
- **0.2 — 2026-10-20 — B2.3:** actualización del estado de avance y referencia a la consolidación de decisiones conceptuales. Las convenciones aprobadas no se modifican. Versión pendiente de aprobación.
- **0.3 — 2026-10-20 — B2.4:** incorporación de 39 requisitos candidatos y referencia a la consolidación B2.4 y al análisis preliminar de riesgos. Las convenciones aprobadas no se modifican. Versión pendiente de aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
