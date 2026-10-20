# ControlCore — Visión del producto

**Proyecto:** ControlCore  
**Empresa:** makeAutomatic  
**Documento:** Visión del producto  
**Versión:** 0.1  
**Estado:** Propuesta para aprobación  
**Fase:** Ingeniería conceptual  
**Fecha de revisión:** 2026-10-19  
**Aprobación:** Pendiente — responsable del proyecto

---

## 1. Propósito

ControlCore es una iniciativa de makeAutomatic para desarrollar una plataforma modular de control, supervisión y diagnóstico de motores y actuadores destinados a aplicaciones industriales.

El producto deberá permitir construir soluciones de automatización adaptables a diferentes máquinas, estaciones de trabajo y procesos productivos.

Su desarrollo estará orientado a la comercialización profesional, considerando desde las primeras etapas los requisitos de ingeniería necesarios para su futura instalación, operación y mantenimiento en entornos industriales.

## 2. Problema que busca resolver

En los procesos industriales existen necesidades de control de movimiento y actuación que pueden requerir soluciones específicas, integración con sistemas existentes, supervisión operativa y capacidades de diagnóstico.

Estas necesidades pueden presentarse en:

- Máquinas de producción.
- Estaciones de ensamblaje.
- Equipos auxiliares de automatización.
- Bancos industriales de prueba.
- Sistemas de posicionamiento.
- Mecanismos de accionamiento y transporte.

ControlCore buscará ofrecer una base tecnológica modular para desarrollar e integrar soluciones de control ajustadas a los requisitos de cada aplicación.

Las necesidades concretas del mercado, los segmentos prioritarios y las ventajas competitivas deberán validarse durante el desarrollo comercial del producto.

## 3. Visión

Desarrollar una plataforma de automatización industrial de makeAutomatic que combine capacidades de control, supervisión y diagnóstico, con una arquitectura modular y extensible, apta para evolucionar hacia productos y soluciones comerciales confiables.

ControlCore deberá ser una plataforma cuya ingeniería pueda comprenderse, mantenerse, verificarse y ampliarse sin depender de modificaciones improvisadas o implementaciones difíciles de reproducir.

## 4. Objetivo general

Diseñar, implementar y validar progresivamente una plataforma modular de control industrial que permita integrar motores y actuadores con capacidades de operación, supervisión, configuración y diagnóstico, bajo requisitos definidos de seguridad, confiabilidad y mantenibilidad.

## 5. Objetivos específicos

1. Establecer una arquitectura modular que permita desarrollar capacidades de control de manera incremental.
2. Definir interfaces claras entre los componentes de hardware, firmware y software.
3. Incorporar mecanismos apropiados de supervisión y diagnóstico.
4. Establecer comportamientos definidos ante fallas y condiciones anormales.
5. Diseñar procedimientos de configuración, operación y mantenimiento.
6. Mantener trazabilidad entre requisitos, decisiones, implementaciones y pruebas.
7. Desarrollar una estrategia de validación que distinga entre laboratorio y operación industrial.
8. Facilitar la evolución del producto hacia nuevas aplicaciones y capacidades.
9. Producir documentación técnica suficiente para respaldar la implementación y el soporte profesional.
10. Preparar una base tecnológica que makeAutomatic pueda ofrecer comercialmente dentro de un alcance de aplicación claramente definido.

## 6. Usuarios y actores previstos

Los posibles actores relacionados con ControlCore incluyen:

**Integradores de automatización:** responsables de incorporar el producto en máquinas o sistemas industriales.

**Ingenieros y técnicos:** responsables de configuración, diagnóstico, pruebas y mantenimiento.

**Operadores de planta:** usuarios de las funciones operativas que se definan para cada aplicación.

**Responsables de producción y mantenimiento:** interesados en disponibilidad, comportamiento operativo y diagnóstico de equipos.

**Equipo de desarrollo de makeAutomatic y aliados especializados:** responsables de diseño, implementación, validación y evolución del producto.

Los perfiles, permisos y funciones concretas de cada actor deberán definirse en los requisitos del sistema.

## 7. Alcance conceptual

ControlCore contempla, como áreas potenciales de desarrollo:

- Control de motores y actuadores.
- Adquisición de señales de realimentación.
- Ejecución de estrategias de control.
- Configuración de parámetros operativos.
- Supervisión del estado del sistema.
- Diagnóstico de fallas.
- Comunicación con sistemas externos.
- Interfaces de operación y mantenimiento.
- Registro de eventos y datos relevantes.

Esta enumeración representa el alcance conceptual de la plataforma, no una lista de funcionalidades aprobadas para la primera versión.

Cada capacidad deberá incorporarse al alcance mediante decisiones de ingeniería y requisitos documentados.

