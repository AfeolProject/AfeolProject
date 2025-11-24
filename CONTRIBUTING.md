
# AFEOL Project – Contribution Guidelines

Thank you for your interest in contributing to the AFEOL Project.  
This document defines clear, structured, and security-focused rules for all contributions.

---

## 1. General Principles

- All contributions must uphold privacy, anonymity, and security.  
- No code or content may introduce telemetry, tracking, data collection, or hidden analytics.  
- All contributions follow the MIT License (see **LICENSE**).  
- Contributors must follow the **AFEOL Coding Standard** and **AFEOL Documentation Standard**.  
- English is **mandatory** for all contributions.  
- Additional languages (e.g., Serbian Cyrillic) are **optional** and may be included when appropriate.

---

## 2. Code Requirements

### Allowed Languages
- Rust  
- Kotlin  
- Bash  
- Python  
- PHP  
- HTML (**inline CSS only**)

❌ JavaScript is not allowed (except minimal Node.js tooling outside production use).

### Style Rules
- UTF-8 encoding only  
- All comments **must be written in English**  
- Mandatory AFEOL comment structure:


- Clean, minimal, readable code  
- No unused dependencies  

### Security Rules
- No external CDNs (fonts, styles, JS, analytics)  
- No external trackers or third-party data collectors  
- No cloud-based dependencies unless explicitly approved  
- Cryptographic components must follow **ZX-AE v1.0+** specifications  
- Network-related code must preserve anonymity (Tor/I2P compatible)

---

## 3. Pull Request Rules

Before opening a PR, ensure:

- The project builds without warnings or errors  
- Changes are grouped into meaningful commits  
- Documentation updates follow the AFEOL Documentation Standard  
- English is primary; additional translations are optional  
- Your PR does not violate AFEOL privacy/security requirements  

Each PR must include:

1. Clear description of the change  
2. Motivation behind the change  
3. Security considerations  
4. Testing explanation  
5. Whether any AFEOL standards are affected  

---

## 4. Documentation Rules

All documentation **must** comply with the AFEOL Documentation Standard:

- **Primary language: English**  
- Optional secondary language: Serbian (ћирилица) or others  
- UTF-8 encoding  
- MIT license header included  
- File naming pattern:


- Text must be concise, technically accurate, and consistent  
- Bilingual sections must be placed English → optional secondary language  

---

## 5. Forbidden Contributions

The following are **not permitted**:

- Proprietary or closed-source components  
- JavaScript files (except limited tooling outside production)  
- Google/Facebook trackers, analytics, browser fingerprinting  
- Cloud services requiring identity or tracking  
- AI-generated code without manual human review  
- Any code weakening anonymity, encryption, or metadata protection  

---

## 6. Communication

For questions, suggestions, or communication with project maintainers:

📩 **Official contact:**  
**afeol@proton.me**

This is the only authorized and privacy-respecting communication channel for the project.

---

## 7. AFEOL Security Notice

All contributors acknowledge:

- The project is strictly **privacy-oriented**, **defensive**, and **research-focused**  
- Contributions must not promote or enable illegal activity  
- Responsible disclosure procedures must be followed  
- All security contributions must align with **Tor/I2P threat models**

---

## 8. Submission Process

1. Fork this repository  
2. Create a feature branch  
3. Commit changes using clear, descriptive messages  
4. Push the branch to your fork  
5. Open a pull request  
6. Wait for review  

Pull requests that meet AFEOL’s strict privacy and security requirements will be merged.

---
