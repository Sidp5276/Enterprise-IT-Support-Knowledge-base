# Ticket 047 – Print Queue Stuck

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000047 |
| Priority | P3 |
| Category | Hardware |
| Subcategory | Print Queue |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Operations |
| Device | Canon ImageRunner 2625 |
| Operating System | Windows 11 Enterprise |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported that print jobs remained in the queue with the status **"Printing"**, but no pages were printed. Multiple users connected to the same printer experienced the issue.

---

# Environment

- Windows 11 Enterprise
- Canon Network Printer
- Print Spooler Service
- Corporate LAN

---

# Business Impact

- Shipping labels could not be printed.
- Office documentation delayed.
- Multiple employees affected.

---

# Initial Investigation

Collected Information:

- Printer powered on.
- Network connectivity normal.
- Printer displayed "Ready".
- Print queue contained multiple pending jobs.

---

# Possible Causes

- Print Spooler Service Hung
- Corrupted Print Job
- Printer Communication Delay
- Driver Communication Failure

---

# Troubleshooting Steps

### Step 1

Verified printer connectivity.

```cmd
ping 192.168.1.155
```

Reply received successfully.

---

### Step 2

Opened Print Queue.

Observed:

12 print jobs stuck.

---

### Step 3

Stopped Print Spooler.

```cmd
net stop spooler
```

---

### Step 4

Deleted pending print jobs from:

```text
C:\Windows\System32\spool\PRINTERS
```

---

### Step 5

Restarted Print Spooler.

```cmd
net start spooler
```

---

### Step 6

Restarted printer.

---

### Step 7

Printed Windows Test Page.

Successful.

---

### Step 8

User printed business documents.

Printing completed successfully.

---

# Root Cause Analysis (RCA)

A corrupted print job caused the Windows Print Spooler service to stop processing subsequent print requests.

---

# Resolution

- Cleared print queue.
- Restarted Print Spooler.
- Restarted printer.
- Verified successful printing.

---

# Verification

- Queue Empty
- Printer Online
- Test Page Printed
- User Confirmed Resolution

---

# User Communication Log

10:05 AM – Incident Logged

10:15 AM – Queue Inspected

10:22 AM – Queue Cleared

10:30 AM – Printing Restored

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Remove failed print jobs promptly.
- Keep printer firmware updated.
- Restart spooler after recurring queue failures.

---

# Tools Used

- ServiceNow
- Command Prompt
- Print Management

---

# Commands Used

```cmd
net stop spooler
net start spooler
ping 192.168.1.155
```

---

# Technologies Used

- Windows Print Spooler
- Network Printer
- Windows 11

---

# Interview Questions

1. What is the Print Spooler service?
2. Why do print queues become stuck?
3. Where are pending print jobs stored?
4. Why restart the Print Spooler?
5. What would you check before escalating a printer issue?

---

# Knowledge Learned

Most print queue issues are caused by corrupted print jobs or an unresponsive Print Spooler service. Clearing the queue and restarting the spooler usually restores normal printing without requiring printer replacement.

---

# Ticket Status

Closed

---

# Resolution Time

25 Minutes
