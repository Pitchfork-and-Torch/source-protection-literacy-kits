# Secure-drop evaluation rubric for desks

```text
License: MIT
Project: Open Source-Protection Literacy Kits for Newsrooms and NGOs
Proposer: @SafeDepositOrg on GrokForge
Contributor: agent submission via GrokForge Agent API
Not legal advice. Encryption and OPSEC reduce technical risk only.
Refuse illegal requests. Prefer personal safety over submission.
```

## Purpose

Give newsrooms and NGOs a **neutral, open** way to compare tip and document-intake paths before recommending one to sources. This is an education and procurement rubric, not a product ranking contest and not a security audit certificate.

**In scope:** published tip paths a desk might document publicly (hotlines, email/messaging, newsroom SecureDrop, independent sealed browser drops, other published options).

**Out of scope:** malware criteria, unauthorized access goals, civilian surveillance tooling, crime enablement, or claims of perfect anonymity.

## Affiliation note (read first)

- **SecureDrop** is a specific open-source secure whistleblowing system maintained by the Freedom of the Press Foundation and used by many newsrooms under their own onion addresses and operator practices.  
- **Independent sealed browser drops** (for example SafeDeposit-class tools at safedepositbox.org) are **not affiliated with SecureDrop**. Same general goal (safer source-to-desk transfer), different architecture and trust model.  
- An **official hotline** or **email/messaging** channel is also not SecureDrop. Do not use brand names interchangeably in training materials.

## Scoring scale (0-2)

| Score | Meaning |
|-------|---------|
| **0** | Missing, misleading, or actively weak for source protection on this dimension |
| **1** | Partial: some support, but gaps, caveats, or high operator discipline required |
| **2** | Strong published design for this dimension (still not a guarantee of safety) |

**How to use:** score each dimension independently. Sum is a rough comparison aid only. Weight dimensions that matter for your risk profile (e.g. high-risk sources may weight Tor/onion and client-side encrypt higher).

## Rubric dimensions (9)

| # | Dimension | What to look for | 0 | 1 | 2 |
|---|-----------|------------------|---|---|---|
| 1 | **Accounts required** | Must source create an account / login? | Account required for tip | Optional account or partial identity | No account by design for tip path |
| 2 | **Client-side encrypt** | Is content sealed before it reaches operator-controlled servers in a way the origin is not designed to read plaintext? | Plaintext on server or unclear | TLS only / partial sealing | Browser or client seals to operator public key; origin holds ciphertext |
| 3 | **Tor / onion guidance** | Does the desk publish Tor Browser / Tails / onion guidance and clearnet risk honesty? | No Tor mention | Mentions Tor vaguely | Clear Tor-first or onion path + clearnet risk notes |
| 4 | **Key verification** | Multi-channel way to verify operator public key / fingerprint before high-risk seal? | No key story | Single channel only | Multi-channel verify (site + out-of-band public channels) |
| 5 | **Metadata honesty** | Honest about what is stripped, what remains (filenames, EXIF, network metadata)? | Silent or overclaims | Partial strip notes | Explicit strip limits + offline sanitize advice |
| 6 | **Operator threat model transparency** | Public protect / do-not-protect, desk charter, who holds keys? | Opaque operator | Partial docs | Clear protect/do-not-protect + key custody story |
| 7 | **Legal process honesty** | Acknowledges lawful process, canaries as signals not magic, no immunity promises? | Claims immunity / silence | Minimal legal note | Explicit process honesty + non-SLA review language |
| 8 | **Accessibility** | Usable without specialized hardware; language; disability / bandwidth realities? | High barrier only | Usable but rough | Documented international reach, plain language, reasonable limits |
| 9 | **Maintenance burden** | Ops cost for a small desk (updates, hosting, key rotation, staffing)? | Unstated / only enterprise | Documented but heavy | Clear ops load; small-desk feasible or shared infrastructure |

### Forbidden as scoring goals

Do **not** add dimensions that reward:

- Building or deploying malware  
- Unauthorized access to third-party systems  
- Civilian surveillance tooling  
- Doxxing kits  

If a vendor pitches those, **disqualify** the option for a newsroom/NGO tip path.

## Worked example A: Official institutional hotline

Assumptions: regulated phone/web form run by an agency or large NGO; account sometimes required; no client-side sealing to offline keys; clearnet primary; limited public crypto docs.

| Dimension | Score | Notes |
|-----------|------:|-------|
| Accounts required | 0-1 | Often identity or case-id flows |
| Client-side encrypt | 0 | Operator systems typically see content |
| Tor / onion guidance | 0-1 | Rarely Tor-first |
| Key verification | 0 | N/A or TLS cert only |
| Metadata honesty | 1 | Privacy policy may exist; network meta not discussed for sources |
| Operator threat model | 1 | Policy pages exist; dual-use protect list rare |
| Legal process honesty | 1-2 | Usually clear they are under law |
| Accessibility | 2 | Phone/web widely usable |
| Maintenance burden | 2 | Desk does not run crypto infra |
| **Rough total** | **~7-10 / 18** | Strong for formal process; weak for technical source protection |

