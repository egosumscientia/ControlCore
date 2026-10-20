# Consolidación de decisiones y especificación preliminar — B2.4

**Proyecto:** ControlCore
**Empresa:** makeAutomatic
**Tipo de proyecto:** Desarrollo de producto industrial comercial
**Documento:** Consolidación de decisiones y especificación preliminar — B2.4
**Versión:** 0.1
**Estado:** Propuesta para aprobación
**Fase:** Ingeniería de requisitos
**Fecha de formalización:** 2026-10-20
**Aprobación documental:** Pendiente — preparado para revisión del responsable del proyecto

---

## 1. Propósito

Este documento consolida las 60 decisiones adoptadas por el responsable del proyecto en la ronda posterior a B2.3, conserva la referencia individual `D01`–`D60`, identifica sus relaciones y prepara la especificación preliminar de requisitos.

Las decisiones se reproducen como reconstrucción resumida de las resoluciones aprobadas. No son una transcripción literal de las preguntas y alternativas originales. Su aprobación no aprueba automáticamente este documento ni los requisitos candidatos.

En este documento, `D01`–`D60` identifican las decisiones de B2.4. Las decisiones de B2.3 se citan mediante `DEC-GOB-0xx` o `B2.3-Dxx` para evitar ambigüedad.

## 2. Alcance y relaciones

B2.4 comprende:

1. La consolidación documental de las 60 decisiones.
2. La estructura del análisis preliminar de riesgos.
3. Los requisitos candidatos `RF-###`, `RNF-###` y `RES-###`.
4. La trazabilidad entre decisiones, peligros, requisitos y verificación.
5. La identificación de redundancias, dependencias, contradicciones y datos pendientes.

B2.4 no implementa hardware, firmware ni software. No diseña circuitos, no selecciona componentes, microcontroladores, protocolos ni tecnologías, no asigna valores cuantitativos no aprobados y no autoriza pruebas físicas ni implementación.

Los requisitos candidatos son propuestas. No constituyen una línea base de requisitos ni sustituyen la aprobación del responsable del proyecto.

## 3. Resumen de la consolidación

| Grupo | Área | Decisiones | Cantidad | Producto documental |
|---|---|---|---:|---|
| G1 | Metodología y trazabilidad | D01–D03 | 3 | Criterios de formulación y trazabilidad |
| G2 | Identificación y evaluación de riesgos | D04–D18 | 15 | Análisis preliminar de riesgos |
| G3 | Fallas y protecciones | D19–D32 | 14 | Requisitos de detección y protección |
| G4 | Verificación y pruebas | D33–D38 | 6 | Matriz de verificación y compuerta de autorización |
| G5 | Operación y control de movimiento | D39–D47 | 9 | Requisitos de habilitación, arranque, parada y control |
| G6 | Regulación PI | D48–D54 | 7 | Requisitos de regulación, medición y desempeño |
| G7 | Configuración y auditoría | D55–D59 | 5 | Requisitos de configuración, recuperación y auditoría |
| G8 | Cierre | D60 | 1 | Consolidación y preparación documental |
| **Total** |  |  | **60** |  |

## 4. Matriz de trazabilidad de las 60 decisiones

