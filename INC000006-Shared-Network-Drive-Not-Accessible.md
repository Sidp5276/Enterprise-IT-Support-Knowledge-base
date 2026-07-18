# Ticket 006 – Shared Network Drive Not Accessible

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000006 |
| Priority | P2 |
| Category | Network Drive |
| Status | Closed |
| Department | Finance |
| Device | Dell Latitude 5430 |
| Operating System | Windows 11 Enterprise |

---

# User Reported Issue

The user reported that the shared network drive (Finance Shared Folder) was inaccessible after logging into Windows. The mapped drive displayed a red "X" icon and generated the message:

> "Windows cannot access \\FS01\Finance"

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- File Server (FS01)
- Active Directory Authentication

---

# Initial Investigation

Information collected:

- User logged in successfully.
- Internet working.
- Other users could access the shared drive.
- VPN not required (Office Network).
- Issue limited to one workstation.

---

# Possible Causes

- Network connectivity issue
- Incorrect drive mapping
- File server unavailable
- DNS resolution issue
- Permission issue
- Cached credentials

---

# Troubleshooting Steps

### Step 1

Verified internet connectivity.

```cmd
ping google.com
```

Result

Reply received successfully.

---

### Step 2

Verified File Server connectivity.

```cmd
ping FS01
```

Result

Successful.

---

### Step 3

Verified DNS resolution.

```cmd
nslookup FS01
```

Result

Hostname resolved successfully.

---

### Step 4

Checked mapped drives.

```cmd
net use
```

Observed disconnected drive.

---

### Step 5

Removed old mapping.

```cmd
net use Z: /delete
```

Completed successfully.

---

### Step 6

Mapped drive again.

```cmd
net use Z: \\FS01\Finance
```

Drive mapped successfully.

---

### Step 7

User opened shared folder.

Folder accessible.

---

# Root Cause Analysis (RCA)

Mapped drive contained stale credentials causing Windows to disconnect from the file server.

---

# Resolution

Removed old mapping.

Mapped network drive again.

Verified successful access.

---

# Verification

- Shared folder opened
- Excel files accessible
- Read/Write permissions verified
- User confirmed issue resolved

---

# Preventive Actions

- Reconnect mapped drives after password changes.
- Verify File Server availability before troubleshooting permissions.
- Remove stale mappings if disconnected.

---

# Commands Used

```cmd
ping google.com

ping FS01

nslookup FS01

net use

net use Z: /delete

net use Z: \\FS01\Finance
```

---

# Technologies Used

- Windows 11
- File Server
- SMB
- DNS
- CMD

---

# Knowledge Learned

- Always verify server connectivity before remapping drives.
- Cached credentials may disconnect mapped drives.
- `net use` is an essential troubleshooting command.

---

# Ticket Status

Closed

---

# Resolution Time

25 Minutes
