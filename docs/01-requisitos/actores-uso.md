# Actores y uso — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Actores y uso
**Versión:** 0.3
**Estado:** Revisión de documento aprobado — actualización B2.4 pendiente de aprobación
**Fase:** Ingeniería de requisitos
**Fecha de revisión:** 2026-10-20
**Aprobación:** Versión 0.2 aprobada el 2026-10-20 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.3 pendiente de aprobación

---

## 1. Propósito

Este documento identifica los actores aprobados de ControlCore, sus responsabilidades generales, sus necesidades, sus interacciones posibles y los aspectos técnicos que permanecen pendientes.

Los actores fueron propuestos en B2.2.1 y aprobados en B2.2.2. Su finalidad es servir de base para derivar requisitos concretos.

La versión 0.3 actualiza únicamente las referencias de estado afectadas por los requisitos candidatos de B2.4. No modifica los actores ni sus responsabilidades aprobadas.

## 2. Alcance

Este documento comprende los actores aprobados y sus responsabilidades generales, derivados de la visión aprobada.

No define autenticación, una matriz detallada de permisos, interfaces, protocolos ni procedimientos definitivos.

Los perfiles funcionales de acceso aprobados en `PREG-P-11` —Operador, Técnico/Integrador y Administrador técnico— son distintos de los actores organizacionales y de uso de este documento. La relación concreta entre actores y perfiles permanece pendiente.

Los identificadores `ACT-P-###` identifican los actores aprobados en este documento. No constituyen un esquema permanente ni reutilizan identificadores `RF-###`, `RNF-###` o `RES-###`.

## 3. Fuente y clasificación

La fuente principal es `docs/00-gobierno/vision-producto.md` (sección 6). Se consultaron además los documentos de gobierno y la estructura de gestión de requisitos.

Las afirmaciones se clasifican como:

- **Hecho documentado:** actor o responsabilidad mencionados en la visión aprobada.
- **Necesidad atribuida:** necesidad del actor derivada de su responsabilidad prevista; las necesidades del producto fueron aprobadas en DEC-GOB-016.
- **Interacción posible:** uso o relación hipotética con ControlCore; no define una interfaz.
- **Aspecto técnico pendiente:** rol, permiso, procedimiento o límite que requiere decisión.

Los siete actores y sus responsabilidades generales fueron aprobados el 2026-10-20 (DEC-GOB-016). La clasificación de origen se conserva como historial. La aprobación no asigna permisos ni confirma procedimientos operativos concretos.

## 4. Actores aprobados

Los siete actores de la tabla están aprobados con sus responsabilidades generales (DEC-GOB-016, 2026-10-20).

| Identificador | Actor | Necesidades principales | Escenarios principales |
|---|---|---|---|
| `ACT-P-01` | Integrador de automatización | `NEC-P-01`, `NEC-P-04`, `NEC-P-06`, `NEC-P-10` | `ESC-P-01`, `ESC-P-02`, `ESC-P-08` |
| `ACT-P-02` | Ingenieros y técnicos | `NEC-P-01` a `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-02`, `ESC-P-03`, `ESC-P-04`, `ESC-P-05`, `ESC-P-07`, `ESC-P-10` |
| `ACT-P-03` | Operador de planta | `NEC-P-02`, `NEC-P-07`, `NEC-P-08` | `ESC-P-03`, `ESC-P-04`, `ESC-P-06` |
| `ACT-P-04` | Responsable de producción | `NEC-P-02`, `NEC-P-07`, `NEC-P-09` | `ESC-P-04`, `ESC-P-06`, `ESC-P-09` |
| `ACT-P-05` | Responsable de mantenimiento | `NEC-P-03`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-05`, `ESC-P-07`, `ESC-P-09`, `ESC-P-10` |
| `ACT-P-06` | Equipo de desarrollo de makeAutomatic | `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-01`, `ESC-P-02`, `ESC-P-05`, `ESC-P-08`, `ESC-P-10` |
| `ACT-P-07` | Aliados especializados | `NEC-P-06`, `NEC-P-10` | `ESC-P-01`, `ESC-P-08`, `ESC-P-10` |

### ACT-P-01 — Integrador de automatización

- **Responsabilidades generales aprobadas:** incorporar ControlCore en máquinas o sistemas industriales; definir el contexto de integración; coordinar la puesta en servicio con el cliente o usuario final.
- **Necesidades relacionadas:** `NEC-P-01`, `NEC-P-04`, `NEC-P-06`, `NEC-P-10`.
- **Interacciones posibles (no interfaces aprobadas):** configuración inicial, puesta en servicio, integración con sistemas existentes y soporte de operación.
- **Información necesaria:** requisitos de la aplicación, condiciones de la máquina, sistemas externos, condiciones de instalación y documentación técnica.
- **Riesgos o limitaciones:** límites de responsabilidad entre ControlCore y la máquina; interfaces externas no definidas; condiciones de instalación desconocidas.
- **Aspectos técnicos pendientes:** alcance de integración, interfaces, responsabilidades, condiciones de instalación y permisos de operación.

### ACT-P-02 — Ingenieros y técnicos

- **Responsabilidades generales aprobadas:** configuración, diagnóstico, pruebas, ajuste y soporte técnico durante el ciclo de vida.
- **Necesidades relacionadas:** `NEC-P-01`, `NEC-P-02`, `NEC-P-03`, `NEC-P-04`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10`.
- **Interacciones posibles (no interfaces aprobadas):** configuración, supervisión, diagnóstico, mantenimiento, actualización y verificación.
- **Información necesaria:** parámetros, estados, fallas, registros, versiones, procedimientos y documentación.
- **Riesgos o limitaciones:** diagnóstico insuficiente; procedimientos no definidos; acceso a información sensible; compatibilidad entre versiones.
- **Aspectos técnicos pendientes:** funciones habilitadas, permisos, formación requerida y procedimientos de operación y mantenimiento.

