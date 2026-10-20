# Auditoría del gobierno documental — B1

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Auditoría integral del gobierno documental  
**Versión:** 0.2  
**Estado:** Informe de auditoría — no aprobatorio  
**Fase:** Gobierno documental  
**Fecha:** 2026-10-19  
**Actualización:** B1.3 — resolución de hallazgos H-03 a H-06  
**Alcance:** cinco documentos sustantivos de gobierno

---

## 1. Objetivo y alcance

Este informe documenta la auditoría integral de los cinco documentos sustantivos de gobierno de ControlCore, realizada durante el bloque B1.2 y actualizada durante B1.3 con la resolución de los hallazgos H-03 a H-06.

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

Las correcciones de B1.3 no modificaron la versión ni el estado de aprobación de los cinco documentos.

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

En B1.3 se añadieron comprobaciones de normalización de rutas, uniformidad de metadatos y correspondencia entre el esquema de la metodología y el registro de decisiones.

No se ejecutaron pruebas de software ni ensayos de hardware porque el repositorio no contiene código ni prototipos en esta fase.

## 5. Clasificación de severidad

- **Bloqueante:** impide la aprobación o compromete la trazabilidad, la seguridad o la integridad del gobierno.
- **Alta:** afecta una regla central y puede producir decisiones incompatibles.
- **Media:** inconsistencia que puede generar interpretaciones divergentes.
- **Baja:** defecto editorial o de referencias sin impacto en obligaciones.
- **Informativa:** observación de estilo, metadatos o brecha de fase.

## 6. Hallazgos

| Identificador | Hallazgo | Severidad | Estado |
|---|---|---|---|
| H-01 | Referencias específicas a proveedores de IA en la metodología | Media | Corregido en B1.2 |
| H-02 | Referencias incompletas al directorio de módulos | Baja | Corregido en B1.2 |
| H-03 | Estilo mixto de referencias internas | Baja | Resuelto en B1.3 |
| H-04 | Colisión terminológica del estado «En revisión» | Media | Resuelto en B1.3 |
| H-05 | Campos del registro de decisiones frente a la metodología | Baja | Resuelto en B1.3 |
| H-06 | Etiquetas de metadatos no uniformes | Informativa | Resuelto en B1.3 |
| H-07 | Documentos técnicos aún vacíos | Informativa | Brecha de fase |
| H-08 | Ausencia de contradicciones críticas y decisiones técnicas prematuras | Informativa | Sin hallazgo |

### H-01 — Referencias específicas a proveedores de IA en la metodología

- **Severidad:** Media.
- **Documento:** `docs/00-gobierno/metodologia-diseno.md`.
- **Ubicación:** secciones 17, 19, 21 y 23.
- **Evidencia histórica:** el título de la sección 17 nombraba a Codex; la sección 19 atribuía el historial de conversaciones a ChatGPT; la sección 21 se titulaba «Consulta de repositorios desde ChatGPT» y dependía de su conector; la sección 23 contenía instrucciones para redirigir a Work.
- **Impacto:** las reglas metodológicas quedaban vinculadas a proveedores concretos y resultaban incompatibles con DEC-GOB-008 y con la neutralidad ya adoptada en `README.md` y `AGENTS.md`.
- **Tratamiento:** corregido en B1.2 mediante generalización a «agentes de IA», «mecanismo de acceso disponible en el entorno» y «otra herramienta o entorno».
- **Estado:** Corregido en B1.2.

### H-02 — Referencias incompletas al directorio de módulos

- **Severidad:** Baja.
- **Documentos:** `docs/00-gobierno/vision-producto.md` (sección 13), `docs/00-gobierno/criterios-calidad.md` (sección 24) y `docs/00-gobierno/definicion-de-terminado.md` (sección 29).
- **Evidencia:** las listas de documentos relacionados no incluían `docs/04-modulos/`, creado en B1.1, aunque la definición de terminado dedica su sección 10 a las especificaciones de módulos y los criterios de calidad son aplicables a ellas.
- **Impacto:** reducción de descubribilidad y de trazabilidad documental; no alteraba ninguna obligación.
- **Tratamiento:** corregido en B1.2 mediante la incorporación de `docs/04-modulos/` o «Las especificaciones de módulos» en las listas correspondientes.
- **Estado:** Corregido en B1.2.

