# ISO/IEC 27001:2022 Annex A Gap Assessment

**Organization:** NorthBridge Health Analytics (fictional)
**Scope:** Production SaaS platform and supporting corporate IT environment (see `01-scenario/company-profile.md`)
**Assessed by:** Head of IT/Security (self-assessment)
**Date:** September 2026
**Standard version:** ISO/IEC 27001:2022 Annex A (93 controls across 4 themes)

## 1. Purpose and Method
This assessment evaluates NorthBridge's current information security controls against ISO/IEC 27001:2022 Annex A to identify gaps ahead of a future certification effort, prompted by a customer's contractual requirement for demonstrable security alignment. This is a **gap assessment**, not a certification audit — it is intended to inform a remediation roadmap, not to make a conformance determination.

## 2. Maturity Scale
| Score | Rating | Description |
|---|---|---|
| 0 | Not Implemented | No control in place; no evidence |
| 1 | Ad Hoc / Partial | Control exists informally or inconsistently; not documented |
| 2 | Largely Implemented | Control is implemented and mostly consistent, but lacks full documentation, ownership, or review cadence |
| 3 | Fully Implemented | Control is documented, consistently applied, owned, and periodically reviewed |

**Target maturity** for all applicable controls is set at **3 (Fully Implemented)**, consistent with certification readiness. **Gap** = Target − Current, translated to Low (0-1), Medium (2), High (3).

## 3. Summary Results

| Theme | # Controls | Applicable | Avg. Current Maturity | Controls at Target (3) | Controls with High Gap |
|---|---|---|---|---|---|
| A.5 Organizational | 37 | 36 | 1.1 | 1 | 20 |
| A.6 People | 8 | 8 | 1.1 | 0 | 5 |
| A.7 Physical | 14 | 6 | 1.8 | 2 | 1 |
| A.8 Technological | 34 | 34 | 1.4 | 1 | 12 |
| **Total** | **93** | **84** | **1.3** | **4** | **38** |

**Overall conclusion:** NorthBridge has pockets of reasonable practice (identity/MFA, code review, cloud-native backups) but lacks the documentation, ownership, and review cadence ISO 27001 requires almost everywhere. The organization is best characterized as having *ad hoc, engineer-driven* security rather than a *managed ISMS*. Priority should go to governance foundations (A.5.1-5.8, A.5.31), supplier/incident management (A.5.19-5.30), and technical monitoring/logging (A.8.15-8.16) — these gaps are both high-severity and prerequisites for most other controls.

## 4. Detailed Control Assessment

