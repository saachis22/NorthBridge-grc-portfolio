# Control Mapping: ISO/IEC 27001:2022 Annex A → NIST CSF 2.0

**Organization:** NorthBridge Health Analytics (fictional)
**Purpose:** Cross-walk NorthBridge's ISO 27001 Annex A controls to the NIST Cybersecurity Framework (CSF) 2.0 Functions and Categories, so the same control set can be communicated to stakeholders who think in NIST terms (common with U.S. healthcare customers and cyber insurers) without maintaining a second control set.
**Basis:** Mapping reflects the general correspondence published by NIST/ISO crosswalk references; adapted here to NorthBridge's specific control implementation status from the Gap Assessment.

## 1. Why This Matters
NorthBridge is pursuing ISO 27001 alignment because of a customer requirement, but many U.S. healthcare and cyber-insurance counterparts assess vendors using NIST CSF language ("Identify, Protect, Detect, Respond, Recover, Govern"). Rather than running two separate assessments, this mapping lets NorthBridge answer either framework's questionnaire from the same underlying control evidence.

## 2. NIST CSF 2.0 Functions Overview
| Function | Focus |
|---|---|
| **Govern (GV)** | Establish and monitor cybersecurity risk management strategy, roles, and policy |
| **Identify (ID)** | Understand assets, risks, and business context |
| **Protect (PR)** | Implement safeguards for critical services and assets |
| **Detect (DE)** | Identify occurrence of cybersecurity events |
| **Respond (RS)** | Take action on detected incidents |
| **Recover (RC)** | Restore capabilities/services impaired by incidents |

*(Govern was added as a distinct Function in NIST CSF 2.0, released in early 2024, reflecting the same governance emphasis ISO 27001 has long required — a useful talking point in interviews.)*

## 3. Crosswalk Summary

| NIST CSF 2.0 Function | Category (examples) | Mapped ISO 27001 Annex A Controls | NorthBridge Current Maturity |
|---|---|---|---|
| **Govern (GV)** | Organizational Context, Risk Management Strategy, Roles & Responsibilities, Policy, Oversight, Supply Chain Risk Management | A.5.1-5.4, A.5.8, A.5.19-5.22, A.5.31, A.5.35-5.37 | Low — policy exists in draft; no formal governance cadence (Findings F-002, F-003) |
| **Identify (ID)** | Asset Management, Risk Assessment, Improvement | A.5.9, A.5.12, A.8.1, A.5.7, A.5.34 | Low-Medium — partial asset inventory; risk register newly established |
| **Protect (PR)** | Identity Management & Access Control, Awareness & Training, Data Security, Platform Security, Technology Infrastructure Resilience | A.5.15-5.18, A.6.1-6.3, A.8.2-8.5, A.8.9, A.8.13, A.8.24, A.8.31 | Medium — Okta MFA and access controls exist; training and hardening gaps remain (R-002, R-008) |
| **Detect (DE)** | Continuous Monitoring, Adverse Event Analysis | A.8.15, A.8.16, A.5.25 | Low — CloudTrail enabled but not monitored/alerted (Finding F-005) |
| **Respond (RS)** | Incident Management, Analysis, Mitigation, Reporting & Communication | A.5.24-5.28 | Very Low — no formal Incident Response Plan (Finding F-003) |
| **Recover (RC)** | Incident Recovery Plan Execution, Communication | A.5.29-5.30, A.8.13-8.14 | Low-Medium — automated backups exist; restore untested (R-007) |

## 4. Detailed Mapping (Selected High-Priority Controls)
This table focuses on the controls tied to open findings and high/critical risks, since those are what a customer questionnaire or insurer is most likely to probe.

| ISO 27001 Control | NIST CSF 2.0 Function.Category | Related Finding/Risk | Status |
|---|---|---|---|
| A.5.24 Incident management planning | RS.MA (Incident Management) | F-003 | Not Implemented |
| A.5.18 Access rights | PR.AA (Identity Mgmt & Access Control) | F-001, R-006 | Partially Implemented |
| A.6.3 Security awareness training | PR.AT (Awareness & Training) | F-004, R-002 | Not Implemented |
| A.8.15/8.16 Logging & Monitoring | DE.CM (Continuous Monitoring) | F-005, R-001, R-003 | Not Implemented |
| A.5.19-5.20 Supplier relationships | GV.SC (Supply Chain Risk Mgmt) | R-004 | Partially Implemented |
| A.8.13 Information backup | RC.RP (Incident Recovery Plan Execution) | R-007 | Partially Implemented |
| A.5.9 Asset inventory | ID.AM (Asset Management) | (supports all findings) | Partially Implemented |

## 5. How to Use This Mapping
- When responding to a **NIST-framed** customer security questionnaire, locate the relevant CSF Function/Category here and cite the underlying ISO control evidence (policy, gap assessment row, or finding) as support.
- When prioritizing remediation, note that most of NorthBridge's weakest areas cluster in **Govern, Detect, and Respond** — consistent with the audit findings, which is a useful sanity check that the two independent framework views agree on where the real gaps are.
- This mapping should be revisited whenever NorthBridge updates its ISO 27001 gap assessment or Statement of Applicability, to keep both framework views in sync.
