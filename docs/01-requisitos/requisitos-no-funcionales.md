# Requisitos no funcionales — ControlCore

**Proyecto:** ControlCore
**Empresa:** makeAutomatic
**Tipo de proyecto:** Desarrollo de producto industrial comercial
**Documento:** Requisitos no funcionales
**Versión:** 0.2
**Estado:** Revisión de documento aprobado — propuesta de requisitos candidatos
**Fase:** Ingeniería de requisitos
**Fecha de revisión:** 2026-10-20
**Aprobación:** Versión 0.1 aprobada el 2026-10-19 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.2 pendiente de aprobación

---

## 1. Propósito

Este documento constituye el registro de los requisitos no funcionales candidatos de ControlCore para el primer incremento.

Los requisitos no funcionales describen atributos medibles de calidad, comportamiento o restricción interna que el producto deberá satisfacer en condiciones definidas.

## 2. Alcance

Este registro comprende exclusivamente requisitos no funcionales identificados con el prefijo `RNF-###`.

No comprende requisitos funcionales ni restricciones externas, que se registran en:

- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`

Los requisitos de este documento son **candidatos propuestos**. No constituyen una línea base, no están aprobados y no autorizan implementación.

## 3. Convenciones

Se aplican las convenciones comunes de `docs/01-requisitos/README.md` (sección 3).

- Prefijo: `RNF-###`.
- El identificador es único, estable y no reutilizable.
- La versión del contenido es independiente del identificador.
- No se asigna un identificador hasta que exista un requisito no funcional definido y registrado.
- Se aplican las convenciones de prioridad y trazabilidad de `docs/01-requisitos/README.md` (secciones 3 y 5).
- La versión de este documento es independiente de la versión de cada requisito individual.
- Las referencias documentales utilizan rutas relativas a la raíz del repositorio.

## 4. Atributos comunes de los candidatos

Todos los candidatos de este documento tienen:

- **Tipo:** `RNF`.
- **Estado:** Propuesto.
- **Versión:** 0.1.
- **Prioridad:** Pendiente de determinar.
- **Evidencia de verificación:** Pendiente.
- **Responsable de aprobación:** Responsable del proyecto.

La verificabilidad se indica en cada ficha. Un requisito con criterio incompleto no se declara verificable ni aprobable.

## 5. Índice de requisitos candidatos

| Identificador | Título | Atributo de calidad | Origen | Verificabilidad |
|---|---|---|---|---|
| RNF-001 | Estabilidad y desempeño del lazo de velocidad | Desempeño y estabilidad | D51; D52; D53; D54 | Parcial — métricas pendientes |
| RNF-002 | Integridad y recuperabilidad de la configuración | Integridad y recuperabilidad | D55; D56 | Parcial — mecanismo pendiente |
| RNF-003 | Integridad y trazabilidad de la auditoría | Auditabilidad | D58 | Parcial — mecanismo pendiente |
| RNF-004 | Control de acceso a parámetros críticos | Seguridad de configuración | D57; D59 | Parcial — autenticación pendiente |
| RNF-005 | Detección de fallas internas y disponibilidad de protecciones | Confiabilidad | D32 | Parcial — cobertura pendiente |

## 6. Requisitos candidatos

### RNF-001 — Estabilidad y desempeño del lazo de velocidad

- **Descripción verificable:** El lazo de velocidad deberá cumplir criterios definidos de estabilidad, error de seguimiento, tiempo de respuesta, sobreimpulso, oscilaciones y respuesta ante cambios de carga, en condiciones de operación especificadas.
- **Justificación:** Asegurar que el control PI no solo funcione, sino que mantenga un comportamiento estable y predecible.
- **Origen:** B2.4-D51; B2.4-D52; B2.4-D53; B2.4-D54.
- **Decisiones relacionadas:** B2.3-D26; B2.3-D35; `DEC-GOB-023`; `DEC-GOB-021`.
- **Dependencias:** RF-009; RF-010; RF-011; RF-013.
- **Riesgos relacionados:** HZ-004.
- **Condiciones de aplicación:** Lazo cerrado, referencias representativas, cambios de carga y perturbaciones controladas.
- **Criterio de aceptación:** Los criterios de estabilidad, error, respuesta, sobreimpulso y oscilación se cumplen en las condiciones aprobadas. Métricas, valores y tolerancias pendientes.
- **Método de verificación:** Análisis, simulación y prueba con cargas y referencias representativas.
- **Verificabilidad:** Parcial — faltan métricas y valores.
- **Pendientes técnicos:** Definir métricas, valores, tolerancias, condiciones de carga y criterios de estabilidad.

### RNF-002 — Integridad y recuperabilidad de la configuración

- **Descripción verificable:** La configuración deberá almacenarse con comprobaciones de integridad y permitir la recuperación de una configuración válida cuando la configuración activa sea inválida o esté corrupta.
- **Justificación:** Evitar que una falla de almacenamiento o una configuración inválida impida una operación segura.
- **Origen:** B2.4-D55; B2.4-D56.
- **Decisiones relacionadas:** B2.3-D36; `DEC-GOB-026`.
- **Dependencias:** RF-023; RF-024.
- **Riesgos relacionados:** HZ-017.
- **Condiciones de aplicación:** Guardado, carga, actualización y recuperación de configuración.
- **Criterio de aceptación:** La corrupción o invalidez se detecta; existe una configuración válida recuperable; la recuperación no habilita el motor sin verificar condiciones de seguridad. Mecanismo pendiente.
- **Método de verificación:** Inspección y prueba con corrupción e invalidez inducidas.
- **Verificabilidad:** Parcial — falta el mecanismo de integridad.
- **Pendientes técnicos:** Definir mecanismo de integridad, versionado, respaldo y recuperación.

