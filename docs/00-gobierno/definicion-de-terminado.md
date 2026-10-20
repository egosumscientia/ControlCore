
# Definición de terminado — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Definición de terminado  
**Versión del documento:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería conceptual  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto  
**Tipo de proyecto:** Desarrollo de producto industrial comercial

---

## 1. Propósito

Este documento establece las condiciones que deberán cumplirse para declarar terminada una actividad, documento, decisión de ingeniería, componente, módulo o fase del proyecto ControlCore.

Su propósito es evitar que los trabajos se consideren completos únicamente porque se haya producido un entregable, escrito código, construido hardware o demostrado una funcionalidad en condiciones favorables.

La definición de terminado constituye un mecanismo de control de calidad y aceptación técnica.

ControlCore es un producto industrial comercial de makeAutomatic. Por tanto, la finalización de los trabajos deberá sustentarse en requisitos definidos, evidencias verificables, documentación coherente y aprobación de la autoridad correspondiente.

Este documento complementa los criterios establecidos en:

- `AGENTS.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/criterios-calidad.md`

La definición de terminado no sustituye los requisitos específicos, los criterios de aceptación particulares ni las obligaciones normativas aplicables.

## 2. Principio fundamental

Una actividad no estará terminada simplemente porque se haya ejecutado.

Un documento no estará terminado simplemente porque contenga información.

Una implementación no estará terminada simplemente porque funcione.

Una prueba no estará terminada simplemente porque se haya ejecutado.

Una fase no estará terminada simplemente porque se hayan completado las tareas previstas.

Para declarar terminado un trabajo deberán cumplirse las condiciones de aceptación correspondientes a su naturaleza, alcance y criticidad.

La finalización deberá sustentarse en evidencia suficiente y no exclusivamente en afirmaciones del ejecutor.

## 3. Alcance de aplicación

La definición de terminado se aplicará, según corresponda, a:

1. Documentos de gobierno.
2. Documentos de requisitos.
3. Decisiones de ingeniería.
4. Diseños arquitectónicos.
5. Especificaciones de módulos.
6. Diseños de hardware.
7. Implementaciones de firmware.
8. Implementaciones de software.
9. Interfaces y comunicaciones.
10. Integraciones entre componentes.
11. Actividades de pruebas.
12. Actividades de validación.
13. Entregas y versiones del producto.
14. Fases del proyecto.

No todos los criterios serán aplicables a todas las actividades.

La evaluación deberá utilizar los criterios generales de este documento y los criterios específicos aprobados para cada entrega.

No deberán exigirse pruebas de implementación a un documento conceptual ni considerarse terminada una implementación únicamente porque su documentación esté completa.

## 4. Estados de los trabajos

Para evitar ambigüedades, los entregables deberán distinguir entre los siguientes estados.

### 4.1. Pendiente

El trabajo está identificado, pero no ha comenzado.

### 4.2. En elaboración

El trabajo se encuentra en desarrollo y todavía no cumple todas las condiciones necesarias para su revisión.

### 4.3. En revisión

El entregable está disponible para evaluación técnica, pero todavía no cuenta con aprobación definitiva.

### 4.4. Requiere correcciones

La revisión ha identificado incumplimientos, defectos, contradicciones o información insuficiente que impiden su aceptación.

### 4.5. Terminado

El entregable cumple los criterios de aceptación aplicables, dispone de las evidencias necesarias y ha recibido la aprobación correspondiente.

### 4.6. Reabierto

Un trabajo anteriormente terminado requiere modificaciones como consecuencia de nuevos requisitos, defectos, cambios aprobados o evidencias posteriores.

El estado terminado no implica que un componente sea inmutable.

Los cambios posteriores deberán gestionarse mediante los procedimientos de control establecidos.

## 5. Condiciones generales de terminado

Una actividad podrá declararse terminada cuando se cumplan todas las condiciones generales que resulten aplicables.

### 5.1. Alcance definido

