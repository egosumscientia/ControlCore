# ControlCore — Metodología de diseño e ingeniería

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Metodología de diseño e ingeniería  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería conceptual  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto

---

## 1. Propósito

Este documento establece la metodología de trabajo para el diseño, desarrollo y evolución de ControlCore.

Su objetivo es garantizar que el proyecto avance mediante decisiones técnicas fundamentadas, documentadas y verificables, evitando tanto la improvisación como la prolongación indefinida de las discusiones de arquitectura.

La metodología deberá permitir:

- Analizar alternativas técnicas con suficiente profundidad.
- Mantener la autoridad del responsable del proyecto sobre las decisiones.
- Aprender durante el proceso de evaluación.
- Identificar riesgos e incertidumbres.
- Estimar y controlar el avance del diseño.
- Determinar cuándo un bloque está suficientemente maduro.
- Transformar las especificaciones aprobadas en tareas de implementación.
- Mantener continuidad entre conversaciones y sesiones.
- Conservar trazabilidad de las decisiones y sus consecuencias.

## 2. Principio fundamental

**ControlCore se diseñará mediante ingeniería estructurada antes de proceder a su implementación, y se construirá posteriormente de manera incremental.**

El objetivo no es responder el mayor número posible de preguntas ni producir documentación por sí misma.

El objetivo es alcanzar un nivel de definición suficiente para implementar, verificar, validar y mantener un producto industrial profesional.

No se comenzará la implementación de un componente mientras existan decisiones fundamentales pendientes que afecten directamente su diseño.

Esto no impide desarrollar experimentos técnicos autorizados para resolver incertidumbres específicas.

## 3. Autoridad y responsabilidades

### 3.1. Responsable del proyecto

El responsable del proyecto de makeAutomatic conserva la autoridad sobre:

- Alcance del producto.
- Selección de alternativas arquitectónicas.
- Priorización de funcionalidades.
- Aprobación de requisitos.
- Aprobación de decisiones técnicas.
- Autorización de implementación.
- Aprobación de cambios de alcance.
- Aceptación de entregables.

La aceptación de una propuesta técnica no sustituye las verificaciones especializadas o evaluaciones de conformidad que correspondan.

### 3.2. Asistente de ingeniería

El asistente de IA actuará como colaborador técnico.

Sus responsabilidades incluyen:

- Identificar las decisiones necesarias.
- Formular preguntas relevantes.
- Investigar alternativas cuando corresponda.
- Presentar ventajas, desventajas y riesgos.
- Recomendar soluciones fundamentadas.
- Detectar contradicciones.
- Identificar dependencias.
- Evaluar la madurez de los bloques.
- Recomendar cuándo cerrar una etapa.
- Preparar documentación técnica.
- Convertir diseños aprobados en tareas verificables.
- Mantener la continuidad documental.

El asistente no deberá imponer sus recomendaciones ni considerar aprobadas decisiones que el responsable no haya seleccionado.

## 4. Diseño mediante decisiones A/B/C

El método preferente de análisis será presentar una decisión de ingeniería por vez.

Cada decisión deberá incluir:

1. Identificación de la cuestión técnica.
2. Contexto necesario para comprenderla.
3. Alternativa A.
4. Alternativa B.
5. Alternativa C.
6. Ventajas y desventajas relevantes.
7. Riesgos y consecuencias técnicas.
8. Recomendación fundamentada del asistente.
9. Solicitud de selección al responsable del proyecto.

Las alternativas deberán ser técnicamente diferenciables y razonables para el problema analizado.

No se inventarán tres alternativas artificiales cuando solo existan una o dos opciones viables.

El responsable podrá seleccionar una alternativa, combinar elementos compatibles, proponer una opción distinta o solicitar investigación adicional.

La recomendación del asistente no tendrá carácter vinculante.

## 5. Una decisión por interacción

Como regla general, se abordará una decisión técnica por interacción.

Esto permitirá:

- Examinar las consecuencias de cada elección.
- Evitar respuestas excesivamente extensas.
- Mantener claridad sobre lo aprobado.
- Facilitar el aprendizaje técnico.
- Registrar las decisiones con precisión.

