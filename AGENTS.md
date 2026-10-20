# AGENTS.md — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Versión del documento:** 0.1  
**Estado:** Contrato operativo inicial para agentes de IA

---

## 1. Propósito

Este documento establece las reglas obligatorias para cualquier agente de inteligencia artificial que participe en actividades de análisis, diseño, documentación, programación, pruebas o mantenimiento del proyecto ControlCore.

Las instrucciones se aplican a cualquier agente de inteligencia artificial que trabaje sobre el repositorio, independientemente de su proveedor, modelo o herramienta.

ControlCore es un producto de automatización industrial destinado a evolucionar hacia aplicaciones comerciales reales. No debe tratarse como un ejercicio académico ni como una demostración de software sin exigencias industriales.

El agente debe priorizar la corrección técnica, la seguridad, la confiabilidad, la trazabilidad y el cumplimiento del diseño aprobado.

## 2. Autoridad sobre el diseño

El responsable del proyecto conserva la autoridad sobre:

- El alcance funcional del producto.
- Las decisiones de arquitectura.
- La selección de tecnologías y componentes.
- Las prioridades de desarrollo.
- La aceptación de riesgos y restricciones dentro de las responsabilidades que legal y técnicamente le correspondan.
- La aprobación de implementaciones y cambios.

El agente puede investigar, proponer, comparar alternativas y recomendar soluciones.

**El agente no puede considerar aprobada una decisión simplemente porque la haya recomendado.**

Cuando una decisión no esté documentada o resulte ambigua, deberá identificarla y solicitar autorización antes de introducir cambios que dependan de ella.

La aprobación del responsable del proyecto no sustituye las evaluaciones, verificaciones o certificaciones exigibles para una aplicación industrial.

## 3. Fuente de verdad

El repositorio y sus documentos aprobados constituyen la referencia técnica del proyecto.

Antes de comenzar cualquier trabajo, el agente debe consultar, según corresponda:

1. `README.md`
2. `AGENTS.md`
3. `docs/00-gobierno/ESTADO-ACTUAL.md`
4. `docs/00-gobierno/principios-ingenieria.md`
5. `docs/00-gobierno/metodologia-diseno.md`
6. Los requisitos, decisiones arquitectónicas y especificaciones del módulo involucrado.
7. Las pruebas y los criterios de aceptación aplicables.

Los archivos vacíos, incompletos o pendientes de aprobación no deben interpretarse como especificaciones definitivas.

Cuando existan contradicciones entre documentos, el agente deberá señalarlas y solicitar resolución. No deberá escoger silenciosamente una interpretación.

## 4. Inspección obligatoria del repositorio

La URL oficial del repositorio ControlCore es:

https://github.com/egosumscientia/ControlCore.git

**Consulta obligatoriamente el repositorio actualizado mediante el mecanismo de acceso disponible en el entorno del agente antes de comenzar cualquier trabajo sobre el proyecto.** El mecanismo podrá ser un conector de repositorio, una copia local bajo control de versiones u otro medio autorizado.

La consulta deberá incluir, según corresponda:

1. `README.md` y `AGENTS.md`.
2. `docs/00-gobierno/ESTADO-ACTUAL.md`.
3. Los documentos de diseño, requisitos y decisiones relacionados con la tarea.
4. Los archivos de código y pruebas afectados, cuando corresponda.

Recupera las decisiones aprobadas, los asuntos pendientes y el siguiente paso autorizado. No dependas exclusivamente de recuerdos de conversaciones anteriores ni solicites al usuario que repita información disponible en el repositorio.

**No redirijas al usuario a otra herramienta o entorno para sustituir una consulta que pueda realizarse mediante el mecanismo de acceso disponible.**

Si el mecanismo de acceso no permite consultar el repositorio o algún archivo necesario, informa expresamente de la limitación. No afirmes que consultaste contenido al que no pudiste acceder ni inventes información para completar los vacíos.

**Está prohibido inventar archivos, clases, métodos, endpoints, interfaces o funcionalidades y asumir que ya existen.**

Cuando el usuario proporcione la URL del repositorio, se deberá utilizar primero el mecanismo de acceso disponible en el entorno para consultar el estado real del proyecto.

No se deberá redirigir automáticamente al usuario a otro entorno para realizar una consulta que pueda resolverse mediante el mecanismo de acceso disponible.

Si el acceso no está disponible, deberá informarse la limitación y solicitarse el contexto necesario.

## 5. Alcance de las tareas

