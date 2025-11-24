# AFEOL Project – Security Policy

The AFEOL Project is built on strict privacy, cryptographic integrity, and anonymous-first design.  
All contributors, maintainers, and researchers must follow the rules defined below.

---

## 1. Supported Versions

Only the **latest main branch** is officially supported.

Security patches are accepted **exclusively** for:
- Production-ready code inside `main`
- Active specifications (ZX-AE v1.0+, AFEOL Security Standard v1.0, AFEOL Cloud Encryption Specification v1.0)

Legacy branches or experimental drafts do **not** receive security fixes.

---

## 2. Reporting a Vulnerability

If you discover a vulnerability, weakness, or behavior that may reduce privacy, anonymity, or cryptographic safety:

📩 **Report immediately and privately:**  
**afeol@proton.me**

Rules for responsible disclosure:
- Do **not** publish, discuss, or share the vulnerability publicly.
- Provide a minimal, actionable description (steps, expected behavior, actual behavior).
- If possible, include a PoC that does **not** compromise real user data.
- Maintainers will confirm receipt within **72 hours**.
- A fix or mitigation will be proposed within **7–14 days** depending on severity.

Anonymous reporting is welcome (Tor/I2P recommended).

---

## 3. Scope of Security Considerations

The following areas are considered critical:

### 🔐 3.1. Cryptography
- All encryption must follow **ZX-AE v1.0+** standards.
- No custom crypto unless part of an approved AFEOL specification.
- No insecure primitives (e.g., PBKDF2 with low rounds, SHA-1, ECB mode, etc.).
- Key-handling must avoid metadata leaks and timing channels.

### 🛡️ 3.2. Privacy & Metadata Protection
- No logs exposing IP, device IDs, session identifiers, or analytics.
- No telemetry, crash reporting, cloud tracking, or CDN-based resources.
- All network code must be compatible with **Tor** and **I2P**.
- Metadata must be minimized or fully stripped whenever possible.

### 🧩 3.3. Code Security
- No external CDNs (fonts, CSS, JS, analytics).
- Only local, auditable dependencies are allowed.
- JavaScript is prohibited in production interfaces (I2P/Tor compatible rule).
- Client-side code must not leak timing, rendering, or fingerprint data.

### 🔒 3.4. Infrastructure & Deployment
- No dependency on cloud identity services (Google, AWS Cognito, Microsoft, etc.).
- All optional server components must be deployable on isolated Linux environments.
- Admin systems follow mandatory **key rotation every 12 months**, per AFEOL Global Security Standard v1.0.

---

## 4. Responsible Disclosure Rules

Your report must:
- Respect privacy and not endanger real users.
- Limit PoC data to synthetic or random information.
- Avoid exploiting the vulnerability against live systems.
- Follow AFEOL’s defensive, research-oriented mission.

Maintainers may request additional clarifications if needed.

---

## 5. Non-Acceptable Security Reports

The following are **not** considered valid vulnerabilities:

❌ Bug reports involving:
- Browser extensions or third-party plugins
- OS-level malware or compromised systems
- User-side misconfiguration unrelated to AFEOL code

❌ Reports about:
- “Missing features”
- Personal preference complaints
- Expected behavior of Tor/I2P networks (latency, instability, etc.)

Only actionable, security-relevant submissions will be processed.

---

## 6. Security Philosophy

All contributors acknowledge:

- The project is **strictly privacy-oriented, defensive, and research-focused**.
- Contributions must **not** promote, encourage, or enable illegal activity.
- AFEOL software is designed with **Tor/I2P threat models** in mind.
- All components must reduce attack surface, metadata, traffic correlation, and fingerprintability.
- Local-first, offline-friendly design is preferred over cloud dependence.

---

## 7. Commitment to the Community

We aim to:
- Provide transparent, open-source, verifiable security
- Maintain documentation for every cryptographic and security-relevant decision
- Ensure long-term compatibility with anonymity networks
- Deliver stable, privacy-respecting tools for researchers, journalists, activists, and everyday users

---

## 8. Contact

📩 **Official Security Contact:**  
**afeol@proton.me**

This is the only authorized and privacy-respecting communication channel for security reporting.

