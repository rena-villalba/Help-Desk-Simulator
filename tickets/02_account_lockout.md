# Scenario 02: Account Lockout

## 🎫 Ticket
**Requester**: Melisa Cetion (Sales)
**Subject**: Account locked after multiple login attempts (4 attempts) 
**Description**: “I tried logging in four times and now can’t sign in.”

## 🔍 Client-side reproduction
- Screenshot of failed logins on the client VM (path: screenshots/2.locked_account_ticket/)
- Evidence the account is locked on the login screen

## 🖥️ Investigation (on DC/AD server)
- Steps performed in ADUC:
  - Found user “m.cetion”
  - Confirmed `Account is locked out`
  - Reset / unlocked account
- Screenshots of ADUC actions

## 🧾 Ticket resolution in FreshService
- Internal note: “Account unlocked at 09:30 PM.”
- Response to user: “I've checked the problem and it's already fixed.”

## ✅ Validation
- Screenshot of successful login on client VM

## 📄 Lessons Learned

- Account lockouts are typically caused by repeated login attempts with incorrect credentials, but they can also be triggered by background services, mapped drives, or old sessions still using outdated passwords.
- Before unlocking an account, it’s important to verify the reason for the lockout — recurring issues may indicate a misconfigured application or a user device storing an outdated password.
- A well-configured GPO for lockout threshold, duration, and reset counter can reduce brute-force attack exposure while balancing usability.
- Lockout auditing should be enabled to allow faster investigation using Event Viewer or PowerShell tools (`Get-EventLog`, `Get-ADUser -LockedOut`).
- Training users to recognize lockouts and report them with proper context (e.g., “I recently changed my password”) can improve help desk efficiency.

