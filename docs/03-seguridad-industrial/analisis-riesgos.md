# Análisis preliminar de riesgos — ControlCore

**Proyecto:** ControlCore
**Empresa:** makeAutomatic
**Tipo de proyecto:** Desarrollo de producto industrial comercial
**Documento:** Análisis preliminar de riesgos
**Versión:** 0.1
**Estado:** Propuesta para aprobación
**Fase:** Ingeniería de requisitos y seguridad industrial
**Fecha de revisión:** 2026-10-20
**Aprobación:** Pendiente — no constituye aceptación de riesgos ni autorización de pruebas

---

## 1. Propósito

Este documento prepara la estructura del análisis preliminar de riesgos del primer incremento de ControlCore y vincula los peligros identificados con funciones de protección y requisitos candidatos.

Su finalidad es orientar la especificación de requisitos de seguridad y la verificación futura. No sustituye un análisis de riesgos completo, no declara conformidad con normas y no autoriza pruebas físicas.

## 2. Alcance y límites

El alcance provisional es el sistema completo del banco de pruebas del primer incremento:

- Motor DC con escobillas.
- Etapa de potencia.
- Alimentación eléctrica.
- Carga mecánica.
- Sensores de velocidad y otras variables.
- Controlador y lógica de control.
- Interfaces locales o de computador utilizadas.
- Operador.
- Entorno del banco.

El análisis considera operación normal, arranque, parada, inversión, mantenimiento, fallas previsibles, errores del operador y recuperación tras interrupciones.

No se asignan valores de gravedad, probabilidad, riesgo inicial o riesgo residual. No se declara que un riesgo sea aceptable. No se seleccionan componentes, protecciones eléctricas concretas ni arquitectura de seguridad.

## 3. Método

El análisis se estructura en cinco etapas:

1. Identificación de peligros por escenario de operación.
2. Análisis de causas, efectos y medidas existentes o propuestas.
3. FMEA de funciones críticas.
4. Evaluación cualitativa y cuantitativa del riesgo, pendiente de escala aprobada.
5. Definición de funciones de protección, requisitos derivados y verificación.

Los identificadores `HZ-###`, `FMEA-###` y `PF-###` son locales de este documento. No son requisitos ni decisiones formales.

## 4. Sistema bajo análisis

| Elemento | Función | Límite considerado | Observación |
|---|---|---|---|
| Motor DC con escobillas | Convertir energía eléctrica en movimiento | Primer incremento | Modelo y parámetros pendientes |
| Etapa de potencia | Entregar energía al motor | Banco de pruebas | Topología y componentes no seleccionados |
| Alimentación | Suministrar energía eléctrica | Banco de pruebas | Tensiones y protecciones pendientes |
| Carga mecánica | Representar la aplicación | Banco de pruebas | Naturaleza y rango pendientes |
| Sensores | Medir velocidad y variables de supervisión | Banco de pruebas | Tipos y rangos pendientes |
| Controlador | Ejecutar control, supervisión y protecciones | Banco de pruebas | Plataforma no seleccionada |
| Operador | Comandar, configurar y detener | Entorno de laboratorio | Formación y permisos pendientes |
| Entorno | Condiciones físicas y eléctricas | Laboratorio | Condiciones ambientales y EMC pendientes |

## 5. Identificación de peligros