El objetivo del trabajo está identificado.

Los límites de la actividad son claros.

No existen ampliaciones de alcance introducidas sin autorización.

### 5.2. Requisitos satisfechos

Los requisitos aplicables han sido atendidos.

Las restricciones relevantes han sido respetadas.

Los criterios de aceptación definidos para la actividad se han cumplido.

### 5.3. Coherencia técnica

El resultado es consistente con la arquitectura y las decisiones aprobadas.

No introduce contradicciones conocidas con otros componentes o documentos vigentes.

### 5.4. Calidad

El trabajo cumple los criterios de calidad correspondientes.

No presenta defectos conocidos que impidan su aceptación.

### 5.5. Verificación

Se han realizado las verificaciones exigidas para la actividad.

Los resultados están documentados.

Las pruebas no ejecutadas están identificadas y justificadas.

### 5.6. Documentación

La documentación necesaria está completa y corresponde al resultado entregado.

Los cambios relevantes están registrados.

### 5.7. Trazabilidad

Es posible identificar los requisitos, decisiones y evidencias relacionados con el trabajo.

### 5.8. Riesgos

Los riesgos relevantes han sido identificados y tratados de acuerdo con el alcance y la fase correspondiente.

Los riesgos residuales que requieran aceptación están documentados y sometidos a la autoridad competente.

### 5.9. Aprobación

El responsable autorizado ha revisado y aceptado el resultado.

La ejecución satisfactoria de una actividad no sustituye la aprobación requerida.

## 6. Definición de terminado para documentos de gobierno

Un documento de gobierno podrá declararse terminado cuando:

1. Su propósito esté claramente establecido.
2. Su alcance esté delimitado.
3. Sus reglas sean comprensibles y aplicables.
4. No existan contradicciones conocidas con documentos superiores o decisiones vigentes.
5. Las responsabilidades estén identificadas cuando corresponda.
6. Las condiciones de aplicación estén definidas.
7. El documento utilice terminología consistente.
8. No presente ambigüedades relevantes.
9. Se encuentre en la ubicación correspondiente del repositorio.
10. Disponga de identificación de versión y estado.
11. Haya sido revisado y aprobado por el responsable del proyecto.

Un documento extenso no se considerará necesariamente completo.

La calidad documental dependerá de su precisión, coherencia, utilidad y capacidad de orientar decisiones y actividades reales.

La incorporación al repositorio, la ejecución de un commit o push y la actualización de la bitácora no constituyen aprobación. La aprobación requiere una decisión expresa del responsable del proyecto conforme a `metodologia-diseno.md`.

No deberán introducirse reglas redundantes o contradictorias únicamente para aumentar el nivel de detalle.

## 7. Definición de terminado para requisitos

Un conjunto de requisitos podrá declararse terminado para un alcance determinado cuando:

1. El alcance funcional esté definido.
2. Los requisitos relevantes estén identificados.
3. Los requisitos sean comprensibles.
4. No existan contradicciones internas conocidas.
5. Las restricciones estén documentadas.
6. Las dependencias relevantes estén identificadas.
7. Los requisitos sean verificables.
8. Existan criterios de aceptación apropiados.
9. Se hayan identificado los requisitos relacionados con seguridad.
10. Los requisitos cuenten con trazabilidad.
11. Los asuntos pendientes que impidan el diseño estén resueltos.
12. El conjunto haya sido revisado y aprobado.

No será necesario conocer todos los requisitos futuros del producto para cerrar un bloque de requisitos.

Sin embargo, deberán estar suficientemente definidos aquellos que condicionan el diseño o la implementación del alcance aprobado.

Los requisitos pendientes que afecten decisiones esenciales impedirán declarar terminado el bloque correspondiente.

## 8. Definición de terminado para decisiones de ingeniería

Una decisión de ingeniería podrá declararse terminada cuando:

