# Measurement Methodology ; Value Stage

> Per ES-ADR-049 §2.7. Quantitative metrics + measurement approach.

## 1. Measurement Scope

Quantitative measurement of value stage instances, supporting CMM level assessment (per assessment.md) and cross-instance comparison.

## 2. Core Metrics

### 2.1 Conformance Metrics

| Metric | Definition | Target |
|--------|-----------|--------|
| Boundary conformance rate | % of instances passing all positive + negative tests | >= 95% at Level 3+ |
| Test pass rate (positive) | # positive tests passing / # positive tests total | = 100% (baseline) |
| Test pass rate (negative) | # negative tests correctly rejecting / # negative tests total | = 100% (baseline) |
| Conformance drift rate | # boundary violations detected post-deployment / quarter | <= 5% at Level 3+ |

### 2.2 Operational Metrics

| Metric | Definition | Target |
|--------|-----------|--------|
| Instantiation count | # of distinct value stage instances | Trending |
| Coverage breadth | # of contexts where value stage applies | Growing |
| Maturity level distribution | # instances at each CMM level | Skewed toward higher levels |
| Time-to-Level-2 | Time from initial awareness to Level 2 conformance | <= 90 days |

### 2.3 Quality Metrics

| Metric | Definition | Target |
|--------|-----------|--------|
| Boundary violation count | # distinct violations per quarter | Decreasing trend |
| Cross-instance consistency | % of shared boundary assertions that align across instances | >= 90% at Level 3+ |
| Documentation completeness | % of required docs present | 100% |

## 3. Measurement Frequency

| Metric category | Frequency |
|-----------------|-----------|
| Conformance | Per-CI-run + quarterly summary |
| Operational | Monthly |
| Quality | Quarterly |

## 4. Instrumentation Requirements

To participate in measurement, an instance MUST expose:

- Conformance test results via standard interface (per ES-ADR-031 §11)
- Instance metadata (org, version, boundary assertions used)
- Boundary violation events (per ES-ADR-049 §2.7)

## 5. Reporting Format

Standard quarterly measurement report includes:

1. Per-metric current value + target
2. Quarter-over-quarter trend
3. Variance flags (metric deviating >= 20% from target)
4. Top 3 boundary violations (by frequency)
5. Top 3 maturity improvements (by level transition)

Reports archived in `measurements/<org>/<quarter>.md`.

## 6. Data Retention

Raw measurement data retained 24 months. Aggregated metrics retained indefinitely for longitudinal analysis.

## 7. Privacy and Confidentiality

Aggregated metrics are public. Per-instance data is confidential and shared only with the instance owner + ES governance.
