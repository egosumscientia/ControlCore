# ControlCore

**Plataforma modular de control y supervisión industrial**

**Empresa:** makeAutomatic  
**Estado:** Ingeniería conceptual y diseño  
**Versión de documentación:** 0.1  
**Tipo de proyecto:** Desarrollo de producto industrial comercial

---

## 1. Descripción del proyecto

**ControlCore** es un proyecto de makeAutomatic orientado al desarrollo de una plataforma modular para el control, la supervisión y el diagnóstico de motores y actuadores utilizados en aplicaciones industriales.

El objetivo es construir un producto profesional que pueda evolucionar desde las primeras pruebas de laboratorio hasta su integración en máquinas, estaciones de trabajo, plantas de ensamblaje y líneas de producción.

ControlCore no se concibe únicamente como una demostración tecnológica ni como un ejercicio de programación. Su desarrollo debe responder a criterios de ingeniería industrial, confiabilidad, seguridad, mantenibilidad y calidad comercial.

## 2. Visión del producto

Desarrollar una plataforma de automatización industrial que permita implementar soluciones de control de movimiento y actuación mediante una arquitectura modular, documentada, verificable y extensible.

La plataforma deberá diseñarse considerando:

- Aplicaciones industriales reales.
- Integración con máquinas y sistemas de automatización.
- Supervisión y diagnóstico de funcionamiento.
- Operación confiable y comportamiento definido ante fallas.
- Mantenimiento y evolución del producto.
- Posibilidad de incorporar nuevos módulos y capacidades.
- Documentación técnica adecuada para implementación, instalación, operación y soporte.

Las capacidades específicas, tecnologías y configuraciones del producto se determinarán durante las fases de ingeniería.

## 3. Objetivo de ingeniería

El proyecto seguirá un proceso estructurado de desarrollo de producto que comprende:

1. Definición de requisitos y restricciones.
2. Evaluación de alternativas técnicas.
3. Selección y documentación de decisiones arquitectónicas.
4. Diseño de hardware, firmware, software e interfaces.
5. Análisis de riesgos y requisitos de seguridad industrial.
6. Planificación de implementación por fases.
7. Construcción de prototipos y validación experimental.
8. Integración, pruebas y verificación.
9. Preparación para despliegue, mantenimiento y comercialización.

El cumplimiento de una fase de laboratorio no constituye, por sí solo, evidencia suficiente de aptitud para operación industrial.

## 4. Principios fundamentales

El desarrollo de ControlCore se regirá por los siguientes principios:

**Orientación industrial:** las decisiones deben considerar condiciones reales de instalación, operación y mantenimiento.

**Seguridad:** los riesgos derivados del control de motores y actuadores deben identificarse, evaluarse y tratarse mediante medidas de ingeniería apropiadas.

**Confiabilidad:** el comportamiento del sistema debe ser predecible tanto durante la operación normal como ante fallas.

**Modularidad:** la arquitectura debe facilitar la evolución del producto sin comprometer innecesariamente los componentes existentes.

**Trazabilidad:** los requisitos, las decisiones de diseño, las implementaciones y las pruebas deben poder relacionarse entre sí.

**Verificabilidad:** cada capacidad implementada debe contar con criterios objetivos de aceptación.

**Mantenibilidad:** el producto debe facilitar diagnóstico, soporte técnico, actualización y sustitución de componentes.

**Calidad profesional:** el objetivo es desarrollar una solución que makeAutomatic pueda ofrecer y respaldar comercialmente.

## 5. Metodología de diseño

La ingeniería del producto se desarrollará mediante rondas estructuradas de decisiones técnicas.

Para cada decisión relevante se procurará presentar tres alternativas, identificadas como **A, B y C**, con sus ventajas, desventajas, riesgos y consecuencias.

El responsable del proyecto seleccionará la alternativa que considere más apropiada, independientemente de la recomendación técnica presentada.

No se establecerá un límite artificial de preguntas por módulo. La profundidad del análisis dependerá de la complejidad, los riesgos y las incertidumbres de cada componente.

El cierre de un bloque de ingeniería dependerá de su madurez técnica y de la existencia de criterios suficientes para implementar y verificar el diseño.

Las decisiones aprobadas se registrarán en la documentación del repositorio.

