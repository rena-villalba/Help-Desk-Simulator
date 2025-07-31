# Scenario 03: Disabled Account

## 🎫 Ticket
**Requester**: Santiago Villa
**Subject**: Disabled Account
**Description**: “Can someone help me, I think there's an issue with my account.”

## 🔍 Client-side reproduction
- Screenshot of disabled account on the client VM (path: screenshots/3.disabled_account_ticket/)
- Evidence the account is disabled on the login screen

## 🖥️ Investigation (on DC/AD server)
- Steps performed in ADUC:
  - Found user “s.villa”
  - Confirmed `Account is disabled`
  - Enable account
- Screenshots of ADUC actions

## 🧾 Ticket resolution in FreshService
- Internal note: “Account enabled at 10:38 PM.”
- Response to user: “Sorry for the trouble, your account is already enabled.”

## ✅ Validation
- Screenshot of successful login on client VM

## 📄 Lessons Learned

- Disabled accounts can result from offboarding actions, policy-based automation, or manual administrative error — it's important to verify **why** the account was disabled before re-enabling it.
- Always check with HR or the manager before reactivating a disabled user to avoid security risks or policy violations.
- Clear documentation and user lifecycle procedures (e.g., onboarding, role changes, offboarding) help prevent unauthorized or accidental account disablement.
- ADUC makes it easy to visually identify and re-enable accounts, but it's crucial to confirm group memberships and login restrictions haven’t been altered before reactivating.
- Proactive monitoring (e.g., daily reports on disabled accounts) can help detect anomalies or ensure expected actions were completed as planned.
