# Information Security Policy

| | |
|---|---|
| **Organization** | NorthBridge Health Analytics (fictional) |
| **Document Owner** | Head of IT / Security |
| **Approved By** | Chief Executive Officer |
| **Version** | 1.0 |
| **Effective Date** | 2026-09-01 |
| **Review Cycle** | Annually, or upon material change to systems, regulations, or business operations |
| **Classification** | Internal |

## 1. Purpose
This policy establishes the framework for protecting the confidentiality, integrity, and availability of NorthBridge Health Analytics' information assets, including Protected Health Information (PHI), employee data, and company intellectual property, in line with HIPAA/HITECH requirements and ISO/IEC 27001 principles.

## 2. Scope
This policy applies to:
- All employees, contractors, and interns of NorthBridge Health Analytics
- All information systems owned, operated, or contracted by NorthBridge, including cloud infrastructure (AWS), corporate collaboration tools (Google Workspace), and source code repositories (GitHub)
- All data created, processed, transmitted, or stored on behalf of NorthBridge, including customer PHI

## 3. Policy Statements

### 3.1 Governance
- The Head of IT/Security is accountable for the information security program and reports security posture to the CEO quarterly.
- This policy and its supporting standards must be reviewed at least annually and approved by leadership.
- Security roles and responsibilities must be documented and communicated to relevant personnel.

### 3.2 Risk Management
- Information security risks must be identified, assessed, and tracked in the corporate risk register in accordance with the Risk Assessment Methodology.
- Risks scoring High or Critical must have a documented treatment plan and owner.

### 3.3 Access Control
- Access to systems and data must follow the principle of least privilege.
- All access to production systems and PHI-containing systems requires multi-factor authentication (MFA).
- User access must be reviewed at least quarterly and revoked within one business day of employee termination.
- Shared or generic accounts are prohibited for accessing production systems containing PHI.

### 3.4 Asset Management
- All systems that store, process, or transmit PHI must be identified and recorded in an asset inventory.
- Assets must be classified according to data sensitivity (Public, Internal, Confidential, Restricted/PHI).

### 3.5 Data Protection
- PHI and other Confidential/Restricted data must be encrypted at rest and in transit using industry-standard encryption (e.g., AES-256, TLS 1.2+).
- Data must only be retained as long as necessary to fulfill business or regulatory requirements, per the data retention schedule.
- Production data must not be copied to non-production environments or personal devices without documented approval.

### 3.6 Endpoint and Network Security
- All company-issued laptops must have full-disk encryption, an endpoint detection tool, and automatic OS/security patching enabled.
- Personal or unmanaged devices accessing company systems must comply with the Acceptable Use and BYOD standards (see Section 6).
- Production network access must be restricted using security groups/firewalls following least-privilege principles.

### 3.7 Application and Change Security
- Code changes to production systems require peer review and passing automated tests prior to merge.
- Dependencies must be scanned for known vulnerabilities as part of the CI/CD pipeline.
- Secrets (API keys, credentials) must not be stored in source code or plaintext configuration files.

### 3.8 Third-Party and Vendor Risk
- Vendors with access to PHI or production systems must undergo a security review prior to onboarding and be bound by a signed Business Associate Agreement (BAA) or equivalent data processing terms.
- Vendor security posture must be reassessed at least annually for critical vendors.

### 3.9 Incident Response
- Suspected or confirmed security incidents must be reported to the Head of IT/Security immediately upon discovery.
- Incidents involving PHI must be assessed for breach notification obligations under HIPAA/HITECH and applicable state law.
- A post-incident review must be conducted for all Major or Severe incidents.

### 3.10 Security Awareness
- All personnel must complete security awareness training upon hire and annually thereafter.
- Phishing simulation exercises must be conducted at least twice per year.

### 3.11 Business Continuity
- Critical systems must have automated backups with defined retention periods.
- Backup restoration must be tested at least annually.

## 4. Roles and Responsibilities
| Role | Responsibility |
|---|---|
| CEO | Ultimate accountability for information security program |
| Head of IT/Security | Policy ownership, risk register maintenance, incident response coordination |
| Engineering Lead | Secure development practices, CI/CD security controls |
| HR Manager | Onboarding/offboarding execution, training compliance tracking |
| All Personnel | Compliance with this policy; timely reporting of suspected incidents |

## 5. Exceptions
Any exception to this policy must be documented, include a business justification and compensating control, and be approved by the Head of IT/Security. Exceptions must be reviewed at least annually.

## 6. Related Documents
- Risk Assessment Methodology
- Acceptable Use Policy (referenced, not yet formalized — tracked as a gap; see ISO 27001 Gap Assessment)
- Incident Response Plan (referenced, not yet formalized — tracked as a gap)
- Data Retention Schedule (referenced, not yet formalized — tracked as a gap)

## 7. Enforcement
Violations of this policy may result in disciplinary action up to and including termination of employment or contract, consistent with company HR policy and applicable law.

## 8. Policy Review History
| Version | Date | Description | Author |
|---|---|---|---|
| 1.0 | 2026-09-01 | Initial policy issued ahead of first ISO 27001 gap assessment | Head of IT/Security |
