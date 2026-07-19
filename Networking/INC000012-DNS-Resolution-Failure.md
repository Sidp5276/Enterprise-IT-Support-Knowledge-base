# Ticket 012 – DNS Resolution Failure

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000012 |
| Priority | P2 |
| Category | DNS |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Marketing |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that websites were not opening using domain names such as **google.com**, but Microsoft Teams remained connected.

Error displayed:

> "DNS_PROBE_FINISHED_NO_INTERNET"

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- Corporate DNS Server

---

# Business Impact

- Internal websites inaccessible.
- External websites not loading.
- Browser dependent applications unavailable.

---

# Initial Investigation

Information collected:

- Internet previously working.
- Other employees unaffected.
- No VPN.
- No recent software changes.

---

# Possible Causes

- DNS Server Down
- Incorrect DNS Configuration
- Corrupted DNS Cache
- Network Adapter Issue
- Firewall Restriction

---

# Troubleshooting Steps

### Step 1

Verified IP Address.

```cmd
ipconfig
```

Result

Valid IP Assigned.

---

### Step 2

Pinged Google using IP.

```cmd
ping 8.8.8.8
```

Result

Successful.

---

### Step 3

Pinged Google using hostname.

```cmd
ping google.com
```

Result

Could not resolve hostname.

---

### Step 4

Verified DNS Server.

```cmd
ipconfig /all
```

Observed incorrect DNS entry.

---

### Step 5

Flushed DNS Cache.

```cmd
ipconfig /flushdns
```

Completed Successfully.

---

### Step 6

Renewed IP Configuration.

```cmd
ipconfig /release

ipconfig /renew
```

Completed Successfully.

---

### Step 7

Verified DNS Resolution.

```cmd
nslookup google.com
```

Hostname resolved successfully.

---

### Step 8

Opened Browser.

Websites loading normally.

---

# Root Cause Analysis (RCA)

Incorrect DNS configuration prevented hostname resolution.

---

# Resolution

Updated DNS configuration.

Flushed DNS Cache.

Renewed IP Address.

Verified successful hostname resolution.

---

# Verification

- Websites Accessible
- Outlook Connected
- Teams Working
- Internal Portal Accessible

---

# User Communication Log

09:40 AM - Incident Logged

09:45 AM - DNS Investigation Started

09:56 AM - DNS Fixed

10:00 AM - User Confirmed Resolution

---

# Escalation Decision

No Escalation Required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Verify DNS Server Settings.
- Flush DNS after configuration changes.
- Monitor DNS Server Health.

---

# Commands Used

```cmd
ipconfig

ipconfig /all

ipconfig /flushdns

ipconfig /release

ipconfig /renew

ping 8.8.8.8

ping google.com

nslookup google.com
```

---

# Technologies Used

- DNS
- TCP/IP
- Windows 11
- CMD

---

# L1 Troubleshooting Flow

Check IP

↓

Ping Public IP

↓

Ping Hostname

↓

Verify DNS

↓

Flush DNS

↓

Renew IP

↓

Verify nslookup

↓

Confirm Website Access

---

# Interview Questions Based on This Ticket

1. What is DNS?
2. Difference between ping 8.8.8.8 and ping google.com?
3. What does nslookup do?
4. What is DNS Cache?
5. Why use ipconfig /flushdns?

---

# Knowledge Learned

- If IP works but hostname fails, suspect DNS.
- Always verify DNS before escalating.
- nslookup is one of the fastest ways to confirm DNS problems.

---

# Ticket Status

Closed

---

# Resolution Time

20 Minutes
