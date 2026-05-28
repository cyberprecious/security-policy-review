# Security Policy Review — MediCare Clinic

**UTIVA Cybersecurity Internship 2026 | Task 5**

---

## Overview

Reviewed and audited the existing security policies at MediCare Clinic, identifying critical gaps and recommending practical improvements to protect patient data and ensure regulatory compliance.

---

## Policy Assessment Summary

| Policy Area | Current State | Status |
|------------|--------------|--------|
| Password Policy | No complexity rules, no expiry | 🔴 Weak |
| Access Control | All staff access all patient records | 🔴 Weak |
| Multi-Factor Authentication | Not implemented anywhere | 🔴 Missing |
| Account Lockout | No lockout policy | 🔴 Missing |
| Data Encryption | HTTP used on internal systems | 🟡 Weak |
| Patch Management | No formal schedule | 🟡 Weak |
| Staff Security Training | No awareness training | 🔴 Missing |
| Incident Response Plan | No formal plan exists | 🔴 Missing |
| Removable Media Policy | USB drives freely used | 🟡 Weak |
| Backup Policy | Manual, inconsistent backups | 🟡 Moderate |

---

## Key Recommendations

### Password Policy
- Minimum 12 characters with complexity requirements
- 90-day password expiry
- No reuse of last 10 passwords
- Deploy a password manager for all staff

### Role-Based Access Control (RBAC)

| Role | Access Granted | Access Restricted |
|------|---------------|------------------|
| Doctor | EMR, patient records, lab results | Billing, admin files |
| Nurse | Vitals, medication records | Full history, billing |
| Admin Staff | Billing, scheduling, insurance | Clinical records |
| Reception | Check-in, appointments | Medical records |
| IT Staff | Network devices, servers | Patient clinical data |

### Multi-Factor Authentication
- Enable MFA on all remote access (VPN, SSH)
- Enable MFA on EMR system for all clinical staff
- Use authenticator apps (Google or Microsoft Authenticator)

### Account Lockout
- Lock after 5 failed login attempts
- 30-minute automatic unlock
- Alert IT administrator on lockout

### Additional Recommendations
- Enforce HTTPS (TLS 1.2+) on all internal systems
- Monthly patch cycle, critical patches within 48 hours
- Mandatory quarterly cybersecurity awareness training
- Disable USB ports on all clinical workstations
- Automate daily backups and test restoration monthly

---

## Files in this Repository

- `security_policy_review.pdf` — Full policy audit document
- `rbac_matrix.md` — Role-based access control matrix
- `recommendations.md` — Detailed improvement recommendations
