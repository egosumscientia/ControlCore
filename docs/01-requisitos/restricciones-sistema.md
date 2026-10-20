# Restricciones del sistema — ControlCore

**Proyecto:** ControlCore
**Empresa:** makeAutomatic
**Tipo de proyecto:** Desarrollo de producto industrial comercial
**Documento:** Restricciones del sistema
**Versión:** 0.2
**Estado:** Revisión de documento aprobado — propuesta de restricciones candidatas
**Fase:** Ingeniería de requisitos
**Fecha de revisión:** 2026-10-20
**Aprobación:** Versión 0.1 aprobada el 2026-10-19 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.2 pendiente de aprobación

---

## 1. Propósito

Este documento constituye el registro de las restricciones candidatas del sistema de ControlCore para el primer incremento.

Las restricciones describen condiciones, límites o exigencias externas que condicionan el producto sin definir por sí mismas un comportamiento funcional ni un atributo de calidad interno.

## 2. Alcance

Este registro comprende exclusivamente restricciones identificadas con el prefijo `RES-###`.

No comprende requisitos funcionales ni no funcionales, que se registran en:

- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`

Las restricciones de este documento son **candidatas propuestas**. No constituyen una línea base, no están aprobadas y no autorizan pruebas físicas ni implementación.

## 3. Convenciones

Se aplican las convenciones comunes de `docs/01-requisitos/README.md` (sección 3).

- Prefijo: `RES-###`.
- El identificador es único, estable y no reutilizable.
- La versión del contenido es independiente del identificador.
- No se asigna un identificador hasta que exista una restricción definida y registrada.
- Se aplican las convenciones de prioridad y trazabilidad de `docs/01-requisitos/README.md` (secciones 3 y 5).
- La versión de este documento es independiente de la versión de cada requisito individual.
- Las referencias documentales utilizan rutas relativas a la raíz del repositorio.

## 4. Atributos comunes de los candidatos

Todos los candidatos de este documento tienen:

- **Tipo:** `RES`.
- **Estado:** Propuesto.
- **Versión:** 0.1.
- **Prioridad:** Pendiente de determinar.
- **Evidencia de verificación:** Pendiente.
- **Responsable de aprobación:** Responsable del proyecto.

La verificabilidad se indica en cada ficha. Una restricción con criterio incompleto no se declara verificable ni aprobable.

## 5. Índice de restricciones candidatas

| Identificador | Título | Fuente | Origen | Verificabilidad |
|---|---|---|---|---|
| RES-001 | Análisis de riesgos previo obligatorio | Gobierno y seguridad | D04–D18 | Completa documental |
| RES-002 | Jerarquía de reducción y riesgos residuales | Gobierno y seguridad | D07; D08; D10 | Completa documental |
| RES-003 | Autorización previa a energización y pruebas físicas | Gobierno y seguridad | D33–D38 | Completa documental |
| RES-004 | Prohibición de declarar conformidad o aceptación sin evidencia | Gobierno y seguridad | D38; B2.3-D17 | Completa documental |
| RES-005 | Registro y trazabilidad de pruebas y anomalías | Gobierno y verificación | D36; D37 | Completa documental |
| RES-006 | Prohibición de límites cuantitativos no justificados | Gobierno y metodología | D51; D52 | Completa documental |
| RES-007 | Alcance del sistema completo del banco | Gobierno y seguridad | D11 | Completa documental |

## 6. Restricciones candidatas

### RES-001 — Análisis de riesgos previo obligatorio

- **Descripción verificable:** No se definirán requisitos de seguridad ni se autorizarán pruebas físicas sin un análisis preliminar de peligros y riesgos que cubra el sistema completo del banco y las operaciones previstas.
- **Justificación:** La seguridad debe derivarse del análisis de riesgos y no de suposiciones sobre el comportamiento del software.
- **Origen:** B2.4-D04; B2.4-D05; B2.4-D06; B2.4-D09; B2.4-D10; B2.4-D11; B2.4-D12; B2.4-D13; B2.4-D14; B2.4-D15; B2.4-D16; B2.4-D17; B2.4-D18.
- **Decisiones relacionadas:** `DEC-GOB-017`; `DEC-GOB-019`.
- **Dependencias:** RES-007; RF-001–RF-022.
- **Riesgos relacionados:** HZ-001–HZ-023.
- **Condiciones de aplicación:** Antes de aprobar requisitos de seguridad, energizar el banco o ejecutar pruebas físicas.
- **Criterio de aceptación:** Existe un análisis documentado con peligros, causas, efectos, medidas, funciones de protección, requisitos derivados, riesgos pendientes y verificación futura; el documento fue revisado por el responsable del proyecto.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Aprobar la escala y los criterios de aceptación de riesgos.

