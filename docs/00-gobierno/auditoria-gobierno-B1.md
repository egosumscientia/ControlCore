# Auditoría del gobierno documental — B1

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Auditoría integral del gobierno documental  
**Versión:** 0.1  
**Estado:** Informe de auditoría — no aprobatorio  
**Fase:** Gobierno documental  
**Fecha:** 2026-10-19  
**Alcance:** cinco documentos sustantivos de gobierno

---

## 1. Objetivo y alcance

Este informe documenta la auditoría integral de los cinco documentos sustantivos de gobierno de ControlCore, realizada durante el bloque B1.2.

La auditoría evalúa consistencia, claridad, autoridad, requisitos, trazabilidad, riesgos, seguridad industrial, verificación, control de cambios, criterios de cierre, independencia de proveedores de IA, ausencia de decisiones técnicas prematuras, referencias documentales y duplicaciones.

La auditoría es documental. No verifica la aptitud técnica, eléctrica, mecánica, ambiental o de seguridad del producto, ni sustituye la aprobación del responsable del proyecto.

## 2. Documentos auditados y versiones

| Documento | Versión | Estado | Fecha de revisión |
|---|---|---|---|
| `docs/00-gobierno/vision-producto.md` | 0.1 | Propuesta para aprobación | 2026-10-19 |
| `docs/00-gobierno/principios-ingenieria.md` | 0.1 | Propuesta para aprobación | 2026-10-19 |
| `docs/00-gobierno/metodologia-diseno.md` | 0.1 | Propuesta para aprobación | 2026-10-19 |
| `docs/00-gobierno/criterios-calidad.md` | 0.1 | Propuesta para aprobación | 2026-10-19 |
| `docs/00-gobierno/definicion-de-terminado.md` | 0.1 | Propuesta para aprobación | 2026-10-19 |

Documentos de apoyo consultados: `README.md`, `AGENTS.md`, `docs/00-gobierno/ESTADO-ACTUAL.md`, `docs/06-decisiones/registro-decisiones.md` y `docs/04-modulos/README.md`.

## 3. Criterios de auditoría

1. Consistencia entre documentos.
2. Claridad y ausencia de ambigüedades.
3. Autoridad y mecanismos de aprobación.
4. Gestión de requisitos.
5. Trazabilidad.
6. Gestión de riesgos e incertidumbres.
7. Seguridad industrial.
8. Verificación y validación.
9. Control de cambios.
10. Criterios de aceptación y cierre.
11. Independencia de proveedores de IA.
12. Ausencia de decisiones técnicas prematuras.
13. Referencias documentales.
14. Duplicaciones y contradicciones.

## 4. Método y evidencia

La auditoría se realizó mediante:

- Lectura completa de los cinco documentos y de sus documentos de apoyo.
- Comparación de reglas equivalentes entre documentos.
- Búsqueda de referencias específicas a proveedores o herramientas de IA.
- Verificación de rutas documentales citadas.
- Verificación de estados y versiones declarados.
- Verificación de identificadores de decisiones.
- Revisión del diff de las correcciones aplicadas.
- Comprobación de que los documentos no seleccionan tecnologías, componentes ni arquitecturas.

No se ejecutaron pruebas de software ni ensayos de hardware porque el repositorio no contiene código ni prototipos en esta fase.

## 5. Clasificación de severidad

- **Bloqueante:** impide la aprobación o compromete la trazabilidad, la seguridad o la integridad del gobierno.
- **Alta:** afecta una regla central y puede producir decisiones incompatibles.
- **Media:** inconsistencia que puede generar interpretaciones divergentes.
- **Baja:** defecto editorial o de referencias sin impacto en obligaciones.
- **Informativa:** observación de estilo, metadatos o brecha de fase.

## 6. Hallazgos

### H-01 — Referencias específicas a proveedores de IA en la metodología

- **Severidad:** Media.
- **Documento:** `docs/00-gobierno/metodologia-diseno.md`.
- **Ubicación:** secciones 17, 19, 21 y 23.
- **Evidencia:** el título de la sección 17 nombraba a Codex; la sección 19 atribuía el historial de conversaciones a ChatGPT; la sección 21 se titulaba «Consulta de repositorios desde ChatGPT» y dependía de su conector; la sección 23 contenía instrucciones para redirigir a Work.
- **Impacto:** las reglas metodológicas quedaban vinculadas a proveedores concretos y resultaban incompatibles con DEC-GOB-008 y con la neutralidad ya adoptada en `README.md` y `AGENTS.md`.
- **Tratamiento:** corregido mediante generalización a «agentes de IA», «mecanismo de acceso disponible en el entorno» y «otra herramienta o entorno».
- **Estado:** Corregido.

