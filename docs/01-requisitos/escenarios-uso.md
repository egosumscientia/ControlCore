# Escenarios de uso — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Escenarios de uso  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto

---

## 1. Propósito

Este documento propone escenarios representativos de utilización industrial de ControlCore.

Su finalidad es facilitar la validación de necesidades, actores y condiciones de uso antes de definir requisitos concretos.

## 2. Alcance

Este documento comprende escenarios conceptuales de puesta en servicio, configuración, operación, supervisión, diagnóstico, mantenimiento, integración, recuperación y actualización.

No especifica interfaces, protocolos, tiempos, algoritmos ni comportamientos de seguridad. No contiene requisitos aprobados.

Los identificadores `ESC-P-###` son provisionales de B2.2.1. No constituyen un esquema permanente ni reutilizan identificadores `RF-###`, `RNF-###` o `RES-###`.

## 3. Fuente y clasificación

La fuente principal es `docs/00-gobierno/vision-producto.md` (secciones 2, 5, 7, 9 y 12). Se consultaron además los documentos de gobierno y la estructura de gestión de requisitos.

Todos los escenarios se clasifican como **hipótesis de aplicación**. No han sido validados con los actores ni aprobados por el responsable del proyecto.

Las condiciones anormales se describen de forma conceptual. Cualquier comportamiento de seguridad, recuperación o parada deberá derivarse del análisis de riesgos y de decisiones posteriores.

## 4. Escenarios propuestos

| Identificador | Escenario | Actores principales | Necesidades relacionadas |
|---|---|---|---|
| `ESC-P-01` | Puesta en servicio | Integrador; ingenieros y técnicos | `NEC-P-04`, `NEC-P-07`, `NEC-P-08`, `NEC-P-10` |
| `ESC-P-02` | Configuración inicial | Integrador; ingenieros y técnicos | `NEC-P-04`, `NEC-P-06`, `NEC-P-10` |
| `ESC-P-03` | Operación normal | Operador; ingenieros y técnicos | `NEC-P-01`, `NEC-P-02`, `NEC-P-07` |
| `ESC-P-04` | Supervisión | Operador; producción; ingenieros y técnicos | `NEC-P-02`, `NEC-P-03`, `NEC-P-09` |
| `ESC-P-05` | Diagnóstico de fallas | Ingenieros y técnicos; mantenimiento | `NEC-P-03`, `NEC-P-05`, `NEC-P-09` |
| `ESC-P-06` | Respuesta ante condiciones anormales | Operador; producción; mantenimiento | `NEC-P-03`, `NEC-P-07`, `NEC-P-08` |
| `ESC-P-07` | Mantenimiento | Ingenieros y técnicos; mantenimiento | `NEC-P-03`, `NEC-P-05`, `NEC-P-10` |
| `ESC-P-08` | Integración con otros sistemas | Integrador; aliados especializados | `NEC-P-06`, `NEC-P-02`, `NEC-P-10` |
| `ESC-P-09` | Recuperación después de interrupciones | Producción; mantenimiento; operador | `NEC-P-03`, `NEC-P-07`, `NEC-P-09` |
| `ESC-P-10` | Actualización o modificación controlada | Ingenieros y técnicos; mantenimiento; aliados | `NEC-P-05`, `NEC-P-06`, `NEC-P-10` |

### ESC-P-01 — Puesta en servicio

- **Actores:** `ACT-P-01`, `ACT-P-02`, `ACT-P-06`.
- **Objetivo:** establecer ControlCore en la aplicación prevista y confirmar que se encuentra listo para la operación supervisada.
- **Condiciones iniciales:** condiciones de instalación definidas; personal autorizado; contexto de la aplicación documentado.
- **Secuencia conceptual:** verificar prerrequisitos de instalación; realizar la configuración inicial; ejecutar comprobaciones de puesta en servicio; confirmar el estado de disponibilidad; registrar el resultado.
- **Resultado esperado:** sistema en un estado operativo definido, con la configuración y las comprobaciones registradas.
- **Condiciones anormales relevantes:** instalación incompleta; configuración incompatible; condiciones de seguridad no resueltas; información de la aplicación insuficiente.
- **Necesidades relacionadas:** `NEC-P-04`, `NEC-P-07`, `NEC-P-08`, `NEC-P-10`.
- **Preguntas abiertas:** `PREG-P-01`, `PREG-P-06`, `PREG-P-11`, `PREG-P-13`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-02 — Configuración inicial