### RES-002 — Jerarquía de reducción y riesgos residuales

- **Descripción verificable:** Cada peligro identificado deberá documentar la aplicación de la jerarquía de reducción del riesgo —diseño inherentemente seguro, medidas técnicas de protección e información sobre riesgos residuales— y el riesgo residual resultante.
- **Justificación:** Evitar que la información o la formación se utilicen como sustituto de medidas de ingeniería.
- **Origen:** B2.4-D07; B2.4-D08; B2.4-D10.
- **Decisiones relacionadas:** `DEC-GOB-017`.
- **Dependencias:** RES-001.
- **Riesgos relacionados:** Todos los peligros identificados.
- **Condiciones de aplicación:** Durante el análisis de riesgos y antes de cerrar la evaluación preliminar.
- **Criterio de aceptación:** Cada peligro registra las medidas consideradas en los tres niveles, la eficacia prevista y el riesgo residual; no se declara aceptación sin evaluación.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Definir criterios de eficacia y aceptación de riesgos residuales.

### RES-003 — Autorización previa a energización y pruebas físicas

- **Descripción verificable:** No se energizará el banco ni se ejecutarán pruebas físicas sin documentación del banco, protecciones, riesgos residuales, procedimiento, criterios de interrupción y autorización explícita del responsable del proyecto.
- **Justificación:** Evitar pruebas improvisadas o con protecciones no verificadas.
- **Origen:** B2.4-D33; B2.4-D34; B2.4-D35.
- **Decisiones relacionadas:** `DEC-GOB-021`.
- **Dependencias:** RES-001; RES-002; RES-005; RF-001–RF-022.
- **Riesgos relacionados:** HZ-002; HZ-019; HZ-020; HZ-022.
- **Condiciones de aplicación:** Antes de cualquier energización o prueba física.
- **Criterio de aceptación:** La compuerta de pruebas está completa y la autorización explícita está registrada. La autorización no se presume por la existencia de este documento.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Definir el procedimiento, los criterios de interrupción y la forma de autorización.

### RES-004 — Prohibición de declarar conformidad o aceptación sin evidencia

- **Descripción verificable:** Ningún documento, requisito o resultado podrá declarar conformidad con normas, aceptación definitiva de riesgos o aptitud para uso industrial sin la evaluación y la evidencia correspondientes.
- **Justificación:** Evitar declaraciones de seguridad o conformidad no sustentadas.
- **Origen:** B2.4-D38.
- **Decisiones relacionadas:** B2.3-D17; `DEC-GOB-017`.
- **Dependencias:** RES-001; RES-002.
- **Riesgos relacionados:** Todos los peligros identificados.
- **Condiciones de aplicación:** Toda declaración de seguridad, conformidad o aceptación.
- **Criterio de aceptación:** Toda declaración de conformidad o aceptación está vinculada a evaluación, evidencia y autoridad competente. La ausencia de evidencia impide la declaración.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Definir el proceso de evaluación de conformidad y la autoridad aplicable.

### RES-005 — Registro y trazabilidad de pruebas y anomalías

- **Descripción verificable:** Toda prueba deberá registrar condiciones iniciales, configuración, procedimiento, mediciones, resultados, anomalías y evidencias, vinculadas a requisitos y riesgos; toda prueba fallida deberá gestionarse con no conformidad, análisis de causa raíz, impacto, corrección y regresión.
- **Justificación:** Permitir la verificación reproducible y la reconstrucción de resultados.
- **Origen:** B2.4-D36; B2.4-D37.
- **Decisiones relacionadas:** B2.3-D58; B2.3-D59; `DEC-GOB-029`.
- **Dependencias:** RES-003; RF-001–RF-027; RNF-001–RNF-005.
- **Riesgos relacionados:** Todos los peligros verificables.
- **Condiciones de aplicación:** Toda prueba de análisis, simulación, laboratorio o banco.
- **Criterio de aceptación:** Cada prueba dispone de un registro completo y trazable; cada falla dispone de no conformidad, causa, impacto, corrección y regresión documentada.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Definir formato, herramientas y retención de evidencias.

