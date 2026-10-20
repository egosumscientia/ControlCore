# Escenarios de uso — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Escenarios de uso  
**Versión:** 0.3  
**Estado:** Revisión de documento aprobado — actualización B2.3 pendiente de aprobación  
**Fase:** Ingeniería conceptual y de requisitos  
**Fecha de revisión:** 2026-10-20  
**Aprobación:** Versión 0.2 aprobada el 2026-10-20 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.3 pendiente de aprobación

---

## 1. Propósito

Este documento registra los escenarios aprobados como base conceptual de utilización industrial de ControlCore.

Los escenarios fueron propuestos en B2.2.1 y aprobados en B2.2.2. Su finalidad es facilitar la derivación de requisitos concretos a partir de condiciones de uso trazables.

La versión 0.3 actualiza únicamente las referencias de estado afectadas por las decisiones conceptuales de B2.3 (`DEC-GOB-022` a `DEC-GOB-030`). No modifica los escenarios aprobados ni las decisiones `DEC-GOB-016` a `DEC-GOB-021`.

## 2. Alcance

Este documento comprende escenarios conceptuales aprobados de puesta en servicio, configuración, operación, supervisión, diagnóstico, mantenimiento, integración, recuperación y actualización.

No especifica interfaces, protocolos, tiempos, algoritmos ni comportamientos de seguridad. La aprobación no valida los detalles técnicos ni las implementaciones. No contiene requisitos aprobados.

Los identificadores `ESC-P-###` identifican los escenarios aprobados en este documento. No constituyen un esquema permanente ni reutilizan identificadores `RF-###`, `RNF-###` o `RES-###`.

## 3. Fuente y clasificación

La fuente principal es `docs/00-gobierno/vision-producto.md` (secciones 2, 5, 7, 9 y 12). Se consultaron además los documentos de gobierno y la estructura de gestión de requisitos.

Todos los escenarios fueron propuestos como **hipótesis de aplicación** en B2.2.1 y aprobados como base conceptual de ingeniería el 2026-10-20 (DEC-GOB-016). La clasificación de origen se conserva como historial. La aprobación no valida los detalles técnicos ni las implementaciones.

Las condiciones anormales se describen de forma conceptual. Cualquier comportamiento de seguridad, recuperación o parada deberá derivarse del análisis de riesgos y de las decisiones DEC-GOB-017 a DEC-GOB-021.

## 4. Escenarios aprobados

Los diez escenarios de la tabla están aprobados como base conceptual de ingeniería (DEC-GOB-016, 2026-10-20). Las preguntas citadas en cada escenario fueron resueltas conceptualmente; las preguntas técnicas derivadas se enumeran en la sección 6.2.

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
- **Preguntas de origen:** `PREG-P-01`, `PREG-P-06`, `PREG-P-11`, `PREG-P-13`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-02 — Configuración inicial

- **Actores:** `ACT-P-01`, `ACT-P-02`.
- **Objetivo:** adaptar la configuración a los requisitos de la aplicación antes de la operación.
- **Condiciones iniciales:** requisitos de la aplicación conocidos; cambios autorizados; configuración de referencia disponible.
- **Secuencia conceptual:** identificar parámetros configurables; definir valores; validar la configuración; registrarla; obtener la aprobación correspondiente.
- **Resultado esperado:** configuración documentada, validada y coherente con la aplicación.
- **Condiciones anormales relevantes:** valores inválidos; configuración inconsistente; cambios no autorizados; pérdida de la configuración de referencia.
- **Necesidades relacionadas:** `NEC-P-04`, `NEC-P-06`, `NEC-P-10`.
- **Preguntas de origen:** `PREG-P-04`, `PREG-P-09`, `PREG-P-11`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-03 — Operación normal

- **Actores:** `ACT-P-03`, `ACT-P-02`.
- **Objetivo:** ejecutar la operación prevista dentro de las condiciones definidas para la aplicación.
- **Condiciones iniciales:** sistema puesto en servicio y configurado; sin fallas activas conocidas; operación autorizada.
- **Secuencia conceptual:** iniciar la operación conforme al procedimiento; mantener la operación dentro de las condiciones definidas; supervisar el estado; detener la operación conforme al procedimiento.
- **Resultado esperado:** operación realizada dentro de las condiciones previstas, con los eventos relevantes registrados.
- **Condiciones anormales relevantes:** condiciones fuera de rango; pérdida de realimentación; pérdida de comunicación; órdenes inválidas o contradictorias.
- **Necesidades relacionadas:** `NEC-P-01`, `NEC-P-02`, `NEC-P-07`.
- **Preguntas de origen:** `PREG-P-04`, `PREG-P-06`, `PREG-P-12`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-04 — Supervisión