### A.5 Organizational Controls (37)
| ID | Control | Applicable | Current | Gap | Notes |
|---|---|---|---|---|---|
| A.5.1 | Policies for information security | Y | 1 | High | Information Security Policy drafted (v1.0) but not yet formally reviewed/communicated org-wide |
| A.5.2 | Information security roles and responsibilities | Y | 1 | High | Head of IT covers security part-time; no formal RACI |
| A.5.3 | Segregation of duties | Y | 1 | High | Small team limits segregation; no compensating controls documented |
| A.5.4 | Management responsibilities | Y | 1 | High | No formal management review of security program |
| A.5.5 | Contact with authorities | Y | 0 | High | No documented process for contacting regulators/law enforcement |
| A.5.6 | Contact with special interest groups | Y | 0 | High | No membership in ISACs or security communities |
| A.5.7 | Threat intelligence | Y | 0 | High | No threat intelligence feed or process |
| A.5.8 | Information security in project management | Y | 1 | High | Security considered informally in dev planning, not standardized |
| A.5.9 | Inventory of information and other associated assets | Y | 1 | High | Partial AWS asset list exists; no formal, maintained inventory |
| A.5.10 | Acceptable use of information and other associated assets | Y | 0 | High | No formal Acceptable Use Policy (identified gap, see Finding F-002) |
| A.5.11 | Return of assets | Y | 1 | Medium | Manual, inconsistent offboarding process (see R-006) |
| A.5.12 | Classification of information | Y | 1 | Medium | Informal PHI vs. non-PHI distinction; no formal classification scheme |
| A.5.13 | Labelling of information | Y | 0 | High | No labelling standard applied to documents or data stores |
| A.5.14 | Information transfer | Y | 1 | Medium | TLS used for transfers; no formal data transfer agreement standard |
| A.5.15 | Access control | Y | 2 | Low | Least-privilege intent via Okta groups; not formally documented policy |
| A.5.16 | Identity management | Y | 2 | Low | Okta SSO centralizes identity; joiner/mover/leaver process informal |
| A.5.17 | Authentication information | Y | 2 | Low | MFA enforced; password policy exists but not formally documented |
| A.5.18 | Access rights | Y | 1 | High | No periodic access review process (see R-006, Finding F-001) |
| A.5.19 | Information security in supplier relationships | Y | 1 | High | No formal vendor security review process (see R-004) |
| A.5.20 | Addressing information security within supplier agreements | Y | 1 | High | Standard MSA used; security/BAA terms inconsistent across vendors |
| A.5.21 | Managing information security in the ICT supply chain | Y | 0 | High | No supply chain risk process for software dependencies |
| A.5.22 | Monitoring, review and change management of supplier services | Y | 0 | High | No ongoing vendor monitoring or reassessment cadence |
| A.5.23 | Information security for use of cloud services | Y | 2 | Low | AWS used with IAM controls; no formal cloud security policy |
| A.5.24 | Information security incident management planning and preparation | Y | 0 | High | No documented Incident Response Plan (Finding F-003) |
| A.5.25 | Assessment and decision on information security events | Y | 1 | Medium | Ad hoc triage by IT; no defined severity/escalation criteria |
| A.5.26 | Response to information security incidents | Y | 1 | Medium | Reactive response only; no documented playbooks |
| A.5.27 | Learning from information security incidents | Y | 0 | High | No post-incident review process |
| A.5.28 | Collection of evidence | Y | 0 | High | No forensic evidence handling procedure |
| A.5.29 | Information security during disruption | Y | 1 | Medium | Cloud redundancy provides some resilience; no documented continuity plan |
| A.5.30 | ICT readiness for business continuity | Y | 1 | Medium | Automated backups exist; restore has never been tested (see R-007) |
| A.5.31 | Legal, statutory, regulatory and contractual requirements | Y | 2 | Low | HIPAA obligations understood; no centralized compliance register |
| A.5.32 | Intellectual property rights | Y | 2 | Low | Standard employment/contractor IP assignment clauses in place |
| A.5.33 | Protection of records | Y | 1 | Medium | No formal records retention/protection schedule |
| A.5.34 | Privacy and protection of PII | Y | 1 | High | HIPAA drives PHI handling in practice; no formal privacy program/DPIA process |
| A.5.35 | Independent review of information security | Y | 0 | High | No internal audit or independent review has occurred |
| A.5.36 | Compliance with policies, rules and standards for information security | Y | 1 | High | No compliance monitoring process for internal policy adherence |
| A.5.37 | Documented operating procedures | Y | 1 | High | Some runbooks exist informally in wiki; not standardized or reviewed |

### A.6 People Controls (8)
| ID | Control | Applicable | Current | Gap | Notes |
|---|---|---|---|---|---|
| A.6.1 | Screening | Y | 2 | Low | Background checks performed by HR for new hires; not documented as policy |
| A.6.2 | Terms and conditions of employment | Y | 2 | Low | Confidentiality/security clauses in offer letters; not explicitly security-focused |
| A.6.3 | Information security awareness, education and training | Y | 0 | High | No formal training program exists (see R-002, Finding F-004) |
| A.6.4 | Disciplinary process | Y | 1 | Medium | Covered generally in HR handbook; not security-specific |
| A.6.5 | Responsibilities after termination or change of employment | Y | 1 | High | Manual offboarding, inconsistently followed (see R-006) |
| A.6.6 | Confidentiality or non-disclosure agreements | Y | 2 | Low | NDAs signed at hire; not periodically reaffirmed |
| A.6.7 | Remote working | Y | 1 | High | Fully remote company with no formal remote working / BYOD policy (see R-011) |
| A.6.8 | Information security event reporting | Y | 1 | Medium | Informal Slack-based reporting; no defined channel or SLA |

