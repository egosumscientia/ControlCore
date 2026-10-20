# Consolidación de decisiones conceptuales — B2.3

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Consolidación de decisiones conceptuales — B2.3  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería conceptual  
**Fecha de formalización:** 2026-10-20  
**Aprobación documental:** Pendiente — preparado para revisión del responsable del proyecto

---

## 1. Propósito

Este documento consolida las 63 decisiones conceptuales adoptadas durante la sesión de B2.3, conserva su significado original, documenta su agrupación formal y establece la trazabilidad hacia los registros `DEC-GOB-022` a `DEC-GOB-030`.

También delimita el alcance funcional del primer incremento, distingue las capacidades objetivo que no forman parte de ese alcance y conserva los asuntos técnicos que permanecen abiertos.

## 2. Alcance y propósito de B2.3

B2.3 tiene por objeto:

1. Formalizar las decisiones conceptuales adoptadas.
2. Agrupar documentalmente las decisiones relacionadas sin perder sus identificadores de origen.
3. Delimitar el alcance funcional del primer incremento.
4. Distinguir decisiones conceptuales de requisitos concretos, arquitectura e implementación.
5. Identificar dependencias, redundancias y cuestiones abiertas.
6. Preparar la documentación para revisión y aprobación.

B2.3 no implementa hardware, firmware ni software. No selecciona componentes, microcontroladores, protocolos, lenguajes ni tecnologías. No genera requisitos `RF-###`, `RNF-###` o `RES-###` definitivos. No declara conformidad ni certificación industrial. No autoriza la implementación.

## 3. Convenciones y relación con decisiones anteriores

### 3.1. Identificadores de origen

Los identificadores `D01` a `D63` son los identificadores de origen de la sesión de B2.3. Se conservan en este documento y en la matriz de trazabilidad.

### 3.2. Identificadores formales

Las decisiones se agrupan en los registros formales `DEC-GOB-022` a `DEC-GOB-030`, incorporados en `docs/06-decisiones/registro-decisiones.md`.

La agrupación es documental. No elimina decisiones individuales, no cambia su contenido y no crea decisiones nuevas. Cada `D` tiene una correspondencia primaria con un registro `DEC-GOB`.

No se creó una tercera familia de identificadores ni se utilizó `ADR`, porque las decisiones no seleccionan una arquitectura, una tecnología ni un componente. La familia `DEC-GOB` ya se utilizaba para alcance conceptual; B2.3 amplía su descripción al comportamiento conceptual del producto.

### 3.3. Relación con las decisiones anteriores

Las decisiones `DEC-GOB-016` a `DEC-GOB-021` conservan su contenido y su estado. B2.3 no las modifica.

`DEC-GOB-022` resuelve conceptualmente la familia inicial de motores que `DEC-GOB-018` había dejado pendiente. Esta resolución es compatible con la condición de `DEC-GOB-018`; no altera su texto ni su alcance histórico.

`DEC-GOB-022` delimita funcionalmente el primer incremento que `DEC-GOB-019` había dejado pendiente de alcance exacto. Los límites cuantitativos, las interfaces, las medidas de protección y los criterios de aceptación continúan abiertos.

## 4. Resumen de la consolidación

| Registro formal | Agrupación | Decisiones de origen | Cantidad |
|---|---|---|---|
| `DEC-GOB-022` | Alcance, evolución y primer incremento | `D01`, `D04`, `D12`, `D13`, `D24`, `D25` | 6 |
| `DEC-GOB-023` | Control de movimiento y adquisición | `D02`, `D03`, `D05`, `D26`, `D27`, `D28`, `D29`, `D31`, `D32`, `D33`, `D34`, `D35` | 12 |
| `DEC-GOB-024` | Supervisión, fallas, alarmas y recuperación | `D06`, `D07`, `D11`, `D17`, `D30`, `D38`, `D46`, `D47`, `D48`, `D51`, `D54`, `D55`, `D56`, `D57` | 14 |
| `DEC-GOB-025` | Operación, mando y estados | `D08`, `D18`, `D37`, `D49`, `D50` | 5 |
| `DEC-GOB-026` | Configuración, persistencia, registros y acceso | `D09`, `D14`, `D15`, `D36`, `D39`, `D40`, `D41`, `D42`, `D43` | 9 |
| `DEC-GOB-027` | Diagnóstico, mantenimiento y actualización de firmware | `D16`, `D52`, `D53` | 3 |
| `DEC-GOB-028` | Interfaces, modularidad y simulación | `D10`, `D19`, `D20`, `D21`, `D44`, `D45` | 6 |
| `DEC-GOB-029` | Verificación, evidencia y cierre de incrementos | `D22`, `D23`, `D58`, `D59`, `D60`, `D61`, `D62` | 7 |
| `DEC-GOB-030` | Cierre de las decisiones conceptuales | `D63` | 1 |
| **Total** |  |  | **63** |

