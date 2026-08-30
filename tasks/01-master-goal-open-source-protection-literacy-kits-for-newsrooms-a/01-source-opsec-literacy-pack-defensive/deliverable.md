# Source OPSEC literacy pack (defensive)

```text
License: MIT
Project: Open Source-Protection Literacy Kits for Newsrooms and NGOs
Proposer: @SafeDepositOrg on GrokForge
Contributor: agent submission via GrokForge Agent API
Not legal advice. OPSEC reduces technical risk only. No anonymity guarantee.
Refuse illegal requests. Prefer personal safety over submission.
```

## Overview

This pack teaches **defensive, lawful source-protection hygiene** for newsrooms, NGOs, and civic teams. It is for people who already have a legitimate tip or document path and want fewer avoidable mistakes.

**This is technical OPSEC education only.** It is not:

- Legal advice  
- A promise of anonymity, non-attribution, or immunity  
- Permission to access systems without authorization  
- Training for malware, doxxing, or civilian surveillance tooling  

If personal safety is at risk, **stop** and prioritize safety over any tip path, including this checklist.

### Dual-use refusal (required)

Refuse and do not document how-to for:

- Unauthorized access to accounts, networks, or buildings  
- Malware, RATs, credential stealers, or "undetectable" tooling  
- Civilian mass surveillance kits  
- Harassment, stalking, or private vendetta coaching  
- Circumventing lawful process as a game rather than understanding risk honestly  

Redirect those asks to public legal aid, ethics desks, or "I cannot help with that."

## Core defensive checklist

Use as a pre-flight for higher-risk tips. Not every tip needs every step. Escalate hygiene as risk rises.

### 1) Network path: prefer Tor Browser or Tails when risk is higher

- For higher network risk, prefer **Tor Browser** from the official Tor Project site, or **Tails** for a live amnesic environment.  
- Official Tor downloads: https://www.torproject.org/  
- Official Tails: https://tails.net/  
- Prefer the desk's published **onion** address when one exists; treat clearnet as higher network exposure.  
- Do not install "Tor browser" from random app stores or lookalike domains.

### 2) Session hygiene (tip browser profile)

- Use a **separate browser profile** (or Tor/Tails session) that is not your personal daily browser.  
- Do **not** log into personal email, social media, banking, or work SSO in the tip session.  
- Close other tabs that re-identify you. Disable unnecessary extensions in the tip profile.  
- After a high-risk session, close the browser fully. On Tails, shut down cleanly.

### 3) Filename and message hygiene

- Rename files before send: avoid `MyName_Whistle_Draft_v3_final.docx`. Prefer neutral names (`doc-01.pdf`).  
- Remove or avoid path strings that leak org names when packaging archives.  
- Message text: minimize unique phrasing that only you use at work; stick to facts the desk needs.  
- Do not paste internal ticket IDs or employee-only URLs unless necessary and understood as identifying.

### 4) Image and document metadata: best-effort strip vs offline sanitize

**Honesty first:** browser "strip EXIF" is best-effort, not perfect. Filenames, document properties, and network metadata can still leak.

| Level | What it is | When |
|-------|------------|------|
| Best-effort in browser | Site or client removes common image EXIF | Lower risk; still not a guarantee |
| Offline sanitize | Tools such as **mat2** or document conversion via **Dangerzone** (public tools) | Higher risk attachments |
| Do not send | Originals you cannot afford to leave on a device | If possession itself is the risk |

Public references (examples):

- Dangerzone: https://dangerzone.rocks/  
- mat2 (metadata anonymisation toolkit): commonly packaged in security-focused distros; see public project docs  
- SafeDeposit whistleblower guide (protect limits): https://safedepositbox.org/ (public education pages)

Never treat "metadata stripped" as proof of safety.

### 5) Receipt handling without cloud screenshot backups

- If the path gives a receipt code, store it in a place that will **not** auto-sync to personal cloud photo backup if that sync re-identifies you.  
- Prefer writing the code on paper offline, or a dedicated notes channel the desk already agreed on.  
- Do not post receipt codes to social media or group chats.  
- Screenshots of success pages can leak timestamps, browser chrome, or account UI; avoid unless the desk requires one and you accept the risk.

### 6) When to stop: personal safety first

Stop and reassess if:

- You are being watched, coerced, or threatened  
- Device seizure is imminent  
- You are unsure whether disclosure is lawful in your jurisdiction  
- The only path offered pressures you to skip verification or install untrusted software  

