# Requisitos funcionales — ControlCore

**Proyecto:** ControlCore
**Empresa:** makeAutomatic
**Tipo de proyecto:** Desarrollo de producto industrial comercial
**Documento:** Requisitos funcionales
**Versión:** 0.2
**Estado:** Revisión de documento aprobado — propuesta de requisitos candidatos
**Fase:** Ingeniería de requisitos
**Fecha de revisión:** 2026-10-20
**Aprobación:** Versión 0.1 aprobada el 2026-10-19 — Responsable del proyecto ControlCore, makeAutomatic; versión 0.2 pendiente de aprobación

---

## 1. Propósito

Este documento constituye el registro de los requisitos funcionales candidatos de ControlCore para el primer incremento.

Los requisitos funcionales describen comportamientos observables que el producto deberá realizar en condiciones definidas. Los candidatos se derivan de las decisiones B2.4 `D01`–`D60` y de las decisiones conceptuales de B2.3.

## 2. Alcance

Este registro comprende exclusivamente requisitos funcionales identificados con el prefijo `RF-###`.

No comprende requisitos no funcionales ni restricciones, que se registran en:

- `docs/01-requisitos/requisitos-no-funcionales.md`
- `docs/01-requisitos/restricciones-sistema.md`

Los requisitos de este documento son **candidatos propuestos**. No constituyen una línea base, no están aprobados y no autorizan implementación.

## 3. Convenciones

Se aplican las convenciones comunes de `docs/01-requisitos/README.md` (sección 3).

- Prefijo: `RF-###`.
- El identificador es único, estable y no reutilizable.
- La versión del contenido es independiente del identificador.
- No se asigna un identificador hasta que exista un requisito funcional definido y registrado.
- Se aplican las convenciones de prioridad y trazabilidad de `docs/01-requisitos/README.md` (secciones 3 y 5).
- La versión de este documento es independiente de la versión de cada requisito individual.
- Las referencias documentales utilizan rutas relativas a la raíz del repositorio.

## 4. Atributos comunes de los candidatos

Todos los candidatos de este documento tienen:

- **Tipo:** `RF`.
- **Estado:** Propuesto.
- **Versión:** 0.1.
- **Prioridad:** Pendiente de determinar.
- **Evidencia de verificación:** Pendiente.
- **Responsable de aprobación:** Responsable del proyecto.

La verificabilidad se indica en cada ficha. Un requisito con criterio incompleto no se declara verificable ni aprobable.

## 5. Índice de requisitos candidatos

| Identificador | Título | Categoría | Origen | Verificabilidad |
|---|---|---|---|---|
| RF-001 | Habilitación condicionada del motor | Habilitación | D39; D40 | Completa cualitativa |
| RF-002 | Validación y registro de comandos | Habilitación y arranque | D41 | Completa cualitativa |
| RF-003 | Tipos de parada | Arranque y parada | D42 | Parcial — prioridades pendientes |
| RF-004 | Verificación de parada real | Arranque y parada | D43 | Parcial — umbral pendiente |
| RF-005 | Perfil de desaceleración | Rampas | D44 | Parcial — valores pendientes |
| RF-006 | Perfil de aceleración | Rampas | D45 | Parcial — valores pendientes |
| RF-007 | Referencias de velocidad | Referencias | D46 | Parcial — límites pendientes |
| RF-008 | Transición lazo abierto/cerrado | Modos de control | D47 | Parcial — límite pendiente |
| RF-009 | Regulación PI configurable | Regulación PI | D48; D54 | Parcial — criterios pendientes |
| RF-010 | Límites PI y anti-windup | Regulación PI | D49 | Completa parametrizada |
| RF-011 | Medición y validación de velocidad | Medición | D50 | Parcial — rangos pendientes |
| RF-012 | Pérdida de realimentación | Fallas | D20 | Parcial — respuesta pendiente |
| RF-013 | Fallas de sensores | Fallas | D21 | Parcial — umbrales pendientes |
| RF-014 | Fallas de comunicaciones | Fallas | D22 | Parcial — tiempos pendientes |
| RF-015 | Protecciones de sobrecorriente y tensión | Protecciones eléctricas | D23; D24 | Parcial — umbrales pendientes |
| RF-016 | Protección térmica | Protecciones térmicas | D25 | Parcial — límites pendientes |
| RF-017 | Bloqueo y pérdida de carga | Protecciones mecánicas | D26; D27 | Parcial — criterios pendientes |
| RF-018 | Aceleración e inversión inesperadas | Fallas operativas | D28; D29 | Parcial — umbrales pendientes |
| RF-019 | Pérdida de control y fallas de potencia | Supervisión de potencia | D30; D31 | Parcial — cobertura pendiente |
| RF-020 | Fallas internas del controlador | Supervisión del controlador | D32 | Parcial — cobertura pendiente |
| RF-021 | Pérdida y recuperación de alimentación | Recuperación | D19 | Parcial — condiciones pendientes |
| RF-022 | Restablecimiento y reinicio condicionados | Recuperación | D18 | Completa cualitativa |
| RF-023 | Configuración validada y persistente | Configuración | D55 | Completa cualitativa |
| RF-024 | Recuperación de configuración inválida | Configuración | D56 | Completa cualitativa |
| RF-025 | Cambio de parámetros por criticidad | Configuración | D57; D59 | Parcial — matriz pendiente |
| RF-026 | Auditoría de cambios de configuración | Auditoría | D58 | Completa cualitativa |
| RF-027 | Registro de eventos, fallas y protecciones | Auditoría y diagnóstico | D42; D43; D56 | Parcial — retención pendiente |