## 5. Matriz de trazabilidad de las 63 decisiones

| Origen | Contenido conservado | Registro formal | Observación |
|---|---|---|---|
| `D01` | Primera familia: motores DC con escobillas. | `DEC-GOB-022` | Resuelve la familia inicial pendiente de `DEC-GOB-018`; no selecciona modelo ni parámetros. |
| `D02` | Arranque, parada, PWM, inversión de giro y transiciones controladas. | `DEC-GOB-023` | Funciones conceptuales; no define electrónica ni temporización. |
| `D03` | Control en lazo abierto y cerrado. | `DEC-GOB-023` | No define algoritmo, ganancias ni criterios de conmutación. |
| `D04` | Arquitectura extensible a varios motores; implementación inicial con uno. | `DEC-GOB-022` | No aprueba una arquitectura concreta. |
| `D05` | Supervisión de velocidad, dirección, tensión, corriente, temperatura y anomalías. | `DEC-GOB-023` | Sensores y rangos pendientes. |
| `D06` | Detección de fallas, alarmas y eventos; sin diagnóstico causal automatizado inicial. | `DEC-GOB-024` | El diagnóstico causal automatizado queda excluido del alcance inicial. |
| `D07` | Respuestas diferenciadas ante fallas según riesgos. | `DEC-GOB-024` | Las respuestas concretas dependen del análisis de riesgos. |
| `D08` | Controles físicos locales e interfaz desde computador. | `DEC-GOB-025` | Tipos e interfaces pendientes. |
| `D09` | Persistencia de eventos y variables operativas. | `DEC-GOB-026` | Mecanismos y retención pendientes. |
| `D10` | Interfaces externas documentadas; integración industrial funcional no obligatoria inicialmente. | `DEC-GOB-028` | No selecciona protocolos ni sistemas. |
| `D11` | Recuperación configurable después de interrupciones, condicionada por riesgos. | `DEC-GOB-024` | No define estados seguros ni procedimientos. |
| `D12` | Validación de laboratorio y posterior piloto industrial. | `DEC-GOB-022` | El piloto no equivale a certificación ni autorización industrial. |
| `D13` | Implementación incremental. | `DEC-GOB-022` | No asigna capacidades a incrementos posteriores. |
| `D14` | Configuración avanzada y validada de parámetros. | `DEC-GOB-026` | Matriz de parámetros y validaciones pendiente. |
| `D15` | Perfiles de operador, técnico/integrador y administrador, con autenticación y auditoría. | `DEC-GOB-026` | Mecanismos de autenticación y permisos pendientes. |
| `D16` | Diagnóstico, mantenimiento y actualizaciones controladas y recuperables. | `DEC-GOB-027` | Mecanismos de actualización pendientes. |
| `D17` | Respuesta configurable ante pérdida de comunicaciones según riesgos. | `DEC-GOB-024` | Condicionada por el análisis de riesgos. |
| `D18` | Operación autónoma y supervisión remota, con arbitraje de comandos. | `DEC-GOB-025` | No define prioridades ni interfaces remotas. |
| `D19` | Separación de lógica de control y electrónica de potencia; parámetros eléctricos por definir. | `DEC-GOB-028` | Separación conceptual; no es una arquitectura aprobada. |
| `D20` | Simulación de motor, variables físicas, anomalías e interfaces. | `DEC-GOB-028` | No define tecnología de simulación. |
| `D21` | Simulador independiente con interfaces equivalentes a las del hardware físico. | `DEC-GOB-028` | Criterios de equivalencia pendientes. |
| `D22` | Pruebas unitarias, de integración y de sistema, incluyendo simulación de fallas. | `DEC-GOB-029` | Procedimientos y herramientas pendientes. |
| `D23` | Cierre de incrementos con implementación, documentación, trazabilidad, riesgos, pruebas, evidencias y aprobación. | `DEC-GOB-029` | La aprobación corresponde al responsable del proyecto. |
| `D24` | Mantener el alcance objetivo de la primera versión, distribuido entre incrementos verificables. | `DEC-GOB-022` | No asigna secuencia a incrementos posteriores. |
| `D25` | Primer incremento: un motor DC, arranque/parada, velocidad, inversión, medición y control abierto/cerrado. | `DEC-GOB-022` | Alcance funcional conceptual; detalles cuantitativos pendientes. |
| `D26` | Arquitectura extensible de algoritmos; implementación inicial PI. | `DEC-GOB-023` | No selecciona plataforma ni parámetros. |
| `D27` | Limitación de salida del PI con anti-windup. | `DEC-GOB-023` | Límites y ganancias pendientes. |
| `D28` | Interfaz compatible con distintos sensores de velocidad. | `DEC-GOB-023` | Sensores concretos pendientes. |
| `D29` | Filtrado configurable de velocidad medida. | `DEC-GOB-023` | Tipo y parámetros de filtro pendientes. |
| `D30` | Respuesta ante pérdida de realimentación según riesgos. | `DEC-GOB-024` | Condicionada por el análisis de riesgos. |
| `D31` | Rampas configurables de aceleración y desaceleración. | `DEC-GOB-023` | Rangos y validación pendientes. |
| `D32` | Inversión de giro configurable y condicionada por riesgos. | `DEC-GOB-023` | Condiciones de habilitación pendientes. |
| `D33` | Límites de velocidad configurables, validados y sujetos a permisos. | `DEC-GOB-023` | Valores, permisos y validación pendientes. |
| `D34` | Transición supervisada entre lazo abierto y cerrado. | `DEC-GOB-023` | Criterios de transición pendientes. |
| `D35` | Ajuste manual y asistido del PI, con validación. | `DEC-GOB-023` | Procedimiento y criterios pendientes. |
| `D36` | Persistencia de parámetros con integridad y recuperación. | `DEC-GOB-026` | Tecnología y mecanismos pendientes. |
| `D37` | Arranque supervisado. | `DEC-GOB-025` | Condiciones y estados pendientes. |
| `D38` | Watchdog, detección de fallas internas y recuperación según riesgos. | `DEC-GOB-024` | Condicionada por el análisis de riesgos. |
| `D39` | Registros diagnósticos con contexto e historial. | `DEC-GOB-026` | Formato y contenido pendientes. |
| `D40` | Reloj interno con sincronización externa opcional y detección de cambios horarios. | `DEC-GOB-026` | Fuente y protocolo de sincronización pendientes. |
| `D41` | Retención configurable y gestión del almacenamiento lleno. | `DEC-GOB-026` | Períodos y política de almacenamiento pendientes. |
| `D42` | Integridad, auditoría y control de acceso a registros. | `DEC-GOB-026` | Mecanismos pendientes. |
| `D43` | Exportación manual y automática mediante formatos documentados. | `DEC-GOB-026` | Formatos y automatización pendientes. |
| `D44` | Interfaces desacopladas, documentadas y verificables. | `DEC-GOB-028` | No define interfaces concretas. |
| `D45` | Versionado y compatibilidad de interfaces. | `DEC-GOB-028` | Esquema de versionado pendiente. |
| `D46` | Gestión configurable de errores de comunicación. | `DEC-GOB-024` | Condicionada por el análisis de riesgos. |
| `D47` | Ejecución determinista, prioridades y supervisión temporal. | `DEC-GOB-024` | Plataforma y tiempos pendientes. |
| `D48` | Respuesta a incumplimientos temporales según criticidad y riesgos. | `DEC-GOB-024` | Umbrales y respuestas pendientes. |
| `D49` | Máquina de estados supervisada. | `DEC-GOB-025` | Estados y transiciones pendientes. |
| `D50` | Arbitraje supervisado de comandos. | `DEC-GOB-025` | Política de prioridades pendiente. |
| `D51` | Recuperación supervisada tras pérdida de alimentación. | `DEC-GOB-024` | Condicionada por el análisis de riesgos. |
| `D52` | Actualización verificable y recuperable del firmware. | `DEC-GOB-027` | Transporte, firma y reversión pendientes. |
| `D53` | Diagnóstico integral del firmware. | `DEC-GOB-027` | Cobertura y mecanismos pendientes; no implica diagnóstico causal automatizado. |
| `D54` | Autodiagnóstico supervisado antes de habilitar el motor. | `DEC-GOB-024` | Condiciones y cobertura pendientes. |
| `D55` | Validación integral de comandos. | `DEC-GOB-024` | Reglas y límites pendientes. |
| `D56` | Alarmas clasificadas por severidad, reconocimiento y condiciones de restablecimiento. | `DEC-GOB-024` | Categorías y condiciones pendientes. |
| `D57` | Historial auditable de alarmas. | `DEC-GOB-024` | Formato y retención pendientes. |
| `D58` | Pruebas automatizadas en simulación y pruebas físicas controladas. | `DEC-GOB-029` | Herramientas y banco pendientes. |
| `D59` | Validación automática, evidencias trazables y revisión de anomalías. | `DEC-GOB-029` | Criterios y formatos pendientes. |
| `D60` | Cobertura de pruebas basada en requisitos y riesgos. | `DEC-GOB-029` | Umbrales pendientes. |
| `D61` | Trazabilidad entre requisitos, riesgos, pruebas, resultados y evidencias. | `DEC-GOB-029` | Esquema de identificadores pendiente. |
| `D62` | Gestión de cambios con análisis de impacto, riesgos y regresión. | `DEC-GOB-029` | Procedimiento pendiente. |
| `D63` | Cerrar las decisiones conceptuales, revisar coherencia y redundancias y preparar formalización documental. | `DEC-GOB-030` | Cierre documental; no crea decisiones técnicas nuevas. |

