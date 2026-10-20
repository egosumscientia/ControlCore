
# Estado actual del proyecto — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Fecha de actualización:** 2026-10-20
**Versión del documento:** 0.12
**Fase actual:** Ingeniería de requisitos (B2)
**Bloque:** B2.4 — Consolidación de decisiones y especificación preliminar
**Estado del bloque:** Decisiones consolidadas; 39 requisitos candidatos propuestos; requisitos no aprobados
**Gobierno documental:** Aprobado — DEC-GOB-009 (2026-10-19)
**Convenciones de requisitos:** Aprobadas — DEC-GOB-010 a DEC-GOB-015
**Necesidades, actores y escenarios:** Aprobados — DEC-GOB-016 (2026-10-20)
**Decisiones conceptuales:** Aprobadas — DEC-GOB-017 a DEC-GOB-021; consolidadas — DEC-GOB-022 a DEC-GOB-030 (B2.3)
**Decisiones B2.4:** D01–D60 consolidadas en documento de propuesta
**Requisitos candidatos:** 27 RF, 5 RNF y 7 RES — propuestos, no aprobados
**Arquitectura:** No definida
**Implementación:** No autorizada

---

## 1. Propósito

Este documento constituye la bitácora de continuidad del proyecto ControlCore.

Su función es registrar el estado de ingeniería al finalizar cada sesión de trabajo, permitiendo retomar el proyecto sin perder las decisiones adoptadas, los avances realizados y los asuntos pendientes.

El repositorio constituye la fuente documental de referencia.

Este archivo deberá actualizarse al cierre de cada sesión relevante, después de realizar las actividades de ingeniería correspondientes.

No sustituye los documentos de requisitos, arquitectura, decisiones técnicas ni validación.

## 2. Visión del producto

ControlCore es una plataforma modular de control y supervisión industrial desarrollada por makeAutomatic.

Su propósito es permitir el desarrollo de soluciones profesionales para control, supervisión y diagnóstico de motores y actuadores utilizados en aplicaciones industriales.

El producto deberá evolucionar mediante un proceso estructurado de ingeniería, desde el diseño conceptual y las pruebas de laboratorio hasta posibles aplicaciones comerciales.

ControlCore no es un ejercicio académico ni un prototipo destinado únicamente a demostrar funcionalidades.

Su desarrollo deberá responder a criterios de:

- Seguridad industrial.
- Confiabilidad.
- Robustez eléctrica y electrónica.
- Calidad de hardware, firmware y software.
- Modularidad.
- Mantenibilidad.
- Trazabilidad.
- Verificabilidad.
- Integración industrial.
- Calidad comercial.

Las capacidades concretas y las tecnologías del producto deberán definirse durante las fases correspondientes.

## 3. Estado general

El proyecto se encuentra en la etapa de gobierno documental aprobado, gestión de requisitos aprobada, necesidades, actores y escenarios aprobados, decisiones conceptuales consolidadas y requisitos candidatos propuestos. Los requisitos concretos permanecen pendientes de aprobación.

El trabajo documental de gobierno comprende los cinco documentos sustantivos, aprobados en versión 0.1:

1. Visión del producto.
2. Principios de ingeniería.
3. Metodología de diseño.
4. Criterios de calidad.
5. Definición de terminado.

Los procedimientos de revisión y aceptación quedan establecidos en esos documentos.

El gobierno documental aprobado establece la base técnica y metodológica para el diseño detallado y la implementación futura.

Durante la sesión del 19 de octubre de 2026 se consolidó el gobierno documental (bloque B1): se revisaron y armonizaron los documentos de visión, principios, metodología, criterios de calidad y definición de terminado, y se actualizó esta bitácora. La consolidación documental no equivale a aprobación formal.

En la misma fecha se ejecutó el bloque B1.1: se generalizaron las reglas de agentes en `README.md` y `AGENTS.md`, se creó el directorio `docs/04-modulos/` con su índice inicial y se incorporaron las reglas DEC-GOB-001 a DEC-GOB-007 al registro formal de decisiones. Los cinco documentos sustantivos de gobierno permanecían como propuestas al cierre de B1.1.

También en esa fecha se ejecutó el bloque B1.2: se generalizaron las referencias de herramienta de `docs/00-gobierno/metodologia-diseno.md`, se registró DEC-GOB-008 y se realizó la auditoría integral de los cinco documentos sustantivos de gobierno. Las correcciones aplicadas son editoriales y no modifican decisiones, obligaciones ni alcance. Los cinco documentos permanecían en estado **Propuesta para aprobación** al cierre de B1.2.

En la misma fecha se ejecutó el bloque B1.3, autorizado por el responsable del proyecto, para resolver los hallazgos H-03 a H-06 de la auditoría: normalización de referencias internas, diferenciación de estados, armonización del esquema DEC-GOB/ADR y unificación de metadatos. No se modificaron decisiones técnicas, requisitos del producto, obligaciones sustantivas ni estados de aprobación.

En la misma fecha se ejecutó el bloque B1.4: el responsable del proyecto aprobó formalmente los cinco documentos de gobierno en versión 0.1, con base en la auditoría B1 versión 0.2, sin condiciones documentales pendientes. La aprobación se registró como DEC-GOB-009 y establece la línea base documental para iniciar la ingeniería de requisitos (B2). La implementación de hardware, firmware y software continúa no autorizada.

En la misma fecha se inició B2 con el bloque B2.1: se estableció la estructura documental de requisitos, el esquema propuesto de identificación, los atributos, los estados y los mecanismos de trazabilidad. No se definieron requisitos concretos ni se aprobaron convenciones. La arquitectura no está definida y la implementación no está autorizada.

En la misma fecha se ejecutó B2.1.1: el responsable del proyecto aprobó las seis decisiones de gestión de requisitos, registradas como DEC-GOB-010 a DEC-GOB-015, y los cuatro documentos de requisitos en versión 0.1. No se definieron requisitos concretos; la arquitectura no está definida y la implementación no está autorizada.

En la misma fecha se inició B2.2 con el bloque B2.2.1: se identificaron diez necesidades candidatas, siete actores y diez escenarios de uso, y se consolidaron quince preguntas abiertas. Los documentos quedaron como propuestas pendientes de validación y aprobación. No se definieron requisitos concretos; la arquitectura no está definida y la implementación no está autorizada.

El 20 de octubre de 2026 se ejecutó B2.2.2: el responsable del proyecto formalizó la aprobación de las diez necesidades, los siete actores y los diez escenarios, registrada como DEC-GOB-016, y las respuestas a las quince preguntas PREG-P-01 a PREG-P-15, registradas como DEC-GOB-017 a DEC-GOB-021. Las decisiones son conceptuales: no constituyen requisitos concretos, arquitectura, selección tecnológica, certificación ni autorización de implementación.

En la misma fecha se ejecutó B2.3: se consolidaron las 63 decisiones conceptuales de la sesión, agrupadas en DEC-GOB-022 a DEC-GOB-030, se delimitó funcionalmente el primer incremento y se actualizaron los asuntos técnicos abiertos. Las decisiones conceptuales no constituyen requisitos concretos, arquitectura aprobada, selección tecnológica, certificación ni autorización de implementación.

En la misma fecha se ejecutó B2.4: se consolidaron las 60 decisiones de la ronda posterior a B2.3, se preparó el análisis preliminar de riesgos y se propusieron 27 requisitos funcionales, 5 no funcionales y 7 restricciones candidatas. Los candidatos están en estado **Propuesto**, no aprobados, y no autorizan pruebas físicas ni implementación.

No se ha aprobado todavía una arquitectura definitiva.

No se ha autorizado la implementación del producto.

No deben asumirse como seleccionados componentes electrónicos, microcontroladores, protocolos, lenguajes de programación o tecnologías específicas que no cuenten con una decisión documentada.

## 4. Documentación de gobierno

### 4.1. Documentos existentes y con contenido verificado

En la revisión del repositorio realizada el 19 de octubre de 2026 se confirmó la existencia y el contenido de:

- `README.md` — descripción general y organización del repositorio.
- `AGENTS.md` — contrato operativo para agentes de IA.
- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/criterios-calidad.md`
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`

Durante B1.1 se incorporaron además:

- `docs/04-modulos/README.md` — índice inicial del directorio de módulos.
- `docs/06-decisiones/registro-decisiones.md` — registro formal de decisiones de gobierno.

Durante B1.2 se incorporó:

- `docs/00-gobierno/auditoria-gobierno-B1.md` — informe de auditoría integral del gobierno documental, actualizado en B1.3 y B1.4.

`README.md` y `AGENTS.md` no fueron modificados durante B1; fueron actualizados en B1.1 para generalizar las reglas de agentes.

Los cinco documentos sustantivos de gobierno se encuentran en estado **Aprobado** en versión 0.1, conforme a DEC-GOB-009. Esta bitácora es un registro de continuidad y no un documento de aprobación.

### 4.2. Estado de incorporación, aprobación y registro

Los documentos de gobierno se encuentran incorporados al repositorio y versionados mediante Git. Su incorporación y publicación no constituyen aprobación formal.

La aprobación formal de los cinco documentos fue otorgada de forma expresa por el responsable del proyecto el 2026-10-19, conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 24). El registro se encuentra en DEC-GOB-009.

El registro formal `docs/06-decisiones/registro-decisiones.md` contiene las reglas DEC-GOB-001 a DEC-GOB-007 y las decisiones aprobadas DEC-GOB-008 a DEC-GOB-030. DEC-GOB-009 registra la aprobación de la línea base de gobierno documental; DEC-GOB-010 a DEC-GOB-015, la línea base de gestión de requisitos; DEC-GOB-016, la aprobación de necesidades, actores y escenarios; DEC-GOB-017 a DEC-GOB-021, las respuestas a PREG-P-01 a PREG-P-15; y DEC-GOB-022 a DEC-GOB-030, la consolidación de las decisiones conceptuales de B2.3.

La consolidación, la matriz de las 63 decisiones y el alcance funcional del primer incremento se documentan en `docs/06-decisiones/consolidacion-decisiones-B2.3.md`.

Las 60 decisiones de B2.4 se documentan en `docs/06-decisiones/consolidacion-decisiones-B2.4.md` con referencias `B2.4-D01` a `B2.4-D60`. No reciben identificadores `DEC-GOB` adicionales porque son criterios técnicos y metodológicos ya aprobados; su consolidación es documental.

Las aprobaciones futuras de documentos requerirán el mismo registro expreso.

El directorio `docs/04-modulos/` fue creado con un archivo índice que describe su propósito y su estado pendiente. No contiene especificaciones de módulos.

### 4.3. Documentos pendientes de contenido

Permanecen sin contenido:

- `docs/02-arquitectura/` — arquitectura general, hardware, firmware, software e interfaces.
- `docs/03-seguridad-industrial/normas-aplicables.md` y `docs/03-seguridad-industrial/requisitos-seguridad.md` — evaluación normativa y requisitos de seguridad específicos. `analisis-riesgos.md` contiene una propuesta preliminar.
- `docs/05-validacion/` — estrategia de pruebas, criterios de aceptación y registro de validaciones.
- `docs/07-roadmap/` — fases y planificación de implementación.
- `docs/08-prompts/` — contratos e instrucciones de trabajo para agentes.
- `docs/04-modulos/` — solo el índice inicial; no contiene especificaciones de módulos.

Los archivos vacíos no deberán interpretarse como especificaciones ni decisiones aprobadas.

`docs/06-decisiones/pendientes.md` contiene los asuntos de B2.1, B2.2.1 y B2.3 resueltos, los datos técnicos pendientes de B2.4 y las preguntas que permanecen abiertas. No es un documento vacío.

La referencia del `README.md` a `docs/04-modulos/` quedó resuelta con la creación del directorio y su índice.

### 4.4. Función de esta bitácora

`docs/00-gobierno/ESTADO-ACTUAL.md` registra la continuidad del proyecto y facilita el inicio de nuevas sesiones de ingeniería.

Su actualización no sustituye los registros formales de decisiones ni constituye aprobación de documentos, decisiones o entregables.

### 4.5. Línea base documental

La línea base de gobierno documental, aprobada el 2026-10-19, está constituida por:

- `docs/00-gobierno/vision-producto.md` — versión 0.1.
- `docs/00-gobierno/principios-ingenieria.md` — versión 0.1.
- `docs/00-gobierno/metodologia-diseno.md` — versión 0.1.
- `docs/00-gobierno/criterios-calidad.md` — versión 0.1.
- `docs/00-gobierno/definicion-de-terminado.md` — versión 0.1.

**Fundamento:** auditoría B1, versión 0.2, sin hallazgos bloqueantes ni pendientes de H-01 a H-06.

**Registro:** DEC-GOB-009.

La línea base habilita el inicio de la ingeniería de requisitos (B2). No autoriza la implementación de hardware, firmware o software.

### 4.6. Línea base de gestión de requisitos

La línea base de gestión de requisitos fue aprobada en B2.1.1:

- `docs/01-requisitos/README.md` — índice y convenciones comunes.
- `docs/01-requisitos/requisitos-funcionales.md` — registro de RF.
- `docs/01-requisitos/requisitos-no-funcionales.md` — registro de RNF.
- `docs/01-requisitos/restricciones-sistema.md` — registro de RES.

Estado: aprobados en versión 0.1 el 2026-10-19 (DEC-GOB-015). Incorporan las decisiones DEC-GOB-010 a DEC-GOB-014.

No contienen requisitos concretos, identificadores asignados ni línea base de requisitos concretos.

El registro histórico de asuntos resueltos se encuentra en `docs/06-decisiones/pendientes.md`.

### 4.7. Documentos de necesidades, actores y escenarios

En B2.2.1 se incorporaron como propuestas:

- `docs/01-requisitos/necesidades-producto.md` — diez necesidades y quince preguntas priorizadas.
- `docs/01-requisitos/actores-uso.md` — siete actores y sus responsabilidades.
- `docs/01-requisitos/escenarios-uso.md` — diez escenarios de uso.

En B2.2.2 fueron aprobados en versión 0.2 (DEC-GOB-016):

- Las diez necesidades `NEC-P-01` a `NEC-P-10`.
- Los siete actores `ACT-P-01` a `ACT-P-07` y sus responsabilidades generales.
- Los diez escenarios `ESC-P-01` a `ESC-P-10` como base conceptual de ingeniería.

Estado: **Aprobado**. Contienen necesidades, actores y escenarios aprobados como base conceptual. No contienen requisitos `RF-###`, `RNF-###` o `RES-###`, no constituyen una línea base de requisitos concretos y no sustituyen la línea base de gestión de requisitos.

En B2.3 se actualizaron únicamente las referencias de estado afectadas por `DEC-GOB-022` a `DEC-GOB-030`:

- `docs/01-requisitos/necesidades-producto.md` — versión 0.3, estado **Revisión de documento aprobado**, pendiente de aprobación.
- `docs/01-requisitos/escenarios-uso.md` — versión 0.3, estado **Revisión de documento aprobado**, pendiente de aprobación.
- `docs/01-requisitos/README.md` — versión 0.2, estado **Revisión de documento aprobado**, pendiente de aprobación.
- `docs/01-requisitos/actores-uso.md` — versión 0.2, sin cambios; no contenía referencias de estado afectadas por B2.3.

Se incorporó `docs/06-decisiones/consolidacion-decisiones-B2.3.md` como documento de consolidación, trazabilidad y delimitación del primer incremento, en estado **Propuesta para aprobación**.

### 4.8. Documentos de B2.4

En B2.4 se incorporaron o actualizaron como propuestas:

- `docs/06-decisiones/consolidacion-decisiones-B2.4.md` — consolidación de las 60 decisiones y matriz de trazabilidad.
- `docs/03-seguridad-industrial/analisis-riesgos.md` — estructura preliminar de peligros, FMEA y funciones de protección.
- `docs/01-requisitos/requisitos-funcionales.md` — 27 requisitos candidatos.
- `docs/01-requisitos/requisitos-no-funcionales.md` — 5 requisitos candidatos.
- `docs/01-requisitos/restricciones-sistema.md` — 7 restricciones candidatas.
- `docs/01-requisitos/README.md` — actualización de estado y referencias.
- `docs/06-decisiones/registro-decisiones.md` — referencia a la consolidación B2.4; sin nuevos `DEC-GOB`.
- `docs/06-decisiones/pendientes.md` — datos técnicos pendientes de B2.4.
- `docs/01-requisitos/necesidades-producto.md` — versión 0.4, actualización de referencias de estado.
- `docs/01-requisitos/escenarios-uso.md` — versión 0.4, actualización de referencias de estado.
- `docs/01-requisitos/actores-uso.md` — versión 0.3, actualización de referencias de estado.

Los tres registros de requisitos conservan la aprobación de su estructura en versión 0.1; sus versiones 0.2 están en **Revisión de documento aprobado**. El índice está en versión 0.3; las necesidades y los escenarios, en 0.4; los actores, en 0.3. Todos están pendientes de aprobación. Los 39 candidatos están en estado **Propuesto**.

## 5. Metodología de ingeniería

ControlCore seguirá una metodología de diseño previo e implementación incremental.

Las decisiones técnicas relevantes se desarrollarán mediante rondas estructuradas de análisis.

La metodología contempla la presentación de alternativas A, B y C, incluyendo sus ventajas, desventajas, riesgos y consecuencias.

El responsable del proyecto conserva la autoridad para seleccionar las alternativas y aprobar las decisiones.

Los agentes de inteligencia artificial podrán investigar, comparar, recomendar y documentar, pero no podrán considerar aprobadas sus propias recomendaciones.

No se establecerá un límite artificial de preguntas por módulo.

La profundidad de cada bloque de ingeniería dependerá de su complejidad, riesgos e incertidumbres.

Las decisiones aprobadas deberán registrarse en el repositorio.

La implementación comenzará únicamente cuando el alcance correspondiente disponga de requisitos, interfaces, comportamientos y criterios de aceptación suficientemente definidos.

## 6. Principios de calidad del desarrollo

El proyecto deberá aplicar prácticas profesionales de ingeniería y desarrollo de software.

Entre los principios establecidos se encuentran:

- DRY: evitar duplicación innecesaria.
- SRP: mantener responsabilidades delimitadas.
- KISS: evitar complejidad injustificada.
- YAGNI: no implementar funcionalidades futuras sin necesidad aprobada.
- Reutilización de componentes existentes.
- Separación de responsabilidades.
- Interfaces y contratos explícitos.
- Gestión adecuada de errores.
- Pruebas reproducibles.
- Trazabilidad de cambios.
- Refactorización controlada.

Antes de crear funciones, clases o módulos nuevos deberá evaluarse si existen componentes reutilizables.

La calidad estructural formará parte de los criterios de aceptación.

Una implementación funcional que introduzca duplicación injustificada, responsabilidades superpuestas o complejidad innecesaria no deberá considerarse terminada.

## 7. Seguridad industrial

ControlCore podrá interactuar con sistemas capaces de producir movimiento, energía mecánica y condiciones potencialmente peligrosas.

Por esta razón, la seguridad deberá incorporarse desde el diseño.

Deberán evaluarse los riesgos asociados con:

- Arranque inesperado.
- Movimiento no controlado.
- Sobrevelocidad.
- Pérdida de realimentación.
- Fallas de sensores.
- Pérdida de comunicaciones.
- Fallas de alimentación.
- Reinicios inesperados.
- Órdenes inválidas.
- Fallas de componentes.

Las medidas de protección se definirán mediante análisis de riesgos y requisitos aplicables.

No se asumirá que una función de software constituye por sí sola una protección de seguridad suficiente.

Las pruebas de laboratorio no equivaldrán automáticamente a validación industrial.

## 8. Decisiones confirmadas

Las siguientes reglas de trabajo están confirmadas por la documentación existente y por las instrucciones establecidas durante la sesión.

Las referencias DEC-GOB-001 a DEC-GOB-030 se conservan como reglas y decisiones de gobierno, de gestión de requisitos, de alcance conceptual y de comportamiento conceptual. Fueron incorporadas al registro formal `docs/06-decisiones/registro-decisiones.md` en los bloques B1.1, B1.2, B1.4, B2.1.1, B2.2.2 y B2.3. DEC-GOB-009 registra la aprobación de la línea base de gobierno documental; DEC-GOB-010 a DEC-GOB-015 aprueban la línea base de gestión de requisitos; DEC-GOB-016 aprueba necesidades, actores y escenarios; DEC-GOB-017 a DEC-GOB-021 formalizan las respuestas a PREG-P-01 a PREG-P-15; DEC-GOB-022 a DEC-GOB-030 consolidan las decisiones conceptuales de B2.3.

**DEC-GOB-001 — Naturaleza del producto**

ControlCore se desarrollará como producto industrial comercial de makeAutomatic, no como una demostración tecnológica aislada.

**DEC-GOB-002 — Ingeniería antes de implementación**

La implementación deberá estar precedida por definiciones suficientes de requisitos, arquitectura, interfaces, comportamiento y aceptación.

**DEC-GOB-003 — Autoridad sobre el diseño**

Las decisiones relevantes deberán ser aprobadas por el responsable del proyecto.

Los agentes de IA no podrán aprobar decisiones por iniciativa propia.

**DEC-GOB-004 — Evaluación de alternativas**

Las decisiones técnicas relevantes seguirán la metodología de análisis de alternativas establecida en `docs/00-gobierno/metodologia-diseno.md`.

**DEC-GOB-005 — Calidad obligatoria**

La calidad estructural, la seguridad, la confiabilidad y la verificabilidad serán condiciones fundamentales del desarrollo.

**DEC-GOB-006 — Repositorio como fuente de referencia**

La continuidad del proyecto deberá basarse en la documentación vigente del repositorio y no exclusivamente en el historial de conversaciones.

**DEC-GOB-007 — Bitácora al cierre de sesión**

`docs/00-gobierno/ESTADO-ACTUAL.md` se actualizará al finalizar las sesiones de ingeniería, una vez completadas las actividades correspondientes.

**DEC-GOB-008 — Independencia de proveedores y herramientas de IA**

Las instrucciones, procedimientos y reglas de ingeniería de ControlCore deberán ser independientes de proveedores, modelos y herramientas específicas de inteligencia artificial. Cualquier agente que participe en el proyecto deberá cumplir las mismas obligaciones de consulta del repositorio, respeto por las decisiones aprobadas, trazabilidad, seguridad, calidad y autoridad del responsable del proyecto.

Estado: Aprobada. Origen: aprobación expresa del responsable del proyecto durante B1.1 y autorización de formalización durante B1.2.

**DEC-GOB-009 — Aprobación de la línea base de gobierno documental**

El responsable del proyecto aprobó formalmente los cinco documentos sustantivos de gobierno en versión 0.1 el 2026-10-19, con base en la auditoría B1 versión 0.2, sin hallazgos bloqueantes ni pendientes de H-01 a H-06. Alcance: gobierno documental e inicio de la ingeniería de requisitos.

Estado: Aprobada. Registro: `docs/06-decisiones/registro-decisiones.md`, DEC-GOB-009.

La aprobación no autoriza la implementación de hardware, firmware o software.

**DEC-GOB-010 a DEC-GOB-015 — Línea base de gestión de requisitos**

El responsable del proyecto aprobó en B2.1.1 las seis decisiones de gestión de requisitos:

- DEC-GOB-010 — Esquema de identificación de requisitos.
- DEC-GOB-011 — Versionado de requisitos.
- DEC-GOB-012 — Estados operativos de requisitos.
- DEC-GOB-013 — Escala de prioridad de requisitos.
- DEC-GOB-014 — Trazabilidad de requisitos.
- DEC-GOB-015 — Estructura documental de requisitos.

Estado: Aprobadas. Registro: `docs/06-decisiones/registro-decisiones.md`.

Estas decisiones no aprueban requisitos concretos del producto ni autorizan la implementación.

