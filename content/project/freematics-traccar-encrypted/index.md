---
title: "freematics-traccar-encrypted"
summary: "A secure UDP telemetry proxy and custom firmware extension enabling encrypted data transmission for Freematics tracking devices."
tags:
  - Telematics
  - IoT security
  - Cryptography
  - GPS tracking
  - Embedded systems
  - Proxy server
date: 2024-05-24
featured: true
image:
  filename: featured.png
  focal_point: Smart
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Harvester57/freematics-traccar-encrypted
---

**freematics-traccar-encrypted** (forked from the original project, now deleted from GitHub) is a custom firmware extension and intermediary proxy designed to secure telematics transmission between Freematics hardware trackers (such as Freematics ONE+) and a Traccar GPS server.

By default, Freematics devices stream vehicle telemetry and GPS data over unencrypted UDP channels because resource-constrained microcontrollers cannot handle the overhead of full TLS handshakes. This project resolves that gap by introducing a lightweight cryptography layer directly onto the device firmware and terminating it via a custom decryption proxy.

### Architecture & Mechanics

*   **Firmware Encryption:** Extends the Freematics `telelogger` sketch with a fast, hardware-friendly symmetric encryption algorithm (ChaCha stream cipher) to secure UDP payloads before transmission.
*   **Decryption Proxy:** A lightweight intermediary service, written in Go, that listens for encrypted telematics packets from the tracker, validates payload integrity, decrypts the contents, and forwards standard unencrypted telematics records to the Traccar backend.
*   **Tamper Prevention:** Protects location coordinates, speed, and OBD-II vehicle diagnostic data against passive eavesdropping and man-in-the-middle spoofing vectors.