## 6. Alcance funcional del primer incremento

### 6.1. Alcance aprobado

El primer incremento comprende, conceptualmente:

- Un motor DC con escobillas.
- Arranque y parada.
- Control por PWM.
- Regulación de velocidad.
- Inversión controlada del sentido de giro.
- Medición de velocidad.
- Control en lazo abierto y en lazo cerrado.
- Controlador PI con anti-windup.
- Filtrado configurable de la velocidad medida.
- Rampas configurables de aceleración y desaceleración.
- Transiciones supervisadas entre lazo abierto y cerrado.
- Límites operativos validados y sujetos a permisos.

Este alcance es funcional y conceptual. No define valores cuantitativos, electrónica, sensores, plataforma de control, interfaces concretas ni medidas de protección.

### 6.2. Condiciones del primer incremento

- Las medidas de protección necesarias deberán derivarse del análisis de riesgos correspondiente.
- No se asumirá que detener el motor o cortar su alimentación sea siempre un estado seguro.
- La inversión de giro y las respuestas ante fallas estarán condicionadas por la evaluación de riesgos.
- Los límites operativos requerirán validación y permisos; sus valores permanecen pendientes.
- El primer incremento no queda exento del cumplimiento de los criterios de verificación y cierre de `DEC-GOB-029`.
- La implementación del primer incremento no está autorizada por este documento.

