# Password Policy

| Field | Value |
|-------|-------|
| **Policy ID** | POL-002 |
| **Version** | 1.2 |
| **Status** | Active |
| **Owner** | IT Security Team |
| **Effective Date** | 2024-01-01 |
| **Review Date** | 2025-01-01 |
| **Approved By** | [IT Manager Name] |

---

## 1. Purpose

This policy establishes minimum standards for the creation, management, and protection of passwords and authentication credentials used to access organisational systems. Strong authentication is a foundational security control that protects against credential-based attacks, which are the most common initial access vector in security incidents.

---

## 2. Scope

This policy applies to:

- All employees, contractors, consultants, and third-party users
- All systems, applications, and services owned or managed by the organisation
- All authentication methods including passwords, PINs, and passphrases

---

## 3. Policy Requirements

### 3.1 Password Construction

| Requirement | Standard | Rationale |
|-------------|---------|-----------|
| Minimum length — standard accounts | **12 characters** | NIST SP 800-63B baseline; longer passwords are exponentially harder to brute force |
| Minimum length — privileged/admin accounts | **16 characters** | Increased risk of privileged accounts warrants stronger credentials |
| Character complexity | **Uppercase + lowercase + number + symbol** | Required by PCI DSS Req 8.3.6 |
| No reuse | **Last 10 passwords** | Prevents cycling of known-compromised passwords |
| No dictionary words | **Enforced by system where possible** | Dictionary attacks are trivially fast |
| No username in password | **Enforced** | Common pattern easily guessed |

### 3.2 Password Rotation

| Account Type | Maximum Age | Notes |
|-------------|-------------|-------|
| Standard user accounts | 365 days | NIST SP 800-63B recommends rotation only when compromise is suspected; PCI DSS Req 8.3.9 requires max 90 days for non-MFA |
| Privileged / admin accounts | 90 days | Mandatory if MFA is not deployed |
| **All accounts with MFA** | **No mandatory rotation** | NIST recommends removing forced rotation when MFA is in place — reduces password reuse |
| Service accounts | Annual review | Rotate upon personnel change or suspected compromise |
| Shared accounts (if approved) | 90 days | Shared accounts require CISO approval and audit logging |

### 3.3 Multi-Factor Authentication (MFA)

MFA is **mandatory** for all of the following:

- [ ] VPN access
- [ ] Remote Desktop Protocol (RDP) access
- [ ] SSH to production servers
- [ ] Cloud console access (AWS, Azure, GCP)
- [ ] Email access from outside the corporate network
- [ ] Any system containing Confidential or Restricted data
- [ ] All privileged (admin) accounts

**Approved MFA methods (in order of preference):**
1. Hardware security key (FIDO2/WebAuthn) — e.g., YubiKey
2. Authenticator app (TOTP) — e.g., Google Authenticator, Microsoft Authenticator
3. Push notification — e.g., Duo Security
4. SMS one-time password — **only where no other method is possible** (SIM-swap risk)

**Prohibited MFA methods:** Email-based OTP for high-risk systems (phishable).

### 3.4 Account Lockout

| Setting | Value |
|---------|-------|
| Lockout threshold | 10 failed attempts (standard) / 5 (privileged accounts) |
| Lockout duration | 30 minutes (auto-unlock) or manual unlock by IT |
| Observation period | 10 minutes (resets attempt counter) |
| Lockout notification | IT Security alerted for privileged account lockouts |

### 3.5 Password Storage

- Passwords must **never** be stored in plaintext
- Hashing algorithm: **bcrypt, scrypt, or Argon2** for new systems; minimum SHA-256 with salt for legacy (upgrade required within 12 months)
- Passwords must **never** be transmitted in plaintext (HTTPS/TLS required)
- Passwords must **never** be stored in: emails, chat messages, ticketing systems, spreadsheets, or documents

### 3.6 Password Managers

- Use of a corporate-approved password manager is **strongly recommended**
- Approved options: [Insert approved products]
- Password manager master password minimum: 20 characters

---

## 4. Roles and Responsibilities

| Role | Responsibility |
|------|---------------|
| **All users** | Choose strong passwords, protect credentials, report suspected compromise immediately |
| **IT Security** | Define and enforce this policy, review annually, approve exceptions |
| **IT Administration** | Configure systems to enforce technical requirements (GPO, IdP settings) |
| **System Owners** | Ensure applications under their ownership comply with this policy |
| **Managers** | Ensure staff complete security awareness training including password hygiene |

---

## 5. Password Reset Procedure

**Standard password reset:**
1. User initiates reset via self-service portal (if available)
2. Identity verified via MFA before reset is permitted
3. New password cannot match any of the last 10 passwords

**Emergency reset (phone/in-person):**
1. IT helpdesk verifies identity via employee ID and manager confirmation
2. Temporary password issued with forced change on next login
3. Reset event logged in ticketing system

**Suspected compromise:**
1. Immediately disable the account
2. Notify the user via an alternate channel (phone)
3. Follow Incident Response Playbook PB-004 (Unauthorised Access)
4. Reset password + revoke all active sessions/tokens before re-enabling

---

## 6. Enforcement

Violations of this policy may result in disciplinary action up to and including termination, depending on severity and intent. IT Security reserves the right to immediately disable accounts that are confirmed to be compromised or that violate this policy in a way that creates risk to the organisation.

---

## 7. Exceptions

Exceptions to this policy require written approval from the CISO or IT Security Lead. All exceptions must be:
- Documented with business justification
- Time-limited (maximum 90 days per exception)
- Reviewed before renewal
- Recorded in the exception register

---

## 8. Compliance Mapping

| Requirement | Framework Reference |
|-------------|-------------------|
| Unique user IDs | PCI DSS Req 8.2; ISO 27001 A.9.1.1 |
| Password complexity | PCI DSS Req 8.3.6; ISO 27001 A.9.4.3 |
| MFA for remote access | PCI DSS Req 8.4.2; NIST SP 800-63B AAL2 |
| Password history | PCI DSS Req 8.3.7 |
| Account lockout | PCI DSS Req 8.3.4 |
| No plaintext storage | PCI DSS Req 8.3.2; ISO 27001 A.10.1 |
| Service account management | SOX ITGC CC6.2 |

---

## 9. Related Documents

- POL-003 — Incident Response Policy
- POL-004 — Remote Access Policy
- POL-007 — Access Control Policy
- Security Awareness Training — Module 2 (Password Hygiene)

---

*Policy Owner: IT Security Team | Review Cycle: Annual | Next Review: 2025-01-01*
