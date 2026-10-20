# Necesidades del producto — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Necesidades del producto  
**Versión:** 0.3  
**Estado:** Revisión de documento aprobado — actualización B2.3 pendiente de aprobación  
**Fase:** Ingeniería conceptual y de requisitos  
**Fecha de revisión:** 2026-10-20  
**Aprobación:** Versión 0.2 aprobada el 2026-10-20 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.3 pendiente de aprobación

---

## 1. Propósito

Este documento identifica las necesidades del producto a partir de la visión aprobada y de los documentos de gobierno de ControlCore, y registra su aprobación formal.

Las necesidades fueron propuestas en B2.2.1 y aprobadas en B2.2.2. Su finalidad es proporcionar una base trazable para la definición posterior de requisitos, sin convertir posibilidades conceptuales en requisitos obligatorios.

La versión 0.3 actualiza únicamente las referencias de estado afectadas por las decisiones conceptuales de B2.3 (`DEC-GOB-022` a `DEC-GOB-030`). No modifica las necesidades aprobadas ni las decisiones `DEC-GOB-016` a `DEC-GOB-021`.

## 2. Alcance

Este documento comprende las necesidades aprobadas del producto, las hipótesis de aplicación conservadas y las preguntas técnicas que permanecen abiertas, en relación con el control, la supervisión, el diagnóstico y la operación industrial de motores y actuadores.

No contiene requisitos funcionales, no funcionales o restricciones aprobadas. No selecciona tecnologías, componentes, protocolos ni arquitecturas.

Los identificadores `NEC-P-###` identifican las necesidades aprobadas en este documento. No constituyen el esquema permanente de requisitos ni se reutilizan como identificadores `RF-###`, `RNF-###` o `RES-###`. Los identificadores `PREG-P-###` identifican las preguntas de B2.2.1, resueltas conceptualmente mediante DEC-GOB-017 a DEC-GOB-021.

## 3. Fuente y clasificación de afirmaciones

La fuente principal es `docs/00-gobierno/vision-producto.md`. Se consultaron además los cinco documentos de gobierno aprobados y la estructura de gestión de requisitos.

Las afirmaciones se clasifican así:

- **Hecho documentado:** establecido explícitamente en un documento aprobado.
- **Necesidad inferida:** derivada de la visión o del alcance conceptual, pero no validada con los actores.
- **Hipótesis de aplicación:** supone un contexto, una aplicación o una interacción todavía no aprobada.
- **Pregunta abierta:** requiere una decisión o confirmación del responsable del proyecto.
- **Alternativa no seleccionada:** opción considerada que no ha sido aprobada.

Las diez necesidades fueron aprobadas el 2026-10-20 (DEC-GOB-016). La clasificación de origen se conserva como historial. La aprobación no convierte las hipótesis de aplicación en requisitos implementables ni confirma que todas las capacidades se incluyan en la primera versión.

## 4. Necesidades aprobadas

Las diez necesidades de la tabla están aprobadas como necesidades del producto (DEC-GOB-016, 2026-10-20).

| Identificador | Necesidad aprobada | Actores principales | Clasificación de origen |
|---|---|---|---|
| `NEC-P-01` | Control de motores y actuadores | Integrador; ingenieros y técnicos | Necesidad inferida |
| `NEC-P-02` | Supervisión de la operación | Operador; producción; ingenieros y técnicos | Necesidad inferida |
| `NEC-P-03` | Diagnóstico de condiciones anormales | Ingenieros y técnicos; mantenimiento | Necesidad inferida |
| `NEC-P-04` | Configuración y puesta en servicio | Integrador; ingenieros y técnicos | Necesidad inferida |
| `NEC-P-05` | Mantenimiento y actualización controlada | Mantenimiento; ingenieros y técnicos | Necesidad inferida |
| `NEC-P-06` | Integración con máquinas y sistemas externos | Integrador; aliados especializados | Hipótesis de aplicación |
| `NEC-P-07` | Operación industrial confiable y comportamiento ante fallas | Operador; producción; mantenimiento | Necesidad inferida |
| `NEC-P-08` | Seguridad y delimitación de responsabilidades | Todos los actores | Hecho documentado; alcance pendiente |
| `NEC-P-09` | Confiabilidad, disponibilidad y recuperación | Producción; mantenimiento | Necesidad inferida |
| `NEC-P-10` | Documentación, verificación y soporte técnico | Desarrollo; integrador; mantenimiento | Necesidad inferida |