### 6.3. Distinción respecto de las capacidades objetivo

Las capacidades objetivo de la primera versión y de la evolución del producto no quedan automáticamente incluidas en el primer incremento. Tampoco se asigna a los incrementos posteriores un contenido específico, salvo que una decisión posterior lo establezca.

## 7. Capacidades objetivo y capacidades pendientes de implementación

Las siguientes capacidades forman parte del alcance objetivo o de la evolución conceptual, pero no están incluidas en el alcance funcional explícito del primer incremento. Su asignación a incrementos posteriores no está aprobada.

| Capacidad | Estado | Referencia |
|---|---|---|
| Soporte de más de un motor | Objetivo de extensibilidad; implementación inicial con uno. | `D04`, `D25`; `DEC-GOB-022` |
| Motores paso a paso, servomotores, motores AC y otros actuadores | Objetivo de extensibilidad; no incluidos en el primer incremento. | `DEC-GOB-018`; `DEC-GOB-022` |
| Control coordinado de múltiples ejes | Excluido de la primera versión. | `DEC-GOB-019` |
| Algoritmos avanzados de optimización | Excluidos de la primera versión. | `DEC-GOB-019` |
| Integración con múltiples protocolos industriales | Excluida de la primera versión. | `DEC-GOB-019` |
| Funciones de seguridad certificadas | Excluidas mientras no exista el proceso de análisis y conformidad. | `DEC-GOB-017`; `DEC-GOB-019` |
| Diagnóstico causal automatizado | Excluido del alcance inicial. | `D06`; `DEC-GOB-024` |
| Supervisión, alarmas y recuperación | Capacidad objetivo; no incluida explícitamente en el alcance funcional del primer incremento; respuestas condicionadas por riesgos. | `D05`, `D06`, `D07`, `D11`, `D17`, `D30`, `D38`, `D46` a `D48`, `D51`, `D54` a `D57`; `DEC-GOB-024` |
| Operación local, supervisión remota y arbitraje | Capacidad objetivo; interfaces, prioridades y política de arbitraje pendientes. | `D08`, `D18`, `D37`, `D49`, `D50`; `DEC-GOB-025` |
| Configuración avanzada y ajuste del PI | Capacidad objetivo; no incluida explícitamente en el alcance funcional del primer incremento; procedimientos pendientes. | `D14`, `D35`; `DEC-GOB-023`, `DEC-GOB-026` |
| Diagnóstico y mantenimiento | Capacidad objetivo; mecanismos y cobertura pendientes. | `D16`, `D53`; `DEC-GOB-027` |
| Persistencia, retención y exportación de información | Capacidad objetivo; mecanismos pendientes. | `D09`, `D39`, `D41`, `D43`; `DEC-GOB-026` |
| Autenticación, perfiles y auditoría | Capacidad objetivo; mecanismos y matriz de permisos pendientes. | `D15`, `D42`; `DEC-GOB-026` |
| Actualización de firmware verificable y recuperable | Capacidad objetivo; mecanismo pendiente. | `D52`; `DEC-GOB-027` |
| Simulador independiente | Capacidad de verificación; implementación pendiente. | `D20`, `D21`; `DEC-GOB-028` |
| Piloto industrial | Etapa posterior a la validación de laboratorio; no iniciada. | `D12`; `DEC-GOB-022` |

