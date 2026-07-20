# SOP 002 – New Employee Onboarding Procedure

---

# Purpose

This Standard Operating Procedure (SOP) describes the standard process for onboarding a new employee by provisioning the required IT resources, applications, and access. The objective is to ensure the employee is productive from Day 1 while maintaining organizational security standards.

---

# Scope

Applicable to all Service Desk (L1) engineers responsible for handling New Hire requests received through ServiceNow.

---

# Prerequisites

- Approved ServiceNow Request (REQ/RITM)
- HR Approval
- Hiring Manager Approval
- Employee Details Available
- Active Directory Administrative Access
- Microsoft 365 Administrative Access

---

# Required Information

Before starting, verify:

- Employee Full Name
- Employee ID
- Department
- Manager Name
- Job Role
- Office Location
- Joining Date
- Required Applications
- Required Distribution Groups
- VPN Requirement
- Shared Folder Access

---

# Procedure

## Step 1 – Verify Request

Open the approved ServiceNow Request.

Ensure all approvals have been completed before proceeding.

---

## Step 2 – Create Active Directory Account

Using Active Directory Users and Computers:

- Create user account
- Assign username
- Set temporary password
- Enable:

✔ User must change password at next logon

---

## Step 3 – Add Security Groups

Assign required AD groups, for example:

- Domain Users
- Department Security Group
- Printer Group
- Shared Folder Group
- VPN Users

---

## Step 4 – Assign Microsoft 365 License

Assign appropriate Microsoft 365 license.

Verify activation for:

- Outlook
- Teams
- OneDrive
- Office Applications

---

## Step 5 – Configure Email

Verify mailbox creation.

Check:

- Email address
- Display name
- Global Address List visibility

---

## Step 6 – Configure VPN Access

If remote access is required:

- Enable VPN permissions
- Add VPN security group
- Provide VPN installation guide

---

## Step 7 – Verify Shared Resources

Grant access to:

- Shared Drives
- Department Folder
- SharePoint Sites
- Required Applications

---

## Step 8 – Deliver Credentials

Provide securely:

- Username
- Temporary Password
- VPN Instructions
- First Login Instructions

---

## Step 9 – User Verification

Confirm the user can successfully access:

- Windows
- Outlook
- Teams
- OneDrive
- Shared Drives
- VPN (if applicable)

---

## Step 10 – Update ServiceNow

Document:

- Account created
- License assigned
- Groups added
- User verified
- Request completed

Close the request.

---

# Security Best Practices

- Never share credentials over unsecured channels.
- Follow the principle of least privilege.
- Assign only required security groups.
- Enforce password change on first login.

---

# Common Issues

| Issue | Resolution |
|--------|------------|
| Mailbox Not Created | Verify Microsoft 365 license |
| User Cannot Login | Check AD account status |
| Teams Missing | Wait for license synchronization |
| VPN Not Working | Verify VPN group membership |
| Shared Drive Missing | Verify NTFS and Share permissions |

---

# Escalation Criteria

Escalate if:

- AD replication fails
- Microsoft 365 license assignment fails
- Mailbox provisioning exceeds expected time
- Required applications cannot be assigned
- Security approval missing

---

# Estimated Completion Time

30–60 Minutes

---

# Related Technologies

- Active Directory
- Microsoft 365
- Exchange Online
- Teams
- OneDrive
- ServiceNow
- VPN

---

# Version History

| Version | Date | Author | Changes |
|----------|------|--------|---------|
| 1.0 | July 2026 | Service Desk | Initial Release |
