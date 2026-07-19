# Ticket 014 – IP Address Conflict Detected

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000014 |
| Priority | P2 |
| Category | IP Address Conflict |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported intermittent network connectivity. Windows displayed the notification:

> "Windows has detected an IP address conflict with another system on the network."

The user was unable to access Outlook, shared drives, or internal applications.

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- DHCP Enabled Network

---

# Business Impact

- Outlook disconnected.
- Shared folders inaccessible.
- ERP unavailable.
- User productivity affected.

---

# Initial Investigation

Information collected:

- Problem started after reconnecting the LAN cable.
- Other users unaffected.
- Internet intermittent.
- Network adapter enabled.

---

# Possible Causes

- Duplicate Static IP
- Incorrect DHCP Reservation
- Rogue Device
- DHCP Misconfiguration

---

# Troubleshooting Steps

### Step 1

Verified IP Address.

```cmd
ipconfig
```

Result

IP Assigned Successfully.

---

### Step 2

Verified complete network configuration.

```cmd
ipconfig /all
```

Observed duplicate IP reported.

---

### Step 3

Checked ARP Cache.

```cmd
arp -a
```

Detected conflicting MAC Address.

---

### Step 4

Released IP Address.

```cmd
ipconfig /release
```

Completed Successfully.

---

### Step 5

Renewed DHCP Lease.

```cmd
ipconfig /renew
```

New IP Assigned.

---

### Step 6

Verified Gateway Connectivity.

```cmd
ping 192.168.1.1
```

Successful.

---

### Step 7

Verified Internet.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 8

Verified Shared Drive Access.

Accessible Successfully.

---

# Root Cause Analysis (RCA)

Another workstation was manually configured with the same IP Address, causing an IP conflict on the network.

---

# Resolution

Obtained a new DHCP lease.

Duplicate IP removed by Network Team.

Connectivity restored.

---

# Verification

- Outlook Connected
- Internet Working
- Shared Drives Accessible
- ERP Accessible
- User Confirmed Resolution

---

# User Communication Log

02:10 PM - Incident Logged

02:18 PM - IP Conflict Identified

02:30 PM - DHCP Lease Renewed

02:36 PM - User Confirmed Resolution

---

# Escalation Decision

Network Team notified to identify duplicate static IP device.

---

# Preventive Actions

- Avoid manual static IP unless required.
- Maintain DHCP reservations.
- Audit duplicate IP devices.

---

# Commands Used

```cmd
ipconfig

ipconfig /all

ipconfig /release

ipconfig /renew

arp -a

ping 192.168.1.1

ping 8.8.8.8
```

---

# Technologies Used

- Windows 11
- DHCP
- ARP
- TCP/IP

---

# L1 Troubleshooting Flow

Check IP

↓

Verify Duplicate IP

↓

ARP Table

↓

Release/Renew

↓

Verify Gateway

↓

Verify Internet

↓

Escalate if duplicate device remains

---

# Interview Questions Based on This Ticket

1. What causes an IP Address Conflict?
2. What is ARP?
3. What does `arp -a` display?
4. Difference between Static IP and DHCP?
5. How do you resolve duplicate IP issues?

---

# Knowledge Learned

- Duplicate IPs cause intermittent connectivity.
- `arp -a` helps identify conflicting MAC addresses.
- DHCP renewal often resolves client-side conflicts.

---

# Ticket Status

Closed

---

# Resolution Time

26 Minutes
