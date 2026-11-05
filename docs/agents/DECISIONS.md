# Decisions — ProiectWeb2

<!-- graffino-agentic:begin v1 -->
> Constraints the code must obey. Status: `approved` (obey) · `proposed` (do not
> build on it) · `superseded-by <ID>` (kept to explain old code).
> Adding or changing an entry needs the user's OK (AGENTS.md → The gate).
<!-- graffino-agentic:end -->

## Index
- D-001 · All server services run containerized in Docker

---

## D-001 · All server services run containerized in Docker
- **Status:** approved
- **Date:** 2026-11-05
- **Rule:** All server-side components, backend services, background workers, and databases must run containerized in Docker.
- **Why:** Ensures consistent environments across developer machines and deployment, eliminating host-dependent configuration drift.
- **Rejected:** Running server services and databases directly on the host OS.
- **Evidence:** User instruction: "mi am isntalat docker si il vom folosi pentru orice chestie legata de server"
- **Source:** user · confidence high
- **Confirmed:** 2026-11-05