- **Actores:** `ACT-P-03`, `ACT-P-04`, `ACT-P-02`.
- **Objetivo:** observar el estado y el comportamiento del sistema para detectar desviaciones.
- **Condiciones iniciales:** sistema en operación; información de supervisión disponible según el diseño que se defina.
- **Secuencia conceptual:** consultar estados y variables relevantes; identificar alarmas o tendencias; registrar observaciones; escalar cuando corresponda.
- **Resultado esperado:** actores informados sobre el estado operativo y las desviaciones identificadas.
- **Condiciones anormales relevantes:** información insuficiente o no actualizada; alarmas no comprendidas; pérdida de la función de supervisión.
- **Necesidades relacionadas:** `NEC-P-02`, `NEC-P-03`, `NEC-P-09`.
- **Preguntas de origen:** `PREG-P-09`, `PREG-P-12`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-05 — Diagnóstico de fallas

- **Actores:** `ACT-P-02`, `ACT-P-05`.
- **Objetivo:** identificar la causa de una falla y aportar información para la corrección.
- **Condiciones iniciales:** falla detectada; personal autorizado; información de operación disponible.
- **Secuencia conceptual:** recopilar evidencia; clasificar la condición; analizar causas posibles; recomendar una acción correctiva; registrar el diagnóstico.
- **Resultado esperado:** diagnóstico documentado y acción correctiva definida.
- **Condiciones anormales relevantes:** diagnóstico no concluyente; evidencia insuficiente; fallas múltiples; pérdida de información.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-05`, `NEC-P-09`.
- **Preguntas de origen:** `PREG-P-09`, `PREG-P-12`, `PREG-P-13`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-06 — Respuesta ante condiciones anormales

- **Actores:** `ACT-P-03`, `ACT-P-04`, `ACT-P-05`.
- **Objetivo:** gestionar una condición anormal conforme a las responsabilidades y procedimientos que se definan.
- **Condiciones iniciales:** condición anormal detectada; procedimientos y análisis de riesgos disponibles.
- **Secuencia conceptual:** detectar la condición; informar a los actores correspondientes; ejecutar la respuesta definida por el diseño aprobado; registrar el evento; escalar cuando corresponda.
- **Resultado esperado:** condición gestionada conforme al diseño aprobado, con responsabilidades respetadas y evidencia registrada.
- **Condiciones anormales relevantes:** responsabilidades no delimitadas; información insuficiente; función de seguridad no definida; fallas simultáneas.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-07`, `NEC-P-08`.
- **Preguntas de origen:** `PREG-P-01`, `PREG-P-02`, `PREG-P-03`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.
- **Nota:** este escenario no define el comportamiento de seguridad ni el estado seguro; ambos dependen del análisis de riesgos.

### ESC-P-07 — Mantenimiento

