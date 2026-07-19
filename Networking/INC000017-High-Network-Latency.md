# Ticket 017 – High Network Latency

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000017 |
| Priority | P2 |
| Category | Performance |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Sales |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that Microsoft Teams calls were freezing and web applications were responding very slowly.

---

# Environment

- Windows 11 Enterprise
- Office LAN
- Cisco Network

---

# Business Impact

- Video meetings interrupted.
- CRM application slow.
- Productivity reduced.

---

# Initial Investigation

- Other nearby users reported similar slowness.
- No packet loss observed initially.
- CPU and Memory utilization normal.

---

# Possible Causes

- Network Congestion
- High Latency
- Router Issue
- ISP Problem
- Switch Overload

---

# Troubleshooting Steps

### Step 1

Checked Internet Connectivity.

```cmd
ping 8.8.8.8 -n 20
```

Average latency:

185 ms

---

### Step 2

Performed Route Trace.

```cmd
tracert 8.8.8.8
```

High delay observed after ISP gateway.

---

### Step 3

Verified Local Gateway.

```cmd
ping 192.168.1.1
```

Latency normal.

---

### Step 4

Network Team contacted ISP.

---

### Step 5

ISP resolved upstream routing issue.

---

### Step 6

Retested.

```cmd
ping 8.8.8.8 -n 20
```

Average latency:

18 ms

---

# Root Cause Analysis (RCA)

ISP routing issue caused excessive latency between corporate network and external destinations.

---

# Resolution

ISP corrected routing.

Latency returned to acceptable levels.

---

# Verification

- Teams Calls Stable
- CRM Working
- Web Browsing Normal
- User Confirmed Resolution

---

# Commands Used

```cmd
ping 8.8.8.8 -n 20

ping 192.168.1.1

tracert 8.8.8.8
```

---

# Technologies Used

- ICMP
- Traceroute
- Cisco Network

---

# Interview Questions Based on This Ticket

1. What is latency?
2. Difference between latency and bandwidth?
3. What does tracert do?
4. Acceptable LAN latency?
5. How do you identify where latency occurs?

---

# Knowledge Learned

High latency does not always indicate packet loss. Comparing gateway latency with internet latency helps isolate whether the issue is internal or external.

---

# Ticket Status

Closed

---

# Resolution Time

42 Minutes
