# Ticket 007 – Windows Activation Error

---

## Ticket Information

| Field | Value |
|-------|---------|
| Ticket ID | INC000007 |
| Priority | P2 |
| Category | Windows Licensing |
| Status | Closed |
| Department | Administration |
| Device | Lenovo ThinkPad T14 |
| Operating System | Windows 11 Enterprise |

---

# User Reported Issue

The user reported that Windows displayed:

> "Activate Windows"

Certain personalization settings were disabled.

---

# Environment

- Windows 11 Enterprise
- Domain Joined
- KMS Activated
- Office Network

---

# Initial Investigation

Information collected:

- Device recently reimaged.
- User connected to office network.
- Internet available.
- Other systems activated successfully.

---

# Possible Causes

- KMS server unreachable
- Activation expired
- Incorrect Windows edition
- Network issue
- Licensing service stopped

---

# Troubleshooting Steps

### Step 1

Verified internet connectivity.

```cmd
ping google.com
```

Successful.

---

### Step 2

Verified KMS Server connectivity.

```cmd
ping kms.company.local
```

Successful.

---

### Step 3

Checked activation status.

```cmd
slmgr /xpr
```

Observed activation expired.

---

### Step 4

Forced activation.

```cmd
slmgr /ato
```

Activation completed successfully.

---

### Step 5

Verified activation again.

```cmd
slmgr /xpr
```

Windows permanently activated.

---

### Step 6

Restarted workstation.

Activation message disappeared.

---

# Root Cause Analysis (RCA)

Windows license activation expired because the workstation had not contacted the corporate KMS server for an extended period.

---

# Resolution

Connected system to KMS server.

Forced activation.

Verified successful licensing.

---

# Verification

- Windows activated
- Personalization restored
- No activation warning
- User confirmed issue resolved

---

# Preventive Actions

- Connect corporate devices to office network periodically.
- Verify KMS connectivity.
- Monitor license expiry.

---

# Commands Used

```cmd
ping kms.company.local

slmgr /xpr

slmgr /ato
```

---

# Technologies Used

- Windows Licensing
- KMS
- CMD
- Windows Enterprise

---

# Knowledge Learned

- Enterprise Windows uses KMS activation.
- `slmgr` is the primary Windows licensing utility.
- KMS activation requires periodic communication with the activation server.

---

# Ticket Status

Closed

---

# Resolution Time

20 Minutes