## 6. Requisitos candidatos

### RF-001 — Habilitación condicionada del motor

- **Descripción verificable:** El sistema no habilitará la etapa de potencia del motor salvo que concurran un comando de habilitación válido, una configuración verificada, condiciones operativas permitidas y comprobaciones de protección satisfactorias.
- **Justificación:** Evitar el arranque inesperado y la operación con protecciones no comprobadas.
- **Origen:** B2.4-D39; B2.4-D40.
- **Decisiones relacionadas:** B2.3-D25; `DEC-GOB-025`.
- **Dependencias:** RF-002; RF-015–RF-022; RF-023; RF-024; RF-026.
- **Riesgos relacionados:** HZ-001; HZ-002; HZ-020; HZ-021; FMEA-001.
- **Condiciones de aplicación:** Antes del primer movimiento, después de un reinicio, después de un cambio de configuración y después de una parada de protección.
- **Criterio de aceptación:** Con al menos una condición ausente o inválida, la etapa de potencia permanece deshabilitada y se registra el motivo. Con todas las condiciones válidas, la habilitación se permite.
- **Método de verificación:** Prueba funcional con condiciones válidas e inválidas; inspección de registros.
- **Verificabilidad:** Completa cualitativa.
- **Pendientes técnicos:** Definir las condiciones operativas permitidas y las comprobaciones de protección exigibles.

### RF-002 — Validación y registro de comandos

- **Descripción verificable:** El sistema validará los comandos de arranque y parada según estado, permisos, condiciones de seguridad y origen; aceptará o rechazará cada comando y registrará el resultado.
- **Justificación:** Evitar la ejecución de comandos inválidos, contradictorios o no autorizados.
- **Origen:** B2.4-D41.
- **Decisiones relacionadas:** `DEC-GOB-025`.
- **Dependencias:** RF-001.
- **Riesgos relacionados:** HZ-001; HZ-021; FMEA-002.
- **Condiciones de aplicación:** Todo comando recibido por la interfaz local o de computador utilizada por el primer incremento.
- **Criterio de aceptación:** Todo comando inválido o no autorizado es rechazado y registrado con su causa. Todo comando válido es aceptado y registrado.
- **Método de verificación:** Prueba con comandos válidos, inválidos, contradictorios y no autorizados; inspección de registros.
- **Verificabilidad:** Completa cualitativa.
- **Pendientes técnicos:** Definir reglas de permisos, origen y prioridad de comandos.

### RF-003 — Tipos de parada

- **Descripción verificable:** El sistema distinguirá parada normal, parada controlada y parada de protección, con condiciones de activación y prioridades derivadas del análisis de riesgos.
- **Justificación:** Evitar que una parada normal prevalezca sobre una parada requerida por protección.
- **Origen:** B2.4-D42.
- **Decisiones relacionadas:** B2.3-D07; B2.3-D25; `DEC-GOB-024`.
- **Dependencias:** RF-004; RF-015–RF-022.
- **Riesgos relacionados:** HZ-003; HZ-004; FMEA-003.
- **Condiciones de aplicación:** Operación normal, falla detectada, pérdida de alimentación y solicitud de parada.
- **Criterio de aceptación:** Cada tipo de parada es observable y distinguible. La parada de protección prevalece sobre la parada normal conforme a la prioridad aprobada.
- **Método de verificación:** Prueba funcional e inspección de la matriz de prioridades.
- **Verificabilidad:** Parcial — falta la matriz de prioridades.
- **Pendientes técnicos:** Definir prioridades, condiciones de activación y comportamiento de cada tipo de parada.

### RF-004 — Verificación de parada real

- **Descripción verificable:** El sistema considerará completada una parada solo cuando la velocidad medida y el estado de la etapa de potencia cumplan las condiciones aprobadas; la emisión del comando no será suficiente.
- **Justificación:** Detectar paradas no efectivas y evitar reanudaciones sobre un motor aún en movimiento.
- **Origen:** B2.4-D43.
- **Decisiones relacionadas:** B2.3-D25; `DEC-GOB-024`.
- **Dependencias:** RF-003; RF-011.
- **Riesgos relacionados:** HZ-003; FMEA-003.
- **Condiciones de aplicación:** Después de toda parada normal, controlada o de protección.
- **Criterio de aceptación:** La parada se declara completada solo cuando la velocidad medida está por debajo del umbral aprobado y el estado de potencia confirma la ausencia de energía motriz. El umbral y el tiempo máximo son pendientes.
- **Método de verificación:** Prueba con inercia y carga representativas; comparación entre comando, velocidad y estado de potencia.
- **Verificabilidad:** Parcial — faltan umbral y tiempo.
- **Pendientes técnicos:** Definir umbral de velocidad, tiempo máximo de parada y señales de confirmación.