### H-03 — Estilo mixto de referencias internas

- **Severidad:** Baja.
- **Documentos:** `docs/00-gobierno/metodologia-diseno.md`, `docs/00-gobierno/criterios-calidad.md` y `docs/00-gobierno/definicion-de-terminado.md`.
- **Evidencia histórica:** algunas referencias usaban la ruta completa desde la raíz del repositorio y otras usaban únicamente el nombre del archivo.
- **Impacto:** inconsistencia de estilo; las referencias eran comprensibles por contexto y no estaban rotas.
- **Corrección B1.3:** se normalizaron las referencias internas a rutas relativas a la raíz del repositorio en los documentos afectados y en los documentos de apoyo que citaban archivos del gobierno.
- **Archivos afectados:** `docs/00-gobierno/metodologia-diseno.md`, `docs/00-gobierno/criterios-calidad.md`, `docs/00-gobierno/definicion-de-terminado.md`, `docs/00-gobierno/ESTADO-ACTUAL.md`, `docs/06-decisiones/registro-decisiones.md` y este informe.
- **Evidencia verificable:** todas las referencias internas a documentos utilizan rutas relativas a la raíz; por ejemplo, `docs/00-gobierno/metodologia-diseno.md`, o los archivos de raíz `README.md` y `AGENTS.md`. La comprobación de rutas existentes no reportó errores.
- **Estado:** Resuelto en B1.3.
- **Riesgo residual:** las referencias futuras deben mantener la convención; no existe una verificación automatizada permanente.

### H-04 — Colisión terminológica del estado «En revisión»

- **Severidad:** Media.
- **Documentos:** `docs/00-gobierno/metodologia-diseno.md` y `docs/00-gobierno/definicion-de-terminado.md`.
- **Evidencia histórica:** el término se usaba para documentos previamente aprobados sujetos a revisión, requisitos previamente aprobados sujetos a modificación, entregables disponibles para evaluación y decisiones que debían reconsiderarse.
- **Impacto:** posibilidad de confusión al reportar estados. Cada sección delimitaba su ámbito, por lo que no existía una contradicción directa.
- **Corrección B1.3:** se establecieron denominaciones inequívocas:
  - **Revisión de decisión:** nueva evidencia exige reconsiderar una decisión anterior.
  - **Revisión de documento aprobado:** una versión aprobada se encuentra sujeta a revisión.
  - **Revisión de requisito aprobado:** un requisito aprobado se encuentra sujeto a modificación.
  - **En evaluación:** un entregable está disponible para evaluación técnica y todavía no cuenta con aprobación definitiva.
- **Archivos afectados:** `docs/00-gobierno/metodologia-diseno.md` (secciones 9, 24.1, 24.3, 25.2 y 25.3), `docs/00-gobierno/definicion-de-terminado.md` (sección 4.3) y `docs/00-gobierno/ESTADO-ACTUAL.md`.
- **Evidencia verificable:** las definiciones de estado de los cinco documentos no reutilizan el término ambiguo; las transiciones, restricciones y autoridades se conservaron.
- **Estado:** Resuelto en B1.3.
- **Riesgo residual:** los documentos futuros deben usar el vocabulario diferenciado; no existe un glosario central automatizado.

### H-05 — Campos del registro de decisiones frente a la metodología

- **Severidad:** Baja.
- **Documentos:** `docs/00-gobierno/metodologia-diseno.md` (sección 10) y `docs/06-decisiones/registro-decisiones.md`.
- **Evidencia histórica:** la metodología enumeraba el conjunto completo de campos para los registros de decisiones, mientras que las entradas DEC-GOB usaban un formato reducido de contenido, justificación, estado y origen.
- **Impacto:** posible expectativa de que toda entrada del registro contuviera el conjunto completo de campos.
- **Corrección B1.3:** la sección 10 de la metodología se dividió en dos formatos expresos:
  - **DEC-GOB (sección 10.1):** identificador, título, contenido, justificación documentada, estado y referencia de origen.
  - **ADR (sección 10.2):** identificador, fecha, bloque, problema, contexto, alternativas evaluadas, recomendación, alternativa seleccionada, justificación, consecuencias, riesgos, dependencias, estado y referencias.