La metodología completa se encuentra en:

`docs/00-gobierno/metodologia-diseno.md`

## 6. Organización del repositorio

El repositorio separa las reglas de gobierno, las especificaciones técnicas, las decisiones arquitectónicas y las instrucciones de implementación.

| Ubicación | Propósito |
|---|---|
| `AGENTS.md` | Instrucciones para agentes de programación e ingeniería |
| `docs/00-gobierno/` | Visión, principios, metodología y criterios de calidad |
| `docs/01-requisitos/` | Requisitos funcionales, no funcionales y restricciones |
| `docs/02-arquitectura/` | Arquitectura de hardware, firmware, software e interfaces |
| `docs/03-seguridad-industrial/` | Análisis de riesgos y requisitos de seguridad |
| `docs/04-modulos/` | Especificaciones de módulos individuales |
| `docs/05-validacion/` | Estrategia de pruebas, aceptación y resultados |
| `docs/06-decisiones/` | Registro de decisiones y asuntos pendientes |
| `docs/07-roadmap/` | Fases y planificación de implementación |
| `docs/08-prompts/` | Contratos e instrucciones de trabajo para agentes |

Los documentos inicialmente vacíos se completarán progresivamente a medida que avance la ingeniería.

## 7. Uso de agentes de inteligencia artificial

Los agentes de IA podrán apoyar las actividades de investigación, evaluación técnica, documentación, implementación, revisión y pruebas.

Estas reglas se aplican a cualquier agente de inteligencia artificial, independientemente de su proveedor, modelo o herramienta.

Su participación estará sujeta a las siguientes condiciones:

- Consultar la documentación vigente antes de proponer modificaciones.
- No asumir como aprobadas decisiones que continúen pendientes.
- Respetar los requisitos y las decisiones arquitectónicas registradas.
- No introducir tecnologías, dependencias o funcionalidades fuera del alcance autorizado.
- Identificar incertidumbres, limitaciones y riesgos.
- Trabajar mediante tareas delimitadas y verificables.
- No confundir resultados de simulación o laboratorio con validación industrial.

Las instrucciones operativas para agentes se definirán en `AGENTS.md`.

## 8. Continuidad del proyecto

El repositorio constituye la fuente documental de referencia para continuar el trabajo entre distintas sesiones de ingeniería.

El archivo:

`docs/00-gobierno/ESTADO-ACTUAL.md`

registrará el bloque activo, las decisiones aprobadas, los asuntos pendientes, el grado de madurez del diseño y el siguiente paso.

Al comenzar una nueva conversación de ingeniería, se deberá consultar el repositorio actualizado mediante el mecanismo de acceso disponible en el entorno del agente (conector de repositorio, control de versiones local u otro medio autorizado), revisar el estado vigente y recuperar los documentos relevantes antes de continuar.

Si el mecanismo de acceso no está disponible, deberá informarse la limitación y no deberá inventarse información para completar los vacíos.

Las decisiones no documentadas no deberán considerarse automáticamente aprobadas.

## 9. Estado actual

**Fase:** Preparación documental e institucionalización de la metodología de ingeniería.

En esta etapa:

- Se está estableciendo la documentación base del producto.
- Se están definiendo las reglas de trabajo y los criterios de calidad.
- No se ha aprobado todavía una arquitectura definitiva.
- No se ha autorizado la implementación del producto.
- Las especificaciones técnicas se desarrollarán mediante rondas de decisiones documentadas.

El estado actualizado debe consultarse en `docs/00-gobierno/ESTADO-ACTUAL.md`.

## 10. Responsabilidad del producto

ControlCore es un proyecto de **makeAutomatic**.

Las decisiones de arquitectura, el alcance del producto y la aprobación de sus fases de desarrollo corresponden al responsable del proyecto.

La incorporación de especialistas, integradores o agentes de desarrollo no sustituye los procesos de revisión, verificación y aceptación técnica.

La aptitud del producto para una aplicación industrial específica deberá establecerse mediante la evaluación de riesgos, el cumplimiento de los requisitos aplicables y las validaciones correspondientes.

---

**ControlCore — makeAutomatic**  
*Ingeniería, automatización y desarrollo de soluciones industriales.*