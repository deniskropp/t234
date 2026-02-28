# Cogito G3: System Background Commands

| Command | Status | Description |
|---|---|---|
| `setInterval (Autonomous Loop)` | ACTIVE | Client-side (index.html). Triggers Halin/Chronos recalibration every 15s. |
| `startHeartbeat` | ACTIVE | Client-side (index.html). Simulating OCS agent signals in Swarm Log. |
| `WebhookDispatcher` | PENDING | To be initialized in T010. Will manage async `fetch()` interventions. |

*Note: All backend (Python/FastAPI) processes have been ABORTED to adhere to the strict TS/JS stack mandate.*
