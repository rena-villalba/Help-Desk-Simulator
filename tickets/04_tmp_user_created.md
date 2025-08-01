# Scenario 04: Temporary User Account Creation (Requested by HR)

## Screenshots Folder
- [Ticket 4 – Temporary User Account Creation](../screenshots/4.tmp_user_ticket)
  
## 🎫 Ticket
**Requester**: Juan Vitoli (HR Department)  
**Subject**: Request to Create Temporary User Account for New Contractor  
**Description**:  
Hello IT Team,

We need to create a temporary domain user account for a new contractor joining the HR team for a short-term project.

Please create the account with the following details:

- Full Name: Facundo Burgos
- Department: Human Resources
- Job Title: HR Data Entry Assistant
- Temporary access: 30 days
- Group membership: HR
- Shared folder access: \\hr-share\data-entry
- Email: Not required
- Workstation: Will be using HR-WS-06
- Account expiration: August 31, 2025
- Password: Please share temporary credentials with HR once set

Let me know once the account is ready.

Thank you,  
Juan Vitoli
Human Resources 

---

## 🔍 Investigation & Planning (IT Team – DC Server)

- Verified with HR that the request is valid and timeframe is correct.
- Checked existing users to ensure the username `f.burgos` is available.
- Created a plan to:
  - Set account expiration date.
  - Confirm login access without email or additional privileges.

---

## 🛠️ Resolution Steps

- Opened **Active Directory Users and Computers (ADUC)**.
- Created new user:
  - Full Name: Facundo Burgos
  - Username: f.burgos
  - Password: TempPassword11
  - Enabled "User must change password at next login"
  - Set **account expiration** for the requested end date
- Verified user appears in AD and account status is **enabled**.

---

## 🧾 Ticket Update

**Internal Note**:  
Temporary account `f.burgos` created for Facundo Burgos with expiration set for Aug 31. Account added to `TempUsers` group. No email access granted as requested.

**Reply to Requester**:  
Hi Juan,  
I want to inform you that the requested user has been created with an expiration date of August 31. Here are the credentials:

User: f.burgos
Password: TempPassword11

Please let me know if there are any issues.

---

## ✅ Validation

- Confirmed that the account:
  - Appears in AD.
  - Can log in from a domain-joined client VM.

---

## 📄 Lessons Learned

- Temporary accounts should always have expiration dates to minimize security risks.
- Creating a dedicated OU or group for temp users simplifies access control and cleanup.
- It's important to confirm access scope with HR or the requester to avoid over-provisioning.
- Documenting the request and the account details in FreshService ensures traceability and compliance.
- Periodic review of temporary accounts can help prevent unused accounts from remaining active beyond their intended timeframe.
