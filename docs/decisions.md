# PPL Decisions

This document records the architectural and design decisions for the PPL project.

### Decision 001 — Offline-first design

**Status:** Accepted

**Decision:** PPL must be capable of useful operation without an Internet connection.

**Notes:** Internet connectivity must not be a fundamental requirement for the core experience.

### Decision 002 — Local discovery

**Status:** Accepted

**Decision:** PPL's primary discovery experience is proximity-oriented.

**Notes:** Discovery is intended to help users find nearby people rather than provide a general Internet-wide social directory.

### Decision 003 — Public calling card

**Status:** Working

**Decision:** PPL discovery should expose a deliberately small public calling card.

**Notes:** The current working concept includes a handle, a short public byline (target approximately 128 characters), and optional interests. The exact protocol representation is not yet decided.

### Decision 004 — Separate discovery from private communication

**Status:** Accepted

**Decision:** Information deliberately exposed during discovery is conceptually separate from subsequent private communication.

**Notes:** Communication beyond deliberately public discovery information is expected to use secure mechanisms provided by the eventual networking/messaging stack. The exact protocol implementation is not yet decided.

### Decision 005 — Standalone device

**Status:** Accepted

**Decision:** The PPL device must be capable of basic operation without requiring a phone, laptop or Internet connection.

**Notes:** A local Wi-Fi web interface/PWA may provide a more convenient secondary interface.

### Decision 006 — Established networking foundations

**Status:** Under investigation

**Decision:** PPL will investigate Reticulum as its underlying networking technology and LXMF as a possible messaging layer rather than immediately creating a completely independent networking and messaging stack.

**Notes:** These technologies are still subject to experimental validation and are not considered final until tested.

### Decision 007 — Small experimental steps

**Status:** Accepted

**Decision:** PPL development will proceed through small, independently testable experiments before attempting an end-to-end implementation.

### Decision 008 — AI architectural boundary

**Status:** Accepted

**Decision:** AI coding agents may investigate, propose and implement approved changes, but must not silently introduce significant product or architectural decisions.

**Notes:** When requirements or architecture are unclear, the agent should identify the uncertainty and ask for direction rather than guessing.

### Decision 009 — Protocol and branding separation

**Status:** Accepted

**Decision:** PPL's underlying protocol and application concepts should remain separate from branding and deployment-specific presentation.

**Notes:** This ensures that sponsored, event or white-label versions remain possible.

### Decision 010 — Scalability is a design concern

**Status:** Accepted

**Decision:** The project will explicitly test behaviour beyond a two-node prototype.

**Notes:** Discovery traffic, radio airtime, resource use, retries, latency and multi-hop behaviour will eventually be measured as node counts increase.
