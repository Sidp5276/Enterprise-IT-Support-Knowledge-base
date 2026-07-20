# Ticket 041 – Incident Creation and Classification

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000041 |
| Priority | P2 |
| Category | Software |
| Subcategory | Microsoft Outlook |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | Dell Latitude 5430 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user contacted the Service Desk stating that Microsoft Outlook would not open. Every attempt to launch Outlook resulted in the application freezing on the loading screen before automatically closing.

---

# Environment

- Windows 11 Enterprise
- Microsoft Outlook 365
- Microsoft 365
- Exchange Online

---

# Business Impact

- User unable to access business emails.
- Customer communication interrupted.
- Finance approvals delayed.

---

# Initial Investigation

Collected Information:

- User successfully logged into Windows.
- Internet connectivity verified.
- Outlook Web (OWA) accessible.
- Issue isolated to Outlook Desktop application.

---

# Incident Classification

| Field | Value |
|------|------|
| Category | Software |
| Subcategory | Microsoft Outlook |
| Impact | Single User |
| Urgency | High |
| Priority | P2 |

---

# Possible Causes

- Corrupted Outlook Profile
- Faulty Outlook Add-ins
- Corrupted OST File
- Damaged Office Installation

---

# Troubleshooting Steps

### Step 1

Verified network connectivity.

Result:

Normal.

---

### Step 2

Logged into Outlook Web.

Mailbox working successfully.

---

### Step 3

Started Outlook in Safe Mode.

```cmd
outlook.exe /safe
```

Result:

Outlook opened successfully.

---

### Step 4

Disabled all COM Add-ins.

Restarted Outlook.

---

### Step 5

Opened Outlook normally.

Application launched successfully.

---

### Step 6

Enabled add-ins individually.

Identified one third-party PDF add-in causing Outlook to crash.

Disabled the faulty add-in permanently.

---

# Root Cause Analysis (RCA)

A third-party Outlook COM Add-in was preventing Outlook from launching normally. Safe Mode confirmed that Outlook itself was healthy and isolated the issue to installed add-ins.

---

# Resolution

- Started Outlook in Safe Mode.
- Disabled faulty COM Add-in.
- Restarted Outlook.
- Verified normal operation.

---

# Verification

- Outlook Opened Successfully
- Emails Accessible
- Calendar Working
- User Confirmed Resolution

---

# User Communication Log

09:10 AM – Incident Logged

09:18 AM – Investigation Started

09:30 AM – Faulty Add-in Identified

09:36 AM – Outlook Restored

09:40 AM – User Confirmed Resolution

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Review third-party Outlook add-ins before deployment.
- Keep Microsoft Office updated.
- Remove unnecessary COM Add-ins.

---

# Tools Used

- ServiceNow
- Outlook
- Outlook Safe Mode

---

# Technologies Used

- Microsoft 365
- Exchange Online
- Outlook
- Windows 11

---

# ITIL Concepts Demonstrated

- Incident Logging
- Categorization
- Priority Assignment
- SLA Tracking
- Work Notes
- Resolution Documentation

---

# Interview Questions

1. What is an Incident in ITIL?
2. What is the difference between Incident and Problem?
3. How do Impact and Urgency determine Priority?
4. Why is categorization important?
5. What information should always be included while creating an incident?

---

# Knowledge Learned

Proper incident categorization ensures tickets are routed to the correct support group and resolved within SLA. Before escalating, L1 engineers should isolate whether the issue is related to Outlook, Exchange Online, or third-party software.

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
