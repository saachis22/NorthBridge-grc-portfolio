# Company Profile: NorthBridge Health Analytics (Fictional)

> **Disclaimer:** NorthBridge Health Analytics is a fictional company created for this self-directed GRC portfolio project. No real organization, employees, or data are represented. All findings, scores, and figures are illustrative.

## Overview
| Attribute | Detail |
|---|---|
| Industry | Healthcare data analytics (SaaS) |
| Size | ~140 employees |
| Headquarters | Austin, TX (fictional) |
| Customers | Regional hospital networks and outpatient clinics |
| Core product | Cloud platform that ingests, analyzes, and reports on de-identified and identifiable patient data for clinical outcome trends |
| Data handled | Protected Health Information (PHI), employee PII, payment data for billing |
| Infrastructure | AWS (multi-account), Google Workspace, Okta SSO, Salesforce, Snowflake, GitHub |
| Regulatory drivers | HIPAA/HITECH, state breach notification laws, customer contractual security requirements |
| Compliance maturity | Early — no formal ISMS; ad hoc policies; first-time gap assessment |

## Why This Scenario
Healthcare data analytics gives a realistic mix of:
- Sensitive regulated data (PHI) driving risk severity
- A cloud-native, SaaS environment (common in real GRC work)
- Third-party/vendor exposure (subprocessors, cloud provider, EHR integrations)
- A believable reason for the company to be starting its first ISO 27001 gap assessment (a hospital customer is requiring evidence of an information security program before renewing a contract)

## Organizational Context (used throughout the portfolio)
- **CISO / Security Lead:** Vacant — currently covered by the Head of IT (part-time on security)
- **IT team:** 4 engineers, no dedicated security engineer
- **Development:** 20 engineers, ships weekly to AWS via CI/CD (GitHub Actions)
- **Trigger for this project:** A hospital customer's procurement team requested a completed security questionnaire and evidence of alignment to ISO 27001 as a condition of contract renewal.

## Scope for This Portfolio
The assessment scope covers the **production SaaS platform and supporting corporate IT environment**, specifically:
- Cloud infrastructure (AWS production and staging accounts)
- Application source code and CI/CD pipeline
- Corporate endpoints, identity, and email (Google Workspace, Okta)
- Third-party vendors with access to PHI or the production environment

Out of scope: physical offices (fully remote company), M&A activity, subsidiaries (none).

## How to Use This Repo
Every artifact in this repository references NorthBridge Health Analytics so the portfolio reads as one coherent engagement rather than disconnected templates. Suggested reading order:

1. `01-scenario/company-profile.md` — this file
2. `02-risk-register/` — risk methodology + register
3. `03-policy/` — Information Security Policy
4. `04-gap-assessment/` — ISO 27001 Annex A gap assessment + Statement of Applicability
5. `05-audit-findings/` — audit-style findings derived from the gap assessment
6. `06-control-mapping/` — ISO 27001 to NIST CSF crosswalk
7. `07-executive-summary/` — leadership-facing summary of the above
