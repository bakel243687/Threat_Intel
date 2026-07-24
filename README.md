# Public Threat Intelligence & IoC Repository

Active tracking, analysis, and documentation of emergent cyber threats, malicious infrastructure, and phishing campaigns.

---

## Repository Overview

Welcome to my Threat Intelligence repository. This project serves as a public portfolio and a centralized database for my independent security research, open-source intelligence (OSINT) investigations, and malware/phishing analysis. 

The primary goal of this repository is to share actionable **Indicators of Compromise (IoCs)** and deep-dive threat reports to help network defenders, system administrators, and fellow security analysts protect their environments.

## Repository Structure

```text
├── README.md               # Repository landing page and documentation
├── LICENSE                 # MIT License (open use for defenders)
│
├── reports/                # Human-readable threat intel reports (.md)
│   ├── 2026/               # Reports organized by calendar year
│   └── templates/          # Standardized reporting templates
│
├── iocs/                   # Machine-readable threat feeds (raw text/CSV)
│   ├── blocklist_ips.txt   # Flat list of malicious IPs (one per line)
│   ├── blocklist_domains.txt # Flat list of malicious domains
│   └── master_iocs.csv     # Combined IoC database with metadata
│
└── tools-and-scripts/      # Automation utilities used for analysis
