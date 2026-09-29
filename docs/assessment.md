# Assessment Methodology ; Value Stage

> Per ES-ADR-049 §2.7. How to assess an instance against the capability maturity model.

## 1. Assessment Scope

Assessment evaluates an instance of value stage against the 5-level Capability Maturity Model defined in `capability-maturity-model.yaml`.

**Scope:** Single instance of value stage operating within a defined organizational boundary.

**Out of scope:** Cross-instance comparison (use measurement.md for that).

## 2. Assessor Qualifications

An assessor MUST have:

- Completed the ES-049 Assessment Training (8 hours, recorded)
- Demonstrated competency on 3+ prior assessments
- No current operational role in the instance being assessed

## 3. Evidence Required per Level

Per `capability-maturity-model.yaml`, each level requires specific evidence:

| Level | Evidence type | Minimum quantity |
|-------|---------------|------------------|
| 0 (Ad-hoc) | None required | 0 |
| 1 (Aware) | Document references + stakeholder confirmation | 1 doc + 1 interview |
| 2 (Defined) | Canonical docs + 5+ passing positive tests | 1 canonical + 5 tests |
| 3 (Implemented) | Production implementation + 10 negative tests + measurement | 2+ contexts + 10 tests + 1 measurement plan |
| 4 (Adaptive) | Optimization evidence + cross-context learning | 2+ optimizations + 1+ cross-context output |

## 4. Conformance Gating

A level is achieved only when ALL evidence criteria are met. Gating:

- Cannot skip levels (must pass through sequentially)
- Level 2 is the minimum for ES-049 conformance
- Level 4 is required for ES-049 reference conformance

## 5. Assessment Process

1. **Scoping:** Define the instance boundary + assessment window (default 6 months)
2. **Evidence collection:** Gather all required artefacts per target level
3. **Independent review:** Second assessor cross-checks evidence
4. **Decision:** Unanimous agreement on level achieved
5. **Reporting:** Assessment report archived in `assessments/<org>/<instance>-<date>.md`

## 6. Re-assessment Cadence

| Level achieved | Re-assessment frequency |
|----------------|--------------------------|
| Level 2 (Defined) | Annual |
| Level 3 (Implemented) | Annual + on material change |
| Level 4 (Adaptive) | Biennial + on material change |

## 7. Dispute Resolution

Disputes between assessors resolved by:

1. Written rationale exchange
2. Independent third assessor review
3. Governance committee final decision (governance@enterprise-semantics.org)
