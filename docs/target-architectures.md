# Target Architectures ; Value Stage

> Per ES-ADR-049 §2.6. Each concept has 3 reference target architectures at increasing scales.

## 1. Small-scale: Single Team / Single Value Stream

**Scope:** A single team operating one value stream with one or more instances of value stage.

**Actors:**
- One team owner (decision authority)
- 1-10 individual contributors (execution)
- One observer / reviewer (oversight)

**Boundary interfaces:**
- Team-to-customer (delivery)
- Team-to-supplier (intake)
- Team-to-governance (compliance)

**Evidence of concept instantiation:**
- At least one explicit definition document referencing value stage
- Documented boundary assertions (per ES-ADR-001 §4)
- Local conformance to 5 positive invariants

**Known limitations:**
- No cross-team coordination patterns
- No enterprise-level visibility
- Limited scale (single team)

## 2. Medium-scale: Single Organization

**Scope:** A single organization operating multiple value streams, each potentially instantiating value stage.

**Actors:**
- Multiple team owners
- Cross-functional coordination roles
- Organizational governance bodies

**Boundary interfaces:**
- Inter-team coordination
- Org-to-customer ecosystems
- Org-to-supplier networks
- Org-to-regulatory

**Evidence of concept instantiation:**
- Documented instantiation in 2+ value streams
- Cross-stream consistency per CMM Level 2 (Definition)
- Organizational conformance baseline

**Known limitations:**
- No multi-org coordination
- No ecosystem-level emergence patterns
- Single legal entity

## 3. Large-scale: Multi-Organization / Ecosystem

**Scope:** Multiple organizations forming an ecosystem where value stage emerges across organizational boundaries.

**Actors:**
- Multiple org-level governance bodies
- Ecosystem coordination authority
- Multi-jurisdiction compliance

**Boundary interfaces:**
- Inter-org value streams
- Ecosystem-to-market
- Ecosystem-to-regulatory (multi-jurisdiction)

**Evidence of concept instantiation:**
- Documented instantiation across 3+ organizations
- Ecosystem-level conformance per CMM Level 3+ (Implementation)
- Cross-org measurement and reporting

**Known limitations:**
- Coordination overhead
- Jurisdictional conflict potential
- Emergent behavior complexity

## Selection Guidance

| Scale | When to use | Minimum org size |
|-------|-------------|-------------------|
| Small | Pilot, single-team deployment, proof of value | 1 team (1-10 people) |
| Medium | Production roll-out, multi-team coordination | 1 org (50+ people) |
| Large | Ecosystem, multi-org, cross-jurisdiction | 3+ orgs (500+ people) |