### ACT-P-03 — Operador de planta

- **Responsabilidades generales aprobadas:** operar las funciones definidas para cada aplicación y responder a las condiciones indicadas por los procedimientos de la planta.
- **Necesidades relacionadas:** `NEC-P-02`, `NEC-P-07`, `NEC-P-08`.
- **Interacciones posibles (no interfaces aprobadas):** operación, supervisión y respuesta ante alarmas o condiciones anormales.
- **Información necesaria:** estado del sistema, alarmas, instrucciones de operación y límites de actuación.
- **Riesgos o limitaciones:** responsabilidades no delimitadas; formación insuficiente; comportamiento ante fallas no definido; condiciones peligrosas.
- **Aspectos técnicos pendientes:** funciones de operación, alarmas, límites de actuación, formación y permisos.

### ACT-P-04 — Responsable de producción

- **Responsabilidades generales aprobadas:** disponibilidad, continuidad operativa, cumplimiento de los objetivos de producción y escalamiento de condiciones anormales.
- **Necesidades relacionadas:** `NEC-P-02`, `NEC-P-07`, `NEC-P-09`.
- **Interacciones posibles (no interfaces aprobadas):** supervisión del estado operativo, consulta de información de producción y coordinación ante interrupciones.
- **Información necesaria:** disponibilidad, eventos relevantes, causas de interrupción y estado de recuperación.
- **Riesgos o limitaciones:** métricas no definidas; límites de responsabilidad; información insuficiente para la toma de decisiones.
- **Aspectos técnicos pendientes:** indicadores requeridos, expectativas de disponibilidad, responsabilidades ante fallas y procedimientos de escalamiento.

### ACT-P-05 — Responsable de mantenimiento

