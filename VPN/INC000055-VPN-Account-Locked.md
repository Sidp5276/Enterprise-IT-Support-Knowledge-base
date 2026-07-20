# Ticket 055 – VPN Account Locked

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000055 |
| Priority | P2 |
| Category | Network |
| Subcategory | VPN Account Lockout |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Procurement |
| Device | Dell Latitude 7420 |
| Operating System | Windows 11 Enterprise |
| VPN Client | Cisco AnyConnect Secure Mobility Client |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported being unable to connect to the corporate VPN.

Error displayed:

> "Account Locked. Contact your administrator."

The user mentioned attempting to log in multiple times before contacting the Service Desk.

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect Secure Mobility Client
- Active Directory
- Corporate VPN Gateway

---

# Business Impact

- User unable to access internal procurement systems.
- Purchase approvals delayed.
- Remote work interrupted.

---

# Initial Investigation

Collected Information:

- Internet connection working.
- VPN server reachable.
- User recently changed password.
- Multiple failed authentication attempts recorded.

---

# Possible Causes

- Multiple Incorrect Password Attempts
- Active Directory Account Lockout Policy
- Cached VPN Credentials
- User Entering Old Password

---

# Troubleshooting Steps

### Step 1

Verified internet connectivity.

```cmd
ping vpn.company.local
```

VPN gateway reachable.

---

### Step 2

Checked Active Directory account.

Observed:

**Account Locked**

---

### Step 3

Verified user identity according to company security policy.

- Employee ID
- Manager Name
- Registered Mobile Number

Identity confirmed.

---

### Step 4

Unlocked the Active Directory account.

---

### Step 5

Cleared cached VPN credentials.

---

### Step 6

Asked user to enter the latest Active Directory password.

VPN authenticated successfully.

---

### Step 7

Verified access to:

- ERP
- Shared Drives
- Outlook
- Teams

---

# Root Cause Analysis (RCA)

The user repeatedly attempted VPN authentication using an outdated password after a recent password change. This triggered the organization's Active Directory account lockout policy. Unlocking the account and removing cached credentials restored VPN access.

---

# Resolution

- Verified user identity.
- Unlocked Active Directory account.
- Cleared cached VPN credentials.
- Verified successful VPN login.

---

# Verification

- VPN Connected
- Internal Resources Accessible
- User Confirmed Resolution

---

# User Communication Log

10:05 AM – Incident Logged

10:15 AM – Identity Verified

10:20 AM – Account Unlocked

10:30 AM – VPN Connected Successfully

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Educate users to update saved VPN credentials after password changes.
- Inform users about the account lockout policy.
- Encourage use of password managers where permitted.

---

# Tools Used

- ServiceNow
- Active Directory Users and Computers
- Cisco AnyConnect

---

# Technologies Used

- Active Directory
- Cisco AnyConnect
- Windows 11
- VPN

---

# ITIL Concepts Demonstrated

- Incident Management
- Identity Verification
- Account Recovery
- Security Compliance
- Service Restoration

---

# Interview Questions

1. What causes an Active Directory account to become locked?
2. How would you verify a user's identity before unlocking an account?
3. Why should cached VPN credentials be cleared after unlocking an account?
4. What is the difference between an account lockout and a disabled account?
5. When should a VPN account lockout incident be escalated?

---

# Knowledge Learned

VPN account lockouts are commonly caused by repeated authentication failures using outdated or incorrect passwords. L1 engineers should always verify the user's identity, unlock the account according to security procedures, clear cached credentials if necessary, and confirm successful access before closing the incident.

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
