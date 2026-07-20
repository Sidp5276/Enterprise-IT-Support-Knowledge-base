# Ticket 054 – VPN Disconnects Frequently

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000054 |
| Priority | P2 |
| Category | Network |
| Subcategory | VPN Stability |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| VPN Client | Cisco AnyConnect Secure Mobility Client |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that the VPN connection disconnected automatically every 10–15 minutes while working remotely. Each disconnection interrupted access to internal applications.

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect Secure Mobility Client
- Corporate VPN Gateway
- Home Broadband Internet Connection

---

# Business Impact

- Frequent interruption of Finance operations.
- ERP sessions disconnected.
- Unsaved work lost.
- Reduced productivity.

---

# Initial Investigation

Collected Information:

- VPN connected successfully.
- Internet connection intermittently unstable.
- Other users not affected.
- Issue isolated to one remote user.

---

# Possible Causes

- Unstable Internet Connection
- Wi-Fi Signal Drops
- VPN Client Outdated
- Network Adapter Power Saving
- ISP Packet Loss

---

# Troubleshooting Steps

### Step 1

Verified internet stability.

```cmd
ping 8.8.8.8 -t
```

Observed intermittent packet loss.

---

### Step 2

Checked VPN logs.

No authentication failures found.

---

### Step 3

Disabled power-saving mode on the wireless network adapter.

---

### Step 4

Updated Cisco AnyConnect to the latest approved version.

---

### Step 5

Asked the user to connect using a wired Ethernet connection for testing.

VPN remained stable.

---

### Step 6

Monitored VPN session for 30 minutes.

No unexpected disconnections observed.

---

# Root Cause Analysis (RCA)

The user's unstable Wi-Fi connection caused intermittent packet loss, resulting in repeated VPN session drops. Switching to a stable wired connection and updating the VPN client resolved the issue.

---

# Resolution

- Updated VPN client.
- Disabled adapter power saving.
- Recommended wired connection.
- Verified stable VPN session.

---

# Verification

- Stable VPN Connection
- No Packet Loss Observed
- ERP Accessible
- User Confirmed Resolution

---

# User Communication Log

02:10 PM – Incident Logged

02:25 PM – Connectivity Tested

02:40 PM – VPN Client Updated

03:05 PM – Stability Confirmed

---

# Escalation Decision

No escalation required.

Issue identified as a client-side network problem.

---

# Preventive Actions

- Prefer wired connections when working remotely.
- Keep VPN client updated.
- Regularly monitor Wi-Fi signal quality.
- Disable unnecessary power-saving features for network adapters.

---

# Tools Used

- ServiceNow
- Cisco AnyConnect
- Command Prompt
- Device Manager

---

# Commands Used

```cmd
ping 8.8.8.8 -t
```

---

# Technologies Used

- Cisco AnyConnect
- Windows 11
- VPN
- TCP/IP
- Wi-Fi Networking

---

# ITIL Concepts Demonstrated

- Incident Management
- Network Troubleshooting
- User Communication
- Root Cause Analysis
- Service Restoration

---

# Interview Questions

1. What can cause frequent VPN disconnections?
2. Why is continuous ping useful during VPN troubleshooting?
3. How does packet loss affect VPN sessions?
4. Why should Wi-Fi stability be verified before escalating a VPN issue?
5. What is the benefit of using a wired connection for VPN users?

---

# Knowledge Learned

Frequent VPN disconnections are not always caused by the VPN server. Poor Wi-Fi quality, packet loss, outdated VPN clients, and network adapter power-saving settings are common client-side causes. Verifying internet stability before escalation helps resolve many VPN incidents quickly.

---

# Ticket Status

Closed

---

# Resolution Time

55 Minutes
```