1. El problema esté claramente identificado.
2. Se conozca el contexto de la decisión.
3. Se hayan identificado las restricciones relevantes.
4. Se hayan evaluado alternativas técnicas apropiadas.
5. Se hayan analizado ventajas y desventajas.
6. Se hayan considerado riesgos y consecuencias.
7. Exista una justificación técnica suficiente.
8. Se haya seleccionado una alternativa.
9. La selección haya sido aprobada por el responsable del proyecto.
10. La decisión esté documentada.
11. Sus consecuencias para otros componentes estén identificadas.

La metodología de ControlCore contempla la presentación de alternativas A, B y C para las decisiones relevantes, conforme a lo establecido en `metodologia-diseno.md`.

La recomendación de un agente de inteligencia artificial no constituye una decisión aprobada.

Una decisión no deberá considerarse terminada cuando dependa de información crítica que todavía no ha sido obtenida.

Cuando una decisión aprobada deba modificarse, deberá aplicarse el procedimiento de revisión correspondiente.

## 9. Definición de terminado para arquitectura

Un diseño arquitectónico podrá declararse terminado para un alcance determinado cuando:

1. Sus objetivos estén definidos.
2. Los requisitos relacionados estén identificados.
3. Los componentes principales estén delimitados.
4. Las responsabilidades estén distribuidas.
5. Las interfaces estén especificadas.
6. Las dependencias estén identificadas.
7. Los flujos relevantes estén descritos.
8. Las restricciones técnicas estén consideradas.
9. Los mecanismos de gestión de fallas estén definidos cuando corresponda.
10. Los requisitos de seguridad aplicables estén considerados.
11. Las decisiones relevantes estén documentadas.
12. La arquitectura permita establecer una estrategia de verificación.
13. Las incertidumbres críticas estén resueltas.
14. El diseño haya sido revisado y aprobado.

La arquitectura deberá tener suficiente madurez para orientar la implementación sin depender de suposiciones esenciales.

No será obligatorio diseñar anticipadamente todas las capacidades futuras del producto.

La extensibilidad deberá considerarse sin introducir complejidad innecesaria.

## 10. Definición de terminado para especificaciones de módulos

La especificación de un módulo podrá declararse terminada cuando:

1. Su propósito esté definido.
2. Sus responsabilidades estén delimitadas.
3. Sus requisitos estén identificados.
4. Sus entradas y salidas estén especificadas.
5. Sus interfaces estén definidas.
6. Su comportamiento normal esté descrito.
7. Sus estados relevantes estén identificados.
8. Sus condiciones de error estén definidas.
9. Sus restricciones estén documentadas.
10. Sus dependencias estén identificadas.
11. Sus criterios de aceptación estén establecidos.
12. Sus requisitos de seguridad aplicables estén considerados.
13. Su integración con otros módulos sea comprensible.
14. La especificación haya sido aprobada.

La especificación deberá permitir que un implementador comprenda qué debe construir y cómo se verificará su comportamiento.

No deberá trasladarse al implementador la responsabilidad de inventar decisiones esenciales que debieron resolverse durante el diseño.

## 11. Definición de terminado para hardware

Un diseño o implementación de hardware podrá declararse terminado para su fase correspondiente cuando:

1. Los requisitos eléctricos y funcionales estén definidos.
2. Los componentes seleccionados estén justificados.
3. Los esquemas estén documentados.
4. Los niveles eléctricos sean compatibles.
5. Los márgenes de operación estén evaluados.
6. Las protecciones necesarias estén consideradas.
7. Las interfaces estén definidas.
8. Las restricciones térmicas y ambientales aplicables estén consideradas.
9. Los riesgos eléctricos y mecánicos relevantes estén evaluados.
10. Los cálculos o análisis necesarios estén disponibles.
11. Las revisiones de diseño correspondientes estén completadas.
12. Las pruebas exigidas para la fase estén ejecutadas.
13. Los resultados estén documentados.
14. Las no conformidades relevantes estén tratadas.
15. El entregable haya recibido aprobación.