### RF-005 — Perfil de desaceleración

- **Descripción verificable:** El sistema aplicará un perfil de desaceleración configurable según el tipo de parada, el motor y la carga, respetando los límites eléctricos, mecánicos y de seguridad aprobados.
- **Justificación:** Evitar desaceleraciones excesivas, sobretensión regenerativa y esfuerzos mecánicos.
- **Origen:** B2.4-D44.
- **Decisiones relacionadas:** B2.3-D31; `DEC-GOB-023`.
- **Dependencias:** RF-003; RF-006.
- **Riesgos relacionados:** HZ-003; HZ-005; HZ-010.
- **Condiciones de aplicación:** Parada normal, controlada y de protección, según corresponda.
- **Criterio de aceptación:** El perfil configurado se aplica y la desaceleración medida permanece dentro de la tolerancia aprobada, sin superar los límites eléctricos y mecánicos. Valores y tolerancias pendientes.
- **Método de verificación:** Prueba con carga representativa y registro de velocidad, corriente y tensión.
- **Verificabilidad:** Parcial — faltan valores y tolerancias.
- **Pendientes técnicos:** Definir perfiles, rangos, tolerancias y límites regenerativos.

### RF-006 — Perfil de aceleración

- **Descripción verificable:** El sistema aplicará un perfil de aceleración configurable, respetando los límites de corriente, velocidad, esfuerzo mecánico y carga aprobados.
- **Justificación:** Evitar sobrecorriente, esfuerzos mecánicos y pérdida de control durante el arranque.
- **Origen:** B2.4-D45.
- **Decisiones relacionadas:** B2.3-D31; `DEC-GOB-023`.
- **Dependencias:** RF-001; RF-007.
- **Riesgos relacionados:** HZ-005; HZ-007.
- **Condiciones de aplicación:** Arranque y cambios de referencia de velocidad.
- **Criterio de aceptación:** El perfil configurado se aplica y la aceleración medida permanece dentro de la tolerancia aprobada, sin superar los límites de corriente y velocidad. Valores pendientes.
- **Método de verificación:** Prueba con carga representativa y registro de velocidad y corriente.
- **Verificabilidad:** Parcial — faltan valores y tolerancias.
- **Pendientes técnicos:** Definir perfiles, rangos y límites.

### RF-007 — Referencias de velocidad

- **Descripción verificable:** El sistema validará las referencias de velocidad contra límites, permisos, estado operativo y restricciones dinámicas; rechazará referencias fuera de rango y aplicará transiciones controladas.
- **Justificación:** Evitar sobrevelocidad, inversiones no deseadas y cambios bruscos.
- **Origen:** B2.4-D46.
- **Decisiones relacionadas:** B2.3-D31; B2.3-D33; `DEC-GOB-023`.
- **Dependencias:** RF-006; RF-008; RF-011.
- **Riesgos relacionados:** HZ-004; HZ-008.
- **Condiciones de aplicación:** Todo cambio de referencia durante operación.
- **Criterio de aceptación:** Las referencias fuera de límites o no autorizadas son rechazadas y registradas. Las referencias válidas se aplican con la transición aprobada. Límites pendientes.
- **Método de verificación:** Prueba con referencias válidas, fuera de rango y no autorizadas.
- **Verificabilidad:** Parcial — faltan límites y permisos.
- **Pendientes técnicos:** Definir rango de velocidad, permisos y restricciones dinámicas.

### RF-008 — Transición lazo abierto/cerrado

- **Descripción verificable:** El sistema supervisará la conmutación entre control en lazo abierto y lazo cerrado, verificará la realimentación y evitará cambios bruscos de salida.
- **Justificación:** Evitar transiciones inestables o con realimentación inválida.
- **Origen:** B2.4-D47.
- **Decisiones relacionadas:** B2.3-D34; `DEC-GOB-023`.
- **Dependencias:** RF-007; RF-009; RF-011.
- **Riesgos relacionados:** HZ-004.
- **Condiciones de aplicación:** Cambio de modo solicitado o automático.
- **Criterio de aceptación:** La transición solo se permite con realimentación válida y el cambio de salida permanece dentro del límite aprobado. Límite pendiente.
- **Método de verificación:** Prueba de transición con realimentación válida e inválida; registro de salida.
- **Verificabilidad:** Parcial — falta el límite de cambio.
- **Pendientes técnicos:** Definir condiciones de conmutación y límite de cambio de salida.

### RF-009 — Regulación PI configurable

