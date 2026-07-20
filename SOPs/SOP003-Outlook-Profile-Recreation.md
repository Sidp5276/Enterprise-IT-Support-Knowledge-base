# SOP 003 – Outlook Profile Recreation Procedure

---

# Purpose

This SOP provides the standard procedure for recreating a Microsoft Outlook profile to resolve issues such as Outlook not opening, repeated password prompts, synchronization failures, corrupted mail profiles, or send/receive errors.

---

# Scope

Applicable to all Service Desk (L1) engineers supporting Microsoft Outlook on Windows devices.

---

# Prerequisites

- Outlook Installed
- User Identity Verified
- Active Internet Connection
- Microsoft 365 License Active
- Administrator Rights (if required)

---

# Common Symptoms

- Outlook will not open
- Outlook crashes on startup
- Constant password prompts
- Mailbox not syncing
- Send/Receive errors
- OST corruption
- Search not working

---

# Procedure

## Step 1 – Verify Issue

Ask the user:

- When did the issue start?
- Is Outlook opening?
- Are other Microsoft 365 apps working?
- Is the issue affecting only one mailbox?

---

## Step 2 – Close Outlook

Ensure Outlook is completely closed.

End any remaining Outlook processes using Task Manager.

---

## Step 3 – Open Mail Settings

Navigate to:

**Control Panel → Mail (Microsoft Outlook)**

Select:

**Show Profiles**

---

## Step 4 – Create New Profile

Select:

**Add**

Provide a meaningful profile name.

Example:

```
Outlook_New
```

---

## Step 5 – Configure Mailbox

Enter:

- User Name
- Email Address
- Password

Allow Outlook to automatically configure the mailbox.

---

## Step 6 – Set Default Profile

Select:

**Always use this profile**

Choose the newly created profile.

---

## Step 7 – Launch Outlook

Open Outlook.

Allow mailbox synchronization to complete.

---

## Step 8 – Verify Functionality

Confirm:

- Emails synchronize
- Calendar opens
- Contacts available
- Send/Receive successful
- Search working

---

## Step 9 – Remove Old Profile (Optional)

Once the new profile is confirmed working:

Delete the old Outlook profile.

---

## Step 10 – Update ServiceNow

Document:

- Original issue
- Profile recreated
- Mailbox synchronized
- User confirmation received

Close the incident.

---

# Security Best Practices

- Never store user passwords.
- Verify user identity before modifying profiles.
- Back up local PST files if required.
- Remove unused Outlook profiles.

---

# Common Issues

| Issue | Resolution |
|--------|------------|
| Autodiscover Fails | Verify DNS and Internet |
| Password Prompt | Re-enter Microsoft 365 credentials |
| Mailbox Not Syncing | Check Exchange Online |
| OST Corruption | Create new Outlook profile |
| Slow Synchronization | Allow mailbox indexing to complete |

---

# Escalation Criteria

Escalate if:

- Exchange Online outage exists
- Mailbox cannot be provisioned
- Autodiscover repeatedly fails
- Microsoft 365 licensing issues persist
- Profile recreation does not resolve the issue

---

# Estimated Completion Time

20–30 Minutes

---

# Related Technologies

- Microsoft Outlook
- Microsoft 365
- Exchange Online
- Windows 11
- ServiceNow

---

# Version History

| Version | Date | Author | Changes |
|----------|------|--------|---------|
| 1.0 | July 2026 | Service Desk | Initial Release |
