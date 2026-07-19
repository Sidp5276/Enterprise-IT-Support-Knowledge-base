# Ticket 025 – New User Account Creation (Onboarding)

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000025 |
| Priority | P3 |
| Category | User Provisioning |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| SLA | 8 Hours |

---

# Request Summary

HR requested creation of a new Active Directory account for a newly hired employee.

---

# Environment

- Windows Server Active Directory
- Microsoft Active Directory Users and Computers (ADUC)
- Microsoft 365 Hybrid Environment

---

# Business Impact

New employee unable to begin work until required accounts and permissions are provisioned.

---

# Provisioning Checklist

✔ User Account Created

✔ Initial Password Assigned

✔ User Must Change Password at Next Logon Enabled

✔ Correct Organizational Unit (OU)

✔ Department Added

✔ Manager Assigned

✔ Required Security Groups Added

✔ Home Drive Configured

✔ Microsoft 365 License Assigned

---

# Implementation Steps

### Step 1

Verified onboarding request approval from HR.

---

### Step 2

Opened Active Directory Users and Computers.

---

### Step 3

Created new user account.

Configured:

- First Name
- Last Name
- Username
- Display Name

---

### Step 4

Assigned temporary password.

Enabled:

✔ User must change password at next logon.

---

### Step 5

Moved user into correct Organizational Unit.

---

### Step 6

Added required security groups.

Examples:

Finance_Users

VPN_Users

Office365_Users

---

### Step 7

Verified successful domain account creation.

---

### Step 8

Shared login credentials securely with HR.

---

# Root Cause Analysis (RCA)

New employee onboarding request completed as per HR approval.

---

# Resolution

Created and configured Active Directory account according to company onboarding standards.

---

# Verification

- Domain Login Successful
- Outlook Ready
- Teams Accessible
- Shared Drives Available
- User Confirmed Successful Login

---

# Escalation Decision

No escalation required.

---

# Preventive Actions

- Use standardized onboarding checklist.
- Verify department and security group assignments.
- Ensure HR approval before account creation.

---

# Tools Used

- Active Directory Users and Computers (ADUC)

---

# Technologies Used

- Active Directory
- Windows Server
- Microsoft 365
- Organizational Units
- Security Groups

---

# Interview Questions

1. How do you create a new user in Active Directory?
2. What is an Organizational Unit (OU)?
3. Why are Security Groups assigned during onboarding?
4. Why should new users change their password at first login?
5. What checks should be completed before closing an onboarding request?

---

# Knowledge Learned

A standardized onboarding process ensures new employees receive the correct access, security group memberships, and resources on their first day while reducing configuration errors.

---

# Ticket Status

Closed

---

# Resolution Time

35 Minutes