### RNF-003 — Integridad y trazabilidad de la auditoría

- **Descripción verificable:** Los registros de cambios de configuración deberán ser completos, ordenados, atribuibles y protegidos contra alteraciones no detectadas, de modo que permitan reconstruir el historial.
- **Justificación:** Sostener la trazabilidad de cambios que afectan el comportamiento del sistema.
- **Origen:** B2.4-D58.
- **Decisiones relacionadas:** B2.3-D42; `DEC-GOB-026`.
- **Dependencias:** RF-026.
- **Riesgos relacionados:** HZ-017.
- **Condiciones de aplicación:** Todo cambio de configuración y toda consulta del historial.
- **Criterio de aceptación:** Cada registro contiene los campos exigidos; el historial es reconstruible; las alteraciones no detectadas se evitan o se detectan. Mecanismo pendiente.
- **Método de verificación:** Inspección de registros y prueba de integridad.
- **Verificabilidad:** Parcial — falta el mecanismo de protección.
- **Pendientes técnicos:** Definir formato, orden, protección de integridad, retención y consulta.

### RNF-004 — Control de acceso a parámetros críticos

- **Descripción verificable:** Solo los perfiles autorizados podrán modificar parámetros críticos, y todo cambio deberá quedar registrado y sujeto a las condiciones operativas aprobadas.
- **Justificación:** Evitar cambios no autorizados que alteren el comportamiento seguro del sistema.
- **Origen:** B2.4-D57; B2.4-D59.
- **Decisiones relacionadas:** B2.3-D15; `DEC-GOB-020`; `DEC-GOB-026`.
- **Dependencias:** RF-025; RNF-003.
- **Riesgos relacionados:** HZ-017; HZ-023.
- **Condiciones de aplicación:** Cambio de parámetros críticos y acceso a funciones de configuración.
- **Criterio de aceptación:** Los cambios no autorizados son rechazados y registrados; los cambios autorizados cumplen las condiciones operativas. Mecanismo de autenticación y matriz de permisos pendientes.
- **Método de verificación:** Inspección y prueba con perfiles autorizados y no autorizados.
- **Verificabilidad:** Parcial — faltan autenticación y matriz de permisos.
- **Pendientes técnicos:** Definir perfiles, autenticación, permisos y condiciones de cambio.

### RNF-005 — Detección de fallas internas y disponibilidad de protecciones

- **Descripción verificable:** El sistema deberá detectar fallas internas del controlador que puedan afectar funciones de control o protección y aplicar una respuesta acorde con su criticidad.
- **Justificación:** Evitar que una falla interna elimine silenciosamente funciones necesarias para la seguridad.
- **Origen:** B2.4-D32.
- **Decisiones relacionadas:** B2.3-D38; B2.3-D47; `DEC-GOB-024`.
- **Dependencias:** RF-020.
- **Riesgos relacionados:** HZ-016.
- **Condiciones de aplicación:** Operación normal y condiciones anómalas del controlador.
- **Criterio de aceptación:** Las clases de falla detectables se detectan y la respuesta aprobada se ejecuta; las funciones de protección requeridas permanecen disponibles o el sistema pasa a un estado seguro definido. Cobertura y tiempos pendientes.
- **Método de verificación:** Análisis, simulación de fallas y prueba controlada.
- **Verificabilidad:** Parcial — faltan cobertura y tiempos.
- **Pendientes técnicos:** Definir clases de falla, cobertura, tiempos y estado seguro.

## 7. Trazabilidad

| Requisito | Decisiones B2.4 | Decisiones B2.3 | Peligros | Verificación |
|---|---|---|---|---|
| RNF-001 | D51; D52; D53; D54 | B2.3-D26; B2.3-D35 | HZ-004 | Análisis y prueba |
| RNF-002 | D55; D56 | B2.3-D36 | HZ-017 | Inspección y prueba |
| RNF-003 | D58 | B2.3-D42 | HZ-017 | Inspección |
| RNF-004 | D57; D59 | B2.3-D15 | HZ-017; HZ-023 | Inspección y prueba |
| RNF-005 | D32 | B2.3-D38; B2.3-D47 | HZ-016 | Análisis y prueba |

## 8. Pendientes

- Todos los requisitos son candidatos y están en estado **Propuesto**.
- Las prioridades no están determinadas.
- Los valores cuantitativos y las métricas no están definidos.
- Varios criterios de aceptación están incompletos y por ello no se declaran verificables.
- No existe línea base de requisitos no funcionales.
- La aprobación corresponde al responsable del proyecto.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/01-requisitos/escenarios-uso.md`
- `docs/03-seguridad-industrial/analisis-riesgos.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.4.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** estructura inicial del registro de requisitos no funcionales. Sin requisitos definidos.
- **0.1 — 2026-10-19 — B2.1.1:** aprobación de la estructura y de la línea base de gestión de requisitos (DEC-GOB-010 a DEC-GOB-015).
- **0.2 — 2026-10-20 — B2.4:** incorporación de cinco requisitos no funcionales candidatos y trazabilidad a D01–D60. Ningún requisito aprobado.
