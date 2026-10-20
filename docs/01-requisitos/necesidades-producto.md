# Necesidades del producto — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Necesidades del producto  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto

---

## 1. Propósito

Este documento identifica necesidades candidatas de los usuarios y del producto a partir de la visión aprobada y de los documentos de gobierno de ControlCore.

Su finalidad es proporcionar una base trazable para la validación con los actores y para la posterior definición de requisitos, sin convertir posibilidades conceptuales en requisitos obligatorios.

## 2. Alcance

Este documento comprende necesidades candidatas, hipótesis de aplicación y preguntas abiertas relacionadas con el control, la supervisión, el diagnóstico y la operación industrial de motores y actuadores.

No contiene requisitos funcionales, no funcionales o restricciones aprobadas. No selecciona tecnologías, componentes, protocolos ni arquitecturas.

Los identificadores `NEC-P-###` y `PREG-P-###` son provisionales de B2.2.1. No constituyen el esquema permanente de requisitos ni se reutilizan como identificadores `RF-###`, `RNF-###` o `RES-###`.

## 3. Fuente y clasificación de afirmaciones

La fuente principal es `docs/00-gobierno/vision-producto.md`. Se consultaron además los cinco documentos de gobierno aprobados y la estructura de gestión de requisitos.

Las afirmaciones se clasifican así:

- **Hecho documentado:** establecido explícitamente en un documento aprobado.
- **Necesidad inferida:** derivada de la visión o del alcance conceptual, pero no validada con los actores.
- **Hipótesis de aplicación:** supone un contexto, una aplicación o una interacción todavía no aprobada.
- **Pregunta abierta:** requiere una decisión o confirmación del responsable del proyecto.
- **Alternativa no seleccionada:** opción considerada que no ha sido aprobada.

Ninguna necesidad de este documento está aprobada. Todas requieren validación y, cuando corresponda, decisión del responsable del proyecto.

## 4. Necesidades candidatas

| Identificador | Necesidad candidata | Actores principales | Clasificación |
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

### NEC-P-01 — Control de motores y actuadores

- **Descripción:** necesidad de disponer de una base para comandar y coordinar motores y actuadores en aplicaciones industriales.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-02`.
- **Problema que busca resolver:** implementar soluciones de control de movimiento y actuación adaptadas a distintas máquinas y procesos.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 1 y 7).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-04`, `PREG-P-05`, `PREG-P-07`.

### NEC-P-02 — Supervisión de la operación

- **Descripción:** necesidad de conocer el estado del sistema, las condiciones de operación y las alarmas relevantes.
- **Actores relacionados:** `ACT-P-02`, `ACT-P-03`, `ACT-P-04`.
- **Problema que busca resolver:** operar con información suficiente y detectar desviaciones.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5 y 7).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-07`, `PREG-P-09`, `PREG-P-12`.

### NEC-P-03 — Diagnóstico de condiciones anormales

- **Descripción:** necesidad de identificar fallas, sus posibles causas y la información necesaria para la corrección.
- **Actores relacionados:** `ACT-P-02`, `ACT-P-05`.
- **Problema que busca resolver:** reducir el tiempo de diagnóstico y facilitar la recuperación del sistema.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5, 7 y 9).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-09`, `PREG-P-12`, `PREG-P-13`.

### NEC-P-04 — Configuración y puesta en servicio

- **Descripción:** necesidad de adaptar el sistema a cada aplicación y verificar su puesta en servicio.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-02`.
- **Problema que busca resolver:** configurar la solución de forma controlada y comprobar que está lista para operar.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5 y 7).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-04`, `PREG-P-09`, `PREG-P-11`.

### NEC-P-05 — Mantenimiento y actualización controlada

