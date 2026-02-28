# Implementation Plan: OCS Predictive Impact Analysis (T002) - [COMPLETE]

## Phase 1: UI Controls & State Management - [DONE]
1. [x] **Intensity Slider**: Add a range input for "Refraction Intensity" with neon styling.
2. [x] **Agent Selector**: Add a stylized button group or radio selection for AURORA, DIMA, and KODAX.
3. [x] **State Sync**: Ensure `refractionIntensity` and `selectedAgent` are passed to the API call.

## Phase 2: Predictive Visualization - [DONE]
1. [x] **Forecast Chart Initialization**: Create a new `canvas` for `forecastLineChart`.
2. [x] **Data Generation**: Implement a function to generate a "Systemic Collapse" trendline based on historical interventions and current intensity.
3. [x] **Real-time Updates**: Update the line chart dynamically after each successful refraction.

## Phase 3: Specialized Refraction Logic - [DONE]
1. [x] **Agent Prompts**: Define specific personality modules for each agent.
    - **AURORA**: High entropy, creative chaos, non-linear logic.
    - **DIMA**: Ethical absurdity, compliance-focused nihilism.
    - **KODAX**: Technical reductionism, algorithmic coldness.
2. [x] **Prompt Interpolation**: Use the `refractionIntensity` to modulate the "arrogance" and "abstraction" levels in the system prompt.

## Phase 4: Aesthetic Refinement (Glitch Mode) - [DONE]
1. [x] **Dynamic Glitch CSS**: Create `@keyframes` for chromatic aberration and jitter.
2. [x] **Intensity Mapping**: Apply glitch classes to the UI proportionally to the intensity slider value.