| D | Área | Resultado de la consolidación | Requisitos candidatos | Riesgos o verificación | Observación |
|---|---|---|---|---|---|
| D01 | Metodología | Requisitos del primer incremento | RF-001–RF-027; RNF-001–RNF-005; RES-001–RES-007 | Análisis preliminar completo | Los candidatos no están aprobados. |
| D02 | Metodología | Atributos, criterios y trazabilidad | Todos los candidatos | Matriz de trazabilidad | Cada ficha incluye origen, criterio, método y pendientes. |
| D03 | Metodología | Priorización por riesgos, criticidad, dependencias y valor | Todos los candidatos | Evaluación de riesgos pendiente | Las prioridades quedan pendientes de determinación. |
| D04 | Riesgos | Análisis preliminar antes de requisitos de seguridad | RES-001 | HZ-001–HZ-023; FMEA-001–FMEA-012 | Estructura preparada; evaluación pendiente. |
| D05 | Riesgos | Peligros eléctricos, mecánicos, térmicos, operativos, de control, sensores y comunicaciones | RES-001; RES-007 | HZ-001–HZ-023 | Sin valores de riesgo asignados. |
| D06 | Riesgos | Gravedad, probabilidad, evitabilidad y medidas | RES-002 | Sección de evaluación de riesgos | Escala y criterios pendientes. |
| D07 | Riesgos | Jerarquía de reducción del riesgo | RES-002 | Sección de jerarquía | Diseño inherente, medidas técnicas e información. |
| D08 | Riesgos | Riesgo inicial y residual; eficacia de medidas | RES-002; RES-004 | Matriz de riesgos residuales | Valores pendientes. |
| D09 | Riesgos | Operación normal, arranque, parada, inversión, mantenimiento, fallas, error del operador y recuperación | RF-001–RF-004; RF-021; RF-022 | HZ-001–HZ-023 | Escenarios cubiertos por la estructura de peligros. |
| D10 | Riesgos | Criterios de aceptación de riesgos y revisión antes de pruebas | RES-001; RES-003; RES-004 | Compuerta de pruebas | No se declara aceptación de riesgos. |
| D11 | Riesgos | Sistema completo del banco de pruebas | RES-007 | Límite del sistema | Motor, electrónica, alimentación, carga, sensores, control, operador y entorno. |
| D12 | Riesgos | Estructura por componentes, funciones, escenarios, causas, efectos y medidas | Documento de riesgos | HZ-001–HZ-023 | Sin valores arbitrarios. |
| D13 | Riesgos | Matriz trazable de peligros y evidencia | Documento de riesgos | HZ, FMEA, PF y requisitos | Trazabilidad documental preparada. |
| D14 | Riesgos | Análisis por escenarios y FMEA | Documento de riesgos | FMEA-001–FMEA-012 | Funciones críticas cubiertas. |
| D15 | Riesgos | Criticidad de funciones | Documento de riesgos | PF-001–PF-014 | Criticidad cuantitativa pendiente. |
| D16 | Riesgos | Funciones de protección derivadas | RF-015–RF-022; PF-001–PF-014 | HZ y FMEA | Requisitos candidatos, no funciones certificadas. |
| D17 | Riesgos | Comportamiento y estado seguro por escenario | RF-003; RF-004; RF-021; RF-022 | HZ-003; HZ-011; HZ-018 | No se asume que detener el motor sea siempre seguro. |
| D18 | Riesgos | Restablecimiento y reinicio condicionados | RF-022 | HZ-018 | Requiere falla eliminada, condiciones seguras y autorización. |
| D19 | Fallas | Pérdida y recuperación de alimentación | RF-021 | HZ-011; HZ-018 | Condiciones de recuperación pendientes. |
| D20 | Fallas | Pérdida de realimentación de velocidad | RF-012 | HZ-013 | Respuesta según riesgos. |
| D21 | Fallas | Fallas de sensores | RF-013 | HZ-013 | Desconexión, rango, incoherencia y datos obsoletos. |
| D22 | Fallas | Fallas de comunicaciones | RF-014 | HZ-014 | Distinción crítica/no crítica y tiempos pendientes. |
| D23 | Fallas | Protección contra sobrecorriente | RF-015 | HZ-007; HZ-009; HZ-019 | Umbrales y tiempos pendientes. |
| D24 | Fallas | Sobretensión, subtensión y regeneración | RF-015 | HZ-010; HZ-011 | Umbrales y tiempos pendientes. |
| D25 | Fallas | Riesgos térmicos del motor y la electrónica | RF-016 | HZ-012 | Límites y sensores pendientes. |
| D26 | Fallas | Bloqueo mecánico | RF-017 | HZ-007 | Criterios de discriminación pendientes. |
| D27 | Fallas | Pérdida de carga | RF-017 | HZ-008 | Criterios de detección pendientes. |
| D28 | Fallas | Aceleración inesperada | RF-018 | HZ-005 | Umbrales y respuesta pendientes. |
| D29 | Fallas | Inversión inesperada | RF-018 | HZ-006 | Umbrales y respuesta pendientes. |
| D30 | Fallas | Pérdida de control | RF-019 | HZ-015 | Coherencia comando-control-comportamiento. |
| D31 | Fallas | Fallas de la etapa de potencia | RF-019 | HZ-015 | Cobertura de detección pendiente. |
| D32 | Fallas | Fallas internas del controlador | RF-020; RNF-005 | HZ-016 | Ejecución, memoria, temporización y recursos. |
| D33 | Verificación | Pruebas trazables por protección | RES-003; RES-005 | Matriz de verificación | Disparador, tiempo y criterio pendientes. |
| D34 | Verificación | Análisis y simulación antes de pruebas físicas | RES-003 | Compuerta de pruebas | Riesgo residual y condiciones de ensayo pendientes. |
| D35 | Verificación | Documentación y autorización antes de energizar | RES-003 | Compuerta de pruebas | Autorización explícita obligatoria. |
| D36 | Verificación | Registro de condiciones, configuración, procedimiento, resultados y evidencias | RES-005 | Registro de verificación | Formato y retención pendientes. |
| D37 | Verificación | Gestión de pruebas fallidas, causa raíz y regresión | RES-005 | Registro de no conformidades | Procedimiento pendiente. |
| D38 | Verificación | Cierre de evaluación preliminar sin aceptación definitiva | RES-004 | Cierre de riesgos | No confundir cierre documental con aceptación. |
| D39 | Operación | Requisitos de arranque, parada y habilitación | RF-001–RF-003 | HZ-001–HZ-003 | Especificación candidata. |
| D40 | Operación | Habilitación condicionada | RF-001 | HZ-001; HZ-002; HZ-020; HZ-021 | Condiciones y protecciones pendientes. |
| D41 | Operación | Validación de comandos de arranque | RF-002 | HZ-001; HZ-021 | Permisos y origen pendientes. |
| D42 | Operación | Parada normal, controlada y de protección | RF-003 | HZ-003; HZ-004 | Prioridades derivadas del riesgo pendientes. |
| D43 | Operación | Verificación de parada real | RF-004 | HZ-003 | Umbral y tiempo pendientes. |
| D44 | Operación | Perfiles de desaceleración | RF-005 | HZ-003; HZ-005; HZ-010 | Valores pendientes. |
| D45 | Operación | Perfiles de aceleración | RF-006 | HZ-005; HZ-007 | Valores pendientes. |
| D46 | Operación | Referencias de velocidad | RF-007 | HZ-004; HZ-008 | Límites y permisos pendientes. |
| D47 | Operación | Conmutación lazo abierto/cerrado | RF-008 | HZ-004 | Criterios de transición pendientes. |
| D48 | PI | Ganancias PI configurables y supervisadas | RF-009 | HZ-004 | Criterios de estabilidad pendientes. |
| D49 | PI | Límites de salida, anti-windup y saturación | RF-010 | HZ-004 | Límites y tiempos pendientes. |
| D50 | PI | Medición, filtrado y realimentación confiable | RF-011 | HZ-013 | Rangos y filtros pendientes. |
| D51 | PI | Criterios de estabilidad, error, respuesta y anomalías | RNF-001 | HZ-004 | Métricas y valores pendientes. |
| D52 | PI | Criterios de desempeño | RNF-001 | HZ-004 | Error, sobreimpulso, oscilación y carga. |
| D53 | PI | Pruebas del PI con cargas y perturbaciones | RNF-001; RES-005 | Registro de verificación | Condiciones de prueba pendientes. |
| D54 | PI | Validación de ganancias y desempeño | RF-009; RNF-001 | HZ-004 | Aceptación pendiente de métricas. |
| D55 | Configuración | Configuración validada, integridad y versión anterior | RF-023; RNF-002 | HZ-017 | Mecanismo pendiente. |
| D56 | Configuración | Configuración inválida y recuperación | RF-024; RNF-002 | HZ-017 | Condiciones de seguridad pendientes. |
| D57 | Configuración | Clasificación de parámetros y cambios en operación | RF-025; RNF-004 | HZ-017; HZ-023 | Matriz de criticidad pendiente. |
| D58 | Configuración | Auditoría de cambios | RF-026; RNF-003 | HZ-017 | Formato y retención pendientes. |
| D59 | Configuración | Aplicación, condiciones y reversión de parámetros | RF-025; RNF-004 | HZ-017; HZ-023 | Procedimiento pendiente. |
| D60 | Cierre | Consolidación, redundancias, pendientes y especificación | Todos los candidatos | Este documento y sus matrices | Cierre documental, no aprobación de requisitos. |