**DEC-GOB-016 a DEC-GOB-021 — Aprobación de necesidades, actores, escenarios y decisiones conceptuales**

El responsable del proyecto aprobó en B2.2.2:

- DEC-GOB-016 — Aprobación de necesidades, actores y escenarios.
- DEC-GOB-017 — Seguridad industrial, responsabilidades y normativa.
- DEC-GOB-018 — Aplicación objetivo, motores y entorno.
- DEC-GOB-019 — Capacidades y exclusiones de la primera versión.
- DEC-GOB-020 — Integración, perfiles funcionales y registro de información.
- DEC-GOB-021 — Aceptación, validación y documentación.

Estado: Aprobadas. Registro: `docs/06-decisiones/registro-decisiones.md`.

Estas decisiones formalizan aprobaciones conceptuales. No aprueban requisitos concretos, arquitectura, tecnologías, protocolos, prestaciones cuantitativas ni funciones de seguridad certificadas, y no autorizan la implementación.

**DEC-GOB-022 a DEC-GOB-030 — Consolidación de decisiones conceptuales de B2.3**

En B2.3 se consolidaron las 63 decisiones conceptuales adoptadas por el responsable del proyecto:

- DEC-GOB-022 — Alcance, evolución y primer incremento.
- DEC-GOB-023 — Control de movimiento y adquisición.
- DEC-GOB-024 — Supervisión, fallas, alarmas y recuperación.
- DEC-GOB-025 — Operación, mando y estados.
- DEC-GOB-026 — Configuración, persistencia, registros y acceso.
- DEC-GOB-027 — Diagnóstico, mantenimiento y actualización de firmware.
- DEC-GOB-028 — Interfaces, modularidad y simulación.
- DEC-GOB-029 — Verificación, evidencia y cierre de incrementos.
- DEC-GOB-030 — Cierre de las decisiones conceptuales.

Estado: Aprobadas — alcance conceptual. Registro: `docs/06-decisiones/registro-decisiones.md`; matriz completa en `docs/06-decisiones/consolidacion-decisiones-B2.3.md`.

Estas decisiones delimitan el alcance funcional del primer incremento y el comportamiento conceptual del producto. No aprueban requisitos concretos, arquitectura, tecnologías, protocolos, componentes, prestaciones cuantitativas ni funciones de seguridad certificadas, y no autorizan la implementación.

**Decisiones B2.4 — D01 a D60**

Las 60 decisiones de la ronda posterior a B2.3 se consolidan en `docs/06-decisiones/consolidacion-decisiones-B2.4.md` con referencias `B2.4-D01` a `B2.4-D60`. No crean una nueva familia formal de decisiones ni sustituyen `DEC-GOB` o `ADR`.

Estas decisiones orientan el análisis preliminar de riesgos y los requisitos candidatos. No aprueban los documentos, los requisitos candidatos, la arquitectura, las pruebas físicas ni la implementación.

Estas referencias se mantienen en la bitácora como origen y resumen. El registro formal se encuentra en `docs/06-decisiones/registro-decisiones.md`.

## 9. Asuntos pendientes

### 9.1. Línea base de gobierno

La línea base documental fue aprobada el 2026-10-19 mediante DEC-GOB-009. No quedan aprobaciones documentales pendientes para el alcance del gobierno.

### 9.2. Coherencia documental

- Verificar, al iniciar el próximo bloque documental, que las referencias entre documentos y la numeración de secciones sigan siendo válidas.

No quedan hallazgos pendientes de H-01 a H-06. Los hallazgos H-03 a H-06 quedaron resueltos en B1.3 y documentados en el informe de auditoría actualizado. La generalización de `docs/00-gobierno/metodologia-diseno.md`, la referencia a `docs/04-modulos/`, la incorporación de DEC-GOB-001 a DEC-GOB-007 y el registro de DEC-GOB-008 quedaron resueltos en B1.1, B1.2 y B1.3.

### 9.3. Requisitos — B2

B2.1 cerró con la aprobación de la línea base de gestión de requisitos (DEC-GOB-010 a DEC-GOB-015).

B2.2 inició con B2.2.1, que propuso diez necesidades, siete actores, diez escenarios y quince preguntas. B2.2.2 formalizó las aprobaciones:

- Las diez necesidades `NEC-P-01` a `NEC-P-10` están aprobadas (DEC-GOB-016).
- Los siete actores `ACT-P-01` a `ACT-P-07` y sus responsabilidades generales están aprobados (DEC-GOB-016).
- Los diez escenarios `ESC-P-01` a `ESC-P-10` están aprobados como base conceptual (DEC-GOB-016).
- Las quince preguntas `PREG-P-01` a `PREG-P-15` están resueltas conceptualmente (DEC-GOB-017 a DEC-GOB-021).

B2.3 consolidó las 63 decisiones conceptuales en `DEC-GOB-022` a `DEC-GOB-030`. La familia inicial del primer incremento queda definida como motores DC con escobillas y su alcance funcional comprende un motor, arranque/parada, PWM, regulación de velocidad, inversión de giro, medición de velocidad y control en lazo abierto y cerrado, junto con PI con anti-windup, filtrado configurable, rampas configurables, transiciones supervisadas y límites validados, conforme a `DEC-GOB-022`.

B2.4 consolidó las 60 decisiones de la ronda posterior a B2.3, preparó la estructura del análisis preliminar de riesgos y propuso 39 requisitos candidatos:

- 27 requisitos funcionales `RF-001` a `RF-027`.
- 5 requisitos no funcionales `RNF-001` a `RNF-005`.
- 7 restricciones `RES-001` a `RES-007`.

Todos los candidatos están en estado **Propuesto**. Ninguno está aprobado.

Permanecen abiertos los datos técnicos y las decisiones necesarias para completar los criterios: límites eléctricos, térmicos y mecánicos; rangos de velocidad y rampas; umbrales y tiempos de protección; ganancias y límites PI; filtros y tiempos de comunicación; métricas de estabilidad y desempeño; matriz de criticidad de parámetros; escala y criterios de aceptación de riesgos; y autorización de pruebas físicas.

No hay requisitos aprobados ni línea base de requisitos concretos.

El próximo paso recomendado es revisar y completar los criterios pendientes, aprobar o rechazar los candidatos y establecer una línea base. No se inicia automáticamente.

La aprobación de la línea base de gestión, de las necesidades, de los actores, de los escenarios y de las decisiones conceptuales no autoriza la implementación del producto. B2.4 no autoriza pruebas físicas ni implementación.

### 9.4. Arquitectura

Pendiente definir la arquitectura general y las arquitecturas de hardware, firmware, software e interfaces.

### 9.5. Seguridad industrial

La estructura preliminar de análisis de riesgos está preparada en `docs/03-seguridad-industrial/analisis-riesgos.md`, con peligros, FMEA y funciones de protección candidatas. Permanecen pendientes la escala y los criterios de aceptación de riesgos, los estados seguros por escenario, los umbrales de protección, la arquitectura de seguridad, la evaluación de normas aplicables y la autorización de pruebas físicas.

### 9.6. Módulos

Pendiente definir los módulos del producto, sus responsabilidades, interfaces y criterios de aceptación.

### 9.7. Validación

Pendiente establecer la estrategia de pruebas, los criterios específicos de aceptación y los procedimientos de registro de evidencias. B2.4 preparó la compuerta documental de autorización y el registro de pruebas, pero no autoriza ensayos físicos.

### 9.8. Planificación

Pendiente definir las fases de desarrollo y la secuencia de implementación.

## 10. Riesgos e incertidumbres actuales

Los principales riesgos de esta etapa son:

**Definiciones prematuras**

Seleccionar tecnologías o arquitecturas antes de disponer de requisitos suficientes.

**Sobrediseño**

Introducir componentes, abstracciones o funcionalidades que todavía no responden a necesidades aprobadas.

**Inconsistencia documental**

Mantener documentos con reglas contradictorias o estados de aprobación ambiguos.

**Aprobación implícita**

