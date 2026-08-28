# Internal Audit Findings

**Organization:** NorthBridge Health Analytics (fictional)
**Audit Type:** Internal self-assessment supporting ISO/IEC 27001:2022 gap assessment
**Period Covered:** September 2026
**Auditor:** Head of IT/Security (self-assessment)
**Format:** Each finding follows the standard Condition / Criteria / Cause / Effect / Recommendation structure used in internal and external audit reporting.

---

## Finding F-001: No Periodic User Access Review Process

| Field | Detail |
|---|---|
| **Finding ID** | F-001 |
| **Related Control(s)** | ISO 27001 Annex A.5.18 (Access rights), A.6.5 (Responsibilities after termination) |
| **Related Risk(s)** | R-006 (Employee Offboarding) |
| **Severity** | High |

**Condition:** No evidence of a periodic (e.g., quarterly) review of user access rights to production systems, AWS, or PHI-containing databases was found. Offboarding is initiated manually via an email from HR to IT, with no checklist tracking or verification of completion.

**Criteria:** ISO/IEC 27001:2022 Annex A.5.18 requires that access rights be reviewed regularly, and A.6.5 requires that access be adjusted or removed upon termination or change of employment in a timely manner. The organization's own Information Security Policy (Section 3.3) requires access revocation within one business day of termination.

**Cause:** No formal, assigned process or tooling exists to review access rights on a recurring basis; offboarding relies on informal, ad hoc communication between HR and IT rather than a defined workflow with sign-off.

**Effect:** Former employees or role-changed staff may retain unnecessary or unauthorized access to systems containing PHI, increasing the risk of unauthorized data access or disclosure, and creating potential HIPAA compliance exposure.

**Recommendation:** Implement a quarterly access review process for all systems in scope, with documented sign-off by system/data owners. Formalize the offboarding process as a shared checklist (e.g., in the HRIS or ticketing system) with a required IT confirmation step, and set a hard SLA of same-business-day access revocation for involuntary terminations.

**Management Response:** *Agreed. IT will implement a quarterly access review beginning Q4 2026 and formalize the offboarding checklist in the ticketing system.*

**Target Remediation Date:** 2026-11-15
**Owner:** Head of IT

---

## Finding F-002: No Formal Acceptable Use Policy

| Field | Detail |
|---|---|
| **Finding ID** | F-002 |
| **Related Control(s)** | ISO 27001 Annex A.5.10 (Acceptable use of information and other associated assets) |
| **Related Risk(s)** | R-011 (Remote Work Environment) |
| **Severity** | Medium |

**Condition:** No Acceptable Use Policy (AUP) exists to define permitted and prohibited use of company systems, data, and personal/unmanaged devices (BYOD) for accessing company resources.

**Criteria:** ISO/IEC 27001:2022 Annex A.5.10 requires rules for the acceptable use of information and associated assets to be identified, documented, and implemented.

**Cause:** Security policy documentation has historically been driven reactively rather than as part of a planned ISMS program; an AUP was not prioritized prior to this assessment.

**Effect:** Employees and contractors lack clear, enforceable guidance on acceptable use of systems and data, increasing the risk of inappropriate data handling, unmanaged device exposure, and inconsistent enforcement in the event of a policy violation.

**Recommendation:** Draft and publish an Acceptable Use Policy covering system use, data handling, BYOD/remote work expectations, and consequences of violation. Require signed acknowledgment from all employees and contractors during onboarding and annually thereafter.

**Management Response:** *Agreed. Draft AUP to be completed alongside the Information Security Policy refresh.*

**Target Remediation Date:** 2026-12-01
**Owner:** Head of IT

---

## Finding F-003: No Documented Incident Response Plan

| Field | Detail |
|---|---|
| **Finding ID** | F-003 |
| **Related Control(s)** | ISO 27001 Annex A.5.24, A.5.25, A.5.26, A.5.27 (Incident management planning, assessment, response, and learning) |
| **Related Risk(s)** | R-001, R-003 (Cloud/PHI-related risks with no defined response path) |
| **Severity** | Critical |

**Condition:** No documented Incident Response Plan exists. Security-relevant events are currently triaged informally by whichever IT staff member is available, with no defined severity classification, escalation path, communication plan, or post-incident review process.

**Criteria:** ISO/IEC 27001:2022 Annex A.5.24 requires the organization to plan and prepare for managing information security incidents, including defined roles, responsibilities, and procedures. Given NorthBridge processes PHI, HIPAA's Security Rule (45 CFR §164.308(a)(6)) similarly requires documented security incident procedures and response/reporting processes.