- **Archivos afectados:** `docs/00-gobierno/metodologia-diseno.md` (sección 10) y `docs/06-decisiones/registro-decisiones.md` (sección 2).
- **Evidencia verificable:** el registro conserva los ocho registros DEC-GOB-001 a DEC-GOB-008, sin cambios en su contenido decisional; solo se normalizaron referencias de ruta conforme a H-03. No se añadieron decisiones técnicas ni datos históricos. El formato ADR contiene todos los campos exigidos por la metodología.
- **Estado:** Resuelto en B1.3.
- **Riesgo residual:** aún no existe ningún registro ADR; el formato se ejercitará cuando se adopte la primera decisión arquitectónica o técnica.

### H-06 — Etiquetas de metadatos no uniformes

- **Severidad:** Informativa.
- **Documentos:** los cinco documentos auditados.
- **Evidencia histórica:** tres documentos usaban «Versión» y dos usaban «Versión del documento»; además, solo dos incluían «Tipo de proyecto».
- **Impacto:** diferencia cosmética; no afectaba la interpretación ni las obligaciones.
- **Corrección B1.3:** se unificó el bloque de metadatos de los cinco documentos con el esquema: Proyecto, Empresa, Tipo de proyecto, Documento, Versión, Estado, Fase, Fecha de revisión y Aprobación.
- **Archivos afectados:** `docs/00-gobierno/vision-producto.md`, `docs/00-gobierno/principios-ingenieria.md`, `docs/00-gobierno/metodologia-diseno.md`, `docs/00-gobierno/criterios-calidad.md` y `docs/00-gobierno/definicion-de-terminado.md`.
- **Evidencia verificable:** los cinco encabezados utilizan las mismas etiquetas y el mismo orden; los valores de versión, estado, fase y fecha se conservaron; ningún documento cambió a estado aprobado.
- **Estado:** Resuelto en B1.3.
- **Riesgo residual:** los documentos futuros deben adoptar el mismo esquema; no existe una verificación automatizada permanente.

### H-07 — Documentos técnicos aún vacíos

- **Severidad:** Informativa (brecha de fase).
- **Documentos:** `docs/01-requisitos/`, `docs/02-arquitectura/`, `docs/03-seguridad-industrial/`, `docs/05-validacion/` y `docs/06-decisiones/pendientes.md`.
- **Evidencia:** los archivos no contienen especificaciones ni registros.
- **Impacto:** no es posible auditar requisitos, arquitectura, riesgos ni validación en esta fase. Es una condición esperada y declarada en `docs/00-gobierno/ESTADO-ACTUAL.md`.
- **Tratamiento:** ninguno en B1.3. Su desarrollo requiere autorización de bloques posteriores.
- **Estado:** Brecha de fase, no defecto de gobierno.

### H-08 — Ausencia de contradicciones críticas y de decisiones técnicas prematuras

- **Severidad:** Informativa (resultado favorable).
- **Evidencia:** no se identificaron selecciones de tecnologías, componentes, protocolos o arquitecturas en los cinco documentos. `docs/00-gobierno/vision-producto.md` (sección 11) declara expresamente las exclusiones de la fase conceptual. Las reglas de autoridad, aprobación, requisitos, trazabilidad, seguridad y cierre son compatibles entre sí.
- **Estado:** Sin hallazgo.

## 7. Correcciones realizadas

1. **H-01:** generalización de las referencias a proveedores de IA en `docs/00-gobierno/metodologia-diseno.md` (secciones 17, 19, 21 y 23), en B1.2.
2. **H-02:** incorporación de `docs/04-modulos/` o «Las especificaciones de módulos» en las listas de documentos relacionados de `docs/00-gobierno/vision-producto.md` (sección 13), `docs/00-gobierno/criterios-calidad.md` (sección 24) y `docs/00-gobierno/definicion-de-terminado.md` (sección 29), en B1.2.
3. **DEC-GOB-008:** registro formal de la decisión de independencia de proveedores y herramientas de IA en `docs/06-decisiones/registro-decisiones.md`, en B1.2.
4. **H-03:** normalización de referencias internas a rutas relativas a la raíz del repositorio, en B1.3.
5. **H-04:** denominaciones diferenciadas para los estados de decisión, documento, requisito y entregable, en B1.3.
6. **H-05:** separación de los formatos DEC-GOB y ADR en `docs/00-gobierno/metodologia-diseno.md`, en B1.3.
7. **H-06:** unificación del bloque de metadatos de los cinco documentos de gobierno, en B1.3.

