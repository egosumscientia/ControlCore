# Actores y uso — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Actores y uso  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto

---

## 1. Propósito

Este documento identifica los actores previstos de ControlCore, sus responsabilidades potenciales, sus necesidades, sus interacciones posibles y los aspectos que requieren confirmación.

Su finalidad es servir de base para validar las necesidades del producto y los escenarios de uso antes de definir requisitos concretos.

## 2. Alcance

Este documento comprende actores y responsabilidades potenciales derivados de la visión aprobada.

No define roles de acceso, permisos, interfaces, protocolos ni procedimientos definitivos.

Los identificadores `ACT-P-###` son provisionales de B2.2.1. No constituyen un esquema permanente ni reutilizan identificadores `RF-###`, `RNF-###` o `RES-###`.

## 3. Fuente y clasificación

La fuente principal es `docs/00-gobierno/vision-producto.md` (sección 6). Se consultaron además los documentos de gobierno y la estructura de gestión de requisitos.

Las afirmaciones se clasifican como:

- **Hecho documentado:** actor o responsabilidad mencionados en la visión aprobada.
- **Necesidad potencial:** necesidad atribuida al actor a partir de su responsabilidad prevista; requiere validación.
- **Interacción posible:** uso o relación hipotética con ControlCore; no define una interfaz.
- **Aspecto por confirmar:** rol, permiso, procedimiento o límite que requiere decisión.

Ningún actor, responsabilidad o permiso está aprobado por este documento.

## 4. Actores identificados

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

- **Responsabilidades previstas:** incorporar ControlCore en máquinas o sistemas industriales; definir el contexto de integración; coordinar la puesta en servicio con el cliente o usuario final.
- **Necesidades potenciales:** `NEC-P-01`, `NEC-P-04`, `NEC-P-06`, `NEC-P-10`.
- **Interacciones posibles:** configuración inicial, puesta en servicio, integración con sistemas existentes y soporte de operación.
- **Información necesaria:** requisitos de la aplicación, condiciones de la máquina, sistemas externos, condiciones de instalación y documentación técnica.
- **Riesgos o limitaciones:** límites de responsabilidad entre ControlCore y la máquina; interfaces externas no definidas; condiciones de instalación desconocidas.
- **Aspectos por confirmar:** alcance de integración, interfaces, responsabilidades, condiciones de instalación y permisos de operación.

### ACT-P-02 — Ingenieros y técnicos

- **Responsabilidades previstas:** configuración, diagnóstico, pruebas, ajuste y soporte técnico durante el ciclo de vida.
- **Necesidades potenciales:** `NEC-P-01`, `NEC-P-02`, `NEC-P-03`, `NEC-P-04`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10`.
- **Interacciones posibles:** configuración, supervisión, diagnóstico, mantenimiento, actualización y verificación.
- **Información necesaria:** parámetros, estados, fallas, registros, versiones, procedimientos y documentación.
- **Riesgos o limitaciones:** diagnóstico insuficiente; procedimientos no definidos; acceso a información sensible; compatibilidad entre versiones.
- **Aspectos por confirmar:** funciones habilitadas, permisos, formación requerida y procedimientos de operación y mantenimiento.

### ACT-P-03 — Operador de planta

- **Responsabilidades previstas:** operar las funciones definidas para cada aplicación y responder a las condiciones indicadas por los procedimientos de la planta.
- **Necesidades potenciales:** `NEC-P-02`, `NEC-P-07`, `NEC-P-08`.
- **Interacciones posibles:** operación, supervisión y respuesta ante alarmas o condiciones anormales.
- **Información necesaria:** estado del sistema, alarmas, instrucciones de operación y límites de actuación.
- **Riesgos o limitaciones:** responsabilidades no delimitadas; formación insuficiente; comportamiento ante fallas no definido; condiciones peligrosas.
- **Aspectos por confirmar:** funciones de operación, alarmas, límites de actuación, formación y permisos.

### ACT-P-04 — Responsable de producción

- **Responsabilidades previstas:** disponibilidad, continuidad operativa, cumplimiento de los objetivos de producción y escalamiento de condiciones anormales.
- **Necesidades potenciales:** `NEC-P-02`, `NEC-P-07`, `NEC-P-09`.
- **Interacciones posibles:** supervisión del estado operativo, consulta de información de producción y coordinación ante interrupciones.
- **Información necesaria:** disponibilidad, eventos relevantes, causas de interrupción y estado de recuperación.
- **Riesgos o limitaciones:** métricas no definidas; límites de responsabilidad; información insuficiente para la toma de decisiones.
- **Aspectos por confirmar:** indicadores requeridos, expectativas de disponibilidad, responsabilidades ante fallas y procedimientos de escalamiento.

### ACT-P-05 — Responsable de mantenimiento

- **Responsabilidades previstas:** planificar y coordinar mantenimiento, diagnóstico, repuestos, actualizaciones y recuperación del sistema.
- **Necesidades potenciales:** `NEC-P-03`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10`.
- **Interacciones posibles:** diagnóstico, mantenimiento preventivo y correctivo, actualización controlada y verificación posterior.
- **Información necesaria:** historial de fallas, registros, versiones, procedimientos, repuestos y criterios de aceptación.
- **Riesgos o limitaciones:** diagnóstico incompleto; actualizaciones incompatibles; falta de repuestos; procedimientos de recuperación no definidos.
- **Aspectos por confirmar:** modelo de mantenimiento, política de actualización, evidencia requerida y responsabilidades de soporte.

