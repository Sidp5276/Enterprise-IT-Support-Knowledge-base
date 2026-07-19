# Ticket 035 – OneDrive Files Not Synchronizing

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000035 |
| Priority | P2 |
| Category | Microsoft 365 |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Marketing |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that files saved in the local OneDrive folder were not synchronizing to the cloud. A red "X" icon was displayed on the OneDrive icon in the system tray, and recent files were not visible when accessing OneDrive through the web portal.

---

# Environment

- Windows 11 Enterprise
- Microsoft 365
- OneDrive for Business
- Microsoft Entra ID (Azure AD)

---

# Business Impact

- Project files not backed up to the cloud.
- Team members unable to access the latest documents.
- Risk of data loss if the device failed.

---

# Initial Investigation

Collected Information:

- Internet connection working normally.
- Microsoft 365 account signed in successfully.
- Outlook and Teams functioning correctly.
- Issue isolated to OneDrive synchronization.

---

# Possible Causes

- OneDrive Sync Client Paused
- User Signed Out of OneDrive
- Storage Quota Reached
- Corrupted OneDrive Cache
- Network Connectivity Issue

---

# Troubleshooting Steps

### Step 1

Verified internet connectivity.

Result:

Connection stable.

---

### Step 2

Checked OneDrive status.

Observed:

Synchronization paused.

---

### Step 3

Resumed OneDrive synchronization.

Waited several minutes.

Result:

Issue persisted.

---

### Step 4

Verified available OneDrive storage.

Result:

Storage within allocated quota.

---

### Step 5

Signed the user out of OneDrive.

Signed back in using Microsoft 365 credentials.

---

### Step 6

Restarted the OneDrive sync client.

Synchronization restarted successfully.

---

### Step 7

Verified synchronization by creating a test document.

Confirmed the file appeared in:

- Local OneDrive folder
- OneDrive Web Portal
- Another synchronized device

---

# Root Cause Analysis (RCA)

The OneDrive sync client had stopped synchronizing due to a corrupted sign-in session. Re-authenticating the Microsoft 365 account refreshed the connection and restored normal synchronization.

---

# Resolution

- Signed out of OneDrive.
- Signed back in using Microsoft 365 credentials.
- Restarted the OneDrive sync client.
- Verified successful synchronization.

---

# Verification

- Files Synchronizing Successfully
- OneDrive Status Showing "Up to Date"
- Test File Uploaded Successfully
- User Confirmed Resolution

---

# User Communication Log

11:05 AM – Ticket Logged

11:12 AM – OneDrive Status Verified

11:18 AM – User Re-authenticated

11:25 AM – Synchronization Restored

11:30 AM – User Confirmed Resolution

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Ensure OneDrive remains signed in after password changes.
- Monitor available cloud storage.
- Keep the OneDrive client updated.
- Advise users not to pause synchronization unless necessary.

---

# Tools Used

- OneDrive Sync Client
- Microsoft 365 Admin Center
- OneDrive Web Portal

---

# Technologies Used

- Microsoft 365
- OneDrive for Business
- Microsoft Entra ID (Azure AD)
- Windows 11

---

# Interview Questions

1. What is OneDrive for Business?
2. How do you troubleshoot OneDrive sync issues?
3. How can you verify whether the problem is local or cloud-based?
4. What happens if a user's OneDrive storage quota is full?
5. What does the "Up to Date" status in OneDrive indicate?
6. Why does signing out and signing back into OneDrive often resolve sync problems?

---

# Knowledge Learned

OneDrive synchronization issues are commonly caused by paused syncing, expired authentication sessions, storage limitations, or client-side cache problems. Before escalating, verify internet connectivity, account status, available storage, and the sync client's health. Re-authenticating the OneDrive client is a common and effective L1 troubleshooting step.

---

# Ticket Status

Closed

---

# Resolution Time

25 Minutes
