# Copilot Instructions for Architecture Codebase

## Overview
This repository contains PlantUML diagrams modeling the architecture of Kiwibank's platforms, infrastructure, and network. The structure is organized by domain (AI, Capability, Compute, Network, Security), with each folder containing `.puml` files for specific systems, flows, or patterns.

## Key Structure & Patterns
- **PlantUML is the primary format**: All architecture artifacts are `.puml` files. Use PlantUML syntax and leverage includes for AWS, Azure, Kubernetes, and other libraries as seen in existing files.
- **Domain-based organization**: Each top-level folder (e.g., `AI/`, `Network/`, `Security/`) represents a major architectural domain. Subfolders (like `Network/Patterns/`) capture reusable patterns.
- **Component and Flow Modeling**: Diagrams model both static structure (components, boundaries) and dynamic flows (e.g., ingress, API calls). See `Network/Akamai Ingress flows.puml` for flow examples.
- **Integration Points**: External services (AWS, Azure, Akamai, Redshield, Infoblox, etc.) are modeled explicitly using PlantUML includes and custom sprites.
- **Naming conventions**: Use clear, descriptive names for components and flows. Follow the style in `AI/AI-Platform-Arch.puml` and `Network/Akamai Ingress.puml`.

## Developer Workflows
- **No build/test automation**: This repo is documentation/diagram only. No code compilation or automated tests are present or required.
- **To view or edit diagrams**: Use a PlantUML-compatible editor or VS Code extension. Render `.puml` files to PNG/SVG for sharing.
- **Adding new diagrams**: Place new `.puml` files in the appropriate domain folder. Reuse includes and patterns where possible.
- **Extending patterns**: Add reusable patterns to subfolders like `Network/Patterns/`.

## Project-Specific Conventions
- **Always use `@startuml`/`@enduml`** in diagrams.
- **Use `!include` for shared libraries** (see top of most `.puml` files).
- **Document flows with clear PlantUML arrows and labels** (see `Akamai Ingress flows.puml`).
- **Keep diagrams concise**: Prefer multiple focused diagrams over one large, complex file.

## Key Files
- `AI/AI-Platform-Arch.puml`: AI platform architecture, integration with cloud and SaaS.
- `Network/Akamai Ingress.puml` & `Akamai Ingress flows.puml`: Ingress architecture and request flows.
- `Network/DNS Topology.puml`: DNS and zone management structure.
- `Network/Patterns/`: Reusable network patterns.

## External Dependencies
- PlantUML libraries: AWS, Azure, Kubernetes, Office, etc. (see `!include` lines in diagrams).

---
For questions or to propose new conventions, contact the architecture team or add a note to this file.