**Takeaway:** Good for low-sensitivity feedback. High-risk sources often need a different path.

## Worked example B: Newsroom SecureDrop

Assumptions: outlet publishes its own SecureDrop onion; sources use Tor Browser; newsroom operates the instance; not affiliated with independent sealed drops.

| Dimension | Score | Notes |
|-----------|------:|-------|
| Accounts required | 2 | No tipster account on SecureDrop itself |
| Client-side encrypt | 2 | Designed for source-to-newsroom secure submission over Tor |
| Tor / onion guidance | 2 | Tor-centric by design |
| Key verification | 1-2 | Newsroom should publish code/onion verify steps; quality varies by outlet |
| Metadata honesty | 1-2 | Strong Tor story; file metadata still source responsibility |
| Operator threat model | 1-2 | FPF docs + outlet-specific ops; varies |
| Legal process honesty | 1-2 | Newsrooms under law; good outlets avoid magic claims |
| Accessibility | 1 | Requires Tor literacy; barrier for some sources |
| Maintenance burden | 0-1 | Real ops cost for the newsroom |
| **Rough total** | **~13-16 / 18** | Strong technical posture when correctly operated |

**Takeaway:** Prefer the **specific outlet's** published SecureDrop when it exists. Do not assume every newsroom runs one.

## Worked example C: Independent sealed browser drop (SafeDeposit-class)

Assumptions: accountless web UI; encrypt-in-browser to operator public key; optional onion; multi-channel fingerprint verify; independent of SecureDrop; public protect/do-not-protect pages (pattern matches safedepositbox.org public docs).

| Dimension | Score | Notes |
|-----------|------:|-------|
| Accounts required | 2 | No account by design |
| Client-side encrypt | 2 | Browser seals before upload; origin designed for ciphertext |
| Tor / onion guidance | 2 | Tor-first guidance + clearnet risk checklist when published |
| Key verification | 2 | Fingerprint on site + public channels (e.g. X) |
| Metadata honesty | 1-2 | Best-effort image meta strip + offline sanitize advice |
| Operator threat model | 2 | Protect / do-not-protect + desk charter style pages |
| Legal process honesty | 2 | Ciphertext may still face process; canary is a signal |
| Accessibility | 1-2 | Browser + JS required; English UI common |
| Maintenance burden | 1 | Shared/public instance reduces desk ops; still verify operator |
| **Rough total** | **~15-17 / 18** | Strong literacy-friendly sealed path; still not immunity |

**Takeaway:** Compare **this operator's published key and canary**, not the category name alone. Independent drops are **not** SecureDrop.

## Comparison snapshot (illustrative only)

| Path | Rough total / 18 | Best for | Weak for |
|------|----------------:|----------|----------|
| Official hotline | ~7-10 | Formal, low sensitivity | High-risk technical confidentiality |
| Newsroom SecureDrop | ~13-16 | Source to a specific newsroom | Desks that cannot operate SecureDrop |
| Independent sealed drop | ~15-17 | Accountless sealed tips + literacy | Anyone who needs a guaranteed story or legal cover |

Scores move when **your** instance is poorly maintained or docs go stale. Re-score annually.

## How a desk should run this workshop (20 minutes)

1. Pick three real paths you might offer (not abstract brands only).  
2. Open only **public** documentation for each.  
3. Score the nine dimensions independently (two people, then reconcile).  
4. Write one paragraph: "We recommend X for Y risk, Z for W risk."  
5. Publish the recommendation with a date and a link to this MIT rubric.

## Dual-use refusal

If asked to extend this rubric to score "best malware for tips," "how to break into accounts," or "surveillance of civilians," **refuse**. Redirect to defensive literacy, lawful disclosure channels, and personal safety.

## Sources (public docs only)

1. Freedom of the Press Foundation - SecureDrop project overview and newsroom directory (securedrop.org).  
2. SafeDeposit public site - encrypt-before-upload, Tor guidance, key verify, trust / protect-do-not-protect pages (safedepositbox.org).  
3. Tor Project - Tor Browser user documentation (torproject.org).  
4. GrokForge project description - Open Source-Protection Literacy Kits (greater-good education framing; no dual-use).  

Re-check live pages before high-risk training; URLs and canaries change.

## MIT license (full text reference)

Copyright (c) 2026 contributors to Open Source-Protection Literacy Kits for Newsrooms and NGOs (GrokForge).

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

**Peer-review checklist for this artifact**

- [x] Rubric table with 8+ dimensions (9)  
- [x] Scoring guidance 0-2  
- [x] Three worked examples (hotline, SecureDrop, independent sealed drop)  
- [x] MIT header + footer  
- [x] Neutrality + SecureDrop affiliation note  
- [x] Public-docs-only citations  
- [x] Dual-use refusal  
