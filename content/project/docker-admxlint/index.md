---
title: "docker-admxlint"
summary: "A CI/CD-ready Docker image wrapping the admx-lint utility to validate Windows GPO ADMX/ADML templates against official XSD schemas."
tags:
  - Docker
  - Container
  - ADMX
  - GPO
  - Linter
  - DevSecOps
date: 2024-05-26
featured: true
image:
  filename: featured.png
  focal_point: Smart
links:
  - icon: github
    icon_pack: fab
    name: Code
    url: https://github.com/Harvester57/docker-admxlint
---

**docker-admxlint** packages the C++ `admx-lint` validator tool into a lightweight, CI/CD-ready Docker image. This container allows system administrators and policy engineers to validate custom Administrative Templates (`.admx`) and language resource files (`.adml`) against official Microsoft XML Schema Definitions (XSD) without having to manually build or run dependencies locally.

It is particularly useful for pipeline automation when building custom GPO baselines.

### Key Use Cases & Features

*   **Schema Compliance:** Verifies namespace structures, element definitions, and category mappings against official Group Policy schemas.
*   **Pipeline Integration:** Easily integrate ADMX lint checks into GitHub Actions, GitLab CI, or custom DevSecOps pipelines.
*   **Zero Local Setup:** Eliminates the need to configure build environments or C++ compilers on local development workstations.

### Quick Usage

Run the linter on your ADMX files by mounting your templates folder into the container:

```bash
docker run --rm -v $(pwd)/policies:/workspace harvester57/docker-admxlint:latest /workspace
```
