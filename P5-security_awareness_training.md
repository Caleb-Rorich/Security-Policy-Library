# Security Awareness Training

**Version:** 1.0 | **Audience:** All Staff | **Duration:** ~30 minutes  
**Completion:** Required annually for all employees and contractors

---

## Introduction

Cybersecurity is not just an IT problem — it is everyone's responsibility. The majority of successful cyberattacks begin not with sophisticated technical hacking, but with a human error: clicking a link, reusing a password, or holding a door open for a stranger.

This training covers the four most critical security behaviours every employee must practice. By the end, you will be able to recognise and respond to the most common threats you will face.

---

## Module 1 — Phishing Recognition

### What Is Phishing?

Phishing is an attempt to trick you into revealing sensitive information (passwords, card numbers) or installing malware by disguising a malicious message as legitimate.

**Types you need to know:**
- **Email phishing** — mass-sent fake emails pretending to be your bank, Microsoft, or your company
- **Spear phishing** — targeted attacks using your name, role, or company details to appear credible
- **Smishing** — phishing via SMS text message
- **Vishing** — phishing via phone call ("I'm from IT Support, I need your password to fix your account")

---

### Red Flags Checklist

Before clicking **any** link or opening **any** attachment, check for these warning signs:

**Sender:**
- [ ] Does the sender's email address match the display name? (hover over the name)
- [ ] Is the domain slightly misspelled? (`paypa1.com` vs `paypal.com`, `microsoFt.com`)
- [ ] Did you expect an email from this person/organisation?

**Content:**
- [ ] Does it create urgency or fear? ("Your account will be suspended in 24 hours!")
- [ ] Does it ask you to click a link to "verify" or "update" credentials?
- [ ] Does it contain generic greetings? ("Dear Customer" instead of your name)
- [ ] Are there grammar errors or unusual phrasing?

**Links:**
- [ ] Hover over the link — does the URL shown match where it claims to go?
- [ ] Does the URL start with `https://`?
- [ ] Is the domain unfamiliar or very long with many subdomains?

**Attachments:**
- [ ] Did you expect this attachment?
- [ ] Is it an unusual file type? (`.exe`, `.zip`, `.iso`, double extensions like `invoice.pdf.exe`)
- [ ] Does the email pressure you to enable macros?

---

### 🎯 Scenario — What Would You Do?

> You receive an email from `IT-Support@company-helpdesk.net` with the subject "URGENT: Your password expires in 2 hours." The email contains a link to "reset your password immediately." The link goes to `company-portal.login-secure.net`.

**Red flags in this scenario:**
1. Sender domain is `company-helpdesk.net` — not the company's real domain
2. Urgency language ("URGENT", "2 hours")
3. Link domain `login-secure.net` is not the company's domain — it's a lookalike

**Correct action:** Do NOT click. Forward the email to `security@company.com` and delete it.

---

### What To Do If You Receive a Suspicious Email