### H-02 — Referencias incompletas al directorio de módulos

- **Severidad:** Baja.
- **Documentos:** `vision-producto.md` (sección 13), `criterios-calidad.md` (sección 24) y `definicion-de-terminado.md` (sección 29).
- **Evidencia:** las listas de documentos relacionados no incluían `docs/04-modulos/`, creado en B1.1, aunque la definición de terminado dedica su sección 10 a las especificaciones de módulos y los criterios de calidad son aplicables a ellas.
- **Impacto:** reducción de descubribilidad y de trazabilidad documental; no alteraba ninguna obligación.
- **Tratamiento:** corregido mediante la incorporación de `docs/04-modulos/` o «Las especificaciones de módulos» en las listas correspondientes.
- **Estado:** Corregido.

### H-03 — Estilo mixto de referencias internas

- **Severidad:** Baja.
- **Documentos:** `metodologia-diseno.md` (secciones 18, 22, 25.1 y 26), `criterios-calidad.md` (sección 12) y `definicion-de-terminado.md` (sección 6).
- **Evidencia:** algunas referencias usan la ruta completa desde la raíz del repositorio y otras usan únicamente el nombre del archivo (`principios-ingenieria.md`, `criterios-calidad.md`, `ESTADO-ACTUAL.md`, `metodologia-diseno.md`).
- **Impacto:** inconsistencia de estilo; las referencias son comprensibles por contexto y no están rotas.
- **Tratamiento:** no corregido. Se recomienda normalizar las rutas en una revisión editorial posterior.
- **Estado:** Pendiente no bloqueante.

### H-04 — Colisión terminológica del estado «En revisión»

- **Severidad:** Media.
- **Documentos:** `metodologia-diseno.md` (secciones 24.1 y 25.2) y `definicion-de-terminado.md` (sección 4.3).
- **Evidencia:** el término «En revisión» se usa con tres alcances distintos: documento previamente aprobado sujeto a revisión, requisito previamente aprobado sujeto a modificación y entregable disponible para evaluación sin aprobación definitiva.
- **Impacto:** posibilidad de confusión al reportar estados. Cada sección delimita su ámbito, por lo que no existe una contradicción directa.
- **Tratamiento:** no corregido. La armonización de vocabulario modificaría reglas de gobierno y requiere decisión del responsable del proyecto. Se recomienda un glosario o denominaciones diferenciadas.
- **Estado:** Pendiente no bloqueante.

### H-05 — Campos del registro de decisiones frente a la metodología

- **Severidad:** Baja.
- **Documentos:** `metodologia-diseno.md` (sección 10) y `docs/06-decisiones/registro-decisiones.md`.
- **Evidencia:** la metodología enumera identificador, fecha, bloque, problema, contexto, alternativas, recomendación, selección aprobada, justificación, consecuencias, riesgos, dependencias, estado y referencias para los registros de decisiones; las entradas DEC-GOB usan contenido, justificación, estado y origen, con el calificador «cuando corresponda» en la metodología.
- **Impacto:** posible expectativa de que toda entrada del registro contenga el conjunto completo de campos.
- **Tratamiento:** no corregido. Se recomienda aclarar que el conjunto completo aplica a decisiones arquitectónicas (ADR) y que las reglas de gobierno pueden usar un formato reducido.
- **Estado:** Pendiente no bloqueante.

### H-06 — Etiquetas de metadatos no uniformes

- **Severidad:** Informativa.
- **Documentos:** los cinco documentos auditados.
- **Evidencia:** `vision-producto.md`, `principios-ingenieria.md` y `metodologia-diseno.md` usan «Versión»; `criterios-calidad.md` y `definicion-de-terminado.md` usan «Versión del documento» y añaden «Tipo de proyecto».
- **Impacto:** diferencia cosmética; no afecta la interpretación ni las obligaciones.
- **Tratamiento:** no corregido. Se recomienda normalizar las etiquetas en una revisión editorial posterior.
- **Estado:** Informativa.

### H-07 — Documentos técnicos aún vacíos

- **Severidad:** Informativa (brecha de fase).
- **Documentos:** `docs/01-requisitos/`, `docs/02-arquitectura/`, `docs/03-seguridad-industrial/`, `docs/05-validacion/` y `docs/06-decisiones/pendientes.md`.
- **Evidencia:** los archivos no contienen especificaciones ni registros.
- **Impacto:** no es posible auditar requisitos, arquitectura, riesgos ni validación en esta fase. Es una condición esperada y declarada en `ESTADO-ACTUAL.md`.
- **Tratamiento:** ninguno en B1.2. Su desarrollo requiere autorización de bloques posteriores.
- **Estado:** Brecha de fase, no defecto de gobierno.