| ID | Escenario u operación | Peligro | Causa posible | Efecto posible | Medidas existentes o propuestas | Función de protección | Requisito candidato | Riesgo inicial/residual |
|---|---|---|---|---|---|---|---|---|
| HZ-001 | Habilitación y arranque | Arranque inesperado | Comando inválido, configuración incorrecta, protección no comprobada | Movimiento no deseado | Habilitación condicionada, validación de comandos, configuración verificada | PF-001 | RF-001; RF-002 | Pendiente de evaluación |
| HZ-002 | Energización del banco | Movimiento con protecciones no verificadas | Prueba sin análisis, protección ausente o no comprobada | Exposición mecánica o eléctrica | Compuerta de pruebas y autorización explícita | PF-014 | RES-003; RES-004 | Pendiente de evaluación |
| HZ-003 | Parada normal o de protección | Parada no efectiva | Comando perdido, falla de potencia, inercia, carga | Movimiento continuo | Tipos de parada, verificación de parada real | PF-002 | RF-003; RF-004 | Pendiente de evaluación |
| HZ-004 | Regulación de velocidad | Sobrevelocidad o pérdida de control | Realimentación inválida, PI inestable, referencia incorrecta | Movimiento fuera de límites | Validación de referencia, supervisión de lazo, límites PI | PF-003; PF-004 | RF-007–RF-012 | Pendiente de evaluación |
| HZ-005 | Aceleración | Aceleración inesperada | Rampa excesiva, comando erróneo, falla de control | Esfuerzo mecánico, pérdida de control | Rampa configurable, supervisión de aceleración | PF-003 | RF-006; RF-018 | Pendiente de evaluación |
| HZ-006 | Inversión de giro | Inversión inesperada | Comando erróneo, falla de control o potencia | Movimiento contrario al esperado | Validación de referencia, supervisión de dirección | PF-003 | RF-018 | Pendiente de evaluación |
| HZ-007 | Operación con carga | Bloqueo mecánico y sobrecorriente | Carga atascada, falla mecánica, sobrecarga | Sobrecalentamiento, daño mecánico o eléctrico | Detección de bloqueo y sobrecorriente | PF-007; PF-009 | RF-015; RF-017 | Pendiente de evaluación |
| HZ-008 | Operación con carga variable | Pérdida de carga y sobrevelocidad | Acoplamiento roto, carga liberada | Sobrevelocidad, daño mecánico | Detección de pérdida de carga y sobrevelocidad | PF-003; PF-009 | RF-007; RF-017 | Pendiente de evaluación |
| HZ-009 | Alimentación y potencia | Sobrecorriente por falla eléctrica | Cortocircuito, falla de aislamiento, componente defectuoso | Daño térmico, incendio, descarga | Protección de sobrecorriente y protecciones independientes si proceden | PF-007 | RF-015 | Pendiente de evaluación |
| HZ-010 | Frenado y desaceleración | Sobretensión regenerativa | Energía devuelta por el motor | Daño de etapa de potencia o alimentación | Detección de sobretensión y respuesta | PF-007 | RF-015 | Pendiente de evaluación |
| HZ-011 | Alimentación | Subtensión o pérdida de alimentación | Corte, caída de tensión, falla de fuente | Pérdida de control, reinicio inesperado | Detección y recuperación supervisada | PF-011 | RF-021 | Pendiente de evaluación |
| HZ-012 | Operación prolongada | Sobrecalentamiento | Sobrecarga, ventilación insuficiente, falla térmica | Daño del motor o electrónica | Supervisión térmica y límites | PF-008 | RF-016 | Pendiente de evaluación |
| HZ-013 | Medición de velocidad | Realimentación inválida o pérdida de sensor | Desconexión, ruido, rango, dato obsoleto | Lazo inestable, sobrevelocidad | Validación de medición y detección de pérdida | PF-004; PF-005 | RF-011–RF-013 | Pendiente de evaluación |
| HZ-014 | Comunicaciones | Pérdida, mensaje inválido o dato obsoleto | Corte de enlace, timeout, corrupción | Comando perdido o supervisión incompleta | Supervisión de comunicaciones y respuesta diferenciada | PF-006 | RF-014 | Pendiente de evaluación |
| HZ-015 | Etapa de potencia | Falla de conmutación, cortocircuito o circuito abierto | Componente defectuoso, comando incorrecto, sobrecarga | Movimiento no controlado, daño eléctrico | Supervisión de coherencia y detección de fallas | PF-010 | RF-019 | Pendiente de evaluación |
| HZ-016 | Controlador | Falla de ejecución, memoria, temporización o recursos | Defecto, sobrecarga, condición anómala | Pérdida de control o de protecciones | Watchdog, detección de fallas internas | PF-010 | RF-020; RNF-005 | Pendiente de evaluación |
| HZ-017 | Configuración | Configuración inválida o cambio no autorizado | Error humano, corrupción, acceso indebido | Comportamiento incorrecto o inseguro | Validación, integridad, recuperación, auditoría | PF-012; PF-013 | RF-023–RF-026 | Pendiente de evaluación |
| HZ-018 | Reinicio o restablecimiento | Reinicio con falla presente | Falla no eliminada, condición insegura | Reanudación peligrosa | Restablecimiento condicionado y verificación | PF-002; PF-011 | RF-022 | Pendiente de evaluación |
| HZ-019 | Instalación eléctrica | Contacto eléctrico o falla de aislamiento | Puesta a tierra deficiente, aislamiento dañado | Descarga eléctrica | Diseño eléctrico, protecciones y verificación | PF-007 | RF-015; RES-003 | Pendiente de evaluación |
| HZ-020 | Banco de pruebas | Atrapamiento o exposición mecánica | Carga móvil, acoplamiento, falta de resguardo | Lesión mecánica | Diseño del banco, resguardos y procedimiento | PF-002 | RF-001; RF-003; RES-003 | Pendiente de evaluación |
| HZ-021 | Operación | Error del operador o comando contradictorio | Comando inválido, prisa, falta de confirmación | Movimiento no deseado | Validación de comandos, permisos y registro | PF-001 | RF-002 | Pendiente de evaluación |
| HZ-022 | Mantenimiento | Intervención con energía o movimiento presente | Falta de bloqueo, procedimiento incompleto | Descarga, movimiento inesperado | Procedimiento de bloqueo y autorización | PF-014 | RES-003; RF-022 | Pendiente de evaluación |
| HZ-023 | Configuración en operación | Cambio de parámetros durante movimiento | Permisos insuficientes, aplicación inmediata | Cambio de comportamiento no controlado | Clasificación de parámetros y condiciones de cambio | PF-012 | RF-025; RNF-004 | Pendiente de evaluación |