### A.7 Physical Controls (14)
*Note: NorthBridge is fully remote with no owned office space; several physical controls are only partially applicable and are managed by the shared co-working operator (out of direct control).*
| ID | Control | Applicable | Current | Gap | Notes |
|---|---|---|---|---|---|
| A.7.1 | Physical security perimeters | Partial | 2 | Low | Managed by third-party co-working operator; not independently verified |
| A.7.2 | Physical entry | Partial | 2 | Low | Badge access managed by building operator |
| A.7.3 | Securing offices, rooms and facilities | Partial | 2 | Low | No dedicated secure rooms; shared space only |
| A.7.4 | Physical security monitoring | Partial | 1 | Medium | CCTV managed by operator; no NorthBridge visibility into logs |
| A.7.5 | Protecting against physical and environmental threats | N | N/A | N/A | Cloud infrastructure hosted by AWS; NorthBridge relies on AWS's controls |
| A.7.6 | Working in secure areas | N | N/A | N/A | No secure areas defined; not applicable to remote-first model |
| A.7.7 | Clear desk and clear screen | Y | 1 | Medium | Recommended informally; not enforced or verified for remote workers |
| A.7.8 | Equipment siting and protection | N | N/A | N/A | No owned data center equipment |
| A.7.9 | Security of assets off-premises | Y | 1 | High | Laptops used off-site with inconsistent encryption verification (see R-008) |
| A.7.10 | Storage media | Y | 1 | Medium | No formal removable media handling/disposal standard |
| A.7.11 | Supporting utilities | N | N/A | N/A | Managed by AWS/co-working operator |
| A.7.12 | Cabling security | N | N/A | N/A | Not applicable; cloud/remote model |
| A.7.13 | Equipment maintenance | Y | 2 | Low | Laptops replaced/serviced via IT vendor on request |
| A.7.14 | Secure disposal or re-use of equipment | Y | 1 | Medium | No documented secure wipe/disposal procedure for retired laptops |

