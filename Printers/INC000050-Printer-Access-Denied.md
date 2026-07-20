# Ticket 050 – Printer Access Denied

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000050 |
| Priority | P3 |
| Category | Hardware |
| Subcategory | Printer Permissions |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported receiving the following error while attempting to print:

> "Access Denied. You do not have permission to use this printer."

The printer was accessible to other Finance department users.

---

# Environment

- Windows 11 Enterprise
- HP LaserJet Enterprise M507
- Print Server
- Active Directory

---

# Business Impact

- User unable to print invoices and payment documents.
- Financial operations delayed.
- Individual user affected.

---

# Initial Investigation

Collected Information:

- Printer online.
- Printer functioning for other users.
- User authenticated successfully.
- Issue isolated to one account.

---

# Possible Causes

- Missing Active Directory Group Membership
- Incorrect Printer Permissions
- Group Policy Delay
- Print Server Permission Issue

---

# Troubleshooting Steps

### Step 1

Verified user account.

Successful login.

---

### Step 2

Checked printer permissions on the Print Server.

Observed:

User lacked **Print** permission.

---

### Step 3

Verified Active Directory security group membership.

User had recently transferred departments and was not a member of the Finance Printer security group.

---

### Step 4

Added user to:

**Finance_Printer_Users**

---

### Step 5

Executed:

```cmd
gpupdate /force
```

Restarted workstation.

---

### Step 6

User logged in again.

Printed Windows Test Page.

Successful.

---

### Step 7

Printed Finance document.

Successful.

---

# Root Cause Analysis (RCA)

The user was missing the required Active Directory security group that granted printer permissions after a departmental transfer. Group membership was updated, and Group Policy refreshed successfully.

---

# Resolution

- Added user to printer security group.
- Updated Group Policy.
- Verified successful printing.

---

# Verification

- Printer Accessible
- Test Page Printed
- Finance Documents Printed
- User Confirmed Resolution

---

# User Communication Log

02:05 PM – Incident Logged

02:20 PM – Permissions Verified

02:30 PM – AD Group Updated

02:40 PM – Printing Restored

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Review printer permissions during department transfers.
- Automate AD group assignments where possible.
- Audit print server permissions regularly.

---

# Tools Used

- ServiceNow
- Active Directory Users and Computers
- Print Management
- Group Policy

---

# Commands Used

```cmd
gpupdate /force
```

---

# Technologies Used

- Active Directory
- Group Policy
- Print Server
- Windows 11

---

# Interview Questions

1. Why can one user receive "Access Denied" while others can print?
2. How do Active Directory groups control printer access?
3. What is the purpose of `gpupdate /force`?
4. How do printer permissions differ from driver issues?
5. What would you check before escalating a printer permission issue?

---

# Knowledge Learned

Enterprise printers are often secured using Active Directory groups and print server permissions. After role or department changes, users may lose printer access if their group memberships are not updated. Verifying permissions and refreshing Group Policy are common L1 troubleshooting steps.

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
