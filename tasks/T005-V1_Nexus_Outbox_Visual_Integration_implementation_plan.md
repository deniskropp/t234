# Implementation Plan: T005-V1 - Nexus Outbox Visual Integration

## 1. UI Section Scaffolding
- [ ] Add the section header "7. Nexus Outbox: External Interventions" with the `neon-text-magenta` class.
- [ ] Create a container div with `grid grid-cols-1 md:grid-cols-3 gap-6`.

## 2. CSS Enhancements
- [ ] Define `.outbox-card` with background `#1a2235`, border-radius `xl`, and a subtle `neon-border-cyan`.
- [ ] Implement `.pulse-glow` animation for active intervention icons.
- [ ] Define `.icon-container` for consistent icon sizing and centering.

## 3. Intervention Card Structure
- [ ] **Jira Card**: Displays `assets/jira_hijack.webp`, status "HIJACKED", and a mock target (e.g., `PROD-404`).
- [ ] **Slack Card**: Displays `assets/slack_interference.webp`, status "INFILTRATED", and a mock channel (e.g., `#general`).
- [ ] **Email Card**: Displays `assets/email_refraction.webp`, status "REFRACTED", and a mock recipient.

## 4. Interaction & Logic
- [ ] Implement a `displayIntervention(type, target)` function that adds a new card to the outbox.
- [ ] Connect this function to the `refractSemantics()` response parsing (T005).

## 5. Verification
- [ ] Confirm the visual consistency with the "Cybernetic Neon Night" aesthetic.
- [ ] Ensure no SVG/Mermaid JS usage.
- [ ] Test the responsive layout on mobile and desktop.