Podrán agruparse decisiones estrechamente relacionadas cuando el responsable lo autorice.

No deberán repetirse preguntas ya resueltas salvo que exista una contradicción, un cambio de requisitos o nueva evidencia que justifique su revisión.

## 6. Profundidad del análisis

No existirá un límite artificial de preguntas por módulo.

Un bloque podrá requerir diez, treinta, sesenta o más decisiones, dependiendo de:

- Complejidad técnica.
- Riesgos de seguridad.
- Dependencias.
- Incertidumbres.
- Requisitos de integración.
- Prestaciones exigidas.
- Necesidades de mantenimiento.
- Exigencias de validación.

El asistente deberá evitar preguntas redundantes, triviales o que no produzcan decisiones útiles.

La profundidad deberá ser proporcional a la importancia de cada asunto.

## 7. Estimaciones iniciales

Antes de comenzar un bloque de ingeniería, el asistente deberá presentar una estimación de trabajo.

La estimación incluirá, cuando sea posible:

- Objetivo del bloque.
- Principales temas que deberán resolverse.
- Intervalo estimado de decisiones o preguntas.
- Dependencias conocidas.
- Riesgos que podrían ampliar el análisis.
- Entregables documentales esperados.

Las estimaciones serán orientativas, no cuotas obligatorias.

Si se necesita ampliar el número previsto de preguntas, el asistente deberá explicar qué incertidumbres justifican esa ampliación.

Las estimaciones podrán actualizarse a medida que avance el diseño.

## 8. Seguimiento del avance

Durante cada bloque se mantendrá un registro de progreso.

El seguimiento deberá identificar:

- Decisiones aprobadas.
- Decisiones pendientes.
- Decisiones condicionadas.
- Hipótesis pendientes de validación.
- Riesgos abiertos.
- Documentos afectados.
- Dependencias con otros bloques.

El asistente presentará evaluaciones periódicas de avance, especialmente al completar conjuntos significativos de decisiones.

No se utilizará exclusivamente el porcentaje de preguntas respondidas como indicador de madurez.

La madurez deberá evaluarse según la cobertura y calidad de las definiciones alcanzadas.

## 9. Estados de las decisiones

Cada decisión relevante deberá tener uno de los siguientes estados:

**Pendiente:** todavía no ha sido seleccionada una alternativa.

**Propuesta:** existe una recomendación, pero no ha sido aprobada.

**Aprobada:** el responsable ha seleccionado expresamente una alternativa.

**Condicionada:** la decisión ha sido seleccionada, pero depende de una comprobación o restricción pendiente.

**Revisión de decisión:** nueva evidencia exige reconsiderar una decisión anterior.

**Sustituida:** otra decisión aprobada reemplaza formalmente la anterior.

Las decisiones condicionadas deberán identificar claramente sus condiciones de validez.

Una decisión aprobada no deberá modificarse silenciosamente.

## 10. Registro de decisiones

Las decisiones de gobierno, arquitectónicas y técnicas se documentarán en:

`docs/06-decisiones/`

Se distinguen dos familias de identificadores y formatos.

### 10.1. Decisiones de gobierno — DEC-GOB

Las decisiones de gobierno se identifican como `DEC-GOB-###` y se registran en `docs/06-decisiones/registro-decisiones.md`.

Cada registro deberá incluir:

- Identificador.
- Título.
- Contenido de la regla o decisión.
- Justificación documentada.
- Estado.
- Referencia de origen.

Este formato se aplica a reglas de gobierno ya confirmadas y a decisiones de gobierno aprobadas expresamente. No requiere evaluación de alternativas técnicas cuando la decisión no selecciona una arquitectura, una tecnología o un componente.

### 10.2. Decisiones arquitectónicas y técnicas — ADR

Las decisiones arquitectónicas y técnicas se identifican como `ADR-###`.

Cada registro deberá incluir, cuando corresponda:

- Identificador.
- Fecha.
- Bloque de ingeniería.
- Problema.
- Contexto.
- Alternativas evaluadas.
- Recomendación técnica.
- Alternativa seleccionada.
- Justificación.
- Consecuencias.
- Riesgos.
- Dependencias.
- Estado.
- Referencias a requisitos, documentos y evidencias.

