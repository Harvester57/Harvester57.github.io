---
title: "sudo-check"
summary: "A lightweight Linux security auditing tool to analyze and verify sudoers configurations and permissions."
tags:
  - Linux security
  - Privilege escalation
  - Auditing
  - Sudo
  - Cybersecurity
  - Bash scripting
date: 2024-05-21
featured: true
image:
  filename: featured.png
  focal_point: Smart
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Harvester57/sudo-check
---

**sudo-check** is a lightweight security auditing utility designed to analyze Linux `/etc/sudoers` files and `/etc/sudoers.d/` directories. It helps security engineers and system administrators quickly identify misconfigurations, overly permissive rules, and potential privilege escalation pathways.

By scanning for common policy weaknesses, this tool provides actionable insights to tighten system access controls.

### Key Auditing Features

*   **Rule Analysis:** Identifies `NOPASSWD` directives and wildcard user specifications that could allow unauthorized root access.
*   **Directive Validation:** Verifies the presence of key security directives such as `env_reset`, `secure_path`, and `use_pty`.
*   **Permission Checks:** Validates the file permissions and ownership of critical configuration files to prevent unauthorized editing.
*   **Alias Resolution:** Parsers user, run-as, and command aliases to audit complex, nested rule structures.