- **Descripción verificable:** El sistema permitirá configurar las ganancias del controlador PI, validará los valores y supervisará oscilación, saturación e inestabilidad potencial.
- **Justificación:** Permitir el ajuste del lazo sin aceptar configuraciones inválidas o inestables.
- **Origen:** B2.4-D48; B2.4-D54.
- **Decisiones relacionadas:** B2.3-D26; B2.3-D35; `DEC-GOB-023`.
- **Dependencias:** RF-010; RF-011; RF-025.
- **Riesgos relacionados:** HZ-004.
- **Condiciones de aplicación:** Ajuste y validación del lazo de velocidad.
- **Criterio de aceptación:** Las ganancias son configurables; los valores inválidos son rechazados; la oscilación, saturación o inestabilidad potencial se detectan y reportan. Criterios pendientes.
- **Método de verificación:** Prueba con juegos de ganancias válidos e inválidos; análisis de estabilidad y respuesta.
- **Verificabilidad:** Parcial — faltan criterios de estabilidad.
- **Pendientes técnicos:** Definir rangos de ganancias y criterios de inestabilidad.

### RF-010 — Límites PI y anti-windup

- **Descripción verificable:** El sistema limitará la salida del PI, aplicará anti-windup y supervisará la saturación persistente, con respuesta basada en riesgos.
- **Justificación:** Evitar saturación, acumulación integral y pérdida de control.
- **Origen:** B2.4-D49.
- **Decisiones relacionadas:** B2.3-D27; `DEC-GOB-023`.
- **Dependencias:** RF-009.
- **Riesgos relacionados:** HZ-004.
- **Condiciones de aplicación:** Operación en lazo cerrado y cambios de referencia.
- **Criterio de aceptación:** La salida no supera el límite configurado; el anti-windup impide la acumulación integral mientras la salida está saturada; la saturación persistente se reporta. El valor del límite y el tiempo de persistencia son pendientes.
- **Método de verificación:** Prueba con saturación inducida y registro de salida e integral.
- **Verificabilidad:** Completa parametrizada; valores pendientes.
- **Pendientes técnicos:** Definir límites de salida y tiempo de saturación persistente.

### RF-011 — Medición y validación de velocidad

- **Descripción verificable:** El sistema validará la vigencia, coherencia y rango de la velocidad medida, aplicará un filtrado configurable y detectará realimentación no confiable.
- **Justificación:** Evitar que el lazo utilice datos inválidos, obsoletos o incoherentes.
- **Origen:** B2.4-D50.
- **Decisiones relacionadas:** B2.3-D28; B2.3-D29; `DEC-GOB-023`.
- **Dependencias:** RF-012; RF-013.
- **Riesgos relacionados:** HZ-013.
- **Condiciones de aplicación:** Toda adquisición de velocidad utilizada por el control o la supervisión.
- **Criterio de aceptación:** Los datos inválidos, obsoletos o fuera de rango son detectados; el filtro configurado se aplica; la realimentación no confiable se reporta. Rangos y filtros pendientes.
- **Método de verificación:** Prueba con señales válidas, ruido, datos obsoletos y fuera de rango.
- **Verificabilidad:** Parcial — faltan rangos y filtros.
- **Pendientes técnicos:** Definir sensor, rango, filtro, frecuencia de muestreo y tiempo de obsolescencia.

### RF-012 — Pérdida de realimentación

- **Descripción verificable:** El sistema detectará la pérdida de realimentación de velocidad y ejecutará la respuesta derivada del análisis de riesgos.
- **Justificación:** Evitar operación en lazo cerrado sin realimentación confiable.
- **Origen:** B2.4-D20.
- **Decisiones relacionadas:** B2.3-D30; `DEC-GOB-024`.
- **Dependencias:** RF-011; RF-003.
- **Riesgos relacionados:** HZ-013; HZ-004.
- **Condiciones de aplicación:** Operación en lazo cerrado y supervisión de velocidad.
- **Criterio de aceptación:** La pérdida se detecta y la respuesta configurada se ejecuta. Tiempo de detección y respuesta pendientes.
- **Método de verificación:** Simulación y prueba con pérdida de señal.
- **Verificabilidad:** Parcial — faltan tiempo y respuesta.
- **Pendientes técnicos:** Definir tiempo de detección y respuesta según riesgos.

### RF-013 — Fallas de sensores

- **Descripción verificable:** El sistema detectará desconexión, valores fuera de rango, incoherencias y datos obsoletos de sensores, con respuestas diferenciadas según el riesgo.
- **Justificación:** Evitar decisiones de control basadas en señales inválidas.
- **Origen:** B2.4-D21.
- **Decisiones relacionadas:** B2.3-D05; B2.3-D30; `DEC-GOB-024`.
- **Dependencias:** RF-011.
- **Riesgos relacionados:** HZ-013.
- **Condiciones de aplicación:** Sensores utilizados por el control y la supervisión.
- **Criterio de aceptación:** Cada clase de falla es detectada y tratada con la respuesta aprobada. Umbrales y tiempos pendientes.
- **Método de verificación:** Prueba con desconexión, rango, incoherencia y datos obsoletos.
- **Verificabilidad:** Parcial — faltan umbrales y respuestas.
- **Pendientes técnicos:** Definir clases, umbrales y respuestas por sensor.