### H-08 — Ausencia de contradicciones críticas y de decisiones técnicas prematuras

- **Severidad:** Informativa (resultado favorable).
- **Evidencia:** no se identificaron selecciones de tecnologías, componentes, protocolos o arquitecturas en los cinco documentos. `vision-producto.md` (sección 11) declara expresamente las exclusiones de la fase conceptual. Las reglas de autoridad, aprobación, requisitos, trazabilidad, seguridad y cierre son compatibles entre sí.
- **Estado:** Sin hallazgo.

## 7. Correcciones realizadas

1. **H-01:** generalización de las referencias a proveedores de IA en `metodologia-diseno.md` (secciones 17, 19, 21 y 23).
2. **H-02:** incorporación de `docs/04-modulos/` o «Las especificaciones de módulos» en las listas de documentos relacionados de `vision-producto.md` (sección 13), `criterios-calidad.md` (sección 24) y `definicion-de-terminado.md` (sección 29).
3. **DEC-GOB-008:** registro formal de la decisión de independencia de proveedores y herramientas de IA en `docs/06-decisiones/registro-decisiones.md`.

No se modificaron decisiones, obligaciones, alcance ni estados de aprobación de los documentos auditados.

## 8. Hallazgos pendientes y riesgos residuales

### 8.1. Hallazgos pendientes no bloqueantes

- **H-03:** estilo mixto de referencias internas.
- **H-04:** colisión terminológica del estado «En revisión».
- **H-05:** diferencia entre los campos de la metodología y el formato del registro.
- **H-06:** etiquetas de metadatos no uniformes.

Ninguno impide la aprobación, pero su permanencia debe ser aceptada expresamente o corregida antes de la aprobación formal.

### 8.2. Riesgos residuales

- Aprobar los documentos con observaciones editoriales no bloqueantes sin dejar constancia de su aceptación.
- Interpretar los documentos técnicos vacíos como especificaciones aprobadas.
- Mantener tres acepciones de «En revisión» y generar confusión en la bitácora o en los registros de requisitos.
- Confundir la aprobación de una regla de gobierno o de un documento con la aptitud industrial del producto.
- No sustituir la auditoría documental por las evaluaciones técnicas, eléctricas, mecánicas, ambientales y de seguridad que correspondan en fases posteriores.

## 9. Evaluación individual y recomendación

| Documento | Evaluación | Recomendación |
|---|---|---|
| `vision-producto.md` | Propósito, alcance, actores, exclusiones y criterios de éxito coherentes. Sin decisiones técnicas prematuras. H-02 corregido. | **Aprobación** |
| `principios-ingenieria.md` | Principios completos de producto, requisitos, seguridad, confiabilidad, calidad, verificación y ciclo de vida. Sin referencias de proveedor. | **Aprobación** |
| `metodologia-diseno.md` | Autoridad, alternativas, estados, trazabilidad, requisitos, control documental y cierre coherentes. H-01 corregido; H-04 y H-05 pendientes no bloqueantes. | **Aprobación condicionada** |
| `criterios-calidad.md` | Criterios completos por disciplina, trazabilidad, verificación, defectos y aceptación. H-02 corregido; H-03 y H-06 son editoriales. | **Aprobación** |
| `definicion-de-terminado.md` | Condiciones de cierre completas por tipo de entregable, evidencias, no conformidades y reapertura. H-02 corregido; H-04 pendiente no bloqueante. | **Aprobación condicionada** |

Las recomendaciones individuales de «Aprobación» indican ausencia de hallazgos bloqueantes en el documento correspondiente. No constituyen aprobación y quedan sujetas a la condición global indicada a continuación.

**Recomendación global: aprobación condicionada.**

La documentación es internamente coherente, no contiene decisiones técnicas prematuras y cubre los criterios de gobierno evaluados. No se identificaron hallazgos bloqueantes.

La condición es que el responsable del proyecto acepte formalmente los hallazgos no bloqueantes H-03 a H-06 o autorice su corrección antes de la aprobación. La metodología y la definición de terminado requieren especial atención por H-04 y H-05.

Esta recomendación no constituye una aprobación. La decisión corresponde al responsable del proyecto y debe registrarse conforme a `metodologia-diseno.md` (sección 24).

## 10. Conclusión

Los cinco documentos sustantivos de gobierno se encuentran en condiciones de ser sometidos a aprobación formal, con las observaciones no bloqueantes indicadas.

La auditoría no encontró contradicciones críticas, decisiones técnicas prematuras ni referencias específicas de proveedor después de las correcciones aplicadas.

La aprobación formal, su alcance, sus condiciones y su registro corresponden exclusivamente al responsable del proyecto.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
