# Implementation Plan: T003 - OCS Autonomous Feedback Loops

## 1. Metric Analysis Layer
- [ ] Define the `Existential Dread` thresholds (e.g., >80% for critical).
- [ ] Update `forecastLineChart` to also store/access historical data from `localStorage`.

## 2. Self-Adjusting Intensity Logic
- [ ] Develop a `calculateDesiredIntensity()` function that considers `Systemic Coherence` vs. `Collapse Probability`.
- [ ] Implement a function for agents to propose an intensity change (e.g., `agentProposeIntensity(newVal)`).

## 3. Dynamic Prompting Integration
- [ ] Modify the `systemInstruction` in `refractSemantics()` to include real-time chart data:
  ```javascript
  const contextData = `System Coherence: ${currentCoherence}, Collapse Prob: ${currentCollapse}`;
  ```
- [ ] Allow the Gemini API to respond with a specific OCS command (e.g., `⫻cmd/mode:REDUCE_INTENSITY`) to trigger UI updates.

## 4. Unprompted Interventions
- [ ] Create a `window.setInterval` loop that checks metrics every 10 seconds.
- [ ] Trigger an "Autonomous Refraction" event if metrics breach a safe threshold, using a randomized agent (DIMA or KODAX).

## 5. Persistence & State Management
- [ ] Implement `saveChartData()` and `loadChartData()` to persist the Line and Bar charts in `localStorage`.
- [ ] Ensure the API key and agent selection also persist correctly after a page reload.

## 6. Verification
- [ ] Confirm no SVG/Mermaid JS usage.
- [ ] Test the automatic intensity adjustment with the API key active.