## 5. Redundancias y relaciones resueltas

| Relación | Tratamiento |
|---|---|
| D04–D14 | Se consolidan en un único documento de análisis preliminar de riesgos, con identificación de peligros, FMEA, evaluación y matriz trazable. No se crean documentos paralelos. |
| D16–D18 | Se separan función de protección, estado seguro y restablecimiento. No se confunde la existencia de una protección con la aceptación de un estado seguro. |
| D20–D22 | Se distinguen pérdida de realimentación, fallas de sensores y fallas de comunicaciones. Cada una tiene detección y respuesta propia. |
| D23–D25 | Se distinguen protección eléctrica, protección de tensión y protección térmica. La supervisión de la etapa de potencia se trata en D30–D31. |
| D26–D29 | Se distinguen bloqueo, pérdida de carga, aceleración inesperada e inversión inesperada. No se unifican sus indicadores ni sus umbrales. |
| D30–D32 | Se distinguen pérdida de control, falla de potencia y falla interna del controlador. Comparten la necesidad de coherencia y supervisión, pero no el mismo mecanismo de detección. |
| D33–D38 | Se separan prueba, verificación previa, autorización, registro, gestión de fallas y cierre de riesgos. La compuerta de pruebas integra las seis decisiones. |
| D39–D43 | Se distinguen habilitación, validación de comandos, tipos de parada y verificación de parada real. La emisión de un comando no se considera prueba de parada. |
| D44–D47 | Se distinguen rampa de desaceleración, rampa de aceleración, referencia de velocidad y transición de lazo. Son funciones complementarias. |
| D48–D54 | Se distinguen configuración PI, límites y anti-windup, medición, criterios de desempeño, pruebas y validación. No se duplican criterios de aceptación. |
| D55–D59 | Se distinguen persistencia, recuperación, clasificación de parámetros, auditoría y aplicación condicionada. La auditoría no sustituye la validación de la configuración. |
| D60 | Cierra la consolidación; no crea requisitos ni aprobaciones nuevas. |