- **Actores:** `ACT-P-01`, `ACT-P-02`.
- **Objetivo:** adaptar la configuración a los requisitos de la aplicación antes de la operación.
- **Condiciones iniciales:** requisitos de la aplicación conocidos; cambios autorizados; configuración de referencia disponible.
- **Secuencia conceptual:** identificar parámetros configurables; definir valores; validar la configuración; registrarla; obtener la aprobación correspondiente.
- **Resultado esperado:** configuración documentada, validada y coherente con la aplicación.
- **Condiciones anormales relevantes:** valores inválidos; configuración inconsistente; cambios no autorizados; pérdida de la configuración de referencia.
- **Necesidades relacionadas:** `NEC-P-04`, `NEC-P-06`, `NEC-P-10`.
- **Preguntas abiertas:** `PREG-P-04`, `PREG-P-09`, `PREG-P-11`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-03 — Operación normal

- **Actores:** `ACT-P-03`, `ACT-P-02`.
- **Objetivo:** ejecutar la operación prevista dentro de las condiciones definidas para la aplicación.
- **Condiciones iniciales:** sistema puesto en servicio y configurado; sin fallas activas conocidas; operación autorizada.
- **Secuencia conceptual:** iniciar la operación conforme al procedimiento; mantener la operación dentro de las condiciones definidas; supervisar el estado; detener la operación conforme al procedimiento.
- **Resultado esperado:** operación realizada dentro de las condiciones previstas, con los eventos relevantes registrados.
- **Condiciones anormales relevantes:** condiciones fuera de rango; pérdida de realimentación; pérdida de comunicación; órdenes inválidas o contradictorias.
- **Necesidades relacionadas:** `NEC-P-01`, `NEC-P-02`, `NEC-P-07`.
- **Preguntas abiertas:** `PREG-P-04`, `PREG-P-06`, `PREG-P-12`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-04 — Supervisión

- **Actores:** `ACT-P-03`, `ACT-P-04`, `ACT-P-02`.
- **Objetivo:** observar el estado y el comportamiento del sistema para detectar desviaciones.
- **Condiciones iniciales:** sistema en operación; información de supervisión disponible según el diseño que se defina.
- **Secuencia conceptual:** consultar estados y variables relevantes; identificar alarmas o tendencias; registrar observaciones; escalar cuando corresponda.
- **Resultado esperado:** actores informados sobre el estado operativo y las desviaciones identificadas.
- **Condiciones anormales relevantes:** información insuficiente o no actualizada; alarmas no comprendidas; pérdida de la función de supervisión.
- **Necesidades relacionadas:** `NEC-P-02`, `NEC-P-03`, `NEC-P-09`.
- **Preguntas abiertas:** `PREG-P-09`, `PREG-P-12`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-05 — Diagnóstico de fallas

- **Actores:** `ACT-P-02`, `ACT-P-05`.
- **Objetivo:** identificar la causa de una falla y aportar información para la corrección.
- **Condiciones iniciales:** falla detectada; personal autorizado; información de operación disponible.
- **Secuencia conceptual:** recopilar evidencia; clasificar la condición; analizar causas posibles; recomendar una acción correctiva; registrar el diagnóstico.
- **Resultado esperado:** diagnóstico documentado y acción correctiva definida.
- **Condiciones anormales relevantes:** diagnóstico no concluyente; evidencia insuficiente; fallas múltiples; pérdida de información.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-05`, `NEC-P-09`.
- **Preguntas abiertas:** `PREG-P-09`, `PREG-P-12`, `PREG-P-13`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-06 — Respuesta ante condiciones anormales

- **Actores:** `ACT-P-03`, `ACT-P-04`, `ACT-P-05`.
- **Objetivo:** gestionar una condición anormal conforme a las responsabilidades y procedimientos que se definan.
- **Condiciones iniciales:** condición anormal detectada; procedimientos y análisis de riesgos disponibles.
- **Secuencia conceptual:** detectar la condición; informar a los actores correspondientes; ejecutar la respuesta definida por el diseño aprobado; registrar el evento; escalar cuando corresponda.
- **Resultado esperado:** condición gestionada conforme al diseño aprobado, con responsabilidades respetadas y evidencia registrada.
- **Condiciones anormales relevantes:** responsabilidades no delimitadas; información insuficiente; función de seguridad no definida; fallas simultáneas.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-07`, `NEC-P-08`.
- **Preguntas abiertas:** `PREG-P-01`, `PREG-P-02`, `PREG-P-03`.
- **Estado:** Hipótesis — requiere validación.
- **Nota:** este escenario no define el comportamiento de seguridad ni el estado seguro; ambos dependen del análisis de riesgos.