El formato ADR deberá permitir documentar la evaluación estructurada de alternativas, la justificación, las consecuencias, los riesgos, las dependencias y la trazabilidad exigidas por esta metodología.

### 10.3. Reglas comunes

Los identificadores deberán ser estables y únicos dentro de su familia.

Los cambios posteriores deberán preservar el historial de las decisiones y su trazabilidad.

La existencia de un registro no constituye aprobación. El estado de aprobación se rige por la sección 9 y por la sección 24.

## 11. Criterios de madurez del diseño

El asistente deberá evaluar periódicamente si un bloque está suficientemente definido.

La evaluación considerará cinco dimensiones.

### 11.1. Cobertura

Los requisitos, comportamientos y restricciones relevantes están identificados.

### 11.2. Coherencia

Las decisiones son compatibles entre sí y con la arquitectura general.

### 11.3. Implementabilidad

Existe información suficiente para desarrollar el componente sin inventar decisiones fundamentales.

### 11.4. Verificabilidad

Los requisitos y comportamientos pueden comprobarse mediante criterios de aceptación y pruebas.

### 11.5. Riesgo

Los riesgos relevantes están identificados y tratados, o cuentan con acciones y responsables definidos para su resolución antes de la etapa que corresponda.

Un bloque no deberá declararse maduro únicamente porque se haya agotado el número estimado de preguntas.

## 12. Evaluaciones periódicas

El asistente deberá emitir evaluaciones de madurez durante el desarrollo de cada bloque.

Estas evaluaciones podrán utilizar las siguientes categorías:

**Insuficiente:** faltan definiciones fundamentales.

**En desarrollo:** existe una base técnica, pero permanecen decisiones importantes.

**Maduro para documentación:** las decisiones permiten consolidar una especificación coherente.

**Maduro para implementación:** las especificaciones y los criterios de aceptación permiten comenzar tareas de desarrollo delimitadas.

**Maduro para validación:** la implementación dispone de condiciones y procedimientos para realizar las pruebas correspondientes.

Estas categorías no representan certificaciones ni declaraciones de aptitud industrial.

## 13. Cierre de bloques

El asistente será responsable de recomendar expresamente el cierre de un bloque cuando considere que se han alcanzado sus objetivos.

La recomendación deberá incluir:

1. Decisiones principales aprobadas.
2. Requisitos cubiertos.
3. Riesgos pendientes.
4. Cuestiones que requieren experimentación.
5. Documentación generada.
6. Dependencias con otros bloques.
7. Evaluación de madurez.
8. Próxima actividad recomendada.

El responsable del proyecto decidirá si aprueba el cierre o solicita profundizar.

El cierre de un bloque no significa que todas las incertidumbres del producto hayan desaparecido.

Significa que el bloque ha alcanzado la madurez necesaria para su siguiente etapa autorizada.

## 14. Gestión de incertidumbres

Las cuestiones no resueltas deberán registrarse explícitamente.

Se distinguirán:

- Decisiones pendientes.
- Hipótesis técnicas.
- Restricciones por confirmar.
- Riesgos.
- Experimentos necesarios.
- Validaciones pendientes.

Cuando una decisión dependa de una prueba física, se documentará:

- Qué debe comprobarse.
- Por qué es necesario.
- Cómo se realizará la prueba.
- Qué resultados permitirán tomar la decisión.

No se reemplazarán datos experimentales desconocidos por suposiciones presentadas como hechos.

## 15. Consolidación documental

Las conversaciones de diseño no constituirán por sí mismas la documentación oficial del proyecto.

Las decisiones aprobadas deberán trasladarse a los archivos Markdown correspondientes.

La documentación deberá reflejar:

- Lo aprobado.
- Lo pendiente.
- Lo descartado.
- Las condiciones de validez.
- Las dependencias.
- Las pruebas necesarias.

Los documentos deberán mantenerse consistentes entre sí.

Cuando una decisión afecte varios documentos, se identificarán las actualizaciones necesarias.

## 16. Separación entre diseño e implementación

