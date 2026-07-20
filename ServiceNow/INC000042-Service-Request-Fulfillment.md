# Ticket 042 – Service Request Fulfillment (New Employee Onboarding)

---

## Ticket Information

| Field | Value |
|-------|---------|
| Request ID | REQ000042 |
| RITM | RITM000042 |
| Priority | Medium |
| Category | Service Request |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | New Employee Laptop |
| Operating System | Windows 11 Enterprise |
| SLA | 1 Business Day |

---

# User Request

Human Resources submitted a request for onboarding a new employee requiring access to standard company resources before the employee's joining date.

Requested services:

- Microsoft Office 365
- VPN Access
- Shared Network Drive
- Outlook Mailbox
- Microsoft Teams

---

# Environment

- Windows 11 Enterprise
- Microsoft 365
- Active Directory
- VPN Client
- Exchange Online

---

# Business Impact

The new employee could not begin work until all required software and access permissions were provisioned.

---

# Initial Verification

Verified:

- HR Approval Available
- Manager Approval Completed
- Employee Account Created
- Laptop Ready for Deployment

---

# Request Fulfillment Steps

### Step 1

Opened ServiceNow Service Catalog.

Located:

**New Employee Onboarding Request**

---

### Step 2

Verified Request.

Generated:

REQ000042

Associated Requested Item:

RITM000042

---

### Step 3

Created fulfillment tasks:

- Install Microsoft Office
- Assign Microsoft 365 License
- Configure Outlook
- Install VPN Client
- Map Shared Network Drive

---

### Step 4

Installed Microsoft Office 365.

Activation completed successfully.

---

### Step 5

Assigned Microsoft 365 Business Premium License.

Provisioning completed.

---

### Step 6

Configured Outlook profile.

Verified mailbox synchronization.

---

### Step 7

Installed VPN Client.

Verified successful connection to corporate network.

---

### Step 8

Mapped departmental shared drive.

Verified read/write permissions.

---

### Step 9

Installed Microsoft Teams.

Verified successful login.

---

### Step 10

Completed all Service Catalog Tasks.

Updated Request as Fulfilled.

---

# Root Cause Analysis (RCA)

Not Applicable.

This was a planned Service Request rather than an Incident.

---

# Resolution

- Office Installed
- Outlook Configured
- Microsoft 365 Activated
- VPN Configured
- Teams Operational
- Shared Drive Accessible

---

# Verification

- Employee Logged In Successfully
- Outlook Working
- Teams Working
- VPN Connected
- Shared Folder Accessible

---

# User Communication Log

08:30 AM – Request Received

08:40 AM – Approvals Verified

09:10 AM – Software Installed

09:30 AM – Access Configured

09:45 AM – Employee Verified Setup

---

# Escalation Decision

No escalation required.

Completed by Service Desk L1.

---

# Preventive Actions

- Maintain standardized onboarding checklist.
- Verify approvals before fulfillment.
- Test all applications before handing over the device.

---

# Tools Used

- ServiceNow
- Microsoft 365 Admin Center
- Active Directory Users and Computers
- VPN Client

---

# Technologies Used

- Microsoft 365
- Active Directory
- Exchange Online
- Microsoft Teams
- VPN
- Windows 11

---

# ITIL Concepts Demonstrated

- Service Request Management
- Request Fulfillment
- Service Catalog
- REQ
- RITM
- Catalog Tasks (SCTASK)
- Approval Workflow

---

# Interview Questions

1. What is the difference between an Incident and a Service Request?
2. What are REQ, RITM, and SCTASK in ServiceNow?
3. Why are approvals required before fulfilling a request?
4. What is Request Fulfillment in ITIL?
5. What information should be documented before closing a Service Request?

---

# Knowledge Learned

Unlike incidents, service requests are planned and follow predefined workflows. In ServiceNow, a request begins with a **REQ**, generates one or more **RITMs**, and is completed through **SCTASKs** assigned to the appropriate support teams. Understanding this lifecycle is essential for enterprise IT Service Desk roles.

---

# Ticket Status

Closed

---

# Resolution Time

1 Hour 15 Minutes
