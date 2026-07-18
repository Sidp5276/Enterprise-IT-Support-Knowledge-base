# INC000001 – Windows Login Failure After Password Reset

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000001 |
| Priority | P2 |
| Category | Windows Login |
| Status | Closed |
| Department | Finance |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |

---

# User Reported Issue

The user was unable to log into the Windows domain account after resetting the password.

Error displayed:

> "The username or password is incorrect."

---

# Environment

- Windows 11 Enterprise
- Domain Joined System
- Office Network
- Active Directory Authentication
- Microsoft Outlook Installed

---

# Initial Investigation

Information gathered from the user:

- Password reset completed 20 minutes ago
- Device connected to office Wi-Fi
- Other users unaffected
- No recent Windows updates
- Internet connection available

---

# Possible Causes

- Incorrect password
- Incorrect username
- Keyboard layout mismatch
- Caps Lock enabled
- Cached credentials
- Active Directory replication delay
- Domain Controller communication issue

---

# Troubleshooting Steps

### Step 1

Verified username.

Result

Correct username confirmed.

---

### Step 2

Checked Caps Lock.

Result

Disabled.

---

### Step 3

Verified internet connectivity.

Command

```cmd
ping google.com
```

Result

Reply received successfully.

---

### Step 4

Verified Domain Controller connectivity.

Command

```cmd
ping dc01.company.local
```

Result

Successful response received.

---

### Step 5

Cleared DNS cache.

Command

```cmd
ipconfig /flushdns
```

Result

DNS cache successfully flushed.

---

### Step 6

Updated Group Policy.

Command

```cmd
gpupdate /force
```

Result

Policy updated successfully.

---

### Step 7

Restarted workstation.

Result

Issue persisted.

---

### Step 8

Password reset performed again by administrator.

Waited five minutes for synchronization.

User attempted login again.

Login successful.

---

# Root Cause Analysis (RCA)

The issue occurred because Active Directory password replication had not completed across the domain controllers immediately after the password reset.

---

# Resolution

Password was reset again.

Waited for Active Directory synchronization.

User successfully authenticated into Windows.

---

# Verification

Verified the following:

- Windows login successful
- Desktop loaded successfully
- Outlook opened successfully
- Microsoft Teams connected
- Shared network drives accessible

Issue resolved successfully.

---

# Preventive Actions

- Wait 5–10 minutes after password reset before attempting login.
- Verify Active Directory replication.
- Confirm Domain Controller connectivity before troubleshooting credentials.

---

# Commands Used

```cmd
ping google.com

ping dc01.company.local

ipconfig /flushdns

gpupdate /force
```

---

# Technologies Used

- Windows 11
- Active Directory Concepts
- TCP/IP
- DNS
- Group Policy
- Command Prompt

---

# Knowledge Learned

- Password synchronization may take time across domain controllers.
- Always verify network connectivity before investigating authentication issues.
- Follow a structured troubleshooting approach.
- Document every troubleshooting step for future reference.

---

# Ticket Status

Closed

---

# Resolution Time

22 Minutes
