
# Estado actual del proyecto — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Fecha de actualización:** 2026-10-19  
**Versión del documento:** 0.4  
**Fase actual:** Gobierno documental y preparación de ingeniería  
**Bloque:** B1.2 — Generalización completa y auditoría de gobierno  
**Estado del bloque:** Auditoría completada; correcciones editoriales aplicadas; aprobación formal pendiente  
**Estado del proyecto:** Ingeniería conceptual — implementación no autorizada

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

El proyecto se encuentra en la etapa de preparación documental y establecimiento de las reglas de ingeniería.

El trabajo documental comprende, como propuestas pendientes de aprobación:

1. Gobierno del proyecto.
2. Principios de ingeniería.
3. Metodología de diseño.
4. Criterios de calidad.
5. Definición de terminado.
6. Procedimientos de revisión y aceptación.

Esta etapa busca establecer una base técnica y metodológica sólida antes de comenzar el diseño detallado y la implementación.

Durante la sesión del 19 de octubre de 2026 se consolidó el gobierno documental (bloque B1): se revisaron y armonizaron los documentos de visión, principios, metodología, criterios de calidad y definición de terminado, y se actualizó esta bitácora. La consolidación documental no equivale a aprobación formal.

En la misma fecha se ejecutó el bloque B1.1: se generalizaron las reglas de agentes en `README.md` y `AGENTS.md`, se creó el directorio `docs/04-modulos/` con su índice inicial y se incorporaron las reglas DEC-GOB-001 a DEC-GOB-007 al registro formal de decisiones. Los cinco documentos sustantivos de gobierno permanecen como propuestas.

También en esa fecha se ejecutó el bloque B1.2: se generalizaron las referencias de herramienta de `docs/00-gobierno/metodologia-diseno.md`, se registró DEC-GOB-008 y se realizó la auditoría integral de los cinco documentos sustantivos de gobierno. Las correcciones aplicadas son editoriales y no modifican decisiones, obligaciones ni alcance. Los cinco documentos permanecen en estado **Propuesta para aprobación**.

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

- `docs/00-gobierno/auditoria-gobierno-B1.md` — informe de auditoría integral del gobierno documental.

`README.md` y `AGENTS.md` no fueron modificados durante B1; fueron actualizados en B1.1 para generalizar las reglas de agentes.

Los cinco documentos sustantivos de gobierno se encuentran en estado **Propuesta para aprobación**. Esta bitácora es un registro de continuidad y no un documento de aprobación.

### 4.2. Estado de incorporación, aprobación y registro

Los documentos de gobierno se encuentran incorporados al repositorio y versionados mediante Git. Su incorporación y publicación no constituyen aprobación formal.

La aprobación formal de cada documento deberá ser otorgada de forma expresa por el responsable del proyecto, conforme a `metodologia-diseno.md` (sección 24). Mientras no exista ese registro, los documentos deberán tratarse como propuestas de referencia y no como especificaciones aprobadas.

El registro formal `docs/06-decisiones/registro-decisiones.md` contiene las reglas DEC-GOB-001 a DEC-GOB-007 y la decisión aprobada DEC-GOB-008. Su registro no implica la aprobación de los documentos sustantivos de gobierno.

El directorio `docs/04-modulos/` fue creado con un archivo índice que describe su propósito y su estado pendiente. No contiene especificaciones de módulos.

### 4.3. Documentos pendientes de contenido

Permanecen sin contenido:

- `docs/01-requisitos/` — requisitos funcionales, no funcionales y restricciones.
- `docs/02-arquitectura/` — arquitectura general, hardware, firmware, software e interfaces.
- `docs/03-seguridad-industrial/` — análisis de riesgos, normas y requisitos de seguridad.
- `docs/05-validacion/` — estrategia de pruebas, criterios de aceptación y registro de validaciones.
- `docs/06-decisiones/pendientes.md` — asuntos pendientes; el registro de decisiones ya está incorporado.
- `docs/07-roadmap/` — fases y planificación de implementación.
- `docs/08-prompts/` — contratos e instrucciones de trabajo para agentes.
- `docs/04-modulos/` — solo el índice inicial; no contiene especificaciones de módulos.

Los archivos vacíos no deberán interpretarse como especificaciones ni decisiones aprobadas.

La referencia del `README.md` a `docs/04-modulos/` quedó resuelta con la creación del directorio y su índice.

### 4.4. Función de esta bitácora

`docs/00-gobierno/ESTADO-ACTUAL.md` registra la continuidad del proyecto y facilita el inicio de nuevas sesiones de ingeniería.

Su actualización no sustituye los registros formales de decisiones ni constituye aprobación de documentos, decisiones o entregables.

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

Las referencias DEC-GOB-001 a DEC-GOB-008 se conservan como reglas y decisiones de gobierno. Fueron incorporadas al registro formal `docs/06-decisiones/registro-decisiones.md` en los bloques B1.1 y B1.2. Su registro no aprueba los documentos sustantivos de gobierno, que permanecen como propuestas.

