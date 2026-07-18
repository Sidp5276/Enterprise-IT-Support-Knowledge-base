# Ticket 008 – BitLocker Recovery Key Prompt

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000008 |
| Priority | P2 |
| Category | BitLocker Recovery |
| Status | Closed |
| Department | Finance |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |

---

# User Reported Issue

The user reported that after restarting the laptop, Windows displayed the BitLocker Recovery screen and requested a 48-digit recovery key before allowing access to the operating system.

---

# Environment

- Windows 11 Enterprise
- BitLocker Enabled
- Domain Joined Device
- TPM Enabled
- Office Network

---

# Initial Investigation

Information collected:

- BIOS settings were recently updated.
- No hardware replacement.
- User unable to access Windows.
- Recovery key not available with the user.

---

# Possible Causes

- BIOS Update
- TPM Change
- Secure Boot Configuration Change
- Motherboard Hardware Change
- BitLocker Security Trigger

---

# Troubleshooting Steps

### Step 1

Verified BitLocker recovery screen.

Result

Recovery Key required.

---

### Step 2

Verified device ownership.

Employee ID confirmed.

---

### Step 3

Retrieved BitLocker Recovery Key from Active Directory / Azure AD.

Recovery Key successfully located.

---

### Step 4

Entered 48-digit Recovery Key.

Windows booted successfully.

---

### Step 5

Verified BitLocker Protection Status.

Command

```cmd
manage-bde -status
```

Result

Protection enabled.

---

### Step 6

Suspended BitLocker temporarily.

Command

```cmd
manage-bde -protectors -disable C:
```

Performed BIOS verification.

---

### Step 7

Re-enabled BitLocker.

Command

```cmd
manage-bde -protectors -enable C:
```

Protection restored successfully.

---

# Root Cause Analysis (RCA)

Recent BIOS firmware update triggered BitLocker security protection, requiring recovery authentication.

---

# Resolution

Retrieved BitLocker Recovery Key.

Authenticated device.

Re-enabled BitLocker after successful verification.

---

# Verification

- Windows boot successful
- Outlook opened
- Teams connected
- BitLocker Protection Enabled
- User confirmed issue resolved

---

# Preventive Actions

- Backup BitLocker Recovery Keys.
- Suspend BitLocker before BIOS updates.
- Document firmware changes.

---

# Commands Used

```cmd
manage-bde -status

manage-bde -protectors -disable C:

manage-bde -protectors -enable C:
```

---

# Technologies Used

- Windows 11
- BitLocker
- TPM
- Active Directory
- CMD

---

# Knowledge Learned

- BIOS changes can trigger BitLocker Recovery.
- Recovery Keys should always be backed up.
- Verify device ownership before sharing Recovery Keys.

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
