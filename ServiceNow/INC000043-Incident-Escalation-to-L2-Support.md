# Ticket 043 – Incident Escalation to L2 Support

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000043 |
| Priority | P2 |
| Category | Business Application |
| Subcategory | ERP Application |
| Status | Resolved (Escalated to L2) |
| Assigned Group | Service Desk L1 |
| Escalated To | Application Support L2 |
| Department | Finance |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported being unable to access the company's ERP application. After entering valid credentials, the application displayed the message:

> "Unable to establish connection with application server."

Multiple users from the Finance department reported the same issue.

---

# Environment

- Windows 11 Enterprise
- ERP Client
- Active Directory Authentication
- Corporate LAN

---

# Business Impact

- Finance team unable to process invoices.
- Payment approvals delayed.
- Critical business operations interrupted.

---

# Initial Investigation

Collected Information:

- User credentials verified.
- Windows login successful.
- Network connectivity normal.
- Internet access available.
- ERP server unreachable.

---

# Possible Causes

- ERP Application Server Down
- Backend Database Issue
- Application Service Failure
- Network Routing Issue
- Server Maintenance

---

# Troubleshooting Steps

### Step 1

Verified user credentials.

Authentication successful.

---

### Step 2

Verified network connectivity.

```cmd
ping ERP-SERVER
```

Request timed out.

---

### Step 3

Verified DNS resolution.

```cmd
nslookup ERP-SERVER
```

DNS resolved correctly.

---

### Step 4

Confirmed issue on another workstation.

Same error observed.

---

### Step 5

Checked ServiceNow for existing incidents.

Multiple users reported identical issue.

---

### Step 6

Determined issue was not user-specific.

Prepared escalation notes.

---

### Step 7

Escalated incident to Application Support (L2) with:

- Error screenshots
- Troubleshooting performed
- Affected departments
- Number of impacted users
- Ping and DNS results

---

# Root Cause Analysis (RCA)

The ERP application server service had stopped unexpectedly. L2 Application Support restarted the application services, restoring connectivity for all users.

---

# Resolution

- L1 completed initial troubleshooting.
- Escalated to L2 with complete investigation details.
- L2 restarted ERP services.
- User access restored.

---

# Verification

- ERP Login Successful
- Application Accessible
- Finance Team Confirmed Resolution
- Incident Closed

---

# User Communication Log

09:05 AM – Incident Logged

09:15 AM – Initial Investigation Completed

09:25 AM – Escalated to L2

09:55 AM – L2 Restored Service

10:00 AM – User Confirmed Resolution

---

# Escalation Decision

Escalated because:

- Multiple users affected
- Infrastructure issue suspected
- Outside L1 support scope

---

# Preventive Actions

- Configure server health monitoring.
- Enable automatic service restart.
- Monitor application availability proactively.

---

# Tools Used

- ServiceNow
- Command Prompt

---

# Commands Used

```cmd
ping ERP-SERVER
nslookup ERP-SERVER
```

---

# Technologies Used

- ServiceNow
- Active Directory
- ERP Application
- Windows 11
- Corporate LAN

---

# ITIL Concepts Demonstrated

- Incident Management
- Functional Escalation
- Major Incident Identification
- Work Notes
- Assignment Groups
- SLA Compliance

---

# Interview Questions

1. When should an incident be escalated to L2?
2. What information should be included before escalation?
3. What is Functional Escalation?
4. How do you identify a Major Incident?
5. Why should L1 perform troubleshooting before escalating?

---

# Knowledge Learned

An incident should only be escalated after L1 troubleshooting is completed and documented. Proper escalation with detailed investigation prevents duplicate work and helps L2 resolve the issue more efficiently.

---

# Ticket Status

Closed

---

# Resolution Time

55 Minutes
