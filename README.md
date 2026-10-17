# NetAST

> **Audit locally. See clearly.** 

NetAST is an independent, client-side network configuration assurance engine designed for high-security environments. It evaluates configuration files against a comprehensive rule catalog entirely within your browser, ensuring your corporate data, topology, and secrets never leave your local machine.

## 🌟 Key Features

- 🔒 **Private by Design:** Deterministic scans run purely in-browser using Web Workers. Configurations are never uploaded, sent to a backend, or saved to local storage.
- 📐 **True Effective-Policy Engine:** Converts text into a structured Abstract Syntax Tree (AST) to evaluate actual device state (e.g., ignoring unapplied ACLs or shutdown interfaces).
- 🧬 **Broad Vendor Support:** Deep parsing and heuristic tokenization across 14 vendor families including Cisco (IOS, ASA, FTD, NX-OS), FortiOS, PAN-OS, Junos, TMOS, Gaia, and more.
- ⚖️ **Change Window Comparison:** Pinpoint introduced or mitigated risks by analyzing "before" and "after" configurations side-by-side locally.
- 🗃️ **Offline Vulnerability Overlay:** Offline CVE matching utilizing integrated NVD CVE and CISA KEV catalogs updated through October 2026.
- 📋 **Compliance at a Click:** One-click generation of audit reports for **PCI DSS 4.0**, **NIST 800-53 r5**, **ISO 27001:2022**, **CIS Controls v8**, and **DISA STIG**.

## 🛠️ Security & Air-Gap Compliance

NetAST features a strict **Content-Security-Policy (CSP)** that forbids all network APIs (`fetch`, `XHR`, `WebSocket`, beacons, form posts). It is fully functional in strict air-gapped environments.

### Running the Egress Self-Test
After deploying the application on a target terminal:
1. Navigate to **Local Settings**.
2. Click **Run egress self-test**.
3. Screenshot the resulting browser network block message as compliance evidence of total isolation.

## 🚀 Getting Started

### Installation / Deployment
Since NetAST has no backend, deployment is as simple as hosting static assets or opening the application locally.

1. Clone the repository:
   ```bash
   git clone https://github.com
   ```
2. Open `NetAst.html` in an enterprise-secured, sandboxed browser profile.

### Configuration Analysis
1. Go to the **Configuration Workspace**.
2. Drop or paste your UTF-8 text CLI exports or PAN-OS XML files (Supports up to 50 GiB files via disk streaming).
3. Click **Run audit** to view effective findings instantly.

## 🤝 Custom Rules
Extend the engine by adding structural blocks or regex checks via the **Rule Catalog** interface. You can backup your setup, triage choices, and custom logic securely using the built-in **AES-256-GCM encrypted backup** utility.

---
*Disclaimer: NetAST is an independent pattern-audit implementation and is not affiliated with any hardware vendor or commercial audit entity.*
