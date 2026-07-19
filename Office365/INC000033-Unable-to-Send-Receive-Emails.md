# Ticket 033 – Unable to Send or Receive Emails

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000033 |
| Priority | P1 |
| Category | Exchange Online |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Finance |
| Device | Dell Latitude 5430 |
| Operating System | Windows 11 Enterprise |
| SLA | 2 Hours |

---

# User Reported Issue

The user reported that Outlook displayed the error:

> "Cannot send or receive emails."

Messages remained in the Outbox and no new emails were received.

---

# Environment

- Windows 11 Enterprise
- Microsoft 365
- Exchange Online
- Outlook Desktop

---

# Business Impact

- Customer communication interrupted.
- Financial approvals delayed.
- Business operations affected.

---

# Initial Investigation

- Internet connectivity verified.
- Outlook running.
- Other Microsoft 365 services operational.

---

# Possible Causes

- Outlook Working Offline
- Mailbox Quota Exceeded
- Authentication Failure
- Exchange Online Service Issue
- Corrupted Outlook Profile

---

# Troubleshooting Steps

### Step 1

Verified Outlook connection.

Status:

Working Offline enabled.

---

### Step 2

Disabled:

**Send/Receive → Work Offline**

---

### Step 3

Performed Send/Receive.

```text
F9
```

Outbox processing started.

---

### Step 4

Verified mailbox quota in Microsoft 365 Admin Center.

Mailbox within limits.

---

### Step 5

Sent test email.

Email delivered successfully.

---

### Step 6

Received test email.

Inbox updated immediately.

---

# Root Cause Analysis (RCA)

Outlook had been accidentally switched to **Work Offline** mode, preventing synchronization with Exchange Online.

---

# Resolution

- Disabled Work Offline mode.
- Performed mailbox synchronization.
- Verified successful mail flow.

---

# Verification

- Emails Sending Successfully
- Emails Receiving Successfully
- Outbox Empty
- User Confirmed Resolution

---

# Preventive Actions

- Educate users on Outlook Offline Mode.
- Verify connection status before troubleshooting Exchange.
- Keep Outlook updated.

---

# Tools Used

- Outlook Desktop
- Microsoft 365 Admin Center

---

# Technologies Used

- Microsoft 365
- Exchange Online
- Outlook

---

# Interview Questions

1. Why would Outlook show "Working Offline"?
2. How do you verify if Exchange Online is the problem?
3. What happens if the mailbox quota is full?
4. How would you troubleshoot emails stuck in the Outbox?
5. Difference between Outlook connectivity issues and Exchange server issues?

---

# Knowledge Learned

Always check Outlook's connection status before assuming an Exchange Online issue. Simple settings such as **Work Offline** can prevent email synchronization even when the network and mailbox are functioning correctly.

---

# Ticket Status

Closed

---

# Resolution Time

18 Minutes