- **Descripción:** necesidad de mantener, actualizar y restaurar el sistema sin perder trazabilidad ni comprometer la operación.
- **Actores relacionados:** `ACT-P-02`, `ACT-P-05`, `ACT-P-06`.
- **Problema que busca resolver:** preservar la operación y la compatibilidad durante el ciclo de vida.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5, 9 y 12).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-11`, `PREG-P-13`, `PREG-P-15`.

### NEC-P-06 — Integración con máquinas y sistemas externos

- **Descripción:** necesidad de intercambiar información y coordinar la operación con máquinas y sistemas existentes.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-07`.
- **Problema que busca resolver:** incorporar ControlCore en entornos industriales con otros equipos y sistemas.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 2, 7 y 9).
- **Clasificación:** Hipótesis de aplicación. No se ha aprobado un conjunto de interfaces ni sistemas externos.
- **Estado de validación:** No validada. Requiere confirmación del alcance de integración.
- **Preguntas abiertas:** `PREG-P-04`, `PREG-P-10`, `PREG-P-11`.

### NEC-P-07 — Operación industrial confiable y comportamiento ante fallas

- **Descripción:** necesidad de un comportamiento predecible en operación normal y ante condiciones anormales.
- **Actores relacionados:** `ACT-P-03`, `ACT-P-04`, `ACT-P-05`.
- **Problema que busca resolver:** mantener la operación dentro de condiciones definidas y evitar respuestas improvisadas ante fallas.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 9 y 12).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-01`, `PREG-P-03`, `PREG-P-06`.

### NEC-P-08 — Seguridad y delimitación de responsabilidades

- **Descripción:** necesidad de identificar peligros, delimitar las funciones de seguridad y establecer qué responsabilidades corresponden a ControlCore y cuáles a la máquina o a sistemas externos.
- **Actores relacionados:** todos los actores; en particular `ACT-P-01`, `ACT-P-05` y el responsable del proyecto.
- **Problema que busca resolver:** evitar que una función de software se considere por sí sola una protección suficiente y evitar vacíos de responsabilidad.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 9, 11 y 12) y `docs/00-gobierno/principios-ingenieria.md` (sección 5).
- **Clasificación:** Hecho documentado en cuanto a la necesidad de considerar la seguridad; alcance, funciones y responsabilidades pendientes.
- **Estado de validación:** No validada. Requiere análisis de riesgos y decisión del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-01`, `PREG-P-02`, `PREG-P-03`.

### NEC-P-09 — Confiabilidad, disponibilidad y recuperación