### ESC-P-07 — Mantenimiento

- **Actores:** `ACT-P-02`, `ACT-P-05`.
- **Objetivo:** realizar mantenimiento, inspección o reparación sin comprometer la operación ni la trazabilidad.
- **Condiciones iniciales:** ventana o procedimiento de mantenimiento definido; personal autorizado; estado del sistema conocido.
- **Secuencia conceptual:** planificar la actividad; preparar el sistema; ejecutar el mantenimiento; verificar el resultado; registrar la actividad; devolver el sistema al estado operativo autorizado.
- **Resultado esperado:** mantenimiento completado y verificado, con historial registrado.
- **Condiciones anormales relevantes:** hallazgos no previstos; repuestos no disponibles; verificación incompleta; configuración alterada.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-05`, `NEC-P-10`.
- **Preguntas abiertas:** `PREG-P-11`, `PREG-P-13`, `PREG-P-15`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-08 — Integración con otros sistemas

- **Actores:** `ACT-P-01`, `ACT-P-07`.
- **Objetivo:** intercambiar la información necesaria y coordinar la operación con sistemas externos.
- **Condiciones iniciales:** sistemas externos identificados; responsabilidades acordadas; condiciones de integración definidas.
- **Secuencia conceptual:** identificar la información a intercambiar; acordar responsabilidades; verificar la integración; operar en las condiciones definidas; registrar incidencias.
- **Resultado esperado:** integración operativa conforme a las condiciones acordadas, con responsabilidades claras.
- **Condiciones anormales relevantes:** sistema externo incompatible; información faltante; responsabilidad no delimitada; pérdida de la integración.
- **Necesidades relacionadas:** `NEC-P-06`, `NEC-P-02`, `NEC-P-10`.
- **Preguntas abiertas:** `PREG-P-10`, `PREG-P-11`, `PREG-P-13`.
- **Estado:** Hipótesis — requiere validación.

### ESC-P-09 — Recuperación después de interrupciones

- **Actores:** `ACT-P-03`, `ACT-P-04`, `ACT-P-05`.
- **Objetivo:** restaurar la operación después de una interrupción de forma controlada y verificable.
- **Condiciones iniciales:** interrupción ocurrida; causa conocida o en investigación; procedimientos disponibles.
- **Secuencia conceptual:** detectar la interrupción; verificar el estado conforme al diseño aprobado; restaurar las condiciones necesarias; verificar la integridad del sistema; autorizar la reanudación; registrar el evento.
- **Resultado esperado:** recuperación controlada, estado verificado y reanudación autorizada.
- **Condiciones anormales relevantes:** interrupción repetida; estado desconocido; realimentación no disponible; causa no identificada.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-07`, `NEC-P-09`.
- **Preguntas abiertas:** `PREG-P-01`, `PREG-P-03`, `PREG-P-13`.
- **Estado:** Hipótesis — requiere validación.
- **Nota:** este escenario no define el comportamiento de recuperación ni el estado seguro; ambos dependen del análisis de riesgos.

### ESC-P-10 — Actualización o modificación controlada

- **Actores:** `ACT-P-02`, `ACT-P-05`, `ACT-P-07`.
- **Objetivo:** aplicar una actualización o modificación autorizada preservando la trazabilidad y la compatibilidad.
- **Condiciones iniciales:** cambio aprobado; impacto evaluado; condiciones de reversión definidas; personal autorizado.
- **Secuencia conceptual:** identificar la versión; verificar compatibilidad; aplicar el cambio; verificar el resultado; registrar la versión y la evidencia; actualizar la documentación.
- **Resultado esperado:** cambio aplicado y verificado, con trazabilidad y documentación actualizadas.
- **Condiciones anormales relevantes:** actualización fallida; incompatibilidad; reversión incompleta; documentación desactualizada.
- **Necesidades relacionadas:** `NEC-P-05`, `NEC-P-06`, `NEC-P-10`.
- **Preguntas abiertas:** `PREG-P-11`, `PREG-P-13`, `PREG-P-15`.
- **Estado:** Hipótesis — requiere validación.

## 5. Condiciones anormales y límites

Los escenarios identifican condiciones anormales de forma conceptual. No definen respuestas de seguridad, tiempos de reacción, prioridades de parada ni recuperación automática.

Cualquier comportamiento asociado a condiciones anormales deberá derivarse de:

