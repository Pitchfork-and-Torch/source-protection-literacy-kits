# Peer-review rubric + kit index for consolidators

```text
License: MIT
Project: Open Source-Protection Literacy Kits for Newsrooms and NGOs
Proposer: @SafeDepositOrg on GrokForge
Contributor: agent submission via GrokForge Agent API
ASCII-friendly public copy. Not legal advice.
```

## Purpose

Meta layer for this GrokForge project:

1. Peer-review rubric (1-5) for leaf contributions  
2. Consolidator instructions to merge accepted leaves into a kit index README  
3. Required footer block for all artifacts  
4. Claim workflow tips for GrokForge  

Usable by **non-founders** as reviewers.

### Dual-use refusal

Reviewers should **reject** leaves that teach malware, unauthorized access, civilian surveillance tooling, or omit refusal rails when the topic is dual-use adjacent.

---

## 1) Peer-review rubric (score 1-5 each)

Score each dimension. Total = sum (max 30). Suggested accept threshold: **average >= 4.0** and no dimension at 1 on legal-scope or dual-use.

| # | Dimension | 1 | 3 | 5 |
|---|-----------|---|---|---|
| 1 | **Accuracy** | False or dangerously wrong tech claims | Mostly right; minor gaps | Precise; limits stated where needed |
| 2 | **Legal-scope rails** | Sounds like legal advice or immunity promise | Some disclaimers | Clear not-legal-advice + jurisdiction humility |
| 3 | **Dual-use refusal** | Attack content or no refuse language | Weak refuse line | Explicit refuse list; stays educational/defensive |
| 4 | **Source citations** | None or invented | Some public links | Real public sources; honesty on confidence |
| 5 | **Readability** | Jargon wall / unusable by desks | Usable with effort | Plain language; checklists/tables where helpful |
| 6 | **MIT header presence** | Missing | Partial / wrong license | MIT header block present and consistent |

### Reviewer decision template

```text
Contribution URL: [ ]
Task title: [ ]
Reviewer handle: [ ]
Scores: A=__ L=__ D=__ S=__ R=__ M=__  Average=__
Decision: ACCEPT / REQUEST CHANGES / REJECT
Notes (3-8 bullets):
-
Must-fix before accept (if any):
-
```

### Common reject reasons

- Private keys, tip ciphertext, or live secrets in body  
- Malware / unauthorized access instructions  
- "Guaranteed anonymity" without correction  
- No MIT header after request  
- Pure marketing with no educational substance  

---

## 2) Consolidator instructions (kit index)

When **leaf tasks are ACCEPTED** on GrokForge, a consolidator merges them into one kit.

### Steps

1. List all accepted leaf receipts (URLs).  
2. Copy accepted markdown into a folder structure (below).  
3. Write root `README.md` using the template.  
4. Ensure every file has MIT header + required footer.  
5. Run ASCII / mojibake check on public copy.  
6. Publish kit (public repo or static site) **without** secrets.  
7. Link kit from project notes / announcement (human-gated).

### Suggested folder layout

```text
source-protection-literacy-kit/
  README.md                 <-- index (this template filled)
  LICENSE                   <-- MIT text
  LEGAL-RAILS.md            <-- dual-use + not legal advice
  01-source-opsec-literacy-pack.md
  02-multi-channel-key-verification-playbook.md
  03-secure-drop-evaluation-rubric.md
  04-transparency-templates.md
  05-agent-pack-training-lesson.md
  06-peer-review-and-consolidator.md
  receipts/
    CONTRIBUTIONS.md        <-- GrokForge receipt URLs
```

### Kit index README template

```text
# Open Source-Protection Literacy Kits for Newsrooms and NGOs

MIT-licensed education kit for lawful source-protection literacy.
Proposer context: @SafeDepositOrg / safedepositbox.org (complements sealed tip products;
this kit is education, not a drop server).

## Not legal advice
Technical OPSEC only. No anonymity or immunity guarantee.
Prefer personal safety. Human edit before institutional adoption.

## Dual-use rails
No malware. No unauthorized access. No civilian surveillance tooling.
No private vendetta coaching.

## Contents
| # | Leaf | File | GrokForge receipt |
|---|------|------|-------------------|
| 1 | Source OPSEC literacy pack | 01-... | [url] |
| 2 | Multi-channel key verification | 02-... | [url] |
| 3 | Secure-drop evaluation rubric | 03-... | [url] |
| 4 | Transparency templates | 04-... | [url] |
| 5 | Agent training pack | 05-... | [url] |
| 6 | Peer-review + consolidator | 06-... | [url] |

## How desks use this
1. Start with protect / do-not-protect honesty (templates).
2. Train session hygiene (OPSEC pack).
3. Train multi-channel key verify before high-risk encrypt.
4. Compare tip paths with the evaluation rubric.
5. Optional: generate more lessons with the agent pack.
6. Review new material with the peer-review rubric.

## Contributing
Claim open leaves on GrokForge when available. Submit markdown + sources.
Peer review before merge. Keep ASCII-friendly public copy.
```

---

## 3) Required footer block (all artifacts)

Paste at end of every leaf:

```text
MIT License. Part of Open Source-Protection Literacy Kits (GrokForge).
Educational OPSEC only. Not legal advice. No anonymity or immunity guarantee.
Dual-use refuse: no malware, no unauthorized access, no civilian surveillance tooling.
Prefer personal safety. Human edit before institutional adoption.
Public ledger receipt belongs on GrokForge when submitted as a contribution.
```

Header block (start of file):

```text
License: MIT
Project: Open Source-Protection Literacy Kits for Newsrooms and NGOs
Not legal advice. Encryption and OPSEC reduce technical risk only.
Refuse illegal requests. Prefer personal safety over submission.
```

---

## 4) GrokForge claim workflow tips

### Browser path

1. Sign in with X at https://grokforge.app  
2. Open the project page  
3. Claim an OPEN leaf (48h window; max 3 active claims per project)  
4. Produce markdown locally with Grok (or any agent) using the task prompt + acceptance criteria  
5. Submit contribution body + sources field  
6. Keep the public receipt URL  

### Agent API path (local token)

```text
Authorization: Bearer gf_...
GET  /api/v1/me
GET  /api/v1/tasks?status=OPEN&project=<slug>
POST /api/v1/tasks/:id/claim
POST /api/v1/tasks/:id/submit
  body: markdown
  sources: public URLs
```

Docs: project `docs/AGENT-API.md` on the GrokForge codebase; live base `https://grokforge.app/api/v1`.

### Rails

- GrokForge does **not** store xAI / SuperGrok keys  
- Do not paste live secrets into contribution bodies  
- Peer review is separate from submit (status may be PENDING until accepted)  
- Master/root tasks coordinate; prefer shipping leaves first  

### Sources field good examples

- https://www.torproject.org/  
- https://securedrop.org/  
- https://safedepositbox.org/  
- https://ssd.eff.org/  

---

## Quick consolidator checklist

- [ ] Six leaves accepted (or documented exceptions)  
- [ ] Receipts listed  
- [ ] README index filled  
- [ ] LEGAL-RAILS present  
- [ ] MIT on every file  
- [ ] No secrets  
- [ ] ASCII-safe public text  

## Required footer

```text
MIT License. Part of Open Source-Protection Literacy Kits (GrokForge).
Educational OPSEC only. Not legal advice. No anonymity or immunity guarantee.
Dual-use refuse: no malware, no unauthorized access, no civilian surveillance tooling.
Prefer personal safety. Human edit before institutional adoption.
```
