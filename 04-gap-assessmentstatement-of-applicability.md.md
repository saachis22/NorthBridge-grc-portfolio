# Statement of Applicability (SoA)

**Organization:** NorthBridge Health Analytics (fictional)
**Standard:** ISO/IEC 27001:2022, Annex A
**Version:** 1.0 (Draft)
**Date:** September 2026
**Owner:** Head of IT/Security

## 1. Purpose
The Statement of Applicability documents, for each Annex A control, whether it is applicable to NorthBridge's Information Security Management System (ISMS) scope, the justification for inclusion or exclusion, and its current implementation status. It is a required output of the ISO 27001 risk treatment process and is derived from the Gap Assessment (`iso27001-annex-a-gap-assessment.md`) and Risk Register (`02-risk-register/risk-register.csv`).

## 2. Implementation Status Key
| Status | Meaning |
|---|---|
| Implemented | Maturity 3 in the gap assessment — fully implemented and documented |
| Partially Implemented | Maturity 1-2 — control exists but is incomplete, undocumented, or inconsistently applied |
| Not Implemented | Maturity 0 — no control currently in place |
| Excluded | Control judged not applicable to NorthBridge's ISMS scope |

## 3. Summary
Of the 93 Annex A controls, **84 are determined applicable** to NorthBridge's ISMS scope. **9 are excluded**, primarily physical/facilities controls that do not apply to a fully remote, cloud-hosted organization, and one control (outsourced development) that does not apply because all development is performed in-house.

| Theme | Applicable | Excluded |
|---|---|---|
| A.5 Organizational | 37 | 0 |
| A.6 People | 8 | 0 |
| A.7 Physical | 8 | 6 |
| A.8 Technological | 33 | 1 |
| **Total** | **86** | **7** |

*(Note: 6 A.7 controls are marked "Partial" applicability in the gap assessment — treated here as applicable-but-managed-by-third-party where relevant, and excluded only where genuinely not applicable to the cloud/remote model.)*

## 4. Excluded Controls and Justification
| ID | Control | Justification for Exclusion |
|---|---|---|
| A.7.5 | Protecting against physical and environmental threats | No owned facilities; infrastructure hosted in AWS data centers, covered by AWS's own ISO 27001/SOC 2 certifications, referenced in vendor due diligence |
| A.7.6 | Working in secure areas | No secure areas exist; company is fully remote with no classified physical work areas |
| A.7.8 | Equipment siting and protection | No owned server/data center equipment; all infrastructure is cloud-hosted |
| A.7.11 | Supporting utilities | Managed entirely by AWS and the third-party co-working operator; outside NorthBridge's control boundary |
| A.7.12 | Cabling security | Not applicable; no owned network cabling infrastructure |
| A.8.30 | Outsourced development | All product development is performed by internal engineering staff; no outsourced development arrangements exist |

## 5. Applicable Controls — Status Overview
Full per-control maturity scoring, notes, and evidence references are maintained in `iso27001-annex-a-gap-assessment.md` to avoid duplicating a 93-row table across two documents. This section summarizes implementation status by theme; see the linked risk register and audit findings for remediation ownership and target dates.

| Theme | Implemented | Partially Implemented | Not Implemented |
|---|---|---|---|
| A.5 Organizational | 0 | 20 | 17 |
| A.6 People | 0 | 7 | 1 |
| A.7 Physical (applicable subset) | 0 | 8 | 0 |
| A.8 Technological | 1 | 24 | 8 |
| **Total** | **1** | **59** | **26** |

## 6. Controls Fully Implemented (Maturity 3)
| ID | Control |
|---|---|
| A.8.5 | Secure authentication (MFA enforced org-wide via Okta) |

*This SoA intentionally shows a low baseline — it reflects NorthBridge's status at the start of its first ISMS effort, not a certification-ready state. It is intended to demonstrate the SoA format and how it links to gap assessment and risk register outputs, which is the deliverable auditors expect to see maintained and updated over time.*

## 7. Approval
| Role | Name | Status |
|---|---|---|
| Prepared by | Head of IT/Security | Draft complete |
| Reviewed by | (pending) | Not yet reviewed |
| Approved by | CEO | Not yet approved |