La aprobación confirma la necesidad, no un conjunto concreto de requisitos, interfaces o capacidades de la primera versión. Las preguntas citadas en cada necesidad fueron resueltas conceptualmente; las preguntas técnicas derivadas se enumeran en la sección 6.2.

### NEC-P-01 — Control de motores y actuadores

- **Descripción:** necesidad de disponer de una base para comandar y coordinar motores y actuadores en aplicaciones industriales.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-02`.
- **Problema que busca resolver:** implementar soluciones de control de movimiento y actuación adaptadas a distintas máquinas y procesos.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 1 y 7).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-04`, `PREG-P-05`, `PREG-P-07`.

### NEC-P-02 — Supervisión de la operación

- **Descripción:** necesidad de conocer el estado del sistema, las condiciones de operación y las alarmas relevantes.
- **Actores relacionados:** `ACT-P-02`, `ACT-P-03`, `ACT-P-04`.
- **Problema que busca resolver:** operar con información suficiente y detectar desviaciones.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5 y 7).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-07`, `PREG-P-09`, `PREG-P-12`.

### NEC-P-03 — Diagnóstico de condiciones anormales

- **Descripción:** necesidad de identificar fallas, sus posibles causas y la información necesaria para la corrección.
- **Actores relacionados:** `ACT-P-02`, `ACT-P-05`.
- **Problema que busca resolver:** reducir el tiempo de diagnóstico y facilitar la recuperación del sistema.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5, 7 y 9).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-09`, `PREG-P-12`, `PREG-P-13`.

### NEC-P-04 — Configuración y puesta en servicio

- **Descripción:** necesidad de adaptar el sistema a cada aplicación y verificar su puesta en servicio.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-02`.
- **Problema que busca resolver:** configurar la solución de forma controlada y comprobar que está lista para operar.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5 y 7).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-04`, `PREG-P-09`, `PREG-P-11`.

### NEC-P-05 — Mantenimiento y actualización controlada

- **Descripción:** necesidad de mantener, actualizar y restaurar el sistema sin perder trazabilidad ni comprometer la operación.
- **Actores relacionados:** `ACT-P-02`, `ACT-P-05`, `ACT-P-06`.
- **Problema que busca resolver:** preservar la operación y la compatibilidad durante el ciclo de vida.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5, 9 y 12).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-11`, `PREG-P-13`, `PREG-P-15`.

### NEC-P-06 — Integración con máquinas y sistemas externos

- **Descripción:** necesidad de intercambiar información y coordinar la operación con máquinas y sistemas existentes.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-07`.
- **Problema que busca resolver:** incorporar ControlCore en entornos industriales con otros equipos y sistemas.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 2, 7 y 9).
- **Clasificación:** Hipótesis de aplicación. No se ha aprobado un conjunto de interfaces ni sistemas externos.
- **Estado:** Aprobada como necesidad — 2026-10-20 (DEC-GOB-016). El alcance de integración permanece pendiente.
- **Preguntas de origen:** `PREG-P-04`, `PREG-P-10`, `PREG-P-11`.

### NEC-P-07 — Operación industrial confiable y comportamiento ante fallas

- **Descripción:** necesidad de un comportamiento predecible en operación normal y ante condiciones anormales.
- **Actores relacionados:** `ACT-P-03`, `ACT-P-04`, `ACT-P-05`.
- **Problema que busca resolver:** mantener la operación dentro de condiciones definidas y evitar respuestas improvisadas ante fallas.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 9 y 12).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-01`, `PREG-P-03`, `PREG-P-06`.

### NEC-P-08 — Seguridad y delimitación de responsabilidades

- **Descripción:** necesidad de identificar peligros, delimitar las funciones de seguridad y establecer qué responsabilidades corresponden a ControlCore y cuáles a la máquina o a sistemas externos.
- **Actores relacionados:** todos los actores; en particular `ACT-P-01`, `ACT-P-05` y el responsable del proyecto.
- **Problema que busca resolver:** evitar que una función de software se considere por sí sola una protección suficiente y evitar vacíos de responsabilidad.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 9, 11 y 12) y `docs/00-gobierno/principios-ingenieria.md` (sección 5).
- **Clasificación:** Hecho documentado en cuanto a la necesidad de considerar la seguridad; alcance, funciones y responsabilidades pendientes.
- **Estado:** Aprobada como necesidad — 2026-10-20 (DEC-GOB-016). El análisis de riesgos y la delimitación concreta de responsabilidades permanecen pendientes.
- **Preguntas de origen:** `PREG-P-01`, `PREG-P-02`, `PREG-P-03`.

### NEC-P-09 — Confiabilidad, disponibilidad y recuperación

- **Descripción:** necesidad de operar de forma confiable y recuperarse de forma controlada después de fallas o interrupciones.
- **Actores relacionados:** `ACT-P-04`, `ACT-P-05`.
- **Problema que busca resolver:** reducir el impacto de las interrupciones y facilitar la continuidad operativa.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 9 y 12).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-06`, `PREG-P-13`, `PREG-P-14`.