## 6. FMEA de funciones críticas

La FMEA es preliminar. No se asignan índices de severidad, ocurrencia o detectabilidad. Esos valores requieren una escala aprobada y evidencia de diseño.

| ID | Función | Modo de falla | Causa posible | Efecto local | Efecto en el sistema | Detección propuesta | Medida o requisito |
|---|---|---|---|---|---|---|---|
| FMEA-001 | Habilitación | Habilita sin condiciones | Comando, configuración o protección ausente | Movimiento no autorizado | Arranque inesperado | Verificación de condiciones | RF-001 |
| FMEA-002 | Validación de comandos | Acepta comando inválido | Validación incompleta u origen no autorizado | Comando incorrecto | Movimiento no deseado | Validación y registro | RF-002 |
| FMEA-003 | Parada | Comando no ejecutado o no verificado | Falla de potencia, pérdida de comando, inercia | Movimiento continuo | Exposición mecánica | Verificación de parada real | RF-003; RF-004 |
| FMEA-004 | Rampa | Perfil no aplicado o excesivo | Configuración inválida, falla de control | Aceleración o desaceleración excesiva | Esfuerzo mecánico o eléctrico | Supervisión de perfil | RF-005; RF-006 |
| FMEA-005 | Lazo cerrado | Inestabilidad o pérdida de realimentación | Ganancias, sensor, saturación | Sobrevelocidad u oscilación | Pérdida de control | Supervisión de lazo y realimentación | RF-008–RF-012 |
| FMEA-006 | Medición de velocidad | Dato obsoleto o incoherente | Sensor, filtro, comunicación | Referencia incorrecta | Lazo inestable | Validación de frescura y coherencia | RF-011–RF-014 |
| FMEA-007 | Protección de sobrecorriente | No detecta o no actúa | Umbral, sensor, lógica o potencia | Sobrecalentamiento | Daño eléctrico o incendio | Detección y prueba | RF-015 |
| FMEA-008 | Protección térmica | No detecta sobretemperatura | Sensor, modelo, tiempo | Daño del motor o electrónica | Falla térmica | Supervisión térmica | RF-016 |
| FMEA-009 | Etapa de potencia | Cortocircuito, circuito abierto o conmutación incorrecta | Componente, comando, aislamiento | Movimiento anómalo | Daño eléctrico o pérdida de control | Coherencia y diagnóstico | RF-019 |
| FMEA-010 | Controlador | Falla de ejecución, memoria o temporización | Defecto, sobrecarga, recurso | Pérdida de lógica | Pérdida de protecciones | Watchdog y autodiagnóstico | RF-020; RNF-005 |
| FMEA-011 | Configuración | Corrupción o cambio no autorizado | Almacenamiento, acceso, error humano | Parámetros incorrectos | Comportamiento inseguro | Integridad, validación y auditoría | RF-023–RF-026 |
| FMEA-012 | Alimentación | Pérdida o recuperación no supervisada | Corte, fuente, protección | Reinicio inesperado | Movimiento no deseado | Detección y recuperación | RF-021; RF-022 |

## 7. Evaluación de riesgos