**Cause:** The organization has not yet invested in formal incident response planning, largely because no significant incident has occurred to date; security process maturity has been reactive rather than proactive.

**Effect:** In the event of a security incident, particularly one involving PHI, the organization risks a delayed, inconsistent, or non-compliant response — including missed HIPAA breach notification deadlines (60 days from discovery), reputational harm, and loss of customer trust.

**Recommendation:** Develop and approve a formal Incident Response Plan defining severity tiers, roles and escalation paths, containment/eradication/recovery procedures, PHI breach notification criteria and timelines, and a mandatory post-incident review for Major/Severe incidents. Conduct at least one tabletop exercise within 90 days of plan approval.

**Management Response:** *Agreed — highest priority given PHI exposure. Plan to be drafted and tabletop-tested before end of Q1 2027.*

**Target Remediation Date:** 2026-11-30 (plan approval); 2027-02-28 (tabletop exercise)
**Owner:** Head of IT

---

## Finding F-004: No Formal Security Awareness Training Program

| Field | Detail |
|---|---|
| **Finding ID** | F-004 |
| **Related Control(s)** | ISO 27001 Annex A.6.3 (Information security awareness, education and training) |
| **Related Risk(s)** | R-002 (Phishing leading to credential theft) |
| **Severity** | Medium |

**Condition:** No formal, recurring security awareness training or phishing simulation program exists. New hires receive general onboarding materials that do not include dedicated security content.

**Criteria:** ISO/IEC 27001:2022 Annex A.6.3 requires personnel to receive appropriate information security awareness, education, and training, and for this to be updated regularly in line with organizational policies and role.

**Cause:** Security training has not been prioritized or budgeted as a standalone program; the organization has relied on technical controls (e.g., MFA) rather than user-focused controls.

**Effect:** Employees may be more susceptible to phishing, social engineering, and unsafe data handling practices, increasing likelihood of credential compromise or accidental PHI disclosure — directly contributing to residual risk R-002.

**Recommendation:** Implement a security awareness training platform with mandatory training at onboarding and annually thereafter, plus phishing simulation exercises at least twice per year with tracked completion and click-rate metrics reported to leadership.

**Management Response:** *Agreed. Vendor evaluation for training platform to begin in Q4 2026.*

**Target Remediation Date:** 2026-12-31
**Owner:** Head of IT

---

## Finding F-005: No Centralized Security Logging or Monitoring

| Field | Detail |
|---|---|
| **Finding ID** | F-005 |
| **Related Control(s)** | ISO 27001 Annex A.8.15 (Logging), A.8.16 (Monitoring activities) |
| **Related Risk(s)** | R-001 (Cloud misconfiguration), R-003 (Insider data exfiltration) |
| **Severity** | High |

**Condition:** AWS CloudTrail logging is enabled but not centrally aggregated, reviewed, or alerted on. No SIEM or equivalent monitoring capability exists across cloud infrastructure or endpoints. Database query-level activity is not logged.

**Criteria:** ISO/IEC 27001:2022 Annex A.8.15 and A.8.16 require event logs to be produced, retained, and regularly monitored to detect anomalous activity, and for monitoring processes to be defined and resourced.

**Cause:** No dedicated security engineering resource has been allocated to build out log aggregation, correlation, or alerting; logging was enabled for basic operational troubleshooting rather than security detection purposes.

**Effect:** The organization has limited ability to detect unauthorized access, data exfiltration, or misconfiguration exploitation in a timely manner, meaning incidents (including those tied to R-001 and R-003) could go unnoticed for an extended period, increasing potential breach impact and delaying legally required notification timelines.

**Recommendation:** Implement centralized log aggregation (e.g., AWS Security Hub / GuardDuty or a lightweight SIEM), define alerting thresholds for high-risk events (e.g., IAM policy changes, unusual data access volume), and assign an on-call owner for triage.

**Management Response:** *Agreed. Will evaluate AWS-native tooling (GuardDuty, Security Hub) as a lower-cost first step before considering a third-party SIEM.*

**Target Remediation Date:** 2027-01-31
**Owner:** Head of IT

---

## Findings Summary

| ID | Title | Severity | Status | Target Date |
|---|---|---|---|---|
| F-001 | No periodic user access review process | High | Open | 2026-11-15 |
| F-002 | No formal Acceptable Use Policy | Medium | Open | 2026-12-01 |
| F-003 | No documented Incident Response Plan | Critical | Open | 2026-11-30 |
| F-004 | No formal security awareness training program | Medium | Open | 2026-12-31 |
| F-005 | No centralized security logging or monitoring | High | Open | 2027-01-31 |