ControlCore tendrá dos actividades claramente diferenciadas.

### 16.1. Ingeniería de diseño

Incluye investigación, análisis, comparación de alternativas, selección de arquitectura, definición de requisitos, evaluación de riesgos y especificación de pruebas.

### 16.2. Ingeniería de implementación

Incluye programación, integración, construcción de hardware, pruebas y corrección de defectos.

La implementación comenzará únicamente cuando el responsable del proyecto la autorice.

Los agentes de programación deberán trabajar sobre especificaciones aprobadas y tareas delimitadas.

## 17. Preparación de tareas de implementación

Una vez que un bloque alcance suficiente madurez, podrá transformarse en tareas de implementación.

Cada tarea deberá definir:

- Objetivo.
- Contexto documental.
- Alcance permitido.
- Archivos o componentes afectados, cuando sean conocidos.
- Requisitos aplicables.
- Interfaces relevantes.
- Restricciones.
- Cambios prohibidos.
- Pruebas esperadas.
- Criterios de aceptación.
- Entregables.

Las tareas deberán ser suficientemente pequeñas para facilitar revisión, validación y control de cambios.

No se utilizarán instrucciones genéricas que deleguen decisiones arquitectónicas fundamentales al agente de programación.

## 18. Calidad de implementación

Las tareas deberán cumplir los principios establecidos en `AGENTS.md` y `docs/00-gobierno/principios-ingenieria.md`.

Se verificará especialmente:

- Ausencia de duplicación injustificada.
- Reutilización de componentes existentes.
- Responsabilidades claramente separadas.
- Interfaces consistentes.
- Complejidad proporcional a los requisitos.
- Gestión adecuada de errores.
- Pruebas reproducibles.
- Respeto del alcance autorizado.

Una implementación funcional que incumpla requisitos estructurales relevantes no deberá considerarse terminada.

## 19. GitHub como memoria técnica

El repositorio GitHub será la referencia persistente del estado del proyecto.

Las conversaciones con asistentes de IA podrán utilizarse para realizar análisis y tomar decisiones, pero la continuidad no dependerá exclusivamente del historial de esas conversaciones.

El repositorio deberá conservar:

- Documentos de gobierno.
- Requisitos.
- Arquitectura.
- Decisiones aprobadas.
- Asuntos pendientes.
- Planes de validación.
- Roadmap.
- Instrucciones para agentes.
- Estado actual.

Los cambios deberán versionarse mediante Git.

## 20. Continuidad entre conversaciones

El archivo:

`docs/00-gobierno/ESTADO-ACTUAL.md`

será el punto principal de recuperación del trabajo.

Deberá contener:

1. Fase actual.
2. Bloque activo.
3. Estado de madurez.
4. Decisiones aprobadas recientemente.
5. Decisiones pendientes.
6. Riesgos e incertidumbres abiertos.
7. Documentos relevantes.
8. Última actividad completada.
9. Próxima decisión o tarea concreta.
10. Fecha de actualización.

Al iniciar una nueva conversación, el asistente deberá consultar este archivo y los documentos relacionados antes de continuar.

## 21. Consulta de repositorios por agentes de IA

Cuando el responsable proporcione la URL de un repositorio, el agente deberá utilizar primero el mecanismo de acceso disponible en su entorno para consultar el repositorio real.

Deberá:

- Identificar el repositorio y la rama relevante.
- Consultar el estado actual.
- Leer los documentos necesarios.
- Verificar las implementaciones existentes antes de proponer cambios.
- Evitar inventar archivos, métodos o funcionalidades.
- Recuperar decisiones documentadas antes de formular nuevas preguntas.

No deberá redirigir automáticamente al usuario a otra herramienta o entorno para una consulta que pueda realizarse mediante el mecanismo de acceso disponible.

Si existe una limitación de acceso, deberá explicarla con precisión.

## 22. Procedimiento de cierre de sesión

Cuando el responsable solicite **«Cierre de sesión»**, el asistente deberá preparar la actualización documental correspondiente.

El cierre incluirá:

- Resumen de actividades.
- Decisiones aprobadas.
- Documentos creados o modificados.
- Estado del bloque.
- Pendientes.
- Riesgos.
- Próximo paso.