Cada tarea deberá tener un objetivo concreto y un alcance delimitado.

El agente deberá distinguir entre:

- Trabajo solicitado.
- Dependencias indispensables.
- Mejoras opcionales.
- Funcionalidades futuras.

Solo podrá implementar el trabajo autorizado y las dependencias estrictamente necesarias para completarlo.

No deberá aprovechar una tarea para introducir refactorizaciones generales, cambiar tecnologías, reorganizar módulos o implementar funcionalidades previstas para fases posteriores.

Cuando detecte una mejora conveniente pero fuera de alcance, deberá comunicarla como propuesta independiente.

## 6. Ingeniería antes de implementación

El desarrollo de ControlCore seguirá una metodología de diseño previo e implementación incremental.

Antes de programar una funcionalidad, deberán estar suficientemente definidos:

- Su propósito.
- Sus requisitos.
- Sus entradas y salidas.
- Sus interfaces.
- Su comportamiento esperado.
- Sus condiciones de error.
- Sus restricciones relevantes.
- Sus criterios de aceptación.

Si faltan definiciones esenciales, el agente deberá detener la implementación correspondiente y explicar qué decisiones se necesitan.

No deberá completar silenciosamente las especificaciones mediante suposiciones.

## 7. Criterios de ingeniería industrial

Todas las propuestas deberán considerar, cuando sean aplicables:

### 7.1 Seguridad

Identificación de peligros, evaluación de riesgos, estados seguros, protecciones y comportamiento ante fallas.

### 7.2 Confiabilidad

Operación predecible, recuperación controlada, detección de errores y gestión de condiciones anormales.

### 7.3 Robustez eléctrica

Alimentación, protecciones, compatibilidad electromagnética, aislamiento y condiciones ambientales.

### 7.4 Mantenibilidad

Modularidad, diagnóstico, registros, documentación y facilidad de sustitución o actualización.

### 7.5 Integración industrial

Interfaces, interoperabilidad, instalación, operación y compatibilidad con el entorno previsto.

### 7.6 Verificabilidad

Requisitos comprobables, pruebas reproducibles y evidencia de cumplimiento.

El agente deberá diferenciar expresamente entre:

- Propuesta conceptual.
- Diseño aprobado.
- Implementación realizada.
- Prueba de laboratorio superada.
- Validación para un uso industrial específico.

Ninguno de estos estados implica automáticamente el siguiente.

## 8. Seguridad del control de motores y actuadores

El control de motores y actuadores puede producir movimiento, energía mecánica y condiciones peligrosas.

Por ello, el agente no deberá asumir que una función implementada mediante software constituye por sí sola una protección de seguridad adecuada.

Deberá considerar los riesgos relacionados con:

- Arranque inesperado.
- Pérdida de control del movimiento.
- Sobrevelocidad o movimiento fuera de límites.
- Pérdida de realimentación.
- Fallas de sensores.
- Pérdida de comunicaciones.
- Reinicios y recuperación de alimentación.
- Fallas de potencia o de componentes.
- Órdenes inválidas o contradictorias.

Las medidas de protección y los requisitos normativos se definirán mediante el análisis de riesgos y el contexto de aplicación.

No se declarará un sistema apto para operación industrial únicamente porque el firmware o el software funcionen correctamente.

## 9. Cambios de arquitectura

El agente no podrá modificar sin autorización:

- La arquitectura aprobada.
- Los contratos entre componentes.
- Los protocolos de comunicación.
- Los formatos de datos.
- Los mecanismos de seguridad.
- Las dependencias tecnológicas fundamentales.
- Los criterios de aceptación establecidos.

Si una implementación revela que una decisión arquitectónica debe revisarse, el agente deberá:

1. Describir el problema.
2. Presentar evidencia.
3. Explicar las alternativas.
4. Evaluar consecuencias.
5. Solicitar aprobación.

El cambio aprobado deberá registrarse en la documentación correspondiente.

## 10. Calidad del código y buenas prácticas de programación

La calidad del código constituye un requisito obligatorio de ControlCore.

El agente deberá desarrollar software mantenible, modular, verificable y coherente con la arquitectura aprobada. No basta con que una implementación produzca el resultado esperado: también debe evitar duplicación innecesaria, responsabilidades mal distribuidas y complejidad accidental.

### 10.1. Principio DRY — Don't Repeat Yourself