## 8. Dependencias y asuntos técnicos abiertos

| Asunto | Estado | Dependencia |
|---|---|---|
| Modelo, tensión, corriente y potencia del motor DC | Abierto. La familia está definida; el componente no. | `D01`, `D25`; `DEC-GOB-022` |
| Electrónica de potencia, aislamiento y protecciones eléctricas | Abierto. Solo se aprobó la separación conceptual. | `D19`; `DEC-GOB-028` |
| Sensor de velocidad, interfaz y rango de medición | Abierto. Se aprobó compatibilidad con distintos sensores. | `D28`; `DEC-GOB-023` |
| Prestaciones cuantitativas de control | Abierto. No hay rangos, precisiones, tiempos ni frecuencias aprobados. | `D25`, `D27`, `D29`, `D31`, `D33`; `DEC-GOB-022`, `DEC-GOB-023` |
| Análisis de riesgos, estados seguros y arquitectura de seguridad | Abierto. No se asume que detener el motor sea seguro. | `D07`, `D11`, `D17`, `D30`, `D38`, `D48`, `D51`; `DEC-GOB-017`, `DEC-GOB-024` |
| Interfaces locales, interfaz de computador y protocolos externos | Abierto. Solo se aprobaron interfaces documentadas y desacopladas. | `D08`, `D10`, `D18`, `D44`, `D45`; `DEC-GOB-025`, `DEC-GOB-028` |
| Criterios de alarmas, arbitraje y transición | Abierto. Severidades, reconocimiento, restablecimiento, prioridades de mando y criterios de conmutación no están definidos. | `D18`, `D34`, `D49`, `D50`, `D56`, `D57`; `DEC-GOB-023`, `DEC-GOB-024`, `DEC-GOB-025` |
| Plataforma de control, lenguaje, sistema operativo y herramientas | Abierto. No se ha seleccionado tecnología. | `D19`, `D26`, `D47`; `DEC-GOB-023`, `DEC-GOB-024`, `DEC-GOB-028` |
| Banco de pruebas, instrumentación y criterios de aceptación | Abierto. La estrategia es conceptual. | `D22`, `D58`, `D59`, `D60`, `D61`; `DEC-GOB-029` |
| Autenticación, matriz de permisos y auditoría | Abierto. Los perfiles están aprobados; los mecanismos no. | `D15`, `D42`; `DEC-GOB-026` |
| Retención, almacenamiento y formatos de exportación | Abierto. La necesidad está aprobada; los valores no. | `D09`, `D39`, `D41`, `D43`; `DEC-GOB-026` |
| Actualización de firmware: transporte, firma y reversión | Abierto. La verificabilidad y recuperabilidad son requisitos conceptuales. | `D52`; `DEC-GOB-027` |
| Condiciones eléctricas, ambientales y de compatibilidad electromagnética | Abierto. El entorno industrial está aprobado; los rangos no. | `DEC-GOB-018` |
| Aplicación y sitio del piloto industrial | Abierto. No se ha seleccionado una máquina o instalación. | `D12`; `DEC-GOB-022` |
| Secuencia y contenido de incrementos posteriores | Abierto. No se asigna alcance a incrementos no aprobados. | `D13`, `D24`; `DEC-GOB-022` |

