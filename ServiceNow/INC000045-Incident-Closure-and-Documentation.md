# Ticket 045 – Incident Closure and Documentation

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000045 |
| Priority | P3 |
| Category | Network |
| Subcategory | VPN |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported being unable to connect to the corporate VPN while working remotely.

Error displayed:

> "VPN Connection Failed. Unable to establish secure connection."

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect VPN
- Active Directory
- Corporate VPN Gateway

---

# Business Impact

- User unable to access internal company resources.
- HR applications inaccessible.
- Work from home interrupted.

---

# Initial Investigation

Collected Information:

- Internet connection working.
- User credentials accepted.
- VPN client installed correctly.
- Issue isolated to VPN authentication.

---

# Possible Causes

- Incorrect VPN Configuration
- Expired User Session
- VPN Client Issue
- Authentication Failure

---

# Troubleshooting Steps

### Step 1

Verified internet connectivity.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 2

Verified DNS resolution.

```cmd
nslookup vpn.company.local
```

Successful.

---

### Step 3

Restarted Cisco AnyConnect VPN Client.

---

### Step 4

Signed the user out of Microsoft 365.

Signed back in.

---

### Step 5

Attempted VPN connection again.

VPN connected successfully.

---

### Step 6

Verified access to:

- Shared Network Drive
- ERP Application
- Internal HR Portal

All resources accessible.

---

# Root Cause Analysis (RCA)

The VPN client had an expired authentication session. Re-authenticating the user's account refreshed the session and restored secure connectivity.

---

# Resolution

- Restarted VPN client.
- Re-authenticated user.
- Verified successful VPN connection.

---

# Verification

- VPN Connected
- Internal Applications Accessible
- Shared Drives Accessible
- User Confirmed Resolution

---

# User Communication Log

03:05 PM – Incident Logged

03:15 PM – Troubleshooting Started

03:25 PM – VPN Connection Restored

03:30 PM – User Confirmed Resolution

---

# Closure Checklist

✔ Root Cause Documented

✔ Resolution Steps Added

✔ User Confirmation Received

✔ Knowledge Base Reviewed

✔ SLA Met

✔ Ticket Categorized Correctly

✔ Work Notes Updated

---

# Closure Notes

Issue resolved after re-authenticating the VPN client. User confirmed stable connectivity and successful access to all required corporate resources. No further action required.

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Keep VPN client updated.
- Restart VPN client after password changes.
- Verify authentication after credential updates.

---

# Tools Used

- ServiceNow
- Cisco AnyConnect
- Command Prompt

---

# Commands Used

```cmd
ping 8.8.8.8
nslookup vpn.company.local
```

---

# Technologies Used

- ServiceNow
- Cisco AnyConnect
- Active Directory
- Windows 11
- VPN

---

# ITIL Concepts Demonstrated

- Incident Resolution
- User Verification
- Resolution Documentation
- SLA Compliance
- Incident Closure

---

# Interview Questions

1. What should be verified before closing an incident?
2. Why is user confirmation important before ticket closure?
3. What information should be included in Closure Notes?
4. What happens if a ticket is closed without verifying the solution?
5. What is the purpose of Resolution Codes and Closure Codes in ServiceNow?

---

# Knowledge Learned

Closing an incident is more than changing the status to "Closed." A Service Desk engineer should verify the solution with the user, document the root cause, record troubleshooting steps, ensure SLA compliance, and add meaningful closure notes. Proper documentation improves future troubleshooting and maintains service quality.

---

# Ticket Status

Closed

---

# Resolution Time

25 Minutes
