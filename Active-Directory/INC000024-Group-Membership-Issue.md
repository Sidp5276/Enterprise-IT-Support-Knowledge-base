# Ticket 024 – User Unable to Access Shared Folder Due to Group Membership

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000024 |
| Priority | P2 |
| Category | Active Directory |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported:

> "Access Denied"

while opening the Finance Shared Folder.

---

# Environment

- Windows 11 Enterprise
- Active Directory
- Windows File Server

---

# Business Impact

- User unable to access department documents.
- Daily reporting delayed.

---

# Initial Investigation

- Other Finance users had access.
- Network connectivity normal.
- Folder server reachable.

---

# Possible Causes

- Missing Security Group
- Incorrect NTFS Permission
- Replication Delay
- Wrong Department Assignment

---

# Troubleshooting Steps

### Step 1

Verified user account in ADUC.

---

### Step 2

Checked **Member Of** tab.

Observed:

Finance_Share_RW group missing.

---

### Step 3

Compared with another Finance employee.

Confirmed required security group.

---

### Step 4

Added user to:

Finance_Share_RW

---

### Step 5

Asked user to log off and log in again.

---

### Step 6

Retested access.

Shared folder opened successfully.

---

# Root Cause Analysis (RCA)

The user was not added to the required Active Directory security group during onboarding.

---

# Resolution

Added the user to the correct security group and refreshed the user's session.

---

# Verification

- Shared Folder Accessible
- No Permission Errors
- User Confirmed Resolution

---

# Escalation Decision

No escalation required.

---

# Preventive Actions

- Verify security group assignment during onboarding.
- Maintain department onboarding checklist.

---

# Tools Used

- Active Directory Users and Computers (ADUC)

---

# Technologies Used

- Active Directory
- NTFS Permissions
- Security Groups
- Windows File Server

---

# Interview Questions

1. Difference between Security Group and Distribution Group?
2. Why is logoff/login sometimes required after group changes?
3. What is NTFS Permission?
4. How do Security Groups simplify permission management?

---

# Knowledge Learned

Access to shared resources should be granted through security groups rather than assigning permissions directly to individual users, making administration simpler and more secure.

---

# Ticket Status

Closed

---

# Resolution Time

22 Minutes
