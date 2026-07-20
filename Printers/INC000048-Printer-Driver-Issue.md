# Ticket 048 – Printer Driver Issue

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000048 |
| Priority | P3 |
| Category | Hardware |
| Subcategory | Printer Driver |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Administration |
| Device | HP LaserJet Pro M404dn |
| Operating System | Windows 11 Enterprise |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported that documents were printing as unreadable symbols and random characters instead of the expected content. Other users connected to the same printer were able to print normally.

---

# Environment

- Windows 11 Enterprise
- HP LaserJet Pro M404dn
- USB/TCP-IP Printer
- HP Universal Print Driver

---

# Business Impact

- Official documents could not be printed.
- Paper and toner wasted.
- Administrative work delayed.

---

# Initial Investigation

Collected Information:

- Printer functioning normally for other users.
- Test page printed incorrectly only from the affected workstation.
- Issue isolated to the local computer.

---

# Possible Causes

- Corrupted Printer Driver
- Incorrect Driver Version
- Driver Compatibility Issue
- Windows Update Driver Conflict

---

# Troubleshooting Steps

### Step 1

Verified printer status.

Printer online.

---

### Step 2

Printed Windows Test Page.

Output contained unreadable characters.

---

### Step 3

Opened:

**Print Management**

Removed existing printer.

---

### Step 4

Uninstalled printer driver.

Restarted workstation.

---

### Step 5

Downloaded and installed the latest HP Universal Print Driver approved by the organization.

---

### Step 6

Added printer again using TCP/IP address.

---

### Step 7

Printed Windows Test Page.

Successful.

---

### Step 8

User printed business document.

Output normal.

---

# Root Cause Analysis (RCA)

The workstation was using a corrupted or incompatible printer driver after a recent Windows update. Reinstalling the approved driver restored normal printing.

---

# Resolution

- Removed old driver.
- Installed latest approved HP driver.
- Reconfigured printer.
- Verified successful printing.

---

# Verification

- Test Page Printed
- Business Document Printed
- User Confirmed Resolution

---

# User Communication Log

11:15 AM – Incident Logged

11:25 AM – Driver Removed

11:40 AM – New Driver Installed

11:48 AM – Printing Verified

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Use only organization-approved printer drivers.
- Keep printer drivers updated.
- Test printing after Windows feature updates.

---

# Tools Used

- ServiceNow
- Print Management
- Device Manager

---

# Technologies Used

- HP Universal Print Driver
- Windows 11
- TCP/IP Printing

---

# Interview Questions

1. How do you identify a printer driver issue?
2. Why can two users experience different printer behavior on the same printer?
3. What is the difference between a printer driver problem and a spooler problem?
4. Why should organization-approved drivers be used?
5. When would you reinstall a printer driver?

---

# Knowledge Learned

If only one workstation experiences printing problems while other users print successfully, the issue is often local to that workstation. Reinstalling the correct printer driver is a common and effective L1 troubleshooting step.

---

# Ticket Status

Closed

---

# Resolution Time

35 Minutes
