# Ticket 020 – Internet Working but Company Application Not Reachable

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000020 |
| Priority | P1 |
| Category | Application Connectivity |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| SLA | 2 Hours |

---

# User Reported Issue

The user reported that internet browsing was working normally, but the company's ERP application could not be accessed.

Error displayed:

> "Unable to connect to server."

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- Internal ERP Application
- Windows Defender Firewall

---

# Business Impact

- Financial transactions delayed.
- Invoice processing unavailable.
- Business operations impacted.

---

# Initial Investigation

Information collected:

- Internet working.
- Outlook connected.
- Teams working.
- Multiple users from the Finance department reported the same issue.

---

# Possible Causes

- ERP Server Down
- Firewall Rule
- DNS Resolution Issue
- Application Service Stopped
- Routing Problem

---

# Troubleshooting Steps

### Step 1

Verified Internet.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 2

Verified ERP Server Resolution.

```cmd
nslookup erp.company.local
```

Hostname resolved successfully.

---

### Step 3

Tested ERP Server Connectivity.

```cmd
ping erp.company.local
```

Successful.

---

### Step 4

Verified Route.

```cmd
tracert erp.company.local
```

Route completed successfully.

---

### Step 5

Checked ERP Service Status.

Application Support Team confirmed the ERP Windows service had stopped unexpectedly after scheduled maintenance.

---

### Step 6

Application Team restarted ERP service.

---

### Step 7

Retested Application.

ERP opened successfully.

---

# Root Cause Analysis (RCA)

The ERP application service was stopped after scheduled server maintenance, preventing client connections while network connectivity remained healthy.

---

# Resolution

- Verified network connectivity.
- Confirmed DNS and routing were functioning correctly.
- Coordinated with the Application Support Team to restart the ERP service.
- Verified successful user access after service restoration.

---

# Verification

- ERP Accessible
- Internet Working
- Outlook Connected
- Teams Connected
- User Confirmed Resolution

---

# User Communication Log

09:40 AM – Ticket Logged

09:50 AM – Network Checks Completed

10:05 AM – Application Team Engaged

10:18 AM – ERP Service Restarted

10:22 AM – User Confirmed Resolution

---

# Escalation Decision

Escalated to Application Support Team after confirming the network infrastructure was functioning correctly.

---

# Preventive Actions

- Monitor critical application services.
- Configure automatic service recovery.
- Validate application availability after maintenance windows.

---

# Commands Used

```cmd
ping 8.8.8.8

nslookup erp.company.local

ping erp.company.local

tracert erp.company.local
```

---

# Technologies Used

- Windows 11
- DNS
- TCP/IP
- ERP
- Windows Services

---

# L1 Troubleshooting Flow

Internet Check

↓

DNS Resolution

↓

Server Reachability

↓

Traceroute

↓

Identify Application Issue

↓

Escalate to Application Team

↓

Verify Resolution

---

# Interview Questions Based on This Ticket

1. If the internet works but an internal application does not, where do you start troubleshooting?
2. How do you differentiate between a network issue and an application issue?
3. Why use `nslookup` before escalating?
4. What information should L1 provide to the Application Support Team?
5. When should an issue be escalated to another team?

---

# Knowledge Learned

Not every connectivity issue is a network issue. By verifying internet access, DNS resolution, server reachability, and routing before escalation, L1 support can confidently determine whether the root cause lies with the application rather than the underlying network.

---

# Ticket Status

Closed

---

# Resolution Time

42 Minutes