Se actualizará el contenido de `docs/00-gobierno/ESTADO-ACTUAL.md` y, cuando corresponda, el registro de decisiones.

Si el asistente no dispone de autorización o capacidad para modificar directamente el repositorio, entregará el contenido listo para incorporarlo mediante el procedimiento elegido por el responsable.

No afirmará que GitHub está actualizado hasta que se haya confirmado la publicación de los cambios.

La actualización de `docs/00-gobierno/ESTADO-ACTUAL.md` no constituye aprobación de documentos, decisiones ni entregables.

## 23. Inicio de una nueva conversación

Para retomar el proyecto, el responsable podrá utilizar el siguiente mensaje:

> Continúa como mi colaborador de ingeniería del proyecto ControlCore de makeAutomatic.
>
> Repositorio GitHub: [URL].
>
> Consulta primero el repositorio mediante el mecanismo de acceso disponible en tu entorno. Lee `AGENTS.md`, `docs/00-gobierno/metodologia-diseno.md` y `docs/00-gobierno/ESTADO-ACTUAL.md`, además de los documentos relevantes para el bloque activo.
>
> Recupera las decisiones aprobadas, los asuntos pendientes y el próximo paso. No me pidas repetir decisiones documentadas ni me redirijas a otra herramienta o entorno.
>
> Trabajaremos una decisión de ingeniería por vez, preferiblemente con alternativas A/B/C, ventajas, desventajas y recomendación técnica. Yo apruebo las decisiones arquitectónicas.
>
> Antes de continuar, indícame brevemente dónde quedamos.

Este mensaje podrá reutilizarse en cualquier conversación nueva.

## 24. Control documental y aprobación

### 24.1. Estados de los documentos

Todo documento de gobierno, requisitos, arquitectura, decisiones o validación deberá disponer de un estado identificable.

Se utilizarán, según corresponda:

- **Borrador:** contenido en elaboración; no apto para uso como referencia.
- **Propuesta para aprobación:** contenido completo para revisión, pero no aprobado.
- **Aprobado:** el responsable del proyecto ha aceptado expresamente la versión indicada.
- **Revisión de documento aprobado:** una versión aprobada se encuentra sujeta a revisión por nueva evidencia o cambio de alcance.
- **Sustituido:** existe una versión posterior aprobada que reemplaza formalmente la anterior.

Estos estados se aplican a documentos. Los estados de las decisiones se rigen por la sección 9 y no deberán confundirse con los estados documentales.

### 24.2. Autoridad y evidencia de aprobación

La aprobación de documentos y decisiones corresponde al responsable del proyecto.

La aprobación deberá ser expresa y registrar, como mínimo:

- Documento o decisión aprobada.
- Versión o alcance aprobado.
- Fecha.
- Autoridad que aprueba.
- Condiciones o limitaciones, cuando existan.

La incorporación de un documento al repositorio, la realización de un commit o push, la recomendación de un agente de IA, la ausencia de objeciones o el transcurso del tiempo no constituirán aprobación.

Mientras un documento permanezca en estado **Propuesta para aprobación**, su contenido podrá utilizarse como referencia de trabajo, pero no como especificación aprobada para implementación.

### 24.3. Registro y trazabilidad

El estado de aprobación deberá reflejarse en el encabezado del documento y en `docs/00-gobierno/ESTADO-ACTUAL.md`.

Las decisiones formales se registrarán en `docs/06-decisiones/`. La bitácora de continuidad no sustituye ese registro.

Los cambios sobre documentos aprobados deberán:

1. Identificar el motivo y el alcance.
2. Pasar el documento al estado **Revisión de documento aprobado** o generar una nueva versión.
3. Evaluar el impacto sobre requisitos, arquitectura, implementación, pruebas y validación.
4. Obtener una nueva aprobación antes de utilizar la versión modificada como base de implementación.

Los cambios relevantes deberán conservar trazabilidad mediante Git.

La numeración de versiones documentales no deberá confundirse con la versión comercial del producto.

## 25. Gestión de requisitos