No se modificaron decisiones técnicas, requisitos del producto, obligaciones sustantivas, alcance ni estados de aprobación.

## 8. Hallazgos pendientes y riesgos residuales

### 8.1. Hallazgos pendientes

No quedan hallazgos pendientes de H-01 a H-06.

H-07 se mantiene como brecha de fase: los documentos técnicos deberán desarrollarse en bloques posteriores autorizados.

### 8.2. Riesgos residuales

- Las referencias internas futuras deben mantener la convención de rutas relativas a la raíz.
- Los estados futuros deben usar las denominaciones diferenciadas de H-04.
- El formato ADR debe aplicarse cuando se registre la primera decisión arquitectónica o técnica.
- Los documentos futuros deben adoptar el esquema uniforme de metadatos.
- Interpretar los documentos técnicos vacíos como especificaciones aprobadas.
- Confundir la aprobación de una regla de gobierno o de un documento con la aptitud industrial del producto.
- No sustituir la auditoría documental por las evaluaciones técnicas, eléctricas, mecánicas, ambientales y de seguridad que correspondan en fases posteriores.

## 9. Evaluación individual y recomendación

| Documento | Evaluación | Recomendación |
|---|---|---|
| `docs/00-gobierno/vision-producto.md` | Propósito, alcance, actores, exclusiones y criterios de éxito coherentes. Sin decisiones técnicas prematuras. H-02 corregido; H-03 y H-06 resueltos. | **Aprobación** |
| `docs/00-gobierno/principios-ingenieria.md` | Principios completos de producto, requisitos, seguridad, confiabilidad, calidad, verificación y ciclo de vida. Sin referencias de proveedor. H-06 resuelto. | **Aprobación** |
| `docs/00-gobierno/metodologia-diseno.md` | Autoridad, alternativas, estados, trazabilidad, requisitos, control documental, esquema DEC-GOB/ADR y cierre coherentes. H-01 corregido; H-03 a H-06 resueltos. | **Aprobación** |
| `docs/00-gobierno/criterios-calidad.md` | Criterios completos por disciplina, trazabilidad, verificación, defectos y aceptación. H-02 corregido; H-03 y H-06 resueltos. | **Aprobación** |
| `docs/00-gobierno/definicion-de-terminado.md` | Condiciones de cierre completas por tipo de entregable, evidencias, no conformidades y reapertura. H-02 corregido; H-03, H-04 y H-06 resueltos. | **Aprobación** |

**Recomendación global: presentar los cinco documentos para aprobación formal.**

Los cuatro hallazgos pendientes de B1.2 quedaron resueltos. No se identificaron hallazgos bloqueantes ni defectos que impidan la aprobación.

Esta recomendación no constituye una aprobación. La decisión corresponde al responsable del proyecto y debe registrarse conforme a `docs/00-gobierno/metodologia-diseno.md` (sección 24).

## 10. Conclusión

Los cinco documentos sustantivos de gobierno se encuentran en condiciones de ser presentados para aprobación formal.

La auditoría no encontró contradicciones críticas, decisiones técnicas prematuras, referencias específicas de proveedor en las reglas operativas ni hallazgos pendientes de H-01 a H-06.

La aprobación formal, su alcance, sus condiciones y su registro corresponden exclusivamente al responsable del proyecto.

## 11. Historial de actualizaciones

- **v0.1 — B1.2:** auditoría inicial. Hallazgos H-01 a H-08. H-01 y H-02 corregidos; H-03 a H-06 pendientes no bloqueantes; H-07 brecha de fase; H-08 sin hallazgo.
- **v0.2 — B1.3:** resolución de H-03 a H-06. Normalización de referencias, diferenciación de estados, esquema DEC-GOB/ADR y unificación de metadatos. Recomendación actualizada a presentar los cinco documentos para aprobación formal.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
