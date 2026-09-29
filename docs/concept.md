# Value Stage Concept

This document is the human-readable companion to the canonical
`ES:CONCEPT:value-stage` concept record.

Per CR-ES-003 §5 + §13 + ADR-ES-003 §13.

## Canonical Definition

A Value Stage is a meaningful transition in the progression of
stakeholder value within a Value Stream.

A Value Stage represents a value-relevant state transition rather than
merely an executable unit of work.

A stage may be realized through:

- one Process
- multiple Processes
- Activities
- Tasks
- Services
- Systems
- human participation
- automated execution

Therefore:

- Value Stage != Process
- Value Stage != Activity
- Value Stage != Task

## Semantic Characteristics

A Value Stage:

1. is meaningful, represents a transition in value progression, not
   merely an executable unit
2. is value-relevant, its input_state and resulting_state describe the
   value progression, not Process input/output
3. is realization-agnostic, may be realized by one or many
   Processes, Services, Systems, etc.
4. is stage-ordered, preceded and followed by other stages within
   its parent Value Stream
5. is capability-dependent, may require one or more Capabilities
6. is outcome-producing, produces an Outcome that contributes to
   stakeholder Value
7. is stakeholder-relevant, serves a stakeholder value contribution
8. is implementation-independent, identity preserved when Processes
   change

## Identity

Canonical identifier: `ES:CONCEPT:value-stage`

WSF grounding: ES-canonical novelty, WSF has no equivalent construct
at Tier 1 or Tier 2. The Value Stage construct is owned by ES.

The Value Stage identifier shall be unique independently of its Process
implementation (per CR-ES-003 §12 VST-ID-002).

## Relationships

Per CR-ES-003 §9 + §10, the 5 Value Stage subject-level predicates are:

| Predicate | Object | Provenance |
|---|---|---|
| precedes | value-stage | CR-ES-003 §10.8 |
| stage-realized-through | external:concept:process | CR-ES-003 §10.9 |
| requires | capability | CR-ES-003 §10.10 |
| stage-produces | external:concept:outcome | CR-ES-003 §10.11 |
| contributes-to | external:concept:stakeholder-value | CR-ES-003 §9 table |

A 6th implicit relationship (belongs-to value-stream, via CR-ES-003 §5)
is captured in concept records but not declared as a top-level
predicate, the containment relationship is held by Value Stream
contains Value Stage (CR-ES-003 §10.2).

## Identity Rules

Per CR-ES-003 §12:

- VST-ID-001: Every Value Stage shall have a unique identifier.
- VST-ID-002: A Value Stage identifier shall be unique independently of
  its Process implementation.
- VST-ID-003: Changing the Process implementing a stage shall not
  inherently change the stage identity.
- VST-ID-004: A Value Stage must belong to at least one Value Stream
  when published as a Value Stream instance.
- VST-ID-005: A stage shall not be identified solely by an
  organizational unit.

## Cardinal rules

- Author: Emmanuel A. Otchere (cardinal author rule, 2026-09-23)
- D-004 dash rule (no en-dash, no em-dash)
- SDO-neutral sourcing (ISO/IEC, ITU-T, ETSI, NIST)
- No vendor-specific material from embargoed sources (cardinal embargo
  2026-09-22)

## See also

- `value-stream.md`, the parent Value Stream concept
- `architecture/value-stream-boundary.md`, semantic boundaries
