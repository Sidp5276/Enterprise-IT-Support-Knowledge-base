# Ticket 010 – Network Printer Not Printing

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000010 |
| Priority | P2 |
| Category | Network Printer |
| Status | Closed |
| Department | Human Resources |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |
| Assigned Group | Service Desk L1 |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that documents sent to the office network printer remained in the print queue and nothing was printed. Other users in the department were also unable to print to the same device.

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- Office LAN
- HP LaserJet Network Printer
- Print Server: PRINT01

---

# Initial Investigation

Information collected:

- Printer displayed "Ready"
- Printer connected to network
- Print jobs stuck in queue
- Multiple users affected
- No recent Windows updates

---

# Possible Causes

- Print Spooler Service stopped
- Printer Offline
- Print Queue Corruption
- Print Server Issue
- Network Connectivity Issue
- Incorrect Printer Driver

---

# Troubleshooting Steps

### Step 1

Verified printer status.

Result

Printer online.

---

### Step 2

Verified network connectivity.

```cmd
ping PRINT01
```

Result

Successful response received.

---

### Step 3

Restarted Print Spooler Service.

```cmd
net stop spooler

net start spooler
```

Result

Service restarted successfully.

---

### Step 4

Cleared Print Queue.

Deleted pending print jobs.

---

### Step 5

Verified printer mapping.

Printer connected correctly.

---

### Step 6

Printed Windows Test Page.

Result

Printed successfully.

---

### Step 7

Requested user to print PDF.

Document printed successfully.

---

# Root Cause Analysis (RCA)

Corrupted print queue caused the Print Spooler service to stop processing print jobs.

---

# Resolution

Restarted Print Spooler Service.

Cleared corrupted print queue.

Verified successful communication with network printer.

---

# Verification

- Test page printed
- PDF printed successfully
- Excel document printed
- User confirmed issue resolved

---

# User Communication Log

**09:20 AM**

User reported inability to print.

**09:30 AM**

Troubleshooting initiated.

**09:42 AM**

Print queue cleared.

**09:48 AM**

Test page successful.

**09:50 AM**

User confirmed issue resolved.

---

# Closure Notes

Incident resolved within SLA.

No escalation required.

---

# Preventive Actions

- Restart Print Spooler if print jobs remain stuck.
- Periodically clear large print queues.
- Verify printer driver after Windows updates.

---

# Commands Used

```cmd
ping PRINT01

net stop spooler

net start spooler
```

---

# Technologies Used

- Windows 11
- Print Spooler
- Network Printer
- CMD
- TCP/IP

---

# Knowledge Learned

- Print Spooler is responsible for managing print jobs.
- A corrupted print queue can prevent all users from printing.
- Always verify printer connectivity before reinstalling drivers.

---

# Interview Questions Based on This Ticket

1. What is the Print Spooler service?
2. How do you restart the Print Spooler?
3. Why do print jobs get stuck?
4. How would you troubleshoot a network printer?
5. What is the difference between a local printer and a network printer?

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
