# Ticket 051 – VPN Authentication Failure

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000051 |
| Priority | P2 |
| Category | Network |
| Subcategory | VPN Authentication |
| Status | Closed |
| Assigned Group | Service Desk L1 |
| Department | Sales |
| Device | Dell Latitude 5440 |
| Operating System | Windows 11 Enterprise |
| VPN Client | Cisco AnyConnect Secure Mobility Client |
| SLA | 4 Hours |

---

# User Reported Issue

The user reported being unable to connect to the corporate VPN while working remotely.

Error displayed:

> "Authentication Failed. Login Denied."

The user confirmed that the Windows password had recently been changed.

---

# Environment

- Windows 11 Enterprise
- Cisco AnyConnect VPN
- Active Directory
- Corporate VPN Gateway

---

# Business Impact

- User unable to access internal applications.
- Shared drives inaccessible.
- Customer work delayed.

---

# Initial Investigation

Collected Information:

- Internet connectivity verified.
- VPN server reachable.
- Username entered correctly.
- Windows login successful.

---

# Possible Causes

- Expired Cached Credentials
- Incorrect Password
- Active Directory Password Recently Changed
- Account Locked
- VPN Authentication Failure

---

# Troubleshooting Steps

### Step 1

Verified internet connectivity.

```cmd
ping 8.8.8.8
```

Successful.

---

### Step 2

Verified VPN gateway connectivity.

```cmd
ping vpn.company.local
```

Successful.

---

### Step 3

Verified Active Directory account.

Account active.

Password recently changed.

---

### Step 4

Asked user to enter the updated Active Directory password.

Authentication still failed.

---

### Step 5

Cleared cached VPN credentials.

Restarted Cisco AnyConnect.

---

### Step 6

User authenticated again using updated credentials.

VPN connected successfully.

---

### Step 7

Verified access to:

- Shared Drives
- ERP Application
- Internal HR Portal

---

# Root Cause Analysis (RCA)

The VPN client was attempting to authenticate using cached credentials from the user's previous password. Clearing the cached credentials and re-authenticating with the updated Active Directory password restored VPN access.

---

# Resolution

- Cleared cached VPN credentials.
- Restarted VPN client.
- Re-authenticated user.
- Verified VPN connectivity.

---

# Verification

- VPN Connected
- Internal Resources Accessible
- User Confirmed Resolution

---

# User Communication Log

09:10 AM – Incident Logged

09:20 AM – Password Change Verified

09:30 AM – Cached Credentials Cleared

09:35 AM – VPN Connected Successfully

---

# Escalation Decision

No escalation required.

Resolved by Service Desk L1.

---

# Preventive Actions

- Advise users to update saved VPN credentials after changing passwords.
- Keep VPN client updated.
- Clear cached credentials if authentication issues occur.

---

# Tools Used

- ServiceNow
- Cisco AnyConnect
- Active Directory Users and Computers

---

# Commands Used

```cmd
ping 8.8.8.8
ping vpn.company.local
```

---

# Technologies Used

- Cisco AnyConnect
- Active Directory
- Windows 11
- VPN

---

# Interview Questions

1. Why can VPN authentication fail after a password change?
2. What are cached credentials?
3. How would you verify whether the problem is with the VPN server or the user's account?
4. What information should be checked before escalating a VPN issue?
5. Why is Active Directory authentication important for VPN access?

---

# Knowledge Learned

VPN authentication issues commonly occur after password changes because the VPN client may continue using cached credentials. Verifying network connectivity, Active Directory account status, and cached credentials are standard L1 troubleshooting steps before escalation.

---

# Ticket Status

Closed

---

# Resolution Time

30 Minutes
