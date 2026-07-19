# Ticket 032 – Outlook Mailbox Not Synchronizing

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000032 |
| Priority | P2 |
| Category | Exchange Online |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Sales |
| Device | HP EliteBook 840 G8 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported that Outlook was open but no new emails were appearing. Emails sent from colleagues were visible in Outlook Web (OWA) but not in the Outlook desktop application.

---

# Environment

- Windows 11 Enterprise
- Microsoft 365
- Outlook 365 Desktop
- Exchange Online

---

# Business Impact

- Delayed email communication.
- Missed customer emails.
- Reduced productivity.

---

# Initial Investigation

- Internet connectivity verified.
- Outlook Web (OWA) functioning normally.
- Issue isolated to Outlook desktop client.

---

# Possible Causes

- Corrupted Outlook Profile
- Cached Exchange Mode Issue
- Corrupted OST File
- Outlook Offline Mode

---

# Troubleshooting Steps

### Step 1

Verified Outlook connection status.

Result:

Connected to Microsoft Exchange.

---

### Step 2

Verified Outlook Web Access.

```text
https://outlook.office.com
```

Mailbox synchronized successfully.

---

### Step 3

Disabled and re-enabled Cached Exchange Mode.

Restarted Outlook.

---

### Step 4

Created a new Outlook profile.

Control Panel → Mail → Show Profiles → Add.

---

### Step 5

Reconfigured Microsoft 365 account.

Mailbox synchronized successfully.

---

### Step 6

Verified latest emails.

Inbox fully synchronized.

---

# Root Cause Analysis (RCA)

The existing Outlook profile had become corrupted, preventing synchronization with Exchange Online.

---

# Resolution

- Created a new Outlook profile.
- Reconfigured Microsoft 365 account.
- Mailbox synchronization restored.

---

# Verification

- Inbox Updated
- New Emails Received
- Calendar Synchronizing
- User Confirmed Resolution

---

# Preventive Actions

- Avoid abrupt Outlook shutdowns.
- Keep Outlook updated.
- Recreate profile if synchronization issues persist.

---

# Tools Used

- Outlook
- Mail Profile Settings
- Outlook Web Access (OWA)

---

# Technologies Used

- Microsoft 365
- Exchange Online
- Outlook

---

# Interview Questions

1. Difference between Outlook Desktop and Outlook Web?
2. What is an OST file?
3. What is Cached Exchange Mode?
4. Why create a new Outlook profile?
5. How do you isolate whether the issue is Outlook or Exchange?

---

# Knowledge Learned

If Outlook Web works but the desktop client does not, the problem is usually local to the user's Outlook profile or OST file rather than Exchange Online.

---

# Ticket Status

Closed

---

# Resolution Time

26 Minutes
