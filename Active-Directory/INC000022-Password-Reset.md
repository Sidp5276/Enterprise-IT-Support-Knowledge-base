# Ticket 022 – Active Directory Password Reset

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000022 |
| Priority | P2 |
| Category | Active Directory |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user forgot the domain password and was unable to sign in.

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Active Directory Domain Services

---

# Business Impact

- User unable to access workstation.
- Outlook unavailable.
- Internal systems inaccessible.

---

# Initial Investigation

Verified user identity using company security verification process before performing a password reset.

---

# Possible Causes

- Forgotten Password
- Password Expired
- Password Complexity Requirement
- User Error

---

# Troubleshooting Steps

### Step 1

Verified user identity using Employee ID and security questions.

---

### Step 2

Opened Active Directory Users and Computers (ADUC).

Located user account.

---

### Step 3

Selected:

**Reset Password**

Assigned temporary password.

---

### Step 4

Enabled:

✔ User must change password at next logon.

---

### Step 5

Provided temporary password securely to the user.

---

### Step 6

User logged in successfully.

Created a new password following company password policy.

---

# Root Cause Analysis (RCA)

The user forgot the domain password and required an administrative password reset.

---

# Resolution

- Password reset successfully.
- Temporary password assigned.
- User created a new password during login.

---

# Verification

- Windows Login Successful
- Outlook Connected
- Teams Connected
- ERP Accessible

---

# User Communication Log

11:20 AM - Ticket Logged

11:28 AM - Identity Verified

11:35 AM - Password Reset

11:40 AM - User Logged In Successfully

---

# Escalation Decision

No escalation required.

---

# Preventive Actions

- Encourage users to use approved password managers.
- Follow password complexity policy.
- Update passwords on all company devices after reset.

---

# Tools Used

- Active Directory Users and Computers (ADUC)

---

# Technologies Used

- Active Directory
- Windows Server
- Domain Authentication

---

# Interview Questions Based on This Ticket

1. How do you reset a user's password in Active Directory?
2. Why should you verify user identity before resetting a password?
3. What does "User must change password at next logon" do?
4. What is a strong password policy?
5. Difference between Password Reset and Password Change?

---

# Knowledge Learned

Password resets are one of the most common L1 support tasks. Identity verification is mandatory before making any account changes to prevent unauthorized access.

---

# Ticket Status

Closed

---

# Resolution Time

20 Minutes
