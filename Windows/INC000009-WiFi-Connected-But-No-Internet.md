# Ticket 009 – Wi-Fi Connected but No Internet Access

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000009 |
| Priority | P2 |
| Category | Windows Networking |
| Status | Closed |
| Department | Marketing |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |

---

# User Reported Issue

The user reported that the laptop was connected to the office Wi-Fi, but websites were not loading and Microsoft Teams remained disconnected.

---

# Environment

- Windows 11 Enterprise
- Office Wi-Fi
- Domain Joined
- Cisco Wireless Network

---

# Initial Investigation

Information collected:

- Wi-Fi connected successfully.
- Signal strength excellent.
- Other employees using same Wi-Fi without issue.
- VPN disabled.

---

# Possible Causes

- Invalid IP Address
- DNS Failure
- Gateway Issue
- Network Adapter Problem
- DHCP Failure

---

# Troubleshooting Steps

### Step 1

Verified IP configuration.

Command

```cmd
ipconfig
```

Observed APIPA Address:

169.254.x.x

---

### Step 2

Released IP Address.

Command

```cmd
ipconfig /release
```

Completed successfully.

---

### Step 3

Renewed IP Address.

Command

```cmd
ipconfig /renew
```

Valid company IP assigned.

---

### Step 4

Flushed DNS.

Command

```cmd
ipconfig /flushdns
```

Completed successfully.

---

### Step 5

Verified Default Gateway.

Command

```cmd
ipconfig
```

Gateway present.

---

### Step 6

Tested connectivity.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 7

Verified DNS.

```cmd
nslookup google.com
```

Hostname resolved successfully.

---

### Step 8

Opened browser.

Internet working normally.

---

# Root Cause Analysis (RCA)

DHCP failed to assign a valid IP Address. The system automatically assigned an APIPA (169.254.x.x) address.

---

# Resolution

Released old IP.

Renewed DHCP lease.

Flushed DNS cache.

Verified internet connectivity.

---

# Verification

- Internet working
- Teams connected
- Outlook synchronized
- Company applications accessible

Issue resolved successfully.

---

# Preventive Actions

- Verify DHCP Server availability.
- Restart Wi-Fi adapter if APIPA appears.
- Report repeated DHCP failures to Network Team.

---

# Commands Used

```cmd
ipconfig

ipconfig /release

ipconfig /renew

ipconfig /flushdns

ping 8.8.8.8

nslookup google.com
```

---

# Technologies Used

- Windows 11
- DHCP
- DNS
- TCP/IP
- CMD

---

# Knowledge Learned

- APIPA (169.254.x.x) indicates DHCP failure.
- Always test IP before DNS.
- Internet troubleshooting should follow Layer 1 to Layer 7 methodology.

---

# Ticket Status

Closed

---

# Resolution Time

28 Minutes
