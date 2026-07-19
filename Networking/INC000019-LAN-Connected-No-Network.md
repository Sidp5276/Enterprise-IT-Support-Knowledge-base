# Ticket 019 – LAN Cable Connected but No Network Access

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000019 |
| Priority | P2 |
| Category | LAN Connectivity |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Procurement |
| Device | Dell OptiPlex 7010 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that the Ethernet cable was connected and the network icon showed "Connected", but no internet or internal company applications were accessible.

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- Cisco Managed Switch

---

# Business Impact

- Unable to access Outlook.
- Shared folders unavailable.
- ERP inaccessible.
- User unable to perform daily tasks.

---

# Initial Investigation

Information collected:

- Ethernet cable securely connected.
- Link LEDs active.
- Other users connected to the same switch had no issues.
- No recent Windows updates or software changes.

---

# Possible Causes

- Faulty Network Adapter
- Incorrect VLAN Assignment
- Switch Port Misconfiguration
- DHCP Failure
- Network Driver Issue

---

# Troubleshooting Steps

### Step 1

Verified IP Configuration.

```cmd
ipconfig /all
```

Result

Valid IP Address assigned.

---

### Step 2

Verified Gateway Connectivity.

```cmd
ping 192.168.1.1
```

Request Timed Out.

---

### Step 3

Disabled and Re-enabled Network Adapter.

```cmd
ncpa.cpl
```

No improvement.

---

### Step 4

Updated Network Adapter Driver.

Device Manager → Network Adapters

Driver successfully updated.

---

### Step 5

Connected another laptop to the same switch port.

Same issue observed.

---

### Step 6

Network Team verified switch configuration.

Incorrect VLAN assigned to switch port.

---

### Step 7

Correct VLAN applied.

Switch port reactivated.

---

### Step 8

Retested Connectivity.

```cmd
ping 192.168.1.1
```

Successful.

---

### Step 9

Verified Internet.

```cmd
ping 8.8.8.8
```

Successful.

---

# Root Cause Analysis (RCA)

The switch port was assigned to the wrong VLAN, preventing access to the corporate network despite the physical connection being active.

---

# Resolution

- Correct VLAN assigned.
- Switch port reconfigured.
- Connectivity restored.

---

# Verification

- Internet Working
- Outlook Connected
- ERP Accessible
- Shared Drives Accessible
- User Confirmed Resolution

---

# User Communication Log

01:20 PM – Ticket Logged

01:30 PM – Initial Investigation Completed

01:45 PM – Network Team Updated VLAN

01:52 PM – User Confirmed Resolution

---

# Escalation Decision

Escalated to Network Team for switch port configuration.

---

# Preventive Actions

- Verify VLAN assignment during new user setup.
- Audit switch ports regularly.
- Maintain switch configuration documentation.

---

# Commands Used

```cmd
ipconfig /all

ping 192.168.1.1

ping 8.8.8.8

ncpa.cpl
```

---

# Technologies Used

- Cisco Switch
- VLAN
- TCP/IP
- Ethernet
- Windows 11

---

# Interview Questions Based on This Ticket

1. What is a VLAN?
2. Can a LAN cable be connected but still have no network access?
3. How do you identify a switch port issue?
4. What is the difference between Layer 1 and Layer 2 problems?
5. Why is VLAN configuration important?

---

# Knowledge Learned

A successful physical connection does not guarantee network connectivity. Incorrect VLAN assignment is a common enterprise issue and usually requires coordination with the Network Team.

---

# Ticket Status

Closed

---

# Resolution Time

35 Minutes