- **Responsabilidades generales aprobadas:** planificar y coordinar mantenimiento, diagnóstico, repuestos, actualizaciones y recuperación del sistema.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10`.
- **Interacciones posibles (no interfaces aprobadas):** diagnóstico, mantenimiento preventivo y correctivo, actualización controlada y verificación posterior.
- **Información necesaria:** historial de fallas, registros, versiones, procedimientos, repuestos y criterios de aceptación.
- **Riesgos o limitaciones:** diagnóstico incompleto; actualizaciones incompatibles; falta de repuestos; procedimientos de recuperación no definidos.
- **Aspectos técnicos pendientes:** modelo de mantenimiento, política de actualización, evidencia requerida y responsabilidades de soporte.

### ACT-P-06 — Equipo de desarrollo de makeAutomatic

- **Responsabilidades generales aprobadas:** concepción, diseño, implementación, verificación, validación, evolución y soporte del producto.
- **Necesidades relacionadas:** `NEC-P-05`, `NEC-P-09`, `NEC-P-10`.
- **Interacciones posibles (no interfaces aprobadas):** desarrollo, configuración, diagnóstico, actualización, soporte y análisis de información de campo.
- **Información necesaria:** requisitos aprobados, arquitectura, resultados de pruebas, incidencias y retroalimentación de los actores.
- **Riesgos o limitaciones:** alcance no validado; necesidades inferidas tratadas como requisitos; criterios de aceptación insuficientes.
- **Aspectos técnicos pendientes:** alcance de desarrollo, modelo de soporte, criterios de aceptación y responsabilidades de validación.

### ACT-P-07 — Aliados especializados

- **Responsabilidades generales aprobadas:** aportar capacidades específicas de ingeniería, fabricación, pruebas, integración o soporte.
- **Necesidades relacionadas:** `NEC-P-06`, `NEC-P-10`.
- **Interacciones posibles (no interfaces aprobadas):** integración, validación, fabricación, pruebas especializadas y soporte.
- **Información necesaria:** especificaciones, interfaces, criterios de aceptación, responsabilidades y condiciones de colaboración.
- **Riesgos o limitaciones:** responsabilidades no delimitadas; transferencia de conocimiento insuficiente; dependencia de interfaces no definidas.
- **Aspectos técnicos pendientes:** alcance de participación, entregables, responsabilidades, interfaces y condiciones contractuales.

## 5. Interacciones, perfiles funcionales y límites de responsabilidad

Las interacciones descritas son posibilidades de uso, no interfaces aprobadas.

Se aprobaron tres perfiles funcionales de acceso —Operador, Técnico/Integrador y Administrador técnico— con responsabilidades diferenciadas (`PREG-P-11`, `DEC-GOB-020`). No se ha seleccionado el mecanismo de autenticación ni una matriz detallada de permisos. Los controles de acceso no sustituyen las protecciones industriales.

| Perfil funcional | Responsabilidad general | Asignación a actores |
|---|---|---|
| Operador | Operación dentro de las funciones definidas para la aplicación. | Pendiente. |
| Técnico/Integrador | Configuración, integración, diagnóstico y soporte técnico. | Pendiente. |
| Administrador técnico | Administración técnica del sistema. | Pendiente. |

Los actores `ACT-P-01` a `ACT-P-07` son actores organizacionales y de uso; no son equivalentes a los perfiles funcionales. La asignación concreta de perfiles a actores y los permisos asociados permanecen pendientes.

`PREG-P-01` (`DEC-GOB-017`) aprobó que ControlCore será responsable de las funciones de control y diagnóstico expresamente especificadas y validadas, y que no sustituirá automáticamente los sistemas de protección de las máquinas. La delimitación documental de responsabilidades entre makeAutomatic, los fabricantes de máquinas y los integradores es obligatoria. La asignación concreta por aplicación continúa pendiente.

## 6. Decisiones aprobadas y preguntas técnicas derivadas

### 6.1. Decisiones aprobadas

Las quince preguntas de B2.2.1 fueron resueltas conceptualmente (DEC-GOB-017 a DEC-GOB-021). Las de mayor relación con este documento son:

| Pregunta | Asunto | Decisión |
|---|---|---|
| `PREG-P-01` | Funciones y responsabilidades de seguridad | `DEC-GOB-017` |
| `PREG-P-04` | Aplicaciones y procesos prioritarios | `DEC-GOB-018` |
| `PREG-P-10` | Sistemas externos e información a intercambiar | `DEC-GOB-020` |
| `PREG-P-11` | Perfiles funcionales y restricciones de acceso | `DEC-GOB-020` |
| `PREG-P-13` | Criterios de aceptación y evidencia | `DEC-GOB-021` |
| `PREG-P-15` | Documentación y soporte técnico | `DEC-GOB-021` |

### 6.2. Preguntas técnicas derivadas que permanecen abiertas

1. Asignación concreta de los perfiles funcionales a los actores y matriz detallada de permisos. Derivada de `PREG-P-11` y `DEC-GOB-020`.
2. Mecanismo de autenticación y control de acceso. Derivado de `PREG-P-11` y `DEC-GOB-020`.
3. Interfaces, protocolos y sistemas externos concretos. Derivados de `PREG-P-10` y `DEC-GOB-020`.
4. Límites de responsabilidad por aplicación entre ControlCore, la máquina, el integrador y el usuario final. Derivados de `PREG-P-01` y `DEC-GOB-017`.
5. Criterios de aceptación y evidencia específicos por actor. Derivados de `PREG-P-13` y `DEC-GOB-021`.
6. Formación, procedimientos operativos y documentación específica por actor. Derivados de `PREG-P-15` y `DEC-GOB-021`.

Estos asuntos no constituyen decisiones aprobadas. Deberán resolverse antes de implementar el alcance afectado.

## 7. Trazabilidad

| Actor | Necesidades | Escenarios | Decisiones | Preguntas de origen |
|---|---|---|---|---|
| `ACT-P-01` | `NEC-P-01`, `NEC-P-04`, `NEC-P-06`, `NEC-P-10` | `ESC-P-01`, `ESC-P-02`, `ESC-P-08` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-04`, `PREG-P-10`, `PREG-P-11` |
| `ACT-P-02` | `NEC-P-01` a `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-02`, `ESC-P-03`, `ESC-P-04`, `ESC-P-05`, `ESC-P-07`, `ESC-P-10` | `DEC-GOB-016`, `DEC-GOB-019`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-09`, `PREG-P-11`, `PREG-P-13` |
| `ACT-P-03` | `NEC-P-02`, `NEC-P-07`, `NEC-P-08` | `ESC-P-03`, `ESC-P-04`, `ESC-P-06` | `DEC-GOB-016`, `DEC-GOB-017`, `DEC-GOB-020` | `PREG-P-01`, `PREG-P-03`, `PREG-P-11` |
| `ACT-P-04` | `NEC-P-02`, `NEC-P-07`, `NEC-P-09` | `ESC-P-04`, `ESC-P-06`, `ESC-P-09` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-021` | `PREG-P-06`, `PREG-P-13` |
| `ACT-P-05` | `NEC-P-03`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-05`, `ESC-P-07`, `ESC-P-09`, `ESC-P-10` | `DEC-GOB-016`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-12`, `PREG-P-13`, `PREG-P-15` |
| `ACT-P-06` | `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-01`, `ESC-P-02`, `ESC-P-05`, `ESC-P-08`, `ESC-P-10` | `DEC-GOB-016`, `DEC-GOB-021` | `PREG-P-13`, `PREG-P-14`, `PREG-P-15` |
| `ACT-P-07` | `NEC-P-06`, `NEC-P-10` | `ESC-P-01`, `ESC-P-08`, `ESC-P-10` | `DEC-GOB-016`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-10`, `PREG-P-11`, `PREG-P-15` |

Estos vínculos son de trazabilidad documental. No constituyen requisitos aprobados ni una asignación de permisos.

## 8. Pendientes

- Los siete actores y sus responsabilidades generales están aprobados (DEC-GOB-016).
- Los tres perfiles funcionales de acceso están aprobados (DEC-GOB-020); la autenticación, la matriz detallada de permisos y su asignación a actores permanecen pendientes.
- Los límites de responsabilidad por aplicación entre ControlCore, la máquina y los sistemas externos permanecen pendientes de delimitación concreta.
- Las preguntas técnicas derivadas de la sección 6.2 permanecen abiertas.
- B2.4 propuso 39 requisitos candidatos `RF-###`, `RNF-###` y `RES-###`; ninguno está aprobado.
- Las preguntas técnicas pendientes se registran en `docs/06-decisiones/pendientes.md`.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/vision-producto.md` (secciones 6, 9 y 12)
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md` (secciones 24, 25 y 26)
- `docs/00-gobierno/criterios-calidad.md` (secciones 3 y 13)
- `docs/00-gobierno/definicion-de-terminado.md` (sección 7)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/escenarios-uso.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.4.md`
- `docs/03-seguridad-industrial/analisis-riesgos.md`

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.2.1:** identificación inicial de actores y responsabilidades potenciales. Propuesta pendiente de validación y aprobación.
- **0.2 — 2026-10-20 — B2.2.2:** aprobación de los siete actores y sus responsabilidades generales (DEC-GOB-016); incorporación de los perfiles funcionales de acceso de `PREG-P-11` (DEC-GOB-020) y de las preguntas técnicas derivadas.
- **0.3 — 2026-10-20 — B2.4:** actualización de la referencia de estado sobre identificadores candidatos. Los actores y sus responsabilidades no se modifican. Versión pendiente de aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
