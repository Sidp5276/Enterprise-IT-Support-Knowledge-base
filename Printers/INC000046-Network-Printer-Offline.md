# Ticket 046 – Network Printer Offline

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000046 |
| Priority | P3 |
| Category | Hardware |
| Subcategory | Network Printer |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Accounts |
| Device | HP LaserJet Pro MFP M428fdw |
| Operating System | Windows 11 Enterprise |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported that the office network printer appeared **Offline** in Windows. Print jobs remained in the queue, and no documents were printed despite multiple attempts.

---

# Environment

- Windows 11 Enterprise
- HP LaserJet Pro M428fdw
- TCP/IP Network Printer
- Corporate LAN

---

# Business Impact

- Users unable to print invoices and financial documents.
- Daily office work delayed.
- Multiple employees affected.

---

# Initial Investigation

Collected Information:

- Printer powered on.
- Printer display showed Ready.
- Multiple users experienced the same issue.
- Printer visible on the network.

---

# Possible Causes

- Printer Offline Mode
- Print Spooler Issue
- Network Connectivity Problem
- Incorrect Printer Port
- Stuck Print Queue

---

# Troubleshooting Steps

### Step 1

Verified printer network connectivity.

```cmd
ping 192.168.1.150
```

Reply received successfully.

---

### Step 2

Opened:

**Control Panel → Devices and Printers**

Verified printer status.

Observed:

Printer marked Offline.

---

### Step 3

Disabled:

**Use Printer Offline**

---

### Step 4

Restarted Print Spooler service.

```cmd
net stop spooler
net start spooler
```

---

### Step 5

Cleared pending print jobs.

Restarted printer.

---

### Step 6

Printed Windows Test Page.

Successfully printed.

---

### Step 7

Asked user to print a business document.

Document printed successfully.

---

# Root Cause Analysis (RCA)

The Windows print spooler had become unresponsive, causing the printer to appear offline. Restarting the spooler service and clearing the print queue restored normal printing.

---

# Resolution

- Restarted Print Spooler.
- Cleared print queue.
- Disabled Offline mode.
- Verified successful printing.

---

# Verification

- Printer Online
- Test Page Printed
- Business Document Printed
- User Confirmed Resolution

---

# Ticket Status

Closed

---

# Resolution Time

22 Minutes
