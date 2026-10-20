# Índice y convenciones de requisitos — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Índice y convenciones de requisitos  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto

---

## 1. Propósito

Este documento establece la estructura común, el esquema de identificación, los atributos, los estados y los mecanismos de trazabilidad para los requisitos de ControlCore.

Su finalidad es que distintos agentes de IA y colaboradores puedan proponer, revisar y verificar requisitos de forma consistente, sin introducir decisiones técnicas no aprobadas.

La creación de este índice evita duplicar las convenciones comunes en los tres registros de requisitos.

## 2. Alcance

Este documento y los tres registros asociados constituyen la estructura inicial de la ingeniería de requisitos.

No definen funcionalidades concretas, no seleccionan tecnologías, no establecen arquitecturas y no aprueban requisitos.

Los requisitos se registrarán en:

- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`

No existe todavía una línea base de requisitos.

## 3. Convenciones

### 3.1. Identificadores

Se propone el siguiente esquema:

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
- Este esquema se propone como convención de B2.1 y requiere aprobación. La metodología aprobada establece que el esquema definitivo se aprobará al iniciar el bloque de requisitos.

### 3.2. Versiones del contenido

Se propone el siguiente esquema de versiones, independiente del identificador:

| Versión | Uso |
|---|---|
| `0.y` | Requisito propuesto o en evaluación; todavía no aprobado. |
| `1.0` | Primera versión aprobada del requisito. |
| `1.y` | Cambios aprobados que preservan alcance, criterios de aceptación y dependencias. |
| `2.0` o superior | Cambios aprobados que alteran alcance, criterios de aceptación, dependencias o interfaces. |

Reglas:

- La versión aprobada es la que se referencia en la línea base de requisitos.
- Una versión anterior no se elimina del historial.
- La versión no sustituye al identificador ni al estado.
- Este esquema se propone y requiere aprobación.

### 3.3. Prioridad

La escala de prioridad se definirá antes de la primera aprobación de requisitos.

Mientras no exista una escala aprobada, el atributo se registrará como **Pendiente de determinar**. No se asignarán valores de prioridad sin una escala documentada.

### 3.4. Referencias y vínculos

- Las referencias documentales utilizan rutas relativas a la raíz del repositorio.
- Las decisiones se referencian mediante `DEC-GOB-###` o `ADR-###`, según su familia.
- La necesidad de origen se referenciará mediante el documento y la sección correspondiente. Si en el futuro se aprueba un esquema de identificadores de necesidad, se utilizará ese esquema.
- Los vínculos hacia arquitectura, implementación, pruebas y evidencias utilizarán el esquema que se defina cuando esos elementos existan. Hasta entonces se registrarán como **Pendiente**.
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

El modelo operativo propuesto distingue los siguientes estados y su relación con la metodología aprobada:

| Estado | Definición | Relación con la metodología |
|---|---|---|
| **Propuesto** | Requisito identificado y registrado, todavía no sometido a evaluación formal. | Equivale a **Propuesto**. |
| **En evaluación** | Requisito sometido a revisión técnica, análisis de consistencia y verificación de criterios. | Subestado operativo de **Propuesto**; se propone como refinamiento y requiere aprobación. |
| **Aprobado** | Requisito aceptado por el responsable del proyecto como base de diseño, implementación o verificación. | Equivale a **Aprobado**. |
| **Revisión de requisito aprobado** | Requisito previamente aprobado sujeto a un cambio controlado. | Equivale a **Revisión de requisito aprobado**. |
| **Sustituido** | Requisito reemplazado formalmente por otro requisito aprobado. | Equivale a **Sustituido**. |
| **Retirado** | Requisito aprobado que se retira del alcance sin sustitución, después de un cambio controlado. | No tiene equivalente exacto en la metodología; se propone como estado operativo adicional y requiere aprobación. |
| **Rechazado** | Requisito propuesto que se descarta antes de su aprobación, conservando el registro. | Equivale a **Rechazado**. |

El vocabulario de la metodología aprobada prevalece. La incorporación de **En evaluación** y **Retirado** como estados operativos requiere aprobación y no modifica la metodología.

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

No existe todavía una línea base de requisitos.

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
- Los demás vínculos utilizarán el esquema que se defina cuando exista el elemento correspondiente.

### 7.3. Requisitos huérfanos, duplicados, contradictorios y no verificables

- **Huérfano:** requisito sin vínculo de necesidad existente o pendiente. Deberá marcarse y no podrá aprobarse hasta resolver el vínculo. Las restricciones con origen externo podrán usar **No aplica** con la fuente documentada.
- **Duplicado:** dos requisitos con el mismo propósito o comportamiento. Deberán fusionarse o diferenciarse explícitamente; no se admitirán identificadores duplicados.
- **Contradictorio:** requisitos incompatibles. La contradicción se registrará en `docs/06-decisiones/pendientes.md` y en `docs/00-gobierno/ESTADO-ACTUAL.md`, y no se aprobará hasta su resolución.
- **No verificable:** requisito sin criterio de aceptación objetivo o método de verificación. No podrá aprobarse; deberá reformularse o permanecer pendiente.

## 8. Pendientes

No se han definido requisitos funcionales, no funcionales ni restricciones.

Las siguientes convenciones se proponen y permanecen pendientes de aprobación:

1. Esquema de identificación `RF-###`, `RNF-###`, `RES-###`.
2. Esquema de versiones del contenido.
3. Estados operativos **En evaluación** y **Retirado** y su relación con la metodología aprobada.
4. Escala de prioridad.
5. Esquema de referencia de necesidades y de vínculos hacia arquitectura, implementación, pruebas y evidencias.
6. Estructura documental de este índice y de los tres registros.

El detalle y las alternativas se encuentran en `docs/06-decisiones/pendientes.md`.

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
- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`
- `docs/02-arquitectura/` (futuro)
- `docs/05-validacion/` (futuro)

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** estructura inicial, convenciones, atributos, estados y trazabilidad propuestos. Pendiente de aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
