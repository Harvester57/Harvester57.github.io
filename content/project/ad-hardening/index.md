---
title: "ad-hardening"
summary: "A comprehensive guidebook and template collection for hardening air-gapped Active Directory environments."
tags:
  - Active Directory
  - Directory services
  - Hardening
  - Air-gap
  - Cybersecurity
  - Windows security
date: 2024-05-20
featured: true
image:
  filename: featured.png
  focal_point: Smart
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Harvester57/ad-hardening
---

**ad-hardening** is a comprehensive guidebook and reference repository dedicated to securing and hardening Active Directory (AD) environments in air-gapped, isolated networks. While physical isolation eliminates many remote threats, it places a heavier security premium on internal access control, endpoint hygiene, and physical media management.

This project outlines step-by-step guidance, configurations, and templates to establish a resilient security posture inside sensitive, non-internet-connected directory environments.

### Core Hardening Pillars

*   **Tiered Administrative Model:** Isolating Tier 0 (Domain Controllers/Admins) credentials from Tier 1 (Servers) and Tier 2 (Workstations) to eliminate lateral escalation risks.
*   **Offline Authentication & MFA:** Strategies for deploying local, offline-capable multi-factor authentication without internet-based validation services.
*   **Service Account Securing:** transitioning legacy service accounts to Group Managed Service Accounts (gMSAs) to enforce automatic password rotation.
*   **Audit & Event Analysis:** Configuration templates for offline Windows Event Forwarding (WEF) and local security log auditing.
*   **Removable Media Control:** Hardening USB and other removable hardware access policies via Group Policy Objects (GPOs) to combat sneakernet malware propagation vectors.