### RF-014 — Fallas de comunicaciones

- **Descripción verificable:** El sistema detectará desconexiones, tiempos de espera, mensajes inválidos y datos obsoletos en los enlaces de comunicación utilizados, distinguiendo funciones críticas y no críticas.
- **Justificación:** Evitar comandos perdidos o supervisión incompleta por fallas de comunicación.
- **Origen:** B2.4-D22.
- **Decisiones relacionadas:** B2.3-D17; `DEC-GOB-024`.
- **Dependencias:** RF-027.
- **Riesgos relacionados:** HZ-014.
- **Condiciones de aplicación:** Enlaces de comunicación internos o con la interfaz de computador del primer incremento. La aplicabilidad a comunicaciones externas está pendiente.
- **Criterio de aceptación:** Cada condición es detectada y clasificada; las funciones críticas reciben la respuesta aprobada. Tiempos de espera pendientes.
- **Método de verificación:** Prueba con desconexión, timeout, mensaje inválido y dato obsoleto.
- **Verificabilidad:** Parcial — faltan tiempos y respuesta.
- **Pendientes técnicos:** Definir enlaces, timeouts y tratamiento por criticidad.

### RF-015 — Protecciones de sobrecorriente y tensión

- **Descripción verificable:** El sistema detectará sobrecorriente, sobretensión y subtensión, considerará la sobretensión regenerativa durante el frenado y ejecutará la respuesta de protección aprobada; cuando el análisis lo exija, dispondrá de protecciones eléctricas independientes.
- **Justificación:** Evitar daño eléctrico, térmico y condiciones peligrosas.
- **Origen:** B2.4-D23; B2.4-D24.
- **Decisiones relacionadas:** B2.3-D05; B2.3-D07; `DEC-GOB-024`.
- **Dependencias:** RF-001; RF-003; RF-019.
- **Riesgos relacionados:** HZ-007; HZ-009; HZ-010; HZ-019; FMEA-007.
- **Condiciones de aplicación:** Operación, arranque, frenado y fallas eléctricas.
- **Criterio de aceptación:** Cada condición se detecta, la salida de potencia se deshabilita y el evento se registra; las protecciones independientes requeridas actúan. Umbrales y tiempos pendientes.
- **Método de verificación:** Análisis, simulación y prueba con condiciones inducidas.
- **Verificabilidad:** Parcial — faltan umbrales, tiempos y arquitectura de protección.
- **Pendientes técnicos:** Definir umbrales, tiempos, histéresis y necesidad de protecciones independientes.

### RF-016 — Protección térmica

- **Descripción verificable:** El sistema supervisará los riesgos térmicos del motor y de la electrónica de potencia, detectará sobretemperatura y ejecutará la respuesta de protección aprobada.
- **Justificación:** Evitar daño térmico y degradación de componentes.
- **Origen:** B2.4-D25.
- **Decisiones relacionadas:** B2.3-D05; `DEC-GOB-024`.
- **Dependencias:** RF-001; RF-003.
- **Riesgos relacionados:** HZ-012; FMEA-008.
- **Condiciones de aplicación:** Operación continua, sobrecarga y fallas de refrigeración.
- **Criterio de aceptación:** La condición térmica se detecta y la respuesta aprobada se ejecuta. Límites, sensores y tiempos pendientes.
- **Método de verificación:** Análisis térmico, simulación y prueba controlada.
- **Verificabilidad:** Parcial — faltan límites y sensores.
- **Pendientes técnicos:** Definir límites, puntos de medición y tiempos de respuesta.

### RF-017 — Bloqueo y pérdida de carga

- **Descripción verificable:** El sistema detectará bloqueo mecánico y pérdida de carga mediante indicadores eléctricos y mecánicos, los diferenciará de transitorios de arranque o carga y ejecutará la respuesta basada en riesgos.
- **Justificación:** Evitar sobrecorriente, sobrevelocidad y daño mecánico.
- **Origen:** B2.4-D26; B2.4-D27.
- **Decisiones relacionadas:** B2.3-D05; `DEC-GOB-024`.
- **Dependencias:** RF-011; RF-015.
- **Riesgos relacionados:** HZ-007; HZ-008; FMEA-009.
- **Condiciones de aplicación:** Arranque, operación con carga y cambios de carga.
- **Criterio de aceptación:** Bloqueo y pérdida de carga se detectan y distinguen; la respuesta aprobada se ejecuta. Criterios y tiempos pendientes.
- **Método de verificación:** Simulación y prueba con carga controlada.
- **Verificabilidad:** Parcial — faltan criterios de discriminación.
- **Pendientes técnicos:** Definir indicadores, umbrales y tiempos de discriminación.

### RF-018 — Aceleración e inversión inesperadas

