# Ticket 003 – Windows PC Running Extremely Slow

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000003 |
| Priority | P3 |
| Category | Performance Issue |
| Status | Closed |
| Department | Sales |
| Device | HP ProBook 440 G8 |
| Operating System | Windows 10 Enterprise |

---

# User Reported Issue

The user reported that the computer had become extremely slow. Applications were taking several minutes to open and the system frequently froze during normal work.

---

# Environment

- Windows 10 Enterprise
- Domain Joined
- Microsoft Office 365
- 8 GB RAM
- SSD Storage

---

# Initial Investigation

Information collected:

- Issue started two days ago.
- No recent software installation.
- Internet working normally.
- Outlook responding slowly.
- Multiple startup applications enabled.

---

# Possible Causes

- High CPU Usage
- High Memory Usage
- Startup Programs
- Low Disk Space
- Windows Updates
- Malware

---

# Troubleshooting Steps

### Step 1

Opened Task Manager.

Observed CPU usage above 95%.

---

### Step 2

Identified Microsoft Teams consuming excessive memory.

Ended unnecessary processes.

---

### Step 3

Disabled unnecessary Startup Applications.

Result

Startup optimized.

---

### Step 4

Checked Disk Usage.

Command

```cmd
wmic logicaldisk get size,freespace,caption
```

Only 8 GB free.

---

### Step 5

Performed Disk Cleanup.

Deleted temporary files.

Recycle Bin emptied.

---

### Step 6

Executed System File Checker.

Command

```cmd
sfc /scannow
```

No integrity violations.

---

### Step 7

Performed Windows Defender Quick Scan.

No threats detected.

---

### Step 8

Restarted system.

Performance significantly improved.

---

# Root Cause Analysis (RCA)

High CPU utilization caused by unnecessary startup applications and insufficient free disk space.

---

# Resolution

Disabled startup applications.

Cleaned temporary files.

Freed disk space.

Restarted workstation.

---

# Verification

Verified:

- Login completed within 30 seconds.
- Outlook opened normally.
- Excel opened successfully.
- CPU usage stabilized below 20%.
- User confirmed issue resolved.

---

# Preventive Actions

- Review startup applications monthly.
- Maintain at least 20% free disk space.
- Restart workstation regularly.
- Remove unused software.

---

# Commands Used

```cmd
wmic logicaldisk get size,freespace,caption

sfc /scannow
```

---

# Technologies Used

- Windows 10
- Task Manager
- CMD
- Windows Defender
- Disk Cleanup

---

# Knowledge Learned

- High CPU does not always indicate hardware failure.
- Startup applications significantly impact performance.
- Disk space should always be monitored.

---

# Ticket Status

Closed

---

# Resolution Time

35 Minutes
