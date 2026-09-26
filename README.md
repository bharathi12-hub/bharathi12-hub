### Bharathithasan S — Security Engineering

BE Computer Science and Engineering (Cyber Security). I build defensive
security tools and test them against the attacks they exist to stop. Looking
for AppSec and security engineering internships and entry-level roles.

**Focus areas:** AppSec, AI/LLM security, applied cryptography, SIEM & log
analysis, static analysis.

**Flagship projects**

- 🛡️ [**AEGIS**](https://github.com/bharathi12-hub/AEGIS-LLM-FIREWALL) — an LLM
  prompt-injection firewall. An OpenAI-compatible gateway that undoes
  homoglyph, zero-width, emoji-tag and base64 obfuscation *before*
  classifying, so character-injection evasion doesn't slip past.
  - On its 30-attack / 30-benign benchmark, a classifier-only baseline lets
    100% of those evasion variants through; AEGIS lets 0% through with no false
    positives. `make bench` regenerates the numbers.
  - I audited my own build and found it inspected only the latest user turn:
    payloads in tool results, system messages and tool descriptions skipped
    every detection layer. Fixed with whole-conversation inspection and
    regression tests
    ([write-up](https://github.com/bharathi12-hub/AEGIS-LLM-FIREWALL/blob/main/docs/HARDENING.md)).
  - 287 tests in [CI](https://github.com/bharathi12-hub/AEGIS-LLM-FIREWALL/actions/workflows/ci.yml);
    findings mapped to OWASP LLM Top 10 and MITRE ATLAS; Kubernetes and Helm
    manifests for deployment.
- 🔐 [**QuantumShield**](https://github.com/bharathi12-hub/QuantumShield) — a
  post-quantum cryptography scanner, co-built with
  [@rohithvenkatesan009-rik](https://github.com/rohithvenkatesan009-rik).
  - Scans 13 languages plus Terraform, Dockerfiles and server configs for
    quantum-vulnerable crypto; Python code gets AST analysis with taint
    tracking from hardcoded secrets to crypto calls.
  - Maps findings to NIST post-quantum replacements (ML-KEM / ML-DSA /
    SLH-DSA, FIPS 203/204/205) and exports SARIF and CycloneDX SBOMs, so
    results plug into existing code-scanning and supply-chain tooling.

**Also built**

- 🌐 [CyberPunk Detection Tool](https://github.com/bharathi12-hub/CyberPunk-Detection-Tool) —
  a Chrome (Manifest V3) extension that combines 12 detection engines
  (phishing and typosquatting, trackers, cookies, security headers,
  fingerprinting, risky downloads) and six threat-intelligence sources into a
  0–100 trust score for each site you visit.
- 🔎 [SSH brute-force detection in Splunk](https://github.com/bharathi12-hub/SSH-Bruteforce-Detection-Splunk) —
  a home SIEM lab: Kali attacks a Metasploitable 2 target, auth logs ship over
  syslog to Splunk, and SPL rules mapped to MITRE ATT&CK T1110 flag the
  failed logins, written up as an incident report.

**Languages & tools:** Python, TypeScript/JavaScript, FastAPI, React,
Node.js/Express, PostgreSQL, Redis, Docker, Kubernetes/Helm, GitHub Actions,
CodeQL, Splunk SPL, Linux.

**Currently exploring:** CTFs, and going deeper into AI/LLM security and
applied cryptography.

📫 [LinkedIn](https://www.linkedin.com/in/bharathithasan-s-115348284)