- **Descripción verificable:** El sistema comparará la velocidad y aceleración medidas con los comandos y la dirección solicitada, detectará aceleración o inversión inesperadas y aplicará la respuesta correspondiente.
- **Justificación:** Detectar pérdida de control o comandos incorrectos antes de que generen condiciones peligrosas.
- **Origen:** B2.4-D28; B2.4-D29.
- **Decisiones relacionadas:** B2.3-D05; `DEC-GOB-024`.
- **Dependencias:** RF-007; RF-011.
- **Riesgos relacionados:** HZ-005; HZ-006.
- **Condiciones de aplicación:** Arranque, cambios de referencia y operación.
- **Criterio de aceptación:** Las condiciones se detectan y la respuesta aprobada se ejecuta. Umbrales y tiempos pendientes.
- **Método de verificación:** Simulación y prueba con comandos y cargas controladas.
- **Verificabilidad:** Parcial — faltan umbrales y tiempos.
- **Pendientes técnicos:** Definir umbrales, ventanas de observación y respuestas.

### RF-019 — Pérdida de control y fallas de potencia

- **Descripción verificable:** El sistema supervisará la coherencia entre comandos, señales de control y comportamiento real, y detectará fallas de la etapa de potencia, incluyendo cortocircuitos, circuitos abiertos y conmutación incorrecta cuando sea observable.
- **Justificación:** Detectar fallas que puedan producir movimiento no controlado o daño eléctrico.
- **Origen:** B2.4-D30; B2.4-D31.
- **Decisiones relacionadas:** B2.3-D05; B2.3-D07; `DEC-GOB-024`.
- **Dependencias:** RF-011; RF-020.
- **Riesgos relacionados:** HZ-015; FMEA-009.
- **Condiciones de aplicación:** Operación, arranque y fallas de potencia.
- **Criterio de aceptación:** Las clases de falla observables se detectan y la respuesta aprobada se ejecuta. Cobertura y tiempos pendientes.
- **Método de verificación:** Análisis, simulación y prueba con fallas inducidas.
- **Verificabilidad:** Parcial — falta cobertura de detección.
- **Pendientes técnicos:** Definir clases de falla, cobertura y respuesta.

### RF-020 — Fallas internas del controlador

- **Descripción verificable:** El sistema detectará fallas internas relacionadas con ejecución, memoria, temporización y recursos, y aplicará la respuesta correspondiente a su criticidad.
- **Justificación:** Evitar que una falla del controlador elimine funciones de control o protección sin detección.
- **Origen:** B2.4-D32.
- **Decisiones relacionadas:** B2.3-D38; B2.3-D47; `DEC-GOB-024`.
- **Dependencias:** RNF-005.
- **Riesgos relacionados:** HZ-016; FMEA-010.
- **Condiciones de aplicación:** Operación normal y condiciones anómalas del controlador.
- **Criterio de aceptación:** Las clases de falla detectables se detectan y la respuesta aprobada se ejecuta. Cobertura y tiempos pendientes.
- **Método de verificación:** Análisis, simulación de fallas y prueba controlada.
- **Verificabilidad:** Parcial — faltan cobertura y tiempos.
- **Pendientes técnicos:** Definir mecanismos de detección, cobertura y respuesta por criticidad.

### RF-021 — Pérdida y recuperación de alimentación

- **Descripción verificable:** El sistema detectará la pérdida de alimentación y, tras su recuperación, verificará las condiciones necesarias antes de permitir nuevamente el movimiento, conforme a la respuesta derivada del riesgo.
- **Justificación:** Evitar reinicios y movimientos no deseados después de una interrupción.
- **Origen:** B2.4-D19.
- **Decisiones relacionadas:** B2.3-D11; B2.3-D51; `DEC-GOB-024`.
- **Dependencias:** RF-001; RF-003; RF-022.
- **Riesgos relacionados:** HZ-011; HZ-018; FMEA-012.
- **Condiciones de aplicación:** Pérdida de alimentación, caída de tensión y recuperación.
- **Criterio de aceptación:** Tras la pérdida, el motor permanece deshabilitado hasta que se verifiquen las condiciones aprobadas; la respuesta de recuperación se ejecuta. Condiciones pendientes.
- **Método de verificación:** Simulación y prueba con interrupciones controladas.
- **Verificabilidad:** Parcial — faltan condiciones de recuperación.
- **Pendientes técnicos:** Definir condiciones, tiempos y comportamiento antes y después de la recuperación.

### RF-022 — Restablecimiento y reinicio condicionados

- **Descripción verificable:** El sistema permitirá el restablecimiento y reinicio solo después de verificar la eliminación de la falla, la presencia de condiciones seguras y la autorización requerida según el riesgo; registrará el evento.
- **Justificación:** Evitar la reanudación con una falla presente o sin autorización.
- **Origen:** B2.4-D18.
- **Decisiones relacionadas:** B2.3-D11; B2.3-D51; `DEC-GOB-024`.
- **Dependencias:** RF-001; RF-003; RF-021.
- **Riesgos relacionados:** HZ-018; HZ-022.
- **Condiciones de aplicación:** Después de una parada de protección, una falla o una pérdida de alimentación.
- **Criterio de aceptación:** El restablecimiento se rechaza mientras la falla o la condición insegura persista; la autorización requerida se registra; el reinicio solo se permite cuando las condiciones son válidas.
- **Método de verificación:** Prueba con falla presente y ausente; inspección de registros.
- **Verificabilidad:** Completa cualitativa.
- **Pendientes técnicos:** Definir condiciones seguras y autorizaciones por tipo de falla.