### A.8 Technological Controls (34)
| ID | Control | Applicable | Current | Gap | Notes |
|---|---|---|---|---|---|
| A.8.1 | User endpoint devices | Y | 1 | High | Encryption/EDR recommended but not centrally enforced (see R-008) |
| A.8.2 | Privileged access rights | Y | 1 | High | AWS admin/root access not tightly restricted or reviewed |
| A.8.3 | Information access restriction | Y | 2 | Low | Okta groups scope access; formal review cadence missing |
| A.8.4 | Access to source code | Y | 2 | Low | GitHub private repos with branch protection; access review informal |
| A.8.5 | Secure authentication | Y | 3 | None | MFA enforced org-wide via Okta for all critical systems |
| A.8.6 | Capacity management | Y | 2 | Low | AWS auto-scaling in use; no formal capacity planning process |
| A.8.7 | Protection against malware | Y | 1 | High | Endpoint AV inconsistently deployed; no central EDR console |
| A.8.8 | Management of technical vulnerabilities | Y | 1 | High | No formal vulnerability scanning or patch SLA (see R-009) |
| A.8.9 | Configuration management | Y | 1 | High | No infrastructure-as-code baseline enforcement or drift detection (see R-001) |
| A.8.10 | Information deletion | Y | 1 | Medium | No documented data deletion procedure for decommissioned data |
| A.8.11 | Data masking | Y | 0 | High | No data masking used in non-production/analytics environments |
| A.8.12 | Data leakage prevention | Y | 0 | High | No DLP tooling in place |
| A.8.13 | Information backup | Y | 2 | Low | Automated daily backups exist; restore never tested (see R-007) |
| A.8.14 | Redundancy of information processing facilities | Y | 2 | Low | Multi-AZ AWS deployment; no documented failover testing |
| A.8.15 | Logging | Y | 1 | High | CloudTrail enabled but not centrally reviewed or alerted on |
| A.8.16 | Monitoring activities | Y | 1 | High | No SIEM or centralized security monitoring/alerting |
| A.8.17 | Clock synchronization | Y | 2 | Low | AWS-managed NTP used by default across infrastructure |
| A.8.18 | Use of privileged utility programs | Y | 1 | Medium | No restriction/logging of admin utility usage on endpoints |
| A.8.19 | Installation of software on operational systems | Y | 1 | Medium | No software allow-listing or install restriction policy |
| A.8.20 | Networks security | Y | 2 | Low | AWS security groups restrict traffic; no network security policy document |
| A.8.21 | Security of network services | Y | 1 | Medium | Third-party network services (VPN) used without formal review |
| A.8.22 | Segregation of networks | Y | 2 | Low | Prod/staging AWS accounts separated; internal network segmentation limited |
| A.8.23 | Web filtering | Y | 0 | High | No web/DNS filtering for corporate endpoints |
| A.8.24 | Use of cryptography | Y | 1 | High | TLS in transit and AWS default encryption at rest; no documented crypto standard/key management policy |
| A.8.25 | Secure development life cycle | Y | 1 | High | No formalized SDLC with security gates |
| A.8.26 | Application security requirements | Y | 1 | Medium | Security requirements not systematically defined per feature |
| A.8.27 | Secure system architecture and engineering principles | Y | 1 | Medium | Architecture decisions made ad hoc without documented security principles |
| A.8.28 | Secure coding | Y | 1 | High | No secure coding standard or static analysis (SAST) in pipeline |
| A.8.29 | Security testing in development and acceptance | Y | 0 | High | No penetration testing or dedicated security testing performed to date |
| A.8.30 | Outsourced development | N | N/A | N/A | All development performed by internal engineering team |
| A.8.31 | Separation of development, test and production environments | Y | 2 | Low | Separate AWS accounts for staging/production |
| A.8.32 | Change management | Y | 1 | High | No formal change advisory process; deploys approved informally (see R-012) |
| A.8.33 | Test information | Y | 1 | High | Production-like data sometimes used in staging without masking |
| A.8.34 | Protection of information systems during audit testing | Y | 1 | Medium | No formal procedure to protect systems during audit/pen-test activity (not yet needed, no testing performed) |

## 5. Prioritized Remediation Themes
Ranked by combination of gap severity and how many downstream controls depend on them:

1. **Governance foundation** (A.5.1-5.4, A.5.31, A.5.35-5.36) — approve and operationalize the Information Security Policy, assign clear ownership, and establish a management review cadence. Almost everything else depends on this existing first.
2. **Incident management** (A.5.24-5.28) — no Incident Response Plan exists; this is a HIPAA breach-notification exposure, not just a certification gap.
3. **Access governance** (A.5.18, A.6.5, A.8.2) — implement periodic access reviews and tighten privileged/offboarding access; directly addresses R-006.
4. **Vendor risk** (A.5.19-5.22) — formalize vendor security review and BAA coverage; directly addresses R-004.
5. **Security monitoring** (A.8.15-8.16) — centralize logging and alerting; currently the biggest blind spot for detecting the risks in the register (R-001, R-003).
6. **Awareness and training** (A.6.3) — quick win, directly addresses R-002.

Full remediation roadmap with owners and dates is tracked in the risk register (`02-risk-register/risk-register.csv`) and audit findings (`05-audit-findings/`).