Deberá distinguirse expresamente entre:

- Diseño de hardware terminado.
- Prototipo construido.
- Prototipo verificado en laboratorio.
- Hardware validado para una aplicación determinada.
- Hardware autorizado para una entrega comercial.

La aprobación de uno de estos estados no implicará automáticamente los siguientes.

## 12. Definición de terminado para firmware

Una implementación de firmware podrá declararse terminada cuando:

1. Cumpla los requisitos aprobados.
2. Respete la arquitectura definida.
3. Utilice interfaces y contratos establecidos.
4. Presente inicialización controlada.
5. Gestione correctamente sus estados.
6. Trate explícitamente las condiciones de error.
7. Respete las restricciones de memoria aplicables.
8. Cumpla las restricciones temporales verificables.
9. Gestione adecuadamente las comunicaciones.
10. Presente comportamiento definido ante reinicios.
11. No introduzca duplicación innecesaria.
12. Mantenga responsabilidades claramente delimitadas.
13. Cuente con pruebas apropiadas.
14. Disponga de resultados verificables.
15. Incluya la documentación necesaria.
16. No presente defectos conocidos que impidan su aceptación.
17. Haya sido revisada y aprobada.

Los requisitos temporales deberán verificarse mediante procedimientos apropiados.

No deberán declararse garantías de tiempo real sin evidencia suficiente.

Cuando el firmware controle actuadores o elementos que puedan producir condiciones peligrosas, su aceptación deberá considerar los requisitos de seguridad correspondientes.

## 13. Definición de terminado para software

Una implementación de software podrá declararse terminada cuando:

1. Cumpla el alcance autorizado.
2. Satisfaga los requisitos aplicables.
3. Respete la arquitectura aprobada.
4. Utilice correctamente los componentes existentes.
5. No duplique innecesariamente lógica o responsabilidades.
6. Aplique los principios DRY, SRP, KISS y YAGNI.
7. Mantenga interfaces claras.
8. Gestione errores de manera explícita.
9. Evite dependencias innecesarias.
10. Mantenga una estructura comprensible.
11. Incluya pruebas apropiadas.
12. No introduzca regresiones conocidas.
13. Disponga de documentación suficiente.
14. Mantenga trazabilidad de cambios.
15. No incluya funcionalidades futuras fuera de alcance.
16. Haya sido revisada y aprobada.

La ejecución correcta de un programa no será evidencia suficiente para declarar terminada su implementación.

También deberán evaluarse la calidad estructural, la reutilización y la mantenibilidad.

Las implementaciones con duplicaciones injustificadas, responsabilidades superpuestas o complejidad accidental relevante no deberán aceptarse como terminadas.

## 14. Definición de terminado para interfaces y comunicaciones

Una interfaz podrá declararse terminada cuando:

1. Su propósito esté definido.
2. Sus participantes estén identificados.
3. Sus entradas y salidas estén especificadas.
4. Los formatos de datos estén documentados.
5. Las unidades y rangos estén definidos cuando corresponda.
6. Las condiciones de error estén identificadas.
7. Los mecanismos de detección de fallas estén establecidos.
8. Las restricciones temporales estén documentadas cuando correspondan.
9. El comportamiento ante pérdida de comunicación esté definido.
10. El comportamiento de recuperación esté definido.
11. La compatibilidad entre componentes esté verificada.
12. Las pruebas aplicables estén completadas.
13. La interfaz haya sido aprobada.

No deberán considerarse garantizadas propiedades de entrega, orden, integridad o disponibilidad que el mecanismo de comunicación no proporcione.

Los contratos aprobados deberán respetarse durante la implementación.

## 15. Definición de terminado para integración

Una actividad de integración podrá declararse terminada cuando:

1. Los componentes participantes estén identificados.
2. Sus versiones sean conocidas.
3. Las interfaces sean compatibles.
4. Los contratos de comunicación se cumplan.
5. Las secuencias de inicialización funcionen conforme al diseño.
6. Los estados compartidos sean coherentes.
7. Las restricciones temporales aplicables se cumplan.
8. Los mecanismos de gestión de errores funcionen según lo especificado.
9. Se hayan evaluado las fallas de integración relevantes.
10. Se hayan ejecutado las pruebas requeridas.
11. Los resultados estén documentados.
12. Los defectos que impidan la aceptación estén resueltos.
13. La integración haya sido aprobada.

La integración no se considerará terminada únicamente porque los componentes puedan intercambiar información o ejecutar una secuencia funcional básica.

Deberá comprobarse el comportamiento conjunto en las condiciones definidas para el alcance correspondiente.

## 16. Definición de terminado para pruebas

Una actividad de pruebas podrá declararse terminada cuando:

1. Su objetivo esté definido.
2. Los requisitos evaluados estén identificados.
3. El procedimiento esté documentado.
4. Las condiciones de ejecución sean conocidas.
5. Los criterios de aceptación estén establecidos.
6. La versión del componente evaluado esté identificada.
7. Las pruebas previstas se hayan ejecutado o sus excepciones estén justificadas y aprobadas.
8. Los resultados observados estén registrados.
9. Las evidencias necesarias estén disponibles.
10. Las desviaciones estén identificadas.
11. Las conclusiones sean consistentes con los resultados.
12. El informe haya sido revisado.

La finalización de una actividad de pruebas no significa necesariamente que el componente haya superado todas las pruebas.

Una campaña de pruebas puede estar terminada y concluir que el producto no cumple los criterios de aceptación.

Los resultados deberán registrarse sin alterar ni ocultar evidencias desfavorables.

No se permitirá declarar superada una prueba no ejecutada.

## 17. Definición de terminado para validación

Una actividad de validación podrá declararse terminada cuando:

1. El contexto de aplicación esté definido.
2. Los requisitos de uso estén identificados.
3. Las condiciones operativas estén especificadas.
4. Los riesgos relevantes estén evaluados.
5. Los procedimientos de validación estén establecidos.
6. Las pruebas exigidas estén ejecutadas.
7. Los resultados estén documentados.
8. Las limitaciones estén identificadas.
9. Los riesgos residuales estén evaluados.
10. Las no conformidades estén tratadas.
11. Las conclusiones estén respaldadas por evidencia.
12. La autoridad competente haya emitido la decisión correspondiente.

La validación deberá distinguirse de la verificación.

La verificación determina si el producto cumple los requisitos especificados.

La validación determina si el producto resulta adecuado para el uso previsto en las condiciones establecidas.

Una validación favorable para una aplicación no deberá extrapolarse automáticamente a otras aplicaciones con condiciones o riesgos diferentes.

## 18. Definición de terminado para seguridad industrial

Las actividades relacionadas con seguridad industrial deberán contar con criterios de cierre específicos derivados del análisis de riesgos y de los requisitos aplicables.

Cuando corresponda, deberán verificarse:

1. Identificación de peligros.
2. Evaluación de riesgos.
3. Definición de medidas de reducción de riesgos.
4. Especificación de funciones de seguridad.
5. Selección justificada de mecanismos de protección.
6. Implementación conforme al diseño aprobado.
7. Verificación de las medidas implementadas.
8. Validación de funciones de seguridad cuando sea exigible.
9. Documentación de riesgos residuales.
10. Cumplimiento de requisitos normativos aplicables.
11. Participación de personal competente.
12. Aprobación por la autoridad correspondiente.

No deberá considerarse terminada una actividad de seguridad cuando existan peligros relevantes sin evaluación o medidas necesarias sin verificar.

La aprobación interna de makeAutomatic no sustituirá evaluaciones, certificaciones o autorizaciones exigibles.

## 19. Definición de terminado para documentación técnica

Una entrega documental podrá declararse terminada cuando:

1. Corresponda al alcance definido.
2. Contenga la información necesaria.
3. Utilice terminología consistente.
4. Sea coherente con el diseño aprobado.
5. Identifique versiones y estados.
6. Mantenga referencias correctas.
7. No contenga contradicciones conocidas.
8. Distinga hechos, hipótesis y decisiones.
9. Describa las limitaciones relevantes.
10. Permita comprender o reproducir el trabajo cuando corresponda.
11. Se encuentre almacenada en el repositorio.
12. Haya sido revisada y aprobada.

No será obligatorio incluir información irrelevante para completar una plantilla.

La documentación deberá ser suficiente, precisa y mantenible, evitando redundancia innecesaria.

## 20. Definición de terminado para tareas ejecutadas por agentes de IA

Una tarea realizada por un agente de inteligencia artificial podrá declararse terminada cuando:

1. El agente haya consultado el contexto necesario.
2. El alcance autorizado esté respetado.
3. No se hayan introducido cambios fuera de alcance.
4. Se hayan respetado las decisiones aprobadas.
5. Los archivos modificados estén identificados.
6. Las implementaciones estén justificadas.
7. Se haya evaluado la reutilización de componentes existentes.
8. No se haya introducido duplicación injustificada.
9. Se hayan ejecutado las verificaciones disponibles.
10. Las pruebas no ejecutadas estén declaradas.
11. Los resultados estén documentados.
12. Los riesgos y limitaciones estén identificados.
13. La documentación afectada esté actualizada.
14. El agente haya presentado un informe de trabajo.
15. El responsable del proyecto haya revisado y aceptado la entrega.

El agente no podrá declarar aprobada una tarea por iniciativa propia.

El informe del agente deberá diferenciar entre:

- Trabajo realizado.
- Trabajo verificado.
- Trabajo pendiente.
- Limitaciones del entorno.
- Riesgos conocidos.
- Decisiones que requieren aprobación.

Cuando la tarea incluya programación, deberá incorporarse la revisión de calidad y reutilización establecida en `AGENTS.md`.

## 21. Definición de terminado para una fase

Una fase del proyecto podrá declararse terminada cuando:

1. Sus objetivos estén identificados.
2. Los entregables obligatorios estén definidos.
3. Los requisitos de salida estén establecidos.
4. Los trabajos requeridos estén completados.
5. Las verificaciones necesarias estén ejecutadas.
6. Las evidencias estén disponibles.
7. Las no conformidades que impidan el cierre estén resueltas.
8. Los riesgos relevantes estén tratados.
9. La documentación esté actualizada.
10. Las decisiones pendientes que bloqueen la siguiente fase estén identificadas y resueltas.
11. Exista una evaluación de cierre.
12. El responsable del proyecto haya aprobado formalmente la finalización.

El cierre de una fase deberá distinguirse de la autorización para comenzar la siguiente.

Una fase podrá estar técnicamente terminada y requerir decisiones adicionales antes de continuar.

No deberá asumirse que el cierre de una fase de laboratorio constituye autorización para utilizar el producto en condiciones industriales.

## 22. Evidencias de terminado

Las evidencias deberán ser apropiadas al tipo de trabajo.

Podrán incluir:

- Documentos aprobados.
- Registros de decisiones.
- Revisiones técnicas.
- Cálculos.
- Diagramas.
- Esquemas eléctricos.
- Archivos de diseño.
- Código fuente.
- Resultados de análisis estático.
- Registros de pruebas.
- Mediciones.
- Informes de simulación.
- Fotografías de montaje.
- Registros de laboratorio.
- Informes de integración.
- Informes de validación.
- Registros de aceptación.

Las evidencias deberán permitir identificar qué se evaluó, bajo qué condiciones y con qué resultado.

Cuando corresponda, deberán relacionarse con una versión concreta del componente o sistema.

No deberán utilizarse evidencias de versiones anteriores para justificar automáticamente la aceptación de versiones modificadas.

## 23. No conformidades y asuntos pendientes

