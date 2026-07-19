# Ticket 026 – User Cannot Access Shared Folder

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000026 |
| Priority | P2 |
| Category | File Share Access |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Operations |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported receiving the following error while opening a departmental shared folder:

> "You do not have permission to access this folder."

---

# Environment

- Windows 11 Enterprise
- Active Directory
- Windows File Server
- SMB File Share

---

# Business Impact

- User unable to access project documents.
- Daily operational work delayed.

---

# Initial Investigation

- Network connectivity verified.
- File server reachable.
- Other department users had access.
- User recently transferred from another department.

---

# Possible Causes

- Incorrect Security Group
- Missing NTFS Permissions
- Share Permission Issue
- AD Replication Delay

---

# Troubleshooting Steps

### Step 1

Verified file server connectivity.

```cmd
ping FILESRV01
```

Successful.

---

### Step 2

Verified user group membership in ADUC.

Observed:

User still belonged to previous department groups.

---

### Step 3

Compared permissions with another Operations employee.

Missing group detected:

Operations_Share_RW

---

### Step 4

Added user to the required security group.

---

### Step 5

Requested user to log off and log back in.

---

### Step 6

Verified shared folder access.

Folder opened successfully.

---

# Root Cause Analysis (RCA)

The user had changed departments, but the required security group membership had not been updated.

---

# Resolution

- Added user to correct AD Security Group.
- User session refreshed.
- Folder access restored.

---

# Verification

- Shared Folder Accessible
- Documents Open Successfully
- User Confirmed Resolution

---

# Preventive Actions

- Review group memberships during department transfers.
- Use standardized access provisioning checklist.

---

# Tools Used

- Active Directory Users and Computers (ADUC)

---

# Technologies Used

- Active Directory
- NTFS Permissions
- SMB
- Windows File Server

---

# Interview Questions

1. Difference between Share Permissions and NTFS Permissions?
2. Why is logoff/login required after changing group membership?
3. What are Effective Permissions?
4. How would you troubleshoot "Access Denied" errors?

---

# Knowledge Learned

File access issues are commonly caused by incorrect security group membership rather than network problems. Always verify both group membership and permissions before escalating.

---

# Ticket Status

Closed

---

# Resolution Time

24 Minutes
