# AFEOL GitHub Security Hardening Checklist v1.0

This document defines the recommended security configuration for all AFEOL GitHub
repositories, with a focus on the main `AfeolProject/AfeolProject` repository.

It is intended for the maintainer and trusted collaborators only.

---

## 0. Scope & Assumptions

- Scope: all repositories under the AFEOL namespace (org or user account).
- Goal: reduce risk of account takeover, malicious commits and secret leakage.
- Principle: minimal access, explicit trust, auditable changes.

---

## A) Organization / Account Security

### A.1 Two-Factor Authentication (2FA)

- [ ] Require 2FA for all members/collaborators

**How to:**

1. Open **Settings → Organization settings / Account settings**  
2. Enable **Require two-factor authentication for everyone**  
3. Remove users without 2FA or downgrade their access

---

### A.2 Member & Team Management

- [ ] Review members at least every 6 months  
- [ ] Use least-privilege roles (Read / Triage / Maintain / Admin)  
- [ ] Remove inactive collaborators

**How to:**

1. **Settings → Manage access / People**  
2. For each member, verify role and activity  
3. Remove or downgrade unused / unknown accounts

---

### A.3 Third-Party Access

- [ ] Audit OAuth apps and GitHub Apps every 6 months  
- [ ] Remove apps that are not strictly needed

**How to:**

1. **Settings → Applications / Installed GitHub Apps / OAuth Apps**  
2. Revoke any app that is not clearly required for AFEOL

---

## B) Repository Security Settings

Apply this to each security-relevant repository (mandatory for `AfeolProject/AfeolProject`).

### B.1 Secret Scanning & Code Scanning

- [ ] Enable **Secret scanning alerts**  
- [ ] Enable **Push protection** (prevent pushing secrets)  
- [ ] Enable **Code scanning** with CodeQL (default workflow is enough)

**How to:**

1. Open **Security → Code scanning** and configure CodeQL  
2. Open **Security → Secret scanning** and enable alerts + push protection  

---

### B.2 Dependabot & Vulnerability Alerts

- [ ] Enable **Dependabot security updates**  
- [ ] Enable **Dependency graph** & **Dependabot alerts**

**How to:**

1. **Settings → Code security and analysis**  
2. Turn on:
   - Dependency graph  
   - Dependabot alerts  
   - Dependabot security updates  

---

### B.3 GitHub Actions

- [ ] If Actions are **NOT** used → disable them  
- [ ] If Actions are used → restrict to:
  - Only `Allow GitHub Actions, and select: Allow actions created by GitHub`  
  - Explicitly approved third-party workflows only

**How to:**

1. **Settings → Actions → General**  
2. Choose appropriate policy (Disabled or Restricted)

---

## C) Branch Protection for `main`

Branch protection is **mandatory** for `main`.

Recommended rule:

- [ ] Protect branch: `main`  
- [ ] Require pull request before merging  
- [ ] Require at least **1** approving review  
- [ ] Dismiss stale approvals when new commits are pushed  
- [ ] Require status checks to pass before merging (if CI exists)  
- [ ] Require branches to be up to date before merging (if CI/state matters)  
- [ ] Do not allow force pushes  
- [ ] Do not allow branch deletion  
- [ ] Require signed commits (see section D)

**How to:**

1. **Settings → Branches → Branch protection rules → Add rule**  
2. Branch name pattern: `main`  
3. Enable the options above and save

---

## D) Commit Signing Policy

Prefer signed commits for all protected branches.

- [ ] Generate GPG or SSH signing key for the maintainer  
- [ ] Configure Git to sign commits by default  
- [ ] Enable **“Require signed commits”** in branch protection for `main`

**How to:**

1. Create a signing key (GPG or SSH) on your machine  
2. Add the public key to GitHub (**Settings → SSH and GPG keys**)  
3. `git config commit.gpgsign true` (or equivalent SSH signing config)  
4. In branch protection for `main`, enable **Require signed commits**

---

## E) Repository Hygiene

For each repo:

- [ ] `LICENSE` present and correct  
- [ ] `README.md` explains purpose and security expectations  
- [ ] `SECURITY.md` present (root)  
- [ ] `.well-known/security.txt` present (if public-facing project)  
- [ ] `.well-known/pgp.asc` present and up to date  
- [ ] `CODE_OF_CONDUCT.md` present  
- [ ] `CONTRIBUTING.md` present  
- [ ] `SUPPORT.md` present (where to ask for help)

AFEOL main repo status (target):

- [x] LICENSE  
- [x] README.md  
- [x] SECURITY.md  
- [x] .well-known/security.txt  
- [x] .well-known/pgp.asc  
- [x] CODE_OF_CONDUCT.md  
- [x] CONTRIBUTING.md  
- [x] SUPPORT.md  

---

## F) Incident Response (Security Events)

- [ ] `SECURITY_ADVISORY_TEMPLATE.md` configured  
- [ ] `SECURITY_CREDITS.md` configured  
- [ ] Defined process:
  - Private report → Triage → Fix → Advisory → Credits

Operational checklist:

1. When a vulnerability is reported:
   - [ ] Acknowledge within 7 days  
   - [ ] Open a **private** security issue or internal note  
   - [ ] Create a work branch for the fix  
2. After fix:
   - [ ] Release a patched version (tag or release)  
   - [ ] Publish a GitHub Security Advisory (if impact justifies it)  
   - [ ] Update `SECURITY_CREDITS.md` if researcher wants credit  

---

## G) Darknet / Privacy-Specific Notes (AFEOL)

For AFEOL projects that run on Tor/I2P/Freenet:

- [ ] Do not publish real server IPs, hostnames or VPN endpoints in the repo  
- [ ] Do not commit logs, traffic captures or sensitive configs  
- [ ] Keep all production secrets (keys, tokens, passwords) **off GitHub**  
- [ ] Use placeholders and `.example` config files instead of real configs  

Examples:

- Use `config/torrc.example` instead of `torrc` with real onion addresses  
- Use `.env.example` instead of `.env` with real credentials  

---

## H) Minimal Initial Setup Sequence

When creating a new AFEOL repository, perform these steps in order:

1. Add `LICENSE`, `README.md`, `SECURITY.md`  
2. Configure **Secret scanning**, **Dependabot** and **Code scanning**  
3. Protect `main` branch (section C)  
4. Require signed commits (section D)  
5. Enforce 2FA for all collaborators (section A.1)  
6. Review third-party apps and integrations (section A.3)

Once all boxes in sections A–H are checked, the repository is considered
**AFEOL GitHub Security Hardened v1.0**.
