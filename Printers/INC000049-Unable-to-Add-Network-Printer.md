# Ticket 049 – Unable to Add Network Printer

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000049 |
| Priority | P3 |
| Category | Hardware |
| Subcategory | Network Printer Installation |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | Dell OptiPlex 7010 |
| Operating System | Windows 11 Enterprise |
| SLA | 8 Hours |

---

# User Reported Issue

The user reported being unable to add the department's network printer. While attempting to connect, Windows displayed the following error:

> "Windows couldn't connect to the printer."

---

# Environment

- Windows 11 Enterprise
- Canon ImageRunner 2630
- TCP/IP Network Printer
- Corporate LAN

---

# Business Impact

- User unable to print HR documents.
- Offer letters and employee forms delayed.
- Department productivity impacted.

---

# Initial Investigation

Collected Information:

- Printer powered on.
- Other users printing successfully.
- User connected to corporate network.
- Issue isolated to one workstation.

---

# Possible Causes

- Incorrect Printer IP Address
- Network Discovery Disabled
- Missing Printer Driver
- Firewall Restriction
- Incorrect Port Configuration

---

# Troubleshooting Steps

### Step 1

Verified network connectivity.

```cmd
ping 192.168.1.160
```

Reply received successfully.

---

### Step 2

Verified printer IP address with Network Team.

Confirmed correct IP.

---

### Step 3

Opened:

**Settings → Bluetooth & Devices → Printers & Scanners**

Attempted automatic printer discovery.

Printer not detected.

---

### Step 4

Selected:

**Add Printer Manually**

Configured printer using TCP/IP address.

---

### Step 5

Installed organization-approved printer driver.

---

### Step 6

Completed printer installation.

Printed Windows Test Page.

Successful.

---

### Step 7

Verified business document printing.

Successful.

---

# Root Cause Analysis (RCA)

Automatic printer discovery failed because the workstation could not locate the printer through network discovery. Manually adding the printer using its TCP/IP address and installing the correct driver resolved the issue.

---

# Resolution

- Added printer manually using TCP/IP.
- Installed approved printer driver.
- Verified successful printing.

---

# Verification

- Printer Installed
- Test Page Printed
- Business Document Printed
- User Confirmed Resolution

---

# User Communication Log

09:20 AM – Incident Logged

09:35 AM – Printer Installation Started

09:50 AM – Printer Added Successfully

09:55 AM – User Confirmed Resolution

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Maintain updated printer inventory.
- Document printer IP addresses.
- Use approved drivers only.

---

# Tools Used

- ServiceNow
- Windows Printer Settings

---

# Commands Used

```cmd
ping 192.168.1.160
```

---

# Technologies Used

- Windows 11
- TCP/IP Printing
- Canon ImageRunner
- Network Printer

---

# Interview Questions

1. How do you manually add a network printer?
2. Why use TCP/IP instead of automatic discovery?
3. What information is required before adding a printer manually?
4. How do you verify network connectivity to a printer?
5. Why is the correct printer driver important?

---

# Knowledge Learned

When Windows cannot automatically discover a printer, adding it manually using its TCP/IP address is a common enterprise solution. Verifying connectivity, using the correct driver, and confirming successful test printing are standard L1 troubleshooting steps.

---

# Ticket Status

Closed

---

# Resolution Time

35 Minutes
