# 📄 Security-Policy-Library

> **IT Security Policy Library & Network Documentation**  
> A professional collection of IT security policies, standards, and network architecture documentation — mapped to PCI DSS, ISO 27001, NIST CSF, and SOX compliance requirements.

---

## 📌 Project Overview

Security policies are the foundation of any organisation's security programme. Without clear, enforceable policies, technical controls alone cannot ensure compliance or consistent security behaviour. This repository demonstrates the ability to:

- **Write professional IT security policies** aligned to industry standards
- **Map policies to compliance frameworks** (PCI DSS, ISO 27001, SOX, NIST CSF)
- **Produce network architecture documentation** per security best practices
- **Develop security awareness training material** for non-technical staff

All policies follow a consistent structure aligned to how real organisations produce governance documentation.

---

## 📂 Repository Structure

```
Security-Policy-Library/
├── README.md                              ← You are here
├── compliance_reference_guide.md          ← Which policies satisfy which frameworks
│
├── /policies
│   ├── 01_acceptable_use_policy.md
│   ├── 02_password_policy.md
│   ├── 03_incident_response_policy.md
│   ├── 04_remote_access_policy.md
│   ├── 05_data_classification_policy.md
│   ├── 06_vulnerability_management_policy.md
│   └── 07_access_control_policy.md
│
├── /diagrams
│   ├── network_architecture.png           ← Full network diagram
│   ├── network_architecture.drawio        ← Editable source file
│   ├── security_zones_overview.png        ← DMZ, internal, external zones
│   └── data_flow_diagram.png              ← Sensitive data flows (PCI scope)
│
├── security_awareness_training.md         ← Training module for staff
└── policy_review_schedule.md             ← Annual review calendar
```

---

## 📋 Policy Library

Each policy follows this standard structure:

> **Purpose → Scope → Policy Statements → Roles & Responsibilities → Enforcement → Compliance Mapping → Review Cycle**

### Policies Included

| # | Policy | Key Frameworks |
|---|--------|---------------|
| 01 | Acceptable Use Policy | ISO A.6.2.1, CIS-4 |
| 02 | Password Policy | PCI DSS 8.3, ISO A.9.4.3, NIST 800-63B |
| 03 | Incident Response Policy | NIST 800-61, ISO A.16.1, PCI DSS 12.10 |
| 04 | Remote Access Policy | PCI DSS 8.4 (MFA), ISO A.6.2.2 |
| 05 | Data Classification Policy | PCI DSS 3.1, ISO A.8.2 |
| 06 | Vulnerability Management Policy | PCI DSS 6.3, ISO A.12.6 |
| 07 | Access Control Policy | PCI DSS 7, ISO A.9.1, SOX CC6.1 |

---

## 📄 Sample Policy Snapshot — Password Policy

```
Policy:       Password Policy
Version:      1.2
Owner:        IT Security Team
Effective:    January 2024
Review Date:  January 2025
```

**Key Requirements:**

| Requirement | Standard |
|-------------|---------|
| Minimum 12 characters | NIST SP 800-63B |
| Complexity: upper, lower, number, symbol | PCI DSS Req 8.3.6 |
| No reuse of last 10 passwords | PCI DSS Req 8.3.7 |
| MFA required for all remote access | PCI DSS Req 8.4.2 |
| Privileged accounts: 90-day rotation | ISO A.9.4.3 |
| Service accounts: reviewed annually | SOX ITGC CC6.2 |

---

## 🌐 Network Architecture

The network diagram (`/diagrams/network_architecture.png`) illustrates a security-zoned network aligned to **defence-in-depth** principles.

### Security Zones