### RES-006 — Prohibición de límites cuantitativos no justificados

- **Descripción verificable:** No se establecerán límites de tensión, corriente, temperatura, velocidad, tiempos de respuesta, tolerancias o umbrales de protección sin análisis, justificación y decisión documentada.
- **Justificación:** Evitar valores inventados o no sustentados que puedan comprometer la seguridad o el desempeño.
- **Origen:** B2.4-D51; B2.4-D52.
- **Decisiones relacionadas:** B2.3-D21; `DEC-GOB-021`.
- **Dependencias:** RES-001; RF-015–RF-018; RNF-001.
- **Riesgos relacionados:** HZ-004; HZ-007; HZ-009; HZ-010; HZ-012.
- **Condiciones de aplicación:** Definición de cualquier umbral, tolerancia o tiempo de respuesta.
- **Criterio de aceptación:** Todo valor cuantitativo es trazable a un análisis, una decisión aprobada o una fuente documentada; los valores no justificados permanecen pendientes.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Ninguno para la restricción; los valores concretos son materia de decisiones posteriores.

### RES-007 — Alcance del sistema completo del banco

- **Descripción verificable:** El análisis de riesgos y la verificación deberán cubrir el sistema completo del banco: motor, electrónica, alimentación, carga mecánica, sensores, control, operador y entorno.
- **Justificación:** Evitar que el análisis se limite al firmware y omita peligros eléctricos, mecánicos o del entorno.
- **Origen:** B2.4-D11.
- **Decisiones relacionadas:** `DEC-GOB-017`.
- **Dependencias:** RES-001.
- **Riesgos relacionados:** HZ-001–HZ-023.
- **Condiciones de aplicación:** Todo análisis de riesgos y plan de verificación del primer incremento.
- **Criterio de aceptación:** El alcance documentado identifica y cubre cada elemento del sistema completo del banco.
- **Método de verificación:** Inspección documental.
- **Verificabilidad:** Completa documental.
- **Pendientes técnicos:** Definir la composición concreta del banco y sus límites físicos.

## 7. Trazabilidad

| Restricción | Decisiones B2.4 | Decisiones B2.3 | Peligros | Verificación |
|---|---|---|---|---|
| RES-001 | D04–D18 | `DEC-GOB-017` | HZ-001–HZ-023 | Inspección documental |
| RES-002 | D07; D08; D10 | `DEC-GOB-017` | Todos | Inspección documental |
| RES-003 | D33–D38 | `DEC-GOB-021` | HZ-002; HZ-019; HZ-020; HZ-022 | Inspección documental |
| RES-004 | D38 | B2.3-D17 | Todos | Inspección documental |
| RES-005 | D36; D37 | B2.3-D58; B2.3-D59 | Todos | Inspección documental |
| RES-006 | D51; D52 | B2.3-D21 | HZ-004; HZ-007; HZ-009; HZ-010; HZ-012 | Inspección documental |
| RES-007 | D11 | `DEC-GOB-017` | HZ-001–HZ-023 | Inspección documental |

## 8. Pendientes

- Todas las restricciones son candidatas y están en estado **Propuesto**.
- Las prioridades no están determinadas.
- Los valores cuantitativos no están definidos.
- No existe línea base de restricciones.
- La aprobación corresponde al responsable del proyecto.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/necesidades-producto.md`
- `docs/01-requisitos/actores-uso.md`
- `docs/01-requisitos/escenarios-uso.md`
- `docs/03-seguridad-industrial/analisis-riesgos.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.4.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** estructura inicial del registro de restricciones. Sin restricciones definidas.
- **0.1 — 2026-10-19 — B2.1.1:** aprobación de la estructura y de la línea base de gestión de requisitos (DEC-GOB-010 a DEC-GOB-015).
- **0.2 — 2026-10-20 — B2.4:** incorporación de siete restricciones candidatas y trazabilidad a D01–D60. Ninguna restricción aprobada.