**DEC-GOB-001 — Naturaleza del producto**

ControlCore se desarrollará como producto industrial comercial de makeAutomatic, no como una demostración tecnológica aislada.

**DEC-GOB-002 — Ingeniería antes de implementación**

La implementación deberá estar precedida por definiciones suficientes de requisitos, arquitectura, interfaces, comportamiento y aceptación.

**DEC-GOB-003 — Autoridad sobre el diseño**

Las decisiones relevantes deberán ser aprobadas por el responsable del proyecto.

Los agentes de IA no podrán aprobar decisiones por iniciativa propia.

**DEC-GOB-004 — Evaluación de alternativas**

Las decisiones técnicas relevantes seguirán la metodología de análisis de alternativas establecida en `metodologia-diseno.md`.

**DEC-GOB-005 — Calidad obligatoria**

La calidad estructural, la seguridad, la confiabilidad y la verificabilidad serán condiciones fundamentales del desarrollo.

**DEC-GOB-006 — Repositorio como fuente de referencia**

La continuidad del proyecto deberá basarse en la documentación vigente del repositorio y no exclusivamente en el historial de conversaciones.

**DEC-GOB-007 — Bitácora al cierre de sesión**

`ESTADO-ACTUAL.md` se actualizará al finalizar las sesiones de ingeniería, una vez completadas las actividades correspondientes.

**DEC-GOB-008 — Independencia de proveedores y herramientas de IA**

Las instrucciones, procedimientos y reglas de ingeniería de ControlCore deberán ser independientes de proveedores, modelos y herramientas específicas de inteligencia artificial. Cualquier agente que participe en el proyecto deberá cumplir las mismas obligaciones de consulta del repositorio, respeto por las decisiones aprobadas, trazabilidad, seguridad, calidad y autoridad del responsable del proyecto.

Estado: Aprobada. Origen: aprobación expresa del responsable del proyecto durante B1.1 y autorización de formalización durante B1.2.

Estas referencias se mantienen en la bitácora como origen y resumen. El registro formal se encuentra en `docs/06-decisiones/registro-decisiones.md`.

## 9. Asuntos pendientes

### 9.1. Aprobación formal de documentos

- Aprobar o rechazar formalmente `vision-producto.md`.
- Aprobar o rechazar formalmente `principios-ingenieria.md`.
- Aprobar o rechazar formalmente `metodologia-diseno.md`.
- Aprobar o rechazar formalmente `criterios-calidad.md`.
- Aprobar o rechazar formalmente `definicion-de-terminado.md`.
- Registrar cada decisión con versión, fecha y autoridad, y actualizar el estado en el encabezado del documento correspondiente.

Mientras no se realice esta aprobación, los documentos permanecen como propuestas.

### 9.2. Coherencia documental

- Atender los hallazgos no bloqueantes H-03 a H-06 del informe de auditoría, aceptándolos formalmente o autorizando su corrección.
- Verificar, al iniciar el próximo bloque documental, que las referencias entre documentos y la numeración de secciones sigan siendo válidas.

La generalización de `metodologia-diseno.md`, la referencia a `docs/04-modulos/`, la incorporación de DEC-GOB-001 a DEC-GOB-007 y el registro de DEC-GOB-008 quedaron resueltos en B1.1 y B1.2.

### 9.3. Requisitos

Pendiente desarrollar las especificaciones funcionales, no funcionales y las restricciones del sistema.

Pendiente definir y aprobar el esquema de identificadores de requisitos al iniciar el bloque correspondiente.

### 9.4. Arquitectura

Pendiente definir la arquitectura general y las arquitecturas de hardware, firmware, software e interfaces.

### 9.5. Seguridad industrial

Pendiente desarrollar el análisis de riesgos, los requisitos específicos de seguridad y la evaluación de normas aplicables.

### 9.6. Módulos

Pendiente definir los módulos del producto, sus responsabilidades, interfaces y criterios de aceptación.

### 9.7. Validación

Pendiente establecer la estrategia de pruebas, los criterios específicos de aceptación y los procedimientos de registro de evidencias.

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

**Terminología de estados**

Usar el término «En revisión» con alcances distintos para documentos, trabajos y requisitos, generando confusión en la bitácora o en los registros.

**Hallazgos editoriales pendientes**

Mantener observaciones no bloqueantes de estilo o metadatos sin una decisión expresa sobre su aceptación o corrección.

**Pérdida de trazabilidad**

Tomar decisiones durante conversaciones sin registrarlas posteriormente en el repositorio.

**Confusión entre pruebas y validación**

Interpretar resultados de laboratorio como evidencia suficiente para operación industrial.

**Implementación anticipada**

Comenzar el desarrollo sin haber definido las condiciones necesarias de seguridad, funcionamiento y aceptación.

Estos riesgos deberán gestionarse mediante la metodología de ingeniería y los controles documentales establecidos.

## 11. Implementación

**Estado: No autorizada.**

La consolidación documental de los bloques B1, B1.1 y B1.2 no modifica este estado.

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

