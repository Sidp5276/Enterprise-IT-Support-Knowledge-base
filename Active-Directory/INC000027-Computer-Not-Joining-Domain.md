# Ticket 027 – Computer Unable to Join Active Directory Domain

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000027 |
| Priority | P2 |
| Category | Domain Join |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | IT |
| Device | Lenovo ThinkCentre M75 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

A newly deployed workstation could not be joined to the company's Active Directory domain.

Error displayed:

> "An Active Directory Domain Controller for the domain could not be contacted."

---

# Environment

- Windows 11 Enterprise
- Windows Server 2022 Domain Controller
- Active Directory Domain Services
- Corporate DNS

---

# Business Impact

- New workstation could not be provisioned.
- User onboarding delayed.

---

# Initial Investigation

- Network cable connected.
- Valid IP address assigned.
- Domain Controller online.
- DNS suspected.

---

# Possible Causes

- Incorrect DNS Server
- Time Synchronization Issue
- Firewall Blocking Domain Traffic
- Domain Controller Unreachable
- Typographical Error in Domain Name

---

# Troubleshooting Steps

### Step 1

Verified IP configuration.

```cmd
ipconfig /all
```

Observed:

DNS Server configured as **8.8.8.8** instead of the internal Domain Controller DNS.

---

### Step 2

Updated Preferred DNS Server to the corporate DNS server.

---

### Step 3

Verified Domain Controller resolution.

```cmd
nslookup dc01.company.local
```

Successful.

---

### Step 4

Verified connectivity.

```cmd
ping dc01.company.local
```

Successful.

---

### Step 5

Attempted domain join again.

Computer successfully joined the domain.

---

### Step 6

Restarted workstation.

Verified domain login.

---

# Root Cause Analysis (RCA)

The workstation was configured to use a public DNS server instead of the organization's internal Active Directory DNS server, preventing it from locating a Domain Controller.

---

# Resolution

- Configured correct internal DNS server.
- Successfully joined workstation to the domain.
- Verified user authentication.

---

# Verification

- Domain Join Successful
- Domain Login Successful
- Group Policies Started Applying
- User Confirmed Resolution

---

# Preventive Actions

- Verify DNS settings before attempting a domain join.
- Include DNS validation in workstation deployment SOP.

---

# Commands Used

```cmd
ipconfig /all

nslookup dc01.company.local

ping dc01.company.local
```

---

# Technologies Used

- Active Directory
- DNS
- Windows Server
- Windows 11

---

# Interview Questions

1. Why is DNS critical for Active Directory?
2. Can a PC join a domain using Google's DNS (8.8.8.8)?
3. What checks would you perform before joining a machine to a domain?
4. What happens after a computer successfully joins a domain?

---

# Knowledge Learned

Active Directory relies heavily on DNS to locate Domain Controllers and authenticate clients. One of the most common causes of domain join failures is an incorrect DNS configuration pointing to a public DNS server instead of the internal AD-integrated DNS server.

---

# Ticket Status

Closed

---

# Resolution Time

28 Minutes
