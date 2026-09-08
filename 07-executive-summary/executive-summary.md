# Executive Summary: Information Security Gap Assessment

**Organization:** NorthBridge Health Analytics (fictional)
**Prepared for:** CEO and Leadership Team
**Prepared by:** Head of IT/Security
**Date:** September 2026
**Purpose:** Summarize the results of NorthBridge's first ISO/IEC 27001:2022 gap assessment, prompted by a hospital customer's contract renewal requirement for demonstrable information security practices.

---

## 1. Bottom Line
NorthBridge has good technical instincts in a few areas — company-wide MFA, cloud-native backups, and code review discipline — but **lacks the formal governance, documentation, and monitoring that ISO 27001 and our customers expect.** Of 93 Annex A controls assessed, only 1 is fully implemented; 59 are partially in place; 26 are not implemented at all. This is a normal starting point for a company at our stage, but it means real work is needed before the next customer renewal cycle, and some gaps carry real regulatory (HIPAA) exposure today — not just a certification risk.

## 2. Top 3 Risks to the Business
| # | Risk | Why It Matters | Current Status |
|---|---|---|---|
| 1 | **No Incident Response Plan** (Finding F-003) | If a security incident occurs — especially one involving patient data — we have no defined process for containment, notification, or recovery. HIPAA requires breach notification within 60 days of discovery; without a plan, we risk missing that window entirely. | Critical — no plan exists |
| 2 | **Cloud misconfiguration exposure** (Risk R-001) | Our production AWS environment relies on manual quarterly reviews rather than automated monitoring, and we have no centralized security logging (Finding F-005). A misconfiguration or intrusion could go undetected for weeks. | High — residual risk score 15/25 |
| 3 | **Inconsistent offboarding / access control** (Risk R-006, Finding F-001) | Former employees may retain system access longer than they should, due to a manual, inconsistently followed offboarding process. This is exactly the kind of gap customer security questionnaires ask about directly. | Medium-High — residual risk score 8/25 |

## 3. What's Already Working
- **Multi-factor authentication is enforced company-wide** via Okta — this is our strongest control today and covers a large share of real-world attack scenarios.
- **Code review and branch protection** are consistently applied in engineering, reducing the risk of unreviewed changes reaching production.
- **Automated cloud backups** run daily, giving us a baseline recovery capability (though untested — see below).
- We now have a **documented risk register, security policy draft, and this gap assessment** — the foundation needed to run a real security program going forward, rather than an ad hoc one.

## 4. Recommended Priorities (Next 2 Quarters)
1. **Approve and formally launch the Information Security Policy** (already drafted) — everything else depends on having an approved governance baseline.
2. **Build and tabletop-test an Incident Response Plan** — highest-severity gap given our PHI exposure; target completion by end of Q1 2027.
3. **Stand up basic centralized logging/alerting** using AWS-native tools (GuardDuty, Security Hub) — a low-cost first step that materially reduces our detection blind spot.
4. **Formalize the offboarding and access review process** — a quick, low-cost fix that closes one of our most customer-visible gaps.
5. **Launch security awareness training** for all staff, including phishing simulations — directly reduces our top human-risk factor.

## 5. What This Means for the Customer Renewal
The requesting hospital customer will likely expect either a completed ISO 27001-aligned questionnaire or a NIST CSF-based response (see `06-control-mapping/`). We are not yet in a position to claim strong alignment, but we can now respond **honestly and specifically** — showing a documented risk register, an approved policy, a real gap assessment, and a committed remediation timeline. This is typically sufficient to satisfy security review teams during a renewal cycle, even ahead of formal certification, provided the remediation commitments are followed through and re-verified at the next review.

## 6. Investment Ask
Closing the highest-priority gaps (Incident Response Plan development, basic security monitoring tooling, and a training platform) is estimated to require **modest tooling spend and a partial-time engineering allocation over the next two quarters** — no full-time security hire is being requested at this stage. A follow-up estimate with specific tooling costs can be provided once vendor evaluation (Section 4, item 3) is complete.

## 7. Next Steps
- Leadership sign-off on the Information Security Policy (target: this month)
- Quarterly review of Critical/High risks with this same reporting format going forward
- Re-run this gap assessment in 6 months to track progress against the 4 fully-implemented-control baseline established here

---
*Supporting detail for every item above is available in the full portfolio: risk register, methodology, policy, gap assessment, Statement of Applicability, audit findings, and NIST CSF mapping.*
