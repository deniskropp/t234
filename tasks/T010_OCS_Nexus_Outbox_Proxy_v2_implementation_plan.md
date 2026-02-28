# Implementation Plan: T010 Nexus Outbox Functional Proxy

## Phase 1: Configuration & Schema
- [ ] Define `assets/endpoints.json` with the following structure:
  ```json
  {
    "targets": {
      "JIRA": { "url": "https://mock.jira.nexus/api/v1/issue", "method": "POST" },
      "SLACK": { "url": "https://mock.slack.nexus/services/hooks", "method": "POST" }
    }
  }
  ```
- [ ] Update `index.html` to load this configuration at initialization.

## Phase 2: Dispatcher Core (JS)
- [ ] Implement `class WebhookDispatcher` in the `<script>` section of `index.html`.
- [ ] Add `async dispatch(agent, target, insight)` method.
- [ ] Integrate `Chronos` cooldown logic to ensure dispatches don't overwhelm target systems.

## Phase 3: UI Enhancement
- [ ] Modify the `updateOutboxUI()` function to include a status badge column.
- [ ] Implement color-coded indicators:
  - `PENDING`: Pulsing Warning Yellow (#ffea00)
  - `SUCCESS`: Steady Neon Cyan (#00e5ff)
  - `ERROR`: Flashing Magenta (#f000ff)

## Phase 4: Integration & Testing
- [ ] Hook `refractSemantics()` into the new `WebhookDispatcher`.
- [ ] Log dispatch results to the Swarm Log using `⫻data/event` syntax.
- [ ] Verify persistence of dispatch status in Synapse memory.
