# Ticket 013 – DHCP Failed to Assign IP Address

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000013 |
| Priority | P2 |
| Category | DHCP |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Accounts |
| Device | Dell Latitude 5420 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that after connecting the LAN cable, internet was unavailable and corporate applications could not be accessed.

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- Cisco Switch
- DHCP Enabled Network

---

# Business Impact

- User unable to access ERP.
- Outlook disconnected.
- Teams offline.

---

# Initial Investigation

Information collected:

- LAN Cable Connected.
- Network Adapter Enabled.
- Other users working normally.

---

# Possible Causes

- DHCP Server Down
- Switch Port Issue
- Invalid Lease
- Network Adapter Issue
- LAN Cable Fault

---

# Troubleshooting Steps

### Step 1

Checked IP Configuration.

```cmd
ipconfig
```

Observed:

169.254.x.x

(APIPA Address)

---

### Step 2

Verified Network Adapter.

Adapter Enabled.

---

### Step 3

Released IP.

```cmd
ipconfig /release
```

Completed Successfully.

---

### Step 4

Renewed DHCP Lease.

```cmd
ipconfig /renew
```

Lease Request Failed.

---

### Step 5

Verified DHCP Server Connectivity.

```cmd
ping 192.168.1.10
```

No Reply.

---

### Step 6

Network Team confirmed DHCP Service restarted.

---

### Step 7

Renewed IP Again.

```cmd
ipconfig /renew
```

Valid IP Assigned.

---

### Step 8

Verified Gateway.

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

DHCP Server service stopped temporarily, preventing clients from obtaining valid IP addresses.

---

# Resolution

Renewed DHCP Lease after DHCP Service restoration.

Verified connectivity.

---

# Verification

- Valid Company IP Assigned
- Outlook Connected
- Teams Online
- ERP Accessible

---

# User Communication Log

11:10 AM - Ticket Logged

11:20 AM - DHCP Failure Identified

11:34 AM - DHCP Restored

11:38 AM - User Confirmed Resolution

---

# Escalation Decision

Escalated to Network Team for DHCP Service restart.

Returned to L1 for verification.

---

# Preventive Actions

- Monitor DHCP Server.
- Configure Redundant DHCP if available.
- Verify DHCP Scope Availability.

---

# Commands Used

```cmd
ipconfig

ipconfig /release

ipconfig /renew

ping 192.168.1.10

ping 192.168.1.1

ping 8.8.8.8
```

---

# Technologies Used

- DHCP
- Windows 11
- Ethernet
- TCP/IP

---

# L1 Troubleshooting Flow

Check IP

↓

Identify APIPA

↓

Release Lease

↓

Renew Lease

↓

Verify DHCP Server

↓

Escalate if DHCP Down

↓

Verify Gateway

↓

Verify Internet

---

# Interview Questions Based on This Ticket

1. What is DHCP?
2. What is APIPA?
3. Why does Windows assign 169.254.x.x?
4. Difference between Static IP and DHCP?
5. What happens during the DHCP DORA process?

---

# Knowledge Learned

- APIPA almost always indicates DHCP communication failure.
- Always verify DHCP before changing network settings.
- L1 can identify DHCP issues; service restart is usually handled by the Network Team.

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
