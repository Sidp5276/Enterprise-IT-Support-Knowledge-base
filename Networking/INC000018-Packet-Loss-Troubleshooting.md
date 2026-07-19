# Ticket 018 – Packet Loss Investigation

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000018 |
| Priority | P1 |
| Category | Packet Loss |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Customer Support |
| Device | HP EliteBook 850 G7 |
| Operating System | Windows 11 Enterprise |
| SLA | 2 Hours |

---

# User Reported Issue

The user reported that video conferencing sessions disconnected repeatedly and VoIP audio was breaking up.

---

# Environment

- Windows 11 Enterprise
- Office LAN
- Cisco Switch
- Cisco Router

---

# Business Impact

- Customer calls interrupted.
- Teams meetings dropped.
- Voice quality poor.

---

# Initial Investigation

- Internet available.
- High complaint volume from same floor.
- Switch LEDs normal.

---

# Possible Causes

- Faulty LAN Cable
- Switch Port Errors
- Network Congestion
- ISP Issue
- Packet Loss

---

# Troubleshooting Steps

### Step 1

Performed Continuous Ping.

```cmd
ping 8.8.8.8 -t
```

Observed intermittent "Request Timed Out."

---

### Step 2

Performed PathPing.

```cmd
pathping 8.8.8.8
```

Packet loss detected between workstation and access switch.

---

### Step 3

Replaced Ethernet Cable.

---

### Step 4

Moved workstation to another switch port.

---

### Step 5

Retested.

```cmd
pathping 8.8.8.8
```

0% packet loss.

---

### Step 6

Verified Microsoft Teams.

Calls stable.

---

# Root Cause Analysis (RCA)

Faulty switch port introduced intermittent packet loss.

---

# Resolution

User connected to a healthy switch port.

Network stabilized.

---

# Verification

- No Packet Loss
- Teams Stable
- VoIP Calls Clear
- User Confirmed Resolution

---

# Commands Used

```cmd
ping 8.8.8.8 -t

pathping 8.8.8.8
```

---

# Technologies Used

- Cisco Switch
- Ethernet
- ICMP
- PathPing

---

# Interview Questions Based on This Ticket

1. What is packet loss?
2. Difference between ping and pathping?
3. What causes packet loss?
4. How does packet loss affect VoIP?
5. Why use continuous ping?

---

# Knowledge Learned

Packet loss often points to a faulty physical link, overloaded network equipment, or ISP issues. `pathping` is especially useful because it combines the capabilities of `ping` and `tracert` to identify where packets are being dropped.

---

# Ticket Status

Closed

---

# Resolution Time

36 Minutes
