# Ticket 016 – VPN Connection Failed

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000016 |
| Priority | P2 |
| Category | VPN |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user was working from home and reported being unable to connect to the corporate VPN.

Error displayed:

> "The VPN connection could not be established."

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect VPN
- Home Wi-Fi
- Azure Active Directory Authentication

---

# Business Impact

- Unable to access ERP.
- Shared drives inaccessible.
- Internal applications unavailable.

---

# Initial Investigation

- Internet working normally.
- Other websites accessible.
- VPN credentials unchanged.
- MFA completed successfully.

---

# Possible Causes

- VPN Service Down
- Expired User Credentials
- Firewall Blocking VPN
- DNS Issue
- VPN Client Corruption

---

# Troubleshooting Steps

### Step 1

Verified Internet Connectivity.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 2

Verified DNS Resolution.

```cmd
nslookup vpn.company.com
```

Hostname resolved successfully.

---

### Step 3

Restarted VPN Client.

No improvement.

---

### Step 4

Restarted VPN Service.

```cmd
services.msc
```

Restarted Cisco AnyConnect Secure Mobility Agent.

---

### Step 5

Attempted VPN Connection Again.

Authentication successful.

Tunnel established.

---

### Step 6

Verified Internal Resources.

- ERP Accessible
- Shared Drive Accessible
- Intranet Working

---

# Root Cause Analysis (RCA)

Cisco AnyConnect background service stopped unexpectedly after a Windows update.

---

# Resolution

Restarted VPN service.

Verified successful VPN tunnel establishment.

---

# Verification

- VPN Connected
- ERP Accessible
- Shared Drives Working
- User Confirmed Resolution

---

# User Communication Log

09:05 AM - Incident Logged

09:12 AM - VPN Service Checked

09:20 AM - VPN Restored

09:23 AM - User Confirmed Resolution

---

# Escalation Decision

No escalation required.

---

# Preventive Actions

- Restart VPN service after Windows updates if required.
- Keep VPN client updated.
- Monitor VPN service health.

---

# Commands Used

```cmd
ping 8.8.8.8

nslookup vpn.company.com

services.msc
```

---

# Technologies Used

- Cisco AnyConnect
- Azure AD
- DNS
- VPN
- Windows 11

---

# Interview Questions Based on This Ticket

1. What is a VPN?
2. Difference between VPN and Proxy?
3. What happens when a VPN tunnel is established?
4. Why is DNS important for VPN?
5. What would you check if VPN authentication succeeds but internal applications are still unreachable?

---

# Knowledge Learned

Always verify internet connectivity before troubleshooting VPN issues. If DNS and authentication are working, checking the VPN client service is a logical next step.

---

# Ticket Status

Closed

---

# Resolution Time

18 Minutes
