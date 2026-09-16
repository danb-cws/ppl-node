# PPL Architecture

This document outlines the proposed architecture for the PPL project. As the project is in its early planning and experimentation phase, many elements are currently considered working assumptions or areas for investigation rather than final implementation decisions.

## Architectural Principles
PPL is designed with a layered approach to separate the human/social experience from the underlying radio and networking technologies. The project prioritizes the use of established standards for networking and cryptography rather than reinventing core infrastructure.

## Conceptual Stack
The architecture is organized into the following layers:

### 1. PPL Experience
The top-level layer focused on user interaction and social objects:
*   **Personas:** Handles, public bylines, interests and social presentation.
*   **Social State:** Social modes/intents, discovery, discovered people, and matches.
*   **Interaction:** Connection requests, contacts, and conversations.
*   **Interfaces:** Physical device UI and optional local Wi-Fi web interface/PWA.

### 2. PPL Application Layer
Defines the semantics and metadata specific to PPL:
*   PPL-specific discovery and profile information.
*   Social interaction and connection-request semantics.
*   Application-specific metadata.

### 3. Networking / Messaging Layer
Leverages established mesh networking technologies:
*   **Reticulum:** Currently the preferred networking technology for identity, addressing, encryption, and routing.
*   **LXMF:** Being investigated for message delivery and store-and-forward capabilities.

### 4. Radio Layer
*   **LoRa Radio:** The primary physical transport.
*   **Hardware:** Currently expected to use SX1262-class radios on prototype hardware.

### 5. Hardware / Device Layer
*   **MCU:** ESP32-class embedded hardware.
*   **Peripherals:** Screen, physical controls (rotary encoder and buttons), battery, and optional buzzer.
*   **Storage & Connectivity:** Local storage and optional Wi-Fi for the PWA interface.

## Architectural Boundaries
PPL aims to define the human/social experience. Where appropriate, the project prefers established mechanisms for:
*   Cryptographic identity and encryption.
*   Addressing and routing.
*   Message delivery.

PPL-specific definitions are focused on identity presentation, discovery mechanisms, public information exposure, connection workflows, and conversation management.

## Discovery (Exploratory)
Discovery is proximity-oriented by design and is currently under investigation. The goal is to allow nearby nodes to expose a small public "calling card."
*   **Content:** Targeted to include handle, a short byline (~128 characters), optional interests, and potential social modes.
*   **Mechanism:** The project is investigating using Reticulum’s existing identity and announce mechanisms rather than a custom unauthenticated broadcast protocol.
*   **Scalability:** Traffic frequency and packet size are critical areas for future scalability testing.

## Messaging (Working Assumptions)
Messaging is conceptually separated from discovery:
*   **Security:** Communication beyond deliberately public discovery information is expected to use the underlying secure mechanisms provided by the selected networking/messaging stack.
*   **Reach:** While discovery is local, messages may travel beyond immediate radio range via Reticulum multi-hop routing or bridge nodes.
*   **Persistence:** LXMF is being investigated for offline message delivery and store-and-forward behavior.

## Local PWA
A local Wi-Fi web interface/PWA serves as an optional convenience interface for:
*   Easier text entry and profile configuration.
*   Contact management and conversation history.
*   Device configuration.
*   *Note:* The device must remain capable of basic operation without the PWA. The exact storage model for long-term history (device vs. PWA) is not yet decided.

## White-Label Deployments
The architecture decouples the core protocol from branding. Deployment-specific configurations (logos, splash screens, event-specific terminology) should remain separate from the underlying social and networking protocol.

## Scalability and Testing
Scalability is a first-class concern. Future testing will involve increasing node counts (from 2 up to larger simulated populations) and busy radio environments. Key metrics include:
*   Discovery traffic and airtime.
*   Collisions, retries, and message latency.
*   Resource usage (CPU, RAM, storage, and battery).

## Experimental Roadmap
The architecture will be validated through a sequence of small experiments:
1.  Two-node Reticulum communication.
2.  LXMF messaging.
3.  Offline/store-and-forward behavior.
4.  PPL identity and profile representation.
5.  PPL discovery mechanisms.
6.  Social connection behavior.
7.  Larger-scale discovery testing.
8.  Physical device UI.
9.  Local PWA.
10. End-to-end PPL prototype.

## Current Uncertainties
The following are **not final decisions** and require further experimentation:
*   Use of Reticulum and LXMF.
*   Discovery packet structure and packet sizes.
*   Social modes and intents.
*   Storage architecture and specific MCU/display hardware.
*   Multi-hop and Internet bridging implementations.