Los requisitos deberán gestionarse como elementos identificables y controlados, no como texto disperso en documentos.

### 25.1. Registro

Los requisitos funcionales, no funcionales y las restricciones se mantendrán en `docs/01-requisitos/`, según su naturaleza.

Cada requisito deberá disponer, cuando corresponda, de:

- Identificador único y estable.
- Enunciado verificable.
- Justificación o necesidad de origen.
- Fuente o autoridad que lo solicita.
- Prioridad.
- Condiciones y límites aplicables.
- Método de verificación.
- Criterio de aceptación.
- Estado.
- Relaciones de trazabilidad.

El esquema definitivo de identificación se aprobará al iniciar el bloque de requisitos y se mantendrá estable durante el proyecto.

Los criterios de calidad aplicables a los requisitos y la cadena de trazabilidad se establecen en `docs/00-gobierno/criterios-calidad.md` (secciones 3 y 13).

### 25.2. Estados y línea base

Los requisitos utilizarán los siguientes estados:

- **Propuesto:** identificado, pero no aprobado.
- **Aprobado:** aceptado como base de diseño, implementación o verificación.
- **Revisión de requisito aprobado:** aprobado previamente y sujeto a modificación.
- **Sustituido:** reemplazado formalmente por otro requisito aprobado.
- **Rechazado:** evaluado y descartado, conservando el registro de la decisión.

Un conjunto de requisitos aprobados para un alcance constituye una línea base. Las modificaciones posteriores a la línea base deberán someterse a control de cambios y conservar trazabilidad.

### 25.3. Requisitos pendientes

Los requisitos no definidos, no aprobados o que se encuentren en estado **Revisión de requisito aprobado** deberán permanecer identificados como tales.

No deberá implementarse una funcionalidad cuyo requisito esencial permanezca pendiente, salvo que exista una autorización expresa para realizar un experimento delimitado y se registre su carácter exploratorio.

## 26. Resolución de contradicciones documentales

Cuando se detecte una contradicción entre requisitos, decisiones, arquitectura, criterios de calidad, documentos de seguridad o instrucciones de trabajo, el agente deberá:

1. Identificarla de forma explícita, citando los documentos y secciones afectados.
2. Determinar su alcance e impacto potencial.
3. Abstenerse de aplicar una interpretación silenciosa.
4. Registrarla como asunto pendiente en `docs/00-gobierno/ESTADO-ACTUAL.md` y, cuando corresponda, en `docs/06-decisiones/pendientes.md`.
5. Suspender la implementación afectada hasta que exista una resolución aprobada, cuando la contradicción comprometa requisitos, seguridad o contratos.

La resolución deberá ser adoptada por el responsable del proyecto y registrada con su justificación.

Una contradicción que afecte condiciones de seguridad se tratará como bloqueante hasta su resolución.

La resolución deberá actualizar de forma coherente todos los documentos afectados y conservar trazabilidad del cambio.

La antigüedad, el consenso aparente o la práctica previa no prevalecerán sobre una decisión aprobada vigente.

## 27. Mejora de la metodología

La metodología podrá revisarse cuando la experiencia del proyecto demuestre que existen procedimientos más eficientes o rigurosos.

Los cambios deberán preservar los principios fundamentales:

- Autoridad del responsable sobre las decisiones.
- Rigor técnico.
- Trazabilidad.
- Seguridad.
- Calidad industrial.
- Implementación controlada.
- Verificación objetiva.
- Continuidad documental.

Las modificaciones importantes deberán registrarse y aprobarse.

## 28. Criterio rector

**El diseño estará suficientemente maduro cuando las decisiones aprobadas permitan avanzar con claridad, sin trasladar incertidumbres fundamentales a la implementación y sin dejar riesgos relevantes sin tratamiento.**

No se buscará responder todas las preguntas imaginables.

Tampoco se cerrará prematuramente un bloque por alcanzar una cantidad determinada de preguntas.

La responsabilidad del asistente será recomendar cuándo continuar investigando y cuándo consolidar lo diseñado.

La decisión final corresponderá al responsable del proyecto.

---

**ControlCore — makeAutomatic**  
*Metodología de diseño e ingeniería — v0.1*