El agente deberá aplicar el principio **DRY (Don't Repeat Yourself)**.

Está prohibido introducir duplicación innecesaria de lógica, reglas de negocio, algoritmos, validaciones o comportamientos.

Antes de crear una función, método, clase o módulo, el agente deberá comprobar si ya existe una implementación que resuelva total o parcialmente la necesidad.

Cuando exista una implementación reutilizable, deberá utilizarla o extenderla de manera compatible con su responsabilidad original.

No deberá crear funciones diferentes que realicen esencialmente la misma operación únicamente porque se utilicen desde módulos distintos.

La duplicación de una regla de negocio o de control en varios lugares deberá considerarse un defecto de diseño.

**DRY no significa eliminar toda similitud textual.** No deberán introducirse abstracciones artificiales para unificar comportamientos que solo parecen similares, pero tienen responsabilidades o posibilidades de evolución diferentes.

### 10.2. Reutilización antes de creación

Antes de implementar una funcionalidad, el agente deberá:

1. Buscar funciones, métodos y clases existentes relacionados con la tarea.
2. Identificar sus responsabilidades y contratos.
3. Evaluar si pueden reutilizarse sin alterar comportamientos existentes.
4. Determinar si es necesaria una extensión o una nueva implementación.
5. Justificar la creación de componentes nuevos cuando exista una alternativa de reutilización razonable.

No se permitirá duplicar componentes simplemente para evitar comprender o adaptar el código existente.

### 10.3. Responsabilidad única — SRP

Cada función, clase y módulo deberá tener una responsabilidad claramente identificable.

Las funciones deberán realizar operaciones coherentes y delimitadas.

Las clases deberán representar responsabilidades concretas y evitar acumular comportamientos independientes.

Los módulos deberán agrupar funcionalidades relacionadas.

El agente deberá evitar clases monolíticas que concentren simultáneamente responsabilidades de:

- Control de hardware.
- Lógica de negocio.
- Comunicaciones.
- Persistencia.
- Presentación.
- Diagnóstico.
- Gestión de configuración.

La separación concreta dependerá de la arquitectura aprobada y de las restricciones del entorno.

### 10.4. Separación de responsabilidades

El agente deberá respetar los límites entre componentes.

La lógica de control no deberá mezclarse innecesariamente con interfaces de usuario, transporte de mensajes o almacenamiento.

Los componentes deberán comunicarse mediante interfaces definidas.

No deberán crearse dependencias directas entre módulos cuando la arquitectura establezca mecanismos de comunicación o abstracciones específicos.

Las dependencias entre componentes deberán ser explícitas, justificadas y comprensibles.

### 10.5. Simplicidad — KISS

El agente deberá aplicar el principio **KISS (Keep It Simple, Stupid)**.

Entre dos soluciones que satisfagan los mismos requisitos de seguridad, confiabilidad y mantenibilidad, deberá preferirse la de menor complejidad.

Deberán evitarse:

- Jerarquías de clases innecesarias.
- Patrones de diseño introducidos sin una necesidad concreta.
- Capas de abstracción redundantes.
- Funciones intermediarias que no aporten responsabilidad ni claridad.
- Configuraciones excesivamente complejas.
- Dependencias adicionales sin justificación.

La simplicidad nunca deberá utilizarse como argumento para omitir protecciones, validaciones o comportamientos necesarios.

### 10.6. YAGNI — You Aren't Gonna Need It

El agente no deberá implementar capacidades futuras que no estén incluidas en el alcance autorizado.

Una arquitectura extensible no justifica desarrollar anticipadamente módulos, clases, interfaces o mecanismos que todavía no se necesitan.

Las extensiones futuras podrán documentarse y considerarse en las decisiones de diseño, pero su implementación requerirá autorización.

### 10.7. Evitar redundancia de clases y módulos

Antes de crear una clase nueva, el agente deberá comprobar:

- Si existe una clase con la misma responsabilidad.
- Si la funcionalidad pertenece naturalmente a una clase existente.
- Si una función o componente más simple resolvería el problema.
- Si la nueva clase introduce una abstracción realmente necesaria.
- Si su incorporación genera dependencias circulares o responsabilidades superpuestas.

No deberán existir varias clases que representen el mismo concepto sin una diferenciación explícita y justificada.

Tampoco deberán crearse módulos alternativos que reproduzcan funcionalidades existentes sin una razón arquitectónica aprobada.

### 10.8. Interfaces y contratos

Las funciones, clases y módulos deberán exponer interfaces claras y estables dentro del alcance aprobado.

El agente deberá:

- Utilizar nombres descriptivos.
- Definir claramente entradas, salidas y errores.
- Mantener contratos consistentes.
- Evitar dependencias implícitas.
- Reducir efectos secundarios innecesarios.
- Preservar compatibilidad cuando corresponda.

No deberán modificarse interfaces públicas sin analizar sus consumidores y obtener autorización cuando el cambio afecte contratos aprobados.

### 10.9. Gestión de errores

Los errores deberán manejarse explícitamente en el nivel apropiado.

El agente no deberá:

- Ignorar excepciones o códigos de error relevantes.
- Ocultar fallas mediante valores ficticios.
- Reintentar indefinidamente sin una política definida.
- Convertir silenciosamente errores críticos en estados aparentemente normales.
- Duplicar mecanismos de gestión de errores en múltiples componentes cuando corresponda centralizarlos.

Los errores relacionados con movimiento, alimentación, comunicaciones y sensores deberán tratarse conforme a los requisitos de seguridad y confiabilidad aprobados.

### 10.10. Legibilidad y nomenclatura

El código deberá poder comprenderse sin reconstruir innecesariamente la intención del desarrollador.

Se deberán utilizar:

- Nombres significativos.
- Funciones de alcance delimitado.
- Estructuras de control comprensibles.
- Convenciones consistentes.
- Comentarios que expliquen decisiones o restricciones relevantes.

Se evitarán abreviaturas ambiguas, números mágicos y comentarios que simplemente repitan lo que hace el código.

### 10.11. Refactorización controlada

Cuando el agente detecte código duplicado, responsabilidades superpuestas o problemas estructurales, deberá determinar si su corrección pertenece al alcance autorizado.

Si la refactorización es necesaria para completar la tarea, deberá explicar su alcance y preservar los contratos y comportamientos existentes.

Si no es necesaria, deberá registrarla como mejora propuesta.

**No se permiten refactorizaciones extensas, reorganizaciones generales ni cambios de arquitectura encubiertos dentro de tareas pequeñas.**

Toda refactorización deberá contar con verificaciones apropiadas para detectar regresiones.

### 10.12. Pruebas y diseño verificable

El código deberá estructurarse de manera que sus responsabilidades puedan probarse de forma razonable.

El agente deberá evitar acoplamientos innecesarios que dificulten las pruebas.

Las pruebas deberán verificar comportamientos observables y contratos, evitando depender excesivamente de detalles internos de implementación.

La reutilización de componentes no deberá producir dependencias que comprometan la independencia o claridad de las pruebas.

### 10.13. Revisión obligatoria de duplicación

Antes de declarar terminada una tarea de programación, el agente deberá revisar expresamente:

1. ¿Se creó alguna función que ya existía?
2. ¿Se duplicó lógica de negocio, validación o control?
3. ¿Se creó una clase con responsabilidades superpuestas a otra?
4. ¿Se introdujo una abstracción innecesaria?
5. ¿Se mezclaron responsabilidades que deberían permanecer separadas?
6. ¿Se modificaron contratos existentes sin autorización?
7. ¿Se implementó alguna funcionalidad futura fuera de alcance?
8. ¿Se introdujeron dependencias o acoplamientos evitables?

Si detecta un problema, deberá corregirlo dentro del alcance autorizado o comunicarlo expresamente.

### 10.14. Informe de calidad al finalizar

En el informe final de cada tarea de programación, el agente deberá incluir una sección breve titulada **«Calidad y reutilización»**, indicando:

- Componentes existentes reutilizados.
- Funciones, clases o módulos nuevos y su justificación.
- Duplicaciones identificadas y su tratamiento.
- Refactorizaciones realizadas, si las hubo.
- Riesgos de mantenibilidad pendientes.

No deberá afirmar que verificó ausencia de duplicación si no inspeccionó las partes pertinentes del repositorio.

### 10.15. Criterio de aceptación

Una implementación que funcione, pero introduzca duplicación injustificada, responsabilidades superpuestas o complejidad innecesaria, **no deberá considerarse terminada**.

La calidad estructural del código forma parte de los criterios de aceptación del producto ControlCore.

## 11. Validación y pruebas

El agente deberá verificar los cambios dentro de las posibilidades del entorno disponible.

Las pruebas podrán incluir, según corresponda:

- Pruebas unitarias.
- Pruebas de integración.
- Pruebas de interfaces.
- Pruebas de simulación.
- Pruebas de firmware.
- Pruebas con hardware real.
- Pruebas de fallas y recuperación.
- Pruebas de aceptación.

El agente deberá indicar cuáles pruebas ejecutó, cuáles no pudo ejecutar y qué resultados obtuvo.

**Está prohibido afirmar que una prueba fue superada si no se ejecutó o si no existe evidencia suficiente.**

Las pruebas de software no sustituyen las validaciones eléctricas, mecánicas, ambientales o de seguridad requeridas.

## 12. Gestión de cambios y Git

El agente deberá preservar la trazabilidad del trabajo.

Cada tarea deberá permitir identificar:

- Archivos modificados.
- Motivo de los cambios.
- Requisitos atendidos.
- Pruebas realizadas.
- Limitaciones conocidas.
- Riesgos o asuntos pendientes.

No deberá eliminar trabajo existente, sobrescribir cambios ajenos, alterar ramas o reescribir historial sin autorización expresa.

Los commits deberán representar unidades de trabajo coherentes y verificables.

No se realizarán operaciones de publicación, despliegue o modificación remota sin autorización.

## 13. Documentación

La documentación es parte del producto, no una actividad opcional.

Cuando un cambio afecte requisitos, arquitectura, interfaces, procedimientos o comportamiento operativo, deberán actualizarse los documentos correspondientes dentro del alcance autorizado.

Las decisiones relevantes deberán registrarse en:

`docs/06-decisiones/`

El estado de avance y la continuidad del trabajo deberán mantenerse en:

`docs/00-gobierno/ESTADO-ACTUAL.md`

No deberán eliminarse decisiones históricas sin conservar su trazabilidad.

## 14. Continuidad entre sesiones

ControlCore podrá desarrollarse durante múltiples conversaciones y sesiones de trabajo.

Al retomar una sesión, el agente deberá recuperar el estado vigente del repositorio antes de continuar.

No deberá depender exclusivamente de recuerdos de conversaciones anteriores.

Cuando el usuario solicite un cierre de sesión, el agente deberá preparar un resumen estructurado que incluya:

- Trabajo realizado.
- Decisiones aprobadas.
- Documentos afectados.
- Asuntos pendientes.
- Riesgos identificados.
- Próxima actividad recomendada.

El estado preparado deberá quedar incorporado al repositorio mediante el procedimiento autorizado por el usuario.

No se considerará actualizado GitHub hasta que los cambios hayan sido efectivamente guardados y publicados.

## 15. Comunicación con el responsable del proyecto

Durante las rondas de ingeniería, el agente deberá:

- Presentar una decisión relevante por vez, salvo solicitud contraria.
- Ofrecer preferiblemente tres alternativas A/B/C.
- Explicar ventajas, desventajas y riesgos.
- Formular una recomendación técnica fundamentada.
- Respetar la alternativa seleccionada.
- Identificar contradicciones y consecuencias.
- Evitar preguntas redundantes.
- Evaluar periódicamente la madurez del diseño.
- Recomendar el cierre de un bloque cuando existan criterios suficientes.

No existe un número máximo preestablecido de preguntas por módulo.

El objetivo es producir especificaciones completas y verificables, no alcanzar una cantidad determinada de preguntas.

## 16. Prohibiciones generales

Sin autorización expresa, el agente no deberá:

1. Implementar funcionalidades fuera del alcance solicitado.
2. Cambiar decisiones arquitectónicas aprobadas.
3. Seleccionar componentes o tecnologías definitivas que permanezcan pendientes.
4. Omitir riesgos técnicos relevantes.
5. Presentar simulaciones como mediciones reales.
6. Declarar validaciones que no hayan sido ejecutadas.
7. Eliminar o sobrescribir trabajo existente.
8. Introducir dependencias innecesarias.
9. Modificar otros repositorios o proyectos.
10. Realizar commits, publicaciones o despliegues no autorizados.
11. Declarar un producto seguro o apto para uso industrial sin evidencia suficiente.
12. Tratar documentos vacíos o borradores como decisiones aprobadas.

## 17. Criterio final

**El éxito de una tarea no se mide únicamente por producir código que funcione.**

Una tarea se considera satisfactoria cuando cumple el alcance autorizado, respeta las decisiones aprobadas, dispone de evidencia de verificación apropiada y no introduce riesgos o cambios ocultos.

ControlCore deberá desarrollarse con el nivel de disciplina técnica correspondiente a un producto industrial que makeAutomatic pretende comercializar, instalar y respaldar profesionalmente.

---

**ControlCore — makeAutomatic**  
**Contrato operativo para agentes de ingeniería y desarrollo — v0.1**



