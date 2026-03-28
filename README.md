# Bion Labs — Project Context

## Business Overview
**Bion Labs** is a retail business specializing in peptides and health products.
This repository contains the source code for the Bion Labs MVP website.

---

## Tech Stack

| Layer | Tool | Notes |
|---|---|---|
| Markup & Structure | HTML5 | Plain `.html` files, no framework |
| Styling | Tailwind CSS (CDN) | No build step, linked via `<script>` tag |
| Payments | Stripe Payment Links | No backend required |
| Hosting | Netlify (free tier) | Drag-and-drop or git-based deploy |
| Domain | TBD (Namecheap / Google Domains) | ~$12/year, pointed at Netlify |
| Version Control | Git + GitHub | Managed workflow described below |

---

## Repository Structure (planned)

```
bion-labs/
├── index.html          # Landing page
├── products.html       # Product catalog
├── about.html          # About / contact
├── assets/
│   ├── images/
│   └── icons/
└── README.md           # This file
```

---

## Initial Setup (completed ✓)

- Git installed on owner's machine
- GitHub account: [BionLabs-ltd](https://github.com/BionLabs-ltd)
- SSH key generated (`ed25519`) and added to GitHub
- Repository created: `git@github.com:BionLabs-ltd/bion-labs.git`

To clone a fresh copy of the repo at any time:
```bash
git clone git@github.com:BionLabs-ltd/bion-labs.git
cd bion-labs
```

---

## Deployment (Netlify)

1. Go to https://netlify.com and log in
2. Drag the project folder onto the deploy area, **or** connect the GitHub repo for automatic deploys on every push
3. Set a custom domain once purchased

---

## Collaborators

| Person | Role |
|---|---|
| Eric | Business owner — GitHub: BionLabs-ltd |
| Friend (tech advisor) | Directs features, communicates with Claude on Eric's machine |
| Claude | Writes all code, manages all git operations via CLI |

---

## Development Workflow

Claude handles all code writing and git operations via CLI on Eric's machine. The process for every feature is:

1. **Tech advisor or Eric describes** what they want
2. **Claude builds it** and presents the result
3. **Eric or tech advisor approves** (any positive signal — "looks good", "perfect", "let's go", etc.)
4. **Claude runs CLI git commands** (`git add`, `git commit`, `git push`) to push to the repository

Git operations are always performed via CLI (`git` on Eric's local machine). Claude never relies on the GitHub web interface for version control. Eric never needs to run git commands manually.

---

## Notes & Decisions Log

- **2026-03-28** — Stack decided: plain HTML + Tailwind CDN + Stripe Payment Links + Netlify. Rationale: zero build tooling, Claude can write/edit files directly, owner can deploy by drag-and-drop.
- **2026-03-28** — SSH key setup discussed. Using `ed25519` format.
- **2026-03-28** — Git and GitHub set up. Repo created under BionLabs-ltd org. SSH key (ed25519) in place.
- **2026-03-28** — Claude assigned to manage all git operations. Commits and pushes happen automatically on owner approval — no explicit "push to git" instruction needed.
- **2026-03-28** — Git operations standardized to CLI only (`git add`, `git commit`, `git push` via terminal on Eric's machine). No GitHub web interface for version control.
- **2026-03-28** — Collaborators clarified: Eric is the business owner (GitHub: BionLabs-ltd). Tech advisor (Eric's friend) directs features and communicates with Claude on Eric's machine.
