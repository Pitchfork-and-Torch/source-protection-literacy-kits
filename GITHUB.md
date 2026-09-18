# GitHub-ready package

This ZIP is ready to push as a public repository that credits GrokForge and all contributors.

## Recommended metadata

- **Owner / org:** `Pitchfork-and-Torch` (or your own account)
- **Repo name:** `open-source-protection-literacy-kits-for-newsrooms-and-ngos`
- **Website / homepage:** https://grokforge.app/projects/open-source-protection-literacy-kits-for-newsrooms-and-ngos/ship
- **Topics:** `grokforge`, `forged-on-grokforge`, `public-goods`, `open-source`
- **Description:** Forged on GrokForge: Open Source-Protection Literacy Kits for Newsrooms and NGOs (v1.0.0)

## Manual publish (any creator)

```bash
unzip open-source-protection-literacy-kits-for-newsrooms-and-ngos-*.zip -d open-source-protection-literacy-kits-for-newsrooms-and-ngos
cd open-source-protection-literacy-kits-for-newsrooms-and-ngos
git init
git add .
git commit -m "feat: sealed package from GrokForge"
# create empty public repo on GitHub, then:
git branch -M main
git remote add origin https://github.com/YOUR_ORG/open-source-protection-literacy-kits-for-newsrooms-and-ngos.git
git push -u origin main
```

Then set the repo **Website** field to the ship page and add topics above.

## Platform publish (founder/admin)

When `GITHUB_PUBLISH_TOKEN` is configured on GrokForge, founder/admin can
**Ship to GitHub** from the sealed ship page. That path creates/updates the org
repo, sets homepage + topics, and records a public ledger event.

## Required credits

Keep README.md, CONTRIBUTORS.md, LICENSE, and NOTICE. Do not strip "Forged on GrokForge".

Ship page: https://grokforge.app/projects/open-source-protection-literacy-kits-for-newsrooms-and-ngos/ship
