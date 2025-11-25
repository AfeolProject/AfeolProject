
# Security Advisory (Draft)
AFEOL Project – GHSA Security Advisory Template

This template is used for drafting and submitting private security advisories
related to any AFEOL module (Portal / Su6 / SecureGSM / ZX-AE / Docs / Other).

---

## 1. Summary

**Type of issue:**  
(e.g., crypto weakness, DoS vector, privilege escalation, metadata leak)

**Affected modules:**  
(List all affected components or directories)

**Severity:**  
(High / Medium / Low)

**CVE / GHSA ID:**  
(Filled automatically after GitHub review)

---

## 2. Technical Details

Describe the issue clearly and technically:

- What is the exact vulnerability?  
- Under what conditions can it be triggered?  
- Can it be exploited remotely?  
- Does it affect anonymity, metadata integrity, or cryptographic safety?  
- Does it relate to Tor/I2P threat models?

---

## 3. Steps to Reproduce

1.  
2.  
3.  

Include PoC (without sensitive or real user data).

---

## 4. Impact

Describe the potential consequences:

- Data exposure  
- Metadata leakage  
- Cryptographic degradation  
- Loss of anonymity  
- Bypass of ZX-AE or AFEOL Security Standard rules  

---

## 5. Recommended Mitigation

Provide suggestions for fix or workaround.

---

## 6. Encrypted Communication (PGP Required)

All sensitive or high-severity advisories **must** be encrypted.

📌 **Public PGP key:**  
https://raw.githubusercontent.com/AfeolProject/AfeolProject/main/.well-known/pgp.asc

📌 **Fingerprint:**  
`6E09 8D86 93AE 0C54 C8F6 B66E F5C2 91C5 1ADB E07F`

📌 **Alternative reference:**  
security.txt → Encryption:  
https://raw.githubusercontent.com/AfeolProject/AfeolProject/main/.well-known/security.txt

---

## 7. Optional Credits (Alias Allowed)

If you want acknowledgment:

Researcher: [alias / anonymous]

---

## 8. Contact for Maintainers

Secure reporting: **afeol@proton.me**  
Tor/I2P communication encouraged.  
