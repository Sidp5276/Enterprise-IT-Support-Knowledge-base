# Ticket 021 – User Account Locked

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000021 |
| Priority | P2 |
| Category | Active Directory |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported being unable to log in to the company laptop.

Error displayed:

> "Your account has been locked. Please contact your administrator."

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Active Directory Domain Services
- Microsoft Active Directory Users and Computers (ADUC)

---

# Business Impact

- User unable to sign in.
- Outlook unavailable.
- Teams inaccessible.
- Work interrupted.

---

# Initial Investigation

Collected Information:

- User recently changed password.
- Multiple login attempts made.
- Other users unaffected.

---

# Possible Causes

- Multiple incorrect password attempts
- Cached old password on another device
- Mobile device using old credentials
- Domain Account Lockout Policy

---

# Troubleshooting Steps

### Step 1

Verified account status using Active Directory Users and Computers (ADUC).

Result:

Account Locked = Yes

---

### Step 2

Checked Account Tab.

Observed:

✔ Account locked

---

### Step 3

Unlocked User Account.

Action:

✔ Selected **Unlock Account**

---

### Step 4

Requested user to log in again.

Login Successful.

---

### Step 5

Asked user to update password on:

- Outlook
- Mobile Phone
- VPN
- Microsoft Teams

to prevent future lockouts.

---

# Root Cause Analysis (RCA)

The user entered an incorrect password multiple times from a mobile device, triggering the Active Directory Account Lockout Policy.

---

# Resolution

- Account unlocked in ADUC.
- User logged in successfully.
- Updated saved passwords on all devices.

---

# Verification

- Windows Login Successful
- Outlook Connected
- Teams Connected
- User Confirmed Resolution

---

# User Communication Log

09:05 AM - Incident Logged

09:10 AM - Account Verified

09:14 AM - Account Unlocked

09:18 AM - User Confirmed Resolution

---

# Escalation Decision

No escalation required.

---

# Preventive Actions

- Update passwords on all connected devices after a password change.
- Avoid repeated incorrect login attempts.
- Review Account Lockout Policy if frequent lockouts occur.

---

# Tools Used

- Active Directory Users and Computers (ADUC)

---

# Technologies Used

- Active Directory
- Windows Server
- Windows 11
- Domain Authentication

---

# Interview Questions Based on This Ticket

1. What causes an AD account to lock?
2. Where do you unlock a user account?
3. What is Account Lockout Policy?
4. How would you identify the source of repeated account lockouts?
5. Difference between Locked Account and Disabled Account?

---

# Knowledge Learned

An account lockout protects the domain from brute-force attacks. L1 engineers can unlock the account, but they should also identify the source of repeated failed logins to prevent recurring incidents.

---

# Ticket Status

Closed

---

# Resolution Time

13 Minutes