Asumir que un documento incorporado al repositorio, publicado mediante Git o citado en una conversación se encuentra formalmente aprobado.

**Referencias documentales obsoletas**

Mantener referencias a directorios, herramientas o documentos que no reflejan el estado real del repositorio.

**Pérdida de trazabilidad**

Tomar decisiones durante conversaciones sin registrarlas posteriormente en el repositorio.

**Confusión entre pruebas y validación**

Interpretar resultados de laboratorio como evidencia suficiente para operación industrial.

**Confusión entre aprobación de gobierno e implementación**

Interpretar la aprobación de la línea base documental o la autorización de B2 como autorización para implementar hardware, firmware o software.

**Requisitos no verificables**

Aprobar requisitos sin criterio de aceptación objetivo o sin método de verificación.

**Aprobación conceptual tratada como especificación completa**

Interpretar las decisiones DEC-GOB-016 a DEC-GOB-021 como requisitos, interfaces, prestaciones o arquitectura aprobados.

**Necesidades y escenarios aprobados usados como requisitos**

Convertir necesidades o escenarios aprobados conceptualmente en requisitos obligatorios sin derivación, verificación y aprobación específicas.

**Preguntas técnicas derivadas asumidas como resueltas**

Tomar decisiones de implementación a partir de respuestas supuestas a las preguntas técnicas que permanecen abiertas.

**Perfiles funcionales confundidos con actores organizacionales**

Asignar permisos o responsabilidades a los actores `ACT-P-01` a `ACT-P-07` como si fueran equivalentes a los perfiles funcionales de DEC-GOB-020.

**Declaración de seguridad o conformidad sin evidencia**

Presentar las decisiones de seguridad como certificación, o considerar que una función de software sustituye las protecciones de la máquina.

**Implementación anticipada**

Comenzar el desarrollo sin haber definido las condiciones necesarias de seguridad, funcionamiento y aceptación.

**Consolidación conceptual tratada como arquitectura o requisito**

Interpretar las decisiones `DEC-GOB-022` a `DEC-GOB-030` como arquitectura aprobada, requisitos verificables o especificaciones de implementación.

**Alcance del primer incremento tratado como autorización**

Interpretar la delimitación funcional del primer incremento como autorización para implementar hardware, firmware o software.

**Familia de motores tratada como selección de componente**

Interpretar que la familia DC con escobillas define el modelo, las prestaciones o la electrónica de potencia del producto.

**Respuestas ante fallas tratadas como funciones de seguridad aprobadas**

Interpretar que las respuestas condicionadas por riesgos de `DEC-GOB-024` definen estados seguros, niveles de integridad o conformidad.

**Requisitos candidatos tratados como aprobados**

Interpretar los 39 requisitos propuestos de B2.4 como línea base o autorización de implementación.

**Valores de riesgo o protección inventados**

Asignar umbrales, tiempos, tolerancias o niveles de riesgo sin análisis y decisión documentada.

**Pruebas físicas anticipadas**

Interpretar la estructura de análisis de riesgos o la compuerta documental como autorización para energizar el banco.

**Confusión entre D01–D60 de B2.4 y D01–D63 de B2.3**

Citar un identificador de decisión sin indicar el bloque de origen.

Los riesgos de terminología de estados y de hallazgos editoriales pendientes quedaron resueltos en B1.3. El riesgo de convenciones de requisitos no aprobadas quedó resuelto en B2.1.1. El riesgo de necesidades, actores y escenarios no aprobados quedó resuelto en B2.2.2. El riesgo de decisiones conceptuales dispersas quedó atendido por la consolidación de B2.3; la aprobación documental de esa consolidación permanece pendiente. B2.4 añade candidatos y estructura de riesgos, no aprobaciones.

Estos riesgos deberán gestionarse mediante la metodología de ingeniería y los controles documentales establecidos.

## 11. Implementación

**Estado: No autorizada.**

La aprobación del gobierno documental en B1.4, el inicio de B2.1, la aprobación de la línea base de gestión de requisitos en B2.1.1, el inicio de B2.2.1, la formalización de B2.2.2, la consolidación de B2.3 y la preparación de candidatos de B2.4 no modifican este estado. La autorización para iniciar B2 — Ingeniería de requisitos no constituye autorización para implementar el producto.

No existe todavía una arquitectura definitiva aprobada para el producto.

No se ha autorizado iniciar el desarrollo de hardware, firmware o software.

La siguiente etapa no deberá comenzar mediante la selección arbitraria de componentes o tecnologías.

La implementación deberá planificarse a partir de requisitos y decisiones de ingeniería documentadas.

## 12. Registro de sesiones

### 12.1. Sesión 2026-10-12 — Preparación documental

**Objetivo:** Continuar la preparación documental y el establecimiento de criterios de gobierno para ControlCore.

**Actividades realizadas:**

1. Se consultó el repositorio mediante el conector de GitHub.
2. Se revisaron `README.md` y `AGENTS.md`.
3. Se verificó la existencia de los documentos de visión, principios y metodología.
4. Se identificaron documentos pendientes de contenido.
5. Se elaboraron las propuestas de criterios de calidad y definición de terminado.
6. Se preparó el contenido inicial de esta bitácora.

**Resultados:** se avanzó en las condiciones generales de calidad y aceptación del producto. No se aprobaron tecnologías ni arquitecturas. No se realizaron actividades de implementación ni pruebas.

**Estado actual de sus pendientes:** la incorporación al repositorio, el commit y el push se completaron en sesiones posteriores y se verificaron el 2026-10-19. La aprobación formal de los documentos quedó pendiente al cierre de esa sesión y se resolvió en B1.4.

### 12.2. Sesión 2026-10-19 — B1: Consolidación del gobierno documental

**Objetivo:** Revisar, completar y armonizar la documentación de gobierno existente, sin introducir decisiones técnicas ni transformar propuestas en decisiones aprobadas.

**Actividades realizadas:**

1. Se verificó la rama `main` y el estado limpio del repositorio antes de comenzar.
2. Se leyeron `README.md`, `AGENTS.md` y todos los documentos de `docs/00-gobierno/`.
3. Se examinó la estructura documental y se identificaron vacíos, duplicaciones y estados de aprobación ambiguos.
4. Se armonizaron los encabezados y estados de los documentos de gobierno.
5. Se definió el régimen de control documental y aprobación en `docs/00-gobierno/metodologia-diseno.md`.
6. Se añadieron criterios de gestión de requisitos y de resolución de contradicciones documentales.
7. Se actualizó esta bitácora con el estado real del repositorio y los asuntos pendientes.
8. Se revisó el diff, se verificó el alcance y se ejecutaron las comprobaciones disponibles.

**Resultados:**

- Documentación de gobierno consolidada en los aspectos de autoridad, aprobación, requisitos, trazabilidad, calidad, seguridad, verificación, control de cambios, incertidumbres y cierre.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se modificaron `README.md` ni `AGENTS.md`.
- No se realizó implementación, prueba de hardware ni validación industrial.
- La aprobación formal de los documentos de gobierno permanecía pendiente al cierre de B1 y se resolvió en B1.4.

**Verificaciones ejecutadas:** revisión del diff, comprobación de referencias internas y archivos citados, búsqueda de estados de aprobación inconsistentes, verificación de que los archivos modificados pertenecen al alcance autorizado y comprobación del estado del árbol de trabajo.

**Limitaciones:** no se ejecutaron pruebas de software porque el repositorio no contiene código ni pruebas en esta fase. La revisión documental no sustituye la aprobación del responsable del proyecto.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.3. Sesión 2026-10-19 — B1.1: Cierre de coherencia documental

**Objetivo:** Resolver los asuntos pendientes de coherencia documental identificados en B1 y preparar el cierre del gobierno documental.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio y la coincidencia de `HEAD` con `origin/main` en el commit B1 `8923b37`.
2. Se leyeron `README.md`, `AGENTS.md`, los documentos de `docs/00-gobierno/` y el registro de decisiones.
3. Se generalizaron las reglas de agentes en `README.md` y `AGENTS.md`, eliminando la dependencia de proveedor, modelo o herramienta.
4. Se creó `docs/04-modulos/README.md` como índice del directorio, sin definir módulos ni especificaciones técnicas.
5. Se incorporaron las reglas DEC-GOB-001 a DEC-GOB-007 en `docs/06-decisiones/registro-decisiones.md`.
6. Se actualizó esta bitácora con los resultados y asuntos pendientes.
7. Se revisó el diff y se ejecutaron las comprobaciones disponibles.