### NEC-P-10 — Documentación, verificación y soporte técnico

- **Descripción:** necesidad de disponer de documentación, criterios de verificación y soporte para instalar, operar, mantener y evolucionar el producto.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-02`, `ACT-P-06`, `ACT-P-07`.
- **Problema que busca resolver:** permitir una implementación y un soporte profesional, con evidencia de aceptación.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5 y 12) y `README.md` (sección 3).
- **Clasificación:** Necesidad inferida.
- **Estado:** Aprobada — 2026-10-20 (DEC-GOB-016).
- **Preguntas de origen:** `PREG-P-13`, `PREG-P-14`, `PREG-P-15`.

## 5. Límites y exclusiones

### 5.1. Límites vigentes

La visión aprobada y las decisiones DEC-GOB-017 a DEC-GOB-030 mantienen los siguientes límites:

- No existe selección definitiva de plataforma electrónica ni arquitectura de control.
- La familia inicial del primer incremento está definida como motores DC con escobillas (`DEC-GOB-022`); el modelo, las prestaciones y la electrónica no están seleccionados.
- No se han aprobado protocolos de comunicación, interfaces concretas ni arquitectura de backend o frontend.
- No se han establecido prestaciones cuantitativas de control, supervisión o diagnóstico.
- No se ha determinado la clasificación de seguridad de una aplicación concreta ni se han aprobado funciones de seguridad certificadas para la primera versión.
- No se ha aprobado un alcance comercial definitivo ni un precio de venta.

Estos límites no se resuelven en este documento.

### 5.2. Límites y definiciones pendientes tras B2.3

| Tema | Estado tras B2.3 | Referencia |
|---|---|---|
| Tipos de motores y actuadores | Objetivo de extensibilidad aprobado; familia inicial del primer incremento definida como motores DC con escobillas; modelo y parámetros pendientes. | `DEC-GOB-018`, `DEC-GOB-022` |
| Aplicaciones industriales prioritarias | Plataforma genérica aprobada; aplicaciones concretas no seleccionadas. | `DEC-GOB-018` |
| Alcance de la primera versión | Capacidades objetivo y exclusiones aprobadas; alcance funcional del primer incremento delimitado; prestaciones y detalles pendientes. | `DEC-GOB-019`, `DEC-GOB-022` |
| Límites de responsabilidad entre ControlCore y la máquina | Obligación de delimitación documental aprobada; asignación concreta pendiente. | `DEC-GOB-017` |
| Funciones de seguridad y responsabilidades externas | Funciones certificadas excluidas de la primera versión; análisis de riesgos y arquitectura de seguridad pendientes. | `DEC-GOB-017`, `DEC-GOB-019` |
| Condiciones de instalación | Entorno industrial real aprobado; condiciones cuantitativas pendientes. | `DEC-GOB-018` |
| Interfaces con sistemas existentes | Interfaces documentadas y arquitectura independiente de protocolos aprobadas; protocolos y sistemas concretos pendientes. | `DEC-GOB-020` |
| Prestaciones esperadas | Criterios medibles exigidos; valores cuantitativos pendientes. | `DEC-GOB-021` |
| Requisitos regulatorios aplicables | Proceso de evaluación adoptado; normas aplicables por determinar según función, aplicación y mercado. | `DEC-GOB-017` |

## 6. Decisiones aprobadas y preguntas técnicas derivadas

### 6.1. Decisiones aprobadas

Las quince preguntas de B2.2.1 fueron resueltas conceptualmente por el responsable del proyecto y registradas en DEC-GOB-017 a DEC-GOB-021. La síntesis siguiente conserva la trazabilidad; el contenido completo se encuentra en `docs/06-decisiones/registro-decisiones.md`.

| Pregunta | Asunto | Decisión | Estado |
|---|---|---|---|
| `PREG-P-01` | Funciones y responsabilidades de seguridad | `DEC-GOB-017` | Resuelta conceptualmente |
| `PREG-P-02` | Análisis de riesgos y normativa | `DEC-GOB-017` | Resuelta conceptualmente |
| `PREG-P-03` | Estados seguros | `DEC-GOB-017` | Resuelta conceptualmente |
| `PREG-P-04` | Aplicación objetivo | `DEC-GOB-018` | Resuelta conceptualmente |
| `PREG-P-05` | Motores y actuadores | `DEC-GOB-018` | Resuelta conceptualmente |
| `PREG-P-06` | Entorno y condiciones | `DEC-GOB-018` | Resuelta conceptualmente |
| `PREG-P-07` | Capacidades funcionales objetivo | `DEC-GOB-019` | Resuelta conceptualmente |
| `PREG-P-08` | Exclusiones iniciales | `DEC-GOB-019` | Resuelta conceptualmente |
| `PREG-P-09` | Nivel funcional inicial | `DEC-GOB-019` | Resuelta conceptualmente |
| `PREG-P-10` | Integración externa | `DEC-GOB-020` | Resuelta conceptualmente |
| `PREG-P-11` | Perfiles funcionales de acceso | `DEC-GOB-020` | Resuelta conceptualmente |
| `PREG-P-12` | Información registrada | `DEC-GOB-020` | Resuelta conceptualmente |
| `PREG-P-13` | Criterios de aceptación | `DEC-GOB-021` | Resuelta conceptualmente |
| `PREG-P-14` | Niveles de validación | `DEC-GOB-021` | Resuelta conceptualmente |
| `PREG-P-15` | Documentación y soporte | `DEC-GOB-021` | Resuelta conceptualmente |

### 6.2. Preguntas técnicas derivadas que permanecen abiertas

Las decisiones anteriores resuelven el marco conceptual, pero no especifican los valores, interfaces, arquitecturas ni procedimientos necesarios para implementar y verificar. B2.3 resolvió conceptualmente la familia inicial y el alcance funcional del primer incremento; los detalles técnicos asociados permanecen abiertos. Permanecen abiertos, al menos:

1. **Modelo, parámetros y electrónica del motor DC del primer incremento.** La familia está definida como motores DC con escobillas; el modelo, la tensión, la corriente, la potencia y la electrónica de potencia permanecen pendientes. Derivado de `D01`, `D19` y `D25` (`DEC-GOB-022`, `DEC-GOB-028`).
2. **Prestaciones cuantitativas de control, supervisión y diagnóstico.** Derivada de `PREG-P-13` y `DEC-GOB-021`.
3. **Condiciones eléctricas, ambientales y de instalación cuantitativas.** Derivada de `PREG-P-06` y `DEC-GOB-018`.
4. **Interfaces, protocolos y sistemas externos concretos.** Derivada de `PREG-P-10` y `DEC-GOB-020`; los principios de desacoplamiento y versionado están aprobados, pero las interfaces concretas no.
5. **Arquitectura de seguridad, funciones de seguridad y estados seguros por aplicación.** Derivada de `PREG-P-01`, `PREG-P-02`, `PREG-P-03` y `DEC-GOB-017`; las respuestas ante fallas están condicionadas por riesgos.
6. **Métodos de verificación, criterios de aceptación cuantitativos y entorno de pruebas.** Derivada de `PREG-P-13`, `PREG-P-14` y `DEC-GOB-021`; la estrategia conceptual está aprobada, pero los procedimientos y valores no.
7. **Límites cuantitativos, interfaces, medidas de protección y criterios de aceptación del primer incremento.** El alcance funcional está delimitado por `D25` (`DEC-GOB-022`); estos detalles permanecen abiertos. Derivado de `PREG-P-07`, `PREG-P-08`, `PREG-P-09` y `DEC-GOB-019`.
8. **Autenticación, matriz detallada de permisos, retención y almacenamiento de información.** Derivada de `PREG-P-11`, `PREG-P-12` y `DEC-GOB-020`; los perfiles están aprobados, pero los mecanismos no.

Estos asuntos no constituyen decisiones aprobadas. Deberán resolverse antes de implementar el alcance afectado.

## 7. Trazabilidad

| Necesidad | Visión | Actores | Escenarios | Decisiones | Preguntas de origen |
|---|---|---|---|---|---|
| `NEC-P-01` | Secciones 1 y 7 | `ACT-P-01`, `ACT-P-02` | `ESC-P-03` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-019` | `PREG-P-04`, `PREG-P-05`, `PREG-P-07` |
| `NEC-P-02` | Secciones 5 y 7 | `ACT-P-02`, `ACT-P-03`, `ACT-P-04` | `ESC-P-03`, `ESC-P-04` | `DEC-GOB-016`, `DEC-GOB-019`, `DEC-GOB-020` | `PREG-P-07`, `PREG-P-09`, `PREG-P-12` |
| `NEC-P-03` | Secciones 5, 7 y 9 | `ACT-P-02`, `ACT-P-05` | `ESC-P-04`, `ESC-P-05` | `DEC-GOB-016`, `DEC-GOB-019`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-09`, `PREG-P-12`, `PREG-P-13` |
| `NEC-P-04` | Secciones 5 y 7 | `ACT-P-01`, `ACT-P-02` | `ESC-P-01`, `ESC-P-02` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-019`, `DEC-GOB-020` | `PREG-P-04`, `PREG-P-09`, `PREG-P-11` |
| `NEC-P-05` | Secciones 5, 9 y 12 | `ACT-P-02`, `ACT-P-05`, `ACT-P-06` | `ESC-P-07`, `ESC-P-10` | `DEC-GOB-016`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-11`, `PREG-P-13`, `PREG-P-15` |
| `NEC-P-06` | Secciones 2, 7 y 9 | `ACT-P-01`, `ACT-P-07` | `ESC-P-08` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-020` | `PREG-P-04`, `PREG-P-10`, `PREG-P-11` |
| `NEC-P-07` | Secciones 9 y 12 | `ACT-P-03`, `ACT-P-04`, `ACT-P-05` | `ESC-P-03`, `ESC-P-06`, `ESC-P-09` | `DEC-GOB-016`, `DEC-GOB-017`, `DEC-GOB-018` | `PREG-P-01`, `PREG-P-03`, `PREG-P-06` |
| `NEC-P-08` | Secciones 9, 11 y 12 | Todos | `ESC-P-06`, `ESC-P-09` | `DEC-GOB-016`, `DEC-GOB-017` | `PREG-P-01`, `PREG-P-02`, `PREG-P-03` |
| `NEC-P-09` | Secciones 9 y 12 | `ACT-P-04`, `ACT-P-05` | `ESC-P-04`, `ESC-P-05`, `ESC-P-09` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-021` | `PREG-P-06`, `PREG-P-13`, `PREG-P-14` |
| `NEC-P-10` | Secciones 5 y 12 | `ACT-P-01`, `ACT-P-02`, `ACT-P-06`, `ACT-P-07` | `ESC-P-01`, `ESC-P-07`, `ESC-P-10` | `DEC-GOB-016`, `DEC-GOB-021` | `PREG-P-13`, `PREG-P-14`, `PREG-P-15` |

Estos vínculos son de trazabilidad documental. No constituyen requisitos aprobados ni una matriz de trazabilidad de requisitos.

Las decisiones `DEC-GOB-022` a `DEC-GOB-030` se relacionan con estas necesidades a través de la matriz de `docs/06-decisiones/consolidacion-decisiones-B2.3.md`. Esa matriz es de trazabilidad conceptual y no crea requisitos.

## 8. Pendientes

- Las diez necesidades están aprobadas (DEC-GOB-016).
- Las quince preguntas de B2.2.1 fueron resueltas conceptualmente (DEC-GOB-017 a DEC-GOB-021).
- Las decisiones conceptuales de B2.3 fueron consolidadas en `DEC-GOB-022` a `DEC-GOB-030`.
- Permanecen abiertas las preguntas técnicas derivadas de la sección 6.2.
- No se han asignado identificadores `RF-###`, `RNF-###` o `RES-###`.
- No se han definido requisitos concretos ni una línea base de requisitos.
- Las preguntas técnicas pendientes se registran en `docs/06-decisiones/pendientes.md`.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md` (secciones 24, 25 y 26)
- `docs/00-gobierno/criterios-calidad.md` (secciones 3 y 13)
- `docs/00-gobierno/definicion-de-terminado.md` (sección 7)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/01-requisitos/escenarios-uso.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.2.1:** identificación inicial de necesidades candidatas y preguntas abiertas. Propuesta pendiente de validación y aprobación.
- **0.2 — 2026-10-20 — B2.2.2:** aprobación de las diez necesidades (DEC-GOB-016); resolución conceptual de `PREG-P-01` a `PREG-P-15` (DEC-GOB-017 a DEC-GOB-021); incorporación de las preguntas técnicas derivadas que permanecen abiertas.
- **0.3 — 2026-10-20 — B2.3:** actualización de las referencias de estado afectadas por `DEC-GOB-022` a `DEC-GOB-030`; precisión de la familia inicial y del alcance funcional del primer incremento. Las necesidades y las decisiones anteriores no se modifican. Versión pendiente de aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
