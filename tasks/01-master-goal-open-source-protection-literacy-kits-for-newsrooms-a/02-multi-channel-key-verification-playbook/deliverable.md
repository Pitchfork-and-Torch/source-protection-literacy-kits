# Multi-channel key verification playbook

```text
License: MIT
Project: Open Source-Protection Literacy Kits for Newsrooms and NGOs
Proposer: @SafeDepositOrg on GrokForge
Contributor: agent submission via GrokForge Agent API
Not legal advice. Key verification reduces phishing risk; it does not guarantee safety.
No private keys. No deposit ciphertext. Educational only.
```

## Purpose

Teach tipsters and desks how to **verify an operator public-key fingerprint across multiple independent public channels** before a high-risk encrypt-and-send.

If channels disagree, **stop**. Do not encrypt to a key you cannot verify.

### Dual-use refusal

This playbook does **not** cover stealing keys, breaking into accounts, malware, or unauthorized access. It is for verifying **public** operator material that desks already publish.

## Why multi-channel matters

A single webpage can be:

- Phished (lookalike domain)  
- Compromised briefly  
- Served differently to some visitors  
- Spoofed in a screenshot  

Independent channels raise the cost of a consistent lie. They do not make attacks impossible.

## Channels you may use (pick 2+ that the desk actually publishes)

| Channel | Example | Independence tip |
|---------|---------|------------------|
| Product **verify** page | `https://example.org/verify` | Type URL carefully; prefer bookmarks after first good verify |
| Desk **X / social** account | Official handle posts fingerprint or link to verify | Confirm handle spelling and history; beware impostors |
| Public **repo or canary** | GitHub/GitLab release note, signed canary text | Prefer HTTPS org you already trust; check commit/release authenticity habits |
| Out-of-band desk channel | Known newsroom contact path, in-person printout, prior authentic email | Only channels you already trust from offline life |
| Onion verify page | Desk-published onion for key material | Still compare fingerprint string to a second channel |

**Never** accept a key only from:

- A stranger in a DM  
- A URL shortened without expansion  
- A PDF attachment from an unknown sender  
- "Urgent" pressure to skip verify  

## Copy-paste checklist (8 steps)

Use this before high-risk sealing.

```text
[ ] 1. Confirm you are on the correct organization and product (no lookalike domain).
[ ] 2. Open Channel A (e.g. official verify page). Record the full fingerprint string offline.
[ ] 3. Open Channel B (e.g. official X account or public repo) without following untrusted redirects.
[ ] 4. Compare Channel A and Channel B character-for-character (not "looks similar").
[ ] 5. If available, open Channel C (onion, canary, or out-of-band) and compare again.
[ ] 6. Confirm key purpose (encryption for tips vs signing) matches what the desk documents.
[ ] 7. Only then encrypt to that public key using the desk's documented method.
[ ] 8. If any channel mismatches or pressure appears to skip steps: STOP. Do not send.
```

### Comparison technique (non-engineer friendly)

- Copy the fingerprint to a plain text file offline, or write it on paper.  
- Compare in groups of 4 characters.  
- Do not trust OCR of a photo of a fingerprint without a second channel.  
- Upper/lowercase and spaces: follow the desk's published format exactly.

## Phishing red-flag list

Treat these as **stop signals**:

1. **Lookalike domains** (`safedeposltbox.org`, extra hyphens, wrong TLD)  
2. **Mismatched fingerprints** across channels that should agree  
3. **Pressure to skip verify** ("send now or lose the story")  
4. **New social account** claiming to be the desk with zero history  
5. **DM-only keys** with no public verify page  
6. **Shortened links** that land on unexpected hosts  
7. **Slightly wrong handle** (`@SafeDeposit0rg` vs real)  
8. **QR codes** from flyers you cannot independently check  
9. **Requests for your private key** or seed phrase (always refuse)  
10. **"Updated key" with no multi-channel announcement** during an incident  

## Desk operator obligations (publish this)

Desks that ask for high-risk tips should publish:

- A stable **verify** URL  
- Fingerprint in at least **two** independent public places  
- Rotation policy (when keys change, how you announce)  
- Clear language: verification reduces phishing risk; it is not legal advice  

## One-page poster version

Print or pin this. ASCII-friendly.

```text
============================================================
  VERIFY THE KEY BEFORE YOU ENCRYPT (high-risk tips)
============================================================

1. Type the official verify URL yourself (no random DMs).
2. Write down the FULL fingerprint.
3. Check a SECOND independent channel (official social,
   public repo/canary, or trusted out-of-band).
4. Match character-for-character.
5. Mismatch or pressure to skip? STOP. Do not send.
6. Never share your private key. Desks only need public keys.

Phishing red flags: lookalike domains, new impostor accounts,
short links, "urgent skip verify", DM-only keys.

This poster is education, not a safety guarantee.
MIT | Source-Protection Literacy Kits | GrokForge
============================================================
```

## Worked mini-example (fictional)

- Channel A verify page shows fingerprint `AAAA BBBB CCCC ...`  
- Desk X account pins the same string  
- Public canary file matches  

-> Proceed only with the desk's documented encrypt flow.

If X shows `AAAA BBBB DDDD ...` while the site shows `CCCC`:

-> **Stop.** Contact the desk via a pre-existing trusted path or wait for a multi-channel correction. Do not "pick the one that looks more official" under time pressure.

## What this playbook never includes

- Private keys or seed phrases  
- Ciphertext of deposits  
- Instructions to hack phishing sites  
- Malware "to catch phishers"  

## Sources (public concepts)

1. SafeDeposit-class public verify / education pattern: https://safedepositbox.org/  
2. Tor Project (when using onion verify paths): https://www.torproject.org/  
3. SecureDrop operator docs (newsroom onion key practices differ by outlet): https://securedrop.org/  
4. General public-key hygiene: prefer out-of-band confirmation of fingerprints (industry standard practice)

## Required footer

```text
MIT License. Part of Open Source-Protection Literacy Kits (GrokForge).
Educational only. Not legal advice. No anonymity guarantee.
Dual-use refuse: no malware, no unauthorized access, no civilian surveillance tooling.
No private keys in this artifact. Human edit before institutional adoption.
```