**Resultados:**

- Decisión aprobada de generalizar las instrucciones de agentes, registrada en esta bitácora.
- Reglas de agentes independientes del proveedor, modelo o herramienta en `README.md` y `AGENTS.md`.
- Referencia a `docs/04-modulos/` resuelta mediante un índice inicial.
- Registro formal de decisiones de gobierno incorporado.
- Los cinco documentos sustantivos de gobierno permanecían en estado **Propuesta para aprobación** al cierre de B1.1.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se realizó implementación ni validación industrial.

**Verificaciones ejecutadas:** revisión del diff, comprobación de referencias internas y rutas, verificación de identificadores únicos, comprobación de ausencia de referencias específicas de proveedor en `README.md` y `AGENTS.md`, verificación del alcance autorizado y comprobación del estado del árbol de trabajo.

**Limitaciones:** no se ejecutaron pruebas de software porque no existe código en esta fase. La generalización de `docs/00-gobierno/metodologia-diseno.md` no formó parte del alcance autorizado de B1.1 y se resolvió en B1.2.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.4. Sesión 2026-10-19 — B1.2: Generalización completa y auditoría de gobierno

**Objetivo:** Completar la generalización de las instrucciones para agentes de IA, registrar formalmente DEC-GOB-008 y realizar una auditoría integral de los cinco documentos sustantivos de gobierno.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B1.1 `3381967`.
2. Se leyeron `README.md`, `AGENTS.md`, los documentos de `docs/00-gobierno/` y el registro de decisiones.
3. Se generalizaron las referencias a proveedores y herramientas en `docs/00-gobierno/metodologia-diseno.md` (secciones 17, 19, 21 y 23).
4. Se registró DEC-GOB-008 en `docs/06-decisiones/registro-decisiones.md`.
5. Se auditaron los cinco documentos sustantivos contra los catorce criterios establecidos en el bloque.
6. Se corrigieron las referencias incompletas a `docs/04-modulos/` en visión, criterios de calidad y definición de terminado.
7. Se creó `docs/00-gobierno/auditoria-gobierno-B1.md` con hallazgos, correcciones, pendientes y recomendación.
8. Se actualizó esta bitácora.
9. Se revisó el diff y se ejecutaron las comprobaciones disponibles.

**Resultados:**

- Metodología independiente de proveedores, modelos y herramientas de IA.
- DEC-GOB-008 aprobada y registrada formalmente.
- Auditoría integral completada sin hallazgos bloqueantes.
- Correcciones editoriales aplicadas sin modificar decisiones, obligaciones ni alcance.
- Hallazgos no bloqueantes H-03 a H-06 documentados; resueltos en B1.3.
- Los cinco documentos sustantivos de gobierno permanecían en estado **Propuesta para aprobación** al cierre de B1.2.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se realizó implementación ni validación industrial.

**Verificaciones ejecutadas:** revisión del diff, comprobación de referencias y rutas, verificación de estados documentales, comprobación de identificadores únicos DEC-GOB-001 a DEC-GOB-008, búsqueda de referencias específicas a proveedores de IA, verificación de conservación de obligaciones, comprobación de trazabilidad de los hallazgos y verificación del alcance autorizado.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. La auditoría es documental y no sustituye las evaluaciones técnicas, eléctricas, mecánicas, ambientales o de seguridad requeridas para una aplicación industrial.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.5. Sesión 2026-10-19 — B1.3: Resolución de hallazgos de auditoría

**Objetivo:** Resolver los hallazgos H-03 a H-06 autorizados por el responsable del proyecto, sin modificar decisiones técnicas, requisitos del producto ni obligaciones sustantivas.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B1.2 `f0d5da6`.
2. Se leyeron `README.md`, `AGENTS.md`, los cinco documentos de gobierno, el informe de auditoría, el registro de decisiones y esta bitácora.
3. Se normalizaron las referencias internas a rutas relativas a la raíz del repositorio (H-03).
4. Se diferenciaron las denominaciones de estado para decisiones, documentos, requisitos y entregables (H-04).
5. Se armonizó la sección 10 de la metodología con el registro de decisiones mediante los formatos DEC-GOB y ADR (H-05).
6. Se unificó el bloque de metadatos de los cinco documentos de gobierno (H-06).
7. Se actualizó el informe de auditoría a la versión 0.2.
8. Se actualizó esta bitácora.
9. Se revisó el diff y se ejecutaron las comprobaciones disponibles.

**Resultados:**

- Hallazgos H-03 a H-06 resueltos.
- Referencias internas normalizadas y verificadas.
- Vocabulario de estados diferenciado sin alterar transiciones, restricciones ni autoridades.
- Esquema DEC-GOB/ADR definido; los ocho registros DEC-GOB permanecen intactos.
- Metadatos uniformes en los cinco documentos.
- Informe de auditoría actualizado; recomienda presentar los cinco documentos para aprobación formal.
- Los cinco documentos permanecían en estado **Propuesta para aprobación** al cierre de B1.3.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se realizó implementación ni validación industrial.

**Verificaciones ejecutadas:** revisión del diff, comprobación de rutas y referencias, consistencia de estados, uniformidad de metadatos, correspondencia metodología-registro, verificación de DEC-GOB-001 a DEC-GOB-008, conservación de obligaciones, ausencia de decisiones técnicas inventadas y verificación del alcance autorizado.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. La auditoría es documental y no sustituye las evaluaciones técnicas, eléctricas, mecánicas, ambientales o de seguridad requeridas para una aplicación industrial.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.6. Sesión 2026-10-19 — B1.4: Aprobación formal del gobierno documental

**Objetivo:** Registrar la aprobación formal de los cinco documentos de gobierno y establecer la línea base documental para iniciar B2 — Ingeniería de requisitos.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B1.3 `19f6098`.
2. Se leyeron `README.md`, `AGENTS.md`, los cinco documentos de gobierno, el informe de auditoría, esta bitácora y el registro de decisiones.
3. Se actualizaron los encabezados de los cinco documentos a estado **Aprobado** y aprobación del 2026-10-19 por el Responsable del proyecto ControlCore, makeAutomatic, conservando la versión 0.1 y el contenido sustantivo.
4. Se registró DEC-GOB-009 en el registro formal de decisiones.
5. Se actualizó el informe de auditoría a la versión 0.3.
6. Se actualizó esta bitácora y se estableció la línea base documental.
7. Se revisó el diff y se ejecutaron las verificaciones.

**Resultados:**

- Cinco documentos de gobierno aprobados formalmente en versión 0.1.
- Línea base documental establecida y registrada en DEC-GOB-009.
- Bloque B1 cerrado.
- Hallazgos H-01 a H-06 resueltos; H-07 brecha de fase; H-08 sin hallazgo.
- B2 — Ingeniería de requisitos autorizado para iniciar; no iniciado en B1.4.
- Implementación de hardware, firmware y software no autorizada.
- No se aprobaron tecnologías, arquitecturas ni requisitos funcionales.

**Verificaciones ejecutadas:** revisión del diff, versiones 0.1 conservadas, estados **Aprobado**, contenido sustantivo sin cambios, registro DEC-GOB-009, decisiones anteriores intactas, referencias documentales, coherencia entre documentos, auditoría y bitácora, ausencia de autorización de implementación y alcance limitado a B1.4.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.7. Sesión 2026-10-19 — B2.1: Estructura, identificación y trazabilidad de requisitos

