# SOP 004 – Network Printer Installation Procedure

---

# Purpose

This Standard Operating Procedure (SOP) explains the process for installing and configuring a network printer on a Windows workstation. The objective is to ensure users can print securely and reliably while following organizational standards.

---

# Scope

Applicable to all Service Desk (L1) engineers responsible for installing or troubleshooting network printers in the corporate environment.

---

# Prerequisites

- Approved ServiceNow Request or Incident
- Printer Powered On
- Printer Connected to Corporate Network
- Printer IP Address Available
- Organization-Approved Printer Driver
- User Logged In
- Local Administrator Rights (if required)

---

# Required Information

Before installation, verify:

- Printer Model
- Printer IP Address
- Department
- User Location
- Printer Driver Version
- Network Connectivity

---

# Procedure

## Step 1 – Verify Printer Availability

Check that:

- Printer is powered on.
- Printer display shows **Ready**.
- Network cable or Wi-Fi connection is active.

Verify connectivity:

```cmd
ping <Printer_IP_Address>
```

Expected Result:

Reply received successfully.

---

## Step 2 – Open Printer Settings

Navigate to:

**Settings → Bluetooth & Devices → Printers & Scanners**

Select:

**Add Device**

---

## Step 3 – Add Printer Manually

If Windows cannot discover the printer automatically:

Select:

**The printer that I want isn't listed**

Choose:

**Add a printer using a TCP/IP address or hostname**

---

## Step 4 – Configure Printer

Enter:

- Printer IP Address
- Device Type: TCP/IP Device

Allow Windows to detect the printer.

---

## Step 5 – Install Driver

Select the organization-approved printer driver.

If unavailable:

- Download from the internal software repository or vendor-approved source.
- Install the latest approved version.

---

## Step 6 – Complete Installation

Finish the installation wizard.

Rename the printer according to company naming standards if required.

Example:

```
Finance_HP_M507
```

---

## Step 7 – Print Test Page

Open:

**Printer Properties → Print Test Page**

Verify successful printing.

---

## Step 8 – Verify User Printing

Ask the user to print a business document.

Confirm:

- Document prints correctly.
- No formatting issues.
- No permission errors.

---

## Step 9 – Update ServiceNow

Document:

- Printer model
- IP address
- Driver version
- Test page successful
- User confirmation received

Close the request or incident.

---

# Security Best Practices

- Install only organization-approved drivers.
- Verify printer permissions before granting access.
- Avoid installing unnecessary printer management software.
- Keep firmware and drivers updated.

---

# Common Issues

| Issue | Resolution |
|--------|------------|
| Printer Offline | Verify power and network connectivity |
| Driver Not Found | Install approved driver |
| Test Page Fails | Restart Print Spooler |
| Access Denied | Verify AD group membership |
| Printer Not Found | Add manually using TCP/IP |

---

# Escalation Criteria

Escalate if:

- Printer hardware failure suspected.
- Printer unreachable on the network.
- Print server unavailable.
- Driver compatibility issue persists.
- Network Team confirms connectivity issue.

---

# Estimated Completion Time

20–30 Minutes

---

# Related Technologies

- Windows 11
- Print Management
- TCP/IP
- Active Directory
- ServiceNow

---

# Version History

| Version | Date | Author | Changes |
|----------|------|--------|---------|
| 1.0 | July 2026 | Service Desk | Initial Release |