- **Actores:** `ACT-P-02`, `ACT-P-05`.
- **Objetivo:** realizar mantenimiento, inspección o reparación sin comprometer la operación ni la trazabilidad.
- **Condiciones iniciales:** ventana o procedimiento de mantenimiento definido; personal autorizado; estado del sistema conocido.
- **Secuencia conceptual:** planificar la actividad; preparar el sistema; ejecutar el mantenimiento; verificar el resultado; registrar la actividad; devolver el sistema al estado operativo autorizado.
- **Resultado esperado:** mantenimiento completado y verificado, con historial registrado.
- **Condiciones anormales relevantes:** hallazgos no previstos; repuestos no disponibles; verificación incompleta; configuración alterada.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-05`, `NEC-P-10`.
- **Preguntas de origen:** `PREG-P-11`, `PREG-P-13`, `PREG-P-15`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-08 — Integración con otros sistemas

- **Actores:** `ACT-P-01`, `ACT-P-07`.
- **Objetivo:** intercambiar la información necesaria y coordinar la operación con sistemas externos.
- **Condiciones iniciales:** sistemas externos identificados; responsabilidades acordadas; condiciones de integración definidas.
- **Secuencia conceptual:** identificar la información a intercambiar; acordar responsabilidades; verificar la integración; operar en las condiciones definidas; registrar incidencias.
- **Resultado esperado:** integración operativa conforme a las condiciones acordadas, con responsabilidades claras.
- **Condiciones anormales relevantes:** sistema externo incompatible; información faltante; responsabilidad no delimitada; pérdida de la integración.
- **Necesidades relacionadas:** `NEC-P-06`, `NEC-P-02`, `NEC-P-10`.
- **Preguntas de origen:** `PREG-P-10`, `PREG-P-11`, `PREG-P-13`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

### ESC-P-09 — Recuperación después de interrupciones

- **Actores:** `ACT-P-03`, `ACT-P-04`, `ACT-P-05`.
- **Objetivo:** restaurar la operación después de una interrupción de forma controlada y verificable.
- **Condiciones iniciales:** interrupción ocurrida; causa conocida o en investigación; procedimientos disponibles.
- **Secuencia conceptual:** detectar la interrupción; verificar el estado conforme al diseño aprobado; restaurar las condiciones necesarias; verificar la integridad del sistema; autorizar la reanudación; registrar el evento.
- **Resultado esperado:** recuperación controlada, estado verificado y reanudación autorizada.
- **Condiciones anormales relevantes:** interrupción repetida; estado desconocido; realimentación no disponible; causa no identificada.
- **Necesidades relacionadas:** `NEC-P-03`, `NEC-P-07`, `NEC-P-09`.
- **Preguntas de origen:** `PREG-P-01`, `PREG-P-03`, `PREG-P-13`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.
- **Nota:** este escenario no define el comportamiento de recuperación ni el estado seguro; ambos dependen del análisis de riesgos.

### ESC-P-10 — Actualización o modificación controlada

- **Actores:** `ACT-P-02`, `ACT-P-05`, `ACT-P-07`.
- **Objetivo:** aplicar una actualización o modificación autorizada preservando la trazabilidad y la compatibilidad.
- **Condiciones iniciales:** cambio aprobado; impacto evaluado; condiciones de reversión definidas; personal autorizado.
- **Secuencia conceptual:** identificar la versión; verificar compatibilidad; aplicar el cambio; verificar el resultado; registrar la versión y la evidencia; actualizar la documentación.
- **Resultado esperado:** cambio aplicado y verificado, con trazabilidad y documentación actualizadas.
- **Condiciones anormales relevantes:** actualización fallida; incompatibilidad; reversión incompleta; documentación desactualizada.
- **Necesidades relacionadas:** `NEC-P-05`, `NEC-P-06`, `NEC-P-10`.
- **Preguntas de origen:** `PREG-P-11`, `PREG-P-13`, `PREG-P-15`.
- **Estado:** Aprobado como escenario conceptual — 2026-10-20 (DEC-GOB-016). Detalles técnicos pendientes.

## 5. Condiciones anormales y límites

Los escenarios identifican condiciones anormales de forma conceptual. No definen respuestas de seguridad, tiempos de reacción, prioridades de parada ni recuperación automática.

`DEC-GOB-017` aprobó que los estados seguros dependen del análisis de riesgos de cada aplicación y que no debe asumirse que detener un motor o cortar su alimentación constituye siempre una condición segura. `DEC-GOB-019` excluyó las funciones de seguridad certificadas de la primera versión mientras no exista el proceso de análisis y evaluación de conformidad correspondiente.

B2.3 aprobó conceptualmente respuestas diferenciadas ante fallas, recuperación configurable tras interrupciones, respuesta ante pérdida de comunicaciones o realimentación, watchdog y recuperación supervisada (`D07`, `D11`, `D17`, `D30`, `D38`, `D51`; `DEC-GOB-024`). Todas ellas están condicionadas por la evaluación de riesgos y no definen estados seguros ni procedimientos concretos.

Cualquier comportamiento asociado a condiciones anormales deberá derivarse de:

- El análisis de riesgos de la aplicación.
- La delimitación de responsabilidades entre ControlCore y la máquina.
- Las decisiones `DEC-GOB-017`, `DEC-GOB-019` y `DEC-GOB-024`.
- Los requisitos de seguridad que se aprueben posteriormente.

## 6. Decisiones aprobadas y preguntas técnicas derivadas

### 6.1. Decisiones aprobadas

Las quince preguntas de B2.2.1 fueron resueltas conceptualmente (DEC-GOB-017 a DEC-GOB-021):

| Pregunta | Asunto | Decisión |
|---|---|---|
| `PREG-P-01` | Funciones y responsabilidades de seguridad | `DEC-GOB-017` |
| `PREG-P-02` | Análisis de riesgos y normativa | `DEC-GOB-017` |
| `PREG-P-03` | Estados seguros | `DEC-GOB-017` |
| `PREG-P-04` | Aplicación objetivo | `DEC-GOB-018` |
| `PREG-P-05` | Motores y actuadores | `DEC-GOB-018` |
| `PREG-P-06` | Entorno y condiciones | `DEC-GOB-018` |
| `PREG-P-07` | Capacidades funcionales objetivo | `DEC-GOB-019` |
| `PREG-P-08` | Exclusiones iniciales | `DEC-GOB-019` |
| `PREG-P-09` | Nivel funcional inicial | `DEC-GOB-019` |
| `PREG-P-10` | Integración externa | `DEC-GOB-020` |
| `PREG-P-11` | Perfiles funcionales de acceso | `DEC-GOB-020` |
| `PREG-P-12` | Información registrada | `DEC-GOB-020` |
| `PREG-P-13` | Criterios de aceptación | `DEC-GOB-021` |
| `PREG-P-14` | Niveles de validación | `DEC-GOB-021` |
| `PREG-P-15` | Documentación y soporte | `DEC-GOB-021` |

### 6.2. Preguntas técnicas derivadas que permanecen abiertas

1. Modelo, parámetros y electrónica del motor DC del primer incremento. La familia está definida como motores DC con escobillas; el modelo, la tensión, la corriente, la potencia y la electrónica de potencia permanecen pendientes. Derivado de `D01`, `D19` y `D25` (`DEC-GOB-022`, `DEC-GOB-028`).
2. Prestaciones cuantitativas de control, supervisión y diagnóstico. Derivadas de `PREG-P-13` y `DEC-GOB-021`.
3. Condiciones eléctricas, ambientales y de instalación cuantitativas. Derivadas de `PREG-P-06` y `DEC-GOB-018`.
4. Interfaces, protocolos y sistemas externos concretos. Derivados de `PREG-P-10` y `DEC-GOB-020`; los principios de desacoplamiento y versionado están aprobados, pero las interfaces concretas no.
5. Arquitectura de seguridad, funciones de seguridad y estados seguros por aplicación. Derivada de `PREG-P-01`, `PREG-P-02`, `PREG-P-03` y `DEC-GOB-017`; las respuestas ante fallas están condicionadas por riesgos.
6. Métodos de verificación, criterios de aceptación cuantitativos y entorno de pruebas. Derivados de `PREG-P-13`, `PREG-P-14` y `DEC-GOB-021`; la estrategia conceptual está aprobada, pero los procedimientos y valores no.
7. Límites cuantitativos, interfaces, medidas de protección y criterios de aceptación del primer incremento. El alcance funcional está delimitado por `D25` (`DEC-GOB-022`); estos detalles permanecen abiertos. Derivado de `PREG-P-07`, `PREG-P-08`, `PREG-P-09` y `DEC-GOB-019`.
8. Autenticación, matriz detallada de permisos, retención y almacenamiento de información. Derivados de `PREG-P-11`, `PREG-P-12` y `DEC-GOB-020`; los perfiles están aprobados, pero los mecanismos no.

Estos asuntos no constituyen decisiones aprobadas. Deberán resolverse antes de implementar el alcance afectado.

## 7. Trazabilidad

| Escenario | Actores | Necesidades | Decisiones | Preguntas de origen |
|---|---|---|---|---|
| `ESC-P-01` | `ACT-P-01`, `ACT-P-02`, `ACT-P-06` | `NEC-P-04`, `NEC-P-07`, `NEC-P-08`, `NEC-P-10` | `DEC-GOB-016`, `DEC-GOB-017`, `DEC-GOB-018`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-01`, `PREG-P-06`, `PREG-P-11`, `PREG-P-13` |
| `ESC-P-02` | `ACT-P-01`, `ACT-P-02` | `NEC-P-04`, `NEC-P-06`, `NEC-P-10` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-019`, `DEC-GOB-020` | `PREG-P-04`, `PREG-P-09`, `PREG-P-11` |
| `ESC-P-03` | `ACT-P-02`, `ACT-P-03` | `NEC-P-01`, `NEC-P-02`, `NEC-P-07` | `DEC-GOB-016`, `DEC-GOB-018`, `DEC-GOB-019`, `DEC-GOB-020` | `PREG-P-04`, `PREG-P-06`, `PREG-P-12` |
| `ESC-P-04` | `ACT-P-02`, `ACT-P-03`, `ACT-P-04` | `NEC-P-02`, `NEC-P-03`, `NEC-P-09` | `DEC-GOB-016`, `DEC-GOB-019`, `DEC-GOB-020` | `PREG-P-09`, `PREG-P-12` |
| `ESC-P-05` | `ACT-P-02`, `ACT-P-05` | `NEC-P-03`, `NEC-P-05`, `NEC-P-09` | `DEC-GOB-016`, `DEC-GOB-019`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-09`, `PREG-P-12`, `PREG-P-13` |
| `ESC-P-06` | `ACT-P-03`, `ACT-P-04`, `ACT-P-05` | `NEC-P-03`, `NEC-P-07`, `NEC-P-08` | `DEC-GOB-016`, `DEC-GOB-017`, `DEC-GOB-019` | `PREG-P-01`, `PREG-P-02`, `PREG-P-03` |
| `ESC-P-07` | `ACT-P-02`, `ACT-P-05` | `NEC-P-03`, `NEC-P-05`, `NEC-P-10` | `DEC-GOB-016`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-11`, `PREG-P-13`, `PREG-P-15` |
| `ESC-P-08` | `ACT-P-01`, `ACT-P-07` | `NEC-P-02`, `NEC-P-06`, `NEC-P-10` | `DEC-GOB-016`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-10`, `PREG-P-11`, `PREG-P-13` |
| `ESC-P-09` | `ACT-P-03`, `ACT-P-04`, `ACT-P-05` | `NEC-P-03`, `NEC-P-07`, `NEC-P-09` | `DEC-GOB-016`, `DEC-GOB-017`, `DEC-GOB-021` | `PREG-P-01`, `PREG-P-03`, `PREG-P-13` |
| `ESC-P-10` | `ACT-P-02`, `ACT-P-05`, `ACT-P-07` | `NEC-P-05`, `NEC-P-06`, `NEC-P-10` | `DEC-GOB-016`, `DEC-GOB-020`, `DEC-GOB-021` | `PREG-P-11`, `PREG-P-13`, `PREG-P-15` |