- El análisis de riesgos de la aplicación.
- La delimitación de responsabilidades entre ControlCore y la máquina.
- Las decisiones del responsable del proyecto.
- Los requisitos de seguridad que se aprueben posteriormente.

## 6. Preguntas abiertas

Las preguntas completas y priorizadas se encuentran en `docs/01-requisitos/necesidades-producto.md` (sección 6).

Las preguntas con mayor relación con los escenarios son:

- `PREG-P-01`, `PREG-P-02`, `PREG-P-03`: seguridad, responsabilidades y estados seguros.
- `PREG-P-04`, `PREG-P-05`, `PREG-P-06`: aplicación objetivo, motores y condiciones.
- `PREG-P-07`, `PREG-P-08`, `PREG-P-09`: capacidades de la primera versión.
- `PREG-P-10`, `PREG-P-11`, `PREG-P-12`: integración, actores e información.
- `PREG-P-13`, `PREG-P-14`, `PREG-P-15`: verificación, entorno de pruebas y soporte.

No se asume ninguna respuesta.

## 7. Trazabilidad preliminar

| Escenario | Actores | Necesidades | Preguntas |
|---|---|---|---|
| `ESC-P-01` | `ACT-P-01`, `ACT-P-02`, `ACT-P-06` | `NEC-P-04`, `NEC-P-07`, `NEC-P-08`, `NEC-P-10` | `PREG-P-01`, `PREG-P-06`, `PREG-P-11`, `PREG-P-13` |
| `ESC-P-02` | `ACT-P-01`, `ACT-P-02` | `NEC-P-04`, `NEC-P-06`, `NEC-P-10` | `PREG-P-04`, `PREG-P-09`, `PREG-P-11` |
| `ESC-P-03` | `ACT-P-02`, `ACT-P-03` | `NEC-P-01`, `NEC-P-02`, `NEC-P-07` | `PREG-P-04`, `PREG-P-06`, `PREG-P-12` |
| `ESC-P-04` | `ACT-P-02`, `ACT-P-03`, `ACT-P-04` | `NEC-P-02`, `NEC-P-03`, `NEC-P-09` | `PREG-P-09`, `PREG-P-12` |
| `ESC-P-05` | `ACT-P-02`, `ACT-P-05` | `NEC-P-03`, `NEC-P-05`, `NEC-P-09` | `PREG-P-09`, `PREG-P-12`, `PREG-P-13` |
| `ESC-P-06` | `ACT-P-03`, `ACT-P-04`, `ACT-P-05` | `NEC-P-03`, `NEC-P-07`, `NEC-P-08` | `PREG-P-01`, `PREG-P-02`, `PREG-P-03` |
| `ESC-P-07` | `ACT-P-02`, `ACT-P-05` | `NEC-P-03`, `NEC-P-05`, `NEC-P-10` | `PREG-P-11`, `PREG-P-13`, `PREG-P-15` |
| `ESC-P-08` | `ACT-P-01`, `ACT-P-07` | `NEC-P-02`, `NEC-P-06`, `NEC-P-10` | `PREG-P-10`, `PREG-P-11`, `PREG-P-13` |
| `ESC-P-09` | `ACT-P-03`, `ACT-P-04`, `ACT-P-05` | `NEC-P-03`, `NEC-P-07`, `NEC-P-09` | `PREG-P-01`, `PREG-P-03`, `PREG-P-13` |
| `ESC-P-10` | `ACT-P-02`, `ACT-P-05`, `ACT-P-07` | `NEC-P-05`, `NEC-P-06`, `NEC-P-10` | `PREG-P-11`, `PREG-P-13`, `PREG-P-15` |

Estos vínculos son preliminares y no constituyen requisitos aprobados ni una matriz de trazabilidad de requisitos.

## 8. Pendientes

- Los diez escenarios son hipótesis y requieren validación con los actores y aprobación del responsable del proyecto.
- No se han definido comportamientos de seguridad, recuperación o parada.
- No se han definido interfaces, protocolos, tiempos ni algoritmos.
- No se han asignado identificadores `RF-###`, `RNF-###` o `RES-###`.
- Las decisiones pendientes se registran en `docs/06-decisiones/pendientes.md`.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/vision-producto.md` (secciones 2, 5, 7, 9 y 12)
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md` (secciones 24, 25 y 26)
- `docs/00-gobierno/criterios-calidad.md` (secciones 3, 9 y 13)
- `docs/00-gobierno/definicion-de-terminado.md` (sección 7)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.2.1:** propuesta inicial de escenarios de uso. Hipótesis pendientes de validación y aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
