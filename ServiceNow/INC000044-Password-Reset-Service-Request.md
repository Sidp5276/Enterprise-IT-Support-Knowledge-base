# Ticket 044 – Password Reset Service Request

---

## Ticket Information

| Field | Value |
|-------|---------|
| Request ID | REQ000044 |
| RITM | RITM000044 |
| Priority | Medium |
| Category | Access Management |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Sales |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |
| SLA | 2 Hours |

---

# User Request

The user contacted the Service Desk stating they had forgotten their Active Directory password and were unable to log in to their workstation.

---

# Environment

- Windows 11 Enterprise
- Active Directory
- Microsoft 365
- Corporate Domain

---

# Business Impact

- User unable to access company resources.
- Daily work interrupted.
- Customer follow-ups delayed.

---

# Initial Verification

Verified user identity using company security policy.

Confirmed:

- Employee ID
- Manager Name
- Date of Birth (or approved verification method)

Identity successfully validated.

---

# Request Fulfillment Steps

### Step 1

Opened Active Directory Users and Computers.

Located user account.

---

### Step 2

Verified account status.

Account active.

---

### Step 3

Selected:

**Reset Password**

Assigned temporary password according to company password policy.

---

### Step 4

Enabled:

✔ User must change password at next logon.

---

### Step 5

Unlocked account (if applicable).

---

### Step 6

Provided temporary password securely over the approved communication channel.

---

### Step 7

User successfully logged into Windows.

Changed password immediately.

---

### Step 8

Verified access to:

- Windows
- Outlook
- Teams
- Shared Network Drives

---

# Root Cause Analysis (RCA)

Not Applicable.

This was a standard Access Management service request initiated by the user.

---

# Resolution

- Identity verified.
- Password reset completed.
- Temporary password issued.
- User changed password successfully.
- Access restored.

---

# Verification

- Windows Login Successful
- Outlook Accessible
- Teams Working
- User Confirmed Resolution

---

# User Communication Log

11:10 AM – Request Logged

11:15 AM – Identity Verified

11:20 AM – Password Reset Completed

11:25 AM – User Logged In

11:30 AM – Request Closed

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Encourage users to use self-service password reset if available.
- Remind users to update recovery methods.
- Follow company password policy.

---

# Tools Used

- ServiceNow
- Active Directory Users and Computers (ADUC)

---

# Technologies Used

- ServiceNow
- Active Directory
- Windows 11
- Microsoft 365

---

# ITIL Concepts Demonstrated

- Access Management
- Identity Verification
- Request Fulfillment
- Security Compliance
- Documentation

---

# Interview Questions

1. Why must user identity be verified before resetting a password?
2. What is the difference between a password reset and an account unlock?
3. What does "User must change password at next logon" do?
4. Why is password reset considered a Service Request instead of an Incident?
5. What security precautions should an L1 engineer follow during password resets?

---

# Knowledge Learned

Password reset requests are among the most common Service Desk tasks. Following identity verification procedures before resetting credentials is essential to protect user accounts and maintain compliance with organizational security policies.

---

# Ticket Status

Closed

---

# Resolution Time

20 Minutes
