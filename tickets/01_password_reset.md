# Scenario 01: Password Reset

## 🎫 Ticket
**Requester**: Juan Vitoli (HR Department)
**Subject**: Reset Password 
**Description**: “Hi! I forgot my password so can someone help me to reset it please, my user is jj.vitoli. Thanks.”

## 🖥️ Investigation (on DC/AD server)
- Steps performed in ADUC:
  - Found user “jj.vitoli”
  - Reset user password
- Screenshots of ADUC actions

## 🧾 Ticket resolution in FreshService
- Internal note: “Password reset at 10:45 PM.”
- Response to user: “I've reset your password and the temporary credential is TemporalPassword$$ so please when you have time, log in and change the password.”

## ✅ Validation
- Screenshot of successful update of new password
- Screenshot of successful login on client VM

## 📄 Lessons Learned

- Password reset requests are one of the most common support tasks and should follow clear identity verification steps before being fulfilled.
- Ensuring that users change their temporary passwords upon next login improves security and aligns with best practices.
- GPO settings such as password complexity and expiration policies must be consistent to avoid user confusion and increase account protection.
- Resetting a password without checking if the account is **disabled** or **locked out** may result in repeated tickets — always check account status first.