### RF-023 — Configuración validada y persistente

- **Descripción verificable:** El sistema guardará configuraciones validadas, comprobará su integridad y conservará la configuración válida anterior para recuperación.
- **Justificación:** Evitar la pérdida o corrupción de parámetros necesarios para una operación segura.
- **Origen:** B2.4-D55.
- **Decisiones relacionadas:** B2.3-D36; `DEC-GOB-026`.
- **Dependencias:** RF-024; RNF-002.
- **Riesgos relacionados:** HZ-017; FMEA-011.
- **Condiciones de aplicación:** Guardado, carga y actualización de configuración.
- **Criterio de aceptación:** Una configuración inválida o corrupta es rechazada; la configuración válida anterior puede recuperarse; el resultado se registra.
- **Método de verificación:** Inspección y prueba con corrupción e invalidez inducidas.
- **Verificabilidad:** Completa cualitativa.
- **Pendientes técnicos:** Definir mecanismo de integridad, almacenamiento y versionado.

### RF-024 — Recuperación de configuración inválida

- **Descripción verificable:** El sistema detectará configuraciones inválidas, recuperará una configuración válida cuando sea posible, verificará las condiciones de seguridad antes de habilitar y registrará el incidente.
- **Justificación:** Evitar que una configuración inválida habilite el motor o impida la recuperación.
- **Origen:** B2.4-D56.
- **Decisiones relacionadas:** B2.3-D36; `DEC-GOB-026`.
- **Dependencias:** RF-023; RF-001.
- **Riesgos relacionados:** HZ-017; FMEA-011.
- **Condiciones de aplicación:** Inicio, cambio de configuración y recuperación de fallas.
- **Criterio de aceptación:** Una configuración inválida no habilita el motor; se recupera una configuración válida o se mantiene un estado seguro; el incidente se registra.
- **Método de verificación:** Prueba con configuraciones inválidas y válidas; inspección de registros.
- **Verificabilidad:** Completa cualitativa.
- **Pendientes técnicos:** Definir configuraciones de respaldo y condiciones de seguridad.

### RF-025 — Cambio de parámetros por criticidad

- **Descripción verificable:** El sistema clasificará los parámetros por criticidad, determinará cuáles pueden modificarse en operación y cuáles requieren parada y autorización adicional, verificará las condiciones operativas, confirmará la aplicación y permitirá la reversión cuando corresponda.
- **Justificación:** Evitar cambios de parámetros que alteren el comportamiento seguro durante la operación.
- **Origen:** B2.4-D57; B2.4-D59.
- **Decisiones relacionadas:** B2.3-D14; B2.3-D15; `DEC-GOB-020`; `DEC-GOB-026`.
- **Dependencias:** RF-026; RNF-004.
- **Riesgos relacionados:** HZ-017; HZ-023.
- **Condiciones de aplicación:** Cambio de cualquier parámetro operativo.
- **Criterio de aceptación:** Los parámetros críticos no pueden modificarse en operación; todo cambio se realiza en el estado permitido; la aplicación se confirma; la reversión se ejecuta cuando corresponde. La matriz de criticidad es pendiente.
- **Método de verificación:** Inspección de la matriz y prueba de cambios permitidos y rechazados.
- **Verificabilidad:** Parcial — falta la matriz de criticidad.
- **Pendientes técnicos:** Definir clasificación, estados permitidos, autorizaciones y reversión.

### RF-026 — Auditoría de cambios de configuración

- **Descripción verificable:** El sistema registrará los valores anteriores y nuevos, usuario, fecha, motivo, validación y resultado de cada cambio de configuración, permitiendo reconstruir el historial.
- **Justificación:** Permitir la trazabilidad y el análisis de cambios que afecten el comportamiento del sistema.
- **Origen:** B2.4-D58.
- **Decisiones relacionadas:** B2.3-D39; B2.3-D42; `DEC-GOB-026`.
- **Dependencias:** RF-025; RNF-003.
- **Riesgos relacionados:** HZ-017; FMEA-011.
- **Condiciones de aplicación:** Todo cambio de configuración, aceptado o rechazado.
- **Criterio de aceptación:** Cada cambio produce un registro con todos los campos exigidos; el historial permite reconstruir la secuencia de cambios.
- **Método de verificación:** Inspección de registros y prueba de cambios aceptados y rechazados.
- **Verificabilidad:** Completa cualitativa.
- **Pendientes técnicos:** Definir formato, retención, protección de integridad y mecanismo de consulta.

### RF-027 — Registro de eventos, fallas y protecciones