1. **Do NOT click** links or open attachments
2. **Report it** by forwarding the full email (with headers) to: `security@[company.com]`
3. **Delete** the email from your inbox
4. If you already clicked: **disconnect from Wi-Fi/network immediately** and call IT Security on ext. [####]

> 💡 **You will never be in trouble for reporting a suspicious email — even if it turns out to be legitimate. You WILL create problems by ignoring it.**

---

## Module 2 — Password Hygiene

### Why Passwords Matter

Every week, millions of stolen username and password combinations are sold on the dark web. If your password from one breached website is reused on your work email, an attacker can log in to your work account without any hacking.

---

### The Three Password Rules

**Rule 1: Make it long.** Length is the most important factor. A 12-character random password takes billions of years to crack by brute force. An 8-character password can be cracked in hours.

```
Weak:    Password1       (8 chars, dictionary word + number = cracked in minutes)
Better:  P@ssw0rd!2024   (12 chars, but predictable pattern = cracked faster than it looks)
Strong:  Tr0pical$Monkey!Lamp  (20 chars, random words + symbols = not crackable)
```

**Rule 2: Make it unique.** Every account needs its own password. If you reuse passwords and one site is breached, all your accounts with that password are compromised.

**Rule 3: Use a password manager.** You cannot remember 50 unique, strong passwords. You do not need to — a password manager does it for you. The master password is the only one you need to remember.

---

### What IT Will NEVER Ask You

- ❌ "Please tell me your password so I can fix your account"
- ❌ "Enter your credentials on this external website to reset your access"
- ❌ "Send me your password by email or Teams"

**IT does not need your password to manage your account.** If anyone — including someone claiming to be IT — asks for your password, this is a social engineering attempt. Report it immediately.

---

### 🎯 Scenario — What Would You Do?

> You get a Teams message from "IT_Support_John" saying your account is flagged for suspicious activity. He asks you to reply with your current password so he can "verify your identity" and fix the issue.

**Correct action:** Do NOT provide the password. Call IT directly on the known helpdesk number to verify. Report the Teams message to IT Security.

---

## Module 3 — Social Engineering

### What Is Social Engineering?

Social engineering is psychological manipulation to trick you into revealing information or taking an action that compromises security. It targets people, not systems — because people are often easier to manipulate than software.

---

### Common Tactics

**Pretexting:** The attacker creates a believable false scenario.
> "Hi, I'm from your company's IT vendor. I need access to your system to perform an urgent maintenance task."

**Impersonation:** Pretending to be someone you trust — a manager, colleague, or IT support.
> "This is David from senior management. I need you to transfer $50,000 urgently. I'll explain later."

**Tailgating / Piggybacking:** Following a legitimate employee through a secured door without swiping their own card.

**Quid pro quo:** Offering something in exchange for information or access.
> "I'll give you a free USB drive if you fill out this quick survey" — USB may contain malware.

---

### How to Defend Against Social Engineering

1. **Verify identity independently.** If someone calls claiming to be your manager or IT, hang up and call them back on a known number.
2. **Question urgency.** Artificial urgency is a manipulation tactic. Legitimate requests rarely require bypassing security controls.
3. **Challenge unknown visitors.** If you see someone in a secure area without a visible badge, politely ask them to identify themselves or call security.
4. **Do not tailgate or allow tailgating.** Every person must badge in individually, even if it feels rude to let a door close on someone.

---

### 🎯 Scenario — What Would You Do?

> A well-dressed person approaches the office entrance while you're entering. They say they forgot their badge and are running late to a meeting with your CEO. They ask you to swipe them in.

**Correct action:** Apologise but decline. Direct them to reception to sign in as a visitor. Even if they're genuine, the procedure protects both of you.

---

## Module 4 — Incident Reporting

### Why Reporting Matters

**The faster an incident is reported, the faster it is contained.** The average time to detect a breach without prompt reporting is 207 days (IBM Cost of a Data Breach Report). Many of those breaches were noticed by employees who assumed "it's probably nothing."

> **There is no such thing as "probably nothing" in security. Report it and let IT Security decide.**

---

### What to Report

| Event | Report it? |
|-------|-----------|
| I clicked a suspicious link | ✅ YES — immediately |
| I received a phishing email (didn't click) | ✅ YES — forward and delete |
| Someone asked for my password | ✅ YES |
| My computer is acting strangely (slow, pop-ups, unusual processes) | ✅ YES |
| I lost a work device or USB drive | ✅ YES — immediately |
| I saw someone in a secure area without a badge | ✅ YES |
| My account was locked out unexpectedly | ✅ YES — may indicate brute force |
| "It's probably fine" | ✅ Report it anyway. You won't get in trouble. |

---

### How to Report

| Situation | Action |
|-----------|--------|
| Suspicious email | Forward to `security@[company.com]` |
| Clicked something / device compromised | **Disconnect from network** → Call IT Security: ext. [####] |
| Lost device | Call IT Security immediately: ext. [####] |
| Suspicious person / physical security | Call security/reception: ext. [####] |
| Out of hours emergency | [Emergency contact number] |

---

### What Happens When You Report

1. IT Security acknowledges within 15 minutes (during business hours)
2. If needed, they will ask to look at your device — this is quick and non-disruptive
3. You will be kept informed of the outcome
4. Your report helps protect the entire organisation

**You will never be disciplined for reporting in good faith.** The only risk is not reporting.

---

## Knowledge Check

Test your understanding before completing this training:

**Q1.** An email asks you to click a link to verify your account. The sender domain looks slightly different from your company's domain. What do you do?
> ✅ Do not click. Forward to security team. Delete.

**Q2.** Someone calls claiming to be IT support and asks for your password to fix an access issue. What do you do?
> ✅ Decline. IT does not need your password. Hang up and call IT on the known number. Report the call.

**Q3.** Your computer suddenly starts running slowly and shows pop-ups you've never seen before. What do you do?
> ✅ Disconnect from the network. Call IT Security immediately. Do not power off.

**Q4.** You receive an email from a vendor you know, but the attachment is unexpected. What do you do?
> ✅ Contact the vendor through a known method (call or separate email) to verify they sent it before opening.

---

## Training Completion

By completing this training, you confirm that you:

- [ ] Understand how to recognise phishing emails
- [ ] Know your reporting procedures for security incidents
- [ ] Will use a strong, unique password (or password manager) for your accounts
- [ ] Will never share your password with anyone
- [ ] Will challenge and report suspicious physical access or social engineering attempts

**Completion record:** Submit acknowledgement via [HR system / IT ticketing portal / manager sign-off sheet]

---

*Security Awareness Training — Version 1.0 | Review annually or after significant incidents*  
*Questions: Contact IT Security at `security@[company.com]` or ext. [####]*