**Estado actual de sus pendientes:** la incorporación al repositorio, el commit y el push se completaron en sesiones posteriores y se verificaron el 2026-10-19. La aprobación formal de los documentos continúa pendiente.

### 12.2. Sesión 2026-10-19 — B1: Consolidación del gobierno documental

**Objetivo:** Revisar, completar y armonizar la documentación de gobierno existente, sin introducir decisiones técnicas ni transformar propuestas en decisiones aprobadas.

**Actividades realizadas:**

1. Se verificó la rama `main` y el estado limpio del repositorio antes de comenzar.
2. Se leyeron `README.md`, `AGENTS.md` y todos los documentos de `docs/00-gobierno/`.
3. Se examinó la estructura documental y se identificaron vacíos, duplicaciones y estados de aprobación ambiguos.
4. Se armonizaron los encabezados y estados de los documentos de gobierno.
5. Se definió el régimen de control documental y aprobación en `metodologia-diseno.md`.
6. Se añadieron criterios de gestión de requisitos y de resolución de contradicciones documentales.
7. Se actualizó esta bitácora con el estado real del repositorio y los asuntos pendientes.
8. Se revisó el diff, se verificó el alcance y se ejecutaron las comprobaciones disponibles.

**Resultados:**

- Documentación de gobierno consolidada en los aspectos de autoridad, aprobación, requisitos, trazabilidad, calidad, seguridad, verificación, control de cambios, incertidumbres y cierre.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se modificaron `README.md` ni `AGENTS.md`.
- No se realizó implementación, prueba de hardware ni validación industrial.
- La aprobación formal de los documentos de gobierno permanece pendiente.

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
- Los cinco documentos sustantivos de gobierno permanecen en estado **Propuesta para aprobación**.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se realizó implementación ni validación industrial.

**Verificaciones ejecutadas:** revisión del diff, comprobación de referencias internas y rutas, verificación de identificadores únicos, comprobación de ausencia de referencias específicas de proveedor en `README.md` y `AGENTS.md`, verificación del alcance autorizado y comprobación del estado del árbol de trabajo.

**Limitaciones:** no se ejecutaron pruebas de software porque no existe código en esta fase. La generalización de `metodologia-diseno.md` no formó parte del alcance autorizado y permanece pendiente.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

### 12.4. Sesión 2026-10-19 — B1.2: Generalización completa y auditoría de gobierno

**Objetivo:** Completar la generalización de las instrucciones para agentes de IA, registrar formalmente DEC-GOB-008 y realizar una auditoría integral de los cinco documentos sustantivos de gobierno.

**Actividades realizadas:**

1. Se verificó la rama `main`, el árbol limpio, la coincidencia de `HEAD` con `origin/main` y la existencia del commit B1.1 `3381967`.
2. Se leyeron `README.md`, `AGENTS.md`, los documentos de `docs/00-gobierno/` y el registro de decisiones.
3. Se generalizaron las referencias a proveedores y herramientas en `metodologia-diseno.md` (secciones 17, 19, 21 y 23).
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
- Hallazgos no bloqueantes H-03 a H-06 documentados y pendientes de aceptación o corrección.
- Los cinco documentos sustantivos de gobierno permanecen en estado **Propuesta para aprobación**.
- No se aprobaron documentos, tecnologías, arquitecturas ni requisitos funcionales.
- No se realizó implementación ni validación industrial.

**Verificaciones ejecutadas:** revisión del diff, comprobación de referencias y rutas, verificación de estados documentales, comprobación de identificadores únicos DEC-GOB-001 a DEC-GOB-008, búsqueda de referencias específicas a proveedores de IA, verificación de conservación de obligaciones, comprobación de trazabilidad de los hallazgos y verificación del alcance autorizado.

**Limitaciones:** no se ejecutaron pruebas de software ni ensayos de hardware porque no existe código ni prototipo en esta fase. La auditoría es documental y no sustituye las evaluaciones técnicas, eléctricas, mecánicas, ambientales o de seguridad requeridas para una aplicación industrial.

**Cierre y publicación:** el bloque se cierra con un commit único y su publicación en la rama activa, conforme al procedimiento autorizado. La confirmación operativa del push se reporta al responsable del proyecto.

## 13. Próximo paso

Los bloques B1, B1.1 y B1.2 quedaron consolidados documentalmente. No se inicia B2 sin autorización expresa.

La siguiente actividad recomendada es:

1. Revisar el informe `docs/00-gobierno/auditoria-gobierno-B1.md` y decidir la aprobación formal de los cinco documentos, aceptando o corrigiendo los hallazgos H-03 a H-06.
2. Registrar cada aprobación con versión, fecha y autoridad, conforme a `metodologia-diseno.md` (sección 24).
3. Una vez aprobado el gobierno, autorizar el bloque de requisitos y definir el esquema de identificadores.

Al iniciar una nueva sesión deberán consultarse `README.md`, `AGENTS.md`, este archivo, el registro de decisiones y el informe de auditoría.

No deberán modificarse decisiones aprobadas sin autorización.

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
