# Ticket 052 – VPN Connected but Unable to Access Internal Resources

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000052 |
| Priority | P2 |
| Category | Network |
| Subcategory | VPN Connectivity |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| VPN Client | Cisco AnyConnect Secure Mobility Client |
| SLA | 4 Hours |

---

# User Reported Issue

The user successfully connected to the corporate VPN but was unable to access internal resources such as shared network drives, the HR Portal, and the ERP application.

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect VPN
- Active Directory
- Corporate LAN

---

# Business Impact

- User unable to perform daily HR operations.
- Internal systems inaccessible.
- Work from home interrupted.

---

# Initial Investigation

Collected Information:

- VPN connected successfully.
- Internet browsing working.
- Internal applications unreachable.
- Issue affecting only one user.

---

# Possible Causes

- Incorrect VPN Route
- DNS Resolution Issue
- Expired VPN Session
- Split Tunnel Configuration
- Network Adapter Issue

---

# Troubleshooting Steps

### Step 1

Verified VPN connection status.

Status:

Connected.

---

### Step 2

Verified internet connectivity.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 3

Verified DNS resolution.

```cmd
nslookup hrportal.company.local
```

Successful.

---

### Step 4

Renewed IP configuration.

```cmd
ipconfig /flushdns
ipconfig /renew
```

Restarted VPN connection.

---

### Step 5

Verified access to shared drive.

Successful.

---

### Step 6

Verified ERP application.

Application opened successfully.

---

### Step 7

Confirmed HR Portal accessibility.

User confirmed all internal resources were available.

---

# Root Cause Analysis (RCA)

The VPN session failed to apply the correct network routes after the initial connection. Disconnecting, renewing network settings, flushing DNS, and reconnecting refreshed the routing information and restored access to internal resources.

---

# Resolution

- Refreshed network configuration.
- Reconnected VPN.
- Verified internal resource access.

---

# Verification

- Shared Drive Accessible
- HR Portal Accessible
- ERP Working
- User Confirmed Resolution

---

# User Communication Log

11:05 AM – Incident Logged

11:20 AM – VPN Verified

11:30 AM – Network Configuration Refreshed

11:40 AM – Internal Access Restored

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Restart VPN after network changes.
- Flush DNS if internal resources cannot be reached.
- Keep VPN client updated.

---

# Tools Used

- ServiceNow
- Cisco AnyConnect
- Command Prompt

---

# Commands Used

```cmd
ping 8.8.8.8
nslookup hrportal.company.local
ipconfig /flushdns
ipconfig /renew
```

---

# Technologies Used

- Cisco AnyConnect
- Active Directory
- Windows 11
- DNS
- VPN

---

# Interview Questions

1. Why can a VPN connect successfully but still fail to access internal resources?
2. What does `ipconfig /flushdns` do?
3. Why is DNS important for VPN users?
4. How would you determine whether the issue is routing or authentication?
5. What are split tunneling and full tunneling?

---

# Knowledge Learned

A successful VPN connection does not always guarantee access to internal resources. DNS, routing, and client network configuration must also be verified. Refreshing the network stack and reconnecting the VPN often resolves client-side connectivity issues.

---

# Ticket Status

Closed

---

# Resolution Time

35 Minutes
