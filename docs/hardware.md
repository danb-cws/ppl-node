# PPL Hardware

## Hardware Currently Owned
The current prototype hardware includes:
*   **2 × Heltec WiFi LoRa 32 V3 boards**
*   **SMA antenna pigtail**
*   **Several antennas**, including a larger high-gain antenna
*   **1 × LilyGO T-Echo**
*   **1 × generic ESP32-WROOM board**
*   **1 × LilyGO T-Display**
*   **1 × ESP32-CAM**
*   **Various breadboards, jumper wires and basic electronic components**
*   **1 × rotary encoder**
*   **1 × 3.7 V Li-ion battery**
*   **1 × small buzzer**
*   **Multimeter**

## Current Preferred PPL Device Concept
The eventual PPL node is currently envisaged as:
*   **LoRa radio**
*   **ESP32-class microcontroller** or similar embedded platform
*   **Integrated screen**
*   **Physical controls** including a rotary encoder and buttons
*   **Internal rechargeable battery**
*   **USB-C charging**
*   **User-replaceable/upgradable external antenna** using a standard SMA connector
*   **Standalone operation** without requiring a phone
*   **Optional local Wi-Fi web interface/PWA**
*   **Optional buzzer** for confirmation, incoming message, error and rotary feedback, with the possibility of silent operation
*   **Deliberately finite local storage**

The battery is intended to be internal rather than user-replaceable. Battery replacement/service can be considered later if required.

## Current Prototype Direction
The **Heltec WiFi LoRa 32 V3** is currently the primary board for initial LoRa and Reticulum experiments. The two Heltec boards are particularly useful for testing communication between two independent nodes.

The **LilyGO T-Echo** is useful as an independent Reticulum/RNode reference device.

The other ESP32 boards can be used for UI, Wi-Fi and other experiments as appropriate.

## Hardware Under Consideration
Possible future integrated e-paper hardware has been discussed, including boards based on:
*   ESP32-S3
*   SX1262 LoRa
*   Integrated e-paper displays
*   USB-C
*   Battery support

*Note: Specific future hardware has NOT been selected. No particular e-paper board has been chosen at this stage.*

## Hardware Principles
*   **Simplicity & Repairability:** Prefer simple, repairable and understandable hardware.
*   **Experimental Validation:** Validate hardware assumptions experimentally before committing to a design.
*   **Compact & Approachable:** Keep the eventual device compact and approachable rather than turning it into a miniature smartphone.
*   **Enclosure Concept:** The physical design may use a small CNC-machined plywood enclosure with clear acrylic/perspex layers, but this is an enclosure concept rather than a final design decision.
*   **Standards-Based:** Standard connectors and replaceable external antennas are desirable.
*   **Minimal Complexity:** Avoid unnecessary hardware complexity.

## Safety and Testing Notes
*   **Battery Safety:** Do not make assumptions about the condition or safety of the existing Li-ion battery.
*   **Radio Regulations:** High-gain antennas must be tested with appropriate attention to radio regulations, antenna matching, transmit power and frequency band.
*   **Not for Life-Safety:** The project is currently experimental hardware and is not certified life-safety or emergency-response equipment.

## Current Status
Hardware selection is not final. The immediate goal is to use existing hardware to validate the radio, Reticulum, messaging, discovery and UI concepts before selecting or designing a final PPL node.