**Objetivo:** Establecer la estructura documental, el esquema de identificación, los atributos, los estados y los mecanismos de trazabilidad de los requisitos de ControlCore.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B1.4 `1e9fb73`.
2. Se leyeron `README.md`, `AGENTS.md`, los cinco documentos aprobados de gobierno, esta bitácora, el registro de decisiones y los archivos de `docs/01-requisitos/`.
3. Se identificaron las reglas de gestión de requisitos de la metodología aprobada (sección 25).
4. Se creó el índice común de requisitos y se completó la estructura de los tres registros existentes.
5. Se propusieron el esquema de identificación `RF-###`, `RNF-###`, `RES-###`, el esquema de versiones, los atributos, los estados y la trazabilidad.
6. Se registraron las decisiones pendientes en `docs/06-decisiones/pendientes.md`.
7. Se actualizó esta bitácora.
8. Se revisó el diff y se ejecutaron las verificaciones.

**Resultados:**

- Estructura documental de requisitos establecida.
- Esquema de identificación, atributos, estados y trazabilidad propuestos.
- Ningún requisito funcional, no funcional o restricción definido.
- Ningún identificador `RF-###`, `RNF-###` o `RES-###` asignado.
- Ninguna convención aprobada; todas pendientes de decisión.
- Ninguna línea base de requisitos.
- Gobierno documental aprobado sin modificaciones.
- Arquitectura no definida.
- Implementación no autorizada.

**Verificaciones ejecutadas:** revisión del diff, consistencia de identificadores, compatibilidad con la metodología aprobada, atributos y transiciones, estructura de trazabilidad, referencias documentales, ausencia de funcionalidades inventadas, integridad de la línea base de gobierno y alcance limitado a B2.1.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. No se definieron requisitos del producto.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.8. Sesión 2026-10-19 — B2.1.1: Formalización de las convenciones de requisitos

**Objetivo:** Registrar las seis decisiones aprobadas por el responsable del proyecto y establecer la línea base de gestión de requisitos.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B2.1 `5290e4a`.
2. Se leyeron `README.md`, `AGENTS.md`, los cinco documentos aprobados de gobierno, los cuatro documentos de requisitos, el registro de decisiones, el registro de pendientes y esta bitácora.
3. Se registraron las seis decisiones aprobadas como DEC-GOB-010 a DEC-GOB-015.
4. Se actualizaron los cuatro documentos de requisitos a estado **Aprobado** y se incorporaron las decisiones de identificación, versionado, estados, prioridades y trazabilidad.
5. Se marcaron los asuntos de B2.1 como resueltos en `docs/06-decisiones/pendientes.md`, conservando las alternativas.
6. Se actualizó esta bitácora.
7. Se revisó el diff y se ejecutaron las verificaciones.

**Resultados:**

- Seis decisiones aprobadas y registradas formalmente.
- Línea base de gestión de requisitos establecida.
- Cuatro documentos de requisitos aprobados en versión 0.1.
- Convenciones de identificación, versionado, estados, prioridades y trazabilidad aprobadas.
- Requisitos concretos no definidos ni aprobados.
- Arquitectura no definida.
- Implementación no autorizada.
- Gobierno documental aprobado sin modificaciones.

**Verificaciones ejecutadas:** revisión del diff, coherencia entre decisiones y documentos, ausencia de contradicciones con la metodología, identificadores DEC-GOB únicos, versionado coherente, estados y transiciones consistentes, prioridades completas, trazabilidad documentada, conservación de registros anteriores, ausencia de requisitos inventados y alcance limitado a B2.1.1.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. No se definieron requisitos concretos.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.9. Sesión 2026-10-19 — B2.2.1: Identificación de necesidades, actores y escenarios de uso

**Objetivo:** Identificar y documentar necesidades, actores, escenarios y preguntas abiertas antes de establecer requisitos funcionales concretos.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B2.1.1 `a5030a3`.
2. Se leyeron `README.md`, `AGENTS.md`, los cinco documentos aprobados de gobierno, los cuatro documentos aprobados de requisitos, el registro de decisiones, el registro de asuntos pendientes y esta bitácora.
3. Se creó `docs/01-requisitos/necesidades-producto.md` con diez necesidades candidatas y quince preguntas abiertas priorizadas.
4. Se creó `docs/01-requisitos/actores-uso.md` con siete actores y sus responsabilidades potenciales.
5. Se creó `docs/01-requisitos/escenarios-uso.md` con diez escenarios de uso como hipótesis.
6. Se registraron las quince preguntas pendientes en `docs/06-decisiones/pendientes.md`.
7. Se actualizó esta bitácora.
8. Se revisó el diff y se ejecutaron las verificaciones.

**Resultados:**

- Diez necesidades candidatas identificadas.
- Siete actores identificados.
- Diez escenarios de uso propuestos.
- Quince preguntas abiertas priorizadas.
- Ninguna necesidad, actor o escenario aprobado; todos pendientes de validación.
- Ningún requisito concreto definido ni aprobado.
- Ningún identificador `RF-###`, `RNF-###` o `RES-###` asignado.
- Sin selección de tecnologías, interfaces, protocolos, tiempos ni comportamientos de seguridad.
- Línea base de gobierno y de gestión de requisitos sin modificaciones.
- Arquitectura no definida.
- Implementación no autorizada.

**Verificaciones ejecutadas:** revisión del diff, trazabilidad hacia documentos aprobados, distinción entre hechos, necesidades inferidas, hipótesis y preguntas, ausencia de requisitos inventados, ausencia de identificadores `RF-###`, `RNF-###` o `RES-###`, ausencia de selección tecnológica, coherencia entre actores, necesidades y escenarios, preguntas abiertas explícitas, integridad de la línea base aprobada y alcance limitado a B2.2.1.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. No se realizó validación con actores humanos ni se definieron requisitos concretos.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.10. Sesión 2026-10-20 — B2.2.2: Formalización de necesidades, actores, escenarios y decisiones

**Objetivo:** Formalizar las aprobaciones expresas de las diez necesidades, los siete actores, los diez escenarios y las quince decisiones identificadas en B2.2.1.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B2.2.1 `9217ec1`.
2. Se leyeron `README.md`, `AGENTS.md`, los cinco documentos aprobados de gobierno, los cuatro documentos aprobados de requisitos, los tres documentos de B2.2.1, el registro de decisiones, el registro de asuntos pendientes y esta bitácora.
3. Se registraron seis decisiones agrupadas: DEC-GOB-016 para las aprobaciones de necesidades, actores y escenarios, y DEC-GOB-017 a DEC-GOB-021 con trazabilidad individual a `PREG-P-01` a `PREG-P-15`.
4. Se actualizaron los tres documentos de B2.2.1 a versión 0.2 y estado **Aprobado**.
5. Se marcaron las quince preguntas como resueltas conceptualmente en `docs/06-decisiones/pendientes.md` y se incorporaron las preguntas técnicas derivadas que permanecen abiertas.
6. Se actualizó esta bitácora.
7. Se revisó el diff y se ejecutaron las verificaciones.

**Resultados:**

- Diez necesidades aprobadas (DEC-GOB-016).
- Siete actores y sus responsabilidades generales aprobados (DEC-GOB-016).
- Diez escenarios aprobados como base conceptual (DEC-GOB-016).
- Quince preguntas resueltas conceptualmente (DEC-GOB-017 a DEC-GOB-021).
- Ningún requisito concreto definido ni aprobado.
- Ningún identificador `RF-###`, `RNF-###` o `RES-###` asignado.
- Sin selección de arquitectura, tecnologías, protocolos, prestaciones cuantitativas ni funciones de seguridad certificadas.
- Preguntas técnicas derivadas conservadas como pendientes.
- Línea base de gobierno y de gestión de requisitos sin modificaciones.
- Arquitectura no definida.
- Implementación no autorizada.

**Verificaciones ejecutadas:** revisión del diff; fidelidad de las quince respuestas; comprobación de 10 necesidades, 7 actores, 10 escenarios y 15 preguntas; unicidad de DEC-GOB-016 a DEC-GOB-021; trazabilidad entre preguntas, decisiones y documentos; ausencia de requisitos concretos; ausencia de declaraciones prematuras de seguridad o conformidad; integridad de las líneas base aprobadas; alcance limitado a B2.2.2.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. La revisión con actores humanos se limitó a la aprobación del responsable del proyecto. Las decisiones formalizadas son conceptuales y no constituyen especificaciones técnicas completas.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.11. Sesión 2026-10-20 — B2.3: Consolidación de decisiones conceptuales

