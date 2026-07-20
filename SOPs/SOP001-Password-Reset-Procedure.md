# SOP 001 – Password Reset Procedure

---

# Purpose

This Standard Operating Procedure (SOP) explains the process for securely resetting a user's Active Directory password while following organizational security policies and ITIL best practices.

---

# Scope

Applicable to all Service Desk (L1) engineers responsible for handling password reset requests for Active Directory users.

---

# Prerequisites

- Access to Active Directory Users and Computers (ADUC)
- User identity verification completed
- ServiceNow request or incident created
- Appropriate permissions to reset passwords

---

# Identity Verification

Before resetting any password, verify the user's identity using approved methods such as:

- Employee ID
- Manager Name
- Registered Mobile Number
- Security Questions (if applicable)

**Never reset a password without completing identity verification.**

---

# Procedure

## Step 1 – Receive Request

- Log the request in ServiceNow.
- Confirm the user's issue.

---

## Step 2 – Verify Identity

Validate the user's identity according to company security policy.

If verification fails:

- Do not proceed.
- Escalate according to security procedures.

---

## Step 3 – Open Active Directory

Launch:

**Active Directory Users and Computers (ADUC)**

Locate the user's account.

---

## Step 4 – Reset Password

Right-click the user account.

Select:

**Reset Password**

Assign a temporary password that complies with the organization's password policy.

---

## Step 5 – Require Password Change

Enable:

✔ **User must change password at next logon**

Unlock the account if it is locked.

---

## Step 6 – Communicate Securely

Provide the temporary password only through an approved communication channel.

Never send passwords through unsecured email or public chat.

---

## Step 7 – Verify Login

Confirm the user can:

- Log in to Windows
- Access Outlook
- Connect to VPN (if applicable)
- Access Microsoft 365 resources

---

## Step 8 – Update ServiceNow

Document:

- Identity verification completed
- Password reset performed
- Temporary password issued securely
- User confirmed successful login

Close the request.

---

# Security Best Practices

- Never disclose passwords to unauthorized individuals.
- Never reuse old passwords.
- Follow the principle of least privilege.
- Lock the workstation when leaving your desk.
- Record all actions in ServiceNow.

---

# Common Issues

| Issue | Resolution |
|--------|------------|
| Account Locked | Unlock account before login |
| Password Expired | Reset password |
| VPN Authentication Failure | Clear cached credentials and retry |
| Outlook Prompts for Password | Update stored credentials |

---

# Escalation Criteria

Escalate to L2 if:

- Active Directory is unavailable.
- Password reset permissions are missing.
- Account is disabled due to HR action.
- Identity cannot be verified.
- Security policy prevents password reset.

---

# Estimated Completion Time

10–20 Minutes

---

# Related Technologies

- Active Directory
- ServiceNow
- Windows 11
- Microsoft 365
- Cisco AnyConnect VPN

---

# Version History

| Version | Date | Author | Changes |
|----------|------|--------|---------|
| 1.0 | July 2026 | Service Desk | Initial Release |
