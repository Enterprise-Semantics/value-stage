# Value Stage

> **Topic:** `concept` (Enterprise-Semantics per-concept repository, ES-ADR-049 + CR-ES-049)
> **Category:** Foundational Concept

## Definition

Foundational reference concept in enterprise architecture. Cross-context applicability across value realization, operational coordination, decision-making, and execution.

Per ES-ADR-031 §4, the 5-category boundary taxonomy anchors this concept: foundational reference or specialization, agentic or autonomous independence, four-state matrix independence, AI-not-required, and cross-context materiality.

## What this repository contains

This repository is a self-contained snapshot of the canonical `Value Stage` concept, mirrored from the central Enterprise-Semantics repositories. It contains:

- The authoritative concept record (`concept.yaml` or `profile.yaml`).
- A conformance test kit with ten boundary tests: five positive conformance cases and five negative rejection cases, each anchored to the five-category taxonomy from ES-ADR-031 §4.
- Six documentation files covering the concept's definition, conformance status, target architectures, capability maturity model, assessment criteria, and measurement indicators.
- Cross-program mappings to the World Semantic Foundation, OpenDEA, and DEA Catalogs (where the concept has material relationships to those authorities).
- Visual diagrams in PlantUML format showing the concept's boundary, relationships, and cardinality.
- Reference examples demonstrating the concept's boundary assertions and conformance levels.

## Repository layout

```
value-stage/
├── concept.yaml            # Authoritative concept record
├── README.md               # This file
├── kit/
│   ├── kit.yaml            # Test kit manifest
│   ├── positive-01.yaml    # Conformance test 1 of 5
│   ├── positive-02.yaml    # Conformance test 2 of 5
│   ├── positive-03.yaml    # Conformance test 3 of 5
│   ├── positive-04.yaml    # Conformance test 4 of 5
│   ├── positive-05.yaml    # Conformance test 5 of 5
│   ├── negative-01.yaml    # Rejection test 1 of 5
│   ├── negative-02.yaml    # Rejection test 2 of 5
│   ├── negative-03.yaml    # Rejection test 3 of 5
│   ├── negative-04.yaml    # Rejection test 4 of 5
│   └── negative-05.yaml    # Rejection test 5 of 5
├── docs/
│   ├── concept.md               # Concept narrative
│   ├── conformance.md           # CI-derived conformance status
│   ├── target-architectures.md  # Where this concept appears in target architectures
│   ├── capability-maturity-model.yaml  # CMM levels (L0 Ad-hoc to L5 Optimizing)
│   ├── assessment.md                  # Maturity assessment criteria
│   └── measurement.md               # KPIs and instrumentation
├── mappings/
│   ├── wsf.yaml               # World Semantic Foundation mapping
│   ├── opendea.yaml           # OpenDEA mapping (where material)
│   └── dea-catalogs.yaml      # DEA Catalogs mapping (where material)
├── visuals/
│   └── value-stage/                 # Concept-specific PlantUML diagrams
└── examples/
    └── value-stage/                 # Concept-specific reference examples
```

## Author

Emmanuel A. Otchere (cardinal author rule, 2026-09-24)

## Provenance

- Decision: ES-ADR-049 + ES-ADR-031
- Implementation: CR-ES-049 + CR-ES-031
- Date: 2026-09-30
- Governance: enterprise-semantics
- Synchronization: This repository is a CI-derived snapshot of the canonical central repositories. The single source of truth remains the `Enterprise-Semantics/enterprise-semantics-*` repository family. Use the `sync-concept-repos` workflow in `Enterprise-Semantics/.github` to refresh after canonical updates.
