# Ticket 015 – Unable to Reach Default Gateway

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000015 |
| Priority | P1 |
| Category | Gateway Connectivity |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Operations |
| Device | Dell Latitude 5430 |
| Operating System | Windows 11 Enterprise |
| SLA | 2 Hours |

---

# User Reported Issue

The user reported that no internal or external websites were accessible.

Internet icon displayed:

> "Connected, No Internet"

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- Cisco Switch
- Corporate Router

---

# Business Impact

- User unable to access ERP.
- Outlook Offline.
- Teams Disconnected.
- Shared Drives Inaccessible.

---

# Initial Investigation

Information collected:

- LAN Cable Connected.
- Other nearby users working.
- Device restarted once.

---

# Possible Causes

- Incorrect Gateway
- Router Failure
- Switch Port Issue
- Network Adapter Issue
- Incorrect IP Configuration

---

# Troubleshooting Steps

### Step 1

Verified IP Configuration.

```cmd
ipconfig
```

Valid IP Assigned.

---

### Step 2

Verified Gateway.

Gateway:

192.168.1.1

---

### Step 3

Tested Gateway.

```cmd
ping 192.168.1.1
```

Request Timed Out.

---

### Step 4

Restarted Network Adapter.

Adapter Disabled and Enabled.

---

### Step 5

Renewed DHCP Lease.

```cmd
ipconfig /release

ipconfig /renew
```

Completed Successfully.

---

### Step 6

Tested Gateway Again.

```cmd
ping 192.168.1.1
```

Successful Reply.

---

### Step 7

Verified Internet.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 8

Verified DNS.

```cmd
nslookup google.com
```

Successful.

---

### Step 9

Opened Corporate Applications.

ERP, Outlook and Teams functioning normally.

---

# Root Cause Analysis (RCA)

Incorrect gateway information was temporarily assigned during DHCP lease allocation, preventing outbound network communication.

---

# Resolution

Renewed DHCP lease.

Correct gateway assigned.

Connectivity restored.

---

# Verification

- Gateway Reachable
- Internet Working
- Outlook Connected
- Teams Connected
- ERP Accessible

---

# User Communication Log

10:20 AM - Incident Logged

10:28 AM - Gateway Failure Identified

10:40 AM - DHCP Lease Renewed

10:44 AM - User Confirmed Resolution

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Verify DHCP Scope.
- Monitor Gateway Availability.
- Report repeated gateway failures to Network Team.

---

# Commands Used

```cmd
ipconfig

ipconfig /release

ipconfig /renew

ping 192.168.1.1

ping 8.8.8.8

nslookup google.com
```

---

# Technologies Used

- Windows 11
- DHCP
- Default Gateway
- DNS
- TCP/IP

---

# L1 Troubleshooting Flow

Check IP

↓

Verify Gateway

↓

Ping Gateway

↓

Renew DHCP

↓

Verify Internet

↓

Verify DNS

↓

Confirm Applications

---

# Interview Questions Based on This Ticket

1. What is a Default Gateway?
2. Why is a Default Gateway required?
3. Can a user access the internet without a gateway?
4. How do you troubleshoot gateway issues?
5. Difference between Gateway, Router and Switch?

---

# Knowledge Learned

- A valid IP alone is insufficient without a reachable default gateway.
- Gateway connectivity should always be tested before investigating DNS or application issues.
- DHCP renewal can resolve incorrect gateway assignments.

---

# Ticket Status

Closed

---

# Resolution Time

24 Minutes