No se asigna una escala numérica ni cualitativa definitiva. La evaluación requiere aprobar previamente:

- Definiciones de gravedad, probabilidad y posibilidad de evitar o limitar el daño.
- Criterios de aceptación y tolerabilidad.
- Método de estimación del riesgo inicial y residual.
- Evidencia requerida para demostrar la eficacia de las medidas.

Mientras esos criterios no estén aprobados, cada peligro se registra como **Pendiente de evaluación**. No se declara riesgo aceptable.

## 8. Jerarquía de reducción del riesgo

| Nivel | Aplicación | Estado |
|---|---|---|
| Diseño inherentemente seguro | Eliminar o reducir el peligro mediante el diseño del banco y del sistema | Pendiente de análisis y decisiones de diseño |
| Medidas técnicas de protección | Funciones de protección, enclavamientos, limitación de energía o movimiento | Pendiente de especificación y verificación |
| Información sobre riesgos residuales | Señalización, procedimientos, formación y advertencias | Pendiente de documentación |

La jerarquía se aplicará antes de considerar la información o la formación como medida suficiente. No se seleccionan aún medidas técnicas concretas.

## 9. Funciones de protección derivadas

| ID | Función de protección | Peligros mitigados | Comportamiento requerido | Requisito candidato | Verificación |
|---|---|---|---|---|---|
| PF-001 | Habilitación supervisada | HZ-001; HZ-002; HZ-020; HZ-021 | Habilitar solo con condiciones válidas y protecciones comprobadas | RF-001; RF-002 | Inspección y prueba |
| PF-002 | Parada de protección y verificación | HZ-003; HZ-018; HZ-020 | Ejecutar la parada y verificar su efecto real | RF-003; RF-004; RF-022 | Análisis y prueba |
| PF-003 | Limitación de referencia, rampas y velocidad | HZ-004; HZ-005; HZ-006; HZ-008 | Limitar referencias, aceleración, desaceleración y velocidad | RF-005–RF-007; RF-018 | Análisis y prueba |
| PF-004 | Supervisión del lazo y realimentación | HZ-004; HZ-013 | Detectar pérdida o invalidez de realimentación y responder | RF-008–RF-012 | Análisis y prueba |
| PF-005 | Supervisión de sensores | HZ-013 | Detectar desconexión, rango, incoherencia y datos obsoletos | RF-011; RF-013 | Análisis y prueba |
| PF-006 | Supervisión de comunicaciones | HZ-014 | Detectar pérdida, timeout, mensaje inválido o dato obsoleto | RF-014 | Análisis y prueba |
| PF-007 | Protección eléctrica | HZ-007; HZ-009; HZ-010; HZ-019 | Detectar sobrecorriente, sobretensión o subtensión y actuar | RF-015 | Análisis y prueba |
| PF-008 | Protección térmica | HZ-012 | Detectar sobretemperatura y responder según riesgo | RF-016 | Análisis y prueba |
| PF-009 | Protección mecánica | HZ-007; HZ-008 | Detectar bloqueo o pérdida de carga y responder | RF-017 | Análisis y prueba |
| PF-010 | Supervisión de potencia y control | HZ-015; HZ-016 | Detectar pérdida de control o falla de potencia | RF-019; RF-020 | Análisis y prueba |
| PF-011 | Recuperación de alimentación | HZ-011; HZ-018 | Impedir movimiento hasta verificar condiciones tras recuperación | RF-021; RF-022 | Análisis y prueba |
| PF-012 | Configuración segura | HZ-017; HZ-023 | Validar, recuperar y condicionar cambios de configuración | RF-023–RF-025 | Inspección y prueba |
| PF-013 | Registro y auditoría | HZ-017 | Registrar eventos y cambios con trazabilidad | RF-026; RF-027 | Inspección y prueba |
| PF-014 | Compuerta de pruebas | HZ-002; HZ-019; HZ-022 | Impedir energización sin documentación y autorización | RES-003; RES-004 | Inspección documental |

Las funciones de protección son candidatas. No son funciones de seguridad certificadas ni sustituyen las protecciones de la máquina o del banco.

## 10. Verificación de protecciones y autorización de pruebas

Antes de energizar el banco o ejecutar pruebas físicas deberá existir:

1. Análisis de peligros actualizado y revisado.
2. FMEA de las funciones críticas.
3. Identificación de riesgos iniciales y residuales.
4. Funciones de protección y requisitos derivados identificados.
5. Verificación por análisis y simulación de las protecciones que lo permitan.
6. Documentación del banco, alimentación, carga, sensores y límites.
7. Procedimiento de prueba con condiciones iniciales, pasos, criterios de interrupción y medidas de emergencia.
8. Riesgos residuales documentados.
9. Autorización explícita del responsable del proyecto.

Ninguna de estas condiciones autoriza por sí sola una prueba física. La autorización es un acto separado y explícito.

## 11. Criterios de aceptación y verificación pendientes

Cada protección requerirá:

- Disparador o condición de activación.
- Comportamiento esperado.
- Tiempo de respuesta, cuando corresponda.
- Condición de restablecimiento.
- Criterio de aceptación.
- Método de verificación.
- Evidencia requerida.
- Riesgo residual después de la medida.

Los valores y tiempos no están definidos. No se declaran verificables las protecciones que dependan de ellos.

## 12. Riesgos residuales

No se ha determinado ningún riesgo residual. Su evaluación requiere:

- Medidas de reducción definidas.
- Eficacia verificada.
- Riesgos restantes identificados.
- Criterios de aceptación aprobados.

La ausencia de un riesgo residual declarado no significa que el riesgo sea aceptable.

## 13. Requisitos derivados y trazabilidad

| Peligro | Función de protección | Requisito candidato | Verificación |
|---|---|---|---|
| HZ-001 | PF-001 | RF-001; RF-002 | Prueba de habilitación y comandos |
| HZ-002 | PF-014 | RES-003; RES-004 | Inspección documental |
| HZ-003 | PF-002 | RF-003; RF-004 | Prueba de parada y verificación |
| HZ-004 | PF-003; PF-004 | RF-007–RF-012 | Análisis y prueba del lazo |
| HZ-005; HZ-006 | PF-003 | RF-018 | Prueba de aceleración e inversión |
| HZ-007; HZ-009 | PF-007; PF-009 | RF-015; RF-017 | Análisis y prueba de protección |
| HZ-008 | PF-003; PF-009 | RF-007; RF-017 | Análisis y prueba |
| HZ-010; HZ-011 | PF-007; PF-011 | RF-015; RF-021 | Análisis y prueba |
| HZ-012 | PF-008 | RF-016 | Análisis y prueba térmica |
| HZ-013 | PF-004; PF-005 | RF-011–RF-013 | Prueba de sensores y realimentación |
| HZ-014 | PF-006 | RF-014 | Prueba de comunicaciones |
| HZ-015; HZ-016 | PF-010 | RF-019; RF-020; RNF-005 | Análisis y prueba |
| HZ-017; HZ-023 | PF-012; PF-013 | RF-023–RF-026 | Inspección y prueba |
| HZ-018 | PF-002; PF-011 | RF-022 | Prueba de restablecimiento |
| HZ-019; HZ-020; HZ-022 | PF-007; PF-014 | RF-015; RES-003 | Inspección y análisis |
| HZ-021 | PF-001 | RF-002 | Prueba de comandos inválidos |

## 14. Asuntos pendientes

1. Aprobar la escala y los criterios de aceptación de riesgos.
2. Definir los estados seguros por escenario.
3. Definir límites eléctricos, térmicos y mecánicos.
4. Definir umbrales y tiempos de protección.
5. Definir la independencia y arquitectura de las protecciones.
6. Definir el banco, la carga, los sensores y la alimentación.
7. Definir el procedimiento de pruebas y los criterios de interrupción.
8. Autorizar formalmente las pruebas físicas.
9. Verificar la eficacia de las medidas y reevaluar el riesgo residual.

## 15. Referencias

- `README.md`
- `AGENTS.md`
- `docs/00-gobierno/ESTADO-ACTUAL.md`
- `docs/00-gobierno/principios-ingenieria.md`
- `docs/00-gobierno/metodologia-diseno.md`
- `docs/00-gobierno/definicion-de-terminado.md`
- `docs/01-requisitos/README.md`
- `docs/01-requisitos/requisitos-funcionales.md`
- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.4.md`
- `docs/06-decisiones/consolidacion-decisiones-B2.3.md`

## 16. Historial de cambios

- **0.1 — 2026-10-20 — B2.4:** estructura preliminar de análisis de riesgos, peligros, FMEA, funciones de protección, compuerta de pruebas y trazabilidad. Sin valores de riesgo asignados; sin autorización de pruebas.
