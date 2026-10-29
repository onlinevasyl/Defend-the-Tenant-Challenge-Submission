# Top 5 Microsoft 365 Security Controls

**Environment:** 100 users, 2 administrators, Microsoft 365 E5/E7

## 1. MFA for All Users

**Why:** Stops credential theft and phishing attacks.

**Implementation:**
- Deploy Conditional Access policies.
- Require Microsoft Authenticator registration for all users.

**Risk Addressed:**
- Password theft
- Credential stuffing
- Phishing attacks

**Tradeoff:**
- Minor user friction during sign-in.

---

## 2. MFA for Admins + Separate Admin Accounts

**Why:** Protects privileged access and reduces the blast radius if an account is compromised.

**Implementation:**
- Create dedicated administrator accounts.
- Require MFA for all privileged roles.
- Roll out to the two administrators first.

**Risk Addressed:**
- Admin account compromise
- Privilege escalation
- Tenant-wide breaches

**Tradeoff:**
- Additional account management overhead.

---

## 3. Block Legacy Authentication

**Why:** Prevents attackers from bypassing MFA using IMAP, POP3, SMTP AUTH, and other legacy protocols.

**Implementation:**
- Review applications and devices for legacy authentication dependencies.
- Create a Conditional Access policy to block legacy authentication.

**Risk Addressed:**
- Password spraying
- MFA bypass attacks
- Credential-based compromise

**Tradeoff:**
- Legacy devices and applications may stop working until upgraded.

---

## 4. Risk-Based Conditional Access

**Why:** Automatically requires MFA when suspicious sign-ins are detected.

**Implementation:**
- Enable Microsoft Entra ID Protection.
- Deploy sign-in risk policies using recommended templates.
- Require MFA for Medium and High-risk sign-ins.

**Risk Addressed:**
- Stolen credentials
- Impossible travel events
- Suspicious login activity

**Tradeoff:**
- Occasional false positives requiring additional verification.

---

## 5. Disable User Consent to Applications

**Why:** Prevents consent phishing and unauthorized application access to organizational data.

**Implementation:**
- Set User Consent to **Do not allow user consent**.
- Require administrator approval for application access.

**Risk Addressed:**
- OAuth consent phishing
- Malicious third-party applications
- Data exfiltration

**Tradeoff:**
- Slower onboarding of new SaaS applications.

---

# Expected Security Outcome

Implementing these controls significantly improves the organization's security posture by:

- Reducing the risk of account compromise.
- Protecting privileged administrative access.
- Eliminating legacy authentication attack paths.
- Detecting and responding to risky sign-ins.
- Preventing unauthorized application access to company data.

These controls provide the highest security impact with relatively low implementation complexity for a 100-user Microsoft 365 environment.
