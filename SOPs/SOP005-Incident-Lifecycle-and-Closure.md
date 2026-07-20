# SOP 005 – Incident Lifecycle and Closure Procedure

---

# Purpose

This Standard Operating Procedure (SOP) defines the standard Incident Management lifecycle followed by the Service Desk. It ensures incidents are handled consistently, resolved within SLA, and documented according to ITIL best practices.

---

# Scope

Applicable to all Service Desk (L1) engineers responsible for managing incidents from initial logging through final closure.

---

# Incident Lifecycle

```
User Reports Issue
        │
        ▼
Incident Logged
        │
        ▼
Categorization & Prioritization
        │
        ▼
Initial Investigation
        │
        ▼
Troubleshooting
        │
        ▼
Resolved?
   ┌─────────────┐
   │             │
  Yes           No
   │             │
   ▼             ▼
User      Escalate to
Verification    L2/L3
   │             │
   └──────┬──────┘
          ▼
Incident Closure
```

---

# Procedure

## Step 1 – Log the Incident

Create a new incident in ServiceNow.

Record:

- User Name
- Department
- Contact Information
- Device Name
- Description of Issue
- Time Reported

---

## Step 2 – Categorize the Incident

Assign:

- Category
- Subcategory
- Assignment Group
- Impact
- Urgency
- Priority

Example:

| Category | Subcategory |
|-----------|-------------|
| Software | Microsoft Outlook |
| Network | VPN |
| Hardware | Printer |

---

## Step 3 – Initial Investigation

Collect:

- Error messages
- Screenshots
- Recent changes
- Number of affected users
- Business impact

Perform basic diagnostics before escalating.

---

## Step 4 – Troubleshooting

Follow approved troubleshooting procedures.

Document every action performed.

Examples:

- Restart application
- Verify network connectivity
- Reset password
- Restart service
- Reinstall software
- Update drivers

---

## Step 5 – Determine Resolution

If the issue is resolved:

- Verify functionality.
- Ask the user to confirm resolution.

If unresolved:

- Escalate to the appropriate L2 or L3 support team.
- Include all troubleshooting notes and evidence.

---

## Step 6 – User Verification

Confirm that:

- The reported issue is resolved.
- Business operations have resumed.
- No additional problems remain.

---

## Step 7 – Document Resolution

Record:

- Root Cause
- Troubleshooting Steps
- Resolution
- Verification Results
- Preventive Actions
- Resolution Time

---

## Step 8 – Close the Incident

Before closing, verify:

- ✔ User Confirmation Received
- ✔ Root Cause Documented
- ✔ Resolution Documented
- ✔ SLA Met
- ✔ Work Notes Complete
- ✔ Appropriate Resolution Code Selected

Update the ticket status to **Closed**.

---

# Security Best Practices

- Verify user identity before making account changes.
- Never close incidents without user confirmation unless approved by policy.
- Document all troubleshooting activities accurately.
- Do not expose sensitive information in work notes.

---

# Common Resolution Codes

| Resolution Code | Example |
|-----------------|---------|
| Configuration Fixed | VPN Configuration Updated |
| Password Reset | AD Password Reset |
| Hardware Replaced | Printer Replaced |
| Software Reinstalled | Outlook Reinstalled |
| User Education | Incorrect Usage Explained |

---

# Escalation Criteria

Escalate when:

- Issue exceeds L1 scope.
- Server or infrastructure failure suspected.
- Multiple users affected.
- Security incident suspected.
- Vendor support required.

---

# Estimated Completion Time

Varies depending on incident priority and SLA.

---

# Related Technologies

- ServiceNow
- Active Directory
- Microsoft 365
- Windows 11
- VPN
- Networking
- Printers

---

# ITIL Concepts Covered

- Incident Management
- Incident Categorization
- Prioritization
- Functional Escalation
- Major Incident Identification
- Service Restoration
- Incident Closure
- SLA Compliance

---

# Version History

| Version | Date | Author | Changes |
|----------|------|--------|---------|
| 1.0 | July 2026 | Service Desk | Initial Release |
