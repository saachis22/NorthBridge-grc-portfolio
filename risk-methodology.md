# Risk Assessment Methodology

**Organization:** NorthBridge Health Analytics (fictional)
**Owner:** Head of IT / Security
**Review cycle:** Annually, or upon significant change to systems, vendors, or regulatory requirements

## 1. Purpose
This document defines how risks are identified, scored, and prioritized in the NorthBridge risk register, so that scoring is consistent and repeatable across assessments.

## 2. Risk Scoring Model
NorthBridge uses a simple **5x5 qualitative risk matrix** (Likelihood x Impact), which is fast to apply and easy for non-technical stakeholders to interpret — appropriate for an organization at early compliance maturity.

### 2.1 Likelihood Scale
| Score | Rating | Description |
|---|---|---|
| 1 | Rare | Would only occur in exceptional circumstances (<5% per year) |
| 2 | Unlikely | Could occur at some point (~5-25% per year) |
| 3 | Possible | Might occur at some point (~25-50% per year) |
| 4 | Likely | Will probably occur (~50-75% per year) |
| 5 | Almost Certain | Expected to occur, possibly multiple times (>75% per year) |

### 2.2 Impact Scale
| Score | Rating | Description |
|---|---|---|
| 1 | Negligible | No material impact; internal nuisance only |
| 2 | Minor | Limited operational disruption; no PHI exposure; no reporting obligation |
| 3 | Moderate | Localized PHI exposure or service disruption; contained with existing controls; possible customer notification |
| 4 | Major | Significant PHI breach, extended outage, or regulatory notification required; reputational and financial harm |
| 5 | Severe | Large-scale PHI breach, HIPAA enforcement action, major customer contract loss, existential business impact |

### 2.3 Risk Score and Heat Map
**Risk Score = Likelihood x Impact** (range 1-25)

| | Impact 1 | Impact 2 | Impact 3 | Impact 4 | Impact 5 |
|---|---|---|---|---|---|
| **Likelihood 5** | 5 | 10 | 15 | 20 | 25 |
| **Likelihood 4** | 4 | 8 | 12 | 16 | 20 |
| **Likelihood 3** | 3 | 6 | 9 | 12 | 15 |
| **Likelihood 2** | 2 | 4 | 6 | 8 | 10 |
| **Likelihood 1** | 1 | 2 | 3 | 4 | 5 |

| Risk Level | Score Range | Response Expectation |
|---|---|---|
| Low | 1-4 | Accept; monitor at next review cycle |
| Medium | 5-9 | Mitigate within 6-12 months; owner assigned |
| High | 10-15 | Mitigate within 90 days; monthly tracking |
| Critical | 16-25 | Immediate action plan; weekly tracking; leadership visibility |

## 3. Inherent vs. Residual Risk
- **Inherent risk** is scored assuming no controls are in place.
- **Existing controls** are documented for context.
- **Residual risk** is scored after accounting for existing controls, and is the score used to prioritize treatment.

## 4. Risk Treatment Options
Each risk is assigned one of four treatments:
- **Mitigate** — reduce likelihood and/or impact via additional controls
- **Accept** — retain the risk as-is (requires documented sign-off if residual score >= 10)
- **Transfer** — shift impact via insurance, contractual terms, or outsourcing
- **Avoid** — eliminate the activity or asset causing the risk

## 5. Roles
| Role | Responsibility |
|---|---|
| Risk Owner | Individual accountable for ensuring treatment actions are completed |
| Head of IT/Security | Maintains the register, facilitates scoring, escalates Critical/High risks |
| Leadership Team | Reviews Critical and High risks quarterly; approves risk acceptance |

## 6. Limitations
This is a qualitative model appropriate for a small-to-mid-size organization without a mature GRC function. As NorthBridge matures, this may be replaced with a quantitative model (e.g., FAIR) for higher-value decisions.