- **Descripción verificable:** El sistema registrará eventos operativos, fallas, alarmas y activaciones de protección con referencia temporal, tipo, severidad, estado y causa cuando esté disponible.
- **Justificación:** Permitir la reconstrucción de incidentes y la verificación del comportamiento de las protecciones.
- **Origen:** B2.4-D42; B2.4-D43; B2.4-D56.
- **Decisiones relacionadas:** B2.3-D06; B2.3-D09; B2.3-D39; `DEC-GOB-024`; `DEC-GOB-026`.
- **Dependencias:** RF-003; RF-004; RF-026.
- **Riesgos relacionados:** HZ-003; HZ-004; HZ-017.
- **Condiciones de aplicación:** Operación, fallas y pruebas.
- **Criterio de aceptación:** Los eventos se registran con los campos definidos y permiten reconstruir la secuencia. La retención y el formato son pendientes.
- **Método de verificación:** Inspección de registros y prueba de eventos inducidos.
- **Verificabilidad:** Parcial — faltan retención y formato.
- **Pendientes técnicos:** Definir tipos, severidades, retención y formato.

## 7. Trazabilidad

| Requisito | Decisiones B2.4 | Decisiones B2.3 | Peligros | Verificación |
|---|---|---|---|---|
| RF-001 | D39; D40 | B2.3-D25 | HZ-001; HZ-002; HZ-020; HZ-021 | Prueba e inspección |
| RF-002 | D41 | B2.3-D25 | HZ-001; HZ-021 | Prueba e inspección |
| RF-003 | D42 | B2.3-D07; B2.3-D25 | HZ-003; HZ-004 | Prueba |
| RF-004 | D43 | B2.3-D25 | HZ-003 | Prueba |
| RF-005 | D44 | B2.3-D31 | HZ-003; HZ-005; HZ-010 | Prueba |
| RF-006 | D45 | B2.3-D31 | HZ-005; HZ-007 | Prueba |
| RF-007 | D46 | B2.3-D31; B2.3-D33 | HZ-004; HZ-008 | Prueba |
| RF-008 | D47 | B2.3-D34 | HZ-004 | Prueba |
| RF-009 | D48; D54 | B2.3-D26; B2.3-D35 | HZ-004 | Análisis y prueba |
| RF-010 | D49 | B2.3-D27 | HZ-004 | Prueba |
| RF-011 | D50 | B2.3-D28; B2.3-D29 | HZ-013 | Prueba |
| RF-012 | D20 | B2.3-D30 | HZ-013; HZ-004 | Simulación y prueba |
| RF-013 | D21 | B2.3-D05; B2.3-D30 | HZ-013 | Prueba |
| RF-014 | D22 | B2.3-D17 | HZ-014 | Prueba |
| RF-015 | D23; D24 | B2.3-D05; B2.3-D07 | HZ-007; HZ-009; HZ-010; HZ-019 | Análisis y prueba |
| RF-016 | D25 | B2.3-D05 | HZ-012 | Análisis y prueba |
| RF-017 | D26; D27 | B2.3-D05 | HZ-007; HZ-008 | Simulación y prueba |
| RF-018 | D28; D29 | B2.3-D05 | HZ-005; HZ-006 | Simulación y prueba |
| RF-019 | D30; D31 | B2.3-D05; B2.3-D07 | HZ-015 | Análisis y prueba |
| RF-020 | D32 | B2.3-D38; B2.3-D47 | HZ-016 | Análisis y prueba |
| RF-021 | D19 | B2.3-D11; B2.3-D51 | HZ-011; HZ-018 | Simulación y prueba |
| RF-022 | D18 | B2.3-D11; B2.3-D51 | HZ-018; HZ-022 | Prueba |
| RF-023 | D55 | B2.3-D36 | HZ-017 | Inspección y prueba |
| RF-024 | D56 | B2.3-D36 | HZ-017 | Inspección y prueba |
| RF-025 | D57; D59 | B2.3-D14; B2.3-D15 | HZ-017; HZ-023 | Inspección y prueba |
| RF-026 | D58 | B2.3-D39; B2.3-D42 | HZ-017 | Inspección |
| RF-027 | D42; D43; D56 | B2.3-D06; B2.3-D09; B2.3-D39 | HZ-003; HZ-004; HZ-017 | Inspección y prueba |

## 8. Pendientes

- Todos los requisitos son candidatos y están en estado **Propuesto**.
- Las prioridades no están determinadas.
- Los valores cuantitativos y tolerancias no están definidos.
- Varios criterios de aceptación están incompletos y por ello no se declaran verificables.
- No existe línea base de requisitos funcionales.
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

- **0.1 — 2026-10-19 — B2.1:** estructura inicial del registro de requisitos funcionales. Sin requisitos definidos.
- **0.1 — 2026-10-19 — B2.1.1:** aprobación de la estructura y de la línea base de gestión de requisitos (DEC-GOB-010 a DEC-GOB-015).
- **0.2 — 2026-10-20 — B2.4:** incorporación de 27 requisitos funcionales candidatos, trazabilidad a D01–D60 y al análisis preliminar de riesgos. Ningún requisito aprobado.