### ACT-P-06 — Equipo de desarrollo de makeAutomatic

- **Responsabilidades previstas:** concepción, diseño, implementación, verificación, validación, evolución y soporte del producto.
- **Necesidades potenciales:** `NEC-P-05`, `NEC-P-09`, `NEC-P-10`.
- **Interacciones posibles:** desarrollo, configuración, diagnóstico, actualización, soporte y análisis de información de campo.
- **Información necesaria:** requisitos aprobados, arquitectura, resultados de pruebas, incidencias y retroalimentación de los actores.
- **Riesgos o limitaciones:** alcance no validado; necesidades inferidas tratadas como requisitos; criterios de aceptación insuficientes.
- **Aspectos por confirmar:** alcance de desarrollo, modelo de soporte, criterios de aceptación y responsabilidades de validación.

### ACT-P-07 — Aliados especializados

- **Responsabilidades previstas:** aportar capacidades específicas de ingeniería, fabricación, pruebas, integración o soporte.
- **Necesidades potenciales:** `NEC-P-06`, `NEC-P-10`.
- **Interacciones posibles:** integración, validación, fabricación, pruebas especializadas y soporte.
- **Información necesaria:** especificaciones, interfaces, criterios de aceptación, responsabilidades y condiciones de colaboración.
- **Riesgos o limitaciones:** responsabilidades no delimitadas; transferencia de conocimiento insuficiente; dependencia de interfaces no definidas.
- **Aspectos por confirmar:** alcance de participación, entregables, responsabilidades, interfaces y condiciones contractuales.

## 5. Interacciones y límites de responsabilidad

Las interacciones descritas son posibilidades de uso, no interfaces aprobadas.

No se definen roles de acceso ni permisos. Cualquier asignación de permisos requerirá una decisión posterior del responsable del proyecto y un análisis de riesgos cuando afecte la seguridad o la operación.

Los límites de responsabilidad entre ControlCore, la máquina, el integrador y el usuario final no están definidos. En particular, no se ha establecido qué funciones de seguridad corresponden a cada parte.

## 6. Preguntas abiertas

Las preguntas completas y priorizadas se encuentran en `docs/01-requisitos/necesidades-producto.md` (sección 6).

Las preguntas con mayor relación con este documento son:

- `PREG-P-01`: funciones y responsabilidades de seguridad.
- `PREG-P-04`: aplicaciones y procesos prioritarios.
- `PREG-P-10`: sistemas externos e información a intercambiar.
- `PREG-P-11`: actores, responsabilidades y restricciones de acceso.
- `PREG-P-13`: criterios de aceptación y evidencia.
- `PREG-P-15`: documentación y soporte técnico.

No se asume ninguna respuesta.

## 7. Trazabilidad preliminar

| Actor | Necesidades | Escenarios | Preguntas |
|---|---|---|---|
| `ACT-P-01` | `NEC-P-01`, `NEC-P-04`, `NEC-P-06`, `NEC-P-10` | `ESC-P-01`, `ESC-P-02`, `ESC-P-08` | `PREG-P-04`, `PREG-P-10`, `PREG-P-11` |
| `ACT-P-02` | `NEC-P-01` a `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-02`, `ESC-P-03`, `ESC-P-04`, `ESC-P-05`, `ESC-P-07`, `ESC-P-10` | `PREG-P-09`, `PREG-P-11`, `PREG-P-13` |
| `ACT-P-03` | `NEC-P-02`, `NEC-P-07`, `NEC-P-08` | `ESC-P-03`, `ESC-P-04`, `ESC-P-06` | `PREG-P-01`, `PREG-P-03`, `PREG-P-11` |
| `ACT-P-04` | `NEC-P-02`, `NEC-P-07`, `NEC-P-09` | `ESC-P-04`, `ESC-P-06`, `ESC-P-09` | `PREG-P-06`, `PREG-P-13` |
| `ACT-P-05` | `NEC-P-03`, `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-05`, `ESC-P-07`, `ESC-P-09`, `ESC-P-10` | `PREG-P-12`, `PREG-P-13`, `PREG-P-15` |
| `ACT-P-06` | `NEC-P-05`, `NEC-P-09`, `NEC-P-10` | `ESC-P-01`, `ESC-P-02`, `ESC-P-05`, `ESC-P-08`, `ESC-P-10` | `PREG-P-13`, `PREG-P-14`, `PREG-P-15` |
| `ACT-P-07` | `NEC-P-06`, `NEC-P-10` | `ESC-P-01`, `ESC-P-08`, `ESC-P-10` | `PREG-P-10`, `PREG-P-11`, `PREG-P-15` |

Estos vínculos son preliminares y no constituyen requisitos aprobados.

## 8. Pendientes

- Los actores, responsabilidades y permisos requieren validación y aprobación.
- Los límites de responsabilidad entre ControlCore, la máquina y los sistemas externos no están definidos.
- No se han definido roles de acceso ni permisos.
- No se han asignado identificadores `RF-###`, `RNF-###` o `RES-###`.
- Las decisiones pendientes se registran en `docs/06-decisiones/pendientes.md`.

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

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.2.1:** identificación inicial de actores y responsabilidades potenciales. Propuesta pendiente de validación y aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
