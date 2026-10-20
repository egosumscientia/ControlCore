# Restricciones del sistema — ControlCore

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Tipo de proyecto:** Desarrollo de producto industrial comercial  
**Documento:** Restricciones del sistema  
**Versión:** 0.1  
**Estado:** Aprobado  
**Fase:** Ingeniería de requisitos  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** 2026-10-19 — Responsable del proyecto ControlCore, makeAutomatic

---

## 1. Propósito

Este documento constituye el registro de las restricciones del sistema de ControlCore.

Las restricciones describen condiciones, límites o exigencias externas que condicionan el producto sin definir por sí mismas un comportamiento funcional ni un atributo de calidad interno.

## 2. Alcance

Este registro comprende exclusivamente restricciones identificadas con el prefijo `RES-###`.

No comprende requisitos funcionales ni no funcionales, que se registran en:

- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`

Las restricciones podrán provenir de normativa, condiciones ambientales, interfaces externas, requisitos del cliente, limitaciones físicas o decisiones de gobierno. Su origen deberá documentarse.

No se ha definido ninguna restricción. No se ha asignado ningún identificador `RES-###`. La línea base de gestión de requisitos está aprobada; no existe una línea base de restricciones concretas.

## 3. Convenciones

Se aplican las convenciones comunes de `docs/01-requisitos/README.md` (sección 3).

- Prefijo: `RES-###`.
- El identificador es único, estable y no reutilizable.
- La versión del contenido es independiente del identificador.
- No se asigna un identificador hasta que exista una restricción definida y registrada.
- Se aplican las convenciones de prioridad y trazabilidad de `docs/01-requisitos/README.md` (secciones 3 y 5).
- La versión de este documento es independiente de la versión de cada requisito individual.
- Las referencias documentales utilizan rutas relativas a la raíz del repositorio.

## 4. Estructura de registro

La ficha normalizada y la obligatoriedad de cada atributo se definen en `docs/01-requisitos/README.md` (sección 4).

El registro de restricciones utiliza la siguiente estructura:

| Identificador | Título | Fuente | Estado | Versión | Alcance de aplicación | Criterio de aceptación | Método de verificación |
|---|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — | — |

**No hay restricciones registradas.** La fila anterior es únicamente una referencia de columnas y no constituye una restricción.

## 5. Estados

Se aplica el ciclo de vida y las transiciones definidos en `docs/01-requisitos/README.md` (sección 5).

La aprobación corresponde al responsable del proyecto. No se establecen aprobaciones automáticas.

## 6. Criterios de calidad

Además de los criterios generales de `docs/01-requisitos/README.md` (sección 6), cada restricción deberá:

- Identificar su fuente externa o de gobierno.
- Delimitar su alcance de aplicación.
- Ser verificable o evaluable mediante un método definido.
- No ocultar una decisión de diseño, tecnología o arquitectura no aprobada.
- No establecer umbrales de seguridad sin análisis de riesgos y justificación documentada.
- No duplicar ni contradecir requisitos o restricciones existentes.
- Ser trazable hacia su fuente y hacia su verificación.

Una restricción que implique una tecnología concreta deberá formularse como condición externa y no como selección tecnológica del proyecto.

## 7. Trazabilidad

Se aplica el mecanismo de trazabilidad de `docs/01-requisitos/README.md` (sección 7).

Cada restricción deberá permitir relacionar, cuando corresponda:

**Fuente externa o de gobierno → `RES-###` → Decisión → Elemento de arquitectura → Implementación → Prueba → Evidencia.**

El vínculo de necesidad del producto podrá registrarse como **No aplica** cuando la restricción provenga de una fuente externa o normativa, con la justificación y la referencia correspondientes.

No existen todavía vínculos registrados porque no se han definido restricciones ni elementos de arquitectura, implementación, prueba o evidencia.

Los vínculos se registrarán como **Existente**, **Pendiente** o **No aplica** según el índice común. No se presupone que todos los elementos existan.

## 8. Pendientes

- No se han definido restricciones.
- No se ha asignado ningún identificador `RES-###`.
- Las convenciones de identificación, versiones, estados, prioridad y trazabilidad están aprobadas (DEC-GOB-010 a DEC-GOB-014).
- La estructura documental está aprobada (DEC-GOB-015).
- La evaluación de normativa aplicable y de condiciones ambientales o de interfaz requiere los análisis correspondientes.
- No existe línea base de restricciones concretas.

## 9. Referencias

- `README.md`
- `AGENTS.md`
- `docs/01-requisitos/README.md`
- `docs/00-gobierno/vision-producto.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md` (secciones 24, 25 y 26)
- `docs/00-gobierno/criterios-calidad.md` (secciones 3, 5, 9 y 13)
- `docs/00-gobierno/definicion-de-terminado.md` (secciones 7, 19 y 20)
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/06-decisiones/registro-decisiones.md`
- `docs/06-decisiones/pendientes.md`
- `docs/02-arquitectura/` (futuro)
- `docs/03-seguridad-industrial/` (futuro)
- `docs/05-validacion/` (futuro)

## 10. Historial de cambios

- **0.1 — 2026-10-19 — B2.1:** estructura inicial del registro de restricciones. Sin restricciones definidas.
- **0.1 — 2026-10-19 — B2.1.1:** aprobación de la estructura y de la línea base de gestión de requisitos (DEC-GOB-010 a DEC-GOB-015).

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*
