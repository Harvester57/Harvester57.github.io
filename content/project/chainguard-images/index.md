---
title: "chainguard-images"
summary: "A collection of secure, minimal, and zero-CVE distroless Docker images hardened for production workloads."
tags:
  - Docker
  - Container security
  - Chainguard
  - Distroless
  - DevSecOps
  - Systems administration
date: 2024-05-25
featured: true
image:
  filename: featured.png
  focal_point: Smart
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Harvester57?tab=repositories&q=chainguard
---

**chainguard-images** is a curated collection of secure, minimal, and production-ready container images built on top of Chainguard's distroless base images (Wolfi/Apko). By stripping out unnecessary tools, shells, package managers, and libraries, these images achieve an extremely small footprint and approach a **Zero-CVE** status by design.

This collection packages various applications and language runtimes, ensuring secure-by-default execution in modern container orchestration stacks.

### Security Benefits of Distroless

*   **Minimizing Attack Surface:** Removing standard shell binaries (`/bin/sh`, `/bin/bash`) and diagnostic tools prevents attackers from executing arbitrary commands upon compromise.
*   **Vulnerability reduction:** Eliminating unused packages results in container images that trigger fewer CVE alerts in security scanners.
*   **Secure Ingestion:** Optimized for high-assurance and air-gapped container registries that require signed, low-overhead artifacts.
*   **Reproducible Builds:** Compiled using secure and verifiable declarative build files.
