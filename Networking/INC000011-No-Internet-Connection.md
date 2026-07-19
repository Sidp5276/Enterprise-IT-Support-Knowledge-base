# Ticket 011 – No Internet Connection

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000011 |
| Priority | P2 |
| Category | Network Connectivity |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that the internet stopped working suddenly. Microsoft Teams showed "Offline", Outlook was unable to synchronize emails, and websites were not loading.

Error displayed:

> "No Internet Access"

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- Ethernet Connection
- Cisco Managed Switch
- Corporate Firewall

---

# Business Impact

- User unable to access Outlook.
- Unable to use Microsoft Teams.
- Internal web applications inaccessible.
- Work interrupted.

---

# Initial Investigation

Information collected from the user:

- Issue started approximately 15 minutes ago.
- No recent software installation.
- Ethernet cable connected.
- Other nearby users had internet connectivity.
- Device restarted once before contacting Service Desk.

---

# Possible Causes

- Loose LAN cable
- Network Adapter Disabled
- Invalid IP Address
- DNS Issue
- Default Gateway Unreachable
- DHCP Failure
- Switch Port Issue

---

# Troubleshooting Steps

### Step 1

Verified physical connection.

- Ethernet cable securely connected.
- Link LED active.

Result

Physical connection normal.

---

### Step 2

Checked IP Configuration.

Command

```cmd
ipconfig
```

Result

Valid IPv4 address assigned.

Default Gateway available.

---

### Step 3

Verified Network Adapter.

Command

```cmd
ncpa.cpl
```

Result

Ethernet Adapter Enabled.

---

### Step 4

Tested TCP/IP Stack.

Command

```cmd
ping 127.0.0.1
```

Result

Successful Reply.

---

### Step 5

Tested Local IP.

Command

```cmd
ping <Local_IP_Address>
```

Example

```cmd
ping 192.168.1.105
```

Result

Successful.

---

### Step 6

Tested Default Gateway.

Command

```cmd
ping 192.168.1.1
```

Result

Successful.

---

### Step 7

Tested Internet Connectivity.

Command

```cmd
ping 8.8.8.8
```

Result

Request Timed Out.

---

### Step 8

Released and Renewed IP Address.

Commands

```cmd
ipconfig /release

ipconfig /renew
```

Result

New DHCP Lease Assigned.

---

### Step 9

Flushed DNS Cache.

Command

```cmd
ipconfig /flushdns
```

Result

Completed Successfully.

---

### Step 10

Tested Internet Again.

Command

```cmd
ping 8.8.8.8
```

Result

Successful Reply.

---

### Step 11

Verified Website Access.

Opened:

- google.com
- outlook.office.com
- company intranet

All websites loaded successfully.

---

# Root Cause Analysis (RCA)

The workstation had obtained an invalid DHCP lease which prevented internet communication. Renewing the IP address established a valid connection to the corporate network.

---

# Resolution

- Released existing IP configuration.
- Renewed DHCP lease.
- Cleared DNS cache.
- Verified internet connectivity.
- Confirmed access to corporate applications.

---

# Verification

Verified successfully:

✅ Internet working

✅ Microsoft Teams connected

✅ Outlook synchronized

✅ Internal applications accessible

✅ User confirmed issue resolved

---

# User Communication Log

**09:15 AM**

User reported no internet access.

**09:22 AM**

Initial troubleshooting started.

**09:30 AM**

DHCP lease renewed.

**09:34 AM**

Internet restored.

**09:36 AM**

User confirmed resolution.

---

# Escalation Decision

No escalation required.

Issue resolved by Service Desk L1.

---

# Preventive Actions

- Verify physical connection before software troubleshooting.
- Restart network adapter if issue recurs.
- Monitor DHCP server health.
- Report repeated lease failures to Network Team.

---

# Commands Used

```cmd
ipconfig

ipconfig /release

ipconfig /renew

ipconfig /flushdns

ping 127.0.0.1

ping <Local_IP>

ping <Default_Gateway>

ping 8.8.8.8

ncpa.cpl
```

---

# Technologies Used

- Windows 11
- TCP/IP
- DHCP
- Ethernet
- DNS
- CMD

---

# L1 Troubleshooting Flow

1. Check Physical Connection
2. Verify IP Address
3. Verify Network Adapter
4. Ping Loopback Address
5. Ping Local IP
6. Ping Default Gateway
7. Ping Public IP
8. Renew DHCP Lease
9. Flush DNS
10. Verify Internet Access

---

# Interview Questions Based on This Ticket

1. What does `ipconfig` do?
2. Difference between `ipconfig` and `ipconfig /all`?
3. Why do we ping `127.0.0.1`?
4. Why do we ping the Default Gateway?
5. Why do we ping `8.8.8.8`?
6. What does `ipconfig /release` do?
7. What does `ipconfig /renew` do?
8. What does `ipconfig /flushdns` do?
9. What is DHCP?
10. How would you troubleshoot "No Internet Connection" in an enterprise environment?

---

# Knowledge Learned

- Always troubleshoot from Layer 1 to Layer 7.
- Verify physical connectivity before software configuration.
- Test connectivity progressively: Loopback → Local IP → Gateway → Internet.
- Renewing the DHCP lease often resolves IP-related connectivity issues.
- Document every troubleshooting step before closing the incident.

---

# Ticket Status

Closed

---

# Resolution Time

21 Minutes