### 5.1. Relaciones entre requisitos candidatos

| Requisitos | Relación | Tratamiento |
|---|---|---|
| RF-003 y RF-004 | Tipo de parada y verificación de su efecto real | Complementarios; no se considera suficiente el comando. |
| RF-012 y RF-013 | Pérdida de realimentación y clases de falla de sensores | RF-012 cubre la pérdida; RF-013 cubre desconexión, rango, incoherencia y obsolescencia. |
| RF-015 y RF-016 | Protecciones eléctricas y térmicas | Fenómenos distintos; pueden compartir sensores, pero no criterios. |
| RF-019 y RF-020 | Pérdida de control o falla de potencia y falla interna del controlador | Orígenes distintos; la detección puede complementarse. |
| RF-023 y RNF-002 | Persistencia funcional y atributo de integridad/recuperabilidad | RF define el comportamiento; RNF define la calidad exigida. |
| RF-026 y RNF-003 | Registro funcional de cambios y atributo de integridad de la auditoría | RF define qué se registra; RNF define la protección del registro. |
| RF-025 y RNF-004 | Condiciones funcionales de cambio y control de acceso | RF define cuándo se permite; RNF define quién puede hacerlo. |

No se identificaron requisitos duplicados. Las superposiciones son complementarias y quedan delimitadas por la tabla anterior.

## 6. Dependencias principales

1. **Riesgos → protecciones → verificación.** D04–D18 orientan las funciones de protección D19–D32; D33–D38 establecen cómo verificarlas.
2. **Habilitación → arranque → parada.** D40–D41 dependen de configuración válida, protecciones comprobadas y comandos válidos; D42–D43 definen la parada y su verificación.
3. **Referencia → rampas → lazo cerrado.** D44–D47 dependen de la medición de velocidad D50 y de la regulación PI D48–D49.
4. **Medición → PI → desempeño.** D50–D54 dependen de una realimentación confiable y de criterios de estabilidad y desempeño.
5. **Configuración → operación → auditoría.** D55–D59 condicionan la habilitación y el cambio de parámetros; D58 conserva la evidencia.
6. **Pruebas → aceptación.** D33–D38 dependen del análisis de riesgos y de la autorización explícita; ninguna prueba física se autoriza por este documento.