```
[ Internet ]
     │
     ▼
[ Perimeter Firewall + IDS/IPS ]
     │
     ├──▶ [ DMZ Zone ]
     │        ├── Web Application Server
     │        ├── Email Gateway / Anti-spam
     │        └── Reverse Proxy
     │
[ Internal Firewall ]
     │
     ├──▶ [ Corporate Network — VLAN 10 ]
     │        ├── User Workstations
     │        ├── File Server
     │        └── Print Server
     │
     ├──▶ [ Server Network — VLAN 20 ]
     │        ├── Domain Controller (Active Directory)
     │        ├── Application Server
     │        └── Database Server (PCI DSS Scope)
     │
     ├──▶ [ Security Network — VLAN 30 ]
     │        ├── SIEM / Wazuh
     │        ├── Vulnerability Scanner
     │        └── Log Aggregation
     │
     └──▶ [ Management VLAN — VLAN 99 ]
              └── Admin Workstations (Jump Hosts Only)
```

This architecture supports:
- **Network segmentation** (PCI DSS Req 1.3)
- **DMZ isolation** of public-facing services
- **Dedicated management VLAN** for privileged access
- **SIEM visibility** across all segments

---

## 🎓 Security Awareness Training

`security_awareness_training.md` is a structured training module covering 4 topics employees most commonly fail on:

| Module | Topics Covered |
|--------|---------------|
| **1 — Phishing** | Red flag identification, hover-check technique, reporting procedure |
| **2 — Password Hygiene** | Password manager usage, what makes a strong passphrase |
| **3 — Social Engineering** | Vishing, pretexting, tailgating awareness |
| **4 — Incident Reporting** | What to report, how to report it, why it matters |

Each module includes a **"What would you do?"** scenario to reinforce learning without requiring a testing platform.

---

## 🗂️ Compliance Reference Guide

`compliance_reference_guide.md` maps each policy to the specific controls it satisfies:

| Framework | Controls Addressed by This Policy Library |
|-----------|------------------------------------------|
| **PCI DSS v4.0** | Req 1.3, 3.1, 6.3, 7, 8.3, 8.4, 10.2, 12.10 |
| **ISO 27001:2022** | A.5.1, A.6.2, A.8.2, A.9.1, A.9.4, A.12.6, A.16.1 |
| **NIST CSF 2.0** | GV.PO-01, PR.AC-1, PR.AC-5, RS.CO-1 |
| **SOX ITGC** | CC6.1, CC6.2, CC7.1, CC7.2, CC9.1 |
| **CIS Controls v8** | CIS-3, CIS-4, CIS-5, CIS-6, CIS-17 |

---

## 🔄 Policy Review Schedule

Policies are reviewed on an annual cycle (or following significant incidents or regulatory changes):

| Policy | Last Review | Next Review | Trigger |
|--------|-------------|-------------|---------|
| All policies | Jan 2024 | Jan 2025 | Annual |
| Remote Access | Jan 2024 | Immediately if: new VPN deployed | Event-based |
| IR Policy | Jan 2024 | After any major incident | Event-based |

---

## 🎯 Skills Demonstrated

- ✅ Professional security policy writing and documentation
- ✅ Multi-framework compliance mapping (PCI DSS, ISO 27001, NIST, SOX)
- ✅ Network architecture diagramming and security zone design
- ✅ Security awareness training development
- ✅ Governance, Risk & Compliance (GRC) documentation skills
- ✅ Clear communication of technical requirements to non-technical audiences

---

## 📖 References

- [SANS Information Security Policy Templates](https://www.sans.org/information-security-policy/)
- [NIST SP 800-63B — Digital Identity Guidelines](https://pages.nist.gov/800-63-3/sp800-63b.html)
- [PCI DSS v4.0 Requirements](https://www.pcisecuritystandards.org/document_library)
- [ISO/IEC 27001:2022 Annex A](https://www.iso.org/standard/27001)
- [CIS Controls v8](https://www.cisecurity.org/controls/v8)

---

*Built as part of a cybersecurity portfolio demonstrating policy development, compliance mapping, and security documentation skills aligned to enterprise security governance requirements.*