**Objetivo:** Consolidar y formalizar las 63 decisiones conceptuales adoptadas, delimitar el primer incremento y preparar la documentación para revisión, sin implementar ni seleccionar tecnologías.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y el commit B2.2.2 `7e72b55`.
2. Se leyeron `README.md`, `AGENTS.md`, los documentos de gobierno, los documentos de requisitos, el registro de decisiones, el registro de asuntos pendientes y esta bitácora.
3. Se identificaron las convenciones `DEC-GOB` y `ADR` y se optó por consolidar las decisiones conceptuales en `DEC-GOB-022` a `DEC-GOB-030`, conservando los identificadores `D01` a `D63`.
4. Se creó `docs/06-decisiones/consolidacion-decisiones-B2.3.md` con la matriz de las 63 decisiones, el alcance del primer incremento, las capacidades pendientes, las redundancias y los asuntos abiertos.
5. Se actualizaron `docs/06-decisiones/registro-decisiones.md`, `docs/06-decisiones/pendientes.md`, `docs/01-requisitos/necesidades-producto.md`, `docs/01-requisitos/escenarios-uso.md` y `docs/01-requisitos/README.md`.
6. Se actualizó esta bitácora.
7. Se revisó el diff y se ejecutaron las verificaciones disponibles.

**Resultados:**

- 63 decisiones conceptuales consolidadas y trazadas.
- Nueve registros formales `DEC-GOB-022` a `DEC-GOB-030`.
- Primer incremento delimitado funcionalmente: un motor DC con escobillas, arranque/parada, PWM, regulación de velocidad, inversión de giro, medición de velocidad y control en lazo abierto y cerrado, con PI con anti-windup, filtrado configurable, rampas configurables, transiciones supervisadas y límites validados.
- Familia inicial de motores resuelta conceptualmente; modelo, parámetros y electrónica pendientes.
- Ningún requisito concreto definido ni aprobado.
- Ningún identificador `RF-###`, `RNF-###` o `RES-###` asignado.
- Sin selección de arquitectura, tecnologías, protocolos, componentes ni prestaciones cuantitativas.
- Sin declaración de conformidad o certificación industrial.
- Asuntos técnicos abiertos conservados y actualizados.
- Cambios preparados para revisión; sin commit ni push.

**Verificaciones ejecutadas:** revisión del diff; comprobación de 63 decisiones y de su correspondencia única con `DEC-GOB-022` a `DEC-GOB-030`; unicidad de identificadores; trazabilidad entre `D`, `DEC-GOB`, necesidades y escenarios; coherencia entre documentos; ausencia de requisitos concretos; ausencia de tecnologías o componentes seleccionados; ausencia de declaraciones de conformidad; integridad de las decisiones previamente aprobadas; alcance limitado a B2.3.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. La consolidación es documental y no sustituye el análisis de riesgos, la arquitectura, la verificación ni la validación industrial. La aprobación documental de la consolidación y de las versiones en revisión permanece pendiente.

**Cierre:** los cambios quedan preparados en el árbol de trabajo para revisión del responsable del proyecto. No se realizó commit ni push.

### 12.12. Sesión 2026-10-20 — B2.4: Consolidación y especificación preliminar

**Objetivo:** Consolidar las 60 decisiones de la ronda posterior a B2.3, preparar la estructura del análisis preliminar de riesgos y proponer requisitos candidatos verificables.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio y la sincronización con `origin/main` en el commit B2.3 `9b18a33`.
2. Se leyeron `README.md`, `AGENTS.md`, la bitácora, el registro de decisiones, la consolidación B2.3, las necesidades, actores, escenarios y los registros de requisitos.
3. Se creó `docs/06-decisiones/consolidacion-decisiones-B2.4.md` con la matriz de las 60 decisiones, redundancias, dependencias, compatibilidad con B2.3 y datos pendientes.
4. Se preparó `docs/03-seguridad-industrial/analisis-riesgos.md` con identificación de peligros, FMEA, funciones de protección y compuerta de pruebas.
5. Se incorporaron 27 requisitos funcionales, 5 no funcionales y 7 restricciones candidatas en los registros correspondientes.
6. Se actualizaron el índice de requisitos y el registro de asuntos pendientes.
7. Se actualizó esta bitácora.
8. Se revisó el diff y se ejecutaron las verificaciones documentales.

**Resultados:**

- 60 decisiones consolidadas y trazadas.
- 23 peligros, 12 análisis FMEA y 14 funciones de protección candidatas.
- 39 requisitos candidatos: 27 `RF`, 5 `RNF` y 7 `RES`.
- Ningún requisito aprobado ni línea base de requisitos.
- Sin valores cuantitativos inventados.
- Sin selección de arquitectura, componentes, protocolos o tecnologías.
- Sin declaración de conformidad ni aceptación de riesgos.
- Sin autorización de pruebas físicas ni implementación.

**Verificaciones ejecutadas:** revisión del diff; cobertura D01–D60; unicidad de identificadores `RF`, `RNF`, `RES`, `HZ`, `FMEA` y `PF`; trazabilidad entre decisiones, peligros y requisitos; ausencia de duplicados; compatibilidad con B2.3; integridad de referencias; `git diff --check`; estado del árbol y sincronización con el remoto.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware. El análisis de riesgos es preliminar y no sustituye la evaluación completa, la arquitectura de seguridad ni la validación industrial. Los requisitos candidatos no están aprobados.

**Cierre:** los cambios se prepararon y verificaron; el commit y el push se realizan al final del bloque conforme a la autorización del responsable del proyecto.

## 13. Próximo paso

B2.4 consolidó las 60 decisiones de la ronda posterior a B2.3, preparó la estructura del análisis preliminar de riesgos y propuso 39 requisitos candidatos.

El próximo paso recomendado es **revisar y completar los criterios pendientes, aprobar o rechazar los candidatos y establecer una línea base de requisitos del primer incremento**. No se inicia automáticamente; requiere instrucciones del responsable del proyecto.

Antes de aprobar requisitos deberán resolverse o registrarse los datos de la sección 9.3 y de `docs/06-decisiones/pendientes.md`: límites eléctricos, térmicos y mecánicos; rangos de velocidad y rampas; umbrales y tiempos de protección; ganancias y límites PI; filtros y tiempos de comunicación; métricas de estabilidad y desempeño; matriz de criticidad de parámetros; escala y criterios de aceptación de riesgos; y autorización de pruebas físicas.

La aprobación de necesidades, actores, escenarios y decisiones no autoriza la implementación. La arquitectura continúa no definida y la implementación de hardware, firmware y software continúa no autorizada. B2.4 no autoriza pruebas físicas.

Al iniciar el próximo bloque deberán consultarse `docs/01-requisitos/necesidades-producto.md`, `docs/01-requisitos/actores-uso.md`, `docs/01-requisitos/escenarios-uso.md`, `docs/01-requisitos/requisitos-funcionales.md`, `docs/01-requisitos/requisitos-no-funcionales.md`, `docs/01-requisitos/restricciones-sistema.md`, `docs/03-seguridad-industrial/analisis-riesgos.md`, `docs/06-decisiones/consolidacion-decisiones-B2.4.md`, el registro de decisiones, el registro de asuntos pendientes y esta bitácora.

Las respuestas a los datos pendientes deberán registrarse como decisiones aprobadas; no deberán asumirse.

## 14. Criterio de continuidad

ControlCore deberá avanzar mediante decisiones documentadas y entregables verificables.

Cada sesión deberá partir del estado real del repositorio.

Las propuestas no aprobadas deberán permanecer identificadas como tales.

Los documentos incompletos no deberán considerarse especificaciones definitivas.

La bitácora deberá reflejar el estado real del proyecto y no una estimación optimista de su avance.

El objetivo es preservar la continuidad técnica, la trazabilidad y la calidad del proceso de ingeniería hasta obtener un producto industrial comercial verificable.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
