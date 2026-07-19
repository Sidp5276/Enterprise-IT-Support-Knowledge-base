# Ticket 023 – User Account Disabled

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000023 |
| Priority | P2 |
| Category | Active Directory |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Sales |
| Device | HP EliteBook 850 G8 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that they were unable to log in to the company laptop.

Error displayed:

> "Your account has been disabled. Please see your system administrator."

---

# Environment

- Windows 11 Enterprise
- Active Directory Domain Services
- Domain Joined Device

---

# Business Impact

- User unable to log in.
- Outlook inaccessible.
- Teams unavailable.
- Daily work interrupted.

---

# Initial Investigation

Collected Information:

- Password reset did not resolve the issue.
- Other users unaffected.
- User recently returned from long leave.

---

# Possible Causes

- HR Offboarding Process
- Manual Account Disable
- Security Policy
- Administrative Error

---

# Troubleshooting Steps

### Step 1

Opened **Active Directory Users and Computers (ADUC).**

---

### Step 2

Located user account.

Observed:

✔ Account Disabled

---

### Step 3

Verified with HR that the employee was active.

HR confirmed employment status.

---

### Step 4

Enabled the account.

Action:

✔ Enable Account

---

### Step 5

Requested user to sign in again.

Login successful.

---

# Root Cause Analysis (RCA)

The account remained disabled after the employee returned from extended leave due to an administrative oversight.

---

# Resolution

- Verified employment status.
- Enabled Active Directory account.
- Confirmed successful login.

---

# Verification

- Windows Login Successful
- Outlook Connected
- Teams Connected
- User Confirmed Resolution

---

# Escalation Decision

HR verification completed before enabling the account.

---

# Preventive Actions

- Review inactive accounts regularly.
- Coordinate HR onboarding/offboarding activities.
- Verify employment status before enabling accounts.

---

# Tools Used

- Active Directory Users and Computers (ADUC)

---

# Interview Questions

1. Difference between Locked and Disabled Account?
2. When should an account be disabled?
3. Why should HR approval be obtained before enabling an account?
4. Can a disabled account authenticate?

---

# Knowledge Learned

Never enable a disabled account without verifying the user's employment status, as disabled accounts may be part of the organization's security or offboarding process.

---

# Ticket Status

Closed

---

# Resolution Time

18 Minutes
