# Ticket 005 – User Profile Service Failed the Sign-in

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000005 |
| Priority | P1 |
| Category | Windows User Profile |
| Status | Closed |
| Department | Finance |
| Device | HP EliteBook 840 G7 |
| Operating System | Windows 10 Enterprise |

---

# User Reported Issue

The user reported that Windows displayed the following message during login:

> **"The User Profile Service failed the sign-in. User profile cannot be loaded."**

The user was unable to access the desktop.

---

# Environment

- Windows 10 Enterprise
- Domain Joined
- Office Network
- Microsoft 365 Installed

---

# Initial Investigation

Information collected:

- Issue started after an unexpected power failure.
- User profile inaccessible.
- Safe Mode available.
- Other domain users could log in successfully.

---

# Possible Causes

- Corrupted user profile
- Registry corruption
- Unexpected shutdown
- Disk corruption
- Profile service failure

---

# Troubleshooting Steps

### Step 1

Booted system into Safe Mode.

Result

Safe Mode loaded successfully.

---

### Step 2

Verified Event Viewer logs.

Observed User Profile Service errors.

---

### Step 3

Checked disk health.

Command

```cmd
chkdsk C: /f
```

Result

Minor file system errors repaired.

---

### Step 4

Verified Windows system files.

Command

```cmd
sfc /scannow
```

Result

Corrupted files repaired.

---

### Step 5

Created temporary administrator account.

Command

```cmd
net user TempAdmin Password@123 /add

net localgroup administrators TempAdmin /add
```

Result

Temporary administrator account created successfully.

---

### Step 6

Logged in using temporary administrator account.

Backed up user profile data.

---

### Step 7

Deleted corrupted profile.

Created a fresh Windows user profile.

Restored Documents, Desktop and Downloads.

---

### Step 8

User logged in successfully.

---

# Root Cause Analysis (RCA)

Unexpected power interruption corrupted the Windows user profile, preventing successful authentication.

---

# Resolution

Created a new Windows profile.

Migrated user data from corrupted profile.

Verified normal login.

---

# Verification

Verified:

- User login successful
- Desktop loaded correctly
- Outlook opened successfully
- Teams connected
- Files restored successfully

Issue resolved successfully.

---

# Preventive Actions

- Enable automatic backups.
- Avoid force shutdowns.
- Use UPS for desktop systems.
- Monitor disk health regularly.

---

# Commands Used

```cmd
chkdsk C: /f

sfc /scannow

net user TempAdmin Password@123 /add

net localgroup administrators TempAdmin /add
```

---

# Technologies Used

- Windows 10
- CMD
- Event Viewer
- User Profiles
- Local User Management

---

# Knowledge Learned

- User profile corruption is different from password issues.
- Always back up user data before deleting profiles.
- Temporary administrator accounts help recover inaccessible systems safely.

---

# Ticket Status

Closed

---

# Resolution Time

55 Minutes