Estos vínculos son de trazabilidad documental. No constituyen requisitos aprobados ni una matriz de trazabilidad de requisitos.

Las decisiones `DEC-GOB-022` a `DEC-GOB-030` se relacionan con estos escenarios a través de la matriz de `docs/06-decisiones/consolidacion-decisiones-B2.3.md`. Esa matriz es de trazabilidad conceptual y no crea requisitos.

## 8. Pendientes

- Los diez escenarios están aprobados como base conceptual (DEC-GOB-016).
- No se han definido comportamientos de seguridad, recuperación o parada para una aplicación concreta.
- No se han definido interfaces, protocolos, tiempos ni algoritmos.
- Las decisiones conceptuales de B2.3 fueron consolidadas en `DEC-GOB-022` a `DEC-GOB-030`.
- Las preguntas técnicas derivadas de la sección 6.2 permanecen abiertas.
- No se han asignado identificadores `RF-###`, `RNF-###` o `RES-###`.
- Las preguntas técnicas pendientes se registran en `docs/06-decisiones/pendientes.md`.

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
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.2.1:** propuesta inicial de escenarios de uso. Hipótesis pendientes de validación y aprobación.
- **0.2 — 2026-10-20 — B2.2.2:** aprobación de los diez escenarios como base conceptual de ingeniería (DEC-GOB-016); incorporación de las decisiones `DEC-GOB-017` a `DEC-GOB-021` y de las preguntas técnicas derivadas.
- **0.3 — 2026-10-20 — B2.3:** actualización de las referencias de estado afectadas por `DEC-GOB-022` a `DEC-GOB-030`; precisión de la familia inicial, del alcance funcional del primer incremento y de las respuestas condicionadas por riesgos. Los escenarios y las decisiones anteriores no se modifican. Versión pendiente de aprobación.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