## 7. Contradicciones y compatibilidad con B2.3

No se identificaron contradicciones sustantivas. Se documentan las siguientes precisiones:

1. **Diagnóstico causal.** `B2.3-D06` excluyó el diagnóstico causal automatizado inicial. D32 se refiere a detección de fallas internas del controlador, no a generación automática de causas.
2. **Funciones de seguridad certificadas.** `DEC-GOB-019` excluyó funciones de seguridad certificadas mientras no exista el proceso de conformidad. Las funciones de protección de B2.4 son candidatas operativas; no son funciones certificadas ni declaran conformidad.
3. **Alcance del primer incremento.** `B2.3-D25` delimitó las funciones de control. B2.4 D01 exige los requisitos necesarios para el primer incremento, incluyendo protecciones y configuración segura. Esto se interpreta como precisión del conjunto de requisitos, no como ampliación de capacidades comerciales ni como autorización de implementación.
4. **Configuración y auditoría.** `B2.3-D15` y `DEC-GOB-026` aprobaron perfiles, autenticación y auditoría conceptuales. B2.4 D57–D59 precisan la criticidad y el cambio de parámetros; el mecanismo de autenticación y la matriz de permisos siguen pendientes.
5. **Separación control-potencia.** `B2.3-D19` aprobó una separación conceptual. B2.4 D31 requiere detectar fallas de la etapa de potencia; no selecciona arquitectura ni componente.
6. **Pruebas físicas.** `B2.3-D12` previó laboratorio y piloto industrial. B2.4 D35 exige autorización explícita antes de energizar; este documento no autoriza pruebas físicas.
7. **Prioridades.** D03 exige priorizar por riesgos y criticidad. Sin evaluación de riesgos no se asignan prioridades; se registran como pendientes.

## 8. Alcance del primer incremento y capacidades posteriores

### 8.1. Requisitos candidatos propuestos para el primer incremento

Los 39 candidatos se proponen para el primer incremento:

- **Control y operación:** RF-001–RF-014; RF-018–RF-022; RF-027.
- **Protecciones y supervisión:** RF-015–RF-017; RF-019–RF-020.
- **Configuración, recuperación y auditoría:** RF-023–RF-026.
- **Atributos de calidad:** RNF-001–RNF-005.
- **Restricciones de seguridad y verificación:** RES-001–RES-007.

La aplicabilidad de RF-014 a comunicaciones externas depende de que el primer incremento defina un enlace de comunicación. Si no existe, el requisito se aplicará solo a los enlaces internos o se registrará como **No aplica** con justificación.

### 8.2. Capacidades que permanecen para incrementos posteriores

No se asigna un incremento concreto a las siguientes capacidades:

- Soporte de más de un motor.
- Motores paso a paso, servomotores, motores AC y otros actuadores.
- Control coordinado de múltiples ejes.
- Algoritmos avanzados de optimización.
- Integración con múltiples protocolos industriales.
- Supervisión remota y arquetipos PLC/HMI/SCADA.
- Diagnóstico causal automatizado.
- Funciones de seguridad certificadas.
- Actualizaciones de firmware y piloto industrial.

Estas capacidades no se convierten en requisitos del primer incremento por aparecer en este documento.

## 9. Datos cuantitativos y decisiones técnicas pendientes

No se asignan valores numéricos. Los siguientes datos son necesarios para completar los criterios de aceptación:

