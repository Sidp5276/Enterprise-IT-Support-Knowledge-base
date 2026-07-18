## Issue

User reports that the system crashes with a Blue Screen of Death (BSOD) during startup.

# Ticket 002 – Windows Blue Screen of Death (BSOD)

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000002 |
| Priority | P1 |
| Category | Windows Operating System |
| Status | Closed |
| Department | Human Resources |
| Device | Dell Latitude 5420 |
| Operating System | Windows 11 Enterprise |

---

# User Reported Issue

The user reported that the laptop suddenly displayed a Blue Screen of Death (BSOD) while working on Microsoft Excel. After rebooting, the same error appeared repeatedly.

---

# Environment

- Windows 11 Enterprise
- Domain Joined Laptop
- Microsoft Office 365
- Dell Latitude 5420
- Company Managed Device

---

# Initial Investigation

Information collected from the user:

- No recent hardware changes
- Windows Update installed previous night
- Laptop rebooting automatically
- Unable to reach desktop
- Other users not affected

---

# Possible Causes

- Corrupted Windows Update
- Faulty Driver
- Damaged System Files
- RAM Issues
- Disk Errors

---

# Troubleshooting Steps

### Step 1

Booted Windows into Safe Mode.

Result

System entered Safe Mode successfully.

---

### Step 2

Checked Event Viewer.

Observed multiple BugCheck errors.

---

### Step 3

Executed System File Checker.

Command

```cmd
sfc /scannow
```

Result

Corrupted files detected and repaired.

---

### Step 4

Checked Windows Image.

Command

```cmd
DISM /Online /Cleanup-Image /RestoreHealth
```

Result

Image restored successfully.

---

### Step 5

Checked Disk Errors.

Command

```cmd
chkdsk C: /f
```

Result

Minor file system errors repaired.

---

### Step 6

Removed recently installed display driver.

Installed latest certified driver.

---

### Step 7

Restarted device.

Windows booted successfully.

---

# Root Cause Analysis (RCA)

A corrupted display driver installed through Windows Update caused repeated BSOD crashes.

---

# Resolution

Removed faulty driver.

Installed stable manufacturer-approved driver.

Verified Windows integrity using SFC and DISM.

---

# Verification

Verified:

- Windows boot successful
- Excel working
- Outlook launched
- Teams connected
- No further BSOD

Issue resolved successfully.

---

# Preventive Actions

- Delay optional Windows Updates.
- Install only certified drivers.
- Monitor Event Viewer after updates.

---

# Commands Used

```cmd
sfc /scannow

DISM /Online /Cleanup-Image /RestoreHealth

chkdsk C: /f
```

---

# Technologies Used

- Windows 11
- Event Viewer
- CMD
- Windows Recovery
- Device Manager

---

# Knowledge Learned

- Always boot into Safe Mode first.
- Verify system files before reinstalling Windows.
- Check recently updated drivers.

---

# Ticket Status

Closed

---

# Resolution Time

45 Minutes