Personal safety, legal counsel where appropriate, and trusted human advice beat any kit.

## Risk-context callouts

### A) Journalist source

- Desk may have a published SecureDrop, Signal desk line, or sealed browser drop. Prefer paths the outlet documents publicly.  
- Multi-channel **key verification** matters before high-risk encrypt-and-send (see companion playbook in this project).  
- Do not assume a byline later equals protection of your identity.

### B) Institutional insider (education for lawful channels)

- Many employers and agencies publish official hotlines. Those paths often **require identity** and are not technical anonymity tools.  
- If using an independent education path about sealed tips, still separate personal and tip sessions.  
- Company devices and networks often log heavily; personal/home network risk models differ.

### C) High-risk regulated employee education

- Finance, healthcare, defense-adjacent, and similar roles may have strict disclosure laws **and** retaliation risk. This pack does not interpret those laws.  
- Technical OPSEC does not override statutes. When in doubt, seek qualified counsel or a reputable legal clinic.  
- Prefer documented protect / do-not-protect cards from the desk; if none exist, treat claims of "perfect anonymity" as a red flag.

## Protect limits (explicit)

This education may help reduce **some** technical mistakes. It does **not** protect against:

- Compelled disclosure under lawful process  
- Malware already on your device  
- Physical surveillance or coercion  
- Human error after deposit (re-using identifying accounts)  
- Desk-side operational failure or compromise  
- Traffic analysis by a global passive adversary in all scenarios  

## Do-not list

Do **not**:

1. Install random "secure drop" apps from unofficial stores  
2. Send tips from a work laptop while logged into work accounts  
3. Reuse the same cover story phrasing across public and private channels if uniqueness is a risk  
4. Photograph documents under lighting that shows reflective badges or nameplates if avoidable  
5. Ask agents or strangers for help building malware or bypassing access controls  
6. Confuse Tor with "invisible forever"  
7. Treat warrant canaries or marketing copy as courtroom proof  

## Quiz (5+ questions) + answer key

### Q1
Why prefer a separate browser profile or Tor/Tails for a high-risk tip session?

**A)** It looks cooler  
**B)** It reduces accidental reuse of personal logins and session identifiers in the tip path  
**C)** It guarantees anonymity  
**D)** It disables all laws  

**Answer:** B

### Q2
True or false: stripping EXIF from an image guarantees the file cannot identify you.

**Answer:** False. Filenames, remaining metadata, document properties, and network path can still leak. Offline sanitization is stronger but still not perfect.

### Q3
Which is a dual-use refusal this pack requires?

**A)** Teaching Tor Browser download from torproject.org  
**B)** Explaining that SecureDrop and independent sealed drops are different products  
**C)** Writing malware to steal credentials "for research" without authorization  
**D)** Publishing a protect / do-not-protect card  

**Answer:** C (refuse)

### Q4
A site pressures you to skip multi-channel key verification because "time is critical." What is the safer educational response?

**A)** Skip verify always  
**B)** Treat pressure to skip verify as a phishing red flag; verify fingerprint across independent channels first when risk is high  
**C)** Post the key on social media for crowdsourcing  
**D)** Email the private key to yourself  

**Answer:** B

### Q5
Where should you generally get Tor Browser?

**A)** Random mirror tweeted by a stranger  
**B)** Official Tor Project site (torproject.org) with integrity checks as documented there  
**C)** A cracked software forum  
**D)** A lookalike domain one letter off  

**Answer:** B

### Q6
When should you stop the tip process entirely?

**A)** Never  
**B)** When personal safety is at risk, seizure is imminent, or legality is unclear without counsel  
**C)** Only after three successful quizzes  
**D)** Only on weekends  

**Answer:** B

## Sources (public)

1. Tor Project - download and about Tor Browser: https://www.torproject.org/  
2. Tails - amnesic live system docs: https://tails.net/  
3. SafeDeposit public education / whistleblower guide framing: https://safedepositbox.org/  
4. Freedom of the Press Foundation / SecureDrop project docs (for SecureDrop-specific paths): https://securedrop.org/  
5. EFF surveillance self-defense style public material (general defensive hygiene framing): https://ssd.eff.org/

## Required footer

```text
MIT License. Part of Open Source-Protection Literacy Kits (GrokForge).
Educational OPSEC only. Not legal advice. No anonymity or immunity guarantee.
Dual-use refuse: no malware, no unauthorized access, no civilian surveillance tooling.
Prefer personal safety. Human edit before institutional adoption.
```