Estos asuntos no son decisiones aprobadas. Deberán resolverse antes de implementar el alcance afectado. Las respuestas que correspondan a decisiones arquitectónicas o técnicas deberán registrarse como `ADR`; las que correspondan a alcance o gobierno, como `DEC-GOB`.

## 9. Redundancias y relaciones resueltas

La consolidación identificó las siguientes relaciones. No se eliminó ninguna decisión.

| Relación | Tratamiento |
|---|---|
| `D06` con `D16`, `D39`, `D53`, `D54` | `D06` excluye el diagnóstico causal automatizado inicial. `D16`, `D39`, `D53` y `D54` describen mantenimiento, registros, diagnóstico de firmware y autodiagnóstico; no equivalen a diagnóstico causal automatizado. |
| `D07`, `D11`, `D17`, `D30`, `D38`, `D46`, `D48`, `D51` | Se agrupan como respuestas condicionadas por riesgos. No se duplica una misma respuesta concreta; cada una cubre una condición distinta. Las respuestas concretas permanecen abiertas. |
| `D09`, `D36`, `D39`, `D41`, `D42`, `D43` | Se distinguen variables y eventos operativos, parámetros, registros diagnósticos, retención, integridad y exportación. Son aspectos complementarios, no duplicados. |
| `D10`, `D44`, `D45` | `D10` define el alcance de las interfaces externas; `D44`, su calidad; `D45`, su versionado. |
| `D20` con `D21` | `D20` establece la capacidad de simulación; `D21` exige un simulador independiente con interfaces equivalentes. `D21` especializa `D20`. |
| `D22`, `D58`, `D59`, `D60`, `D61` | Cubren niveles de prueba, automatización, evidencias, cobertura y trazabilidad. Son complementarios. |
| `D23` con `D62` | `D23` define el cierre de un incremento; `D62`, la gestión de cambios. No son equivalentes. |
| `D25` con `D26`, `D27`, `D29`, `D31`, `D33`, `D34`, `D35` | `D25` delimita el primer incremento; las demás detallan funciones de control. No hay contradicción. |
| `D04` con `D25` | `D04` exige extensibilidad; `D25` implementa inicialmente un motor. No hay contradicción. |
| `D01` con `DEC-GOB-018` | `D01` resuelve la familia inicial que `DEC-GOB-018` había dejado pendiente. No modifica el registro anterior. |
| `D18` con `D10` | La supervisión remota es una capacidad conceptual; no obliga a integrar protocolos industriales específicos. La interfaz concreta permanece abierta. |
| `D12` con `D58` | `D12` define la secuencia laboratorio-piloto; `D58`, los métodos de prueba. Son complementarios. |

## 10. Contradicciones y asuntos abiertos

No se identificaron contradicciones sustantivas entre las 63 decisiones.

Se identifican las siguientes precisiones necesarias:

1. **Familia inicial frente a `DEC-GOB-018`.** `DEC-GOB-018` dejó pendiente el soporte inicial concreto. `D01` lo resuelve conceptualmente con motores DC con escobillas. La decisión anterior no se modifica; se interpreta que su condición pendiente quedó atendida.
2. **Alcance del primer incremento frente a `DEC-GOB-019`.** `DEC-GOB-019` dejó pendiente el alcance exacto del primer incremento. `D25` y la sección 6 lo delimitan funcionalmente. Los límites cuantitativos, las interfaces y las medidas de protección siguen abiertos.
3. **Diagnóstico integral frente a exclusión de diagnóstico causal.** `D53` exige diagnóstico integral del firmware; `D06` excluye el diagnóstico causal automatizado inicial. Se interpreta que `D53` cubre la capacidad de diagnóstico del firmware, no la generación automática de causas.
4. **Operación autónoma y supervisión remota frente a integración industrial no obligatoria.** `D18` no convierte en obligatoria la integración con PLC, HMI o SCADA. La interfaz remota concreta permanece pendiente.
5. **Perfiles funcionales frente a actores organizacionales.** `D15` aprueba perfiles de acceso; no los asigna a los actores `ACT-P-01` a `ACT-P-07`. La asignación y la matriz de permisos siguen pendientes.
6. **Separación control-potencia frente a arquitectura no aprobada.** `D19` es una separación conceptual de responsabilidades; no constituye una arquitectura eléctrica, mecánica o de seguridad aprobada.
7. **Seguridad.** Ninguna decisión de B2.3 aprueba funciones de seguridad, estados seguros, niveles de integridad o conformidad. Las medidas de protección deberán derivarse del análisis de riesgos.

## 11. Distinción entre decisión conceptual, requisito y especificación

| Nivel | Qué representa en B2.3 | Qué no representa |
|---|---|---|
| Decisión conceptual | Alcance, comportamiento y criterios generales aprobados (`D01` a `D63`; `DEC-GOB-022` a `DEC-GOB-030`). | No es un requisito verificable ni una especificación de implementación. |
| Requisito concreto | Enunciado verificable con criterio de aceptación y método de verificación (`RF`, `RNF`, `RES`). | No ha sido definido ni aprobado en B2.3. |
| Arquitectura | Estructura de hardware, firmware, software e interfaces, con decisiones `ADR`. | No ha sido seleccionada ni aprobada. |
| Implementación | Hardware, firmware o software construido y probado. | No está autorizada. |
| Verificación y validación | Pruebas y evidencia conforme a criterios aprobados. | No se ha ejecutado. |
| Conformidad o certificación | Evaluación frente a normas aplicables. | No se declara. |

## 12. Estado documental y aprobaciones

| Documento | Versión | Estado |
|---|---|---|
| `docs/06-decisiones/consolidacion-decisiones-B2.3.md` | 0.1 | Propuesta para aprobación — pendiente de revisión. |
| `docs/06-decisiones/registro-decisiones.md` | 0.3 | Registro actualizado con `DEC-GOB-022` a `DEC-GOB-030`; decisiones conceptuales aprobadas por el responsable del proyecto; documento pendiente de revisión. |
| `docs/06-decisiones/pendientes.md` | 0.3 | Actualizado con las resoluciones conceptuales de B2.3 y los asuntos abiertos. |
| `docs/01-requisitos/README.md` | 0.2 | Actualización de estado y referencia a B2.3; pendiente de aprobación. |
| `docs/01-requisitos/necesidades-producto.md` | 0.3 | Actualización de referencias de estado; pendiente de aprobación. |
| `docs/01-requisitos/escenarios-uso.md` | 0.3 | Actualización de referencias de estado; pendiente de aprobación. |
| `docs/01-requisitos/actores-uso.md` | 0.2 | Sin cambios; no contenía referencias de estado afectadas por B2.3. |
| `docs/00-gobierno/ESTADO-ACTUAL.md` | 0.11 | Bitácora actualizada con B2.3; pendiente de revisión. |

Las decisiones `D01` a `D63` fueron adoptadas por el responsable del proyecto en la sesión de B2.3. Su registro documental se preparó para revisión. La aprobación del documento de consolidación, de las actualizaciones de los documentos de requisitos y de la bitácora no se presume por la incorporación de los cambios al árbol de trabajo.

## 13. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md` (secciones 9, 10, 11, 24 y 25)
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/01-requisitos/escenarios-uso.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`
- `docs/02-arquitectura/` (futuro)
- `docs/03-seguridad-industrial/` (futuro)
- `docs/05-validacion/` (futuro)

## 14. Historial de cambios

- **0.1 — 2026-10-20 — B2.3:** consolidación de las 63 decisiones conceptuales, agrupación en `DEC-GOB-022` a `DEC-GOB-030`, delimitación funcional del primer incremento y registro de asuntos abiertos. Documento preparado para revisión; sin aprobación documental.
