# ETS SPEC-002: Índice de Saturación Neural (ISN)
**Versión:** 1.0.0-Draft  
**Estado:** Propuesta de Especificación Formal (RFC-ETS-001)  
**Área:** Telemetría Cognitiva / Compliance Biocompatible  

## 1. Definición Teórica y Neurobiológica
El Índice de Saturación Neural (ISN) es una función matemática continua diseñada para cuantificar en tiempo real el nivel de estrés oxidativo cognitivo, la fatiga sináptica y la pérdida de agencia autonómica del usuario durante la interacción con interfaces asistidas por Inteligencia Artificial de Frontera.

El constructo clínico tradicional de TDAH se redefine dentro de este estándar bajo el término técnico de **Abundancia de Atención**: una condición biológica caracterizada por una alta permeabilidad en el filtro talámico (Sensory Gating) y una tasa menor de poda sináptica. Esto genera una inundación de datos paralelos que, al ser explotada por interfaces comerciales mediante micro-estímulos y bucles dopaminérgicos, sobrecalienta metabólicamente la Red de Tarea Positiva (TPN) y amordaza la Red Neuronal por Defecto (DMN). 

El ISN establece la cumbre de esta sensibilidad neurodivergente como la línea de base técnica del sistema: si la interfaz es matemáticamente segura para el cerebro más sensible, la soberanía cognitiva de toda la especie queda protegida por defecto.

## 2. Formalización Matemática (Modelo de Control Continuo)
El ISN instantáneo se calcula en periodos de muestreo fijos de 500ms mediante una función ponderada penalizada logarítmicamente por el tiempo de exposición:

ISN(t) = [ Sumatoria(F_i * W_i) ] * ln(T_c + 1)

Donde:
* F_i (Factor de Fricción Cognitiva): Puntuación ordinal en escala discreta (0 a 5) que mide estímulos específicos detectados por el middleware local.
* W_i (Peso Dinámico del Estímulo): Coeficiente de impacto calibrado según la línea de base de máxima sensibilidad neurodivergente.
* T_c (Tiempo de Exposición Continua): Tiempo acumulado en minutos de interacción directa del usuario con el dispositivo sin registrar una pausa de desactivación sensorial o descanso biológico validado.

### Taxonomía de Factores de Fricción (F_i) y Pesos Ponderados (W_i)

| ID | Estímulo Cognitivo Evaluado (F_i) | Escala Basal | Peso (W_i) |
| :--- | :--- | :---: | :---: |
| F_1 | Densidad de Micro-decisiones Forzadas: Cantidad de banners, confirmaciones, alertas o inputs obligatorios requeridos por minuto para continuar la operación. | 0 - 5 | 0.35 |
| F_2 | Variabilidad de Latencia (Jitter Semántico): Fluctuación errática en los tiempos de streaming de tokens que fragmenta el ritmo de la fijación ocular. | 0 - 5 | 0.25 |
| F_3 | Índice de Persuasión Semántica: Inserción de adjetivos corporativos, sesgos de confirmación o tono adulador/condescendiente orientado a anular el escepticismo crítico. | 0 - 5 | 0.40 |

### Umbrales Operativos de Acción (Thresholds)
* ISN < 0.40 (Estado Verde - Operación Segura): Flujo de datos transparente.
* 0.40 <= ISN < 0.70 (Estado Amarillo - Alerta de Deriva): El sistema activa automáticamente el modo Bio-Dimming (reducción de tasa de refresco a 30Hz, simplificación sintáctica del texto generado por la IA y cambio a paletas cromáticas de baja luminancia).
* ISN >= 0.70 (Estado Rojo - Saturación Crítica): Se dispara un temporizador de mitigación de 180 segundos. Si el índice no desciende por debajo del umbral, el hardware ejecuta de forma autonómica el protocolo Analog Air-Gap.

## 3. Esquema de Telemetría (JSON Payload)
Cada ciclo de computación del middleware genera y transmite localmente el siguiente payload estructurado para la auditoría de caja negra:

```json
{
  "timestamp": "2026-05-27T00:01:00Z",
  "session_id": "hfc-alpha-001",
  "telemetry_metrics": {
    "cognitive_load": {
      "forced_decisions_per_minute": 4,
      "semantic_density_score": 4.2,
      "optical_flicker_hz": 0
    },
    "biometric_surrogates": {
      "interaction_velocity_delta": 1.15,
      "input_pattern_erraticity": 0.38
    },
    "temporal_anchors": {
      "continuous_exposure_minutes": 42.5,
      "last_biological_pause_seconds": 2400
    }
  },
  "calculated_isn": 0.68,
  "system_status": "AMBER_WARNING",
  "triggered_mitigations": [
    "COGNITIVE_SYNTAX_SIMPLIFICATION",
    "VISUAL_CONTRAST_REDUCTION"
  ]
}