Antes de declarar terminado un trabajo deberán revisarse los defectos, las no conformidades y los asuntos pendientes relacionados.

Los asuntos pendientes deberán clasificarse según su impacto.

### 23.1. Bloqueantes

Impiden demostrar el cumplimiento de requisitos, comprometen condiciones de seguridad o hacen imposible verificar aspectos esenciales del alcance.

Un trabajo con asuntos bloqueantes abiertos no podrá declararse terminado.

### 23.2. No bloqueantes

Son asuntos que no impiden cumplir los criterios de aceptación del alcance evaluado.

Podrán mantenerse abiertos únicamente cuando:

- Estén identificados.
- Su impacto haya sido evaluado.
- No comprometan requisitos obligatorios.
- No oculten riesgos inaceptables.
- Exista una justificación documentada.
- Su tratamiento posterior esté definido cuando corresponda.
- La autoridad competente haya aceptado expresamente su permanencia.

### 23.3. Mejoras futuras

Son capacidades, optimizaciones o ampliaciones que no forman parte del alcance aprobado.

No deberán impedir el cierre de una tarea cuando no sean necesarias para satisfacer sus requisitos.

Las mejoras futuras deberán registrarse separadamente y no implementarse sin autorización.

## 24. Reapertura de trabajos terminados

Un trabajo terminado podrá reabrirse cuando:

- Se identifique un defecto relevante.
- Cambien requisitos aprobados.
- Se modifique una interfaz relacionada.
- Se apruebe una modificación arquitectónica.
- Aparezcan nuevos riesgos.
- Se detecten contradicciones documentales.
- Las pruebas posteriores revelen incumplimientos.
- Cambien condiciones de aplicación que afecten la validez de la aceptación.

La reapertura deberá identificar el motivo, el alcance afectado y las verificaciones necesarias.

No será obligatorio repetir todas las pruebas anteriores si puede justificarse técnicamente un alcance de regresión más limitado.

La aceptación anterior deberá conservarse como registro histórico, sin presentarse como evidencia suficiente para una versión modificada.

## 25. Responsabilidad de aceptación

La persona o equipo que ejecuta una tarea es responsable de presentar el resultado y sus evidencias.

La revisión técnica deberá evaluar el cumplimiento de los criterios aplicables.

El responsable del proyecto conserva la autoridad sobre la aprobación de entregables y fases dentro de sus competencias.

Cuando una actividad requiera intervención de especialistas o entidades competentes, su participación deberá incorporarse al proceso de aceptación.

Los agentes de inteligencia artificial podrán recomendar el cierre de una tarea, pero no sustituir la decisión de aprobación.

No deberá confundirse:

- Ejecución.
- Verificación.
- Revisión.
- Aceptación.
- Autorización de uso industrial.

Cada actividad representa una responsabilidad diferente.

## 26. Registro de cierre

El cierre de un trabajo relevante deberá dejar constancia de:

1. Identificación del trabajo.
2. Objetivo y alcance.
3. Entregables producidos.
4. Requisitos atendidos.
5. Verificaciones realizadas.
6. Resultados obtenidos.
7. No conformidades relevantes.
8. Asuntos pendientes aceptados.
9. Limitaciones conocidas.
10. Versión o referencia del entregable.
11. Responsable de revisión.
12. Decisión de aceptación.
13. Fecha de cierre.

El nivel de detalle del registro deberá ser proporcional a la criticidad del trabajo.

El repositorio y sus mecanismos de control de versiones podrán utilizarse como parte de la evidencia de cierre.

No será necesario duplicar información que ya se encuentre registrada de manera confiable y trazable.

## 27. Relación con el estado actual del proyecto

El documento:

`docs/00-gobierno/ESTADO-ACTUAL.md`

funcionará como registro de continuidad y cierre de las sesiones de ingeniería.

Su actualización se realizará al finalizar cada sesión de trabajo, después de completar las actividades documentales y técnicas correspondientes.

Deberá resumir:

- Trabajos realizados durante la sesión.
- Documentos creados o modificados.
- Decisiones aprobadas.
- Actividades terminadas.
- Actividades en curso.
- Asuntos pendientes.
- Riesgos o bloqueos relevantes.
- Próximo paso recomendado.

Este registro no sustituirá los documentos técnicos ni los registros formales de decisiones y aceptación.

Su propósito será permitir la continuidad del proyecto sin perder el contexto de ingeniería entre sesiones.

La actualización de la bitácora no deberá utilizarse para declarar terminados trabajos que todavía no cumplan sus criterios de aceptación.

Tampoco constituye aprobación de documentos, decisiones ni entregables.

## 28. Lista general de comprobación

Antes de proponer el cierre de una actividad, deberá comprobarse lo siguiente:

- [ ] El objetivo está definido.
- [ ] El alcance autorizado se ha respetado.
- [ ] Los requisitos aplicables están identificados.
- [ ] Los criterios de aceptación están establecidos.
- [ ] El trabajo cumple los requisitos correspondientes.
- [ ] El resultado es coherente con el diseño aprobado.
- [ ] Las interfaces afectadas son consistentes.
- [ ] Los riesgos relevantes han sido evaluados.
- [ ] Las verificaciones requeridas están completas.
- [ ] Los resultados están documentados.
- [ ] Las no conformidades bloqueantes están resueltas.
- [ ] Los asuntos pendientes están identificados.
- [ ] La documentación necesaria está actualizada.
- [ ] Los cambios son trazables.
- [ ] Las limitaciones conocidas están declaradas.
- [ ] La revisión técnica correspondiente se ha realizado.
- [ ] La aceptación requerida ha sido otorgada.

Esta lista constituye una referencia general.

No todos sus elementos serán aplicables a todas las actividades.

Los criterios específicos del entregable prevalecerán en cuanto al detalle técnico requerido, sin eliminar obligaciones generales de seguridad, calidad o trazabilidad.

## 29. Relación con otros documentos

Este documento deberá aplicarse conjuntamente con:

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/criterios-calidad.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/01-requisitos/`
- `docs/02-arquitectura/`
- `docs/03-seguridad-industrial/`
- `docs/04-modulos/`
- `docs/05-validacion/`
- `docs/06-decisiones/`
- `docs/07-roadmap/`

Los criterios de calidad establecen las propiedades y condiciones generales que debe satisfacer el producto.

La definición de terminado establece cuándo existe evidencia suficiente para aceptar un trabajo.

Los criterios de aceptación específicos determinan las condiciones técnicas concretas de cada componente o entrega.

La metodología de diseño establece cómo se analizan y aprueban las decisiones de ingeniería.

Estos documentos deberán mantenerse coherentes y complementarios.

## 30. Principio de cierre

En ControlCore, terminar significa demostrar que un trabajo cumple las condiciones acordadas para su alcance y fase de desarrollo.

La finalización no deberá basarse únicamente en la cantidad de trabajo realizado, la existencia de código, la construcción de un prototipo o la ejecución de pruebas aisladas.

Todo entregable deberá evaluarse mediante requisitos, criterios de calidad, verificaciones y evidencias apropiadas.

Una implementación funcional podrá continuar abierta si presenta defectos estructurales, riesgos no tratados o verificaciones pendientes que impidan su aceptación.

Un diseño podrá declararse terminado sin que exista todavía una implementación física, siempre que cumpla los criterios de madurez y aprobación establecidos para esa etapa.

Una campaña de pruebas podrá declararse terminada aunque sus resultados sean desfavorables, siempre que la ejecución y sus conclusiones estén correctamente documentadas.

La aptitud de ControlCore para una aplicación industrial deberá establecerse mediante los procesos de evaluación, verificación, validación y autorización correspondientes.

El objetivo de esta definición es asegurar que cada avance del proyecto represente un resultado técnicamente sustentado, verificable y coherente con el desarrollo de un producto industrial profesional.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