## 8. Estrategia de evolución

El producto se desarrollará de manera incremental.

Se buscará establecer una arquitectura que permita validar primero un conjunto acotado de capacidades y ampliar posteriormente su funcionalidad.

Las etapas previstas a nivel conceptual son:

### Etapa 1 — Ingeniería del producto

Definición de requisitos, restricciones, arquitectura, interfaces, riesgos y criterios de validación.

### Etapa 2 — Validación de concepto

Construcción de prototipos y experimentos para comprobar decisiones técnicas fundamentales.

### Etapa 3 — Desarrollo e integración

Implementación de los componentes definidos y verificación de su funcionamiento conjunto.

### Etapa 4 — Ingeniería para aplicación industrial

Evaluación y tratamiento de los requisitos eléctricos, mecánicos, ambientales, operativos y de seguridad correspondientes al uso previsto.

### Etapa 5 — Preparación comercial

Consolidación de documentación, procedimientos de instalación, mantenimiento, soporte y evidencias de aceptación para las aplicaciones autorizadas.

Estas etapas no representan todavía un cronograma aprobado ni garantizan la aptitud comercial del producto.

## 9. Principios de calidad del producto

ControlCore deberá desarrollarse considerando los siguientes atributos:

**Seguridad:** tratamiento sistemático de peligros y riesgos asociados al movimiento y la actuación.

**Confiabilidad:** comportamiento controlado y predecible durante operación normal y ante fallas.

**Robustez:** resistencia adecuada a las condiciones eléctricas y ambientales de la aplicación prevista.

**Modularidad:** separación clara de responsabilidades y posibilidad de evolución controlada.

**Mantenibilidad:** facilidad de diagnóstico, reparación, sustitución y actualización.

**Interoperabilidad:** interfaces documentadas para integración con otros sistemas.

**Verificabilidad:** criterios de aceptación medibles y pruebas reproducibles.

**Trazabilidad:** relación documentada entre necesidades, requisitos, decisiones y resultados.

**Calidad del software:** aplicación de principios de diseño, reutilización y prevención de duplicación innecesaria.

## 10. Modelo de desarrollo

makeAutomatic dirigirá la concepción del producto, las decisiones arquitectónicas y la definición de los requisitos de aceptación.

El proyecto podrá incorporar especialistas y aliados técnicos para actividades específicas de ingeniería, implementación, fabricación, pruebas o integración.

La participación de terceros deberá desarrollarse sobre especificaciones y responsabilidades claramente definidas.

Los agentes de inteligencia artificial podrán asistir en el análisis, la documentación y la implementación, pero no sustituirán la aprobación técnica ni las validaciones correspondientes.

## 11. Límites y exclusiones actuales

Durante la fase de ingeniería conceptual:

- No existe una selección definitiva de plataforma electrónica.
- No se ha aprobado una arquitectura de control.
- No se han definido todos los tipos de motores o actuadores que soportará el producto.
- No se han aprobado protocolos de comunicación específicos.
- No se ha definido una arquitectura definitiva de backend o frontend.
- No se han establecido prestaciones cuantitativas de control.
- No se ha determinado la clasificación de seguridad requerida para una aplicación concreta.
- No se ha aprobado un alcance comercial definitivo ni un precio de venta.

Estas definiciones se resolverán progresivamente mediante el proceso de ingeniería.

## 12. Criterios de éxito

El éxito del proyecto no se limitará a demostrar movimiento de un motor o funcionamiento de una interfaz.

ControlCore deberá alcanzar, para cada versión y aplicación prevista:

1. Cumplimiento verificable de requisitos aprobados.
2. Comportamiento de control dentro de prestaciones especificadas.
3. Gestión adecuada de fallas y condiciones anormales.
4. Arquitectura documentada y mantenible.
5. Calidad de implementación y pruebas reproducibles.
6. Integración demostrada entre componentes.
7. Riesgos identificados y tratados conforme al uso previsto.
8. Documentación apropiada para instalación, operación y soporte.
9. Evidencia suficiente para sustentar las declaraciones técnicas y comerciales del producto.

La liberación para uso industrial requerirá una evaluación específica de cumplimiento y aceptación.

## 13. Relación con otros documentos

Esta visión establece la orientación general del producto.

Las definiciones detalladas se encontrarán en:

- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/criterios-calidad.md`
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/01-requisitos/`
- `docs/02-arquitectura/`
- `docs/03-seguridad-industrial/`
- `docs/04-modulos/`
- `docs/05-validacion/`
- `docs/06-decisiones/`

La visión no sustituye los requisitos técnicos ni constituye por sí sola una especificación implementable.

---

**ControlCore — makeAutomatic**  
*Visión de producto industrial — v0.1*