- **Descripción:** necesidad de operar de forma confiable y recuperarse de forma controlada después de fallas o interrupciones.
- **Actores relacionados:** `ACT-P-04`, `ACT-P-05`.
- **Problema que busca resolver:** reducir el impacto de las interrupciones y facilitar la continuidad operativa.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 9 y 12).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-06`, `PREG-P-13`, `PREG-P-14`.

### NEC-P-10 — Documentación, verificación y soporte técnico

- **Descripción:** necesidad de disponer de documentación, criterios de verificación y soporte para instalar, operar, mantener y evolucionar el producto.
- **Actores relacionados:** `ACT-P-01`, `ACT-P-02`, `ACT-P-06`, `ACT-P-07`.
- **Problema que busca resolver:** permitir una implementación y un soporte profesional, con evidencia de aceptación.
- **Origen documental:** `docs/00-gobierno/vision-producto.md` (secciones 5 y 12) y `README.md` (sección 3).
- **Clasificación:** Necesidad inferida.
- **Estado de validación:** Pendiente de validación con actores y aprobación del responsable del proyecto.
- **Preguntas abiertas:** `PREG-P-13`, `PREG-P-14`, `PREG-P-15`.

## 5. Límites y exclusiones

### 5.1. Límites ya aprobados

La visión aprobada establece que, en la fase conceptual, no existe selección definitiva de plataforma electrónica, arquitectura de control, tipos de motores o actuadores, protocolos de comunicación, arquitectura de backend o frontend, prestaciones cuantitativas, clasificación de seguridad ni alcance comercial definitivo.

Estos límites no se resuelven en este documento.

### 5.2. Límites pendientes de determinación

| Tema | Estado | Pregunta asociada |
|---|---|---|
| Tipos de motores y actuadores | Desconocido — requiere decisión | `PREG-P-05` |
| Aplicaciones industriales prioritarias | Desconocido — requiere decisión | `PREG-P-04` |
| Alcance de la primera versión | Desconocido — requiere decisión | `PREG-P-07`, `PREG-P-08` |
| Límites de responsabilidad entre ControlCore y la máquina | Desconocido — requiere decisión | `PREG-P-01` |
| Funciones de seguridad y responsabilidades externas | Desconocido — requiere análisis y decisión | `PREG-P-01`, `PREG-P-02`, `PREG-P-03` |
| Condiciones de instalación | Desconocido — requiere validación | `PREG-P-06` |
| Interfaces con sistemas existentes | Desconocido — requiere validación | `PREG-P-10` |
| Prestaciones esperadas | Desconocido — requiere decisión | `PREG-P-13`, `PREG-P-14` |
| Requisitos regulatorios aplicables | Desconocido — requiere evaluación | `PREG-P-02` |

## 6. Preguntas abiertas priorizadas

Las preguntas siguientes requieren respuesta del responsable del proyecto. No se asume ninguna respuesta.

### 6.1. Prioridad 1 — Seguridad y alcance

| Identificador | Pregunta | Vínculos |
|---|---|---|
| `PREG-P-01` | ¿Qué funciones de seguridad y qué responsabilidades corresponden a ControlCore frente a la máquina y a los sistemas externos? | `NEC-P-08`; actores; `ESC-P-06`, `ESC-P-09` |
| `PREG-P-02` | ¿Qué análisis de riesgos y qué marco normativo deben aplicarse según el uso previsto y el mercado? | `NEC-P-08`; `ESC-P-06` |
| `PREG-P-03` | ¿Qué condiciones deben considerarse estados seguros y quién los define? | `NEC-P-07`, `NEC-P-08`; `ESC-P-06`, `ESC-P-09` |

### 6.2. Prioridad 2 — Aplicación industrial objetivo

| Identificador | Pregunta | Vínculos |
|---|---|---|
| `PREG-P-04` | ¿Qué aplicaciones, máquinas y procesos industriales son prioritarios para la primera versión? | `NEC-P-01`, `NEC-P-06`; actores |
| `PREG-P-05` | ¿Qué tipos de motores y actuadores deben considerarse en el alcance inicial? | `NEC-P-01`; `ESC-P-03` |
| `PREG-P-06` | ¿Qué condiciones eléctricas, ambientales y de instalación deben soportarse? | `NEC-P-07`, `NEC-P-09`; `ESC-P-01`, `ESC-P-03` |

### 6.3. Prioridad 3 — Capacidades de la primera versión

| Identificador | Pregunta | Vínculos |
|---|---|---|
| `PREG-P-07` | ¿Qué capacidades del alcance conceptual —control, supervisión, diagnóstico, configuración, integración y registro— forman parte de la primera versión? | `NEC-P-01` a `NEC-P-10` |
| `PREG-P-08` | ¿Qué capacidades quedan explícitamente fuera de la primera versión? | Todos los actores; `ESC-P-01` a `ESC-P-10` |
| `PREG-P-09` | ¿Qué nivel de configuración, supervisión y diagnóstico se requiere inicialmente? | `NEC-P-02`, `NEC-P-03`, `NEC-P-04`; `ESC-P-02`, `ESC-P-04`, `ESC-P-05` |

### 6.4. Prioridad 4 — Interfaces y condiciones operativas

| Identificador | Pregunta | Vínculos |
|---|---|---|
| `PREG-P-10` | ¿Con qué sistemas externos debe integrarse ControlCore y qué información debe intercambiar? | `NEC-P-06`; `ACT-P-01`, `ACT-P-07`; `ESC-P-08` |
| `PREG-P-11` | ¿Qué actores deben operar, configurar y mantener el sistema, y qué responsabilidades y restricciones de acceso deben definirse? | Actores; `ESC-P-01`, `ESC-P-02`, `ESC-P-07`, `ESC-P-10` |
| `PREG-P-12` | ¿Qué información debe registrarse y conservarse para operación, diagnóstico y auditoría? | `NEC-P-02`, `NEC-P-03`, `NEC-P-09`; `ESC-P-04`, `ESC-P-05` |

### 6.5. Prioridad 5 — Verificación y aceptación

| Identificador | Pregunta | Vínculos |
|---|---|---|
| `PREG-P-13` | ¿Qué criterios de aceptación y qué evidencia deben exigirse para la primera versión? | `NEC-P-10`; todos los escenarios |
| `PREG-P-14` | ¿Qué entorno de pruebas, banco o máquina de referencia se utilizará para verificar y validar el producto? | `NEC-P-09`, `NEC-P-10`; todos los escenarios |
| `PREG-P-15` | ¿Qué documentación y soporte técnico debe entregarse con el producto? | `NEC-P-10`; `ACT-P-02`, `ACT-P-05`, `ACT-P-07` |

## 7. Trazabilidad preliminar

| Necesidad | Visión | Actores | Escenarios | Preguntas |
|---|---|---|---|---|
| `NEC-P-01` | Secciones 1 y 7 | `ACT-P-01`, `ACT-P-02` | `ESC-P-03` | `PREG-P-04`, `PREG-P-05`, `PREG-P-07` |
| `NEC-P-02` | Secciones 5 y 7 | `ACT-P-02`, `ACT-P-03`, `ACT-P-04` | `ESC-P-03`, `ESC-P-04` | `PREG-P-07`, `PREG-P-09`, `PREG-P-12` |
| `NEC-P-03` | Secciones 5, 7 y 9 | `ACT-P-02`, `ACT-P-05` | `ESC-P-04`, `ESC-P-05` | `PREG-P-09`, `PREG-P-12`, `PREG-P-13` |
| `NEC-P-04` | Secciones 5 y 7 | `ACT-P-01`, `ACT-P-02` | `ESC-P-01`, `ESC-P-02` | `PREG-P-04`, `PREG-P-09`, `PREG-P-11` |
| `NEC-P-05` | Secciones 5, 9 y 12 | `ACT-P-02`, `ACT-P-05`, `ACT-P-06` | `ESC-P-07`, `ESC-P-10` | `PREG-P-11`, `PREG-P-13`, `PREG-P-15` |
| `NEC-P-06` | Secciones 2, 7 y 9 | `ACT-P-01`, `ACT-P-07` | `ESC-P-08` | `PREG-P-04`, `PREG-P-10`, `PREG-P-11` |
| `NEC-P-07` | Secciones 9 y 12 | `ACT-P-03`, `ACT-P-04`, `ACT-P-05` | `ESC-P-03`, `ESC-P-06`, `ESC-P-09` | `PREG-P-01`, `PREG-P-03`, `PREG-P-06` |
| `NEC-P-08` | Secciones 9, 11 y 12 | Todos | `ESC-P-06`, `ESC-P-09` | `PREG-P-01`, `PREG-P-02`, `PREG-P-03` |
| `NEC-P-09` | Secciones 9 y 12 | `ACT-P-04`, `ACT-P-05` | `ESC-P-04`, `ESC-P-05`, `ESC-P-09` | `PREG-P-06`, `PREG-P-13`, `PREG-P-14` |
| `NEC-P-10` | Secciones 5 y 12 | `ACT-P-01`, `ACT-P-02`, `ACT-P-06`, `ACT-P-07` | `ESC-P-01`, `ESC-P-07`, `ESC-P-10` | `PREG-P-13`, `PREG-P-14`, `PREG-P-15` |

Estos vínculos son preliminares y no constituyen requisitos aprobados ni una matriz de trazabilidad de requisitos.

## 8. Pendientes

- Las diez necesidades candidatas requieren validación con los actores y decisión del responsable del proyecto.
- Las quince preguntas abiertas requieren respuesta; no se asume ninguna.
- No se han asignado identificadores `RF-###`, `RNF-###` o `RES-###`.
- No se han definido requisitos concretos ni una línea base de requisitos.
- Las decisiones pendientes se registran en `docs/06-decisiones/pendientes.md`.

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

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.2.1:** identificación inicial de necesidades candidatas y preguntas abiertas. Propuesta pendiente de validación y aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
