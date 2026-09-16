# PPL Project Brief

## Overview
PPL is a small, offline-first, privacy-focused radio device for discovering nearby people and exchanging direct encrypted messages without relying on a central social-media platform. The device is designed to operate independently, prioritizing privacy, offline functionality, and a simple, approachable user experience.

## Current Status
The PPL project is currently in a greenfield state and is in the planning and hardware experimentation phase.

## Established Project Goals
*   **Offline-First & Proximity Discovery:** Enable users to discover others nearby without an Internet connection or a central platform.
*   **Standalone Operation:** The device functions as a dedicated unit with its own screen and physical controls, not requiring a smartphone or Internet connection.
*   **Privacy & Simplicity:** Privacy, offline operation, finite local storage, and simplicity are core requirements.
*   **Secure Communication:** Communication beyond deliberately public discovery information must be encrypted.
*   **Social Onboarding:** Support onboarding with a user handle, optional public byline, optional interests, and configurable social modes/intents.
*   **Protocol-Branding Separation:** The underlying PPL protocol should remain separate from branding and deployment-specific configurations to support white-labelled or sponsored events (e.g., festivals, conferences).
*   **Standardized Foundations:** Reuse established networking and cryptographic mechanisms rather than inventing unnecessary new ones.

## Current Working Assumptions
*   **Discovery Interface:** Local discovery is the primary "hook." A nearby person can see a small public calling card consisting of a handle, a short byline (targeted at ~128 characters), and optional interests.
*   **Intentional Discovery:** The goal of discovery is to facilitate human connection (deciding whether you want to know another person) rather than simply indicating device presence.
*   **Local Web Interface:** A local Wi-Fi web interface or PWA may provide a convenient alternative for phone or laptop users, but it is secondary to the device's standalone operation.
*   **MVP UI Design:** The initial user interface will focus on simple nested/cascading menus, scrolling lists, and navigation via a rotary encoder and buttons.
*   **Networking Stack:** Reticulum is the preferred underlying networking technology for investigation.
*   **Messaging Layer:** LXMF is being investigated as the messaging layer on top of Reticulum.
*   **Application Focus:** The PPL-specific software layer is primarily concerned with the human/social experience, including identity, discovery, connection requests, and conversations.
*   **Device Storage:** Device storage should be deliberately finite and privacy-friendly, with longer-term history potentially maintained locally by the optional PWA rather than requiring cloud storage.

## Ideas Still Being Explored
*   **Mesh Networking & Reach:** While discovery remains local/proximity-oriented by design, messaging may travel beyond immediate radio range via a Reticulum mesh, including multi-hop and potentially Internet-connected bridge nodes.
*   **Social Modes & Interests:** Configurable modes (e.g., Social, Dating, Networking, Event) and specific interest categories (e.g., hiking, music, coffee) are being explored and are not yet final protocol decisions.
*   **Scalability:** Discovery and messaging mechanisms must eventually be tested and validated at scales beyond a two-device prototype.
