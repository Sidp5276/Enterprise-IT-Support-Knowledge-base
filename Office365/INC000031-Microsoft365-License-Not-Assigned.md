# Ticket 031 – Microsoft 365 License Not Assigned

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000031 |
| Priority | P2 |
| Category | Microsoft 365 |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Human Resources |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported being unable to access Outlook, Microsoft Teams, and OneDrive after receiving a new company laptop.

Errors observed:

- "Your mailbox couldn't be found."
- "License required."
- Teams sign-in unsuccessful.

---

# Environment

- Windows 11 Enterprise
- Microsoft 365
- Microsoft Entra ID (Azure AD)
- Exchange Online

---

# Business Impact

- User unable to send or receive emails.
- Teams unavailable.
- OneDrive inaccessible.
- New employee onboarding delayed.

---

# Initial Investigation

Collected Information:

- User account successfully synchronized with Microsoft Entra ID.
- Password authentication successful.
- Internet connectivity normal.
- Multiple Microsoft 365 applications unavailable.

---

# Possible Causes

- Microsoft 365 License Not Assigned
- License Assignment Delay
- Incorrect License Type
- Provisioning In Progress

---

# Troubleshooting Steps

### Step 1

Verified user account in Microsoft 365 Admin Center.

Result:

User account found successfully.

---

### Step 2

Opened:

Users → Active Users

Selected affected user.

---

### Step 3

Checked **Licenses and Apps**.

Observed:

❌ No Microsoft 365 license assigned.

---

### Step 4

Assigned:

✔ Microsoft 365 Business Premium License

Saved changes.

---

### Step 5

Waited for Microsoft 365 provisioning to complete.

Approximate provisioning time:

5–10 minutes.

---

### Step 6

Asked user to sign out and sign back into:

- Outlook
- Teams
- OneDrive

---

### Step 7

Verified service availability.

✔ Outlook mailbox created.

✔ Teams login successful.

✔ OneDrive synchronized successfully.

---

# Root Cause Analysis (RCA)

The user account was created successfully, but no Microsoft 365 license had been assigned during the onboarding process. Without an assigned license, Microsoft 365 services such as Exchange Online, Teams, and OneDrive could not be provisioned.

---

# Resolution

- Assigned Microsoft 365 Business Premium license.
- Allowed provisioning to complete.
- Verified successful access to all Microsoft 365 services.

---

# Verification

- Outlook Working
- Exchange Mailbox Available
- Teams Login Successful
- OneDrive Sync Working
- User Confirmed Resolution

---

# User Communication Log

09:15 AM – Ticket Logged

09:22 AM – License Verification Started

09:28 AM – License Assigned

09:36 AM – Microsoft 365 Provisioning Completed

09:40 AM – User Confirmed Resolution

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Include Microsoft 365 license assignment in onboarding checklist.
- Verify license provisioning before handing over new laptops.
- Periodically audit unlicensed user accounts.

---

# Tools Used

- Microsoft 365 Admin Center
- Microsoft Entra Admin Center

---

# Technologies Used

- Microsoft 365
- Microsoft Entra ID (Azure AD)
- Exchange Online
- Microsoft Teams
- OneDrive

---

# Interview Questions

1. Why is a Microsoft 365 license required?
2. What happens if a user has no Exchange Online license?
3. What is Microsoft Entra ID (formerly Azure AD)?
4. How do you assign a Microsoft 365 license?
5. Why might Teams and OneDrive stop working if a license is removed?

---

# Knowledge Learned

Assigning a Microsoft 365 license is one of the first tasks performed during user onboarding. Many Microsoft cloud services—including Exchange Online, Teams, and OneDrive—depend on the appropriate license being assigned before they become available to the user.

---

# Ticket Status

Closed

---

# Resolution Time

25 Minutes
