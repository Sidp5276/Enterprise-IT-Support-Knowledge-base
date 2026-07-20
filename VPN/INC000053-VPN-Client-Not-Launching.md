# Ticket 053 – VPN Client Not Launching

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000053 |
| Priority | P3 |
| Category | Software |
| Subcategory | VPN Client |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Marketing |
| Device | HP EliteBook 840 G9 |
| Operating System | Windows 11 Enterprise |
| VPN Client | Cisco AnyConnect Secure Mobility Client |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported that Cisco AnyConnect would not launch after double-clicking the desktop shortcut. No error message appeared, and the application closed immediately.

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect Secure Mobility Client
- Active Directory
- Corporate VPN Gateway

---

# Business Impact

- User unable to work remotely.
- Internal company resources inaccessible.
- Marketing campaign activities delayed.

---

# Initial Investigation

Collected Information:

- Workstation booted normally.
- Other applications launched successfully.
- VPN shortcut responsive but application closed immediately.
- Issue isolated to one workstation.

---

# Possible Causes

- Corrupted VPN Client Installation
- VPN Service Not Running
- Missing Application Files
- Windows Update Conflict
- Corrupted User Profile

---

# Troubleshooting Steps

### Step 1

Verified Cisco AnyConnect service.

Opened:

**Services (services.msc)**

Observed:

**Cisco AnyConnect Secure Mobility Agent** service stopped.

---

### Step 2

Started the service.

Service started successfully.

---

### Step 3

Attempted to launch VPN client.

Issue persisted.

---

### Step 4

Uninstalled Cisco AnyConnect from **Programs and Features**.

Restarted workstation.

---

### Step 5

Installed the latest organization-approved Cisco AnyConnect package.

---

### Step 6

Restarted workstation again.

---

### Step 7

Launched VPN client.

Application opened normally.

---

### Step 8

Established VPN connection.

Verified access to:

- Shared Drives
- Outlook
- ERP Application

---

# Root Cause Analysis (RCA)

The Cisco AnyConnect installation had become corrupted following a recent Windows update. Reinstalling the approved VPN client restored normal functionality.

---

# Resolution

- Restarted VPN service.
- Reinstalled Cisco AnyConnect.
- Verified successful VPN connection.
- Confirmed access to internal resources.

---

# Verification

- VPN Client Opens Successfully
- VPN Connected
- Internal Applications Accessible
- User Confirmed Resolution

---

# User Communication Log

09:00 AM – Incident Logged

09:15 AM – VPN Service Checked

09:30 AM – VPN Client Reinstalled

09:45 AM – User Confirmed Resolution

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Keep VPN client updated.
- Use only organization-approved installers.
- Verify VPN functionality after major Windows updates.

---

# Tools Used

- ServiceNow
- Cisco AnyConnect
- Windows Services
- Programs and Features

---

# Technologies Used

- Cisco AnyConnect
- Windows 11
- Active Directory
- VPN

---

# ITIL Concepts Demonstrated

- Incident Management
- Software Troubleshooting
- Application Recovery
- User Verification
- SLA Compliance

---

# Interview Questions

1. What would you check if a VPN client does not open?
2. Why check Windows services before reinstalling software?
3. When should a VPN client be reinstalled?
4. What could corrupt a VPN installation?
5. How do you verify a successful VPN repair?

---

# Knowledge Learned

Application launch failures are often caused by stopped services or corrupted installations. Before reinstalling software, L1 engineers should verify supporting services and basic application dependencies to minimize downtime.

---

# Ticket Status

Closed

---

# Resolution Time

45 Minutes