| Dato pendiente | Requisitos afectados | Estado |
|---|---|---|
| Tensión, corriente y potencia nominal y máxima del motor | RF-015; RF-016; RF-019; RES-007 | Pendiente |
| Rango de velocidad y dirección permitida | RF-007; RF-018; RNF-001 | Pendiente |
| Límites y tiempos de aceleración y desaceleración | RF-005; RF-006 | Pendiente |
| Umbral y tiempo de sobrecorriente | RF-015 | Pendiente |
| Umbrales de sobretensión, subtensión y regeneración | RF-015 | Pendiente |
| Límites térmicos y tiempos de respuesta | RF-016 | Pendiente |
| Indicadores y umbrales de bloqueo y pérdida de carga | RF-017 | Pendiente |
| Umbrales de aceleración e inversión inesperadas | RF-018 | Pendiente |
| Ganancias PI, límites de salida y tiempo de saturación | RF-009; RF-010 | Pendiente |
| Filtro, frecuencia de muestreo y tiempo de datos obsoletos | RF-011; RF-014 | Pendiente |
| Umbral y tiempo de verificación de parada | RF-004 | Pendiente |
| Criterios de estabilidad, error, sobreimpulso y respuesta | RNF-001 | Pendiente |
| Matriz de criticidad y condiciones de cambio de parámetros | RF-025; RNF-004 | Pendiente |
| Retención y formato de registros de configuración y eventos | RF-026; RF-027; RNF-003 | Pendiente |
| Escala y criterios de aceptación de riesgos | RES-001; RES-002; RES-004 | Pendiente |
| Procedimiento y criterios de interrupción de pruebas | RES-003; RES-005 | Pendiente |

## 10. Decisiones adicionales necesarias

Se requieren decisiones posteriores para:

1. Definir la escala y los criterios de aceptación de riesgos.
2. Definir el estado seguro y el comportamiento requerido para cada escenario de falla.
3. Aprobar los límites eléctricos, térmicos y mecánicos del motor y del banco.
4. Aprobar los umbrales y tiempos de las protecciones.
5. Aprobar los criterios de estabilidad y desempeño del lazo de velocidad.
6. Aprobar la matriz de criticidad de parámetros y los permisos de cambio.
7. Aprobar el mecanismo de autenticación y la matriz de permisos.
8. Definir el alcance de comunicaciones del primer incremento.
9. Aprobar la política de retención y auditoría.
10. Autorizar formalmente el banco, los procedimientos y las pruebas físicas.
11. Definir la arquitectura de seguridad y la independencia de protecciones.
12. Seleccionar motor, etapa de potencia y sensores mediante decisiones técnicas posteriores, no mediante esta especificación.

## 11. Estado de los requisitos candidatos

| Familia | Cantidad | Estado |
|---|---:|---|
| `RF-###` | 27 | Propuestos |
| `RNF-###` | 5 | Propuestos |
| `RES-###` | 7 | Propuestos |
| **Total** | **39** | **Ninguno aprobado** |

Ningún candidato tiene prioridad asignada. Las prioridades se determinarán después del análisis de riesgos y de la evaluación de dependencias.

### 11.1. Trazabilidad preliminar hacia necesidades

| Requisitos | Necesidades relacionadas | Estado del vínculo |
|---|---|---|
| RF-001–RF-004 | NEC-P-01; NEC-P-02; NEC-P-07; NEC-P-08 | Preliminar |
| RF-005–RF-010 | NEC-P-01; NEC-P-02; NEC-P-09 | Preliminar |
| RF-011–RF-014 | NEC-P-02; NEC-P-03; NEC-P-07; NEC-P-08 | Preliminar |
| RF-015–RF-022 | NEC-P-03; NEC-P-07; NEC-P-08; NEC-P-09 | Preliminar |
| RF-023–RF-027 | NEC-P-03; NEC-P-04; NEC-P-05; NEC-P-09; NEC-P-10 | Preliminar |
| RNF-001 | NEC-P-02; NEC-P-09 | Preliminar |
| RNF-002–RNF-004 | NEC-P-04; NEC-P-05; NEC-P-09; NEC-P-10 | Preliminar |
| RNF-005 | NEC-P-03; NEC-P-07; NEC-P-08 | Preliminar |
| RES-001–RES-007 | NEC-P-08; NEC-P-10 | Preliminar |

Estos vínculos son de trazabilidad documental y no convierten las necesidades en requisitos aprobados.

## 12. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/01-requisitos/escenarios-uso.md`
- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`
- `docs/03-seguridad-industrial/analisis-riesgos.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`
- `docs/06-decisiones/pendientes.md`

## 13. Historial de cambios

- **0.1 — 2026-10-20 — B2.4:** consolidación de las 60 decisiones, matriz de trazabilidad, requisitos candidatos y preparación de la especificación preliminar. Documento preparado para revisión; sin aprobación documental.
